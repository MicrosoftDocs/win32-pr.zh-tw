---
title: 'LVM_SETTOOLTIPS 訊息 (Commctrl .h) '
description: 設定 [清單視圖] 控制項將用來顯示工具提示的工具提示控制項。 您可以明確地傳送此訊息，或使用 ListView \_ SetToolTips 宏。
ms.assetid: 5b4335a4-e9f0-4b13-b00b-516af3b60bf1
keywords:
- LVM_SETTOOLTIPS message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_SETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ff749c24a35cf73de2d75b8a3b516197b57aac4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464880"
---
# <a name="lvm_settooltips-message"></a>LVM \_ SETTOOLTIPS 訊息

設定 [清單視圖] 控制項將用來顯示工具提示的工具提示控制項。 您可以明確地傳送此訊息，或使用 [**ListView \_ SetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settooltips) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>要設定之工具提示控制項的控制碼。</dd> <dt>

*lParam* 
</dt> <dd>

必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

將控制碼傳回至先前的工具提示控制項。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**LVM \_ GETTOOLTIPS**](lvm-gettooltips.md)
</dt> </dl>

 

 





