---
description: MPEG-2 分隔器媒體類型
ms.assetid: d0ff2011-4ee3-4f5e-8bd0-af9f4c6346e8
title: MPEG-2 分隔器媒體類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b29151e5128531cbd2e71c6eda0f2b4b16658c8e68577de0fbb0542189c2931f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748578"
---
# <a name="mpeg-2-splitter-media-types"></a>MPEG-2 分隔器媒體類型

[Mpeg-2 分隔](mpeg-2-splitter.md)器篩選器目前支援音訊和影片。 由 DVD 定義的子串流支援杜比 AC-3。 篩選準則也支援 MPEG-2 音訊。 媒體類型取決於 MPEG-2 分隔器是否提供 PE 封包或 PE 承載。

### <a name="video"></a>影片

針對 MPEG-2 影片，媒體類型如下所示。


|                | PE 輸出 | 承載輸出
|------------------|------------------------------------------|--------------------------------|
| **主要類型**       | **媒體媒體的 \_ MPEG2 \_ pe**                | **媒體 \_ 媒體**           |
| **亞**          | **MEDIASUBTYPE \_ MPEG2 \_ 影片**           | **MEDIASUBTYPE \_ MPEG2 \_ 影片** |
| **格式類型**      | **格式 \_ MPEG2Video**                   | **格式 \_ MPEG2Video**         |
| **格式結構** | [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) | **MPEG2VIDEOINFO**             |



 

### <a name="ac-3-audio"></a>AC-3 音訊

針對 AC 3 音訊，媒體類型如下所示。

| | PE 輸出 | 承載輸出 |
|------------------|--------------------------------------|------------------------------|
| **主要類型**       | **媒體媒體的 \_ MPEG2 \_ pe**                | **媒體 \_ 媒體**         |
| **亞**          | **MEDIASUBTYPE \_ 杜 \_ AC3**             | **MEDIASUBTYPE \_ 杜 \_ AC3** |
| **格式類型**      | 格式 \_ WaveFormatEx                 | **格式 \_ WaveFormatEx**     |
| **格式結構** | [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) | **WAVEFORMATEX**             |



 

適用于 AC-3 的 **WAVEFORMATEX** 結構的 **wFormatTag** 成員目前為 **WAVE \_ 格式 \_ 未知**，但這可能會變更。

### <a name="mpeg-2-audio"></a>MPEG-2 音訊

針對 MPEG-2 音訊，媒體類型如下所示。



|  | PE 輸出 | 承載輸出 |
|------------------|-------------------------------|--------------------------------|
| **主要類型**       | **媒體媒體的 \_ MPEG2 \_ pe**     | **媒體 \_ 媒體**           |
| **亞**          | **MEDIASUBTYE \_ MPEG2 \_ 音訊** | **MEDIASUBTYPE \_ MPEG2 \_ 音訊** |
| **格式類型**      | **格式 \_ WaveFormatEx**      | **格式 \_ WaveFormatEx**       |
| **格式結構** | **WAVEFORMATEX**              | **WAVEFORMATEX**               |



 

MPEG-2 音訊的 **WAVEFORMATEX** 結構的 **wFormatTag** 成員目前為 **WAVE \_ 格式 \_ 未知**，但這可能會變更。

MPEG-2 分割器會假設串流 D0 至 DF 是用於多重通道擴充資料流程，因為它們適用于 DVD MPEG-2 音訊。 因此，每當選取資料流程 C *x* 時，分隔器也會轉送串流 D *x* 的封包。

### <a name="lpcm-audio"></a>LPCM 音訊

針對 LPCM 音訊，媒體類型如下所示。



|  | PE 輸出 | 承載輸出 |
|------------------|------------------------------------|------------------------------------|
| **主要類型**       | **媒體媒體的 \_ MPEG2 \_ pe**          | **媒體 \_ 媒體**               |
| **亞**          | **MEDIASUBTYPE \_ DVD \_ LPCM \_ 音訊** | **MEDIASUBTYPE \_ DVD \_ LPCM \_ 音訊** |
| **格式類型**      | **格式 \_ WaveFormatEx**           | **格式 \_ WaveFormatEx**           |
| **格式結構** | **WAVEFORMATEX**                   | **WAVEFORMATEX**                   |



 

**WAVEFORMATEX** 結構的 LPCM 音訊 **wFormatTag** 成員目前為 **WAVE \_ 格式 \_ 未知**，但這可能會變更。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[MPEG-2 媒體類型](mpeg-2-media-types.md)
</dt> </dl>

 

 
