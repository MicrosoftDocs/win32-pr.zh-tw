---
title: 'TB_SETBUTTONWIDTH 訊息 (Commctrl .h) '
description: 設定工具列控制項中的最小和最大按鈕寬度。
ms.assetid: 3311216a-e0b2-48bb-bad7-0a04185573cf
keywords:
- TB_SETBUTTONWIDTH message Windows 控制項
topic_type:
- apiref
api_name:
- TB_SETBUTTONWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e105770d72e90108b9c31311f77599520cecea8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103758"
---
# <a name="tb_setbuttonwidth-message"></a>TB \_ SETBUTTONWIDTH 訊息

設定工具列控制項中的最小和最大按鈕寬度。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))會指定最小按鈕寬度（以圖元為單位）。 工具列按鈕絕不會比這個值窄。

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定最大按鈕寬度（以圖元為單位）。 如果按鈕文字太寬，控制項會以省略號點顯示。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回非零，否則傳回零。

## <a name="remarks"></a>備註

使用 [ **TB] \_ SETBUTTONWIDTH** 可設定按鈕在新增之前允許的最大寬度和最小值。 使用 [**TB \_ SETBUTTONSIZE**](tb-setbuttonsize.md) 來設定按鈕的實際大小。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

