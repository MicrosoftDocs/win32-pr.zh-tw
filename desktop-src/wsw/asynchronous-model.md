---
title: 非同步模型
description: Windows Web 服務 API 中的大部分作業都可以同步或非同步方式執行。
ms.assetid: d0b3f154-2219-4085-a652-e9aeb126598c
keywords:
- Windows 的非同步模型 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54cc59df90c37d8bad0ba3db145f9a4a61185c9577152215b027545bbea32494
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119344928"
---
# <a name="asynchronous-model"></a>非同步模型

Windows Web 服務 API 中的大部分作業都可以同步或非同步方式執行。 若要同步呼叫函式，請針對 [**WS \_ ASYNC \_ 內容**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) 結構傳遞 null 值。 若要指定函式可能會以非同步方式執行，請將非 null 的 **WS \_ 非同步 \_ 內容** 傳遞給函數。

非同步呼叫時，函式會以同步或非同步方式完成。 如果函式以同步方式完成，它會傳回指出最後一個成功或錯誤的值，而且此值一律是 **WS \_ S \_ ASYNC** 以外的值 (請參閱 [Windows Web 服務傳回值](windows-web-services-return-values.md)) 。 但是，以 **\_ \_ 非同步** 方式傳回的值表示函式會以非同步方式完成。 當函式以非同步方式完成時，會叫用回呼以指示作業完成。 此回呼表示最後的成功或錯誤值。 如果作業同步完成，則不會呼叫回呼。

若要建立異步內容，請初始化 [**WS \_ ASYNC \_ 內容**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context)結構的 **回呼** 和 **callbackState** 欄位。 **CallbackState** 欄位是用來指定傳遞至 [**WS \_ ASYNC \_ 回檔**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback)函數的使用者定義資料指標。

下列範例示範如何以非同步方式呼叫函式，方法是將指標傳遞至包含回呼的 [**WS \_ ASYNC \_ 內容**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) 結構，以及指向狀態資料的指標。

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

非同步函式只會在函式呼叫期間使用 [**WS \_ ASYNC \_ 內容**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) 結構 (不會在非同步作業) 期間使用，因此您可以在堆疊上安全地宣告它。

如果任何其他參數（除了 [**WS \_ ASYNC \_ 內容**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) 結構以外）會以指標的形式傳遞至非同步函式，且函式會以非同步方式完成，則呼叫端必須負責保持這些參數所指向的值， (不會釋出) 直到叫用非同步回呼為止。

回呼可能執行的作業有一些限制。 如需可能作業的詳細資訊，請參閱 [**WS \_ 回呼 \_ 模型**](/windows/desktop/api/WebServices/ne-webservices-ws_callback_model)。

當您執行非同步函式時，請勿在非同步函式傳回給呼叫端之前，在呼叫非同步函式的相同執行緒上叫用回呼，因為這樣會中斷非同步模型。

在執行需要執行一連串非同步作業的函式時，請考慮使用 [**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) helper 函數。

非同步函式 [範例](asyncmodelexample.md) 顯示如何執行和取用遵循非同步模型的函式。

啟動非同步 IO 作業會耗用系統資源。 如果啟動足夠的 IO 作業，系統可能會變成沒有回應。 若要避免這種情況，應用程式必須限制其啟動的非同步運算元目。

非同步模型會使用下列 API 元素。

| 回呼                                         | 描述                                                                                                                           |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**WS \_ ASYNC \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback) | 用於非同步模型的回呼函數參數。                                                                     |
| [**WS \_ ASYNC \_ 函數**](/windows/desktop/api/WebServices/nc-webservices-ws_async_function) | 與 [**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) 搭配使用，以指定要在一系列非同步作業中叫用的下一個函數。 |



 



| 列舉型別                                      | 描述                                                                                                       |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [**WS \_ 回呼 \_ 模型**](/windows/desktop/api/WebServices/ne-webservices-ws_callback_model) | 指定回呼 (的執行緒行為，例如， [**WS \_ ASYNC \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback)) 。 |



 



| 函式                                 | 描述                                                                                                                                                                    |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) | 叫用使用者定義的回呼，該回呼可以起始非同步作業，並指出非同步作業完成時應呼叫的函式。 |



 



| 結構                                          | 描述                                                                                                                           |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**WS \_ 非同步 \_ 內容**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context)     | 指定非同步回呼以及使用者定義資料的指標，其將會傳遞至非同步回呼。            |
| [**WS \_ 非同步 \_ 操作**](/windows/desktop/api/WebServices/ns-webservices-ws_async_operation) | 與 [**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) 搭配使用，以指定要在一系列非同步作業中叫用的下一個函數。 |
| [**WS \_ 非同步 \_ 狀態**](/windows/desktop/api/WebServices/ns-webservices-ws_async_state)         | 供 [**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) 用來管理非同步作業的狀態。                                    |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[非同步函式範例](asyncmodelexample.md)
</dt> <dt>

[**WS \_ ASYNC \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback)
</dt> <dt>

[**WS \_ 非同步 \_ 內容**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context)
</dt> <dt>

[**WS \_ 回呼 \_ 模型**](/windows/desktop/api/WebServices/ne-webservices-ws_callback_model)
</dt> <dt>

[**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute)
</dt> </dl>

 

 




