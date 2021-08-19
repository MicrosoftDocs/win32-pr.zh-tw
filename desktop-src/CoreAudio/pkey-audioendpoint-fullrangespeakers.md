---
description: PKEY \_ AudioEndpoint \_ FullRangeSpeakers 屬性會為連線到音訊端點裝置的全範圍喇叭指定通道設定遮罩。
ms.assetid: c0a54b3d-84dc-4771-8891-167ce00e2218
title: 'PKEY_AudioEndpoint_FullRangeSpeakers (Mmdeviceapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad27e5623189ce3ba78707377837493c1ea8dccb248d02ddd3d8e2c64570bed6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118406444"
---
# <a name="pkey_audioendpoint_fullrangespeakers"></a>PKEY \_ AudioEndpoint \_ FullRangeSpeakers

**PKEY \_ AudioEndpoint \_ FullRangeSpeakers** 屬性會為連線到音訊端點裝置的全範圍喇叭指定通道設定遮罩。 遮罩表示全範圍喇叭的實體設定，並指定將通道指派給這些喇叭。

**PROPVARIANT** 結構的 **vt** 成員會設定為 vt \_ UI4。

**PROPVARIANT** 結構的 **uintVal** 成員包含轉換成 **UINT** 型別的通道設定遮罩。

全範圍的喇叭可以從低音到高音的全範圍播放音效。 通常，較大的喇叭是完整範圍，但較小的喇叭的播放低音音效會大幅降低。 在 Windows Vista 中，音訊引擎會使用此屬性來管理音訊輸出串流中音訊端點裝置所播放的低音等級。

這個屬性的通道設定遮罩與 [**PKEY \_ AudioEndpoint \_ PhysicalSpeakers**](pkey-audioendpoint-physicalspeakers.md) 屬性的通道設定遮罩具有相同的格式。 如需通道設定遮罩的詳細資訊，請參閱下列各項：

-   \_ \_ Windows DDK 檔中 KSPROPERTY 音訊通道設定屬性的描述 \_ 。
-   標題為「家用劇院喇叭設定的音訊驅動程式支援」的白皮書，位於 Windows 網站的[音訊裝置技術](https://www.microsoft.com/whdc/device/audio/default.mspx)上。

系統會 \_ 從使用者取得 PKEY AudioEndpoint FullRangeSpeakers 屬性的通道設定遮罩 \_ 。 使用者透過 [Windows 多媒體] 控制台輸入此資訊，Mmsys.cpl。 如需 Mmsys.cpl 的詳細資訊，請參閱 Windows DDK 檔。

\_音訊端點裝置的 PKEY AudioEndpoint FullRangeSpeakers 屬性的通道設定遮罩 \_ 是 \_ 相同裝置之 PKEY AudioEndpoint PhysicalSpeakers 屬性的通道設定遮罩的子集 \_ 。

例如，如果音訊端點裝置會驅動一組5.1 環繞音效的喇叭，則 [PKEY AudioEndpoint PhysicalSpeakers] 屬性的通道設定遮罩 \_ \_ 就是 KSAUDIO \_ 喇叭 \_ 5POINT1。 此遮罩表示前端、前端、前端、側邊和側邊右喇叭的存在，以及喇叭。 如果左上角和右上方的喇叭大到足以產生低音音效，但較小的前端和側喇叭不是，則 PKEY AudioEndpoint FullRangeSpeakers 內容的通道設定遮罩 \_ \_ 是 KSAUDIO \_ \_ 的喇叭，它只會指出左右喇叭。 通道設定遮罩 KSAUDIO \_ 喇叭 \_ 5POINT1 和 KSAUDIO \_ 喇叭 \_ 身歷聲定義于標頭檔 Ksmedia .h 中。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>Mmdeviceapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**音訊端點屬性**](audio-endpoint-properties.md)
</dt> <dt>

[核心音訊屬性](core-audio-properties.md)
</dt> <dt>

[**PKEY \_ AudioEndpoint \_ PhysicalSpeakers 屬性**](pkey-audioendpoint-physicalspeakers.md)
</dt> </dl>

 

 




