---
description: IWbemObjectSink 介面會建立接收介面，以接收 WMI 程式設計模型內的所有通知類型。
ms.assetid: 987aea1d-912a-4691-987f-181c1ef1a8a9
ms.tgt_platform: multiple
title: 'IWbemObjectSink 介面 (Wbemcli .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWbemObjectSink
api_type:
- COM
api_location:
- Fastprox.dll
ms.openlocfilehash: 980865605eadfd5e4cb61a511317dec7838b8e47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983428"
---
# <a name="iwbemobjectsink-interface"></a><span data-ttu-id="3e1c7-103">IWbemObjectSink 介面</span><span class="sxs-lookup"><span data-stu-id="3e1c7-103">IWbemObjectSink interface</span></span>

<span data-ttu-id="3e1c7-104">**IWbemObjectSink** 介面會建立接收介面，以接收 WMI 程式設計模型內的所有通知類型。</span><span class="sxs-lookup"><span data-stu-id="3e1c7-104">The **IWbemObjectSink** interface creates a sink interface that can receive all types of notifications within the WMI programming model.</span></span> <span data-ttu-id="3e1c7-105">用戶端必須執行這個介面，以接收 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)的 [非同步方法](making-an-asynchronous-call-with-c--.md)和特定類型的事件通知的結果。</span><span class="sxs-lookup"><span data-stu-id="3e1c7-105">Clients must implement this interface to receive both the results of the [asynchronous methods](making-an-asynchronous-call-with-c--.md) of [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices), and specific types of event notifications.</span></span> <span data-ttu-id="3e1c7-106">提供者會使用，但不會執行此介面將事件和物件提供給 WMI。</span><span class="sxs-lookup"><span data-stu-id="3e1c7-106">Providers use, but do not implement this interface to provide events and objects to WMI.</span></span>

<span data-ttu-id="3e1c7-107">一般而言，提供者會呼叫由 WMI 提供給它們的實作為。</span><span class="sxs-lookup"><span data-stu-id="3e1c7-107">Typically, providers call an implementation provided to them by WMI.</span></span> <span data-ttu-id="3e1c7-108">在這些情況下，呼叫 [**表示**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) 提供物件給 WMI 服務。</span><span class="sxs-lookup"><span data-stu-id="3e1c7-108">In these cases, call [**Indicate**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) to provide objects to the WMI service.</span></span> <span data-ttu-id="3e1c7-109">之後，請呼叫 [**SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) 來指出通知序列的結尾。</span><span class="sxs-lookup"><span data-stu-id="3e1c7-109">After that, call [**SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) to indicate the end of the notification sequence.</span></span> <span data-ttu-id="3e1c7-110">當接收沒有任何物件時，您也可以呼叫 **SetStatus** 來指出錯誤。</span><span class="sxs-lookup"><span data-stu-id="3e1c7-110">You can also call **SetStatus** to indicate errors when the sink does not have any objects.</span></span>

<span data-ttu-id="3e1c7-111">當您對 WMI 的非同步用戶端進行程式設計時，使用者會提供執行。</span><span class="sxs-lookup"><span data-stu-id="3e1c7-111">When programming asynchronous clients of WMI, the user provides the implementation.</span></span> <span data-ttu-id="3e1c7-112">WMI 會呼叫傳遞物件的方法，並設定結果的狀態。</span><span class="sxs-lookup"><span data-stu-id="3e1c7-112">WMI calls the methods to deliver objects and set the status of the result.</span></span>

> [!Note]  
> <span data-ttu-id="3e1c7-113">如果用戶端應用程式在兩個不同的重迭非同步呼叫中傳遞相同的接收介面，WMI 將無法保證回呼的順序。</span><span class="sxs-lookup"><span data-stu-id="3e1c7-113">If a client application passes the same sink interface in two different overlapping asynchronous calls, WMI does not guarantee the order of the callback.</span></span> <span data-ttu-id="3e1c7-114">進行重迭非同步呼叫的用戶端應用程式應該傳遞不同的接收物件，或序列化其呼叫。</span><span class="sxs-lookup"><span data-stu-id="3e1c7-114">Client applications that make overlapping asynchronous calls should either pass different sink objects, or serialize their calls.</span></span>

 

> [!Note]  
> <span data-ttu-id="3e1c7-115">由於回呼的回呼可能不會與用戶端所需的驗證層級傳回，因此建議您使用 [半同步] 而非 [非同步通訊]。</span><span class="sxs-lookup"><span data-stu-id="3e1c7-115">Because the call-back to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="3e1c7-116">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="3e1c7-116">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

## <a name="members"></a><span data-ttu-id="3e1c7-117">成員</span><span class="sxs-lookup"><span data-stu-id="3e1c7-117">Members</span></span>

<span data-ttu-id="3e1c7-118">**IWbemObjectSink** 介面具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="3e1c7-118">The **IWbemObjectSink** interface has these types of members:</span></span>

