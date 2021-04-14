---
description: 本主題說明如何在 Microsoft 媒體基礎中執行非同步方法。
ms.assetid: cd94280d-7267-4d35-8333-aa4a5bd81b73
title: 撰寫非同步方法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3d8360d0c15fe25661b8cd0f0f5adc9768db8ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320271"
---
# <a name="writing-an-asynchronous-method"></a>撰寫非同步方法

本主題說明如何在 Microsoft 媒體基礎中執行非同步方法。

非同步方法在媒體基礎管線中很普遍。 非同步方法可讓您更輕鬆地在多個執行緒之間散發工作。 以非同步方式執行 i/o 特別重要，因為從檔案或網路讀取時，不會封鎖管線的其餘部分。

如果您要撰寫媒體來源或媒體接收器，請務必正確處理非同步作業，因為您的元件效能會影響整個管線。

> [!Note]  
> 媒體基礎轉換 (MFTs) 預設使用同步方法。

 

### <a name="work-queues-for-asynchronous-operations"></a>非同步作業的工作佇列

在媒體基礎中， [非同步回呼方法](asynchronous-callback-methods.md) 與 [工作佇列](work-queues.md)之間會有接近的關聯性。 工作佇列是將工作從呼叫端的執行緒移至背景工作執行緒的抽象概念。 若要在工作佇列上執行工作，請執行下列動作：

1.  執行 [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) 介面。
2.  呼叫 [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) 來建立 *結果* 物件。 結果物件會公開 [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult)。 結果物件包含三個指標：

    -   呼叫端之 [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) 介面的指標。
    -   狀態物件的選擇性指標。 如果有指定，狀態物件必須執行 **IUnknown**。
    -   私用物件的選擇性指標。 如果有指定，這個物件也必須執行 **IUnknown**。

    最後兩個指標可以是 **Null**。 否則，請使用它們來保存非同步作業的相關資訊。

3.  呼叫 [**MFPutWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex) ，以將工作專案排入佇列。
4.  工作佇列執行緒會呼叫您的 [**IMFAsyncCallback：： Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) 方法。
5.  [**在叫用方法內**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke)進行工作。 此方法的 *pAsyncResult* 參數是步驟2中的 [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) 指標。 使用這個指標來取得狀態物件和私用物件：
    -   若要取得狀態物件，請呼叫 [**IMFAsyncResult：： >getstate**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstate)。
    -   若要取得私用物件，請呼叫 [**IMFAsyncResult：： GetObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getobject)。

或者，您可以藉由呼叫 [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) 函式來合併步驟2和3。 就內部而言，此函數會呼叫 [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) 來建立結果物件。

下圖顯示呼叫者、結果物件、狀態物件和私用物件之間的關聯性。

![顯示非同步結果物件的圖表](images/workqueues01.png)

下列順序圖表顯示物件如何將工作專案排在佇列中。 當工作佇列執行緒呼叫 [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke)時，物件會在該執行緒上執行非同步作業。

![顯示物件如何將工作專案排在佇列中的圖表](images/workqueues02.png)

請務必記住，從工作佇列所擁有的執行緒呼叫 [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) 。 您 **的叫** 用必須具備執行緒安全。 此外，如果您使用平臺工作佇列 (**MFASYNC \_ 回呼 \_ 佇列 \_ 標準**) ，您永遠都不會封鎖執行緒，因為這可能會封鎖整個媒體基礎管線，使其無法處理資料。 如果您需要執行將封鎖或需要很長時間才能完成的作業，請使用私用工作佇列。 若要建立私用工作佇列，請呼叫 [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue)。 任何執行 i/o 作業的管線元件，都應該避免因相同原因而封鎖 i/o 呼叫。 [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)介面提供適用于非同步檔案 i/o 的實用抽象概念。

### <a name="implementing-the-beginend-pattern"></a>執行 Begin. ../End.。。模式

