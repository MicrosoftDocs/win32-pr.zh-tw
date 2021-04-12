---
description: 搭配使用 Demux 與基本資料流程
ms.assetid: dd98aada-8309-428e-9609-2542195bc6ec
title: 搭配使用 Demux 與基本資料流程
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6b9004d6c99db96405797016b0d9854c96dae92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319535"
---
# <a name="using-the-demux-with-elementary-streams"></a><span data-ttu-id="2671a-103">搭配使用 Demux 與基本資料流程</span><span class="sxs-lookup"><span data-stu-id="2671a-103">Using the Demux with Elementary Streams</span></span>

<span data-ttu-id="2671a-104">當 MPEG-2 demux 傳遞 PE 承載時，它會以批次方式傳送媒體範例的 ES 位元組資料流程。</span><span class="sxs-lookup"><span data-stu-id="2671a-104">When the MPEG-2 demux delivers PES payloads, it sends the ES byte stream in batches of media samples.</span></span> <span data-ttu-id="2671a-105">預設樣本大小為8K。</span><span class="sxs-lookup"><span data-stu-id="2671a-105">The default sample size is 8K.</span></span> <span data-ttu-id="2671a-106">Demux 會在每個 PE 界限上啟動新的媒體範例，但可能會將單一 PE 承載分成數個範例。</span><span class="sxs-lookup"><span data-stu-id="2671a-106">The demux starts a new media sample on each PES boundary, but may break a single PES payload into several samples.</span></span> <span data-ttu-id="2671a-107">例如，如果 PE 承載是20K，則會在兩個8K 樣本中傳遞，後面接著一個4K 範例。</span><span class="sxs-lookup"><span data-stu-id="2671a-107">For example, if a PES payload is 20K, it will be delivered in two 8K samples followed by one 4K sample.</span></span> <span data-ttu-id="2671a-108">Demux 不會檢查位元組資料流程的內容。</span><span class="sxs-lookup"><span data-stu-id="2671a-108">The demux does not examine the contents of the byte stream.</span></span> <span data-ttu-id="2671a-109">它是由剖析序列標頭和尋找格式變更所需的解碼器。</span><span class="sxs-lookup"><span data-stu-id="2671a-109">It is up to the decoder to parse the sequence headers and look for format changes.</span></span>

<span data-ttu-id="2671a-110">當 demux 濾波器的輸出連接到該解碼器時，它會提供建立 pin 時所指定的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="2671a-110">When the demux filter's output pin connects to the decoder, it offers the media type that was specified when the pin was created.</span></span> <span data-ttu-id="2671a-111">因為 demux 不會檢查 ES 位元組資料流程，所以不會驗證媒體類型。</span><span class="sxs-lookup"><span data-stu-id="2671a-111">Because the demux does not examine the ES byte stream, it does not validate the media type.</span></span> <span data-ttu-id="2671a-112">理論上，MPEG-2 的解碼器應該能夠只連接已填入的主要類型和子類型，以指出資料的類型。</span><span class="sxs-lookup"><span data-stu-id="2671a-112">In theory, an MPEG-2 decoder should be able to connect with just the major type and subtype filled in, to indicate the type of data.</span></span> <span data-ttu-id="2671a-113">然後，此解碼器應檢查抵達媒體範例中的序列標頭。</span><span class="sxs-lookup"><span data-stu-id="2671a-113">The decoder should then examine the sequence headers that arrive in the media samples.</span></span> <span data-ttu-id="2671a-114">不過，在實務上，除非媒體類型包含完整的格式區塊，否則許多解碼器都不會連接。</span><span class="sxs-lookup"><span data-stu-id="2671a-114">However, in practice, many decoders will not connect unless the media type includes a complete format block.</span></span>

<span data-ttu-id="2671a-115">例如，假設 PID 0x31 包含 MPEG-2 主要設定檔的影片。</span><span class="sxs-lookup"><span data-stu-id="2671a-115">For example, suppose that PID 0x31 contains MPEG-2 main profile video.</span></span> <span data-ttu-id="2671a-116">您至少必須執行下列步驟。</span><span class="sxs-lookup"><span data-stu-id="2671a-116">At a minimum, you would need to do the following steps.</span></span>

<span data-ttu-id="2671a-117">首先，建立 MPEG-2 影片的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="2671a-117">First, create a media type for MPEG-2 video.</span></span> <span data-ttu-id="2671a-118">立即保留格式區塊：</span><span class="sxs-lookup"><span data-stu-id="2671a-118">Leaving aside the format block for now:</span></span>


```C++
AM_MEDIA_TYPE mt;
ZeroMemory(&mt, sizeof(AM_MEDIA_TYPE));
mt.majortype = MEDIATYPE_Video ;
mt.subtype = MEDIASUBTYPE_MPEG2_VIDEO;
// Possibly create a format block (not shown here).
```



<span data-ttu-id="2671a-119">接下來，在 demux 上建立輸出圖釘：</span><span class="sxs-lookup"><span data-stu-id="2671a-119">Next, create an output pin on the demux:</span></span>


