---
description: 呼叫非同步方法
ms.assetid: 1d8688a5-d476-457d-a0ad-e4f106ac3484
title: 呼叫非同步方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4a53f5f0a3062ad6af955fbbfdd8cd05c82b30271cf680d6434bc652d567325
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959198"
---
# <a name="calling-asynchronous-methods"></a>呼叫非同步方法

在媒體基礎中，會以非同步方式執行許多作業。 非同步作業可改善效能，因為它們不會封鎖呼叫執行緒。 媒體基礎中的非同步作業是由一組具有命名慣例 **Begin ...** 和 **End**... 的方法所定義。 這兩個方法一起定義了串流上的非同步讀取作業。

若要啟動非同步作業，請呼叫 **Begin** 方法。 **Begin** 方法一律包含至少兩個參數：

-   [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback)介面的指標。 應用程式必須執行這個介面。
-   選擇性狀態物件的指標。

當作業完成時， [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) 介面會通知應用程式。 如需如何執行此介面的範例，請參閱 [執行非同步回呼](implementing-the-asynchronous-callback.md)。 狀態物件是選擇性的。 如果有指定，則必須執行 **IUnknown** 介面。 您可以使用 state 物件來儲存回呼所需的任何狀態資訊。 如果您不需要狀態資訊，可以將此參數設定為 **Null**。 **Begin** 方法可能包含該方法特定的其他參數。

如果 **Begin** 方法傳回失敗碼，表示作業立即失敗，而且不會叫用回呼。 如果 **Begin** 方法成功，則表示作業已暫止，並且會在作業完成時叫用回呼。

例如， [**IMFByteStream：： BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread) 方法會在位元組資料流程上啟動非同步讀取作業：


```C++
    BYTE data[DATA_SIZE];
    ULONG cbRead = 0;

    CMyCallback *pCB = new (std::nothrow) CMyCallback(pStream, &hr);

    if (pCB == NULL)
    {
        hr = E_OUTOFMEMORY;
    }

    // Start an asynchronous request to read data.
    if (SUCCEEDED(hr))
    {
        hr = pStream->BeginRead(data, DATA_SIZE, pCB, NULL);
    }
```



回呼方法是 [**IMFAsyncCallback：： Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke)。 它有單一參數 *pAsyncResult*，也就是 [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) 介面的指標。 若要完成非同步作業，請呼叫符合非同步 **Begin** 方法的 **End** 方法。 **End** 方法一律採用 **IMFAsyncResult** 指標。 一律傳入您在 **Invoke** 方法中收到的相同指標。 除非您呼叫 **End** 方法，否則非同步作業不會完成。 您可以從叫 **用方法內** 呼叫 End 方法，也可以從另一個執行緒呼叫 **End** 方法。

例如，若要在位元組資料流程上完成 [**IMFByteStream：： BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread) ，請呼叫 [**IMFByteStream：： EndRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-endread)：


```C++
    STDMETHODIMP Invoke(IMFAsyncResult* pResult)
    {
        m_hrStatus = m_pStream->EndRead(pResult, &m_cbRead);

        SetEvent(m_hEvent);

        return S_OK;
    }
```



**End** 方法的傳回值表示非同步作業的狀態。 在大部分情況下，您的應用程式會在非同步作業完成後執行某些工作，不論是否成功完成。 您有幾種選項：

-   在 [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) 方法內執行工作。 只要您的應用程式永遠不會封鎖呼叫執行緒或等候叫 **用方法內** 的任何內容，就可以接受這個方法。 如果您封鎖呼叫的執行緒，您可能會封鎖串流管線。 例如，您可能會更新某些狀態變數，但不會執行同步讀取作業或等候 mutex 物件。
-   在 [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) 方法中，設定事件並立即傳回。 應用程式的呼叫執行緒會等待事件，並在發出事件時執行工作。
-   [**在叫用方法中**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke)，將私用視窗訊息張貼至應用程式視窗，並立即傳回。 應用程式會在其訊息迴圈上執行工作。  (請務必透過呼叫 **PostMessage**（而非 **SendMessage**）來張貼訊息，因為 **SendMessage** 可以封鎖回呼執行緒。 ) 

請務必記住， [**調用**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) 是從另一個執行緒呼叫。 您的應用程式會負責確保在 **Invoke** 內執行的任何工作都是安全線程。

依預設，呼叫 [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) 的執行緒不會假設您的回呼物件行為。 （選擇性）您可以執行 [**IMFAsyncCallback：： GetParameters**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-getparameters) 方法，以傳回回呼執行的相關資訊。 否則，此方法可能會傳回 **E \_ >notimpl**：


```C++
    STDMETHODIMP GetParameters(DWORD* pdwFlags, DWORD* pdwQueue)
    {
        // Implementation of this method is optional.
        return E_NOTIMPL;
    }
```



如果您在 **Begin** 方法中指定了狀態物件，則可以藉由呼叫 [**IMFAsyncResult：： >getstate**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstate)，從回呼方法內取出它。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[非同步回呼方法](asynchronous-callback-methods.md)
</dt> </dl>

 

 



