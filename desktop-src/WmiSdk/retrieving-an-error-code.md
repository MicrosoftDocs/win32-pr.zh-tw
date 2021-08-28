---
description: 如同所有的應用程式，WMI 會從 Windows 作業系統接收錯誤碼。
ms.assetid: f54b8e7c-c531-47d5-bab8-780652b94555
ms.tgt_platform: multiple
title: 正在抓取錯誤碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f16bb7af3c5c2b17d3a99ac00c9122a2ddfa6c075f463819e182fe44193613a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640628"
---
# <a name="retrieving-an-error-code"></a>正在抓取錯誤碼

如同所有的應用程式，WMI 會從 Windows 作業系統接收錯誤碼。

當您收到錯誤碼時，您有下列選項：

-   查看事件記錄檔。

    WMI 會將錯誤訊息傳送到事件記錄檔服務，該服務會檢查事件記錄檔，以協助判斷錯誤的原因。 您可以使用 [事件記錄](/previous-versions/windows/desktop/eventlogprov/event-log-provider) 提供者支援的類別，以程式設計方式存取事件記錄檔。

-   正常取出錯誤碼。

    WMI 支援取得錯誤碼的標準技術，也就是 c + + 的 COM 錯誤碼，以及原生錯誤物件（例如 [ (VBScript) 的 Err 物件](/previous-versions//sbf5ze0e(v=vs.85))），如果提供者提供錯誤資訊，則為 [**SWbemLastError**](swbemlasterror.md) 。

如需詳細資訊，請參閱 [操作類別和實例資訊](manipulating-class-and-instance-information.md)。

本主題將討論下列各節：

-   [處理 VBScript 的錯誤](#handling-an-error-with-vbscript)
-   [使用 c + + 處理錯誤](#handling-an-error-using-c)

## <a name="handling-an-error-with-vbscript"></a>處理 VBScript 的錯誤

如果透過適用于 WMI 的腳本 API 呼叫 WMI 會導致錯誤，您可以使用下列選項來存取錯誤資訊：

-   使用指令碼語言的原生錯誤機制，例如，VBScript 使用 [Err 物件 (vbscript) ](/previous-versions//sbf5ze0e(v=vs.85)) 來支援錯誤處理。
-   建立 [**SWbemLastError**](swbemlasterror.md) 物件以取得錯誤報表。

下列腳本會示範如何使用原生 [Err 物件 (VBScript) ](/previous-versions//sbf5ze0e(v=vs.85))。 如果指定了不正確的進程控制碼值，就會產生錯誤。


```VB
On Error Resume Next
Set objProcess = GetObject( _
    "winmgmts:root\cimv2:Win32_Process.Handle='one'")
Wscript.Echo Err.Number
```



> [!Note]
>
> 透過 "winmgmts：" 連接至 WMI 時，Err 物件的 **Description** 屬性 [ (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)) 是空的。 但是，如果您使用 [**wbemscripting.swbemlocator**](swbemlocator.md)進行連接，則可以使用描述。
>
> 下表列出 [ (VBScript) 的 Err 物件 ](/previous-versions//sbf5ze0e(v=vs.85))屬性。
>
> 
>
> | 屬性                   | 包含                                                       |
> |----------------------------|----------------------------------------------------------------|
> | **說明**<br/> | 錯誤的當地語系化、人們看得懂的描述。<br/> |
> | **Number**<br/>      | 適用于 WMI 的腳本 API 所傳回的 **HRESULT** 。<br/>  |
> | **來源**<br/>      | 識別引發錯誤的物件。<br/>        |
>
> 
>
>  

 

下列腳本會示範如何使用 [**SWbemLastError**](swbemlasterror.md) 物件來取得詳細的錯誤資訊。 請注意，並非所有提供者都會提供資訊給 **SWbemLastError**。 如需有關腳本中錯誤碼的詳細資訊，請參閱 [WbemErrorEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum)。


```VB
On Error Resume Next
Set obj = GetObject("winmgmts:root\cimv2:Win32_Process.Handle='one'")
Set LastError = createobject("wbemscripting.swbemlasterror")
Wscript.Echo "Operation = " & LastError.operation & VBCRLF & "ParameterInfo = " _
            & LastError.ParameterInfo & VBCRLF & "ProviderName = " & LastError.ProviderName
```



## <a name="handling-an-error-using-c"></a>使用 c + + 處理錯誤

WMI 用戶端應用程式可以接收 COM 特定或 WMI 特定的錯誤。 COM 錯誤符合 COM 錯誤碼的結構。 所有 WMI 介面都可以傳回 COM 特定的錯誤，但 [**IWbemCoNtext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext)、 [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject)和 [**IWbemQualifierSet**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) 介面除外。 如需 COM 錯誤碼的詳細資訊，請參閱 [錯誤處理](../com/error-handling-in-com.md)。 WMI 介面的參考頁面會在錯誤碼區段中列出適當的 WMI 錯誤碼。

用戶端應用程式必須遵循 COM 標準來檢查狀態和錯誤傳回碼。 您必須選擇的主要差異是，您是否想要從同步、半同步或非同步呼叫取得錯誤碼。

**使用 c + + 存取同步和半同步的錯誤訊息**

1.  使用 [GetErrorInfo]( /windows/win32/api/oleauto/nf-oleauto-geterrorinfo) COM 函式的呼叫來取出錯誤資訊。

    請務必在介面方法表示錯誤之後立即呼叫 [GetErrorInfo]( /windows/win32/api/oleauto/nf-oleauto-geterrorinfo) 。 這包括您在處理半同步處理常式時所呼叫的任何 [**IWbemCallResult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult) 方法。

2.  使用 [**IErrorInterface：： QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 方法的呼叫來檢查傳回的 COM 錯誤物件。

    請務必 \_ 在 [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))呼叫中為 *riid* 參數指定 IID WbemClassObject。 **QueryInterface** 方法會傳回 WMI 類別的實例，通常是 [**\_ \_ ExtendedStatus**](--extendedstatus.md)。

WMI 不會透過 [GetErrorInfo]( /windows/win32/api/oleauto/nf-oleauto-geterrorinfo) 提供錯誤物件來進行非同步呼叫，因為沒有任何方法可以知道非同步呼叫發生的時間或執行緒。 因此，您的程式碼只能處理特定的錯誤，或透過 COM 傳遞呼叫失敗。

> [!Note]  
> 由於接收端的回呼可能不會與用戶端所需的驗證層級傳回，因此建議您使用 [半同步] 而非 [非同步通訊]。 如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。

 

**使用 c + + 存取非同步錯誤訊息**

-   從 [**IWbemObjectSink：： SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus)的執行中取出 COM 錯誤物件。

    下列虛擬程式碼顯示用戶端應用程式的一般錯誤處理執行。

    ```C++
    HRESULT hRes = SomeMethod;

    // Check for specific error and status codes.
    if (hRes == WBEM_E_NOT_FOUND)
    {
    // Processing to handle specific error code
    }
    else if hRes == WBEM_S_DUPLICATE_OBJECTS
    {
    // All other cases, including errors specific to COM
    }
    else if (FAILED(hRes))
    {

    }
    ```

    

 

