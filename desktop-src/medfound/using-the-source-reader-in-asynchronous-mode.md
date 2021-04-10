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
# <a name="using-the-source-reader-in-asynchronous-mode"></a>使用非同步模式的來源讀取器

本主題說明如何使用非同步模式的 [來源讀取器](source-reader.md) 。 在非同步模式中，應用程式會提供回呼介面，用來通知應用程式有可用的資料。

本主題假設您已閱讀 [使用來源讀取程式來處理媒體資料](processing-media-data-with-the-source-reader.md)的主題。

## <a name="using-asynchronous-mode"></a>使用非同步模式

來源讀取器在同步模式或非同步模式下運作。 上一節中所示的程式碼範例假設來源讀取器使用同步模式，這是預設值。 在同步模式中， [**IMFSourceReader：： ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) 方法會在媒體來源產生下一個範例時封鎖。 媒體來源通常會從某些外部來源 (（例如本機檔案或網路連線) ）取得資料，因此方法可以封鎖呼叫執行緒一段明顯的時間。

在非同步模式中， [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) 會立即傳回，而工作會在另一個執行緒上執行。 作業完成之後，來源讀取器會透過 [**IMFSourceReaderCallback**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereadercallback) 回呼介面呼叫應用程式。 若要使用非同步模式，您必須在第一次建立來源讀取器時提供回呼指標，如下所示：

1.  藉由呼叫 [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) 函數來建立屬性存放區。
2.  在屬性存放區上設定 [MF \_ 來源 \_ 讀取器 \_ 非同步 \_ 回呼](mf-source-reader-async-callback.md) 屬性。 屬性值是您回呼物件的指標。
3.  當您建立來源讀取器時，請將屬性存放區傳遞給 *pAttributes* 參數中的建立函數。 所有用來建立來源讀取器的函式都有此參數。

下列範例會示範這些步驟。


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



建立來源讀取器之後，您就無法在同步和非同步之間切換模式。

若要以非同步模式取得資料，請呼叫 [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) 方法，但將最後四個參數設定為 **Null**，如下列範例所示。


```C++
    // Request the first sample.
    hr = pReader->ReadSample(MF_SOURCE_READER_FIRST_VIDEO_STREAM, 
        0, NULL, NULL, NULL, NULL);
```



當 [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) 方法以非同步方式完成時，來源讀取器會呼叫您的 [**IMFSourceReaderCallback：： OnReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) 方法。 這個方法有五個參數：

-   *hrStatus*：包含 **HRESULT** 值。 這是 [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) 會在同步模式中傳回的相同值。 如果 *hrStatus* 包含錯誤碼，您可以忽略其餘的參數。
-   *dwStreamIndex*、 *dwStreamFlags*、llTimestamp 和 *pSample*：這三個參數相當於 [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample)中的最後三個參數。 它們分別包含串流號碼、狀態旗標和 [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) 指標。


```C++
    STDMETHODIMP OnReadSample(HRESULT hrStatus, DWORD dwStreamIndex,
        DWORD dwStreamFlags, LONGLONG llTimestamp, IMFSample *pSample);
```



此外，回呼介面會定義其他兩種方法：

-   [**OnEvent**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onevent)。 當媒體來源中發生特定事件（例如緩衝或網路連接事件）時，通知應用程式。
-   [**OnFlush**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onflush)。 當 [**Flush**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-flush) 方法完成時呼叫。

## <a name="implementing-the-callback-interface"></a>執行回呼介面

回呼介面必須是安全線程，因為從背景工作執行緒呼叫 [**OnReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) 和其他回呼方法。

當您執行回呼時，有幾種不同的方法可以採用。 例如，您可以在回呼內執行所有工作，也可以使用回呼來通知應用程式 (例如，藉由向事件控制碼發出信號，) 然後從應用程式執行緒執行工作。

針對您對 [**IMFSourceReader：： ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample)方法所進行的每個呼叫，將會呼叫 [**OnReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample)方法一次。 若要取得下一個範例，請再次呼叫 **ReadSample** 。 如果發生錯誤，則會以 *hrStatus* 參數的錯誤碼來呼叫 **OnReadSample** 。

下列範例顯示回呼介面的最基本實作為。 首先，以下是執行介面之類別的宣告。


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



在此範例中，我們對 [**OnEvent**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onevent) 和 [**OnFlush**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onflush) 方法不感興趣，因此它們只會傳回 **S \_ OK**。 類別會使用事件控制碼來為應用程式發出信號;這個控制碼是透過函式提供。

在這個最基本的範例中， [**OnReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) 方法只會將時間戳記列印到主控台視窗。 然後，它會儲存狀態碼和資料流程結尾旗標，併發出事件控制碼的信號：


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



下列程式碼顯示應用程式會使用此回呼類別，從媒體檔案讀取所有的影片畫面：


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[來源讀取程式](source-reader.md)
</dt> </dl>

 

 