```C++
// Query the demux filter for IMpeg2Demultiplexer.
IMpeg2Demultiplexer *pDemux;
hr = pFilter->QueryInterface(IID_IMpeg2Demultiplexer, (void**)&pDemux);
if (SUCCEEDED(hr))
{
    // Create a new output pin.
    IPin *pPin0;
    hr = pDemux->CreateOutputPin(&mt, L"Video Pin", &pPin0);
    if (SUCCEEDED(hr))
    {
        ....
    }
}
```



<span data-ttu-id="2671a-120">然後，查詢 **IMPEG2PIDMap** 介面的新 pin，並呼叫 **MapPID**。</span><span class="sxs-lookup"><span data-stu-id="2671a-120">Then, query the new pin for the **IMPEG2PIDMap** interface and call **MapPID**.</span></span> <span data-ttu-id="2671a-121">指定適用于 PE 承載的 PID 號碼0x30< 和媒體 \_ 基本 \_ 資料流程。</span><span class="sxs-lookup"><span data-stu-id="2671a-121">Specify PID number 0x30, and MEDIA\_ELEMENTARY\_STREAM for PES payloads.</span></span>


```C++
// Query the pin for IMPEG2PIDMap. This implicitly configures the
// demux to carry a transport stream. 
IMPEG2PIDMap *pPidMap;
hr = pPin0->QueryInterface(IID_IMPEG2PIDMap, (void**)&pPidMap);
if (SUCCEEDED(hr))
{
    // Assign PID 0x31 to pin 0. Set the type to "PES payload."
    ULONG Pid = 0x031;
    hr = pPidMap->MapPID(1, &Pid, MEDIA_ELEMENTARY_STREAM);
    pPidMap->Release();
}
```



<span data-ttu-id="2671a-122">最後，在完成時釋放所有介面：</span><span class="sxs-lookup"><span data-stu-id="2671a-122">Finally, release all interfaces when you are done:</span></span>


```C++
pPin0->Release();
pDemux->Release();
```



<span data-ttu-id="2671a-123">以下是設定媒體類型（包括格式區塊）的更完整範例。</span><span class="sxs-lookup"><span data-stu-id="2671a-123">Here is a more complete example of setting the media type, including the format block.</span></span> <span data-ttu-id="2671a-124">此範例仍假設 MPEG-2 主要設定檔的影片。</span><span class="sxs-lookup"><span data-stu-id="2671a-124">This example still assumes an MPEG-2 main profile video.</span></span> <span data-ttu-id="2671a-125">詳細資料會根據資料流程內容而有所不同：</span><span class="sxs-lookup"><span data-stu-id="2671a-125">The details will vary depending on stream contents:</span></span>


```C++
// Set up a byte array to hold the first sequence header. 
// This may or may not be required, depending on the decoder.
BYTE SeqHdr[] = { ... };  // Contains the sequence header (not shown).

AM_MEDIA_TYPE mt;
ZeroMemory(&mt, sizeof(AM_MEDIA_TYPE));
mt.majortype = MEDIATYPE_Video ;
mt.subtype = MEDIASUBTYPE_MPEG2_VIDEO;
mt.formattype = FORMAT_MPEG2Video;

// Allocate the format block, including space for the sequence header. 
mt.cbFormat = sizeof(MPEG2VIDEOINFO) + sizeof(SeqHdr);
mt.pbFormat = (BYTE*)CoTaskMemAlloc(mt.cbFormat);
if (mt.pbFormat == NULL)
{
    // Out of memory; return an error code.
}
ZeroMemory(mt.pbFormat, mt.cbFormat);

// Cast the buffer pointer to an MPEG2VIDEOINFO struct.
MPEG2VIDEOINFO *pMVIH = (MPEG2VIDEOINFO*)mt.pbFormat;

RECT rcSrc = {0, 480, 0, 720};        // Source rectangle.
pMVIH->hdr.rcSource = rcSrc;
pMVIH->hdr.dwBitRate = 4000000;       // Bit rate.
pMVIH->hdr.AvgTimePerFrame = 333667;  // 29.97 fps.
pMVIH->hdr.dwPictAspectRatioX = 4;    // 4:3 aspect ratio.
pMVIH->hdr.dwPictAspectRatioY = 3;

// BITMAPINFOHEADER information.
pMVIH->hdr.bmiHeader.biSize = 40;
pMVIH->hdr.bmiHeader.biWidth = 720;
pMVIH->hdr.bmiHeader.biHeight = 480;

pMVIH->dwLevel = AM_MPEG2Profile_Main;  // MPEG-2 profile. 
pMVIH->dwProfile = AM_MPEG2Level_Main;  // MPEG-2 level.

// Copy the sequence header into the format block.
pMVIH->cbSequenceHeader = sizeof(SeqHdr); // Size of sequence header.
memcpy(pMVIH->dwSequenceHeader, SeqHdr, sizeof(SeqHdr));
```



## <a name="related-topics"></a><span data-ttu-id="2671a-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="2671a-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2671a-127">使用 MPEG-2 信號信號</span><span class="sxs-lookup"><span data-stu-id="2671a-127">Using the MPEG-2 Demultiplexer</span></span>](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 



