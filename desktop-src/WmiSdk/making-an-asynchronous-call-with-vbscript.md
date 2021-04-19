---
description: 對 WMI 方法或提供者方法進行非同步呼叫，可讓腳本在物件返回 SWbemSink 物件時繼續執行，而且會由 SWbemSink. OnObjectReady 等方法來處理。
ms.assetid: 61f401d9-c874-472d-8dd3-7cf9d7f20a12
ms.tgt_platform: multiple
title: 使用 VBScript 進行非同步呼叫
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c2b3ec0c1bd771f59a4e456cb8e57c3bb3e9e394
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988822"
---
# <a name="making-an-asynchronous-call-with-vbscript"></a><span data-ttu-id="79aea-103">使用 VBScript 進行非同步呼叫</span><span class="sxs-lookup"><span data-stu-id="79aea-103">Making an Asynchronous Call with VBScript</span></span>

<span data-ttu-id="79aea-104">對 [*WMI 方法*](gloss-w.md) 或 [*提供者方法*](gloss-p.md) 進行非同步呼叫，可讓腳本在物件返回 [**SWbemSink**](swbemsink.md) 物件時繼續執行，而且會由 [**SWbemSink. OnObjectReady**](swbemsink-onobjectready.md)等方法來處理。</span><span class="sxs-lookup"><span data-stu-id="79aea-104">Making an asynchronous call to a [*WMI method*](gloss-w.md) or a [*provider method*](gloss-p.md) allows a script to continue executing while objects return to an [**SWbemSink**](swbemsink.md) object, and are handled by methods such as [**SWbemSink.OnObjectReady**](swbemsink-onobjectready.md).</span></span> <span data-ttu-id="79aea-105">但是，不建議使用非同步呼叫，因為在進行呼叫時，資料可能不會以相同的安全性層級傳回。</span><span class="sxs-lookup"><span data-stu-id="79aea-105">However, asynchronous calls are not recommended because the data may not be returned at the same level of security as the call is made.</span></span>

<span data-ttu-id="79aea-106">使用非同步接收呼叫（例如 [**SWbemSink. OnObjectReady**](swbemsink-onobjectready.md) ）來取得傳回的資料時，您可以設定下列登錄值。</span><span class="sxs-lookup"><span data-stu-id="79aea-106">When using asynchronous sink calls like [**SWbemSink.OnObjectReady**](swbemsink-onobjectready.md) to get returned data, you can set the following registry value.</span></span>

<span data-ttu-id="79aea-107">**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **UnsecAppAccessControlDefault**</span><span class="sxs-lookup"><span data-stu-id="79aea-107">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**UnsecAppAccessControlDefault**</span></span>

<span data-ttu-id="79aea-108">設定此登錄值可確保傳回至接收的資料物件驗證。</span><span class="sxs-lookup"><span data-stu-id="79aea-108">Setting this registry value ensures authentication of the data objects returned to the sink.</span></span> <span data-ttu-id="79aea-109">如果 **UnsecAppAccessControlDefault** 設定為一個 (1) ，則 WMI 會執行資料傳回的存取檢查。</span><span class="sxs-lookup"><span data-stu-id="79aea-109">If **UnsecAppAccessControlDefault** is set to one (1), then WMI performs access checking of the data return.</span></span> <span data-ttu-id="79aea-110">存取檢查會確認資料來自正確的來源。</span><span class="sxs-lookup"><span data-stu-id="79aea-110">Access checks verify that the data comes from the correct source.</span></span> <span data-ttu-id="79aea-111">如需詳細資訊，請參閱 [在非同步呼叫上設定安全性](setting-security-on-an-asynchronous-call.md)。</span><span class="sxs-lookup"><span data-stu-id="79aea-111">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

