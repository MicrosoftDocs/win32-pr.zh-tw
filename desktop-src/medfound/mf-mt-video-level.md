---
description: 指定影片媒體類型中的 MPEG-2 或 h.264 層級。 這是 MF \_ MT \_ MPEG2 \_ 層級的別名。
ms.assetid: 23786FC8-ACA4-4F6A-98BA-57A8C76BD4C6
title: 'MF_MT_VIDEO_LEVEL 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b40f1ebc6834373e00253f494e3fc76c20c343af17d754c7c4fe642b802d16ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012768"
---
# <a name="mf_mt_video_level-attribute"></a>MF \_ MT \_ 影片 \_ 層級屬性

指定影片媒體類型中的 MPEG-2 或 h.264 層級。 這是 [MF \_ MT \_ MPEG2 \_ 層級](mf-mt-mpeg2-level-attribute.md)的別名。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="remarks"></a>備註

**H.264 編碼器：**

擴充支援的層級，以包含 [**eAVEncH264VLevel5 \_ 2**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vlevel)。

預設值：建議的預設值是選取符合影片編碼設定的最小層級（包括解析度、畫面播放速率等）。

建議的預設值：選取符合影片編碼設定的最小層級，包括解析度、畫面播放速率等等。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1 \[僅限桌面應用程式\]<br/>                                       |
| 最低支援的伺服器<br/> | Windows Server 2012\[僅限 R2 desktop 應用程式\]<br/>                            |
| 標頭<br/>                   | <dl> <dt>Mfapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




