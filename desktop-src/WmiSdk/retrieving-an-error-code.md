---
description: 如同所有的應用程式，WMI 會從 Windows 作業系統接收錯誤碼。
ms.assetid: f54b8e7c-c531-47d5-bab8-780652b94555
ms.tgt_platform: multiple
title: 正在抓取錯誤碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75c42dbd160ef6412c332e2da2c01f6590e10966
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977240"
---
# <a name="retrieving-an-error-code"></a><span data-ttu-id="84f97-103">正在抓取錯誤碼</span><span class="sxs-lookup"><span data-stu-id="84f97-103">Retrieving an Error Code</span></span>

<span data-ttu-id="84f97-104">如同所有的應用程式，WMI 會從 Windows 作業系統接收錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="84f97-104">As with all applications, WMI receives error codes from the Windows operating system.</span></span>

<span data-ttu-id="84f97-105">當您收到錯誤碼時，您有下列選項：</span><span class="sxs-lookup"><span data-stu-id="84f97-105">When you receive an error code, you have the following options:</span></span>

-   <span data-ttu-id="84f97-106">查看事件記錄檔。</span><span class="sxs-lookup"><span data-stu-id="84f97-106">Look at the event log.</span></span>

    <span data-ttu-id="84f97-107">WMI 會將錯誤訊息傳送到事件記錄檔服務，該服務會檢查事件記錄檔，以協助判斷錯誤的原因。</span><span class="sxs-lookup"><span data-stu-id="84f97-107">WMI sends error messages to the Event Log service that checks the event logs to help determine the cause of an error.</span></span> <span data-ttu-id="84f97-108">您可以使用 [事件記錄](/previous-versions/windows/desktop/eventlogprov/event-log-provider) 提供者支援的類別，以程式設計方式存取事件記錄檔。</span><span class="sxs-lookup"><span data-stu-id="84f97-108">You can use the classes that the [Event Log](/previous-versions/windows/desktop/eventlogprov/event-log-provider) provider supports to access event logs programmatically.</span></span>

