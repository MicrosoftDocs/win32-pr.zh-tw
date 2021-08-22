---
title: 'DWM_TNP 常數 (Dwmapi.dll) '
description: DWM 縮圖屬性結構所使用的旗標 \_ \_ ，用來指出其中一個成員包含有效的資訊。
ms.assetid: 8eee1baf-e24e-40af-92ab-a7acae267ecc
topic_type:
- apiref
api_name:
- DWM_TNP_RECTDESTINATION
- DWM_TNP_RECTSOURCE
- DWM_TNP_OPACITY
- DWM_TNP_VISIBLE
- DWM_TNP_SOURCECLIENTAREAONLY
api_location:
- Dwmapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ee82f8e0384c5523b8656c0ecc6cc40bad959c2c9ad6fa1c7b19486d73b00db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985240"
---
# <a name="dwm_tnp-constants"></a>DWM \_ TNP 常數

[**DWM \_ 縮圖 \_ 屬性**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_thumbnail_properties)結構所使用的旗標，用來指出其中一個成員包含有效的資訊。

<dl> <dt>

<span id="DWM_TNP_RECTDESTINATION"></span><span id="dwm_tnp_rectdestination"></span>**DWM \_ TNP \_ RECTDESTINATION**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



已指定 **rcDestination** 成員的值。


</dt> </dl> </dd> <dt>

<span id="DWM_TNP_RECTSOURCE"></span><span id="dwm_tnp_rectsource"></span>**DWM \_ TNP \_ RECTSOURCE**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



已指定 **rcSource** 成員的值。


</dt> </dl> </dd> <dt>

<span id="DWM_TNP_OPACITY"></span><span id="dwm_tnp_opacity"></span>**DWM \_ TNP \_ 不透明度**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



已指定 **不透明度** 成員的值。


</dt> </dl> </dd> <dt>

<span id="DWM_TNP_VISIBLE"></span><span id="dwm_tnp_visible"></span>**DWM \_ TNP \_ 可見**
</dt> <dd> <dl> <dt>

0x00000008
</dt> <dt>



已指定 **fVisible** 成員的值。


</dt> </dl> </dd> <dt>

<span id="DWM_TNP_SOURCECLIENTAREAONLY"></span><span id="dwm_tnp_sourceclientareaonly"></span>**DWM \_ TNP \_ SOURCECLIENTAREAONLY**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



已指定 **fSourceClientAreaOnly** 成員的值。


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                      |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Dwmapi.dll。h</dt> </dl> |



 

 





