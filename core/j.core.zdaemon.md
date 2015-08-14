## j.core.zdaemon

- /opt/jumpscale7/lib/JumpScale/grid/zdaemon/ZDaemonFactory.py

### def getZDaemonClient(addr="127.0.0.1", port=5651, org="myorg", user="root", passwd="1234", ssl=False, category="core",\ (l40)

example usage, see example for server at self.getZDaemon

client=j.core.zdaemon.getZDaemonClient(ipaddr="127.0.0.1",port=5651,login="root",passwd="1234",ssl=False)

        print client.echo("Hello World.")

### def getZDaemon(port=4444, name="", nrCmdGreenlets=50, sslorg="", ssluser="", sslkeyvaluestor=None) (l9)

is a generic usable zmq daemon which has a data & cmd channel (data channel not completely implemented for now)

zd=j.core.zdaemon.getZDaemon(port=5651,nrCmdGreenlets=50)

class MyCommands():
    def __init__(self,daemon):
        self.daemon=daemon

    def pingcmd(self,session=None):
        return "pong"

    def echo(self,msg="",session=None):
        return msg

#remark always need to add **args in method because user & returnformat are passed as params which can 
  be used in method

zd.addCMDsInterface(MyCommands)  #pass as class not as object !!!
zd.start()

use self.getZDaemonClientClass as client to this daemon

### def getZDaemonHAClient(connections=None, org="myorg", user="root", passwd="1234", ssl=False, category="core",\ (l56)

example usage, see example for server at self.getZDaemon

client=j.core.zdaemon.getZDaemonHAClient([('127.0.0.1', 5544)],login="root",passwd="1234",ssl=False)

        print client.echo("Hello World.")

### def getZDaemonTransportClass() (l71)

#example usage:
import JumpScale.grid.zdaemon
class BlobStorTransport(j.core.zdaemon.getZDaemonTransportClass()):
    def sendMsg(self,timeout=0, *args):
        self._cmdchannel.send_multipart(args)
        result=self._cmdchannel.recv_multipart()
        return result
transp=BlobStorTransport(addr=ipaddr,port=port,gevent=True)

### def initSSL4Server(organization, serveruser, sslkeyvaluestor=None) (l102)

use this to init your ssl keys for the server (they can be used over all transports)

### def getZDaemonAgent(ipaddr="127.0.0.1", port=5651, org="myorg", user="root", passwd="1234", ssl=False, reset=False, roles=[]) (l86)

example usage, see example for server at self.getZDaemon

agent=j.core.zdaemon.getZDaemonAgent(ipaddr="127.0.0.1",port=5651,login="root",passwd="1234",ssl=False,roles=["*"])
agent.start()

@param roles describes which roles the agent can execute e.g. node.1,hypervisor.virtualbox.1,*
    * means all
