---
description: 讀取現有檔案的 ASF 標頭物件
ms.assetid: 0e37f0d3-a37b-4f36-a133-7b1922e9944b
title: 讀取現有檔案的 ASF 標頭物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b231cb0b9af6b24f84efaa6403a4774e66bbb646
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971689"
---
# <a name="reading-the-asf-header-object-of-an-existing-file"></a><span data-ttu-id="a4ac7-103">讀取現有檔案的 ASF 標頭物件</span><span class="sxs-lookup"><span data-stu-id="a4ac7-103">Reading the ASF Header Object of an Existing File</span></span>

<span data-ttu-id="a4ac7-104">ASF ContentInfo 物件儲存的資訊代表媒體檔案的 ASF 標頭物件。</span><span class="sxs-lookup"><span data-stu-id="a4ac7-104">The ASF ContentInfo object stores information that represents the ASF Header Objects of a media file.</span></span> <span data-ttu-id="a4ac7-105">需要填入的 ContentInfo 物件，才能讀取和剖析現有的 ASF 檔。</span><span class="sxs-lookup"><span data-stu-id="a4ac7-105">A populated ContentInfo object is required in order to read and parse an existing ASF file.</span></span>

<span data-ttu-id="a4ac7-106">藉由呼叫 [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) 函式來建立 ContentInfo 物件之後，應用程式必須使用要讀取之 ASF 檔案的標頭資訊來初始化它。</span><span class="sxs-lookup"><span data-stu-id="a4ac7-106">After creating the ContentInfo object by calling the [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) function, the application must initialize it with header information from the ASF file that is to be read.</span></span> <span data-ttu-id="a4ac7-107">若要填入物件，請呼叫 [**IMFASFContentInfo：:P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader)。</span><span class="sxs-lookup"><span data-stu-id="a4ac7-107">To populate the object, call [**IMFASFContentInfo::ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader).</span></span>

<span data-ttu-id="a4ac7-108">**ParseHeader** 需要包含 ASF 檔案標頭物件的媒體緩衝區。</span><span class="sxs-lookup"><span data-stu-id="a4ac7-108">**ParseHeader** requires a media buffer that contains the Header Object of the ASF file.</span></span> <span data-ttu-id="a4ac7-109">其中一個選項是使用標頭物件來填滿媒體緩衝區，以建立檔案的位元組資料流程，然後從位元組資料流程將前30個位元組的資料讀取至媒體緩衝區。</span><span class="sxs-lookup"><span data-stu-id="a4ac7-109">One option is to fill a media buffer with the Header Object to create a byte stream for the file and then read the first 30 bytes of data from the byte stream into a media buffer.</span></span> <span data-ttu-id="a4ac7-110">然後，您可以將標頭物件的前24個位元組傳遞給 [**IMFASFContentInfo：： GetHeaderSize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getheadersize) 方法，以取得大小。</span><span class="sxs-lookup"><span data-stu-id="a4ac7-110">You can then get the size by passing the first 24 bytes of the Header Object to the [**IMFASFContentInfo::GetHeaderSize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getheadersize) method.</span></span> <span data-ttu-id="a4ac7-111">取得大小之後，您可以讀取媒體緩衝區中的整個標頭物件，並將它傳遞至 **ParseHeader**。</span><span class="sxs-lookup"><span data-stu-id="a4ac7-111">After getting the size, you can read the entire Header Object in a media buffer and pass it to **ParseHeader**.</span></span> <span data-ttu-id="a4ac7-112">方法會在 *cbOffsetWithinHeader* 參數中指定之媒體緩衝區開頭的位移處開始剖析。</span><span class="sxs-lookup"><span data-stu-id="a4ac7-112">The method starts parsing at the offset from the start of the media buffer specified in the *cbOffsetWithinHeader* parameter.</span></span>

<span data-ttu-id="a4ac7-113">下列程式碼範例會建立 ContentInfo 物件，並將其初始化，以讀取位元組資料流程中包含的現有 ASF 檔。</span><span class="sxs-lookup"><span data-stu-id="a4ac7-113">The following example code creates and initializes a ContentInfo object for reading an existing ASF file contained in a byte stream.</span></span> <span data-ttu-id="a4ac7-114">首先，我們會定義 helper 函式，以從位元組資料流程讀取資料，並配置媒體緩衝區來保存資料：</span><span class="sxs-lookup"><span data-stu-id="a4ac7-114">First, we define a helper function that reads data from a byte stream and allocates a media buffer to hold the data:</span></span>


