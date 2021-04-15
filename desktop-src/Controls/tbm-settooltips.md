---
title: 'TBM_SETTOOLTIPS 訊息 (Commctrl .h) '
description: 將工具提示控制項指派給 [對等] 控制項。
ms.assetid: 9bba1084-d04e-4631-a5cc-408849a14eb1
keywords:
- TBM_SETTOOLTIPS message Windows 控制項
topic_type:
- apiref
api_name:
- TBM_SETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8d60c7e108db926b85e7d9e1167f33c1ed807a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464769"
---
# <a name="tbm_settooltips-message"></a>TBM \_ SETTOOLTIPS 訊息

將工具提示控制項指派給 [對等] 控制項。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

現有工具提示控制項的控制碼。

</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

未使用此訊息的傳回值。

## <a name="remarks"></a>備註

當使用 [ [**tb] \_ 工具提示**](trackbar-control-styles.md) 樣式建立的 [顯示] 控制項時，它會建立一個預設的工具提示控制項，顯示在滑杆旁邊，顯示滑杆的目前位置。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





