---
description: 最半同步呼叫是呼叫 WMI 方法的建議方法，例如 IWbemServices：： ExecMethod 和提供者方法，例如 Win32 LogicalDisk 類別的 Chkdsk 方法 \_ 。
ms.assetid: 3d5ddd77-19f7-42d0-b8ca-a0a11f6b3f0f
ms.tgt_platform: multiple
title: 使用 c + + 進行半同步呼叫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c4546a7220d191b822e9f0f30a767e89e4dc26a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513737"
---
# <a name="making-a-semisynchronous-call-with-c"></a><span data-ttu-id="89105-103">使用 c + + 進行半同步呼叫</span><span class="sxs-lookup"><span data-stu-id="89105-103">Making a Semisynchronous Call with C++</span></span>

<span data-ttu-id="89105-104">最半同步呼叫是呼叫 WMI 方法的建議方法，例如 [**IWbemServices：： ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) 和提供者方法，例如 [**Win32 \_ LogicalDisk 類別的 Chkdsk 方法**](/windows/desktop/CIMWin32Prov/chkdsk-method-in-class-win32-logicaldisk)。</span><span class="sxs-lookup"><span data-stu-id="89105-104">Semisynchronous calls are the recommended means to call WMI methods, such as [**IWbemServices::ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) and provider methods, such as the [**Chkdsk Method of the Win32\_LogicalDisk Class**](/windows/desktop/CIMWin32Prov/chkdsk-method-in-class-win32-logicaldisk).</span></span>

<span data-ttu-id="89105-105">同步處理的其中一個缺點是，呼叫端執行緒會被封鎖，直到呼叫完成為止。</span><span class="sxs-lookup"><span data-stu-id="89105-105">One disadvantage of synchronous processing is that the caller thread is blocked until the call completes.</span></span> <span data-ttu-id="89105-106">瓶頸可能會導致處理時間延遲。</span><span class="sxs-lookup"><span data-stu-id="89105-106">The blockage can cause a delay in processing time.</span></span> <span data-ttu-id="89105-107">相反地，非同步呼叫必須在腳本中執行 [**SWbemSink**](swbemsink.md) 。</span><span class="sxs-lookup"><span data-stu-id="89105-107">In contrast, an asynchronous call must implement [**SWbemSink**](swbemsink.md) in script.</span></span> <span data-ttu-id="89105-108">在 c + + 中，非同步程式碼必須實 [**IWbemObjectSink**](iwbemobjectsink.md) 介面、使用多個執行緒，並控制傳回給呼叫端的資訊流程。</span><span class="sxs-lookup"><span data-stu-id="89105-108">In C++, asynchronous code must implement the [**IWbemObjectSink**](iwbemobjectsink.md) interface, use multiple threads, and control the flow of information back to the caller.</span></span> <span data-ttu-id="89105-109">例如，查詢中的大型結果集可能需要相當長的時間才能傳遞，並強制呼叫者花大量系統資源來處理傳遞。</span><span class="sxs-lookup"><span data-stu-id="89105-109">Large result sets from queries, for example, can take a considerable amount of time to deliver and forces the caller to spend significant system resources to handle the delivery.</span></span>

<span data-ttu-id="89105-110">最半處理處理可透過輪詢特殊狀態物件來執行 [**IWbemCallResult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult) 介面，以解決執行緒的問題和未受控制的傳遞問題。</span><span class="sxs-lookup"><span data-stu-id="89105-110">Semisynchronous processing solves both the thread blockage and uncontrolled delivery problems by polling a special status object that implements the [**IWbemCallResult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult) interface.</span></span> <span data-ttu-id="89105-111">透過 **IWbemCallResult**，您可以改善查詢、列舉和事件通知的速度和效率。</span><span class="sxs-lookup"><span data-stu-id="89105-111">Through **IWbemCallResult**, you can improve the speed and efficiency of queries, enumerations, and event notifications.</span></span>

