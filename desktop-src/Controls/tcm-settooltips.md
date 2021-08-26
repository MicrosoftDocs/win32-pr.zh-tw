---
title: 'TCM_SETTOOLTIPS 訊息 (Commctrl .h) '
description: 將工具提示控制項指派給索引標籤控制項。 您可以使用 TabCtrl SetToolTips 宏明確地傳送此訊息 \_ 。
ms.assetid: c1b173b1-9da6-441a-a2b6-3875e2c343f8
keywords:
- TCM_SETTOOLTIPS 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TCM_SETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8bfec3b7272ceae3dcbf1781e3bb17a988f2252b3c0a74822677bff6ea39209
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104688"
---
# <a name="tcm_settooltips-message"></a>TCM \_ SETTOOLTIPS 訊息

將工具提示控制項指派給索引標籤控制項。 您可以使用 [**TabCtrl \_ SetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_settooltips) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

工具提示控制項的控制碼。

</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

您可以使用 [**TCM \_ GETTOOLTIPS**](tcm-gettooltips.md) 訊息來取得與索引標籤控制項相關聯的工具提示控制項。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