如 [呼叫非同步方法](calling-asynchronous-methods.md)中所述，媒體基礎中的非同步方法通常會使用 **Begin ...** /**結束 ...** 模式。 在此模式中，非同步作業會使用兩種具有類似以下特徵的方法：

``` syntax
// Starts the asynchronous operation.
HRESULT BeginX(IMFAsyncCallback *pCallback, IUnknown *punkState);

// Completes the asynchronous operation. 
// Call this method from inside the caller's Invoke method.
HRESULT EndX(IMFAsyncResult *pResult);
```

若要讓方法成為真正的非同步方式， **BeginX** 的實，必須在另一個執行緒上執行實際的工作。 這是工作佇列進入圖片的位置。 在接下來的步驟中， *呼叫* 端是呼叫 **BeginX** 和 **EndX** 的程式碼。 這可能是應用程式或媒體基礎管線。 *元件* 是可執行 **BeginX** 和 **EndX** 的程式碼。

1.  呼叫端會呼叫 **Begin ...**，將指標撥入電話端的 [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) 介面。
2.  元件會建立新的非同步結果物件。 這個物件會儲存呼叫端的回呼介面和狀態物件。 一般來說，它也會儲存元件完成作業所需的任何私用狀態資訊。 此步驟中的結果物件在下圖中標示為「結果1」。
3.  元件會建立第二個結果物件。 此結果物件會儲存兩個指標：第一個結果物件和被呼叫端的回呼介面。 下圖中的這個結果物件會標示為「結果2」。
4.  元件會呼叫 [**MFPutWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex) ，以將新的工作專案排入佇列。
5.  在 [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) 方法中，此元件會執行非同步工作。
6.  元件會呼叫 [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback) 來叫用呼叫端的回呼方法。
7.  呼叫端會呼叫 **EndX** 方法。

![顯示物件如何實行開始/結束模式的圖表](images/workqueues03.png)

## <a name="asynchronous-method-example"></a>非同步方法範例

為了說明這段討論，我們將使用假設範例。 請考慮用來計算平方根的非同步方法：


```C++
    HRESULT BeginSquareRoot(double x, IMFAsyncCallback *pCB, IUnknown *pState);
    HRESULT EndSquareRoot(IMFAsyncResult *pResult, double *pVal);
```



的 *x* 參數 `BeginSquareRoot` 是將計算其平方根的值。 平方根會在的 *pVal* 參數中傳回 `EndSquareRoot` 。

以下是可執行這兩種方法的類別宣告：


```C++
class SqrRoot : public IMFAsyncCallback
{
    LONG    m_cRef;
    double  m_sqrt;

    HRESULT DoCalculateSquareRoot(AsyncOp *pOp);

public:

    SqrRoot() : m_cRef(1)
    {

    }

    HRESULT BeginSquareRoot(double x, IMFAsyncCallback *pCB, IUnknown *pState);
    HRESULT EndSquareRoot(IMFAsyncResult *pResult, double *pVal);

    // IUnknown methods.
    STDMETHODIMP QueryInterface(REFIID riid, void **ppv)
    {
        static const QITAB qit[] = 
        {
            QITABENT(SqrRoot, IMFAsyncCallback),
            { 0 }
        };
        return QISearch(this, qit, riid, ppv);
    }

    STDMETHODIMP_(ULONG) AddRef()
    {
        return InterlockedIncrement(&m_cRef);
    }

    STDMETHODIMP_(ULONG) Release()
    {
        LONG cRef = InterlockedDecrement(&m_cRef);
        if (cRef == 0)
        {
            delete this;
        }
        return cRef;
    }

    // IMFAsyncCallback methods.

    STDMETHODIMP GetParameters(DWORD* pdwFlags, DWORD* pdwQueue)
    {
        // Implementation of this method is optional.
        return E_NOTIMPL;  
    }
    // Invoke is where the work is performed.
    STDMETHODIMP Invoke(IMFAsyncResult* pResult);
};
```



`SqrRoot`類別會實 [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) ，讓它可以將平方根運算放在工作佇列上。 `DoCalculateSquareRoot`方法是計算平方根的私用類別方法。 將從工作佇列執行緒呼叫這個方法。

首先，我們需要一種方法來儲存 *x* 的值，以便在工作佇列執行緒呼叫時進行取出 `SqrRoot::Invoke` 。 以下是儲存資訊的簡單類別：


```C++
class AsyncOp : public IUnknown
{
    LONG    m_cRef;

public:

    double  m_value;

    AsyncOp(double val) : m_cRef(1), m_value(val) { }

    STDMETHODIMP QueryInterface(REFIID riid, void **ppv)
    {
        static const QITAB qit[] = 
        {
            QITABENT(AsyncOp, IUnknown),
            { 0 }
        };
        return QISearch(this, qit, riid, ppv);
    }

    STDMETHODIMP_(ULONG) AddRef()
    {
        return InterlockedIncrement(&m_cRef);
    }

    STDMETHODIMP_(ULONG) Release()
    {
        LONG cRef = InterlockedDecrement(&m_cRef);
        if (cRef == 0)
        {
            delete this;
        }
        return cRef;
    }
};
```



這個類別會執行 **IUnknown** ，以便將它儲存在結果物件中。

下列程式碼會 `BeginSquareRoot` 執行方法：


```C++
HRESULT SqrRoot::BeginSquareRoot(double x, IMFAsyncCallback *pCB, IUnknown *pState)
{
    AsyncOp *pOp = new (std::nothrow) AsyncOp(x);
    if (pOp == NULL)
    {
        return E_OUTOFMEMORY;
    }

    IMFAsyncResult *pResult = NULL;

    // Create the inner result object. This object contains pointers to:
    // 
    //   1. The caller's callback interface and state object. 
    //   2. The AsyncOp object, which contains the operation data.
    //

    HRESULT hr = MFCreateAsyncResult(pOp, pCB, pState, &pResult);

    if (SUCCEEDED(hr))
    {
        // Queue a work item. The work item contains pointers to:
        // 
        // 1. The callback interface of the SqrRoot object.
        // 2. The inner result object.

        hr = MFPutWorkItem(MFASYNC_CALLBACK_QUEUE_STANDARD, this, pResult);

        pResult->Release();
    }

    return hr;
}
```



此程式碼會執行以下動作：

1.  建立類別的新實例 `AsyncOp` ，以保存 *x* 的值。
2.  呼叫 [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) 來建立結果物件。 此物件包含數個指標：
    -   呼叫端之 [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) 介面的指標。
    -   呼叫端之狀態物件的指標， (*pState*) 。
    -   `AsyncOp` 物件的指標。
3.  呼叫 [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) 以將新的工作專案排入佇列。 此呼叫會以隱含方式建立外部結果物件，此物件會保存下列指標：
    -   `SqrRoot`物件之 [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback)介面的指標。
    -   步驟2中內部結果物件的指標。

下列程式碼會 `SqrRoot::Invoke` 執行方法：


```C++
// Invoke is called by the work queue. This is where the object performs the
// asynchronous operation.

STDMETHODIMP SqrRoot::Invoke(IMFAsyncResult* pResult)
{
    HRESULT hr = S_OK;

    IUnknown *pState = NULL;
    IUnknown *pUnk = NULL;
    IMFAsyncResult *pCallerResult = NULL;

    AsyncOp *pOp = NULL; 

    // Get the asynchronous result object for the application callback. 

    hr = pResult->GetState(&pState);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pState->QueryInterface(IID_PPV_ARGS(&pCallerResult));
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the object that holds the state information for the asynchronous method.
    hr = pCallerResult->GetObject(&pUnk);
    if (FAILED(hr))
    {
        goto done;
    }

    pOp = static_cast<AsyncOp*>(pUnk);

    // Do the work.

    hr = DoCalculateSquareRoot(pOp);

done:
    // Signal the application.
    if (pCallerResult)
    {
        pCallerResult->SetStatus(hr);
        MFInvokeCallback(pCallerResult);
    }

    SafeRelease(&pState);
    SafeRelease(&pUnk);
    SafeRelease(&pCallerResult);
    return S_OK;
}
```



這個方法會取得內部結果物件和 `AsyncOp` 物件。 然後，它會將 `AsyncOp` 物件傳遞至 `DoCalculateSquareRoot` 。 最後，它會呼叫 [**IMFAsyncResult：： SetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-setstatus) 來設定狀態碼和 [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback) ，以叫用呼叫端的回呼方法。

`DoCalculateSquareRoot`方法完全符合您的預期：


```C++
HRESULT SqrRoot::DoCalculateSquareRoot(AsyncOp *pOp)
{
    pOp->m_value = sqrt(pOp->m_value);

    return S_OK;
}
```



叫用呼叫端的回呼方法時，呼叫端會負責呼叫 **End ...** 方法（在此案例中 `EndSquareRoot` 為）。 `EndSquareRoot`是呼叫端如何捕獲非同步作業結果的方式，在此範例中為計算的平方根。 這項資訊會儲存在結果物件中：


```C++
HRESULT SqrRoot::EndSquareRoot(IMFAsyncResult *pResult, double *pVal)
{
    *pVal = 0;

    IUnknown *pUnk = NULL;

    HRESULT hr = pResult->GetStatus();

    if (FAILED(hr))
    {
        goto done;
    }

    hr = pResult->GetObject(&pUnk);
    if (FAILED(hr))
    {
        goto done;
    }

    AsyncOp *pOp = static_cast<AsyncOp*>(pUnk);

    // Get the result.
    *pVal = pOp->m_value;

done:
    SafeRelease(&pUnk);
    return hr;
}
```



## <a name="operation-queues"></a>作業佇列

到目前為止，tacitly 假設非同步作業可在任何時間完成，不論物件的目前狀態為何。 例如，假設當應用程式呼叫時，如果 `BeginSquareRoot` 先前呼叫相同的方法仍處於暫止狀態，會發生什麼事。 `SqrRoot`類別可能會在前一個工作專案完成之前將新的工作專案排在佇列中。 但是，工作佇列不保證會將工作專案序列化。 回想一下，工作佇列可以使用一個以上的執行緒來分派工作專案。 在多執行緒環境中，可能會在前一個工作專案完成之前叫用工作專案。 即使在叫用回呼之前發生內容切換，也可以依順序叫用工作專案。

基於這個理由，如果需要，則物件會負責自行序列化作業。 換句話說，如果物件需要作業 *a* 完成，才能啟動作業 *B* ，則在作業 *A* 完成之前，物件都不能將工作專案排入 *B* 的佇列。 物件可以透過自己的擱置作業佇列來滿足這項需求。 在物件上呼叫非同步方法時，物件會將要求放在它自己的佇列上。 當每個非同步作業完成時，物件會從佇列提取下一個要求。 [MPEG1Source 範例](mpeg1source-sample.md)顯示如何執行這類佇列的範例。

單一方法可能涉及數個非同步作業，特別是在使用 i/o 呼叫時。 當您執行非同步方法時，請仔細考慮序列化需求。 例如，當先前的 i/o 要求仍在擱置中時，物件是否可以啟動新的作業？ 如果新的作業變更了物件的內部狀態，則當先前的 i/o 要求完成時，會發生什麼事，並傳回可能已過時的資料？ 良好的狀態圖表有助於識別有效的狀態轉換。

## <a name="cross-thread-and-cross-process-considerations"></a>跨執行緒和跨進程的考慮

工作佇列不會使用 COM 封送處理來封送處理跨執行緒界限的介面指標。 因此，即使物件已註冊為單元執行緒，或應用程式執行緒已輸入單一執行緒的單元 (STA) ，也會從不同的執行緒叫用 [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) 回呼。 在任何情況下，所有媒體基礎管線元件都應該使用「兩者」執行緒模型。

媒體基礎中的某些介面會定義某些非同步方法的遠端版本。 當跨進程界限呼叫其中一個方法時，媒體基礎 proxy/stub DLL 會呼叫遠端版本的方法，此方法會執行方法參數的自訂封送處理。 在遠端進程中，存根會將呼叫轉譯回物件上的本機方法。 此程式對應用程式和遠端物件都是透明的。 這些自訂封送處理方法主要是針對在受保護媒體路徑中載入的物件 (PMP) 。 如需 PMP 的詳細資訊，請參閱 [受保護的媒體路徑](protected-media-path.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[非同步回呼方法](asynchronous-callback-methods.md)
</dt> <dt>

[工作佇列](work-queues.md)
</dt> </dl>

 

 



