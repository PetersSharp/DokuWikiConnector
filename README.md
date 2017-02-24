# DocuWikiConnector
.NET DocuWiki Connector API
see [stCoCServer](https://github.com/PetersSharp/stCoCServer)

DocuWikiConnector [source](https://github.com/PetersSharp/stCoCServer/tree/master/stCoCServer/stExtLib/stDokuWikiConnector-dll)

DocuWikiConnector [Test suite](https://github.com/PetersSharp/stCoCServer/tree/master/stCoCServer/stTest/TestDokuWikiConnector)

DocuWikiConnector [Method Documentation](https://github.com/PetersSharp/stCoCServer/tree/master/stCoCServer/stExtLib/stDokuWikiConnector-dll/Doc)

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


