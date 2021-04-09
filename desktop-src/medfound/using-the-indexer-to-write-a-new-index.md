---
description: 本主題說明如何將 Advanced 系統格式的索引寫入 (ASF) 檔。
ms.assetid: a14e3bef-0232-4259-930a-d860ed9230fd
title: 使用索引子來寫入新的索引
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d37922b693c83a8417dea4006fc38397b805fb71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691595"
---
# <a name="using-the-indexer-to-write-a-new-index"></a><span data-ttu-id="2bc37-103">使用索引子來寫入新的索引</span><span class="sxs-lookup"><span data-stu-id="2bc37-103">Using the Indexer to Write a New Index</span></span>

<span data-ttu-id="2bc37-104">本主題說明如何將 Advanced 系統格式的索引寫入 (ASF) 檔。</span><span class="sxs-lookup"><span data-stu-id="2bc37-104">This topic shows how to write an index for an Advanced Systems Format (ASF) file.</span></span>

<span data-ttu-id="2bc37-105">以下是建立 ASF 索引的一般程式：</span><span class="sxs-lookup"><span data-stu-id="2bc37-105">Here is the general procedure for creating an ASF index:</span></span>

1.  <span data-ttu-id="2bc37-106">初始化 ASF 索引子物件的新實例，如 [索引子建立和](indexer-creation-and-configuration.md)設定中所述。</span><span class="sxs-lookup"><span data-stu-id="2bc37-106">Initialize a new instance of the ASF indexer object, as described in [Indexer Creation and Configuration](indexer-creation-and-configuration.md).</span></span>
2.  <span data-ttu-id="2bc37-107">（選擇性）設定索引子。</span><span class="sxs-lookup"><span data-stu-id="2bc37-107">Optionally, configure the indexer.</span></span>
3.  <span data-ttu-id="2bc37-108">將 ASF 資料封包傳送至索引子。</span><span class="sxs-lookup"><span data-stu-id="2bc37-108">Send ASF data packets to the indexer.</span></span>
4.  <span data-ttu-id="2bc37-109">認可索引。</span><span class="sxs-lookup"><span data-stu-id="2bc37-109">Commit the index.</span></span>
5.  <span data-ttu-id="2bc37-110">從索引子取得已完成的索引，並將其寫入至資料流程。</span><span class="sxs-lookup"><span data-stu-id="2bc37-110">Get the completed index from the indexer, and write it to a stream.</span></span>

## <a name="configure-the-indexer"></a><span data-ttu-id="2bc37-111">設定索引子</span><span class="sxs-lookup"><span data-stu-id="2bc37-111">Configure the Indexer</span></span>

<span data-ttu-id="2bc37-112">若要使用索引子來寫入新的索引物件，索引子物件必須有旗標 MFASF \_ 索引子使用 \_ \_ \_ [**IMFASFIndexer：： SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setflags) 的呼叫來寫入新的索引集，然後再使用 [**IMFASFIndexer：： Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-initialize)進行初始化。</span><span class="sxs-lookup"><span data-stu-id="2bc37-112">To use the indexer to write a new index object, the indexer object must have the flag MFASF\_INDEXER\_WRITE\_NEW\_INDEX set with a call to [**IMFASFIndexer::SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setflags) before it is initialized with [**IMFASFIndexer::Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-initialize).</span></span>

<span data-ttu-id="2bc37-113">設定索引子來寫入索引時，呼叫端會選擇要編制索引的資料流程。</span><span class="sxs-lookup"><span data-stu-id="2bc37-113">When the indexer is configured for writing an index, the caller chooses the streams to be indexed.</span></span> <span data-ttu-id="2bc37-114">根據預設，索引子會嘗試建立所有資料流程的索引物件。</span><span class="sxs-lookup"><span data-stu-id="2bc37-114">By default, the indexer attempts to create an Index Object for all streams.</span></span> <span data-ttu-id="2bc37-115">預設時間間隔為一秒。</span><span class="sxs-lookup"><span data-stu-id="2bc37-115">The default time interval is one second.</span></span>

<span data-ttu-id="2bc37-116">[**IMFASFIndexer：： SetIndexStatus**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexstatus) 可以用來覆寫索引子物件的資料流程和索引類型的預設選擇。</span><span class="sxs-lookup"><span data-stu-id="2bc37-116">[**IMFASFIndexer::SetIndexStatus**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexstatus) can be used to override the indexer object's default choice of streams and index types.</span></span>

<span data-ttu-id="2bc37-117">下列範例程式碼示範如何初始化 ASF \_ 索引描述元 \_ 和 asf \_ 索引識別碼，然後 \_ 再呼叫 [**SetIndexStatus**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexstatus)。</span><span class="sxs-lookup"><span data-stu-id="2bc37-117">The following example code shows the initialization of an ASF\_INDEX\_DESCRIPTOR and an ASF\_INDEX\_IDENTIFIER before a call to [**SetIndexStatus**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexstatus).</span></span>


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