<span data-ttu-id="89105-112">下列程式描述如何使用 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) 介面進行半同步呼叫。</span><span class="sxs-lookup"><span data-stu-id="89105-112">The following procedure describes how to make a semisynchronous call with the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) interface.</span></span>

<span data-ttu-id="89105-113">**若要使用 IWbemServices 介面進行半同步呼叫**</span><span class="sxs-lookup"><span data-stu-id="89105-113">**To make a semisynchronous call with the IWbemServices interface**</span></span>

1.  <span data-ttu-id="89105-114">以正常方式進行呼叫，但使用 WBEM 旗標會在 *IFlags* 參數中設定 **\_ \_ \_ 立即** 傳回旗標。</span><span class="sxs-lookup"><span data-stu-id="89105-114">Make your call as normal, but with the **WBEM\_FLAG\_RETURN\_IMMEDIATELY** flag set in the *IFlags* parameter.</span></span>

    <span data-ttu-id="89105-115">您可以將 **WBEM \_ 旗 \_ 標 \_ 立即** 傳回與其他對特定方法有效的旗標。</span><span class="sxs-lookup"><span data-stu-id="89105-115">You can combine **WBEM\_FLAG\_RETURN\_IMMEDIATELY** with other flags that are valid for the specific method.</span></span> <span data-ttu-id="89105-116">例如，針對所有傳回列舉值的呼叫，請使用 **WBEM 旗標 [ \_ \_ \_ 僅轉寄** ] 旗標。</span><span class="sxs-lookup"><span data-stu-id="89105-116">For example, use the **WBEM\_FLAG\_FORWARD\_ONLY** flag for all calls that return enumerators.</span></span> <span data-ttu-id="89105-117">以組合方式設定這些旗標可節省時間和空間，並提升回應能力。</span><span class="sxs-lookup"><span data-stu-id="89105-117">Setting these flags in combination saves time and space, and improves responsiveness.</span></span>

2.  <span data-ttu-id="89105-118">輪詢您的結果。</span><span class="sxs-lookup"><span data-stu-id="89105-118">Poll for your results.</span></span>

    <span data-ttu-id="89105-119">如果您呼叫的方法會傳回列舉值，例如 [**IWbemServices：： CreateClassEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenum) 或 [**Iwbemservices：： ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery)，您可以使用 [**IEnumWbemClassObject：： Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) 或 [**IEnumWbemClassObject：： NextAsync**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-nextasync) 方法來輪詢枚舉器。</span><span class="sxs-lookup"><span data-stu-id="89105-119">If you call a method that returns an enumerator, such as [**IWbemServices::CreateClassEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenum) or [**IWbemServices::ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery), you can poll the enumerators with the [**IEnumWbemClassObject::Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) or [**IEnumWbemClassObject::NextAsync**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-nextasync) methods.</span></span> <span data-ttu-id="89105-120">**IEnumWbemClassObject：： NextAsync** 呼叫為非封鎖並立即傳回。</span><span class="sxs-lookup"><span data-stu-id="89105-120">The **IEnumWbemClassObject::NextAsync** call is nonblocking and returns immediately.</span></span> <span data-ttu-id="89105-121">在背景中，WMI 會藉由呼叫 [**IWbemObjectSink：：指示**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate)，開始傳遞要求的物件數目。</span><span class="sxs-lookup"><span data-stu-id="89105-121">In the background, WMI begins to deliver the requested number of objects by calling [**IWbemObjectSink::Indicate**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate).</span></span> <span data-ttu-id="89105-122">WMI 接著會停止，並等候其他 **NextAsync** 呼叫。</span><span class="sxs-lookup"><span data-stu-id="89105-122">WMI then stops and waits for another **NextAsync** call.</span></span>

    <span data-ttu-id="89105-123">如果您呼叫的方法不會傳回列舉值，例如 [**IWbemServices：： GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)，您必須將 *ppCallResult* 參數設定為有效的指標。</span><span class="sxs-lookup"><span data-stu-id="89105-123">If you call a method that does not return an enumerator, such as [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject), you must set the *ppCallResult* parameter to a valid pointer.</span></span> <span data-ttu-id="89105-124">在傳回的指標上使用 [**IWbemCallResult：： GetCallStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemcallresult-getcallstatus) ，以 **取得 \_ WBEM \_ S 沒有 \_ 錯誤**。</span><span class="sxs-lookup"><span data-stu-id="89105-124">Use the [**IWbemCallResult::GetCallStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemcallresult-getcallstatus) on the returned pointer to retrieve **WBEM\_S\_NO\_ERROR**.</span></span>

