---
title: 非同步模型
description: Windows Web 服務 API 中的大部分作業都可以同步或非同步方式執行。
ms.assetid: d0b3f154-2219-4085-a652-e9aeb126598c
keywords:
- 適用于 Windows 的非同步模型 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0c5e38dfbc0bc2ed397949da86f9a572a5b1ed5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106990877"
---
# <a name="asynchronous-model"></a><span data-ttu-id="44ab8-106">非同步模型</span><span class="sxs-lookup"><span data-stu-id="44ab8-106">Asynchronous Model</span></span>

<span data-ttu-id="44ab8-107">Windows Web 服務 API 中的大部分作業都可以同步或非同步方式執行。</span><span class="sxs-lookup"><span data-stu-id="44ab8-107">Most operations in Windows Web Services API can be performed synchronously or asynchronously.</span></span> <span data-ttu-id="44ab8-108">若要同步呼叫函式，請針對 [**WS \_ ASYNC \_ 內容**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) 結構傳遞 null 值。</span><span class="sxs-lookup"><span data-stu-id="44ab8-108">To call a function synchronously, pass a null value for the [**WS\_ASYNC\_CONTEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) structure.</span></span> <span data-ttu-id="44ab8-109">若要指定函式可能會以非同步方式執行，請將非 null 的 **WS \_ 非同步 \_ 內容** 傳遞給函數。</span><span class="sxs-lookup"><span data-stu-id="44ab8-109">To specify that a function may be performed asynchronously, pass a non-null **WS\_ASYNC\_CONTEXT** to the function.</span></span>

<span data-ttu-id="44ab8-110">非同步呼叫時，函式會以同步或非同步方式完成。</span><span class="sxs-lookup"><span data-stu-id="44ab8-110">When called asynchronously, a function can nevertheless complete synchronously or asynchronously.</span></span> <span data-ttu-id="44ab8-111">如果函式以同步方式完成，它會傳回指出最後一個成功或錯誤的值，而且此值一律是 **WS \_ S \_ ASYNC** 以外的值 (請參閱 [Windows Web 服務傳回值](windows-web-services-return-values.md)) 。</span><span class="sxs-lookup"><span data-stu-id="44ab8-111">If the function completes synchronously, it returns a value that indicates the final success or error, and this value is always something other than **WS\_S\_ASYNC** (See [Windows Web Services Return Values](windows-web-services-return-values.md)).</span></span> <span data-ttu-id="44ab8-112">但是，以 **\_ \_ 非同步** 方式傳回的值表示函式會以非同步方式完成。</span><span class="sxs-lookup"><span data-stu-id="44ab8-112">A return value of **WS\_S\_ASYNC**, however, indicates that the function will complete asynchronously.</span></span> <span data-ttu-id="44ab8-113">當函式以非同步方式完成時，會叫用回呼以指示作業完成。</span><span class="sxs-lookup"><span data-stu-id="44ab8-113">When the function completes asynchronously, a callback is invoked to signal completion of the operation.</span></span> <span data-ttu-id="44ab8-114">此回呼表示最後的成功或錯誤值。</span><span class="sxs-lookup"><span data-stu-id="44ab8-114">This callback indicates the final success or error value.</span></span> <span data-ttu-id="44ab8-115">如果作業同步完成，則不會呼叫回呼。</span><span class="sxs-lookup"><span data-stu-id="44ab8-115">The callback is not called if the operation completes synchronously.</span></span>

<span data-ttu-id="44ab8-116">若要建立異步內容，請初始化 [**WS \_ ASYNC \_ 內容**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context)結構的 **回呼** 和 **callbackState** 欄位。</span><span class="sxs-lookup"><span data-stu-id="44ab8-116">To create an asynchronous context, initialize the **callback** and **callbackState** fields of the [**WS\_ASYNC\_CONTEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) structure.</span></span> <span data-ttu-id="44ab8-117">**CallbackState** 欄位是用來指定傳遞至 [**WS \_ ASYNC \_ 回檔**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback)函數的使用者定義資料指標。</span><span class="sxs-lookup"><span data-stu-id="44ab8-117">The **callbackState** field is used to specify a pointer to user-defined data which is passed to the [**WS\_ASYNC\_CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback) function.</span></span>

