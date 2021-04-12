---
title: 'LVM_DELETEALLITEMS 訊息 (Commctrl .h) '
description: 移除清單視圖控制項中的所有專案。 您可以明確地傳送此訊息，或使用 ListView \_ DeleteAllItems 宏來傳送。
ms.assetid: 816bf565-79e9-4f5d-b5b4-5cdecce8a61c
keywords:
- LVM_DELETEALLITEMS message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_DELETEALLITEMS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e92344e3cccf7578b8953206a9550022f6c6095
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464297"
---
# <a name="lvm_deleteallitems-message"></a>LVM \_ DELETEALLITEMS 訊息

移除清單視圖控制項中的所有專案。 您可以明確地傳送此訊息，或使用 [**ListView \_ DeleteAllItems**](/windows/desktop/api/Commctrl/nf-commctrl-listview_deleteallitems) 宏來傳送。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

當清單視圖控制項收到 **LVM \_ DELETEALLITEMS** 訊息時，它會將 [**LVN \_ DELETEALLITEMS**](lvn-deleteallitems.md) 通知程式碼傳送至其父視窗。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





