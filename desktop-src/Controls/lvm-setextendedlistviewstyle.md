---
title: 'LVM_SETEXTENDEDLISTVIEWSTYLE 訊息 (Commctrl .h) '
description: 在清單視圖控制項中設定延伸樣式。 您可以明確地傳送此訊息，或使用 ListView \_ SetExtendedListViewStyle 或 listview \_ SetExtendedListViewStyleEx 宏。
ms.assetid: eb3f47ed-484a-49a8-94b0-e50ee081bd69
keywords:
- LVM_SETEXTENDEDLISTVIEWSTYLE message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_SETEXTENDEDLISTVIEWSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7d36869283d863bef7b31187a002125c9cd79bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103933921"
---
# <a name="lvm_setextendedlistviewstyle-message"></a>LVM \_ SETEXTENDEDLISTVIEWSTYLE 訊息

在清單視圖控制項中設定延伸樣式。 您可以明確地傳送此訊息，或使用 [**listview \_ SetExtendedListViewStyle**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyle) 或 [**listview \_ SetExtendedListViewStyleEx**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyleex) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

**DWORD** 值，指定要對 *lParam* 中的哪些樣式造成影響。 這個參數可以是 [**延伸 List-View 樣式**](extended-list-view-styles.md)的組合。 只有 *wParam* 中的擴充樣式會變更。 所有其他樣式都會維持不變。 如果此參數為零，則 *lParam* 中的所有樣式都會受到影響。

</dd> <dt>

*lParam* 
</dt> <dd>

**DWORD** 值，指定要設定的擴充清單視圖控制項樣式。 這個參數可以是 [**延伸 List-View 樣式**](extended-list-view-styles.md)的組合。 未設定，但在 *wParam* 中指定的樣式會被移除。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回包含先前的擴充清單視圖控制項樣式的 **DWORD** 值。

## <a name="remarks"></a>備註

*WParam* 參數可讓您修改一或多個擴充樣式，而不需要先取出現有的樣式。 例如，如果您傳遞 [**lvs) 的 \_ \_ FULLROWSELECT**](extended-list-view-styles.md) for *wParam* 和0（ *lParam*），將會清除 **lvs) \_ EX \_ FULLROWSELECT** 樣式，但所有其他樣式都會保持不變。

基於回溯相容性的理由， [**ListView \_ SetExtendedListViewStyle**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyle) 宏尚未更新為使用 *wParam*。 若要使用 *wParam* 值，請使用 [**ListView \_ SetExtendedListViewStyleEx**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyleex) 宏。

當您使用此訊息來設定 [**lvs) \_ EX \_ 核取方塊**](extended-list-view-styles.md) 樣式時，將會捨棄任何先前設定的狀態影像索引。 所有核取方塊都會初始化為未核取的狀態。 狀態影像索引是包含在 [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema)結構的 **state** 成員中的位12到15。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