<span data-ttu-id="44ab8-118">下列範例示範如何以非同步方式呼叫函式，方法是將指標傳遞至包含回呼的 [**WS \_ ASYNC \_ 內容**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) 結構，以及指向狀態資料的指標。</span><span class="sxs-lookup"><span data-stu-id="44ab8-118">The following example shows calling a function asynchronously by passing a pointer to a [**WS\_ASYNC\_CONTEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) structure that contains the callback and a pointer to the state data.</span></span>

``` syntax
HRESULT ExampleAsyncFunction(WS_ASYNC_CONTEXT* asyncContext);
void ExampleAsyncFunction()
{
    // Set up the WS_ASYNC_CONTEXT structure.
    MyState* myState = ...;  \\ Declare a pointer to user-defined data.
    WS_ASYNC_CONTEXT asyncContext;
    asyncContext.callback = MyCallback;  \\ Set the callback.
    asyncContext.callbackState = myState; \\ Set the pointer to the user-defined data.

    // Start the asynchronous operation
    HRESULT hr = SomeFunction(&asyncContext);

    if (hr == WS_S_ASYNC)
    {
        // The operation is completing asynchronously.  The callback is called 
        // when the operation is complete.
    }
    else
    {
        // The operation completed synchronously.  The callback is not called.
    }
}
void CALLBACK MyCallback(HRESULT hr, WS_CALLBACK_MODEL callbackModel, void* callbackState)
{
    MyState* myState = (MyState*)callbackState;

    // The operation completed asynchronously.
}
```

<span data-ttu-id="44ab8-119">非同步函式只會在函式呼叫期間使用 [**WS \_ ASYNC \_ 內容**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) 結構 (不會在非同步作業) 期間使用，因此您可以在堆疊上安全地宣告它。</span><span class="sxs-lookup"><span data-stu-id="44ab8-119">The [**WS\_ASYNC\_CONTEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) structure is used by the asynchronous function only for the duration of the function call (not for the duration of the asynchronous operation), so you can safely declare it on the stack.</span></span>

<span data-ttu-id="44ab8-120">如果任何其他參數（除了 [**WS \_ ASYNC \_ 內容**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) 結構以外）會以指標的形式傳遞至非同步函式，且函式會以非同步方式完成，則呼叫端必須負責保持這些參數所指向的值， (不會釋出) 直到叫用非同步回呼為止。</span><span class="sxs-lookup"><span data-stu-id="44ab8-120">If any other parameters, besides the [**WS\_ASYNC\_CONTEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) structure, are passed to an asynchronous function as pointers and the function completes asynchronously, it is the responsibility of the caller to keep the values pointed to by these parameters alive (not freed) until the asynchronous callback is invoked.</span></span>

<span data-ttu-id="44ab8-121">回呼可能執行的作業有一些限制。</span><span class="sxs-lookup"><span data-stu-id="44ab8-121">There are limitations on what operations a callback may perform.</span></span> <span data-ttu-id="44ab8-122">如需可能作業的詳細資訊，請參閱 [**WS \_ 回呼 \_ 模型**](/windows/desktop/api/WebServices/ne-webservices-ws_callback_model)。</span><span class="sxs-lookup"><span data-stu-id="44ab8-122">For more information on possible operations , see the [**WS\_CALLBACK\_MODEL**](/windows/desktop/api/WebServices/ne-webservices-ws_callback_model).</span></span>

