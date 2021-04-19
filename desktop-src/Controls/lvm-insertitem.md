---
title: 'LVM_INSERTITEM 訊息 (Commctrl .h) '
description: 在清單視圖控制項中插入新專案。 您可以明確地傳送此訊息，或使用 ListView \_ InsertItem 宏來傳送。
ms.assetid: ac283e81-5b9f-4a90-acdb-fd7813c9cb84
keywords:
- LVM_INSERTITEM message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_INSERTITEM
- LVM_INSERTITEMA
- LVM_INSERTITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 467c6b595e307dc16f87e40da858ff8b120fb3f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969809"
---
# <a name="lvm_insertitem-message"></a>LVM \_ INSERTITEM 訊息

在清單視圖控制項中插入新專案。 您可以明確地傳送此訊息，或使用 [**ListView \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem) 宏來傳送。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

[**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema)結構的指標，指定清單視圖專案的屬性。 您可以使用 **iItem** 成員來指定以零為基底的索引，這是應該插入新專案的位置。 如果這個值大於 listview 目前所包含的專案數目，新的專案會附加至清單結尾並指派正確的索引。 檢查訊息的傳回值，以判斷指派給專案的實際索引。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回新專案的索引，否則傳回-1。

## <a name="remarks"></a>備註

您無法使用 [**ListView \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem) 或 **LVM \_ InsertItem** 插入子。 [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema)結構的 **iSubItem** 成員必須為零。 請參閱 [**LVM \_ SETITEM**](lvm-setitem.md) ，以取得設定子內容的相關資訊。

如果清單視圖控制項已設定 [**lvs) \_ EX \_ 核取方塊**](extended-list-view-styles.md)樣式，則會忽略任何在 [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema)結構之 **狀態** 成員的位12到15中放置的值。 使用這個樣式集加入專案時，一律會將它設定為未核取的狀態。

如果清單視圖控制項有 [ [**lvs) \_ SORTASCENDING**](list-view-window-styles.md) ] 或 [ [**lvs) \_ SORTDESCENDING**](list-view-window-styles.md) ] 視窗樣式，則當您嘗試插入具有 INSERTITEM LPSTR 的專案做為其 TEXTCALLBACK 成員的值時， **LVM \_ pszText** 訊息將會失敗 \_ 。 

如果下列條件成立， **LVM \_ INSERTITEM** 訊息會將新的專案插入排序次序中的適當位置：

-   您使用的是其中一個 LVS) \_ SORTXXX 樣式。
-   您未使用 [**lvs) \_ OWNERDRAW**](list-view-window-styles.md) 樣式。
-   **Pitem** 所指向之結構的 **pszText** 成員未設定為 LPSTR \_ TEXTCALLBACK。

如果 [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) 結構未 \_ 在 **遮罩** 成員中包含 LVIF GROUPID，則 **iGroupId** 成員的值預設為 I \_ GROUPIDCALLBACK。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **LVM \_INSERTITEMW** (Unicode) 和 **LVM \_ INSERTITEMA** (ANSI) <br/>             |



 

 





