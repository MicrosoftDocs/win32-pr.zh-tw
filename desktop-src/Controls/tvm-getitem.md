---
title: 'TVM_GETITEM 訊息 (Commctrl .h) '
description: 抓取部分或所有樹狀檢視專案的屬性。 您可以使用 TreeView GetItem 宏明確地傳送此訊息 \_ 。
ms.assetid: e26ec000-967d-46de-8f71-6ebc36fefe5e
keywords:
- TVM_GETITEM message Windows 控制項
topic_type:
- apiref
api_name:
- TVM_GETITEM
- TVM_GETITEMA
- TVM_GETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dff96f4721a3c50eda54792b2b1c003cd808bf11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106572"
---
# <a name="tvm_getitem-message"></a>TVM \_ GETITEM 訊息

抓取部分或所有樹狀檢視專案的屬性。 您可以使用 [**TreeView \_ GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitem) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

[**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema)結構的指標，此結構會指定要取出並接收專案相關資訊的資訊。 使用 [4.71 版](common-control-versions.md) 和更新版本時，您可以改用 [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) 結構。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

傳送訊息時， [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema)或 [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa)結構的 **hItem** 成員會識別要取得相關資訊的專案，而 **遮罩** 成員會指定要抓取的屬性。

如果在 \_ [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema)或 [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa)結構的 **mask** 成員中設定 TVIF 文字旗標， **pszText** 成員必須指向有效的緩衝區，而且 **cchTextMax** 成員必須設定為該緩衝區中的字元數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **TVM \_GETITEMW** (Unicode) 和 **TVM \_ GETITEMA** (ANSI) <br/>                   |



 

 





