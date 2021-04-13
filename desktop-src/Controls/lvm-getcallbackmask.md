---
title: 'LVM_GETCALLBACKMASK 訊息 (Commctrl .h) '
description: 取得清單視圖控制項的回呼遮罩。 您可以明確地傳送此訊息，或使用 ListView \_ GetCallbackMask 宏來傳送。
ms.assetid: fb05593d-14b9-4e53-acb3-d5ac61e517ec
keywords:
- LVM_GETCALLBACKMASK message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETCALLBACKMASK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68438b748f5260bb7cc6e43702442aa4cbe3a84e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464281"
---
# <a name="lvm_getcallbackmask-message"></a>LVM \_ GETCALLBACKMASK 訊息

取得清單視圖控制項的回呼遮罩。 您可以明確地傳送此訊息，或使用 [**ListView \_ GetCallbackMask**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcallbackmask) 宏來傳送。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回回呼遮罩。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





