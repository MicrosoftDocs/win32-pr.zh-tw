---
description: ASF 索引子是 WMContainer 層元件，可用來以 Advanced 系統格式讀取或寫入索引物件 (ASF) 檔。 本主題提供有關使用 ASF 索引子在 ASF 檔案內搜尋的資訊。
ms.assetid: 9c501d33-847e-448e-a19c-39dfbc7757ca
title: 使用索引子在 ASF 檔案內搜尋
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c40c35f876fdc5452c596048d121fb0c2933094a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983561"
---
# <a name="using-the-indexer-to-seek-within-an-asf-file"></a>使用索引子在 ASF 檔案內搜尋

ASF *索引子* 是 WMContainer 層元件，可用來以 Advanced 系統格式讀取或寫入索引物件 (ASF) 檔。 本主題提供有關使用 ASF 索引子在 ASF 檔案內搜尋的資訊。

-   [初始化用來搜尋的索引子](#initializing-the-indexer-for-seeking)
-   [取得搜尋位置。](#getting-the-seek-position)
-   [相關主題](#related-topics)

如需 ASF 檔案結構的詳細資訊，請參閱 [asf 檔案結構](asf-file-structure.md)。

## <a name="initializing-the-indexer-for-seeking"></a>初始化用來搜尋的索引子

若要初始化 ASF 索引子以進行搜尋：

1.  呼叫 [**MFCreateASFIndexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfindexer) 來建立 ASF 索引子的新實例。
2.  呼叫 [**IMFASFIndexer：： initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-initialize) 以初始化索引子。 這個方法會從 ASF 標頭取得資訊，以判斷哪些 ASF 資料流程已編制索引。 依預設，會針對搜尋設定索引子物件。
3.  呼叫 [**IMFASFIndexer：： GetIndexPosition**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getindexposition) ，以在 ASF 檔案中尋找索引的位移。
4.  呼叫 [**MFCreateASFIndexerByteStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfindexerbytestream) 函數，以建立位元組資料流程來讀取索引。 此函式的輸入是包含 ASF 檔案之位元組資料流程的指標，而索引 (自上一個步驟) 的位移。
5.  呼叫 [**IMFASFIndexer：： SetIndexByteStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexbytestreams) ，在索引子上設定索引位元組資料流程。

下列程式碼顯示這些步驟：


```C++
HRESULT CreateASFIndexer(
    IMFByteStream *pContentByteStream,  // Pointer to the content byte stream
    IMFASFContentInfo *pContentInfo,
    IMFASFIndexer **ppIndexer
    )
{
    IMFASFIndexer *pIndexer = NULL;
    IMFByteStream *pIndexerByteStream = NULL;

    QWORD qwLength = 0, qwIndexOffset = 0, qwBytestreamLength = 0;

    // Create the indexer.
    HRESULT hr = MFCreateASFIndexer(&pIndexer);
    if (FAILED(hr))
    {
        goto done;
    }

    //Initialize the indexer to work with this ASF library
    hr =  pIndexer->Initialize(pContentInfo);
    if (FAILED(hr))
    {
        goto done;
    }

    //Check if the index exists. You can only do this after creating the indexer

    //Get byte stream length
    hr = pContentByteStream->GetLength(&qwLength);
    if (FAILED(hr))
    {
        goto done;
    }

    //Get index offset
    hr = pIndexer->GetIndexPosition(pContentInfo, &qwIndexOffset);
    if (FAILED(hr))
    {
        goto done;
    }

    if ( qwIndexOffset >= qwLength)
    {
        //index object does not exist, release the indexer
        goto done;
    }
    else
    {
        // initialize the indexer
        // Create a byte stream that the Indexer will use to read in
        // and parse the indexers.
         hr = MFCreateASFIndexerByteStream(
             pContentByteStream,
             qwIndexOffset,
             &pIndexerByteStream
             );

        if (FAILED(hr))
        {
            goto done;
        }
   }

    hr = pIndexer->SetIndexByteStreams(&pIndexerByteStream, 1);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the pointer to the caller.
    *ppIndexer = pIndexer;
    (*ppIndexer)->AddRef();

done:
    SafeRelease(&pIndexer);
    SafeRelease(&pIndexerByteStream);
    return hr;
}
```



## <a name="getting-the-seek-position"></a>取得搜尋位置。

1.  若要找出特定的資料流程是否已編制索引，請呼叫 [**IMFASFIndexer：： GetIndexStatus**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getindexstatus)。 如果串流已編制索引， *pfIsIndexed* 參數會收到值 **TRUE**;否則，它會收到值 **FALSE**。
2.  根據預設，索引子會使用向前搜尋。 若要進行反向搜尋 (也就是從檔案結尾搜尋) ，請呼叫 [**IMFASFIndexer：： SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setflags) ，並設定 **MFASF \_ 索引子 \_ READ \_ FOR \_ REVERSEPLAYBACK** 旗標。 否則，請略過此步驟。
3.  如果已編制資料流程的索引，請呼叫 [**IMFASFIndexer：： GetSeekPositionForValue**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getseekpositionforvalue)，以取得指定之呈現時間的搜尋位置。 這個方法會讀取 ASF 索引，並尋找最接近所要求時間的索引項目目。 方法會傳回索引項目所指定之資料封包的位元組位移。 位元組位移會相對於 ASF 資料物件的開頭。

[**GetSeekPositionForValue**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getseekpositionforvalue)方法會採用 [**ASF \_ 索引 \_ 識別碼**](/windows/desktop/api/wmcontainer/ns-wmcontainer-asf_index_identifier)結構的指標。 此結構會指定索引類型和資料流程識別碼。 目前，索引類型必須是 GUID \_ Null，以指定以時間為基礎的索引。

下列程式碼會根據給定的資料流程識別碼和目標呈現時間，取得搜尋位置。 如果呼叫成功，則會傳回 *pcbDataOffset* 參數中的資料位移，以及 *phnsApproxSeekTime* 中近似的實際搜尋時間。


```C++
HRESULT GetSeekPositionWithIndexer(
    IMFASFIndexer *pIndexer,
    WORD          wStreamNumber,
    MFTIME        hnsSeekTime,          // Desired seek time, in 100-nsec.
    BOOL          bReverse,
    QWORD         *pcbDataOffset,       // Receives the offset in bytes.
    MFTIME        *phnsApproxSeekTime   // Receives the approximate seek time.
    )
{
    // Query whether the stream is indexed.

    ASF_INDEX_IDENTIFIER IndexIdentifier = { GUID_NULL, wStreamNumber };

    BOOL fIsIndexed = FALSE;

    ASF_INDEX_DESCRIPTOR descriptor;

    DWORD cbIndexDescriptor = sizeof(descriptor);

    HRESULT hr = pIndexer->GetIndexStatus(
        &IndexIdentifier,
        &fIsIndexed,
        (BYTE*)&descriptor,
        &cbIndexDescriptor
        );

    if (hr == MF_E_BUFFERTOOSMALL)
    {
        hr = S_OK;
    }
    else if (FAILED(hr))
    {
        goto done;
    }

    if (!fIsIndexed)
    {
        hr = MF_E_ASF_NOINDEX;
        goto done;
    }

    if (bReverse)
    {
        hr = pIndexer->SetFlags(MFASF_INDEXER_READ_FOR_REVERSEPLAYBACK);
        if (FAILED(hr))
        {
            goto done;
        }
    }

    // Get the offset from the indexer.

    PROPVARIANT var;

    var.vt = VT_I8;
    var.hVal.QuadPart = hnsSeekTime;

    hr = pIndexer->GetSeekPositionForValue(
        &var,
        &IndexIdentifier,
        pcbDataOffset,
        phnsApproxSeekTime,
        0
        );

done:
    return hr;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[ASF 索引子](asf-index-object.md)
</dt> </dl>

 

 



