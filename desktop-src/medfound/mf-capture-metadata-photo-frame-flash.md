---
description: 指出是否已針對捕捉的框架觸發快閃。
ms.assetid: CF900CB4-8967-40F3-B60C-867192A641E9
title: 'MF_CAPTURE_METADATA_PHOTO_FRAME_FLASH 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a885786674c524b382912100171502dba78a010b2169738233b5aaad88ed701a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973917"
---
# <a name="mf_capture_metadata_photo_frame_flash-attribute"></a>MF \_ CAPTURE \_ METADATA \_ PHOTO \_ FRAME \_ FLASH 屬性

指出是否已針對捕捉的框架觸發快閃。

## <a name="data-type"></a>資料類型

**UINT32**



| 值                                                                               | 意義                                                                                                                                               |
|-------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl>        | 未在此框架上觸發 flash。<br/>                                                                                                   |
| <dl> <dt>非零</dt> </dl> | 此框架上已觸發 flash。<br/>                                                                                                       |
| <dl> <dt>1</dt> </dl>        | 保留<br/> 請勿明確檢查值1。 應用程式應該只檢查！ = 0，以指出是否已觸發 flash。<br/> |



 

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

 

 




