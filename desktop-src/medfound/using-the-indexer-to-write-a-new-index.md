---
description: 本主題說明如何將 Advanced 系統格式的索引寫入 (ASF) 檔。
ms.assetid: a14e3bef-0232-4259-930a-d860ed9230fd
title: 使用索引子來寫入新的索引
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9fbc604a9493f7feea61e34500e0f620a051b05b1431ec2d4917df9f8ed15b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034526"
---
# <a name="using-the-indexer-to-write-a-new-index"></a>使用索引子來寫入新的索引

本主題說明如何將 Advanced 系統格式的索引寫入 (ASF) 檔。

以下是建立 ASF 索引的一般程式：

1.  初始化 ASF 索引子物件的新實例，如 [索引子建立和](indexer-creation-and-configuration.md)設定中所述。
2.  （選擇性）設定索引子。
3.  將 ASF 資料封包傳送至索引子。
4.  認可索引。
5.  從索引子取得已完成的索引，並將其寫入至資料流程。

## <a name="configure-the-indexer"></a>設定索引子

若要使用索引子來寫入新的索引物件，索引子物件必須有旗標 MFASF \_ 索引子使用 \_ \_ \_ [**IMFASFIndexer：： SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setflags) 的呼叫來寫入新的索引集，然後再使用 [**IMFASFIndexer：： Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-initialize)進行初始化。

設定索引子來寫入索引時，呼叫端會選擇要編制索引的資料流程。 根據預設，索引子會嘗試建立所有資料流程的索引物件。 預設時間間隔為一秒。

[**IMFASFIndexer：： SetIndexStatus**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexstatus) 可以用來覆寫索引子物件的資料流程和索引類型的預設選擇。

下列範例程式碼示範如何初始化 ASF \_ 索引描述元 \_ 和 asf \_ 索引識別碼，然後 \_ 再呼叫 [**SetIndexStatus**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexstatus)。


```
ASF_INDEX_DESCRIPTOR IndexerType;
ZeroMemory(&IndexerType, sizeof(ASF_INDEX_DESCRIPTOR));

ASF_INDEX_IDENTIFIER IndexIdentifier;
ZeroMemory(&IndexIdentifier, sizeof(ASF_INDEX_IDENTIFIER));

IndexIdentifier.guidIndexType = GUID_NULL;
IndexIdentifier.wStreamNumber = 1;

IndexerType.Identifier = IndexIdentifier;
IndexerType.cPerEntryBytes  = MFASFINDEXER_PER_ENTRY_BYTES_DYNAMIC;
IndexerType.dwInterval  = MFASFINDEXER_NO_FIXED_INTERVAL;

hr = pIndexer->SetIndexStatus((BYTE*)&IndexerType, sizeof(ASF_INDEX_DESCRIPTOR), TRUE);
```



索引識別碼必須將其 GUID 索引類型設定為 GUID \_ Null，以表示索引類型會以時間為基礎的呈現。 索引識別碼也必須以要編制索引之 ASF 資料流程的資料流程號碼進行初始化。 設定索引識別碼之後，請使用它來初始化索引描述項。

索引描述元結構具有必須在呼叫 [**SetIndexStatus**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexstatus)之前設定的成員。 **識別碼** 是一種 [**ASF \_ 索引 \_ 識別碼**](/windows/desktop/api/wmcontainer/ns-wmcontainer-asf_index_identifier) 結構，用來識別串流號碼和索引類型。 **cPerEntryBytes** 是用於每個索引項目的位元組數目。 如果 \_ 每個 \_ 專案位元組動態 MFASFINDEXER 此值 \_ \_ ，索引項目就會有變數大小。 **dwInterval** 是索引編制間隔。 MFASFINDEXER \_ 沒有 \_ 固定間隔的值 \_ 表示沒有固定的索引間隔。

## <a name="send-asf-data-packets-to-the-indexer"></a>將 ASF 資料封包傳送至索引子

因為索引子是 WMContainer 層級物件，所以必須在封包產生期間與多工器一起使用。

從 [**GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket) 傳回的封包，可以透過對 [**GenerateIndexEntries**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-generateindexentries) 的呼叫傳送至索引子物件，在其中會針對每個傳送的封包建立索引項目。

下列程式碼示範如何完成這項操作：


