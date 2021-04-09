---
title: 'RB_SHOWBAND 訊息 (Commctrl .h) '
description: 顯示或隱藏 Rebar 控制項中的指定頻。
ms.assetid: 18097aca-e1b4-4359-9d08-4e62406f3f7f
keywords:
- RB_SHOWBAND message Windows 控制項
topic_type:
- apiref
api_name:
- RB_SHOWBAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e27c9cedeb42e7eeed9432af9c2a040ac4991810
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106248"
---
# <a name="rb_showband-message"></a>RB \_ SHOWBAND 訊息

顯示或隱藏 Rebar 控制項中的指定頻。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

Rebar 控制項中的寬線索引（以零為基底）。

</dd> <dt>

*lParam* 
</dt> <dd>

**布林** 值，指出是否應該顯示或隱藏帶狀。 如果此值為非零值，則會顯示此波段。 否則，將會隱藏此波段。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回非零，否則傳回零。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





