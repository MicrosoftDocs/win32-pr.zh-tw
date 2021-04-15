---
description: 音訊功能
ms.assetid: de96f6ee-b526-4ac2-93ac-a731f86ef5d5
title: 音訊功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c2cf02927b69d807f400c4185a7d4ddbdd14322
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510293"
---
# <a name="audio-capabilities"></a>音訊功能

針對音訊功能， [**IAMStreamConfig：： GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) 會傳回一組 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type) 和 [**音訊串流設定 \_ \_ \_ cap**](/windows/win32/api/strmif/ns-strmif-audio_stream_config_caps) 結構的陣列。 如同影片，您可以使用這種方式來公開 pin 的所有音訊功能，例如資料速率，以及它是否支援 mono 或身歷聲。

如需與 GetStreamCaps 相關的影片相關範例，請參閱 [影片功能](video-capabilities.md)。

假設您支援脈衝程式碼調整 (PCM) wave 格式 (如 [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) 結構所表示) 以每秒11025、22050和44100樣本的取樣率，全都以8或16位 mono 或身歷聲表示。 在此情況下，您會提供兩組結構。 第一組會有 **音訊 \_ 串流設定 \_ \_ cap** 功能結構，指出您最多可支援每秒11025到22050個樣本，每秒最多可有11025個樣本 (資料細微性是支援值之間的差異) ; 每個樣本最多16位的16位最大位，每個樣本有8位的資料細微性，以及最少一個通道和兩個通道的最大值。 第一個配對的媒體類型會是您在該範圍內的預設 PCM 格式，可能是22千赫茲 (kHz) 16 位的身歷聲。 您的第二組是一項功能，顯示每秒最小和最大樣本的 44100;8位 (最小) 和16位 (每個樣本最多) 位，每個樣本的資料細微性為8位;以及最少一個通道和兩個通道。 媒體類型會是預設的 44 kHz 格式，可能是 44 kHz 16 位的身歷聲。

如果您支援非 PCM wave 格式，這個方法所傳回的媒體類型可顯示您支援的非 PCM 格式 (預設的取樣率、位元速率和通道) ，以及媒體類型所附的功能結構，可描述您所支援的其他範例速率、位元速率和通道。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[公開捕捉和壓縮格式](exposing-capture-and-compression-formats.md)
</dt> </dl>

 

 
