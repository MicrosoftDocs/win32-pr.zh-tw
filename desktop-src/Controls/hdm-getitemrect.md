---
title: 'HDM_GETITEMRECT 訊息 (Commctrl .h) '
description: 取得標題控制項中指定專案的周框。 您可以明確地傳送此訊息，或使用標頭 \_ GetItemRect 宏。
ms.assetid: b483ef97-3700-425b-8160-81c673850f68
keywords:
- HDM_GETITEMRECT message Windows 控制項
topic_type:
- apiref
api_name:
- HDM_GETITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4baec72bd914a9d2dad72556a5444c0059452cf3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465885"
---
# <a name="hdm_getitemrect-message"></a>HDM \_ GETITEMRECT 訊息

取得標題控制項中指定專案的周框。 您可以明確地傳送此訊息，或使用 [**標頭 \_ GetItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitemrect) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* \[在\]
</dt> <dd>

以零為基底的標頭控制項專案索引，為其取得周框矩形。

</dd> <dt>

*lParam* \[in、out\]
</dt> <dd>

[**矩形**](/windows/win32/api/windef/ns-windef-rect)的指標，此結構會接收周框的資訊。 訊息寄件者負責配置此結構。 在矩形結構中傳回的座標會以相對於標題控制項父系的方式表示。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回非零，否則傳回零。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





