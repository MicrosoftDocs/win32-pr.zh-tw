---
description: 搭配使用 Demux 與基本資料流程
ms.assetid: dd98aada-8309-428e-9609-2542195bc6ec
title: 搭配使用 Demux 與基本資料流程
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dec805b4c93432c6532edaefac50e9bd15ad8fac5a7d9672fd358c66e57363fd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119964668"
---
# <a name="using-the-demux-with-elementary-streams"></a>搭配使用 Demux 與基本資料流程

當 MPEG-2 demux 傳遞 PE 承載時，它會以批次方式傳送媒體範例的 ES 位元組資料流程。 預設樣本大小為8K。 Demux 會在每個 PE 界限上啟動新的媒體範例，但可能會將單一 PE 承載分成數個範例。 例如，如果 PE 承載是20K，則會在兩個8K 樣本中傳遞，後面接著一個4K 範例。 Demux 不會檢查位元組資料流程的內容。 它是由剖析序列標頭和尋找格式變更所需的解碼器。

當 demux 濾波器的輸出連接到該解碼器時，它會提供建立 pin 時所指定的媒體類型。 因為 demux 不會檢查 ES 位元組資料流程，所以不會驗證媒體類型。 理論上，MPEG-2 的解碼器應該能夠只連接已填入的主要類型和子類型，以指出資料的類型。 然後，此解碼器應檢查抵達媒體範例中的序列標頭。 不過，在實務上，除非媒體類型包含完整的格式區塊，否則許多解碼器都不會連接。

例如，假設 PID 0x31 包含 MPEG-2 主要設定檔的影片。 您至少必須執行下列步驟。

首先，建立 MPEG-2 影片的媒體類型。 立即保留格式區塊：


```C++
AM_MEDIA_TYPE mt;
ZeroMemory(&mt, sizeof(AM_MEDIA_TYPE));
mt.majortype = MEDIATYPE_Video ;
mt.subtype = MEDIASUBTYPE_MPEG2_VIDEO;
// Possibly create a format block (not shown here).
```



接下來，在 demux 上建立輸出圖釘：


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



然後，查詢 **IMPEG2PIDMap** 介面的新 pin，並呼叫 **MapPID**。 指定適用于 PE 承載的 PID 號碼0x30< 和媒體 \_ 基本 \_ 資料流程。


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



最後，在完成時釋放所有介面：


```C++
pPin0->Release();
pDemux->Release();
```



以下是設定媒體類型（包括格式區塊）的更完整範例。 此範例仍假設 MPEG-2 主要設定檔的影片。 詳細資料會根據資料流程內容而有所不同：


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 MPEG-2 信號信號](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 



