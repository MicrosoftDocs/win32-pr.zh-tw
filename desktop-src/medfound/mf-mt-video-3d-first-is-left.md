---
description: 若為3D 影片格式，請指定左邊視圖的視圖。
ms.assetid: 4F33BF2D-EB32-46B6-B071-F9130D404201
title: 'MF_MT_VIDEO_3D_FIRST_IS_LEFT 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 027d91509d772a9200cdfc0ac64cce15514aa5a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104386289"
---
# <a name="mf_mt_video_3d_first_is_left-attribute"></a>MF \_ MT \_ VIDEO \_ 3d \_ FIRST \_ 是 \_ LEFT 屬性

若為3D 影片格式，請指定左邊視圖的視圖。

## <a name="data-type"></a>資料類型

**BOOL** 儲存為 **UINT32**

## <a name="remarks"></a>備註

針對3D 影片，每個影片範例都會包含兩個視圖，分別是指定的 *第一個視圖* 和 *第二* 個視圖。 在記憶體中，視圖的確切版面配置是由 [MF \_ MT \_ VIDEO \_ 3d \_ 格式](mf-mt-video-3d-format.md) 屬性所表示。



| 格式               | 第一個視圖              | 第二個視圖               |
|----------------------|-------------------------|---------------------------|
| 以並存方式封裝  | 緩衝區的左邊半部 | 緩衝區的上半部  |
| 由上到下壓縮 | 緩衝區的上半部  | 緩衝區的下半部 |
| Multiview            | 緩衝區索引0          | 緩衝區索引1            |
| 基底視圖            | 整個框架            | 不存在               |



 

依預設，第一個視圖是左方視圖，而第二個視圖是右視圖。 如果已交換左方和右邊的視圖，請將 \_ \_ \_ 媒體類型中的 MF MT 影片 \_ 第一個 \_ \_ 屬性設為 [FALSE]。

> [!Note]  
> 在 *基底視圖* 格式中 (**MFVideo3DSampleFormat \_ 基礎** 視圖) ，只會保留基底視圖，因此不適用此屬性。

 

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

 

 




