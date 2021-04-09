---
description: H.264 影片類型
ms.assetid: aa3166b2-6b04-44fa-bc9d-c8ff46f99201
title: H.264 影片類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dcd33703798e305947cdcd663c7a86c7c494683
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103935612"
---
# <a name="h264-video-types"></a>H.264 影片類型

下列是針對 h.264 video 定義的媒體子類型。



| Subtype                | FOURCC | Description                                                    |
|------------------------|--------|----------------------------------------------------------------|
| **MEDIASUBTYPE \_ AVC1** | AVC1 | 位流不含開始代碼。                           |
| **MEDIASUBTYPE \_ H264** | H264 | 位流與開始代碼。                              |
| **MEDIASUBTYPE \_ h264** | h264 | 相當於 **MEDIASUBTYPE \_ H264**，具有不同的 FOURCC。 |
| **MEDIASUBTYPE \_ X264** | 'X264' | 相當於 **MEDIASUBTYPE \_ H264**，具有不同的 FOURCC。 |
| **MEDIASUBTYPE \_ x264** | 'x264' | 相當於 **MEDIASUBTYPE \_ H264**，具有不同的 FOURCC。 |



 

這些子類型 Guid 會在 wmcodecdsp 中宣告。

這些媒體類型的主要差異在於位流中的起始碼是否存在。 如果子類型為 **MEDIASUBTYPE \_ AVC1**，則位流不會包含開始程式碼。

### <a name="h264-bitstream-with-start-codes"></a>使用開始代碼的 h.264 位流

以無線方式傳輸，或包含在 MPEG 2 程式或傳輸串流中，或在 HD DVD 上錄製的 h.264 bitstreams，會如 ITU-T 的附錄 B 中所述格式化。 根據此規格，位流包含一連串的網路抽象層單位 (NALUs) ，其中每個單位的開頭都是等於0x000001 或0x00000001 的起始程式碼。

當位流中有起始程式碼時，會使用下列媒體類型：



|             |                                                                                                   |
|-------------|---------------------------------------------------------------------------------------------------|
| 主要類型  | **媒體 \_ 媒體**                                                                              |
| 子類型    | **MEDIASUBTYPE \_H264**、 **MEDIASUBTYPE \_ h264**、 **MEDIASUBTYPE \_ X264** 或 **MEDIASUBTYPE \_ X264** |
| 格式類型 | **格式 \_VideoInfo**、 **format \_ VideoInfo2**、 **format \_ MPEG2Video** 或 **GUID \_ Null**          |



 

如果格式類型為 **GUID \_ Null**，則不存在任何格式結構。

當位流包含開始程式碼時，此處所列的任何格式類型都已足夠，因為此解碼器不需要任何額外的資訊來剖析串流。 位流已包含此解碼器所需的所有資訊，而起始程式碼可讓解碼器找出每個 NALU 的開頭。

下列子類型相同：

### <a name="h264-bitstream-without-start-codes"></a>位流不含起始碼

[設定] 容器格式會儲存不含起始代碼的 h.264 資料。 相反地，每個 NALU 的前面都會加上長度欄位，這會提供 NALU 的長度（以位元組為單位）。 長度欄位的大小可能會有所不同，但通常是1、2或4個位元組。

當位流中沒有起始碼時，會使用下列媒體類型。



|             |                        |
|-------------|------------------------|
| 主要類型  | **媒體 \_ 媒體**   |
| Subtype     | **MEDIASUBTYPE \_ AVC1** |
| 格式類型 | **格式 \_ MPEG2Video** |



 

格式區塊是 [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) 結構。 應填入此結構，如下所示：

-   **hdr**：描述位流的 [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) 結構。 結構的 [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) 部分之後不會有色彩表，而且 **biClrUsed** 必須為零。
-   **dwStartTimeCode**：未使用。 設定為零。
-   **cbSequenceHeader**： **dwSequenceHeader** 陣列的長度（以位元組為單位）。
-   **dwProfile**：指定 h.264 設定檔。
-   **dwLevel**：指定 h.264 層級。
-   **dwFlags**：每個 **NALU** 之前出現的長度欄位所使用的位元組數目。 [長度] 欄位表示下列 NALU 的大小（以位元組為單位）。 例如，如果 **dwFlags** 是4，則每個 NALU 的前面都會加上4個位元組的長度欄位。 有效的值為1、2和4。
-   **dwSequenceHeader**：一個位元組陣列，其中可能包含 sequence 參數集 (SPS) ，以及 (PPS) NALUs 的圖片參數集。

「配置」容器可能會包含 sequence 參數集 (SPS) 或圖片參數集 (PPS) 作為檔案標頭中的特殊 NAL 單位或個別資料流程 (不同于影片串流) 。 當建立格式時，媒體類型可以在 **dwSequenceHeader** 陣列中指定 SPS 和 PPS NAL 單位。 如果 **cbSequenceHeader** 大於零，則 **dwSequenceHeader** 是位元組陣列的開頭，其中包含 SPS 和 PPS NALUs （以2位元組長度欄位分隔），而所有以網路位元組順序排列， (位元組由大到小的) 。 您可以同時具有 SPS 和 PPS，而不是其中一個類型，或無。 您可以檢查 NALU 本身的 **nal \_ unit \_ type** 欄位來判斷每個 NALU 的實際型別。

使用此媒體類型時，每個媒體範例都會從 NALU 的開頭開始，而 NAL 的單位則不會跨越樣本。 這可讓解碼器從資料損毀或捨棄的範例復原。

 

 