<span data-ttu-id="44ab8-123">當您執行非同步函式時，請勿在非同步函式傳回給呼叫端之前，在呼叫非同步函式的相同執行緒上叫用回呼，因為這樣會中斷非同步模型。</span><span class="sxs-lookup"><span data-stu-id="44ab8-123">When you implement an asynchronous function, do not invoke the callback on the same thread that called the asynchronous function before the asynchronous function has returned to the caller, as this disrupts the asynchronous model.</span></span>

<span data-ttu-id="44ab8-124">在執行需要執行一連串非同步作業的函式時，請考慮使用 [**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) helper 函數。</span><span class="sxs-lookup"><span data-stu-id="44ab8-124">When implementing a function that needs to execute a series of asynchronous operations, consider using the [**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) helper function.</span></span>

<span data-ttu-id="44ab8-125">非同步函式 [範例](asyncmodelexample.md) 顯示如何執行和取用遵循非同步模型的函式。</span><span class="sxs-lookup"><span data-stu-id="44ab8-125">The [Asynchronous Function Example](asyncmodelexample.md) shows how to implement and consume functions that follow the asynchronous model.</span></span>

<span data-ttu-id="44ab8-126">啟動非同步 IO 作業會耗用系統資源。</span><span class="sxs-lookup"><span data-stu-id="44ab8-126">Starting an asynchronous IO operation consumes system resources.</span></span> <span data-ttu-id="44ab8-127">如果啟動足夠的 IO 作業，系統可能會變成沒有回應。</span><span class="sxs-lookup"><span data-stu-id="44ab8-127">If enough IO operations are started, the system can become unresponsive.</span></span> <span data-ttu-id="44ab8-128">若要避免這種情況，應用程式必須限制其啟動的非同步運算元目。</span><span class="sxs-lookup"><span data-stu-id="44ab8-128">To prevent this, an application needs to limit the number of asynchronous operations that it starts.</span></span>

<span data-ttu-id="44ab8-129">非同步模型會使用下列 API 元素。</span><span class="sxs-lookup"><span data-stu-id="44ab8-129">The asynchronous model uses the following API elements.</span></span>

| <span data-ttu-id="44ab8-130">回呼</span><span class="sxs-lookup"><span data-stu-id="44ab8-130">Callback</span></span>                                         | <span data-ttu-id="44ab8-131">Description</span><span class="sxs-lookup"><span data-stu-id="44ab8-131">Description</span></span>                                                                                                                           |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="44ab8-132">**WS \_ ASYNC \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="44ab8-132">**WS\_ASYNC\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback) | <span data-ttu-id="44ab8-133">用於非同步模型的回呼函數參數。</span><span class="sxs-lookup"><span data-stu-id="44ab8-133">The callback function parameter used with the asynchronous model.</span></span>                                                                     |
| [<span data-ttu-id="44ab8-134">**WS \_ ASYNC \_ 函數**</span><span class="sxs-lookup"><span data-stu-id="44ab8-134">**WS\_ASYNC\_FUNCTION**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_async_function) | <span data-ttu-id="44ab8-135">與 [**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) 搭配使用，以指定要在一系列非同步作業中叫用的下一個函數。</span><span class="sxs-lookup"><span data-stu-id="44ab8-135">Used with the [**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) to specify the next function to invoke in a series of asynchronous operations.</span></span> |



 



| <span data-ttu-id="44ab8-136">列舉型別</span><span class="sxs-lookup"><span data-stu-id="44ab8-136">Enumeration</span></span>                                      | <span data-ttu-id="44ab8-137">描述</span><span class="sxs-lookup"><span data-stu-id="44ab8-137">Description</span></span>                                                                                                       |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="44ab8-138">**WS \_ 回呼 \_ 模型**</span><span class="sxs-lookup"><span data-stu-id="44ab8-138">**WS\_CALLBACK\_MODEL**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_callback_model) | <span data-ttu-id="44ab8-139">指定回呼 (的執行緒行為，例如， [**WS \_ ASYNC \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback)) 。</span><span class="sxs-lookup"><span data-stu-id="44ab8-139">Specifies the threading behavior of a callback (for example, a [**WS\_ASYNC\_CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback)).</span></span> |



 



