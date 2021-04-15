---
description: 產生新的 ASF 標頭物件
ms.assetid: cf73306d-156a-45c0-a3d6-ae48734f5709
title: 產生新的 ASF 標頭物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f303be4eb3353a0e7ddf1dad0eff9956f68d7db5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510789"
---
# <a name="generating-a-new-asf-header-object"></a><span data-ttu-id="5b3fb-103">產生新的 ASF 標頭物件</span><span class="sxs-lookup"><span data-stu-id="5b3fb-103">Generating a New ASF Header Object</span></span>

<span data-ttu-id="5b3fb-104">若要將 ContentInfo 物件中包含的資訊轉換成二進位 ASF 標頭物件格式，應用程式必須呼叫 [**IMFASFContentInfo：： GenerateHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader)。</span><span class="sxs-lookup"><span data-stu-id="5b3fb-104">To convert the information contained in the ContentInfo object to a binary ASF Header Object format, the application must call [**IMFASFContentInfo::GenerateHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader).</span></span> <span data-ttu-id="5b3fb-105">此呼叫必須在產生資料封包，且 ContentInfo 物件包含更新資訊之後進行。</span><span class="sxs-lookup"><span data-stu-id="5b3fb-105">This call must be made after the data packets are generated and the ContentInfo object contains updated information.</span></span> <span data-ttu-id="5b3fb-106">**GenerateHeader** 會傳回媒體緩衝區的指標，其中包含有效格式的標頭資訊。</span><span class="sxs-lookup"><span data-stu-id="5b3fb-106">**GenerateHeader** returns a pointer to a media buffer that contains the header information in the valid format.</span></span> <span data-ttu-id="5b3fb-107">然後，應用程式可以在新的 ASF 檔案開頭，寫入媒體緩衝區所指向的資料。</span><span class="sxs-lookup"><span data-stu-id="5b3fb-107">The application can then write the data, pointed to by the media buffer, at the beginning of a new ASF file.</span></span>

## <a name="to-write-a-new-header-object-by-using-the-contentinfo-object"></a><span data-ttu-id="5b3fb-108">使用 ContentInfo 物件撰寫新的標頭物件</span><span class="sxs-lookup"><span data-stu-id="5b3fb-108">To write a new Header Object by using the ContentInfo object</span></span>

1.  <span data-ttu-id="5b3fb-109">呼叫 [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) 以建立空的 ContentInfo 物件。</span><span class="sxs-lookup"><span data-stu-id="5b3fb-109">Call [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) to create an empty ContentInfo object.</span></span>
2.  <span data-ttu-id="5b3fb-110">呼叫 [**IMFASFContentInfo：： SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) ，將設定檔物件提供給 ContentInfo 物件。</span><span class="sxs-lookup"><span data-stu-id="5b3fb-110">Call [**IMFASFContentInfo::SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) to supply the profile object to the ContentInfo object.</span></span> <span data-ttu-id="5b3fb-111">如需建立設定檔的詳細資訊，請參閱 [建立 ASF 設定檔](creating-an-asf-profile.md)。</span><span class="sxs-lookup"><span data-stu-id="5b3fb-111">For information about creating profiles, see [Creating an ASF Profile](creating-an-asf-profile.md).</span></span>
3.  <span data-ttu-id="5b3fb-112">呼叫 [**IMFASFContentInfo：： GenerateHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader) ，並在 *pIHeader* 參數中傳遞 **Null** ，並在 *pcbHeader* 參數中接收已填入 ContentInfo 物件的大小。</span><span class="sxs-lookup"><span data-stu-id="5b3fb-112">Call [**IMFASFContentInfo::GenerateHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader) and pass **NULL** in the *pIHeader* parameter and receive the size of the populated ContentInfo object in the *pcbHeader* parameter.</span></span> <span data-ttu-id="5b3fb-113">應用程式可以使用此值來配置記憶體，或將包含標頭物件的媒體緩衝區。</span><span class="sxs-lookup"><span data-stu-id="5b3fb-113">The application can use this value to allocate memory or the media buffer that will contain the Header Object.</span></span>

    <span data-ttu-id="5b3fb-114">收到的標頭大小包含填補大小，這會根據標頭物件的實際大小來調整。</span><span class="sxs-lookup"><span data-stu-id="5b3fb-114">The header size received includes the padding size, which is adjusted depending on the actual size of the header objects.</span></span> <span data-ttu-id="5b3fb-115">標頭物件的大小上限為 10 MB。</span><span class="sxs-lookup"><span data-stu-id="5b3fb-115">The maximum size of the header objects is 10 MB.</span></span> <span data-ttu-id="5b3fb-116">如果大小超過此值， **GenerateHeader** 就會失敗，並出現 MF \_ E \_ ASF \_ INVALIDDATA 錯誤。</span><span class="sxs-lookup"><span data-stu-id="5b3fb-116">If the size exceeds this value, **GenerateHeader** fails with the MF\_E\_ASF\_INVALIDDATA error.</span></span>