-   <span data-ttu-id="84f97-109">正常取出錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="84f97-109">Retrieve the error code normally.</span></span>

    <span data-ttu-id="84f97-110">WMI 支援取得錯誤碼的標準技術，也就是 c + + 的 COM 錯誤碼，以及原生錯誤物件（例如 [ (VBScript) 的 Err 物件](/previous-versions//sbf5ze0e(v=vs.85))），如果提供者提供錯誤資訊，則為 [**SWbemLastError**](swbemlasterror.md) 。</span><span class="sxs-lookup"><span data-stu-id="84f97-110">WMI supports the standard techniques to retrieve error codes, which are COM error codes for C++, and native error objects, such as [Err Object (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)), or [**SWbemLastError**](swbemlasterror.md) if the provider supplies error information.</span></span>

<span data-ttu-id="84f97-111">如需詳細資訊，請參閱 [操作類別和實例資訊](manipulating-class-and-instance-information.md)。</span><span class="sxs-lookup"><span data-stu-id="84f97-111">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

<span data-ttu-id="84f97-112">本主題將討論下列各節：</span><span class="sxs-lookup"><span data-stu-id="84f97-112">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="84f97-113">處理 VBScript 的錯誤</span><span class="sxs-lookup"><span data-stu-id="84f97-113">Handling an Error with VBScript</span></span>](#handling-an-error-with-vbscript)
-   [<span data-ttu-id="84f97-114">使用 c + + 處理錯誤</span><span class="sxs-lookup"><span data-stu-id="84f97-114">Handling an Error Using C++</span></span>](#handling-an-error-using-c)

## <a name="handling-an-error-with-vbscript"></a><span data-ttu-id="84f97-115">處理 VBScript 的錯誤</span><span class="sxs-lookup"><span data-stu-id="84f97-115">Handling an Error with VBScript</span></span>

<span data-ttu-id="84f97-116">如果透過適用于 WMI 的腳本 API 呼叫 WMI 會導致錯誤，您可以使用下列選項來存取錯誤資訊：</span><span class="sxs-lookup"><span data-stu-id="84f97-116">If a call to WMI through the Scripting API for WMI causes an error, you have the following options to access the error information:</span></span>

-   <span data-ttu-id="84f97-117">使用指令碼語言的原生錯誤機制，例如，VBScript 使用 [Err 物件 (vbscript) ](/previous-versions//sbf5ze0e(v=vs.85)) 來支援錯誤處理。</span><span class="sxs-lookup"><span data-stu-id="84f97-117">Use native error mechanisms of the scripting language, for example, in VBScript use [Err Object (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)) to support error handling.</span></span>
-   <span data-ttu-id="84f97-118">建立 [**SWbemLastError**](swbemlasterror.md) 物件以取得錯誤報表。</span><span class="sxs-lookup"><span data-stu-id="84f97-118">Create an [**SWbemLastError**](swbemlasterror.md) object to get an error report.</span></span>

<span data-ttu-id="84f97-119">下列腳本會示範如何使用原生 [Err 物件 (VBScript) ](/previous-versions//sbf5ze0e(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="84f97-119">The following script shows use of the native [Err Object (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)).</span></span> <span data-ttu-id="84f97-120">如果指定了不正確的進程控制碼值，就會產生錯誤。</span><span class="sxs-lookup"><span data-stu-id="84f97-120">When an incorrect value for the process handle is given, an error is generated.</span></span>


```VB
On Error Resume Next
Set objProcess = GetObject( _
    "winmgmts:root\cimv2:Win32_Process.Handle='one'")
Wscript.Echo Err.Number
```



> [!Note]
>
> <span data-ttu-id="84f97-121">透過 "winmgmts：" 連接至 WMI 時，Err 物件的 **Description** 屬性 [ (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)) 是空的。</span><span class="sxs-lookup"><span data-stu-id="84f97-121">The **Description** property of [Err Object (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)) is empty when connecting to WMI through the "winmgmts:" moniker.</span></span> <span data-ttu-id="84f97-122">但是，如果您使用 [**wbemscripting.swbemlocator**](swbemlocator.md)進行連接，則可以使用描述。</span><span class="sxs-lookup"><span data-stu-id="84f97-122">However, if you connect using [**SWbemLocator**](swbemlocator.md), the description is available.</span></span>
>
> <span data-ttu-id="84f97-123">下表列出 [ (VBScript) 的 Err 物件 ](/previous-versions//sbf5ze0e(v=vs.85))屬性。</span><span class="sxs-lookup"><span data-stu-id="84f97-123">The following table lists the properties of [Err Object (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)).</span></span>
>
> 
>
> | <span data-ttu-id="84f97-124">屬性</span><span class="sxs-lookup"><span data-stu-id="84f97-124">Property</span></span>                   | <span data-ttu-id="84f97-125">包含</span><span class="sxs-lookup"><span data-stu-id="84f97-125">Contains</span></span>                                                       |
> |----------------------------|----------------------------------------------------------------|
> | <span data-ttu-id="84f97-126">**說明**</span><span class="sxs-lookup"><span data-stu-id="84f97-126">**Description**</span></span><br/> | <span data-ttu-id="84f97-127">錯誤的當地語系化、人們看得懂的描述。</span><span class="sxs-lookup"><span data-stu-id="84f97-127">Localized, human-readable description of the error.</span></span><br/> |
> | <span data-ttu-id="84f97-128">**Number**</span><span class="sxs-lookup"><span data-stu-id="84f97-128">**Number**</span></span><br/>      | <span data-ttu-id="84f97-129">適用于 WMI 的腳本 API 所傳回的 **HRESULT** 。</span><span class="sxs-lookup"><span data-stu-id="84f97-129">**HRESULT** returned by the Scripting API for WMI.</span></span><br/>  |
> | <span data-ttu-id="84f97-130">**來源**</span><span class="sxs-lookup"><span data-stu-id="84f97-130">**Source**</span></span><br/>      | <span data-ttu-id="84f97-131">識別引發錯誤的物件。</span><span class="sxs-lookup"><span data-stu-id="84f97-131">Identifies the object that raised the error.</span></span><br/>        |
>
> 
>
>  

 

<span data-ttu-id="84f97-132">下列腳本會示範如何使用 [**SWbemLastError**](swbemlasterror.md) 物件來取得詳細的錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="84f97-132">The following script shows use of an [**SWbemLastError**](swbemlasterror.md) object to obtain detailed error information.</span></span> <span data-ttu-id="84f97-133">請注意，並非所有提供者都會提供資訊給 **SWbemLastError**。</span><span class="sxs-lookup"><span data-stu-id="84f97-133">Note that not all providers supply information to **SWbemLastError**.</span></span> <span data-ttu-id="84f97-134">如需有關腳本中錯誤碼的詳細資訊，請參閱 [WbemErrorEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="84f97-134">For more information about error codes in script, see [WbemErrorEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>


```VB
On Error Resume Next
Set obj = GetObject("winmgmts:root\cimv2:Win32_Process.Handle='one'")
Set LastError = createobject("wbemscripting.swbemlasterror")
Wscript.Echo "Operation = " & LastError.operation & VBCRLF & "ParameterInfo = " _
            & LastError.ParameterInfo & VBCRLF & "ProviderName = " & LastError.ProviderName
```



## <a name="handling-an-error-using-c"></a><span data-ttu-id="84f97-135">使用 c + + 處理錯誤</span><span class="sxs-lookup"><span data-stu-id="84f97-135">Handling an Error Using C++</span></span>

<span data-ttu-id="84f97-136">WMI 用戶端應用程式可以接收 COM 特定或 WMI 特定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="84f97-136">A WMI client application can receive either COM-specific or WMI-specific errors.</span></span> <span data-ttu-id="84f97-137">COM 錯誤符合 COM 錯誤碼的結構。</span><span class="sxs-lookup"><span data-stu-id="84f97-137">The COM errors conform to the structure of COM error codes.</span></span> <span data-ttu-id="84f97-138">所有 WMI 介面都可以傳回 COM 特定的錯誤，但 [**IWbemCoNtext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext)、 [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject)和 [**IWbemQualifierSet**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) 介面除外。</span><span class="sxs-lookup"><span data-stu-id="84f97-138">All WMI interfaces can return a COM-specific error except the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext), [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject), and [**IWbemQualifierSet**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) interfaces.</span></span> <span data-ttu-id="84f97-139">如需 COM 錯誤碼的詳細資訊，請參閱 [錯誤處理](../com/error-handling-in-com.md)。</span><span class="sxs-lookup"><span data-stu-id="84f97-139">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span> <span data-ttu-id="84f97-140">WMI 介面的參考頁面會在錯誤碼區段中列出適當的 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="84f97-140">The reference pages of the WMI interfaces list the appropriate WMI error codes in the Error Codes section.</span></span>

<span data-ttu-id="84f97-141">用戶端應用程式必須遵循 COM 標準來檢查狀態和錯誤傳回碼。</span><span class="sxs-lookup"><span data-stu-id="84f97-141">A client application must follow the COM standards for checking status and error return codes.</span></span> <span data-ttu-id="84f97-142">您必須選擇的主要差異是，您是否想要從同步、半同步或非同步呼叫取得錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="84f97-142">The main difference you must choose is whether you wish to retrieve the error code from a synchronous, semisynchronous, or asynchronous call.</span></span>

<span data-ttu-id="84f97-143">**使用 c + + 存取同步和半同步的錯誤訊息**</span><span class="sxs-lookup"><span data-stu-id="84f97-143">**To access synchronous and semisynchronous error messages using C++**</span></span>

1.  <span data-ttu-id="84f97-144">使用 [GetErrorInfo]( /windows/win32/api/oleauto/nf-oleauto-geterrorinfo) COM 函式的呼叫來取出錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="84f97-144">Retrieve the error information with a call to the [GetErrorInfo]( /windows/win32/api/oleauto/nf-oleauto-geterrorinfo) COM function.</span></span>

    <span data-ttu-id="84f97-145">請務必在介面方法表示錯誤之後立即呼叫 [GetErrorInfo]( /windows/win32/api/oleauto/nf-oleauto-geterrorinfo) 。</span><span class="sxs-lookup"><span data-stu-id="84f97-145">Make sure to call [GetErrorInfo]( /windows/win32/api/oleauto/nf-oleauto-geterrorinfo) immediately after an interface method indicates an error.</span></span> <span data-ttu-id="84f97-146">這包括您在處理半同步處理常式時所呼叫的任何 [**IWbemCallResult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult) 方法。</span><span class="sxs-lookup"><span data-stu-id="84f97-146">This includes any of the [**IWbemCallResult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult) methods you call while processing a semisynchronous process.</span></span>

2.  <span data-ttu-id="84f97-147">使用 [**IErrorInterface：： QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 方法的呼叫來檢查傳回的 COM 錯誤物件。</span><span class="sxs-lookup"><span data-stu-id="84f97-147">Examine the returned COM error object with a call to the [**IErrorInterface::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method.</span></span>

    <span data-ttu-id="84f97-148">請務必 \_ 在 [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))呼叫中為 *riid* 參數指定 IID WbemClassObject。</span><span class="sxs-lookup"><span data-stu-id="84f97-148">Make sure to specify IID\_WbemClassObject for the *riid* parameter in the [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) call.</span></span> <span data-ttu-id="84f97-149">**QueryInterface** 方法會傳回 WMI 類別的實例，通常是 [**\_ \_ ExtendedStatus**](--extendedstatus.md)。</span><span class="sxs-lookup"><span data-stu-id="84f97-149">The **QueryInterface** method returns an instance of a WMI class, typically [**\_\_ExtendedStatus**](--extendedstatus.md).</span></span>

<span data-ttu-id="84f97-150">WMI 不會透過 [GetErrorInfo]( /windows/win32/api/oleauto/nf-oleauto-geterrorinfo) 提供錯誤物件來進行非同步呼叫，因為沒有任何方法可以知道非同步呼叫發生的時間或執行緒。</span><span class="sxs-lookup"><span data-stu-id="84f97-150">WMI does not deliver the error object through [GetErrorInfo]( /windows/win32/api/oleauto/nf-oleauto-geterrorinfo) for an asynchronous call because there is no way to know when, or on which thread the asynchronous call occurred.</span></span> <span data-ttu-id="84f97-151">因此，您的程式碼只能處理特定的錯誤，或透過 COM 傳遞呼叫失敗。</span><span class="sxs-lookup"><span data-stu-id="84f97-151">Therefore, your code can only handle specific errors or pass the call failure through COM.</span></span>

> [!Note]  
> <span data-ttu-id="84f97-152">由於接收端的回呼可能不會與用戶端所需的驗證層級傳回，因此建議您使用 [半同步] 而非 [非同步通訊]。</span><span class="sxs-lookup"><span data-stu-id="84f97-152">Because the callback to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="84f97-153">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="84f97-153">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

<span data-ttu-id="84f97-154">**使用 c + + 存取非同步錯誤訊息**</span><span class="sxs-lookup"><span data-stu-id="84f97-154">**To access asynchronous error messages using C++**</span></span>

-   <span data-ttu-id="84f97-155">從 [**IWbemObjectSink：： SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus)的執行中取出 COM 錯誤物件。</span><span class="sxs-lookup"><span data-stu-id="84f97-155">Retrieve the COM error object from your implementation of [**IWbemObjectSink::SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus).</span></span>

    <span data-ttu-id="84f97-156">下列虛擬程式碼顯示用戶端應用程式的一般錯誤處理執行。</span><span class="sxs-lookup"><span data-stu-id="84f97-156">The following pseudocode shows a typical error handling implementation for a client application.</span></span>

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

    

 

