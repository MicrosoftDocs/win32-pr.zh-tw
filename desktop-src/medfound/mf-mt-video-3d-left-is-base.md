---
description: 若為3D 影片格式，請指定哪個 view 是基底視圖。
ms.assetid: 11555BA0-D9BE-4239-A857-C9EEE86A8520
title: 'MF_MT_VIDEO_3D_LEFT_IS_BASE 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb03bc12d32b96abc52999ef6a3b21580c4ac1c59125a076b9eb1d620e0bd362
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118741590"
---
# <a name="mf_mt_video_3d_left_is_base-attribute"></a>MF \_ MT \_ VIDEO \_ 3d \_ 左邊 \_ 是 \_ 基底屬性

若為3D 影片格式，請指定哪個 view 是基底視圖。

## <a name="data-type"></a>資料類型

**BOOL** 儲存為 **UINT32**

## <a name="remarks"></a>備註

根據預設，3D 影片順序中的左視圖是基底視圖。 如果右視圖是基底視圖，請將此屬性設定為 **FALSE**。

若要將 stereoscopic video 轉換成2D，請保留基底視圖，並捨棄另一個視圖。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[桌面應用程式 \| UWP 應用程式\]<br/>                                  |
| 最低支援的伺服器<br/> | Windows Server 2012 \[桌面應用程式 \| UWP 應用程式\]<br/>                        |
| 標頭<br/>                   | <dl> <dt>Mfapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