| <span data-ttu-id="44ab8-140">函式</span><span class="sxs-lookup"><span data-stu-id="44ab8-140">Function</span></span>                                 | <span data-ttu-id="44ab8-141">描述</span><span class="sxs-lookup"><span data-stu-id="44ab8-141">Description</span></span>                                                                                                                                                                    |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="44ab8-142">**WsAsyncExecute**</span><span class="sxs-lookup"><span data-stu-id="44ab8-142">**WsAsyncExecute**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) | <span data-ttu-id="44ab8-143">叫用使用者定義的回呼，該回呼可以起始非同步作業，並指出非同步作業完成時應呼叫的函式。</span><span class="sxs-lookup"><span data-stu-id="44ab8-143">Invokes a user-defined callback which can initiate an asynchronous operation and indicate a function that should be called when the asynchronous operation has been completed.</span></span> |



 



| <span data-ttu-id="44ab8-144">結構</span><span class="sxs-lookup"><span data-stu-id="44ab8-144">Structure</span></span>                                          | <span data-ttu-id="44ab8-145">Description</span><span class="sxs-lookup"><span data-stu-id="44ab8-145">Description</span></span>                                                                                                                           |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="44ab8-146">**WS \_ 非同步 \_ 內容**</span><span class="sxs-lookup"><span data-stu-id="44ab8-146">**WS\_ASYNC\_CONTEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_async_context)     | <span data-ttu-id="44ab8-147">指定非同步回呼以及使用者定義資料的指標，其將會傳遞至非同步回呼。</span><span class="sxs-lookup"><span data-stu-id="44ab8-147">Specifies the asynchronous callback and a pointer to user-defined data, which will be passed to the asynchronous callback.</span></span>            |
| [<span data-ttu-id="44ab8-148">**WS \_ 非同步 \_ 操作**</span><span class="sxs-lookup"><span data-stu-id="44ab8-148">**WS\_ASYNC\_OPERATION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_async_operation) | <span data-ttu-id="44ab8-149">與 [**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) 搭配使用，以指定要在一系列非同步作業中叫用的下一個函數。</span><span class="sxs-lookup"><span data-stu-id="44ab8-149">Used with the [**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) to specify the next function to invoke in a series of asynchronous operations.</span></span> |
| [<span data-ttu-id="44ab8-150">**WS \_ 非同步 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="44ab8-150">**WS\_ASYNC\_STATE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_async_state)         | <span data-ttu-id="44ab8-151">供 [**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) 用來管理非同步作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="44ab8-151">Used by [**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) to manage the state of an asynchronous operation.</span></span>                                    |



 

## <a name="related-topics"></a><span data-ttu-id="44ab8-152">相關主題</span><span class="sxs-lookup"><span data-stu-id="44ab8-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44ab8-153">非同步函式範例</span><span class="sxs-lookup"><span data-stu-id="44ab8-153">Asynchronous Function Example</span></span>](asyncmodelexample.md)
</dt> <dt>

[<span data-ttu-id="44ab8-154">**WS \_ ASYNC \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="44ab8-154">**WS\_ASYNC\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback)
</dt> <dt>

[<span data-ttu-id="44ab8-155">**WS \_ 非同步 \_ 內容**</span><span class="sxs-lookup"><span data-stu-id="44ab8-155">**WS\_ASYNC\_CONTEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_async_context)
</dt> <dt>

[<span data-ttu-id="44ab8-156">**WS \_ 回呼 \_ 模型**</span><span class="sxs-lookup"><span data-stu-id="44ab8-156">**WS\_CALLBACK\_MODEL**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_callback_model)
</dt> <dt>

[<span data-ttu-id="44ab8-157">**WsAsyncExecute**</span><span class="sxs-lookup"><span data-stu-id="44ab8-157">**WsAsyncExecute**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute)
</dt> </dl>

 

 




