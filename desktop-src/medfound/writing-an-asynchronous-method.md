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
# <a name="writing-an-asynchronous-method"></a><span data-ttu-id="475f8-103">撰寫非同步方法</span><span class="sxs-lookup"><span data-stu-id="475f8-103">Writing an Asynchronous Method</span></span>

<span data-ttu-id="475f8-104">本主題說明如何在 Microsoft 媒體基礎中執行非同步方法。</span><span class="sxs-lookup"><span data-stu-id="475f8-104">This topic describes how to implement an asynchronous method in Microsoft Media Foundation.</span></span>

<span data-ttu-id="475f8-105">非同步方法在媒體基礎管線中很普遍。</span><span class="sxs-lookup"><span data-stu-id="475f8-105">Asynchronous methods are ubiquitous in the Media Foundation pipeline.</span></span> <span data-ttu-id="475f8-106">非同步方法可讓您更輕鬆地在多個執行緒之間散發工作。</span><span class="sxs-lookup"><span data-stu-id="475f8-106">Asynchronous methods make it easier to distribute work among several threads.</span></span> <span data-ttu-id="475f8-107">以非同步方式執行 i/o 特別重要，因為從檔案或網路讀取時，不會封鎖管線的其餘部分。</span><span class="sxs-lookup"><span data-stu-id="475f8-107">It is particularly important to perform I/O asynchronously, so that reading from a file or network does not block the rest of the pipeline.</span></span>

<span data-ttu-id="475f8-108">如果您要撰寫媒體來源或媒體接收器，請務必正確處理非同步作業，因為您的元件效能會影響整個管線。</span><span class="sxs-lookup"><span data-stu-id="475f8-108">If you are writing a media source or media sink, it is crucial to handle asynchronous operations correctly, because your component's performance has an impact on the entire pipeline.</span></span>

> [!Note]  
> <span data-ttu-id="475f8-109">媒體基礎轉換 (MFTs) 預設使用同步方法。</span><span class="sxs-lookup"><span data-stu-id="475f8-109">Media Foundation transforms (MFTs) use synchronous methods by default.</span></span>

 

### <a name="work-queues-for-asynchronous-operations"></a><span data-ttu-id="475f8-110">非同步作業的工作佇列</span><span class="sxs-lookup"><span data-stu-id="475f8-110">Work Queues For Asynchronous Operations</span></span>

<span data-ttu-id="475f8-111">在媒體基礎中， [非同步回呼方法](asynchronous-callback-methods.md) 與 [工作佇列](work-queues.md)之間會有接近的關聯性。</span><span class="sxs-lookup"><span data-stu-id="475f8-111">In Media Foundation, there is a close relationship between [Asynchronous Callback Methods](asynchronous-callback-methods.md) and [Work Queues](work-queues.md).</span></span> <span data-ttu-id="475f8-112">工作佇列是將工作從呼叫端的執行緒移至背景工作執行緒的抽象概念。</span><span class="sxs-lookup"><span data-stu-id="475f8-112">A work queue is an abstraction for moving work from the caller's thread to a worker thread.</span></span> <span data-ttu-id="475f8-113">若要在工作佇列上執行工作，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="475f8-113">To perform work on a work queue, do the following:</span></span>