<span data-ttu-id="2bc37-118">索引識別碼必須將其 GUID 索引類型設定為 GUID \_ Null，以表示索引類型會以時間為基礎的呈現。</span><span class="sxs-lookup"><span data-stu-id="2bc37-118">The index identifier must have its GUID index type set to GUID\_NULL to indicate that the index type will be presentation time-based.</span></span> <span data-ttu-id="2bc37-119">索引識別碼也必須以要編制索引之 ASF 資料流程的資料流程號碼進行初始化。</span><span class="sxs-lookup"><span data-stu-id="2bc37-119">The index identifier must also be initialized with the stream number of the ASF stream to be indexed.</span></span> <span data-ttu-id="2bc37-120">設定索引識別碼之後，請使用它來初始化索引描述項。</span><span class="sxs-lookup"><span data-stu-id="2bc37-120">After the index identifier is set, use it to initialize the index descriptor.</span></span>

<span data-ttu-id="2bc37-121">索引描述元結構具有必須在呼叫 [**SetIndexStatus**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexstatus)之前設定的成員。</span><span class="sxs-lookup"><span data-stu-id="2bc37-121">The index descriptor structure has members which must be set before the call to [**SetIndexStatus**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexstatus).</span></span> <span data-ttu-id="2bc37-122">**識別碼** 是一種 [**ASF \_ 索引 \_ 識別碼**](/windows/desktop/api/wmcontainer/ns-wmcontainer-asf_index_identifier) 結構，用來識別串流號碼和索引類型。</span><span class="sxs-lookup"><span data-stu-id="2bc37-122">**Identifier** is an [**ASF\_INDEX\_IDENTIFIER**](/windows/desktop/api/wmcontainer/ns-wmcontainer-asf_index_identifier) structure that identifies the stream number and the type of index.</span></span> <span data-ttu-id="2bc37-123">**cPerEntryBytes** 是用於每個索引項目的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="2bc37-123">**cPerEntryBytes** is the number of bytes used for each index entry.</span></span> <span data-ttu-id="2bc37-124">如果 \_ 每個 \_ 專案位元組動態 MFASFINDEXER 此值 \_ \_ ，索引項目就會有變數大小。</span><span class="sxs-lookup"><span data-stu-id="2bc37-124">If the value is MFASFINDEXER\_PER\_ENTRY\_BYTES\_DYNAMIC, the index entries have variable size.</span></span> <span data-ttu-id="2bc37-125">**dwInterval** 是索引編制間隔。</span><span class="sxs-lookup"><span data-stu-id="2bc37-125">**dwInterval** is the indexing interval.</span></span> <span data-ttu-id="2bc37-126">MFASFINDEXER \_ 沒有 \_ 固定間隔的值 \_ 表示沒有固定的索引間隔。</span><span class="sxs-lookup"><span data-stu-id="2bc37-126">A value of MFASFINDEXER\_NO\_FIXED\_INTERVAL indicates that there is no fixed indexing interval.</span></span>

## <a name="send-asf-data-packets-to-the-indexer"></a><span data-ttu-id="2bc37-127">將 ASF 資料封包傳送至索引子</span><span class="sxs-lookup"><span data-stu-id="2bc37-127">Send ASF Data Packets to the Indexer</span></span>

<span data-ttu-id="2bc37-128">因為索引子是 WMContainer 層級物件，所以必須在封包產生期間與多工器一起使用。</span><span class="sxs-lookup"><span data-stu-id="2bc37-128">Because the indexer is a WMContainer level object, it must be used in conjunction with the multiplexer during packet generation.</span></span>

<span data-ttu-id="2bc37-129">從 [**GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket) 傳回的封包，可以透過對 [**GenerateIndexEntries**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-generateindexentries) 的呼叫傳送至索引子物件，在其中會針對每個傳送的封包建立索引項目。</span><span class="sxs-lookup"><span data-stu-id="2bc37-129">Packets returned from [**GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket) can be sent to the indexer object through calls to [**GenerateIndexEntries**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-generateindexentries) where it creates index entries for each packet sent.</span></span>

<span data-ttu-id="2bc37-130">下列程式碼示範如何完成這項操作：</span><span class="sxs-lookup"><span data-stu-id="2bc37-130">The following code demonstrates how this may be done:</span></span>


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



<span data-ttu-id="2bc37-131">如需詳細資訊，請參閱 [產生新的 ASF 資料封包](generating-new-asf-data-packets.md)。</span><span class="sxs-lookup"><span data-stu-id="2bc37-131">For more information, see [Generating New ASF Data Packets](generating-new-asf-data-packets.md).</span></span>

## <a name="commit-the-index"></a><span data-ttu-id="2bc37-132">認可索引</span><span class="sxs-lookup"><span data-stu-id="2bc37-132">Commit the Index</span></span>