<span data-ttu-id="79aea-112">名稱結尾為 "Async" 的非同步方法 \_ 一律會在呼叫後立即傳回，讓程式可以繼續執行。</span><span class="sxs-lookup"><span data-stu-id="79aea-112">Asynchronous methods with names that end in "Async\_" always return immediately after being called so that a program can continue executing.</span></span> <span data-ttu-id="79aea-113">例如， [**SWbemServices.ExecQuery**](swbemservices-execquery.md) 是同步的，並且會封鎖執行，直到傳回所有物件為止。</span><span class="sxs-lookup"><span data-stu-id="79aea-113">For example, [**SWbemServices.ExecQuery**](swbemservices-execquery.md) is synchronous and blocks execution until all of the objects are returned.</span></span> <span data-ttu-id="79aea-114">[**SWbemServices.Exe的 cQueryAsync**](swbemservices-execqueryasync.md)方法是非封鎖的非同步版本。</span><span class="sxs-lookup"><span data-stu-id="79aea-114">The [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md) method is the nonblocking asynchronous version.</span></span> <span data-ttu-id="79aea-115">以更安全的方式呼叫 **SWbemServices.ExecQuery** 非封鎖的方式，就是進行呼叫 [*半同步方式*](gloss-s.md)。</span><span class="sxs-lookup"><span data-stu-id="79aea-115">A more secure way to make the call to **SWbemServices.ExecQuery** nonblocking is by making the call [*semisynchronously*](gloss-s.md).</span></span> <span data-ttu-id="79aea-116">如需詳細資訊，請參閱 [在非同步呼叫上設定安全性](setting-security-on-an-asynchronous-call.md) ，並 [使用 VBScript 進行半同步呼叫](making-a-semisynchronous-call-with-vbscript.md)。</span><span class="sxs-lookup"><span data-stu-id="79aea-116">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md) and [Making a Semisynchronous Call with VBScript](making-a-semisynchronous-call-with-vbscript.md).</span></span>

<span data-ttu-id="79aea-117">非同步呼叫的 *iFlags* 參數一律預設為零 (0) 。</span><span class="sxs-lookup"><span data-stu-id="79aea-117">The *iFlags* parameter for asynchronous calls always defaults to zero (0).</span></span> <span data-ttu-id="79aea-118">非同步方法不會提供 [**swbemobjectset 搭配使用**](swbemobjectset.md) 集合給接收器副程式。</span><span class="sxs-lookup"><span data-stu-id="79aea-118">Asynchronous methods do not supply an [**SWbemObjectSet**](swbemobjectset.md) collection to the sink subroutine.</span></span> <span data-ttu-id="79aea-119">相反地，您的腳本或應用程式中的 [**SWbemSink. OnObjectReady**](swbemsink-onobjectready.md) 事件副程式會在每個物件提供時收到。</span><span class="sxs-lookup"><span data-stu-id="79aea-119">Instead, the [**SWbemSink.OnObjectReady**](swbemsink-onobjectready.md) event subroutine in your script or application receives each object as it is provided.</span></span>

<span data-ttu-id="79aea-120">當原始非同步呼叫完成時，它會呼叫物件接收的 [**SWbemSink. OnCompleted**](swbemsink-oncompleted.md) 事件，然後執行您放置於其中的程式碼，以處理呼叫的結果。</span><span class="sxs-lookup"><span data-stu-id="79aea-120">When the original asynchronous call is complete, it calls the [**SWbemSink.OnCompleted**](swbemsink-oncompleted.md) event of the object sink, and executes the code you place there to process the result of the call.</span></span>

> [!Note]  
> <span data-ttu-id="79aea-121">使用中的伺服器頁 (ASP) 作為腳本主機，並不支援非同步呼叫。</span><span class="sxs-lookup"><span data-stu-id="79aea-121">An Active Server Page (ASP) as a script host does not support an asynchronous call.</span></span>

 

<span data-ttu-id="79aea-122">下列程式描述如何使用 VBScript 進行非同步呼叫。</span><span class="sxs-lookup"><span data-stu-id="79aea-122">The following procedure describes how to make an asynchronous call by using VBScript.</span></span>

<span data-ttu-id="79aea-123">**使用 VBScript 進行非同步呼叫**</span><span class="sxs-lookup"><span data-stu-id="79aea-123">**To make an asynchronous call using VBScript**</span></span>

