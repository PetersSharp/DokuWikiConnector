# DokuWikiConnector
[![Release](https://img.shields.io/github/release/PetersSharp/DokuWikiConnector.svg?style=flat)](https://github.com/PetersSharp/DokuWikiConnector/releases/latest)
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
using stDokuWikiConnector.Data;

    RpcXml xml = new RpcXml("http://you-dokuwiki-url.org/", "userquest", "userquest");
    XMLMethodPageList dokuList = xml.DokuPageList("wiki:") as XMLMethodPageList;
    foreach (var items in dokuList.Params.Param.Value.Array.Data.Value)
    {
        foreach (var item in items.Struct.Member)
        {
            Console.WriteLine(
              item.Name +
              ((string.IsNullOrWhiteSpace(item.Value.Int)) ? " " : " [" + item.Value.Int + "] ") +
              ((string.IsNullOrWhiteSpace(item.Value.String)) ? "" : item.Value.String)
            );
        }
    }

```