<span data-ttu-id="2bc37-133">最後一個封包已為其建立索引項目目之後，就必須認可索引。</span><span class="sxs-lookup"><span data-stu-id="2bc37-133">After the last packet has had an index entry created for it, the index must be committed.</span></span> <span data-ttu-id="2bc37-134">這是透過呼叫 [**IMFASFIndexer：： CommitIndex**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-commitindex)來完成。</span><span class="sxs-lookup"><span data-stu-id="2bc37-134">This is done with a call to [**IMFASFIndexer::CommitIndex**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-commitindex).</span></span> <span data-ttu-id="2bc37-135">**CommitIndex** 會取得 ContentInfo 物件的指標，該物件會描述 ASF 檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="2bc37-135">**CommitIndex** takes a pointer to the ContentInfo object which describes the content of the ASF file.</span></span> <span data-ttu-id="2bc37-136">認可索引會完成索引編制，並以新的檔案大小和 seekability 資訊更新標頭。</span><span class="sxs-lookup"><span data-stu-id="2bc37-136">Committing the index finishes the indexing and updates the header with new information about file size and seekability.</span></span>

## <a name="get-the-completed-index"></a><span data-ttu-id="2bc37-137">取得完成的索引</span><span class="sxs-lookup"><span data-stu-id="2bc37-137">Get the Completed Index</span></span>

<span data-ttu-id="2bc37-138">若要從索引子取得完成的索引，請執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="2bc37-138">To get the completed index from the indexer, perform the following steps:</span></span>

1.  <span data-ttu-id="2bc37-139">呼叫 [**IMFASFIndexer：： GetIndexWriteSpace**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getindexwritespace) 來取得索引的大小。</span><span class="sxs-lookup"><span data-stu-id="2bc37-139">Call [**IMFASFIndexer::GetIndexWriteSpace**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getindexwritespace) to get the size of the index.</span></span>
2.  <span data-ttu-id="2bc37-140">呼叫 [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) 來建立媒體緩衝區。</span><span class="sxs-lookup"><span data-stu-id="2bc37-140">Call [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) to create a media buffer.</span></span> <span data-ttu-id="2bc37-141">您可以配置夠大的緩衝區來容納整個索引，配置較小的緩衝區，並以區塊取得索引。</span><span class="sxs-lookup"><span data-stu-id="2bc37-141">You can either allocate an buffer that is large enough to hold the entire index, of allocate a smaller buffer and get the index in chunks.</span></span>
3.  <span data-ttu-id="2bc37-142">呼叫 [**IMFASFIndexer：： GetCompletedIndex**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getcompletedindex) 來取得索引資料。</span><span class="sxs-lookup"><span data-stu-id="2bc37-142">Call [**IMFASFIndexer::GetCompletedIndex**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getcompletedindex) to get the index data.</span></span> <span data-ttu-id="2bc37-143">在第一次呼叫時，請將 *cbOffsetWithinIndex* 參數設定為零。</span><span class="sxs-lookup"><span data-stu-id="2bc37-143">On the first call, set the *cbOffsetWithinIndex* parameter to zero.</span></span> <span data-ttu-id="2bc37-144">如果您取得以區塊為單位的索引，則每次以上一個呼叫中的資料大小遞增 *cbOffsetWithinIndex* 。</span><span class="sxs-lookup"><span data-stu-id="2bc37-144">If you get the index in chunks, increment *cbOffsetWithinIndex* each time by the size of the data from the previous call.</span></span>
4.  <span data-ttu-id="2bc37-145">呼叫 [**IMFMediaBuffer：： Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) 以取得索引資料的指標和資料的大小。</span><span class="sxs-lookup"><span data-stu-id="2bc37-145">Call [**IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) to get a pointer to the index data and the size of the data.</span></span>
5.  <span data-ttu-id="2bc37-146">將索引資料寫入至 ASF 檔案。</span><span class="sxs-lookup"><span data-stu-id="2bc37-146">Write the index data to the ASF file.</span></span>
6.  <span data-ttu-id="2bc37-147">呼叫 [**IMFMediaBuffer：： unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) 以解除鎖定媒體緩衝區。</span><span class="sxs-lookup"><span data-stu-id="2bc37-147">Call [**IMFMediaBuffer::Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) to unlock the media buffer.</span></span>
7.  <span data-ttu-id="2bc37-148">重複步驟3到6，直到您已撰寫整個索引為止。</span><span class="sxs-lookup"><span data-stu-id="2bc37-148">Repeat steps 3–6 until you have written the entire index.</span></span>

<span data-ttu-id="2bc37-149">下列程式碼顯示這些步驟：</span><span class="sxs-lookup"><span data-stu-id="2bc37-149">The following code shows these steps:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="2bc37-150">相關主題</span><span class="sxs-lookup"><span data-stu-id="2bc37-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2bc37-151">ASF 索引子</span><span class="sxs-lookup"><span data-stu-id="2bc37-151">ASF Indexer</span></span>](asf-index-object.md)
</dt> </dl>

 

 