1.  <span data-ttu-id="79aea-124">連接至 WMI 並取得 [**SWbemServices**](swbemservices.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="79aea-124">Connect to WMI and get an [**SWbemServices**](swbemservices.md) object.</span></span>

    ```VB
    Set Service = GetObject("Winmgmts:")
    ```

    

2.  <span data-ttu-id="79aea-125">使用 [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) 或 (（僅適用于 Windows Script Host 2.0）建立物件接收) 將 events 屬性設為 **TRUE** 的物件標記。</span><span class="sxs-lookup"><span data-stu-id="79aea-125">Create the object sink using either [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) or (for Windows Script Host 2.0 only) the OBJECT tag with an events attribute set to **TRUE**.</span></span>

    ```VB
    Set sink = WScript.CreateObject("WbemScripting.SWbemSink","SINK_")
    ```

    

    <span data-ttu-id="79aea-126">-或-</span><span class="sxs-lookup"><span data-stu-id="79aea-126">-or-</span></span>

    ```VB
    <OBJECT progid="WbemScripting.SWbemSink" ID="SINK" events="true"/>
    ```

    

3.  <span data-ttu-id="79aea-127">針對非同步事件可以觸發的每個事件建立副程式。</span><span class="sxs-lookup"><span data-stu-id="79aea-127">Create a subroutine for each event an asynchronous event can trigger.</span></span> <span data-ttu-id="79aea-128">這些事件會定義為 [**SWbemObject**](swbemobject.md)上的方法。</span><span class="sxs-lookup"><span data-stu-id="79aea-128">These events are defined as methods on [**SWbemObject**](swbemobject.md).</span></span> <span data-ttu-id="79aea-129">例如，WMI 會在每個實例傳回時，對 [**SWbemSink OnObjectReady 回呼。**](swbemsink-onobjectready.md)</span><span class="sxs-lookup"><span data-stu-id="79aea-129">For example, WMI makes a callback to [**SWbemSink.OnObjectReady**](swbemsink-onobjectready.md) as each instance returns.</span></span>

    <span data-ttu-id="79aea-130">當您建立副程式時，請將程式碼放在副程式中，以在收到每個事件時處理。</span><span class="sxs-lookup"><span data-stu-id="79aea-130">When you create the subroutine, place code in the subroutine to handle each event when it is received.</span></span>

    ```VB
    Sub SINK_OnCompleted(
          iHResult, 
          objErrorObject, 
          objAsyncContext
          )
        WScript.Echo "Asynchronous operation is done."
    End Sub

    Sub SINK_OnObjectReady(objObject, objAsyncContext)
        WScript.Echo (objObject.Name)
    End Sub
    ```

    

    <span data-ttu-id="79aea-131">檢查 [**OnCompleted**](swbemsink-oncompleted.md)事件所傳回的 *iHresult* 參數，以判斷非同步呼叫是否成功，或是否發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="79aea-131">Examine the *iHresult* parameter returned by the [**OnCompleted**](swbemsink-oncompleted.md) event to determine whether or not the asynchronous call is successful, or if an error occurred.</span></span> <span data-ttu-id="79aea-132">如果成功，在 *iHresult* 參數中傳遞的值等於零 (0) 。</span><span class="sxs-lookup"><span data-stu-id="79aea-132">If successful, the value passed in the *iHresult* parameter is equal to zero (0).</span></span> <span data-ttu-id="79aea-133">任何其他值可能會指出錯誤，而您應該檢查 *objErrorObject* 參數中所傳回錯誤物件的值。</span><span class="sxs-lookup"><span data-stu-id="79aea-133">Any other value may indicate an error, and you should check the values in the error object that is returned in the *objErrorObject* parameter.</span></span>

4.  <span data-ttu-id="79aea-134">進行非同步呼叫，並在 *objWbemSink* 參數中傳遞您接收器的名稱。</span><span class="sxs-lookup"><span data-stu-id="79aea-134">Make an asynchronous call and pass the name of your sink in the *objWbemSink* parameter.</span></span>

    ```VB
    Service.InstancesOfAsync sink, "Win32_process"
    ```

    

5.  <span data-ttu-id="79aea-135">進行呼叫，以防止腳本在接收到所有事件之前結束。</span><span class="sxs-lookup"><span data-stu-id="79aea-135">Make a call that prevents the script from ending before all of the events are received.</span></span> <span data-ttu-id="79aea-136">如果您的腳本可以使用螢幕介面執行，簡單的方法是使用 Windows Script Host (WSH) `Echo` 命令，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="79aea-136">If your script can run with a screen interface, a simple way to do this is to use a Windows Script Host (WSH) `Echo` command, which is shown in the following example.</span></span>

    ```VB
    WScript.Echo "Waiting for instances."
    ```

    

    <span data-ttu-id="79aea-137">當您執行此腳本時，您可能會在 **等候實例** 訊息之前看到第一個實例傳回，或您可能會看到它。</span><span class="sxs-lookup"><span data-stu-id="79aea-137">When you execute this script you may see the first instance return before the **Waiting for instances** message or you may see it after.</span></span> <span data-ttu-id="79aea-138">這是非同步處理的本質。</span><span class="sxs-lookup"><span data-stu-id="79aea-138">This is the nature of asynchronous processing.</span></span> <span data-ttu-id="79aea-139">如果您太快關閉 [ **等待實例** ] 訊息方塊，則可能不會看到所有的實例。</span><span class="sxs-lookup"><span data-stu-id="79aea-139">If you close the **Waiting for instances** message box too soon, you may not see all of the instances.</span></span>

6.  <span data-ttu-id="79aea-140">如果您有數個不同的非同步呼叫傳回相同接收的結果，請將任何必要的區分資料儲存在 *objWbemAsyncCoNtext* 內容參數中。</span><span class="sxs-lookup"><span data-stu-id="79aea-140">If you have results from several different asynchronous calls returning to the same sink, store any necessary distinguishing data in the *objWbemAsyncContext* context parameter.</span></span>

7.  <span data-ttu-id="79aea-141">完成接收時，請使用 [**cancel**](swbemsink-cancel.md) 方法取消您的非同步呼叫。</span><span class="sxs-lookup"><span data-stu-id="79aea-141">When finished with the sink, cancel your asynchronous call with the [**Cancel**](swbemsink-cancel.md) method.</span></span>

    ```VB
    objwbemsink.Cancel()
    ```

    

    <span data-ttu-id="79aea-142">[**Cancel**](swbemsink-cancel.md)方法會指示 WSH 取消與指定接收器物件相關聯的所有非同步呼叫。</span><span class="sxs-lookup"><span data-stu-id="79aea-142">The [**Cancel**](swbemsink-cancel.md) method instructs WSH to cancel all of the asynchronous calls associated with a given sink object.</span></span> <span data-ttu-id="79aea-143">因此，您可能會想要針對必須獨立的非同步作業使用不同的接收。</span><span class="sxs-lookup"><span data-stu-id="79aea-143">Thus, you may want to use separate sinks for asynchronous operations that must be independent.</span></span>

8.  <span data-ttu-id="79aea-144">藉由將接收器物件指派給來釋放接收器物件 `Nothing` 。</span><span class="sxs-lookup"><span data-stu-id="79aea-144">Release the sink object by assigning the sink object to `Nothing`.</span></span>

    ```VB
    set objwbemsink= Nothing
    ```

    

<span data-ttu-id="79aea-145">下列程式碼範例顯示本機電腦上所有 [**Win32 \_ 進程**](/windows/desktop/CIMWin32Prov/win32-process) 實例的非同步查詢。</span><span class="sxs-lookup"><span data-stu-id="79aea-145">The following code example shows an asynchronous query for all the instances of [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) on the local machine.</span></span> <span data-ttu-id="79aea-146">如需相同方法的半同步版本，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="79aea-146">For a semisynchronous version of the same method, see [Calling a Method](calling-a-method.md).</span></span>


```VB
' Create an object sink
set oSink = WScript.CreateObject("wbemscripting.swbemsink","sink_")
' Connect to WMI and the cimv2 namespace, and obtain
' an SWbemServices object
set oSvc = GetObject("winmgmts:root\cimv2")

bdone = false
' Query for all Win32_Process objects
osvc.ExecQueryAsync oSink, "SELECT Name FROM Win32_Process"
' Wait until all instances are returned. 
' The bdone flag prevents the script from exiting until
' the sink.OnCompleted subroutine is executed when
' all the objects are returned.
while not bdone    
    wscript.sleep 1000
wend

' The sink subroutine to handle the OnObjectReady 
' event. This is called as each object returns.
sub sink_OnObjectReady(oInst, octx)
    WScript.Echo "Got Instance: " & oInst.Name
end sub
' The sink subroutine to handle the OnCompleted event.
' This is called when all the objects are returned. 
' The oErr parameter obtains an SWbemLastError object,
' if available from the provider.
sub sink_OnCompleted(HResult, oErr, oCtx)
    WScript.Echo "ExecQueryAsync completed"
    bdone = true
end sub
```



## <a name="related-topics"></a><span data-ttu-id="79aea-147">相關主題</span><span class="sxs-lookup"><span data-stu-id="79aea-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79aea-148">呼叫方法</span><span class="sxs-lookup"><span data-stu-id="79aea-148">Calling a Method</span></span>](calling-a-method.md)
</dt> <dt>

[<span data-ttu-id="79aea-149">維護 WMI 安全性</span><span class="sxs-lookup"><span data-stu-id="79aea-149">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> </dl>

 

 
