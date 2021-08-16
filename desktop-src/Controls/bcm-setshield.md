---
title: 'BCM_SETSHIELD 訊息 (Commctrl .h) '
description: 設定指定之按鈕或命令連結的「提高許可權」狀態，以顯示提高許可權的圖示。 明確地傳送此訊息，或使用按鈕 \_ SetElevationRequiredState 宏。
ms.assetid: 2ce2a006-7136-415b-824b-46b282b100f4
keywords:
- BCM_SETSHIELD 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- BCM_SETSHIELD
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67ab7ab495e713d9f2c8d58c6723489f0099a7c2cba9df93d4f08870d521a0cb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921488"
---
# <a name="bcm_setshield-message"></a>BCM \_ SETSHIELD 訊息

設定指定之按鈕或命令連結的「提高許可權」狀態，以顯示提高許可權的圖示。 明確地傳送此訊息，或使用 [**按鈕 \_ SetElevationRequiredState**](/windows/desktop/api/Commctrl/nf-commctrl-button_setelevationrequiredstate) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

必須為零。

</dd> <dt>

*lParam* \[在\]
</dt> <dd>

**布林** 值，為 **TRUE** 表示繪製提升許可權的圖示，否則為 **FALSE** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回1，否則傳回錯誤碼。

## <a name="remarks"></a>備註

您必須將應用程式列入使用 comctl32.dll 第6版才能獲得這種功能。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





