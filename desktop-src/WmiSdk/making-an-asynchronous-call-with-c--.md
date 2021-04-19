---
description: 以 c + + 撰寫的 WMI 應用程式，可以使用 IWbemServices COM 介面的許多方法進行非同步呼叫。
ms.assetid: 5179969f-bc7d-4408-84ef-7b003950a59f
ms.tgt_platform: multiple
title: 使用 c + + 進行非同步呼叫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7f093aef4b1a1b4dbede53333e77d737f8efd69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979836"
---
# <a name="making-an-asynchronous-call-with-c"></a><span data-ttu-id="d6873-103">使用 c + + 進行非同步呼叫</span><span class="sxs-lookup"><span data-stu-id="d6873-103">Making an Asynchronous Call with C++</span></span>

<span data-ttu-id="d6873-104">以 c + + 撰寫的 WMI 應用程式，可以使用 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) COM 介面的許多方法進行非同步呼叫。</span><span class="sxs-lookup"><span data-stu-id="d6873-104">WMI applications written in C++ can make asynchronous calls by using many of the methods of the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) COM interface.</span></span> <span data-ttu-id="d6873-105">不過，呼叫 [*WMI 方法*](gloss-w.md) 或 [*提供者方法*](gloss-p.md) 的建議程式是使用半同步呼叫，因為半同步呼叫比非同步呼叫更安全。</span><span class="sxs-lookup"><span data-stu-id="d6873-105">However, the recommended procedure for calling a [*WMI method*](gloss-w.md) or a [*provider method*](gloss-p.md) is by using semisynchronous calls because semisynchronous calls are more secure than asynchronous calls.</span></span> <span data-ttu-id="d6873-106">如需詳細資訊，請參閱 [使用 c + + 進行半同步呼叫](making-a-semisynchronous-call-with-c--.md) ，以及 [在非同步呼叫上設定安全性](setting-security-on-an-asynchronous-call.md)。</span><span class="sxs-lookup"><span data-stu-id="d6873-106">For more information, see [Making a Semisynchronous Call with C++](making-a-semisynchronous-call-with-c--.md) and [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

<span data-ttu-id="d6873-107">下列程式描述如何在您的進程中使用接收器進行非同步呼叫。</span><span class="sxs-lookup"><span data-stu-id="d6873-107">The following procedure describes how to make an asynchronous call by using the sink in your process.</span></span>

<span data-ttu-id="d6873-108">**使用 c + + 進行非同步呼叫**</span><span class="sxs-lookup"><span data-stu-id="d6873-108">**To make an asynchronous call using C++**</span></span>

1.  <span data-ttu-id="d6873-109">執行 [**IWbemObjectSink**](iwbemobjectsink.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="d6873-109">Implement the [**IWbemObjectSink**](iwbemobjectsink.md) interface.</span></span>

    <span data-ttu-id="d6873-110">進行非同步呼叫的所有應用程式都必須執行 [**IWbemObjectSink**](iwbemobjectsink.md)。</span><span class="sxs-lookup"><span data-stu-id="d6873-110">All applications that make asynchronous calls must implement [**IWbemObjectSink**](iwbemobjectsink.md).</span></span> <span data-ttu-id="d6873-111">暫存事件取用者也會執行 **IWbemObjectSink** 來接收事件的通知。</span><span class="sxs-lookup"><span data-stu-id="d6873-111">Temporary event consumers also implement **IWbemObjectSink** to receive notification of events.</span></span>

2.  <span data-ttu-id="d6873-112">登入目標 WMI 命名空間。</span><span class="sxs-lookup"><span data-stu-id="d6873-112">Log on to the target WMI namespace.</span></span>

    <span data-ttu-id="d6873-113">應用程式一律需要在初始化階段呼叫 COM 函數 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) 。</span><span class="sxs-lookup"><span data-stu-id="d6873-113">Applications always have to call the COM function [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) during the initialization phase.</span></span> <span data-ttu-id="d6873-114">如果在進行非同步呼叫之前沒有這麼做，WMI 就會釋放應用程式接收，而不會完成非同步呼叫。</span><span class="sxs-lookup"><span data-stu-id="d6873-114">If they do not do so before making an asynchronous call, WMI releases the application sink without completing the asynchronous call.</span></span> <span data-ttu-id="d6873-115">如需詳細資訊，請參閱 [初始化 WMI 應用程式的 COM](initializing-com-for-a-wmi-application.md)。</span><span class="sxs-lookup"><span data-stu-id="d6873-115">For more information, see [Initializing COM for a WMI Application](initializing-com-for-a-wmi-application.md).</span></span>

3.  <span data-ttu-id="d6873-116">設定接收的安全性。</span><span class="sxs-lookup"><span data-stu-id="d6873-116">Set the security for your sink.</span></span>

    <span data-ttu-id="d6873-117">非同步呼叫會建立您可能必須處理的各種安全性問題，例如允許 WMI 存取您的應用程式。</span><span class="sxs-lookup"><span data-stu-id="d6873-117">Asynchronous calls create a variety of security issues that you may have to deal with, for example, allowing WMI access to your application.</span></span> <span data-ttu-id="d6873-118">如需詳細資訊，請參閱 [在非同步呼叫上設定安全性](setting-security-on-an-asynchronous-call.md)。</span><span class="sxs-lookup"><span data-stu-id="d6873-118">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

4.  <span data-ttu-id="d6873-119">進行非同步呼叫。</span><span class="sxs-lookup"><span data-stu-id="d6873-119">Make the asynchronous call.</span></span>

    <span data-ttu-id="d6873-120">方法會立即傳回，而 **不會有 \_ \_ \_ 錯誤** 的成功碼。</span><span class="sxs-lookup"><span data-stu-id="d6873-120">The method returns immediately with the **WBEM\_S\_NO\_ERROR** success code.</span></span> <span data-ttu-id="d6873-121">在等候作業完成時，應用程式可以繼續執行其他工作。</span><span class="sxs-lookup"><span data-stu-id="d6873-121">The application can proceed with other tasks while waiting for the operation to complete.</span></span> <span data-ttu-id="d6873-122">WMI 會在應用程式的 [**IWbemObjectSink**](iwbemobjectsink.md) 執行中呼叫方法，以將其回報給應用程式。</span><span class="sxs-lookup"><span data-stu-id="d6873-122">WMI reports back to the application by calling methods in the [**IWbemObjectSink**](iwbemobjectsink.md) implementation of your application.</span></span>

5.  <span data-ttu-id="d6873-123">如有必要，請定期檢查您的執行是否有更新。</span><span class="sxs-lookup"><span data-stu-id="d6873-123">If necessary, check your implementation periodically for updates.</span></span>

    <span data-ttu-id="d6873-124">應用程式可以藉由在對 **WBEM \_ 旗標 \_ 傳送 \_ 狀態** 的非同步呼叫中設定 *lFlags* 參數，來接收中繼狀態的通知。</span><span class="sxs-lookup"><span data-stu-id="d6873-124">Applications can receive notification of intermediate status by setting the *lFlags* parameter in the asynchronous call to **WBEM\_FLAG\_SEND\_STATUS**.</span></span> <span data-ttu-id="d6873-125">WMI 會將 [**IWbemObjectSink**](iwbemobjectsink.md)的 *lFlags* 參數設定為 **WBEM \_ 狀態 \_ 進度**，以報告呼叫的狀態。</span><span class="sxs-lookup"><span data-stu-id="d6873-125">WMI reports the status of your call by setting the *lFlags* parameter of [**IWbemObjectSink**](iwbemobjectsink.md) to **WBEM\_STATUS\_PROGRESS**.</span></span>

6.  <span data-ttu-id="d6873-126">如有必要，您可以呼叫 [**IWbemServices：： CancelCallAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) 方法，在 WMI 完成處理之前取消呼叫。</span><span class="sxs-lookup"><span data-stu-id="d6873-126">If necessary, you can cancel the call before WMI finishes processing by calling the [**IWbemServices::CancelCallAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) method.</span></span>

    <span data-ttu-id="d6873-127">[**CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall)方法會藉由立即釋出 [**IWbemObjectSink**](iwbemobjectsink.md)介面的指標來取消非同步處理，並保證在 **CancelAsyncCall** 傳回之前釋放指標。</span><span class="sxs-lookup"><span data-stu-id="d6873-127">The [**CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) method cancels asynchronous processing by immediately releasing the pointer to the [**IWbemObjectSink**](iwbemobjectsink.md) interface and guarantees that the pointer is released before **CancelAsyncCall** returns.</span></span>

    <span data-ttu-id="d6873-128">如果您使用執行 **IUnsecured** 介面的包裝函式物件來裝載 [**IWbemObjectSink**](iwbemobjectsink.md)，您可能會發現一些額外的複雜性。</span><span class="sxs-lookup"><span data-stu-id="d6873-128">If you are using a wrapper object implementing the **IUnsecured** interface to host [**IWbemObjectSink**](iwbemobjectsink.md), you may find some additional complications.</span></span> <span data-ttu-id="d6873-129">由於應用程式必須將相同的指標傳遞至在原始非同步呼叫中傳遞的 [**CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) ，因此應用程式必須在包裝函式物件之前保持不變，直到它清楚不需要取消。</span><span class="sxs-lookup"><span data-stu-id="d6873-129">Because the application must pass the same pointer to [**CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) that was passed in the original asynchronous call, the application must hold on to the wrapper object until it becomes clear that cancellation is not required.</span></span> <span data-ttu-id="d6873-130">如需詳細資訊，請參閱 [在非同步呼叫上設定安全性](setting-security-on-an-asynchronous-call.md)。</span><span class="sxs-lookup"><span data-stu-id="d6873-130">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

7.  <span data-ttu-id="d6873-131">完成時，請清除指標並關閉應用程式。</span><span class="sxs-lookup"><span data-stu-id="d6873-131">When finished, clean up pointers and shut down the application.</span></span>

    <span data-ttu-id="d6873-132">WMI 透過 [**SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) 方法提供最後的狀態呼叫。</span><span class="sxs-lookup"><span data-stu-id="d6873-132">WMI provides the final status call through the [**SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) method.</span></span>

    > [!Note]  
    > <span data-ttu-id="d6873-133">傳送最終狀態更新之後，WMI 會藉由呼叫實 [**IWbemObjectSink**](iwbemobjectsink.md)介面之類別的 **發行** 方法，來釋出物件接收。</span><span class="sxs-lookup"><span data-stu-id="d6873-133">After sending the final status update, WMI releases the object sink by calling the **Release** method for the class that implements the [**IWbemObjectSink**](iwbemobjectsink.md) interface.</span></span> <span data-ttu-id="d6873-134">在上述範例中，這是 **QuerySink：： Release** 方法。</span><span class="sxs-lookup"><span data-stu-id="d6873-134">In the previous example, this is the **QuerySink::Release** method.</span></span> <span data-ttu-id="d6873-135">如果您想要控制接收物件的存留期，您可以使用一個 (1) 的初始參考計數來執行接收器。</span><span class="sxs-lookup"><span data-stu-id="d6873-135">If you want to have control over the lifetime of the sink object, you can implement the sink with an initial reference count of one (1).</span></span>

     

    <span data-ttu-id="d6873-136">如果用戶端應用程式在兩個不同的重迭非同步呼叫中傳遞相同的接收介面，WMI 將無法保證回呼的順序。</span><span class="sxs-lookup"><span data-stu-id="d6873-136">If a client application passes the same sink interface in two different overlapping asynchronous calls, WMI does not guarantee the order of the callback.</span></span> <span data-ttu-id="d6873-137">進行重迭的非同步呼叫的用戶端應用程式應該傳遞不同的接收物件或序列化呼叫。</span><span class="sxs-lookup"><span data-stu-id="d6873-137">A client application making overlapping asynchronous calls should either pass different sink objects or serialize the calls.</span></span>

<span data-ttu-id="d6873-138">下列範例需要下列參考和 \# include 語句。</span><span class="sxs-lookup"><span data-stu-id="d6873-138">The following example requires the following reference and \#include statements.</span></span>


```C++
#include <iostream>
using namespace std;
#pragma comment(lib, "wbemuuid.lib")
#include <wbemidl.h>
```



<span data-ttu-id="d6873-139">下列範例說明如何使用 [**ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) 方法進行非同步查詢，但不會建立安全性設定或釋放 [**IWbemObjectSink**](iwbemobjectsink.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="d6873-139">The following example describes how to make an asynchronous query using the [**ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) method, but does not create security settings or release the [**IWbemObjectSink**](iwbemobjectsink.md) object.</span></span> <span data-ttu-id="d6873-140">如需詳細資訊，請參閱 [在非同步呼叫上設定安全性](setting-security-on-an-asynchronous-call.md)。</span><span class="sxs-lookup"><span data-stu-id="d6873-140">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>


```C++
// Set input parameters to ExecQueryAsync.
BSTR QueryLang = SysAllocString(L"WQL");
BSTR Query = SysAllocString(L"SELECT * FROM MyClass");

// Create IWbemObjectSink object and set pointer.
QuerySink *pSink = new QuerySink;

IWbemServices* pSvc = 0;

// Call ExecQueryAsync.
HRESULT hRes = pSvc->ExecQueryAsync(QueryLang, 
                                    Query, 
                                    0, 
                                    NULL, 
                                    pSink);

// Check for errors.
if (hRes)
{
    printf("ExecQueryAsync failed with = 0x%X\n", hRes);
    SysFreeString(QueryLang);
    SysFreeString(Query);
    delete pSink;    
    return ERROR;
}
```



> [!Note]  
> <span data-ttu-id="d6873-141">上述程式碼不會進行編譯而不會發生錯誤，因為尚未定義 **QuerySink** 類別。</span><span class="sxs-lookup"><span data-stu-id="d6873-141">The code above does not compile without error because the **QuerySink** class has not been defined.</span></span> <span data-ttu-id="d6873-142">如需 **QuerySink** 的詳細資訊，請參閱 [**IWbemObjectSink**](iwbemobjectsink.md)。</span><span class="sxs-lookup"><span data-stu-id="d6873-142">For more information about **QuerySink**, see [**IWbemObjectSink**](iwbemobjectsink.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="d6873-143">相關主題</span><span class="sxs-lookup"><span data-stu-id="d6873-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d6873-144">呼叫方法</span><span class="sxs-lookup"><span data-stu-id="d6873-144">Calling a Method</span></span>](calling-a-method.md)
</dt> </dl>

 

 
