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
# <a name="using-the-demux-with-psi-streams"></a>使用 Demux 搭配 PSI 資料流程

若要使用 MPEG-2 demux 篩選從 MPEG-2 傳輸資料流程取得 PSI 資訊，請在 demux 上以下列媒體類型建立輸出 pin：

-   主要類型： KSDATAFORMAT \_ 類型的 \_ MPEG2 \_ 區段
-   子類型： MEDIASUBTYPE \_ None
-   格式類型： GUID \_ Null

然後使用所需的 PID 和旗標媒體 MPEG2 PSI 來呼叫輸出 pin 的 [**IMPEG2PIDMap：： MapPID**](/previous-versions/windows/desktop/api/Bdaiface/nf-bdaiface-impeg2pidmap-mappid) 方法 \_ \_ 。


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



每個完整的 PSI 區段都是在一個媒體範例中提供。 若要取得與資料表區段相關聯的 PID 號碼，請在媒體範例上呼叫 [**IMediaSample2：： GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) 。 在 **AM \_ sample2.xml \_ 屬性** 結構中， **dwTypeSpecificFlags** 旗標的低13位提供 PID。 如果您將多個 PSI Pid 對應到相同的輸出 pin，這會很有用。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 MPEG-2 信號信號](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 



