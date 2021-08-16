---
description: 在 IMFTransform 上，指定硬體編碼器所支援的最大巨大區塊處理速率（每秒巨大區塊）。
ms.assetid: 1AA41DE3-C37C-41BA-9549-5F12373DDB3B
title: 'MF_VIDEO_MAX_MB_PER_SEC 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c76e6a44a6e0993f9cf6410a0092708da767f92815fc98020dd2f4d88359370
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118739236"
---
# <a name="mf_video_max_mb_per_sec-attribute"></a>MF \_ VIDEO \_ 最 \_ 大 \_ 每 \_ 秒 MB 數屬性

在 [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)上，指定硬體編碼器所支援的最大巨大區塊處理速率（每秒巨大區塊）。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="remarks"></a>備註

這是唯讀的屬性。

**H.264/AVC 編碼器：**

這個屬性會受到下列屬性的影響：

-   [MF \_MT \_ 影片 \_ 層級](mf-mt-video-level.md) (是 [MF \_ MT \_ MPEG2 \_ 層級](mf-mt-mpeg2-level-attribute.md) 的別名) 
-   [CODECAPI \_ AVEncCommonQualityVsSpeed](../directshow/avenccommonqualityvsspeed-property.md)
-   [CODECAPI \_ AVEncMPVDefaultBPictureCount](../directshow/avencmpvdefaultbpicturecount-property.md)

如果有 [MF \_ MT \_ 影片 \_ 層級](mf-mt-video-level.md) 屬性，編碼器應該會傳回指定層級所支援的最高位元速率和解析度的處理速率。 如果 \_ \_ 不存在 MF MT 影片 \_ 層級屬性，則應使用預設層級4。

如果已設定 [CODECAPI \_ AVEncCommonQualityVsSpeed](../directshow/avenccommonqualityvsspeed-property.md) ICodecAPI 屬性，編碼器應該會傳回與此屬性所設定之值相對應的處理速率。 如果 CODECAPI \_ AVEncCommonQualityVsSpeed 屬性不存在，則應該使用預設值0，這應該是最快的處理模式。

如果 [CODECAPI \_ AVEncMPVDefaultBPictureCount](../directshow/avencmpvdefaultbpicturecount-property.md) ICodecAPI 屬性已設定為有效且支援的值，則編碼器應該會傳回與此屬性所設定之值相對應的處理速率。 如果 CODECAPI \_ AVEncMPVDefaultBPictureCount 屬性不是 presen，則應該使用預設值 0 B 的框架。

應用程式只能使用較低的28位。 較高的4bits 會保留供日後使用。 應用程式應該忽略上面的4位，而且 MFTs 應該將前4位設定為0。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1 \[桌面應用程式 \| UWP 應用程式\]<br/>                                |
| 最低支援的伺服器<br/> | Windows Server 2012R2 \[ desktop apps \| UWP 應用程式\]<br/>                     |
| 標頭<br/>                   | <dl> <dt>Mfapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
