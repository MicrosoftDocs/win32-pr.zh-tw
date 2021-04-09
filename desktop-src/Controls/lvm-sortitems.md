---
title: 'LVM_SORTITEMS 訊息 (Commctrl .h) '
description: 使用應用程式定義的比較函式來排序清單視圖控制項的專案。 每個專案的索引都會變更，以反映新的序列。 您可以明確地傳送此訊息，或使用 ListView \_ SortItems 宏來傳送。
ms.assetid: ed3d5cec-69af-49a1-9cb7-eb5da1163071
keywords:
- LVM_SORTITEMS message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_SORTITEMS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1aba6e739a15eec5e951d7c3ead04aa36a8201f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935173"
---
# <a name="lvm_sortitems-message"></a>LVM \_ SORTITEMS 訊息

使用應用程式定義的比較函式來排序清單視圖控制項的專案。 每個專案的索引都會變更，以反映新的序列。 您可以明確地傳送此訊息，或使用 [**ListView \_ SortItems**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sortitems) 宏來傳送。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

傳遞給比較函數的應用程式定義值。

</dd> <dt>

*lParam* 
</dt> <dd>

應用程式定義的比較函式的指標。 每次需要比較兩個清單專案的相對順序時，就會在排序作業期間呼叫比較函數。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

比較函數的形式如下：

``` syntax
int CALLBACK CompareFunc(LPARAM lParam1, LPARAM lParam2, LPARAM lParamSort);
```

*LParam1* 參數是與第一個要比較的專案相關聯的值，而 *lParam2* 參數則是與第二個專案相關聯的值。 這些值是在專案插入清單中時，在專案的 [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema)結構的 **lParam** 成員中指定的值。 [**ListView \_ SortItems**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sortitems)的 *wParam* 參數會傳遞給回呼函式，做為它的第三個參數。

如果第一個專案應該在第二個專案之前，比較函式必須傳回負值，如果第一個專案應接在第二個專案，則為正值，如果兩個專案相等，則為零。

> [!Note]  
> 在排序過程中，清單視圖內容不穩定。 如果回呼函式將任何訊息傳送至 GETITEM 的 LVM GETITEM 以外的 [**LVM \_**](lvm-getitem.md) 控制項， ([**ListView \_**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitem)) ，結果就是無法預期的結果。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