3.  <span data-ttu-id="89105-125">完成通話。</span><span class="sxs-lookup"><span data-stu-id="89105-125">Finish your call.</span></span>

    <span data-ttu-id="89105-126">針對傳回列舉值的呼叫，WMI 會呼叫 [**IWbemObjectSink：： SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) 來回報作業是否完成。</span><span class="sxs-lookup"><span data-stu-id="89105-126">For a call that returns an enumerator, WMI calls [**IWbemObjectSink::SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) to report the completion of the operation.</span></span> <span data-ttu-id="89105-127">如果您不需要整個結果，請呼叫 [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject)：：[**release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) 方法來釋放列舉值。</span><span class="sxs-lookup"><span data-stu-id="89105-127">If you do not need the entire result, release the enumerator by calling the [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject)::[**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method.</span></span> <span data-ttu-id="89105-128">在 WMI 中呼叫 **釋放** 結果會取消傳遞保留的所有物件。</span><span class="sxs-lookup"><span data-stu-id="89105-128">Calling **Release** results in WMI canceling the delivery of all objects that remain.</span></span>

    <span data-ttu-id="89105-129">若為不使用列舉值的呼叫，請透過方法的 *plStatus* 參數抓取 [**GetCallStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemcallresult-getcallstatus)物件。</span><span class="sxs-lookup"><span data-stu-id="89105-129">For a call that does not use an enumerator, retrieve the [**GetCallStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemcallresult-getcallstatus) object through the *plStatus* parameter of your method.</span></span>

<span data-ttu-id="89105-130">本主題中的 c + + 程式碼範例需要下列 \# include 語句才能正確編譯。</span><span class="sxs-lookup"><span data-stu-id="89105-130">The C++ code example in this topic requires the following \#include statements to compile correctly.</span></span>


```C++
#include <comdef.h>
#include <wbemidl.h>
```



<span data-ttu-id="89105-131">下列程式碼範例示範如何進行對 [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)的半同步呼叫。</span><span class="sxs-lookup"><span data-stu-id="89105-131">The following code example shows how to make a semisynchronous call to [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).</span></span>


```C++
void GetObjSemiSync(IWbemServices *pSvc)
{

    IWbemCallResult *pCallRes = 0;
    IWbemClassObject *pObj = 0;
    
    HRESULT hRes = pSvc->GetObject(_bstr_t(L"MyClass=\"AAA\""), 0,
        0, 0, &pCallRes
        );
        
    if (hRes || pCallRes == 0)
        return;
        
    while (true)
    {
        LONG lStatus = 0;
        HRESULT hRes = pCallRes->GetCallStatus(5000, &lStatus);
        if ( hRes == WBEM_S_NO_ERROR || hRes != WBEM_S_TIMEDOUT )
            break;

        // Do another task
    }

    hRes = pCallRes->GetResultObject(5000, &pObj);
    if (hRes)
    {
        pCallRes->Release();
        return;
    }

    pCallRes->Release();

    // Use the object.

    // ...

    // Release it.
    // ===========
        
    pObj->Release();    // Release objects not owned.            
  
}
```



## <a name="related-topics"></a><span data-ttu-id="89105-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="89105-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89105-133">呼叫方法</span><span class="sxs-lookup"><span data-stu-id="89105-133">Calling a Method</span></span>](calling-a-method.md)
</dt> </dl>

 

 
