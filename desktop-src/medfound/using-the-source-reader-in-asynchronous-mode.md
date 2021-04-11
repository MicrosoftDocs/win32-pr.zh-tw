---
description: 本主題說明如何使用非同步模式的來源讀取器。
ms.assetid: 9D3C2780-D7DB-4151-8474-9A19EC94F6BE
title: 使用非同步模式的來源讀取器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 357d0405cb3e594d059b7c93e793250e0be88562
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026387"
---
# <a name="using-the-source-reader-in-asynchronous-mode"></a><span data-ttu-id="b450b-103">使用非同步模式的來源讀取器</span><span class="sxs-lookup"><span data-stu-id="b450b-103">Using the Source Reader in Asynchronous Mode</span></span>

<span data-ttu-id="b450b-104">本主題說明如何使用非同步模式的 [來源讀取器](source-reader.md) 。</span><span class="sxs-lookup"><span data-stu-id="b450b-104">This topic describes how to use the [Source Reader](source-reader.md) in asynchronous mode.</span></span> <span data-ttu-id="b450b-105">在非同步模式中，應用程式會提供回呼介面，用來通知應用程式有可用的資料。</span><span class="sxs-lookup"><span data-stu-id="b450b-105">In asynchronous mode, the application provides a callback interface, which is used to notify the application that data is available.</span></span>

<span data-ttu-id="b450b-106">本主題假設您已閱讀 [使用來源讀取程式來處理媒體資料](processing-media-data-with-the-source-reader.md)的主題。</span><span class="sxs-lookup"><span data-stu-id="b450b-106">This topic assumes that you have already read the topic [Using the Source Reader to Process Media Data](processing-media-data-with-the-source-reader.md).</span></span>

## <a name="using-asynchronous-mode"></a><span data-ttu-id="b450b-107">使用非同步模式</span><span class="sxs-lookup"><span data-stu-id="b450b-107">Using Asynchronous Mode</span></span>

<span data-ttu-id="b450b-108">來源讀取器在同步模式或非同步模式下運作。</span><span class="sxs-lookup"><span data-stu-id="b450b-108">The Source Reader operates either in synchronous mode or asynchronous mode.</span></span> <span data-ttu-id="b450b-109">上一節中所示的程式碼範例假設來源讀取器使用同步模式，這是預設值。</span><span class="sxs-lookup"><span data-stu-id="b450b-109">The code example shown in the previous section assumes that the Source Reader is using synchronous mode, which is the default.</span></span> <span data-ttu-id="b450b-110">在同步模式中， [**IMFSourceReader：： ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) 方法會在媒體來源產生下一個範例時封鎖。</span><span class="sxs-lookup"><span data-stu-id="b450b-110">In synchronous mode, the [**IMFSourceReader::ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) method blocks while the media source produces the next sample.</span></span> <span data-ttu-id="b450b-111">媒體來源通常會從某些外部來源 (（例如本機檔案或網路連線) ）取得資料，因此方法可以封鎖呼叫執行緒一段明顯的時間。</span><span class="sxs-lookup"><span data-stu-id="b450b-111">A media source typically acquires data from some external source (such as a local file or a network connection), so the method can block the calling thread for a noticeable amount of time.</span></span>

<span data-ttu-id="b450b-112">在非同步模式中， [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) 會立即傳回，而工作會在另一個執行緒上執行。</span><span class="sxs-lookup"><span data-stu-id="b450b-112">In asynchronous mode, the [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) returns immediately and the work is performed on another thread.</span></span> <span data-ttu-id="b450b-113">作業完成之後，來源讀取器會透過 [**IMFSourceReaderCallback**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereadercallback) 回呼介面呼叫應用程式。</span><span class="sxs-lookup"><span data-stu-id="b450b-113">After the operation is complete, the Source Reader calls the application through the [**IMFSourceReaderCallback**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereadercallback) callback interface.</span></span> <span data-ttu-id="b450b-114">若要使用非同步模式，您必須在第一次建立來源讀取器時提供回呼指標，如下所示：</span><span class="sxs-lookup"><span data-stu-id="b450b-114">To use asynchronous mode, you must provide a callback pointer when you first create the Source Reader, as follows:</span></span>

