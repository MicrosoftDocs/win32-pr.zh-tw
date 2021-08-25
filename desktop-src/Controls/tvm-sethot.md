---
title: 'TVM_SETHOT 訊息 (Commctrl .h) '
description: 設定樹狀檢視控制項的熱專案。 您可以使用 TreeView SetHot 宏明確地傳送此訊息 \_ 。
ms.assetid: 5e7368f5-40ce-4e7b-bbe3-5fe0b17181a8
keywords:
- TVM_SETHOT 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TVM_SETHOT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87ca61fd0bd3e25f37229cd5cee54f9bbb59b3a5c7556ae745821a8dc4d595d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913948"
---
# <a name="tvm_sethot-message"></a>TVM \_ SETHOT 訊息

\[適用于內部用途;不建議在應用程式中使用。 未來的 Windows 版本可能不支援此訊息。\]

設定樹狀檢視控制項的熱專案。 您可以使用 [**TreeView \_ SetHot**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sethot) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

新熱專案的控制碼。 如果這個值為 **Null**，則樹狀檢視控制項將設定為沒有熱專案。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。

## <a name="security-considerations"></a>安全性考量

使用此訊息可能會危害程式的安全性。

## <a name="remarks"></a>備註

*熱專案* 是滑鼠停留在上方的專案。 這則訊息會讓專案看起來像是最忙碌的專案，即使滑鼠未停留在其上也一樣。

如果未設定 [**電視 \_ TRACKSELECT**](tree-view-control-window-styles.md) 樣式，則此訊息不會顯示任何效果。

如果成功，此訊息將會重新繪製熱專案。

如果 *lParam* 為 **Null** ，而且樹狀檢視控制項正在追蹤滑鼠，則會忽略此訊息。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TreeView \_ SetHot**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sethot)
</dt> </dl>

 

 





