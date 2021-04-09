---
title: 'LVM_SETITEM 訊息 (Commctrl .h) '
description: 設定部分或全部清單視圖專案的屬性。 您也可以傳送 LVM \_ SETITEM 來設定子內容的文字。 您可以明確地傳送此訊息，或使用 ListView \_ SetItem 宏來傳送。
ms.assetid: f1189b5d-bce7-4569-b4b9-bd750d7ef505
keywords:
- LVM_SETITEM message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_SETITEM
- LVM_SETITEMA
- LVM_SETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 623339c3d1ecc7a74cf20b5e52fb621666391bd5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024859"
---
# <a name="lvm_setitem-message"></a>LVM \_ SETITEM 訊息

設定部分或全部清單視圖專案的屬性。 您也可以傳送 LVM \_ SETITEM 來設定子內容的文字。 您可以明確地傳送此訊息，或使用 [**ListView \_ SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitem) 宏來傳送。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

[**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema)結構的指標，其中包含新的專案屬性。 **IItem** 和 **iSubItem** 成員會識別專案或子專案，而 **遮罩** 成員會指定要設定的屬性。 如果 **遮罩** 成員指定 LVIF \_ 文字值，則 **pszText** 成員是以 null 結束之字串的位址，而且會忽略 **cchTextMax** 成員。 如果 **遮罩** 成員指定 LVIF \_ 狀態值， **stateMask** 成員就會指定要變更的專案狀態，而 **狀態** 成員會包含這些狀態的值。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

若要設定清單視圖專案的屬性，請將 [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema)結構的 **iItem** 成員設定為專案的索引，並將 **iSubItem** 成員設定為零。 針對某個專案，您可以設定 **LVITEM** 結構的 **state**、 **pszText**、 **iImage** 和 **lParam** 成員。

若要設定子集合的文字，請設定 **iItem** 和 **iSubItem** 成員來指出特定的子工作，並使用 **pszText** 成員來指定文字。 或者，您也可以使用 [**ListView \_ SetItemText**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemtext) 宏來設定子內容的文字。 您無法設定子屬性的 **狀態** 或 **lParam** 成員，因為子集合沒有這些屬性。 在4.70 版和更新版本中，您可以設定子集合的 **iImage** 成員。 如果清單視圖控制項具有 [**lvs) \_ EX \_ SUBITEMIMAGES**](extended-list-view-styles.md) 擴充樣式，則會顯示子元件映射。 先前的版本會忽略子工作映射。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **LVM \_SETITEMW** (Unicode) 和 **LVM \_ SETITEMA** (ANSI) <br/>                   |



 

 





