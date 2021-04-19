---
title: 查詢資源的特定實例
description: 呼叫 Session. 列舉具有可將列舉範圍縮小為查詢的選擇性參數。
ms.assetid: 69d2fe79-9aad-4c8c-a65e-c6bb0e51c063
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 30ae068c712dd04ba892220657ad64820a890040
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106966862"
---
# <a name="querying-for-specific-instances-of-a-resource"></a>查詢資源的特定實例

呼叫 [**Session. 列舉**](session-enumerate.md) 具有可將列舉範圍縮小為查詢的選擇性參數。 由於 [Winrm 腳本 api](winrm-scripting-api.md) 和 [Winrm c + + API](winrm-c---api.md) 是以基礎 WS-Management 通訊協定為基礎，因此參數會使用與用來查詢通訊協定（*篩選* 和 *篩選方言*）相同的術語。

您可以使用 [**Session**](session-enumerate.md) 的篩選和方言參數，也可以建立並提供 [**ResourceLocator**](resourcelocator.md) 物件和 [**AddSelector**](resourcelocator-addselector.md) 方法，但不能同時執行這兩者。

此程式會針對已系結 TCP/IP 和啟用的網路介面卡執行查詢。 此查詢會要求將 **IpEnabled** 屬性設定為 **True** 的所有 [**Win32 \_ >networkadapterconfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration)實例。 除了新增 *篩選* 和 *方言* 以外，查詢的處理方式類似簡單列舉。

在此範例中，資源常數的資源名稱是以星號 "" 表示， \* 因為 *strFilter* 字串中已提及類別名稱（ [**Win32 \_ >networkadapterconfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration)）。

**查詢資源的特定實例**

1.  為了方便閱讀，請將 Uri 定義為常數。

    ```VB
    Const RemoteComputer = "servername.domain.com"
    Const Resource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/*"
    Const Dialect = "http://schemas.microsoft.com/wbem/wsman/1/WQL"
    ```

    

2.  建立工作階段。

    ```VB
    Set objWsman = CreateObject("Wsman.Automation")
    Set objSession = objWsman.CreateSession("https://" & RemoteComputer)
    ```

    

3.  建立篩選字串。 Windows 遠端管理支援 [WQL](/windows/desktop/WmiSdk/wql-sql-for-wmi) 做為篩選方言。

    ```VB
    strFilter = "SELECT * FROM Win32_NetworkAdapterConfiguration WHERE IpEnabled=TRUE"
    ```

    

4.  在 *旗標* 參數中設定任何必要的 [**列舉常數**](enumeration-constants.md)。

    請注意，如果旗標包含 [**列舉常數**](enumeration-constants.md) **WSManFlagHierarchyDeepBasePropsOnly** 或 **WSManFlagHierarchyShallow** ，則 WinRM 服務會傳回 **\_ \_ \_ \_ 不支援** 的錯誤錯誤碼錯誤的 WSMAN 多型模式。

5.  呼叫 [**Session。列舉**](session-enumerate.md) 方法。 此呼叫會啟動列舉。 **Session** 方法會建立 WS-Management 的通訊協定列舉內容，並保留在 [**列舉**](enumerator.md)值物件中。

    ```VB
    Set objResultSet = objSession.Enumerate(Resource, strFilter, Dialect)
    ```

    

6.  呼叫 [**ReadItem**](enumerator-readitem.md) 方法，以取得結果的下一個專案。 在 WS-Management 通訊協定中，這會對應至提取作業。 使用 [**AtEndOfStream**](enumerator-atendofstream.md) 方法做為控制項，以瞭解何時停止讀取。

    ```VB
    While Not objResultSet.AtEndOfStream
        DisplayOutput(objResultSet.ReadItem)
    Wend
    ```

    

下列 VBScript 程式碼範例顯示完整的腳本。


```VB
Const RemoteComputer = "servername.domain.com"
Const Resource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/*"
Const Dialect = "http://schemas.microsoft.com/wbem/wsman/1/WQL"

Set objWsman = CreateObject("Wsman.Automation")
Set objSession = objWsman.CreateSession("https://" & RemoteComputer)

strFilter = "SELECT * FROM Win32_NetworkAdapterConfiguration WHERE IpEnabled=TRUE"

Set objResultSet = objSession.Enumerate(Resource, strFilter, Dialect)

While Not objResultSet.AtEndOfStream
    DisplayOutput(objResultSet.ReadItem)
Wend

'****************************************************
' Displays WinRM XML message using built-in XSL
'****************************************************
Sub DisplayOutput(strWinRMXml)
    Dim xmlFile, xslFile
    Set xmlFile = CreateObject("MSXml2.DOMDocument.3.0") 
    Set xslFile = CreateObject("MSXml2.DOMDocument.3.0")
    xmlFile.LoadXml(strWinRMXml)
    xslFile.Load("WsmTxt.xsl")
    Wscript.Echo xmlFile.TransformNode(xslFile) 
End Sub
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 Windows 遠端管理](using-windows-remote-management.md)
</dt> <dt>

[列舉或列出資源的所有實例](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> <dt>

[**ResourceLocator**](resourcelocator.md)
</dt> </dl>

 

 