```C++
// Read the ASF Header Object from a byte stream and return a pointer to the 
// populated ASF ContentInfo object.
//
// The current read position of the byte stream must be at the start of the
// ASF Header Object.

HRESULT CreateContentInfo(IMFByteStream *pStream, 
    IMFASFContentInfo **ppContentInfo)
{
    const DWORD MIN_ASF_HEADER_SIZE = 30;
    
    QWORD cbHeader = 0;
    DWORD cbBuffer = 0;

    IMFASFContentInfo *pContentInfo = NULL;
    IMFMediaBuffer *pBuffer = NULL;

    // Create the ASF ContentInfo object.
    HRESULT hr = MFCreateASFContentInfo(&pContentInfo);
    
    // Read the first 30 bytes to find the total header size.

    if (SUCCEEDED(hr))
    {
        hr = MFCreateMemoryBuffer(MIN_ASF_HEADER_SIZE, &pBuffer);
    }
    if (SUCCEEDED(hr))
    {
        hr = ReadFromByteStream(pStream, pBuffer,MIN_ASF_HEADER_SIZE);
    }
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->GetHeaderSize(pBuffer, &cbHeader);
    }

    // Pass the first 30 bytes to the ContentInfo object.
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->ParseHeader(pBuffer, 0);
    }

    SafeRelease(&pBuffer);

    if (SUCCEEDED(hr))
    {
        cbBuffer = (DWORD)(cbHeader - MIN_ASF_HEADER_SIZE);

        hr = MFCreateMemoryBuffer(cbBuffer, &pBuffer);
    }

    // Read the rest of the header and finish parsing the header.
    if (SUCCEEDED(hr))
    {
        hr = ReadFromByteStream(pStream, pBuffer, cbBuffer);
    }
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->ParseHeader(pBuffer, MIN_ASF_HEADER_SIZE);
    }
    if (SUCCEEDED(hr))
    {
        // Return the pointer to the caller.
        *ppContentInfo = pContentInfo;
        (*ppContentInfo)->AddRef();
    }
    SafeRelease(&pBuffer);
    SafeRelease(&pContentInfo);
    return hr;
} 
```



<span data-ttu-id="a4ac7-115">下一個範例會從位元組資料流程讀取 ASF 標頭物件，並填入 ASF ContentInfo 物件。</span><span class="sxs-lookup"><span data-stu-id="a4ac7-115">The next example reads the ASF Header Object from a byte stream and populates an ASF ContentInfo object.</span></span>


```C++
// Read the ASF Header Object from a byte stream and return a pointer to the 
// populated ASF ContentInfo object.
//
// The current read position of the byte stream must be at the start of the
// ASF Header Object.

HRESULT CreateContentInfo(IMFByteStream *pStream, 
    IMFASFContentInfo **ppContentInfo)
{
    const DWORD MIN_ASF_HEADER_SIZE = 30;
    
    QWORD cbHeader = 0;
    DWORD cbBuffer = 0;

    IMFASFContentInfo *pContentInfo = NULL;
    IMFMediaBuffer *pBuffer = NULL;

    // Create the ASF ContentInfo object.
    HRESULT hr = MFCreateASFContentInfo(&pContentInfo);
    
    // Read the first 30 bytes to find the total header size.

    if (SUCCEEDED(hr))
    {
        hr = MFCreateMemoryBuffer(MIN_ASF_HEADER_SIZE, &pBuffer);
    }
    if (SUCCEEDED(hr))
    {
        hr = ReadFromByteStream(pStream, pBuffer,MIN_ASF_HEADER_SIZE);
    }
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->GetHeaderSize(pBuffer, &cbHeader);
    }

    // Pass the first 30 bytes to the ContentInfo object.
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->ParseHeader(pBuffer, 0);
    }

    SafeRelease(&pBuffer);

    if (SUCCEEDED(hr))
    {
        cbBuffer = (DWORD)(cbHeader - MIN_ASF_HEADER_SIZE);

        hr = MFCreateMemoryBuffer(cbBuffer, &pBuffer);
    }

    // Read the rest of the header and finish parsing the header.
    if (SUCCEEDED(hr))
    {
        hr = ReadFromByteStream(pStream, pBuffer, cbBuffer);
    }
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->ParseHeader(pBuffer, MIN_ASF_HEADER_SIZE);
    }
    if (SUCCEEDED(hr))
    {
        // Return the pointer to the caller.
        *ppContentInfo = pContentInfo;
        (*ppContentInfo)->AddRef();
    }
    SafeRelease(&pBuffer);
    SafeRelease(&pContentInfo);
    return hr;
} 
```



> [!Note]  
> <span data-ttu-id="a4ac7-116">這些範例會使用 [SafeRelease](saferelease.md) 函式來釋放介面指標。</span><span class="sxs-lookup"><span data-stu-id="a4ac7-116">These examples use the [SafeRelease](saferelease.md) function to release interface pointers.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="a4ac7-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="a4ac7-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4ac7-118">ASF ContentInfo 物件</span><span class="sxs-lookup"><span data-stu-id="a4ac7-118">ASF ContentInfo Object</span></span>](asf-contentinfo-object.md)
</dt> <dt>

[<span data-ttu-id="a4ac7-119">ASF 標頭物件</span><span class="sxs-lookup"><span data-stu-id="a4ac7-119">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="a4ac7-120">媒體基礎中的 ASF 支援</span><span class="sxs-lookup"><span data-stu-id="a4ac7-120">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="a4ac7-121">從 ASF 標頭物件取得資訊</span><span class="sxs-lookup"><span data-stu-id="a4ac7-121">Getting Information from ASF Header Objects</span></span>](getting-information-from-asf-header-objects.md)
</dt> </dl>

 

 