4.  <span data-ttu-id="5b3fb-117">呼叫 [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) ，在步驟3中建立所接收大小的媒體緩衝區。</span><span class="sxs-lookup"><span data-stu-id="5b3fb-117">Call [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) to create a media buffer of the received size in step 3.</span></span>
5.  <span data-ttu-id="5b3fb-118">再次呼叫 **GenerateHeader** ，以從步驟4所建立之媒體緩衝區中的 ContentInfo 物件產生新的 ASF 標頭物件。</span><span class="sxs-lookup"><span data-stu-id="5b3fb-118">Call **GenerateHeader** again to generate the new ASF Header Object from the ContentInfo object in the media buffer created in step 4.</span></span>

    <span data-ttu-id="5b3fb-119">媒體緩衝區中的資料長度會更新，並在 *pcbHeader* 參數中傳回新的大小。</span><span class="sxs-lookup"><span data-stu-id="5b3fb-119">The length of the data in the media buffer is updated and the new size is returned in the *pcbHeader* parameter.</span></span>

6.  <span data-ttu-id="5b3fb-120">在檔案的開頭寫入媒體緩衝區的內容。</span><span class="sxs-lookup"><span data-stu-id="5b3fb-120">Write the contents of the media buffer at the beginning of the file.</span></span> <span data-ttu-id="5b3fb-121">應用程式可以使用位元組資料流程來執行寫入作業。</span><span class="sxs-lookup"><span data-stu-id="5b3fb-121">The application can use the byte stream to perform the writing operation.</span></span> <span data-ttu-id="5b3fb-122">如需範例程式碼，請參閱 [**IMFByteStream：： Write**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write)。</span><span class="sxs-lookup"><span data-stu-id="5b3fb-122">For example code, see [**IMFByteStream::Write**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write).</span></span>

### <a name="example"></a><span data-ttu-id="5b3fb-123">範例</span><span class="sxs-lookup"><span data-stu-id="5b3fb-123">Example</span></span>

<span data-ttu-id="5b3fb-124">下列範例程式碼示範如何建立 ContentInfo 物件，並產生媒體緩衝區來儲存新的標頭物件。</span><span class="sxs-lookup"><span data-stu-id="5b3fb-124">The following example code shows how to create a ContentInfo object and generate a media buffer to store the new Header Object.</span></span> <span data-ttu-id="5b3fb-125">如需使用此程式碼的完整範例，請參閱 [教學課程：將 ASF 資料流程從一個檔案複製到另](tutorial--copying-asf-streams-from-one-file-to-another.md)一個檔案。</span><span class="sxs-lookup"><span data-stu-id="5b3fb-125">For a complete example that uses this code, see [Tutorial: Copying ASF Streams from One File to Another](tutorial--copying-asf-streams-from-one-file-to-another.md).</span></span>


```C++
//-------------------------------------------------------------------
// WriteASFFile
//
// Writes the complete ASF file.
//-------------------------------------------------------------------

HRESULT WriteASFFile( 
    IMFASFContentInfo *pContentInfo, // ASF Content Info for the output file.
    IMFByteStream *pDataStream,      // Data stream.
    PCWSTR pszFile                   // Output file name.
    )
{
    
    IMFMediaBuffer *pHeaderBuffer = NULL;
    IMFByteStream *pWmaStream = NULL;

    DWORD cbHeaderSize = 0;
    DWORD cbWritten = 0;

    // Create output file.
    HRESULT hr = MFCreateFile(
        MF_ACCESSMODE_WRITE, 
        MF_OPENMODE_DELETE_IF_EXIST,
        MF_FILEFLAGS_NONE,
        pszFile,
        &pWmaStream
        );

    // Get the size of the ASF Header Object.
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->GenerateHeader(NULL, &cbHeaderSize);
    }

    // Create a media buffer.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateMemoryBuffer(cbHeaderSize, &pHeaderBuffer);
    }

    // Populate the media buffer with the ASF Header Object.
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->GenerateHeader(pHeaderBuffer, &cbHeaderSize);
    }
 
    // Write the header contents to the byte stream for the output file.
    if (SUCCEEDED(hr))
    {
        hr = WriteBufferToByteStream(pWmaStream, pHeaderBuffer, &cbWritten);
    }

    if (SUCCEEDED(hr))
    {
        hr = pDataStream->SetCurrentPosition(0);
    }

    // Append the data stream to the file.

    if (SUCCEEDED(hr))
    {
        hr = AppendToByteStream(pDataStream, pWmaStream);
    }

    SafeRelease(&pHeaderBuffer);
    SafeRelease(&pWmaStream);

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="5b3fb-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="5b3fb-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b3fb-127">為新檔案撰寫 ASF 標頭物件</span><span class="sxs-lookup"><span data-stu-id="5b3fb-127">Writing an ASF Header Object for a New File</span></span>](writing-an-asf-header-object-for-a-new-file.md)
</dt> </dl>

 

 



