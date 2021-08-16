---
title: 'TDM_SET_BUTTON_ELE加值稅ION_REQUIRED_STATE 訊息 (Commctrl .h) '
description: 指定指定的工作對話方塊按鈕或命令連結是否應該有 (UAC) 盾牌圖示的使用者帳戶控制;亦即，按鈕叫用的動作是否需要提高許可權。
ms.assetid: c4321fdb-3ea9-49bf-b53d-eb73d5b11084
keywords:
- TDM_SET_BUTTON_ELE加值稅ION_REQUIRED_STATE 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TDM_SET_BUTTON_ELEVATION_REQUIRED_STATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c69998da085a74b144179a0a4244c787cd3a871d63eca1e5df9c4e555b1a7e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104618"
---
# <a name="tdm_set_button_elevation_required_state-message"></a>TDM \_ 設定 \_ 按鈕提高 \_ 許可權的 \_ 必要 \_ 狀態訊息

指定指定的工作對話方塊按鈕或命令連結是否應該有 (UAC) 盾牌圖示的使用者帳戶控制;亦即，按鈕叫用的動作是否需要提高許可權。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* \[在\]
</dt> <dd>

要更新之推播按鈕或命令連結的識別碼。

</dd> <dt>

*lParam* \[在\]
</dt> <dd>

設定為0，以指定按鈕叫用的動作不需要提高許可權。 設定為非零，以指定動作需要提高許可權。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值會被忽略。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





