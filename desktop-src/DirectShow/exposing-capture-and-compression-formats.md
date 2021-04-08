---
description: 公開捕捉和壓縮格式
ms.assetid: f7466cfe-b13e-4ee9-82f9-0528ed97bf99
title: 公開捕捉和壓縮格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02051d9e68b3ad919b96dca53b674305787b3186
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103688496"
---
# <a name="exposing-capture-and-compression-formats"></a>公開捕捉和壓縮格式

本文描述如何使用 [**IAMStreamConfig：： GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) 方法來傳回捕捉和壓縮格式。 這種方法可以取得所接受媒體類型的詳細資訊，而不是列舉釘選媒體類型的傳統方式，因此通常應該改用。 **GetStreamCaps** 可以傳回音頻或影片允許的格式類型相關資訊。 此外，本文還提供一些範例程式碼，示範如何重新連接轉換篩選的輸入 pin，以確保您的篩選準則可以產生特定的輸出。

**GetStreamCaps** 方法會傳回一組媒體類型和功能結構的陣列。 媒體類型是 [**\_ 媒體 \_**](/windows/win32/api/strmif/ns-strmif-am_media_type) 類型結構，而功能則是以 [**音訊 \_ 串流設定 \_ \_ caps**](/windows/win32/api/strmif/ns-strmif-audio_stream_config_caps) 結構或 [**影片 \_ 串流設定 \_ \_ caps**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) 結構來表示。 本文的第一節提供影片範例，而第二個區段則呈現音訊範例。

本文包含下列主題：

-   [影片功能](video-capabilities.md)
-   [音訊功能](audio-capabilities.md)
-   [重新連接您的輸入，以確保特定的輸出類型](reconnecting-your-input-to-ensure-specific-output-types.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[撰寫 DirectShow 篩選器](writing-directshow-filters.md)
</dt> </dl>

 

 