-   [<span data-ttu-id="3e1c7-119">方法</span><span class="sxs-lookup"><span data-stu-id="3e1c7-119">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="3e1c7-120">方法</span><span class="sxs-lookup"><span data-stu-id="3e1c7-120">Methods</span></span>

<span data-ttu-id="3e1c7-121">**IWbemObjectSink** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="3e1c7-121">The **IWbemObjectSink** interface has these methods.</span></span>



| <span data-ttu-id="3e1c7-122">方法</span><span class="sxs-lookup"><span data-stu-id="3e1c7-122">Method</span></span>                                         | <span data-ttu-id="3e1c7-123">描述</span><span class="sxs-lookup"><span data-stu-id="3e1c7-123">Description</span></span>                                                                                                             |
|:-----------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3e1c7-124">**表明**</span><span class="sxs-lookup"><span data-stu-id="3e1c7-124">**Indicate**</span></span>](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate)   | <span data-ttu-id="3e1c7-125">接收通知物件。</span><span class="sxs-lookup"><span data-stu-id="3e1c7-125">Receives notification objects.</span></span><br/>                                                                               |
| [<span data-ttu-id="3e1c7-126">**SetStatus**</span><span class="sxs-lookup"><span data-stu-id="3e1c7-126">**SetStatus**</span></span>](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) | <span data-ttu-id="3e1c7-127">由來源呼叫以指出通知順序的結尾，或將其他狀態碼傳送至接收。</span><span class="sxs-lookup"><span data-stu-id="3e1c7-127">Called by sources to indicate the end of a notification sequence, or to send other status codes to the sink.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3e1c7-128">備註</span><span class="sxs-lookup"><span data-stu-id="3e1c7-128">Remarks</span></span>

<span data-ttu-id="3e1c7-129">當 (**IWbemObjectSink** 或 [**IWbemEventSink**](iwbemeventsink.md)) 執行事件訂閱接收時，請勿從接收器物件的 [**指示**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) 或 [**SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) 方法內呼叫 WMI。</span><span class="sxs-lookup"><span data-stu-id="3e1c7-129">When implementing an event subscription sink (**IWbemObjectSink** or [**IWbemEventSink**](iwbemeventsink.md)), do not call into WMI from within the [**Indicate**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) or [**SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) methods on the sink object.</span></span> <span data-ttu-id="3e1c7-130">例如，呼叫 [**IWbemServices：： CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) 以從實作為中取消接收 [**，可能會**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) 干擾 WMI 狀態。</span><span class="sxs-lookup"><span data-stu-id="3e1c7-130">For example, calling [**IWbemServices::CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) to cancel the sink from within an implementation of [**Indicate**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) can interfere with the WMI state.</span></span> <span data-ttu-id="3e1c7-131">若要取消事件訂閱，請設定旗標，並從另一個執行緒或物件呼叫 **IWbemServices：： CancelAsyncCall** 。</span><span class="sxs-lookup"><span data-stu-id="3e1c7-131">To cancel an event subscription, set a flag and call **IWbemServices::CancelAsyncCall** from another thread or object.</span></span> <span data-ttu-id="3e1c7-132">對於與事件接收無關的執行（例如物件、列舉和查詢查詢），您可以回呼 WMI。</span><span class="sxs-lookup"><span data-stu-id="3e1c7-132">For implementations that are not related to an event sink, such as object, enum, and query retrievals, you can call back into WMI.</span></span>

<span data-ttu-id="3e1c7-133">接收程式應在100毫秒內處理事件通知，因為傳遞事件通知的 WMI 執行緒無法執行其他工作，直到接收物件處理完成為止。</span><span class="sxs-lookup"><span data-stu-id="3e1c7-133">Sink implementations should process the event notification within 100 MSEC because the WMI thread that delivers the event notification cannot do other work until the sink object has completed processing.</span></span> <span data-ttu-id="3e1c7-134">如果通知需要大量處理，接收端可以使用另一個執行緒的內部佇列來處理處理。</span><span class="sxs-lookup"><span data-stu-id="3e1c7-134">If the notification requires a large amount of processing, the sink can use an internal queue for another thread to handle the processing.</span></span>

## <a name="examples"></a><span data-ttu-id="3e1c7-135">範例</span><span class="sxs-lookup"><span data-stu-id="3e1c7-135">Examples</span></span>

<span data-ttu-id="3e1c7-136">下列程式碼範例是物件接收的簡單執行。</span><span class="sxs-lookup"><span data-stu-id="3e1c7-136">The following code example is a simple implementation of an object sink.</span></span> <span data-ttu-id="3e1c7-137">此範例可搭配 [**iwbemservices：： ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) 或 [**Iwbemservices：： CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) 使用，以接收傳回的實例：</span><span class="sxs-lookup"><span data-stu-id="3e1c7-137">This sample can be used with [**IWbemServices::ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) or [**IWbemServices::CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) to receive the returned instances:</span></span>


```C++
#include <iostream>
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")

class QuerySink : public IWbemObjectSink
{
    LONG m_lRef;
    bool bDone; 

public:
    QuerySink() { m_lRef = 0; }
   ~QuerySink() { bDone = TRUE; }

    virtual ULONG STDMETHODCALLTYPE AddRef();
    virtual ULONG STDMETHODCALLTYPE Release();        
    virtual HRESULT STDMETHODCALLTYPE 
        QueryInterface(REFIID riid, void** ppv);

    virtual HRESULT STDMETHODCALLTYPE Indicate( 
            /* [in] */
            LONG lObjectCount,
            /* [size_is][in] */
            IWbemClassObject __RPC_FAR *__RPC_FAR *apObjArray
            );
        
    virtual HRESULT STDMETHODCALLTYPE SetStatus( 
            /* [in] */ LONG lFlags,
            /* [in] */ HRESULT hResult,
            /* [in] */ BSTR strParam,
            /* [in] */ IWbemClassObject __RPC_FAR *pObjParam
            );
};


ULONG QuerySink::AddRef()
{
    return InterlockedIncrement(&m_lRef);
}

ULONG QuerySink::Release()
{
    LONG lRef = InterlockedDecrement(&m_lRef);
    if(lRef == 0)
        delete this;
    return lRef;
}

HRESULT QuerySink::QueryInterface(REFIID riid, void** ppv)
{
    if (riid == IID_IUnknown || riid == IID_IWbemObjectSink)
    {
        *ppv = (IWbemObjectSink *) this;
        AddRef();
        return WBEM_S_NO_ERROR;
    }
    else return E_NOINTERFACE;
}


HRESULT QuerySink::Indicate(long lObjCount, IWbemClassObject **pArray)
{
    for (long i = 0; i < lObjCount; i++)
    {
        IWbemClassObject *pObj = pArray[i];

        // ... use the object.

        // AddRef() is only required if the object will be held after
        // the return to the caller.
    }

    return WBEM_S_NO_ERROR;
}

HRESULT QuerySink::SetStatus(
            /* [in] */ LONG lFlags,
            /* [in] */ HRESULT hResult,
            /* [in] */ BSTR strParam,
            /* [in] */ IWbemClassObject __RPC_FAR *pObjParam
        )
{
    printf("QuerySink::SetStatus hResult = 0x%X\n", hResult);
    return WBEM_S_NO_ERROR;
}
```



## <a name="requirements"></a><span data-ttu-id="3e1c7-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="3e1c7-138">Requirements</span></span>



| <span data-ttu-id="3e1c7-139">需求</span><span class="sxs-lookup"><span data-stu-id="3e1c7-139">Requirement</span></span> | <span data-ttu-id="3e1c7-140">值</span><span class="sxs-lookup"><span data-stu-id="3e1c7-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e1c7-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3e1c7-141">Minimum supported client</span></span><br/> | <span data-ttu-id="3e1c7-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3e1c7-142">Windows Vista</span></span><br/>                                                                                 |
| <span data-ttu-id="3e1c7-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3e1c7-143">Minimum supported server</span></span><br/> | <span data-ttu-id="3e1c7-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3e1c7-144">Windows Server 2008</span></span><br/>                                                                           |
| <span data-ttu-id="3e1c7-145">標頭</span><span class="sxs-lookup"><span data-stu-id="3e1c7-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e1c7-146"><dt>Wbemcli (包含 Wbemidl) </dt></span><span class="sxs-lookup"><span data-stu-id="3e1c7-146"><dt>Wbemcli.h (include Wbemidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="3e1c7-147">程式庫</span><span class="sxs-lookup"><span data-stu-id="3e1c7-147">Library</span></span><br/>                  | <dl> <span data-ttu-id="3e1c7-148"><dt>Wbemuuid .lib</dt></span><span class="sxs-lookup"><span data-stu-id="3e1c7-148"><dt>Wbemuuid.lib</dt></span></span> </dl>                  |
| <span data-ttu-id="3e1c7-149">DLL</span><span class="sxs-lookup"><span data-stu-id="3e1c7-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e1c7-150"><dt>Fastprox.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e1c7-150"><dt>Fastprox.dll</dt></span></span> </dl>                  |



## <a name="see-also"></a><span data-ttu-id="3e1c7-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3e1c7-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e1c7-152">適用于 WMI 的 COM API</span><span class="sxs-lookup"><span data-stu-id="3e1c7-152">COM API for WMI</span></span>](com-api-for-wmi.md)
</dt> <dt>

[<span data-ttu-id="3e1c7-153">使用 c + + 進行非同步呼叫</span><span class="sxs-lookup"><span data-stu-id="3e1c7-153">Making an Asynchronous Call with C++</span></span>](making-an-asynchronous-call-with-c--.md)
</dt> <dt>

[<span data-ttu-id="3e1c7-154">在非同步呼叫上設定安全性</span><span class="sxs-lookup"><span data-stu-id="3e1c7-154">Setting Security on an Asynchronous Call</span></span>](setting-security-on-an-asynchronous-call.md)
</dt> <dt>

[<span data-ttu-id="3e1c7-155">在您的應用程式期間接收事件</span><span class="sxs-lookup"><span data-stu-id="3e1c7-155">Receiving Events for the Duration of your Application</span></span>](receiving-events-for-the-duration-of-your-application.md)
</dt> </dl>

 

 




