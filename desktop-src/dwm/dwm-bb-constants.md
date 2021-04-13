---
title: Dwmapi.dll) 常數的 DWM 模糊 (
description: DWM \_ BLURBEHIND 結構用來指出其中一個成員包含有效資訊的旗標。
ms.assetid: d6dd552c-1f3b-4f16-8705-f5016ed55d9e
topic_type:
- apiref
api_name:
- DWM_BB_ENABLE
- DWM_BB_BLURREGION
- DWM_BB_TRANSITIONONMAXIMIZED
api_location:
- Dwmapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbe08e0315d4c4b906cdb897ac7ad5dd34d50fbf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508811"
---
# <a name="dwm-blur-behind-constants"></a>常數模糊背後常數

[**DWM \_ BLURBEHIND**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind)結構用來指出其中一個成員包含有效資訊的旗標。

<dl> <dt>

<span id="DWM_BB_ENABLE"></span><span id="dwm_bb_enable"></span>**DWM \_ BB \_ 啟用**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



已指定 **fEnable** 成員的值。


</dt> </dl> </dd> <dt>

<span id="DWM_BB_BLURREGION"></span><span id="dwm_bb_blurregion"></span>**DWM \_ BB \_ BLURREGION**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



已指定 **hRgnBlur** 成員的值。


</dt> </dl> </dd> <dt>

<span id="DWM_BB_TRANSITIONONMAXIMIZED"></span><span id="dwm_bb_transitiononmaximized"></span>**DWM \_ BB \_ TRANSITIONONMAXIMIZED**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



已指定 **fTransitionOnMaximized** 成員的值。


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                      |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Dwmapi.dll。h</dt> </dl> |



 

 





