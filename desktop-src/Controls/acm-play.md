---
title: 'ACM_PLAY 訊息 (Commctrl .h) '
description: 在動畫控制項中播放 AVI 剪輯。 當執行緒繼續執行時，控制項會在背景中播放剪輯。 您可以明確地傳送此訊息，或使用動畫 \_ 播放宏。
ms.assetid: 738b7305-bb77-441d-a198-17daf3b76039
keywords:
- ACM_PLAY message Windows 控制項
topic_type:
- apiref
api_name:
- ACM_PLAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e501f3718e1b8172e2b7b16566f992c26346b7f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464669"
---
# <a name="acm_play-message"></a>未通過的 \_ 播放訊息

在動畫控制項中播放 AVI 剪輯。 當執行緒繼續執行時，控制項會在背景中播放剪輯。 您可以明確地傳送此訊息，或使用 [**動畫 \_ 播放**](/windows/desktop/api/Commctrl/nf-commctrl-animate_play) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

指定重播 AVI 剪輯次數的 **UINT** 。 -1 值表示無限期地重新播放剪輯。

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))是開始播放之框架的以零為起始的索引。 值必須小於65536。 值為零表示以 AVI 剪輯中的第一個框架為開頭。

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))是播放結束之框架的以零為基底的索引。 值必須小於65536。 值-1 表示以 AVI 剪輯中的最後一個框架結尾。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回非零，否則傳回零。

## <a name="remarks"></a>備註

您可以使用 [**動畫 \_ 搜尋**](/windows/desktop/api/Commctrl/nf-commctrl-animate_seek) 來指示動畫控制項，以顯示 AVI 剪輯的特定框架。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

