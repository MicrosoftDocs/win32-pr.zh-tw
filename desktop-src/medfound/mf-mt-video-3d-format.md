---
description: 針對影片媒體類型，指定3D 影片框架儲存在記憶體中的方式。
ms.assetid: 880DF017-5841-4C0A-82AF-F092DEF5406B
title: 'MF_MT_VIDEO_3D_FORMAT 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66f2b12f907edb2875b3b121607509288787c8e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979303"
---
# <a name="mf_mt_video_3d_format-attribute"></a>MF \_ MT \_ VIDEO \_ 3d \_ 格式屬性

針對影片媒體類型，指定3D 影片框架儲存在記憶體中的方式。

## <a name="data-type"></a>資料類型

**MFVideo3DFormat** 儲存為 **UINT32**

## <a name="remarks"></a>備註

這個屬性的值是 [**MFVideo3DFormat**](/windows/desktop/api/mfapi/ne-mfapi-mfvideo3dformat) 列舉的成員。 只有當 [MF \_ MT \_ VIDEO \_ 3d](mf-mt-video-3d.md) 屬性為 **TRUE** 時，才會套用此屬性。

未壓縮的3D 影片格式需要此屬性。 這對壓縮的3D 影片是選擇性的。 傳遞編碼框架的媒體來源可能可以根據檔案容器中的資訊來設定屬性。 否則，應該由解碼器的輸出媒體類型中的解碼器來設定屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                  |
| 最低支援的伺服器<br/> | Windows Server 2012 \[ desktop app \| UWP 應用程式\]<br/>                        |
| 標頭<br/>                   | <dl> <dt>Mfapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