1.  <span data-ttu-id="b450b-115">藉由呼叫 [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) 函數來建立屬性存放區。</span><span class="sxs-lookup"><span data-stu-id="b450b-115">Create an attribute store by calling the [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) function.</span></span>
2.  <span data-ttu-id="b450b-116">在屬性存放區上設定 [MF \_ 來源 \_ 讀取器 \_ 非同步 \_ 回呼](mf-source-reader-async-callback.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="b450b-116">Set the [MF\_SOURCE\_READER\_ASYNC\_CALLBACK](mf-source-reader-async-callback.md) attribute on the attribute store.</span></span> <span data-ttu-id="b450b-117">屬性值是您回呼物件的指標。</span><span class="sxs-lookup"><span data-stu-id="b450b-117">The attribute value is a pointer to your callback object.</span></span>
3.  <span data-ttu-id="b450b-118">當您建立來源讀取器時，請將屬性存放區傳遞給 *pAttributes* 參數中的建立函數。</span><span class="sxs-lookup"><span data-stu-id="b450b-118">When you create the Source Reader, pass the attribute store to the creation function in the *pAttributes* parameter.</span></span> <span data-ttu-id="b450b-119">所有用來建立來源讀取器的函式都有此參數。</span><span class="sxs-lookup"><span data-stu-id="b450b-119">All of the functions to create the Source Reader have this parameter.</span></span>

<span data-ttu-id="b450b-120">下列範例會示範這些步驟。</span><span class="sxs-lookup"><span data-stu-id="b450b-120">The following example shows these steps.</span></span>


```C++
HRESULT CreateSourceReaderAsync(
    PCWSTR pszURL, 
    IMFSourceReaderCallback *pCallback, 
    IMFSourceReader **ppReader)
{
    HRESULT hr = S_OK;
    IMFAttributes *pAttributes = NULL;

    hr = MFCreateAttributes(&pAttributes, 1);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pAttributes->SetUnknown(MF_SOURCE_READER_ASYNC_CALLBACK, pCallback);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = MFCreateSourceReaderFromURL(pszURL, pAttributes, ppReader);

done:
    SafeRelease(&pAttributes);
    return hr;
}
```



<span data-ttu-id="b450b-121">建立來源讀取器之後，您就無法在同步和非同步之間切換模式。</span><span class="sxs-lookup"><span data-stu-id="b450b-121">After you create the Source Reader, you cannot switch modes between synchronous and asynchronous.</span></span>

<span data-ttu-id="b450b-122">若要以非同步模式取得資料，請呼叫 [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) 方法，但將最後四個參數設定為 **Null**，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="b450b-122">To get data in asynchronous mode, call the [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) method but set the last four parameters to **NULL**, as shown in the following example.</span></span>


```C++
    // Request the first sample.
    hr = pReader->ReadSample(MF_SOURCE_READER_FIRST_VIDEO_STREAM, 
        0, NULL, NULL, NULL, NULL);
```



<span data-ttu-id="b450b-123">當 [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) 方法以非同步方式完成時，來源讀取器會呼叫您的 [**IMFSourceReaderCallback：： OnReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) 方法。</span><span class="sxs-lookup"><span data-stu-id="b450b-123">When the [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) method completes asynchronously, the Source Reader calls your [**IMFSourceReaderCallback::OnReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) method.</span></span> <span data-ttu-id="b450b-124">這個方法有五個參數：</span><span class="sxs-lookup"><span data-stu-id="b450b-124">This method has five parameters:</span></span>

-   <span data-ttu-id="b450b-125">*hrStatus*：包含 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="b450b-125">*hrStatus*: Contains an **HRESULT** value.</span></span> <span data-ttu-id="b450b-126">這是 [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) 會在同步模式中傳回的相同值。</span><span class="sxs-lookup"><span data-stu-id="b450b-126">This is the same value that [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) would return in synchronous mode.</span></span> <span data-ttu-id="b450b-127">如果 *hrStatus* 包含錯誤碼，您可以忽略其餘的參數。</span><span class="sxs-lookup"><span data-stu-id="b450b-127">If *hrStatus* contains an error code, you can ignore the remaining parameters.</span></span>
-   <span data-ttu-id="b450b-128">*dwStreamIndex*、 *dwStreamFlags*、llTimestamp 和 *pSample*：這三個參數相當於 [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample)中的最後三個參數。</span><span class="sxs-lookup"><span data-stu-id="b450b-128">*dwStreamIndex*, *dwStreamFlags*, llTimestamp, and *pSample*: These three parameters are equivalent to the last three parameters in [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample).</span></span> <span data-ttu-id="b450b-129">它們分別包含串流號碼、狀態旗標和 [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) 指標。</span><span class="sxs-lookup"><span data-stu-id="b450b-129">They contain the stream number, status flags, and [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) pointer, respectively.</span></span>


```C++
    STDMETHODIMP OnReadSample(HRESULT hrStatus, DWORD dwStreamIndex,
        DWORD dwStreamFlags, LONGLONG llTimestamp, IMFSample *pSample);
```



<span data-ttu-id="b450b-130">此外，回呼介面會定義其他兩種方法：</span><span class="sxs-lookup"><span data-stu-id="b450b-130">In addition, the callback interface defines two other methods:</span></span>

-   <span data-ttu-id="b450b-131">[**OnEvent**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onevent)。</span><span class="sxs-lookup"><span data-stu-id="b450b-131">[**OnEvent**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onevent).</span></span> <span data-ttu-id="b450b-132">當媒體來源中發生特定事件（例如緩衝或網路連接事件）時，通知應用程式。</span><span class="sxs-lookup"><span data-stu-id="b450b-132">Notifies the application when certain events occur in media source, such as buffering or network connection events.</span></span>
-   <span data-ttu-id="b450b-133">[**OnFlush**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onflush)。</span><span class="sxs-lookup"><span data-stu-id="b450b-133">[**OnFlush**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onflush).</span></span> <span data-ttu-id="b450b-134">當 [**Flush**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-flush) 方法完成時呼叫。</span><span class="sxs-lookup"><span data-stu-id="b450b-134">Called when the [**Flush**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-flush) method completes.</span></span>

## <a name="implementing-the-callback-interface"></a><span data-ttu-id="b450b-135">執行回呼介面</span><span class="sxs-lookup"><span data-stu-id="b450b-135">Implementing the Callback Interface</span></span>

<span data-ttu-id="b450b-136">回呼介面必須是安全線程，因為從背景工作執行緒呼叫 [**OnReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) 和其他回呼方法。</span><span class="sxs-lookup"><span data-stu-id="b450b-136">The callback interface must be thread-safe, because [**OnReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) and the other callback methods are called from worker threads.</span></span>

<span data-ttu-id="b450b-137">當您執行回呼時，有幾種不同的方法可以採用。</span><span class="sxs-lookup"><span data-stu-id="b450b-137">There are several different approaches you can take when you implement the callback.</span></span> <span data-ttu-id="b450b-138">例如，您可以在回呼內執行所有工作，也可以使用回呼來通知應用程式 (例如，藉由向事件控制碼發出信號，) 然後從應用程式執行緒執行工作。</span><span class="sxs-lookup"><span data-stu-id="b450b-138">For example, you can do all of the work inside the callback, or you can use the callback to notify the application (for example, by signaling an event handle) and then do work from the application thread.</span></span>

<span data-ttu-id="b450b-139">針對您對 [**IMFSourceReader：： ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample)方法所進行的每個呼叫，將會呼叫 [**OnReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample)方法一次。</span><span class="sxs-lookup"><span data-stu-id="b450b-139">The [**OnReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) method will be called once for every call that you make to the [**IMFSourceReader::ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) method.</span></span> <span data-ttu-id="b450b-140">若要取得下一個範例，請再次呼叫 **ReadSample** 。</span><span class="sxs-lookup"><span data-stu-id="b450b-140">To get the next sample, call **ReadSample** again.</span></span> <span data-ttu-id="b450b-141">如果發生錯誤，則會以 *hrStatus* 參數的錯誤碼來呼叫 **OnReadSample** 。</span><span class="sxs-lookup"><span data-stu-id="b450b-141">If an error occurs, **OnReadSample** is called with an error code for the *hrStatus* parameter.</span></span>

<span data-ttu-id="b450b-142">下列範例顯示回呼介面的最基本實作為。</span><span class="sxs-lookup"><span data-stu-id="b450b-142">The following example shows a minimal implementation of the callback interface.</span></span> <span data-ttu-id="b450b-143">首先，以下是執行介面之類別的宣告。</span><span class="sxs-lookup"><span data-stu-id="b450b-143">First, here is the declaration of a class that implements the interface.</span></span>


```C++
#include <shlwapi.h>

class SourceReaderCB : public IMFSourceReaderCallback
{
public:
    SourceReaderCB(HANDLE hEvent) : 
      m_nRefCount(1), m_hEvent(hEvent), m_bEOS(FALSE), m_hrStatus(S_OK)
    {
        InitializeCriticalSection(&m_critsec);
    }

    // IUnknown methods
    STDMETHODIMP QueryInterface(REFIID iid, void** ppv)
    {
        static const QITAB qit[] =
        {
            QITABENT(SourceReaderCB, IMFSourceReaderCallback),
            { 0 },
        };
        return QISearch(this, qit, iid, ppv);
    }
    STDMETHODIMP_(ULONG) AddRef()
    {
        return InterlockedIncrement(&m_nRefCount);
    }
    STDMETHODIMP_(ULONG) Release()
    {
        ULONG uCount = InterlockedDecrement(&m_nRefCount);
        if (uCount == 0)
        {
            delete this;
        }
        return uCount;
    }

    // IMFSourceReaderCallback methods
    STDMETHODIMP OnReadSample(HRESULT hrStatus, DWORD dwStreamIndex,
        DWORD dwStreamFlags, LONGLONG llTimestamp, IMFSample *pSample);

    STDMETHODIMP OnEvent(DWORD, IMFMediaEvent *)
    {
        return S_OK;
    }

    STDMETHODIMP OnFlush(DWORD)
    {
        return S_OK;
    }

public:
    HRESULT Wait(DWORD dwMilliseconds, BOOL *pbEOS)
    {
        *pbEOS = FALSE;

        DWORD dwResult = WaitForSingleObject(m_hEvent, dwMilliseconds);
        if (dwResult == WAIT_TIMEOUT)
        {
            return E_PENDING;
        }
        else if (dwResult != WAIT_OBJECT_0)
        {
            return HRESULT_FROM_WIN32(GetLastError());
        }

        *pbEOS = m_bEOS;
        return m_hrStatus;
    }
    
private:
    
    // Destructor is private. Caller should call Release.
    virtual ~SourceReaderCB() 
    {
    }

    void NotifyError(HRESULT hr)
    {
        wprintf(L"Source Reader error: 0x%X\n", hr);
    }

private:
    long                m_nRefCount;        // Reference count.
    CRITICAL_SECTION    m_critsec;
    HANDLE              m_hEvent;
    BOOL                m_bEOS;
    HRESULT             m_hrStatus;

};
```



<span data-ttu-id="b450b-144">在此範例中，我們對 [**OnEvent**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onevent) 和 [**OnFlush**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onflush) 方法不感興趣，因此它們只會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="b450b-144">In this example, we are not interested in the [**OnEvent**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onevent) and [**OnFlush**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onflush) methods, so they simply return **S\_OK**.</span></span> <span data-ttu-id="b450b-145">類別會使用事件控制碼來為應用程式發出信號;這個控制碼是透過函式提供。</span><span class="sxs-lookup"><span data-stu-id="b450b-145">The class uses an event handle to signal the application; this handle is provided through the constructor.</span></span>

<span data-ttu-id="b450b-146">在這個最基本的範例中， [**OnReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) 方法只會將時間戳記列印到主控台視窗。</span><span class="sxs-lookup"><span data-stu-id="b450b-146">In this minimal example, the [**OnReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) method just prints the time stamp to the console window.</span></span> <span data-ttu-id="b450b-147">然後，它會儲存狀態碼和資料流程結尾旗標，併發出事件控制碼的信號：</span><span class="sxs-lookup"><span data-stu-id="b450b-147">Then it stores the status code and the end-of-stream flag, and signals the event handle:</span></span>


```C++
HRESULT SourceReaderCB::OnReadSample(
    HRESULT hrStatus,
    DWORD /* dwStreamIndex */,
    DWORD dwStreamFlags,
    LONGLONG llTimestamp,
    IMFSample *pSample      // Can be NULL
    )
{
    EnterCriticalSection(&m_critsec);

    if (SUCCEEDED(hrStatus))
    {
        if (pSample)
        {
            // Do something with the sample.
            wprintf(L"Frame @ %I64d\n", llTimestamp);
        }
    }
    else
    {
        // Streaming error.
        NotifyError(hrStatus);
    }

    if (MF_SOURCE_READERF_ENDOFSTREAM & dwStreamFlags)
    {
        // Reached the end of the stream.
        m_bEOS = TRUE;
    }
    m_hrStatus = hrStatus;

    LeaveCriticalSection(&m_critsec);
    SetEvent(m_hEvent);
    return S_OK;
}
```



<span data-ttu-id="b450b-148">下列程式碼顯示應用程式會使用此回呼類別，從媒體檔案讀取所有的影片畫面：</span><span class="sxs-lookup"><span data-stu-id="b450b-148">The following code shows the application would use this callback class to read all of the video frames from a media file:</span></span>


```C++
HRESULT ReadMediaFile(PCWSTR pszURL)
{
    HRESULT hr = S_OK;

    IMFSourceReader *pReader = NULL;
    SourceReaderCB *pCallback = NULL;

    HANDLE hEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
    if (hEvent == NULL)
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
        goto done;
    }

    // Create an instance of the callback object.
    pCallback = new (std::nothrow) SourceReaderCB(hEvent);
    if (pCallback == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }

    // Create the Source Reader.
    hr = CreateSourceReaderAsync(pszURL, pCallback, &pReader);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = ConfigureDecoder(pReader, MF_SOURCE_READER_FIRST_VIDEO_STREAM);
    if (FAILED(hr))
    {
        goto done;
    }

    // Request the first sample.
    hr = pReader->ReadSample(MF_SOURCE_READER_FIRST_VIDEO_STREAM, 
        0, NULL, NULL, NULL, NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    while (SUCCEEDED(hr))
    {
        BOOL bEOS;
        hr = pCallback->Wait(INFINITE, &bEOS);
        if (FAILED(hr) || bEOS)
        {
            break;
        }
        hr = pReader->ReadSample(MF_SOURCE_READER_FIRST_VIDEO_STREAM,
            0, NULL, NULL, NULL, NULL);
    }

done:
    SafeRelease(&pReader);
    SafeRelease(&pCallback);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="b450b-149">相關主題</span><span class="sxs-lookup"><span data-stu-id="b450b-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b450b-150">來源讀取程式</span><span class="sxs-lookup"><span data-stu-id="b450b-150">Source Reader</span></span>](source-reader.md)
</dt> </dl>

 

 



