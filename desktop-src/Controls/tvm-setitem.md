---
title: 'TVM_SETITEM 訊息 (Commctrl .h) '
description: TVM \_ SETITEM 訊息會設定部分或全部樹狀檢視專案的屬性。 您可以使用 TreeView SetItem 宏明確地傳送此訊息 \_ 。
ms.assetid: 28d288bf-a557-4fce-870c-ffa368ece5a9
keywords:
- TVM_SETITEM message Windows 控制項
topic_type:
- apiref
api_name:
- TVM_SETITEM
- TVM_SETITEMA
- TVM_SETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95750af3aa43a25f0ff4eae5533df5d9aef23537
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465464"
---
# <a name="tvm_setitem-message"></a>TVM \_ SETITEM 訊息

**TVM \_ SETITEM** 訊息會設定部分或全部樹狀檢視專案的屬性。 您可以使用 [**TreeView \_ SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitem) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

[**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema)結構的指標，其中包含新的專案屬性。 使用 [4.71 版](common-control-versions.md) 和更新版本時，您可以改用 [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) 結構。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

[**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema)或 [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa)結構的 **hItem** 成員會識別專案，而 **遮罩** 成員會指定要設定的屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **TVM \_SETITEMW** (Unicode) 和 **TVM \_ SETITEMA** (ANSI) <br/>                   |



 

 





