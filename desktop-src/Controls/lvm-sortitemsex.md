---
title: 'LVM_SORTITEMSEX 訊息 (Commctrl .h) '
description: 使用應用程式定義的比較函式來排序清單視圖控制項的專案。 每個專案的索引都會變更，以反映新的序列。 您可以明確地傳送此訊息，或使用 ListView \_ SortItemsEx 宏來傳送。
ms.assetid: eab2f6f5-68fd-4cb6-acf4-cb267ee40fdc
keywords:
- LVM_SORTITEMSEX message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_SORTITEMSEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99e524b00cb5ff1260eb68e7d86e185e5ae60c75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024663"
---
# <a name="lvm_sortitemsex-message"></a>LVM \_ SORTITEMSEX 訊息

使用應用程式定義的比較函式來排序清單視圖控制項的專案。 每個專案的索引都會變更，以反映新的序列。 您可以明確地傳送此訊息，或使用 [**ListView \_ SortItemsEx**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sortitemsex) 宏來傳送。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

傳遞給比較函數的應用程式定義值。

</dd> <dt>

*lParam* 
</dt> <dd>

應用程式定義的比較函式的指標。 每次需要比較兩個清單專案的相對順序時，就會在排序作業期間呼叫它。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

比較函數的形式如下：

``` syntax
int CALLBACK CompareFunc(LPARAM lParam1, LPARAM lParam2, LPARAM lParamSort);  
```

此訊息類似于 [**LVM \_ SORTITEMS**](lvm-sortitems.md)，但傳遞給比較函數的資訊類型除外。 使用 **LVM \_ SORTITEMSEX**， *lParam1* 是第一個專案的目前索引，而 *lParam2* 是第二個專案的目前索引。 如有需要，您可以傳送 [**LVM \_ GETITEMTEXT**](lvm-getitemtext.md) 訊息來取得專案的詳細資訊。

如果第一個專案應該在第二個專案之前，比較函式必須傳回負值，如果第一個專案應接在第二個專案，則為正值，如果兩個專案相等，則為零。

> [!Note]  
> 在排序過程中，清單視圖內容不穩定。 如果回呼函式將任何訊息傳送至 GETITEM 的 LVM GETITEM 以外的 [**LVM \_**](lvm-getitem.md) 控制項， ([**ListView \_**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitem)) ，結果就是無法預期的結果。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





