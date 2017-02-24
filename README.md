# DokuWikiConnector
[![Release](https://img.shields.io/github/release/PetersSharp/stCoCServer.svg?style=flat)](https://github.com/PetersSharp/stCoCServer/releases/latest)
[![Issues](https://img.shields.io/github/issues/PetersSharp/stCoCServer.svg?style=flat)](https://github.com/PetersSharp/stCoCServer/issues)
[![License](http://img.shields.io/:license-mit-blue.svg)](https://github.com/PetersSharp/stCoCServer/blob/master/LICENSE)

####.NET RPC-XML DokuWiki Connector API

 this part of stCoCServer, see [stCoCServer](https://github.com/PetersSharp/stCoCServer)
* DokuWikiConnector [source](https://github.com/PetersSharp/stCoCServer/tree/master/stCoCServer/stExtLib/stDokuWikiConnector-dll)
* DokuWikiConnector [Test suite](https://github.com/PetersSharp/stCoCServer/tree/master/stCoCServer/stTest/TestDokuWikiConnector)
* DokuWikiConnector [Method Documentation](https://github.com/PetersSharp/stCoCServer/tree/master/stCoCServer/stExtLib/stDokuWikiConnector-dll/Doc)

####Example use:

```csharp

using stDokuWikiConnector;

    xml = new RpcXml(TestProgram.dkwUrl, "clanquest", "clanquest");
    var dokuList = xml.DokuPageList("wiki:") as stDokuWikiConnector.Data.XMLMethodPageList;
    foreach (var items in dokuList.Params.Param.Value.Array)
    {
        // ...
    }
```


