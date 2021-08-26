---
description: 說明如何建立 Microsoft Active Server Pages (ASP) ，將遠端電腦的相關資訊顯示到未安裝 WMI 的電腦。
ms.assetid: add08566-6408-43e4-9d0d-4c0851540602
ms.tgt_platform: multiple
title: 建立 WMI 的 Active Server Pages
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ee7b31a5f4874e0ae4431ac452ea604da9c154bbb78e8debb91aad7ea892fa09
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030608"
---
# <a name="creating-active-server-pages-for-wmi"></a>建立 WMI 的 Active Server Pages

Microsoft Active Server Pages (ASP) 可以同時包含伺服器端和用戶端腳本，藉此建立動態網頁。 ASP 頁面的速度會比用戶端 HTML 網頁快許多，因為大部分的工作都是在伺服器上完成。 您也可以使用 ASP 頁面，將遠端電腦的相關資訊顯示到未安裝 Windows Management Instrumentation (WMI) 的其他電腦。

下列程式說明如何搭配使用 WMI 與 ASP。

**使用 WMI 搭配 ASP**

1.  撰寫使用 WMI 的 ASP 網頁 ( .asp) ，並將它放在 web 伺服器可存取的目錄中。

    您可以使用數種指令碼語言（包括 VBScript）來開發 WMI 的 ASP 腳本。 您可以建立 ASP 頁面的 WMI 腳本部分，就像是使用 WMI 來建立任何其他使用 WMI 的腳本一樣，有一個重要的限制：您無法在 ASP 頁面內使用非同步 WMI 方法。 另請注意，對 **GetObject** 或 **CreateObject** 的任何呼叫都必須在伺服器端程式碼中。 如需詳細資訊，請參閱 [適用于 WMI 的腳本 API](scripting-api-for-wmi.md)。

2.  設定 Internet Information Services (IIS) 的驗證設定。 如需詳細資訊，請參閱 [針對 WMI ASP 腳本設定 IIS 5 和更新版本](configuring-iis-5-for-wmi-asp-scripting.md)。
3.  停用匿名存取，並啟用 ASP 檔案的 Windows 整合式驗證。 您可以使用位於 **主控台**[系統 **管理工具**] 資料夾中的 IIS 嵌入式管理單元，來設定 ASP 頁面的這些設定。

## <a name="wmi-asp-page-example"></a>WMI ASP 頁面範例

下列範例會使用 Active Server 頁面中的 Windows Management Instrumentation (WMI)  (ASP) ，以顯示執行此腳本之伺服器的 IP 位址和預設 ip 閘道設定。


```VB
<%@ LANGUAGE="VBSCRIPT"%>
<HTML>
<HEAD>
<TITLE>WMI ASP Example:
    Read Default Gateway and IP Address information </TITLE>
</HEAD>

<BODY>

<%
On Error Resume Next
set IPConfigSet = GetObject("winmgmts:" _
   & "{impersonationLevel=impersonate}!root\cimv2").ExecQuery" _
    & "("SELECT IPAddress, DefaultIPGateway "" _ 
    & " FROM Win32_NetworkAdapterConfiguration WHERE IPEnabled=TRUE")
%>

<%If Err <> 0 Then %>
    <%if err.number = -2147217405 then%>
        <p>Error 0x80041003: Access Denied: 
           Check permissions and file security for this ASP file.</p>
    <%else%>
        <p>Error description: <%=Err.description%> 
           error number <%=Err.number%></p>
    <%end if%>

<%end if %>

<%for each IPConfig in IPConfigSet%>

    <%if Not IsNull(IPConfig.IPAddress) then %>
        <%for i=LBound(IPConfig.IPAddress) 
            to UBound(IPConfig.IPAddress)%>
            <p>IP Address: <%=IPConfig.IPAddress(i)%></p>
        <%next%>
    <%end if%>
    

    <%if Not IsNull(IPConfig.DefaultIPGateway) then %>
        <%for i=LBound(IPConfig.DefaultIPGateway) 
            to UBound(IPConfig.DefaultIPGateway)%>
            <p>Default IP Gateway: 
                <%=IPConfig.DefaultIPGateway(i)%></p>
        <%next%>
    <%end if%>
<%next%>

<%If Err <> 0 Then %>
    <p>error description: <%=Err.description%> 
       error number <%=Err.number%></p>
<%end if %>

</BODY>
</HTML>
```



 

 