```C++
HRESULT SendSampleToMux(
    IMFASFMultiplexer *pMux,
    IMFASFIndexer *pIndex,
    IMFSample *pSample,
    WORD wStream,
    IMFByteStream *pDestStream
    )
{
    IMFSample *pOutputSample = NULL;
    IMFMediaBuffer *pDataPacket = NULL;

    DWORD dwMuxStatus = ASF_STATUSFLAGS_INCOMPLETE;

    HRESULT hr = pMux->ProcessSample(wStream, pSample, 0);
    if (FAILED(hr))
    {
        goto done;
    }

    while (dwMuxStatus & ASF_STATUSFLAGS_INCOMPLETE)
    {
        hr = pMux->GetNextPacket(&dwMuxStatus, &pOutputSample);
        if (FAILED(hr))
        {
            goto done;
        }

        if (pOutputSample)
        {
            // Send the data packet to the indexer
            hr = pIndex->GenerateIndexEntries(pOutputSample);
            if (FAILED(hr))
            {
                goto done;
            }

            // Convert the sample to a contiguous buffer.
            hr = pOutputSample->ConvertToContiguousBuffer(&pDataPacket);
            if (FAILED(hr))
            {
                goto done;
            }

            // Write the buffer to the byte stream.
            hr = WriteBufferToByteStream(pDestStream, pDataPacket, NULL);
            if (FAILED(hr))
            {
                goto done;
            }
        }

        SafeRelease(&pOutputSample);
        SafeRelease(&pDataPacket);
    }

done:
    SafeRelease(&pOutputSample);
    SafeRelease(&pDataPacket);
    return hr;
}
```



如需詳細資訊，請參閱 [產生新的 ASF 資料封包](generating-new-asf-data-packets.md)。

## <a name="commit-the-index"></a>認可索引

最後一個封包已為其建立索引項目目之後，就必須認可索引。 這是透過呼叫 [**IMFASFIndexer：： CommitIndex**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-commitindex)來完成。 **CommitIndex** 會取得 ContentInfo 物件的指標，該物件會描述 ASF 檔案的內容。 認可索引會完成索引編制，並以新的檔案大小和 seekability 資訊更新標頭。

## <a name="get-the-completed-index"></a>取得完成的索引

若要從索引子取得完成的索引，請執行下列步驟：

1.  呼叫 [**IMFASFIndexer：： GetIndexWriteSpace**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getindexwritespace) 來取得索引的大小。
2.  呼叫 [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) 來建立媒體緩衝區。 您可以配置夠大的緩衝區來容納整個索引，配置較小的緩衝區，並以區塊取得索引。
3.  呼叫 [**IMFASFIndexer：： GetCompletedIndex**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getcompletedindex) 來取得索引資料。 在第一次呼叫時，請將 *cbOffsetWithinIndex* 參數設定為零。 如果您取得以區塊為單位的索引，則每次以上一個呼叫中的資料大小遞增 *cbOffsetWithinIndex* 。
4.  呼叫 [**IMFMediaBuffer：： Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) 以取得索引資料的指標和資料的大小。
5.  將索引資料寫入至 ASF 檔案。
6.  呼叫 [**IMFMediaBuffer：： unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) 以解除鎖定媒體緩衝區。
7.  重複步驟3到6，直到您已撰寫整個索引為止。

下列程式碼顯示這些步驟：


```C++
HRESULT WriteASFIndex(IMFASFIndexer *pIndex,IMFByteStream *pStream)
{
    const DWORD cbChunkSize = 4096;

    IMFMediaBuffer *pBuffer = NULL;

    QWORD cbIndex = 0;
    DWORD cbIndexWritten = 0;

    HRESULT hr = pIndex->GetIndexWriteSpace(&cbIndex);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = MFCreateMemoryBuffer(cbChunkSize, &pBuffer);
    if (FAILED(hr))
    {
        goto done;
    }

    while (cbIndexWritten < cbIndex)
    {
        BYTE *pData = NULL;
        DWORD cbData = 0;
        DWORD cbWritten = 0;

        hr = pIndex->GetCompletedIndex(pBuffer, cbIndexWritten);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pBuffer->Lock(&pData, NULL, &cbData);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pStream->Write(pData, cbData, &cbWritten);

        (void)pBuffer->Unlock();

        if (FAILED(hr))
        {
            goto done;
        }

        cbIndexWritten += cbData;
    }

done:
    SafeRelease(&pBuffer);
    return hr;
};
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[ASF 索引子](asf-index-object.md)
</dt> </dl>

 

 



