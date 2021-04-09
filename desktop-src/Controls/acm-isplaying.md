---
title: 'ACM_ISPLAYING 訊息 (Commctrl .h) '
description: 檢查 Audio-Video 交錯 (AVI) 剪輯是否現正播放。 您可以明確地傳送此訊息，或使用動畫 \_ >isplaying 宏。
ms.assetid: ebb0c92a-99d2-49c1-9de1-8bdbd032be3a
keywords:
- ACM_ISPLAYING message Windows 控制項
topic_type:
- apiref
api_name:
- ACM_ISPLAYING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f663872ce02b9520e3e033cb5bc5a3da12bb3c3c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024805"
---
# <a name="acm_isplaying-message"></a>\_>isplaying 訊息

檢查 Audio-Video 交錯 (AVI) 剪輯是否現正播放。 您可以明確地傳送此訊息，或使用 [**動畫 \_ >isplaying**](/windows/desktop/api/Commctrl/nf-commctrl-animate_isplaying) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回非零，否則傳回零。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





