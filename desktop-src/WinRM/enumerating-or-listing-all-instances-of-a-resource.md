---
title: 列舉或列出資源的所有實例
description: Session 方法是取得指定資源之所有實例的 Windows 遠端管理方法。
ms.assetid: c50c37bf-e19a-473b-8d27-ab3bb4ec86a0
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1f510d0e0cc8115ca4dca7c7e46dd5e987ef0dd15dd4fa7d92e47d737e467d8f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119679988"
---
# <a name="enumerating-or-listing-all-instances-of-a-resource"></a>列舉或列出資源的所有實例

[**Session**](session-enumerate.md)方法是取得指定資源之所有實例的 Windows 遠端管理方法。

[**Session**](session-enumerate.md)方法不會在 [**swbemobjectset 搭配使用**](/windows/desktop/WmiSdk/swbemobjectset)物件中取得集合，例如使用 [WMI 查詢](/windows/desktop/WmiSdk/querying-wmi)作為參數的 [**SWbemService.ExecQuery**](/windows/desktop/WmiSdk/swbemservices-execquery)呼叫 (例如 `ExecQuery("SELECT * from Win32_LogicalDisk")`) ，或 [**\_ 呼叫 SWbemObject**](/windows/desktop/WmiSdk/swbemobject-instances-)之類的方法。 **Session 和列舉**[**值物件方法**](enumerator.md)更類似于用來將檔案讀取為數據流的腳本 [TextStream](/previous-versions//312a5kbt(v=vs.85))物件作業。

若要將檔案讀取為文字資料流程，您必須建立腳本 [TextStream](/previous-versions//312a5kbt(v=vs.85)) 物件，並呼叫 [TextStream](/previous-versions//h7se9d4f(v=vs.85)) 方法來讀取檔案的每一行。 以類似的方式，您可以呼叫 [**Session。列舉**](session-enumerate.md) 方法以 [**取得列舉值物件，**](enumerator.md) 並呼叫 [**ReadItem**](enumerator-readitem.md) 方法來取得下一個專案。 就像從文字檔讀取的情況一樣，您可以呼叫 [**AtEndOfStream**](enumerator-atendofstream.md) 屬性來檢查是否已到達資料項目的結尾。

**列舉資源**

1.  建立工作階段。

    ```VB
    Const RemoteComputer = "servername.domain.com"
    Set objWsman = CreateObject( "WSMan.Automation" )
    Set objSession = objWsman.CreateSession( "https://" _
        & RemoteComputer )
    ```

    

2.  建立用來識別資源的 URI。

    ```VB
    strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
                 "wmi/root/cimv2/Win32_ScheduledJob"
    ```

    

3.  呼叫 [**Session。列舉**](session-enumerate.md) 方法。 此呼叫會啟動列舉。 在 WinRM 中，列舉作業不會以與 WMI 相同的方式取得集合。 相反地， **Session** 方法會建立在 [**列舉**](enumerator.md) 值物件中維護的 WS-Management 通訊協定列舉內容。

    ```VB
    Set EnumJobs = objSession.Enumerate( strResource )
    ```

    

4.  呼叫 [**ReadItem**](enumerator-readitem.md) 方法，以取得結果的下一個專案。 在 WS-Management 通訊協定中，這會對應至提取作業。 使用 [**AtEndOfStream**](enumerator-atendofstream.md) 方法做為控制項，以瞭解何時停止讀取。

    ```VB
    While Not EnumJobs.AtEndOfStream
        NumOfJobs = NumOfJobs + 1
        DisplayOutput( EnumJobs.ReadItem ) 
    Wend
    ```

    

下列 VBScript 程式碼範例顯示完整的腳本。


```VB
Const RemoteComputer = "servername.domain.com"
Set objWsman = CreateObject( "WSMan.Automation" )
Set objSession = objWsman.CreateSession( "https://" & RemoteComputer )
strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
              "wmi/root/cimv2/Win32_ScheduledJob"

Set EnumJobs = objSession.Enumerate( strResource )
NumOfJobs = 0
While Not EnumJobs.AtEndOfStream
    NumOfJobs = NumOfJobs + 1
    DisplayOutput( EnumJobs.ReadItem ) 
Wend
Wscript.Echo "There are " & NumOfJobs & " jobs scheduled."

'****************************************************
' Displays WinRM XML message using built-in XSL
'****************************************************
Sub DisplayOutput( strWinRMXml )
    Dim xmlFile, xslFile
    Set xmlFile = CreateObject( "MSXml2.DOMDocument.3.0" ) 
    Set xslFile = CreateObject( "MSXml2.DOMDocument.3.0" )
    xmlFile.LoadXml( strWinRMXml )
    xslFile.Load( "WsmTxt.xsl" )
    Wscript.Echo xmlFile.TransformNode( xslFile ) 
End Sub
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於 Windows 遠端管理](about-windows-remote-management.md)
</dt> <dt>

[使用 Windows 遠端管理](using-windows-remote-management.md)
</dt> <dt>

[Windows遠端系統管理參考](windows-remote-management-reference.md)
</dt> </dl>

 

 