1.  <span data-ttu-id="475f8-114">執行 [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) 介面。</span><span class="sxs-lookup"><span data-stu-id="475f8-114">Implement the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span>
2.  <span data-ttu-id="475f8-115">呼叫 [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) 來建立 *結果* 物件。</span><span class="sxs-lookup"><span data-stu-id="475f8-115">Call [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) to create a *result* object.</span></span> <span data-ttu-id="475f8-116">結果物件會公開 [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult)。</span><span class="sxs-lookup"><span data-stu-id="475f8-116">The result object exposes the [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult).</span></span> <span data-ttu-id="475f8-117">結果物件包含三個指標：</span><span class="sxs-lookup"><span data-stu-id="475f8-117">The result object contains three pointers:</span></span>

    -   <span data-ttu-id="475f8-118">呼叫端之 [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="475f8-118">A pointer to the caller's [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span>
    -   <span data-ttu-id="475f8-119">狀態物件的選擇性指標。</span><span class="sxs-lookup"><span data-stu-id="475f8-119">An optional pointer to a state object.</span></span> <span data-ttu-id="475f8-120">如果有指定，狀態物件必須執行 **IUnknown**。</span><span class="sxs-lookup"><span data-stu-id="475f8-120">If specified, the state object must implement **IUnknown**.</span></span>
    -   <span data-ttu-id="475f8-121">私用物件的選擇性指標。</span><span class="sxs-lookup"><span data-stu-id="475f8-121">An optional pointer to a private object.</span></span> <span data-ttu-id="475f8-122">如果有指定，這個物件也必須執行 **IUnknown**。</span><span class="sxs-lookup"><span data-stu-id="475f8-122">If specified, this object also must implement **IUnknown**.</span></span>

    <span data-ttu-id="475f8-123">最後兩個指標可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="475f8-123">The last two pointers can be **NULL**.</span></span> <span data-ttu-id="475f8-124">否則，請使用它們來保存非同步作業的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="475f8-124">Otherwise, use them to hold information about the asynchronous operation.</span></span>

3.  <span data-ttu-id="475f8-125">呼叫 [**MFPutWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex) ，以將工作專案排入佇列。</span><span class="sxs-lookup"><span data-stu-id="475f8-125">Call [**MFPutWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex) to queue to the work item.</span></span>
4.  <span data-ttu-id="475f8-126">工作佇列執行緒會呼叫您的 [**IMFAsyncCallback：： Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) 方法。</span><span class="sxs-lookup"><span data-stu-id="475f8-126">The work-queue thread calls your [**IMFAsyncCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method.</span></span>
5.  <span data-ttu-id="475f8-127">[**在叫用方法內**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke)進行工作。</span><span class="sxs-lookup"><span data-stu-id="475f8-127">Do the work inside your [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method.</span></span> <span data-ttu-id="475f8-128">此方法的 *pAsyncResult* 參數是步驟2中的 [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) 指標。</span><span class="sxs-lookup"><span data-stu-id="475f8-128">The *pAsyncResult* parameter of this method is the [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) pointer from step 2.</span></span> <span data-ttu-id="475f8-129">使用這個指標來取得狀態物件和私用物件：</span><span class="sxs-lookup"><span data-stu-id="475f8-129">Use this pointer to get the state object and private object:</span></span>
    -   <span data-ttu-id="475f8-130">若要取得狀態物件，請呼叫 [**IMFAsyncResult：： >getstate**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstate)。</span><span class="sxs-lookup"><span data-stu-id="475f8-130">To get the state object, call [**IMFAsyncResult::GetState**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstate).</span></span>
    -   <span data-ttu-id="475f8-131">若要取得私用物件，請呼叫 [**IMFAsyncResult：： GetObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getobject)。</span><span class="sxs-lookup"><span data-stu-id="475f8-131">To get the private object, call [**IMFAsyncResult::GetObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getobject).</span></span>

<span data-ttu-id="475f8-132">或者，您可以藉由呼叫 [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) 函式來合併步驟2和3。</span><span class="sxs-lookup"><span data-stu-id="475f8-132">As an alternative, you can combine steps 2 and 3 by calling the [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) function.</span></span> <span data-ttu-id="475f8-133">就內部而言，此函數會呼叫 [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) 來建立結果物件。</span><span class="sxs-lookup"><span data-stu-id="475f8-133">Internally, this function calls [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) to create the result object.</span></span>

<span data-ttu-id="475f8-134">下圖顯示呼叫者、結果物件、狀態物件和私用物件之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="475f8-134">The following diagram shows the relationships between the caller, the result object, the state object, and the private object.</span></span>

![顯示非同步結果物件的圖表](images/workqueues01.png)

<span data-ttu-id="475f8-136">下列順序圖表顯示物件如何將工作專案排在佇列中。</span><span class="sxs-lookup"><span data-stu-id="475f8-136">The following sequence diagram shows how an object queues a work item.</span></span> <span data-ttu-id="475f8-137">當工作佇列執行緒呼叫 [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke)時，物件會在該執行緒上執行非同步作業。</span><span class="sxs-lookup"><span data-stu-id="475f8-137">When the work-queue thread calls [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke), the object performs the asynchronous operation on that thread.</span></span>

![顯示物件如何將工作專案排在佇列中的圖表](images/workqueues02.png)

<span data-ttu-id="475f8-139">請務必記住，從工作佇列所擁有的執行緒呼叫 [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) 。</span><span class="sxs-lookup"><span data-stu-id="475f8-139">It is important to remember [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) is called from a thread that is owned by the work queue.</span></span> <span data-ttu-id="475f8-140">您 **的叫** 用必須具備執行緒安全。</span><span class="sxs-lookup"><span data-stu-id="475f8-140">Your implementation of **Invoke** must be thread safe.</span></span> <span data-ttu-id="475f8-141">此外，如果您使用平臺工作佇列 (**MFASYNC \_ 回呼 \_ 佇列 \_ 標準**) ，您永遠都不會封鎖執行緒，因為這可能會封鎖整個媒體基礎管線，使其無法處理資料。</span><span class="sxs-lookup"><span data-stu-id="475f8-141">In addition, if you use the platform work queue (**MFASYNC\_CALLBACK\_QUEUE\_STANDARD**), it is critical that you never block the thread, because that can block the entire Media Foundation pipeline from processing data.</span></span> <span data-ttu-id="475f8-142">如果您需要執行將封鎖或需要很長時間才能完成的作業，請使用私用工作佇列。</span><span class="sxs-lookup"><span data-stu-id="475f8-142">If you need to perform an operation that will block or take a long time to complete, use a private work queue.</span></span> <span data-ttu-id="475f8-143">若要建立私用工作佇列，請呼叫 [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue)。</span><span class="sxs-lookup"><span data-stu-id="475f8-143">To create a private work queue, call [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue).</span></span> <span data-ttu-id="475f8-144">任何執行 i/o 作業的管線元件，都應該避免因相同原因而封鎖 i/o 呼叫。</span><span class="sxs-lookup"><span data-stu-id="475f8-144">Any pipeline component that performs I/O operations should avoid blocking I/O calls for the same reason.</span></span> <span data-ttu-id="475f8-145">[**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)介面提供適用于非同步檔案 i/o 的實用抽象概念。</span><span class="sxs-lookup"><span data-stu-id="475f8-145">The [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) interface provides a useful abstraction for asynchronous file I/O.</span></span>

### <a name="implementing-the-beginend-pattern"></a><span data-ttu-id="475f8-146">執行 Begin. ../End.。。模式</span><span class="sxs-lookup"><span data-stu-id="475f8-146">Implementing the Begin.../End... Pattern</span></span>

<span data-ttu-id="475f8-147">如 [呼叫非同步方法](calling-asynchronous-methods.md)中所述，媒體基礎中的非同步方法通常會使用 **Begin ...** /**結束 ...** 模式。</span><span class="sxs-lookup"><span data-stu-id="475f8-147">As described in [Calling Asynchronous Methods](calling-asynchronous-methods.md), asynchronous methods in Media Foundation often use the **Begin...**/**End....** pattern.</span></span> <span data-ttu-id="475f8-148">在此模式中，非同步作業會使用兩種具有類似以下特徵的方法：</span><span class="sxs-lookup"><span data-stu-id="475f8-148">In this pattern, an asynchronous operation uses two methods with signatures similar to the following:</span></span>

``` syntax
// Starts the asynchronous operation.
HRESULT BeginX(IMFAsyncCallback *pCallback, IUnknown *punkState);

// Completes the asynchronous operation. 
// Call this method from inside the caller's Invoke method.
HRESULT EndX(IMFAsyncResult *pResult);
```

<span data-ttu-id="475f8-149">若要讓方法成為真正的非同步方式， **BeginX** 的實，必須在另一個執行緒上執行實際的工作。</span><span class="sxs-lookup"><span data-stu-id="475f8-149">To make the method truly asynchronous, the implementation of **BeginX** must perform the actual work on another thread.</span></span> <span data-ttu-id="475f8-150">這是工作佇列進入圖片的位置。</span><span class="sxs-lookup"><span data-stu-id="475f8-150">This is where work queues come into the picture.</span></span> <span data-ttu-id="475f8-151">在接下來的步驟中， *呼叫* 端是呼叫 **BeginX** 和 **EndX** 的程式碼。</span><span class="sxs-lookup"><span data-stu-id="475f8-151">In the steps that follow, the *caller* is the code that calls **BeginX** and **EndX**.</span></span> <span data-ttu-id="475f8-152">這可能是應用程式或媒體基礎管線。</span><span class="sxs-lookup"><span data-stu-id="475f8-152">This might be an application or the Media Foundation pipeline.</span></span> <span data-ttu-id="475f8-153">*元件* 是可執行 **BeginX** 和 **EndX** 的程式碼。</span><span class="sxs-lookup"><span data-stu-id="475f8-153">The *component* is the code that implements **BeginX** and **EndX**.</span></span>

1.  <span data-ttu-id="475f8-154">呼叫端會呼叫 **Begin ...**，將指標撥入電話端的 [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) 介面。</span><span class="sxs-lookup"><span data-stu-id="475f8-154">The caller calls **Begin...**, passing in a pointer to the caller's [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span>
2.  <span data-ttu-id="475f8-155">元件會建立新的非同步結果物件。</span><span class="sxs-lookup"><span data-stu-id="475f8-155">The component creates a new asynchronous result object.</span></span> <span data-ttu-id="475f8-156">這個物件會儲存呼叫端的回呼介面和狀態物件。</span><span class="sxs-lookup"><span data-stu-id="475f8-156">This object stores the caller's callback interface and state object.</span></span> <span data-ttu-id="475f8-157">一般來說，它也會儲存元件完成作業所需的任何私用狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="475f8-157">Typically, it also stores any private state information that the component needs to complete the operation.</span></span> <span data-ttu-id="475f8-158">此步驟中的結果物件在下圖中標示為「結果1」。</span><span class="sxs-lookup"><span data-stu-id="475f8-158">The result object from this step is labeled "Result 1" in the next diagram.</span></span>
3.  <span data-ttu-id="475f8-159">元件會建立第二個結果物件。</span><span class="sxs-lookup"><span data-stu-id="475f8-159">The component creates a second result object.</span></span> <span data-ttu-id="475f8-160">此結果物件會儲存兩個指標：第一個結果物件和被呼叫端的回呼介面。</span><span class="sxs-lookup"><span data-stu-id="475f8-160">This result object stores two pointers: The first result object, and the callback interface of the callee.</span></span> <span data-ttu-id="475f8-161">下圖中的這個結果物件會標示為「結果2」。</span><span class="sxs-lookup"><span data-stu-id="475f8-161">This result object is labeled "Result 2" in the next diagram.</span></span>
4.  <span data-ttu-id="475f8-162">元件會呼叫 [**MFPutWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex) ，以將新的工作專案排入佇列。</span><span class="sxs-lookup"><span data-stu-id="475f8-162">The component calls [**MFPutWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex) to queue a new work item.</span></span>
5.  <span data-ttu-id="475f8-163">在 [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) 方法中，此元件會執行非同步工作。</span><span class="sxs-lookup"><span data-stu-id="475f8-163">In the [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method, the component does the asynchronous work.</span></span>
6.  <span data-ttu-id="475f8-164">元件會呼叫 [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback) 來叫用呼叫端的回呼方法。</span><span class="sxs-lookup"><span data-stu-id="475f8-164">The component calls [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback) to invoke the caller's callback method.</span></span>
7.  <span data-ttu-id="475f8-165">呼叫端會呼叫 **EndX** 方法。</span><span class="sxs-lookup"><span data-stu-id="475f8-165">The caller calls the **EndX** method.</span></span>

![顯示物件如何實行開始/結束模式的圖表](images/workqueues03.png)

## <a name="asynchronous-method-example"></a><span data-ttu-id="475f8-167">非同步方法範例</span><span class="sxs-lookup"><span data-stu-id="475f8-167">Asynchronous Method Example</span></span>

<span data-ttu-id="475f8-168">為了說明這段討論，我們將使用假設範例。</span><span class="sxs-lookup"><span data-stu-id="475f8-168">To illustrate this discussion, we will use a contrived example.</span></span> <span data-ttu-id="475f8-169">請考慮用來計算平方根的非同步方法：</span><span class="sxs-lookup"><span data-stu-id="475f8-169">Consider an asynchronous method for computing a square root:</span></span>


```C++
    HRESULT BeginSquareRoot(double x, IMFAsyncCallback *pCB, IUnknown *pState);
    HRESULT EndSquareRoot(IMFAsyncResult *pResult, double *pVal);
```



<span data-ttu-id="475f8-170">的 *x* 參數 `BeginSquareRoot` 是將計算其平方根的值。</span><span class="sxs-lookup"><span data-stu-id="475f8-170">The *x* parameter of `BeginSquareRoot` is the value whose square root will be calculated.</span></span> <span data-ttu-id="475f8-171">平方根會在的 *pVal* 參數中傳回 `EndSquareRoot` 。</span><span class="sxs-lookup"><span data-stu-id="475f8-171">The square root is returned in the *pVal* parameter of `EndSquareRoot`.</span></span>

<span data-ttu-id="475f8-172">以下是可執行這兩種方法的類別宣告：</span><span class="sxs-lookup"><span data-stu-id="475f8-172">Here is the declaration of a class that implements these two methods:</span></span>


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



<span data-ttu-id="475f8-173">`SqrRoot`類別會實 [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) ，讓它可以將平方根運算放在工作佇列上。</span><span class="sxs-lookup"><span data-stu-id="475f8-173">The `SqrRoot` class implements [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) so that it can put the square root operation on a work queue.</span></span> <span data-ttu-id="475f8-174">`DoCalculateSquareRoot`方法是計算平方根的私用類別方法。</span><span class="sxs-lookup"><span data-stu-id="475f8-174">The `DoCalculateSquareRoot` method is the private class method that calculates the square root.</span></span> <span data-ttu-id="475f8-175">將從工作佇列執行緒呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="475f8-175">This method will be called from the work queue thread.</span></span>

<span data-ttu-id="475f8-176">首先，我們需要一種方法來儲存 *x* 的值，以便在工作佇列執行緒呼叫時進行取出 `SqrRoot::Invoke` 。</span><span class="sxs-lookup"><span data-stu-id="475f8-176">First, we need a way to store the value of *x*, so that it can be retrieved when the work queue thread calls `SqrRoot::Invoke`.</span></span> <span data-ttu-id="475f8-177">以下是儲存資訊的簡單類別：</span><span class="sxs-lookup"><span data-stu-id="475f8-177">Here is a simple class that stores the information:</span></span>


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



<span data-ttu-id="475f8-178">這個類別會執行 **IUnknown** ，以便將它儲存在結果物件中。</span><span class="sxs-lookup"><span data-stu-id="475f8-178">This class implements **IUnknown** so that it can be stored in a result object.</span></span>

<span data-ttu-id="475f8-179">下列程式碼會 `BeginSquareRoot` 執行方法：</span><span class="sxs-lookup"><span data-stu-id="475f8-179">The following code implements the `BeginSquareRoot` method:</span></span>


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



<span data-ttu-id="475f8-180">此程式碼會執行以下動作：</span><span class="sxs-lookup"><span data-stu-id="475f8-180">This code does the following:</span></span>

1.  <span data-ttu-id="475f8-181">建立類別的新實例 `AsyncOp` ，以保存 *x* 的值。</span><span class="sxs-lookup"><span data-stu-id="475f8-181">Creates a new instance of the `AsyncOp` class to hold the value of *x*.</span></span>
2.  <span data-ttu-id="475f8-182">呼叫 [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) 來建立結果物件。</span><span class="sxs-lookup"><span data-stu-id="475f8-182">Calls [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) to create a result object.</span></span> <span data-ttu-id="475f8-183">此物件包含數個指標：</span><span class="sxs-lookup"><span data-stu-id="475f8-183">This object holds several pointers:</span></span>
    -   <span data-ttu-id="475f8-184">呼叫端之 [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="475f8-184">A pointer to the caller's [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span>
    -   <span data-ttu-id="475f8-185">呼叫端之狀態物件的指標， (*pState*) 。</span><span class="sxs-lookup"><span data-stu-id="475f8-185">A pointer to the caller's state object (*pState*).</span></span>
    -   <span data-ttu-id="475f8-186">`AsyncOp` 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="475f8-186">A pointer to the `AsyncOp` object.</span></span>
3.  <span data-ttu-id="475f8-187">呼叫 [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) 以將新的工作專案排入佇列。</span><span class="sxs-lookup"><span data-stu-id="475f8-187">Calls [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) to queue a new work item.</span></span> <span data-ttu-id="475f8-188">此呼叫會以隱含方式建立外部結果物件，此物件會保存下列指標：</span><span class="sxs-lookup"><span data-stu-id="475f8-188">This call implicitly creates an outer result object, which holds the following pointers:</span></span>
    -   <span data-ttu-id="475f8-189">`SqrRoot`物件之 [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="475f8-189">A pointer to the `SqrRoot` object's [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span>
    -   <span data-ttu-id="475f8-190">步驟2中內部結果物件的指標。</span><span class="sxs-lookup"><span data-stu-id="475f8-190">A pointer to the inner result object from step 2.</span></span>

<span data-ttu-id="475f8-191">下列程式碼會 `SqrRoot::Invoke` 執行方法：</span><span class="sxs-lookup"><span data-stu-id="475f8-191">The following code implements the `SqrRoot::Invoke` method:</span></span>


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



<span data-ttu-id="475f8-192">這個方法會取得內部結果物件和 `AsyncOp` 物件。</span><span class="sxs-lookup"><span data-stu-id="475f8-192">This method gets the inner result object and the `AsyncOp` object.</span></span> <span data-ttu-id="475f8-193">然後，它會將 `AsyncOp` 物件傳遞至 `DoCalculateSquareRoot` 。</span><span class="sxs-lookup"><span data-stu-id="475f8-193">Then it passes the `AsyncOp` object to `DoCalculateSquareRoot`.</span></span> <span data-ttu-id="475f8-194">最後，它會呼叫 [**IMFAsyncResult：： SetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-setstatus) 來設定狀態碼和 [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback) ，以叫用呼叫端的回呼方法。</span><span class="sxs-lookup"><span data-stu-id="475f8-194">Finally, it calls [**IMFAsyncResult::SetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-setstatus) to set the status code and [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback) to invoke the caller's callback method.</span></span>

<span data-ttu-id="475f8-195">`DoCalculateSquareRoot`方法完全符合您的預期：</span><span class="sxs-lookup"><span data-stu-id="475f8-195">The `DoCalculateSquareRoot` method does exactly what you would expect:</span></span>


```C++
HRESULT SqrRoot::DoCalculateSquareRoot(AsyncOp *pOp)
{
    pOp->m_value = sqrt(pOp->m_value);

    return S_OK;
}
```



<span data-ttu-id="475f8-196">叫用呼叫端的回呼方法時，呼叫端會負責呼叫 **End ...** 方法（在此案例中 `EndSquareRoot` 為）。</span><span class="sxs-lookup"><span data-stu-id="475f8-196">When the caller's callback method is invoked, it is the caller's responsibility to call the **End...** method—in this case, `EndSquareRoot`.</span></span> <span data-ttu-id="475f8-197">`EndSquareRoot`是呼叫端如何捕獲非同步作業結果的方式，在此範例中為計算的平方根。</span><span class="sxs-lookup"><span data-stu-id="475f8-197">The `EndSquareRoot` is how the caller retrieves the result of the asynchronous operation, which in this example is the computed square root.</span></span> <span data-ttu-id="475f8-198">這項資訊會儲存在結果物件中：</span><span class="sxs-lookup"><span data-stu-id="475f8-198">This information is stored in the result object:</span></span>


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



## <a name="operation-queues"></a><span data-ttu-id="475f8-199">作業佇列</span><span class="sxs-lookup"><span data-stu-id="475f8-199">Operation Queues</span></span>

<span data-ttu-id="475f8-200">到目前為止，tacitly 假設非同步作業可在任何時間完成，不論物件的目前狀態為何。</span><span class="sxs-lookup"><span data-stu-id="475f8-200">So far, it has been tacitly assumed that an asynchronous operation could be done at any time, regardless of the object's current state.</span></span> <span data-ttu-id="475f8-201">例如，假設當應用程式呼叫時，如果 `BeginSquareRoot` 先前呼叫相同的方法仍處於暫止狀態，會發生什麼事。</span><span class="sxs-lookup"><span data-stu-id="475f8-201">For example, consider what happens if an application calls `BeginSquareRoot` while an earlier call to the same method is still pending.</span></span> <span data-ttu-id="475f8-202">`SqrRoot`類別可能會在前一個工作專案完成之前將新的工作專案排在佇列中。</span><span class="sxs-lookup"><span data-stu-id="475f8-202">The `SqrRoot` class might queue the new work item before the previous work item is done.</span></span> <span data-ttu-id="475f8-203">但是，工作佇列不保證會將工作專案序列化。</span><span class="sxs-lookup"><span data-stu-id="475f8-203">However, work queues are not guaranteed to serialize work items.</span></span> <span data-ttu-id="475f8-204">回想一下，工作佇列可以使用一個以上的執行緒來分派工作專案。</span><span class="sxs-lookup"><span data-stu-id="475f8-204">Recall that a work queue can use more than one thread to dispatch work items.</span></span> <span data-ttu-id="475f8-205">在多執行緒環境中，可能會在前一個工作專案完成之前叫用工作專案。</span><span class="sxs-lookup"><span data-stu-id="475f8-205">In a multithreaded environment, a work item might be invoked before the previous one has completed.</span></span> <span data-ttu-id="475f8-206">即使在叫用回呼之前發生內容切換，也可以依順序叫用工作專案。</span><span class="sxs-lookup"><span data-stu-id="475f8-206">Work items can even be invoked out of order, if a context switch happens to occur just before the callback is invoked.</span></span>

<span data-ttu-id="475f8-207">基於這個理由，如果需要，則物件會負責自行序列化作業。</span><span class="sxs-lookup"><span data-stu-id="475f8-207">For this reason, it is the object's responsibility to serialize operations on itself, if required.</span></span> <span data-ttu-id="475f8-208">換句話說，如果物件需要作業 *a* 完成，才能啟動作業 *B* ，則在作業 *A* 完成之前，物件都不能將工作專案排入 *B* 的佇列。</span><span class="sxs-lookup"><span data-stu-id="475f8-208">In other words, if the object requires operation *A* to finish before operation *B* can start, the object must not queue a work item for *B* until operation *A* has completed.</span></span> <span data-ttu-id="475f8-209">物件可以透過自己的擱置作業佇列來滿足這項需求。</span><span class="sxs-lookup"><span data-stu-id="475f8-209">An object can meet this requirement by having its own queue of pending operations.</span></span> <span data-ttu-id="475f8-210">在物件上呼叫非同步方法時，物件會將要求放在它自己的佇列上。</span><span class="sxs-lookup"><span data-stu-id="475f8-210">When an asynchronous method is called on the object, the object puts the request on its own queue.</span></span> <span data-ttu-id="475f8-211">當每個非同步作業完成時，物件會從佇列提取下一個要求。</span><span class="sxs-lookup"><span data-stu-id="475f8-211">As each asynchronous operation is completed, the object pulls the next request from the queue.</span></span> <span data-ttu-id="475f8-212">[MPEG1Source 範例](mpeg1source-sample.md)顯示如何執行這類佇列的範例。</span><span class="sxs-lookup"><span data-stu-id="475f8-212">The [MPEG1Source Sample](mpeg1source-sample.md) shows an example of how to implement such a queue.</span></span>

<span data-ttu-id="475f8-213">單一方法可能涉及數個非同步作業，特別是在使用 i/o 呼叫時。</span><span class="sxs-lookup"><span data-stu-id="475f8-213">A single method might involve several asynchronous operations, particularly when I/O calls are used.</span></span> <span data-ttu-id="475f8-214">當您執行非同步方法時，請仔細考慮序列化需求。</span><span class="sxs-lookup"><span data-stu-id="475f8-214">When you implement asynchronous methods, think carefully about serialization requirements.</span></span> <span data-ttu-id="475f8-215">例如，當先前的 i/o 要求仍在擱置中時，物件是否可以啟動新的作業？</span><span class="sxs-lookup"><span data-stu-id="475f8-215">For example, is it valid for the object to start a new operation while a previous I/O request is still pending?</span></span> <span data-ttu-id="475f8-216">如果新的作業變更了物件的內部狀態，則當先前的 i/o 要求完成時，會發生什麼事，並傳回可能已過時的資料？</span><span class="sxs-lookup"><span data-stu-id="475f8-216">If the new operation changes the object's internal state, what happens when a previous I/O request completes and returns data that might now be stale?</span></span> <span data-ttu-id="475f8-217">良好的狀態圖表有助於識別有效的狀態轉換。</span><span class="sxs-lookup"><span data-stu-id="475f8-217">A good state diagram can help to identify the valid state transitions.</span></span>

## <a name="cross-thread-and-cross-process-considerations"></a><span data-ttu-id="475f8-218">跨執行緒和跨進程的考慮</span><span class="sxs-lookup"><span data-stu-id="475f8-218">Cross-Thread and Cross-Process Considerations</span></span>

<span data-ttu-id="475f8-219">工作佇列不會使用 COM 封送處理來封送處理跨執行緒界限的介面指標。</span><span class="sxs-lookup"><span data-stu-id="475f8-219">Work queues do not use COM marshaling to marshal interface pointers across thread boundaries.</span></span> <span data-ttu-id="475f8-220">因此，即使物件已註冊為單元執行緒，或應用程式執行緒已輸入單一執行緒的單元 (STA) ，也會從不同的執行緒叫用 [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) 回呼。</span><span class="sxs-lookup"><span data-stu-id="475f8-220">Therefore, even if an object is registered as apartment-threaded or the application thread has entered a single-threaded apartment (STA), [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) callbacks will be invoked from a different thread.</span></span> <span data-ttu-id="475f8-221">在任何情況下，所有媒體基礎管線元件都應該使用「兩者」執行緒模型。</span><span class="sxs-lookup"><span data-stu-id="475f8-221">In any case, all Media Foundation pipeline components should use the "Both" threading model.</span></span>

<span data-ttu-id="475f8-222">媒體基礎中的某些介面會定義某些非同步方法的遠端版本。</span><span class="sxs-lookup"><span data-stu-id="475f8-222">Some interfaces in Media Foundation define remote versions of some asynchronous methods.</span></span> <span data-ttu-id="475f8-223">當跨進程界限呼叫其中一個方法時，媒體基礎 proxy/stub DLL 會呼叫遠端版本的方法，此方法會執行方法參數的自訂封送處理。</span><span class="sxs-lookup"><span data-stu-id="475f8-223">When one of these methods is called across process boundaries, the Media Foundation proxy/stub DLL calls the remote version of the method, which performs custom marshaling of the method parameters.</span></span> <span data-ttu-id="475f8-224">在遠端進程中，存根會將呼叫轉譯回物件上的本機方法。</span><span class="sxs-lookup"><span data-stu-id="475f8-224">In the remote process, the stub translates the call back into the local method on the object.</span></span> <span data-ttu-id="475f8-225">此程式對應用程式和遠端物件都是透明的。</span><span class="sxs-lookup"><span data-stu-id="475f8-225">This process is transparent to both the application and the remote object.</span></span> <span data-ttu-id="475f8-226">這些自訂封送處理方法主要是針對在受保護媒體路徑中載入的物件 (PMP) 。</span><span class="sxs-lookup"><span data-stu-id="475f8-226">These custom marshaling methods are provided primarily for objects that are loaded in the protected media path (PMP).</span></span> <span data-ttu-id="475f8-227">如需 PMP 的詳細資訊，請參閱 [受保護的媒體路徑](protected-media-path.md)。</span><span class="sxs-lookup"><span data-stu-id="475f8-227">For more information about the PMP, see [Protected Media Path](protected-media-path.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="475f8-228">相關主題</span><span class="sxs-lookup"><span data-stu-id="475f8-228">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="475f8-229">非同步回呼方法</span><span class="sxs-lookup"><span data-stu-id="475f8-229">Asynchronous Callback Methods</span></span>](asynchronous-callback-methods.md)
</dt> <dt>

[<span data-ttu-id="475f8-230">工作佇列</span><span class="sxs-lookup"><span data-stu-id="475f8-230">Work Queues</span></span>](work-queues.md)
</dt> </dl>

 

 



