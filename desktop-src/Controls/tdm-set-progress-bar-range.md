---
title: 'TDM_SET_PROGRESS_BAR_RANGE 訊息 (Commctrl .h) '
description: 在工作對話方塊中設定進度列的最小值和最大值。
ms.assetid: ca8b48bc-cf56-4678-bb3d-7c730a96d98c
keywords:
- TDM_SET_PROGRESS_BAR_RANGE 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TDM_SET_PROGRESS_BAR_RANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54d94da64bd01b17addeb8f65def177e7e7e5d7daccbafb1629d1158f8c6636d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119875908"
---
# <a name="tdm_set_progress_bar_range-message"></a>TDM \_ 設定 \_ 進度 \_ 列 \_ 範圍訊息

在工作對話方塊中設定進度列的最小值和最大值。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* \[在\]
</dt> <dd>

必須為零。

</dd> <dt>

*lParam* \[在\]
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))會指定最小值。 根據預設，最小值為零。 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定最大值。 根據預設，最大值為100。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回先前的最小值和最大值，否則傳回零。 [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))包含最小值，而 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))包含最大值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

