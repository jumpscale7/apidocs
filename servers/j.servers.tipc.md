## j.servers.tipc

- /opt/jumpscale7/lib/JumpScale/grid/tipc/TipcFactory.py

### def getClient(servaddr, category="core", org="myorg", user="root", passwd="passwd", ssl=False, roles=[]) (l30)

### def getServer(servaddr, sslorg=None, ssluser=None, sslkeyvaluestor=None) (l6)

HOW TO USE:
daemon=j.servers.tornado.getServer(port=4444)

class MyCommands():
    def __init__(self,daemon):
        self.daemon=daemon

    #session always needs to be there
    def pingcmd(self,session=session):
        return "pong"

    def echo(self,msg="",session=session):
        return msg

daemon.addCMDsInterface(MyCommands,category="optional")  #pass as class not as object !!! chose category if only 1 then can leave ""

daemon.start()
