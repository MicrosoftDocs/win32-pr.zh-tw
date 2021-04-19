---
description: 使用 Demux 搭配 PSI 資料流程
ms.assetid: 355e905e-ff21-4bde-a018-ed9631ef5ed5
title: 使用 Demux 搭配 PSI 資料流程
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 659e4a12bfef25f24a5e6cac38d191f86ab80b4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996820"
---
# <a name="using-the-demux-with-psi-streams"></a><span data-ttu-id="5cbad-103">使用 Demux 搭配 PSI 資料流程</span><span class="sxs-lookup"><span data-stu-id="5cbad-103">Using the Demux with PSI Streams</span></span>

<span data-ttu-id="5cbad-104">若要使用 MPEG-2 demux 篩選從 MPEG-2 傳輸資料流程取得 PSI 資訊，請在 demux 上以下列媒體類型建立輸出 pin：</span><span class="sxs-lookup"><span data-stu-id="5cbad-104">To get PSI information from an MPEG-2 transport stream using the MPEG-2 demux filter, create an output pin on the demux with the following media type:</span></span>

-   <span data-ttu-id="5cbad-105">主要類型： KSDATAFORMAT \_ 類型的 \_ MPEG2 \_ 區段</span><span class="sxs-lookup"><span data-stu-id="5cbad-105">Major type: KSDATAFORMAT\_TYPE\_MPEG2\_SECTIONS</span></span>
-   <span data-ttu-id="5cbad-106">子類型： MEDIASUBTYPE \_ None</span><span class="sxs-lookup"><span data-stu-id="5cbad-106">Subtype: MEDIASUBTYPE\_None</span></span>
-   <span data-ttu-id="5cbad-107">格式類型： GUID \_ Null</span><span class="sxs-lookup"><span data-stu-id="5cbad-107">Format type: GUID\_NULL</span></span>

<span data-ttu-id="5cbad-108">然後使用所需的 PID 和旗標媒體 MPEG2 PSI 來呼叫輸出 pin 的 [**IMPEG2PIDMap：： MapPID**](/previous-versions/windows/desktop/api/Bdaiface/nf-bdaiface-impeg2pidmap-mappid) 方法 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="5cbad-108">Then call the output pin's [**IMPEG2PIDMap::MapPID**](/previous-versions/windows/desktop/api/Bdaiface/nf-bdaiface-impeg2pidmap-mappid) method with the desired PID and the flag MEDIA\_MPEG2\_PSI.</span></span>


```C++
// Query the demux filter for IMpeg2Demultiplexer.
IMpeg2Demultiplexer *pDemux = NULL;
hr = pFilter->QueryInterface(IID_IMpeg2Demultiplexer, (void**)&pDemux);
if (SUCCEEDED(hr))
{
    // Define the media type.
    AM_MEDIA_TYPE mt;
    ZeroMemory(&mt, sizeof(AM_MEDIA_TYPE));
    mt.majortype = KSDATAFORMAT_TYPE_MPEG2_SECTIONS;
    mt.subtype = MEDIASUBTYPE_None;

    // Create a new output pin.
    IPin *pPin;
    hr = pDemux->CreateOutputPin(&mt, L"PSI Pin", &pPin);
    if (SUCCEEDED(hr))
    {
        // Map the PID.
        IMPEG2PIDMap *pPidMap = NULL;
        hr = pPin->QueryInterface(IID_IMPEG2PIDMap, (void**)&pPidMap);
        if (SUCCEEDED(hr))
        {
            ULONG Pid[] = { 0x00 }; // Map any desired PIDs. 
            ULONG cPid = 1;
            hr = pPidMap->MapPID(cPid, Pid, MEDIA_MPEG2_PSI);
            pPidMap->Release();
        }
        pPin->Release();
    }
    pDemux->Release();
}
```



<span data-ttu-id="5cbad-109">每個完整的 PSI 區段都是在一個媒體範例中提供。</span><span class="sxs-lookup"><span data-stu-id="5cbad-109">Each complete PSI section is delivered in one media sample.</span></span> <span data-ttu-id="5cbad-110">若要取得與資料表區段相關聯的 PID 號碼，請在媒體範例上呼叫 [**IMediaSample2：： GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) 。</span><span class="sxs-lookup"><span data-stu-id="5cbad-110">To retrieve the PID number associated with a table section, call [**IMediaSample2::GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) on the media sample.</span></span> <span data-ttu-id="5cbad-111">在 **AM \_ sample2.xml \_ 屬性** 結構中， **dwTypeSpecificFlags** 旗標的低13位提供 PID。</span><span class="sxs-lookup"><span data-stu-id="5cbad-111">The PID is given in the low 13 bits of the **dwTypeSpecificFlags** flag in the **AM\_SAMPLE2\_PROPERTIES** structure.</span></span> <span data-ttu-id="5cbad-112">如果您將多個 PSI Pid 對應到相同的輸出 pin，這會很有用。</span><span class="sxs-lookup"><span data-stu-id="5cbad-112">This is useful if you map multiple PSI PIDs to the same output pin.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5cbad-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="5cbad-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5cbad-114">使用 MPEG-2 信號信號</span><span class="sxs-lookup"><span data-stu-id="5cbad-114">Using the MPEG-2 Demultiplexer</span></span>](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 



