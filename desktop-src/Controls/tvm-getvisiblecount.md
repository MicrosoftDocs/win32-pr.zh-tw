---
title: 'TVM_GETVISIBLECOUNT 訊息 (Commctrl .h) '
description: 取得可在樹狀檢視控制項的用戶端視窗中完整顯示的專案數。 您可以使用 TreeView GetVisibleCount 宏明確地傳送此訊息 \_ 。
ms.assetid: c3519543-3fb2-4ecf-ac01-905d0946cb1b
keywords:
- TVM_GETVISIBLECOUNT message Windows 控制項
topic_type:
- apiref
api_name:
- TVM_GETVISIBLECOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1927d21741b109c5f00aa964b058dc0c34732529
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934087"
---
# <a name="tvm_getvisiblecount-message"></a>TVM \_ GETVISIBLECOUNT 訊息

取得可在樹狀檢視控制項的用戶端視窗中完整顯示的專案數。 您可以使用 [**TreeView \_ GetVisibleCount**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getvisiblecount) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回樹狀檢視控制項的用戶端視窗中可完全顯示的專案數。

## <a name="remarks"></a>備註

可以完全可見的專案數可能會大於控制項中的專案數。 控制項會將用戶端視窗的高度除以專案的高度，以計算此值。

請注意，傳回值是可 *完全* 可見的專案數。 如果您可以看到所有的20個專案和一個以上的專案，則傳回值為20。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





