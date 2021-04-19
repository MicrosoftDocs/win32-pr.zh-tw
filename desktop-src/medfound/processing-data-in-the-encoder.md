---
description: 處理編碼器中的資料
ms.assetid: 7be4c5e7-db2c-4063-8e5c-af6ffb861aa5
title: 處理編碼器中的資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99b7fedef50df61851408d084b511497eacd0288
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106969243"
---
# <a name="processing-data-in-the-encoder"></a>處理編碼器中的資料

在您協商編碼器 MFT 的輸入類型和輸出類型（如 [編碼器上的媒體類型協商](media-type-negotiation-on-the-encoder.md)中所述）之後，您就可以開始處理媒體資料範例。 資料會以媒體範例形式傳遞 ([**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) 介面) ，也會從輸出中以媒體範例形式接收。

將資料傳送至編碼器進行處理之前，您必須配置媒體範例，並新增一個包含需要編碼之媒體資料的媒體緩衝區。 呼叫 [**IMFTransform：:P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) ，並將指標傳遞至配置的媒體範例。 除了媒體範例， **ProcessInput** 還需要輸入資料流程識別碼。 若要取得資料流程識別碼，請呼叫 [**IMFTransform：： GetStreamIDs**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamids)。 因為編碼器設計成隻有一個輸出和一個輸出，所以這些資料流程識別碼的值一律為0。

若要從編碼器取得資料，請呼叫 [**IMFTransform：:P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)。 呼叫 [**ProcessOutput**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessoutput)之前，您必須先找出編碼器是否配置輸出媒體範例，或者您必須明確地執行此動作。 若要這樣做，請呼叫 [**IMFTransform：： GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo)。 這會在 [**MFT \_ 輸出 \_ 資料流程 \_ 資訊**](/windows/desktop/api/mftransform/ns-mftransform-mft_output_stream_info) 結構中傳回輸出媒體範例資訊。 如果編碼器配置媒體範例，則會傳回 \_ \_ dwFlags 成員中的 MFT 輸出資料流程 \_ 提供 \_ 範例旗標，且 **cbSize** 成員會包含零。  如果編碼器預期您要配置輸出緩衝區，請根據 **cbSize** 中傳回的大小建立輸出媒體範例和相關聯的媒體緩衝區。 當您呼叫 [**ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample)時，請將指標傳遞至新建立的媒體範例。 在編碼會話期間，編碼器會使用編碼的資料，填滿輸出媒體範例所指向的媒體緩衝區。

若要啟動編碼會話，請呼叫 [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput)將輸入媒體範例傳遞給編碼器。 編碼器會開始處理和資料，並產生一或多個輸出媒體範例，只要 [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) 傳回 MF \_ E \_ 轉換 \_ 需要 \_ 更多 \_ 輸入，就必須加以取出。 如果您呼叫 **ProcessInput** 傳遞更多輸入（只要有輸出資料要抓取）， **ProcessInput** 就會因為 MF \_ E NOTACCEPTING 而失敗 \_ 。 除非用戶端至少呼叫 **ProcessOutput** 一次，否則編碼器不接受任何其他輸入。

您應該為所有傳遞的輸入樣本設定正確的時間戳記和持續時間。 時間戳記並非絕對必要，但有助於維護音訊/影片同步處理。 如果您沒有範例的時間戳記，最好不要將其保留，而不是使用不確定的值。

## <a name="encoder-processing-example"></a>編碼器處理範例

下列範例程式碼示範如何呼叫 [**IMFTransform：:P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) 來取得編碼的範例。 如需此範例的完整內容，請參閱 [編碼器範例程式碼](encoder-example-code.md)。


```C++
HRESULT CWmaEncoder::ProcessOutput(IMFSample **ppSample)
{
    if (m_pMFT == NULL)
    {
        return MF_E_NOT_INITIALIZED;
    }

    *ppSample = NULL;

    IMFMediaBuffer* pBufferOut = NULL;
    IMFSample* pSampleOut = NULL;

    DWORD dwStatus;
  
    MFT_OUTPUT_STREAM_INFO mftStreamInfo = { 0 };
    MFT_OUTPUT_DATA_BUFFER mftOutputData = { 0 };

    HRESULT hr = m_pMFT->GetOutputStreamInfo(m_dwOutputID, &mftStreamInfo);
    if (FAILED(hr))
    {
        goto done;
    }

    //create a buffer for the output sample
    hr = MFCreateMemoryBuffer(mftStreamInfo.cbSize, &pBufferOut);
    if (FAILED(hr))
    {
        goto done;
    }

    //Create the output sample
    hr = MFCreateSample(&pSampleOut);
    if (FAILED(hr))
    {
        goto done;
    }

    //Add the output buffer 
    hr = pSampleOut->AddBuffer(pBufferOut);
    if (FAILED(hr))
    {
        goto done;
    }
 
    //Set the output sample
    mftOutputData.pSample = pSampleOut;

    //Set the output id
    mftOutputData.dwStreamID = m_dwOutputID;

    //Generate the output sample
    hr = m_pMFT->ProcessOutput(0, 1, &mftOutputData, &dwStatus);
    if (hr == MF_E_TRANSFORM_NEED_MORE_INPUT)
    {
        hr = S_OK;
        goto done;
    }

    // TODO: Handle MF_E_TRANSFORM_STREAM_CHANGE

    if (FAILED(hr))
    {
        goto done;
    }

    *ppSample = pSampleOut;
    (*ppSample)->AddRef();

done:
    SafeRelease(&pBufferOut);
    SafeRelease(&pSampleOut);
    return hr;
};
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[ASF 多工器](asf-multiplexer.md)
</dt> <dt>

[具現化編碼器 MFT](instantiating-the-encoder-mft.md)
</dt> <dt>

[Windows Media 編碼器](windows-media-encoders.md)
</dt> </dl>

 

 



