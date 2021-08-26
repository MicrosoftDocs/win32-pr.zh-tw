---
title: 'TVM_SORTCHILDREN 訊息 (Commctrl .h) '
description: 排序樹狀檢視控制項中所指定父專案的子專案。 您可以使用 TreeView SortChildren 宏明確地傳送此訊息 \_ 。
ms.assetid: c18bcd5f-c083-46ee-873b-d3100b0d7b04
keywords:
- TVM_SORTCHILDREN 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TVM_SORTCHILDREN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f975814fadc5271c562e4e8e420c35dbb3450142bed797af83af73fdf81a55d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913798"
---
# <a name="tvm_sortchildren-message"></a>TVM \_ SORTCHILDREN 訊息

排序樹狀檢視控制項中所指定父專案的子專案。 您可以使用 [**TreeView \_ SortChildren**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sortchildren) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

值，指定排序是否為遞迴。 將 *wParam* 設為 **TRUE** ，以排序父專案底下的所有子專案層級。 否則，只會排序父系的直屬子系。

</dd> <dt>

*lParam* 
</dt> <dd>

要排序其子專案的父專案的控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

此訊息會在專案名稱上使用 [**lstrcmpi**](/windows/desktop/api/winbase/nf-winbase-lstrcmpia) Alphabetizes 樹狀目錄專案。 您可以使用 [**TVM \_ SORTCHILDRENCB**](tvm-sortchildrencb.md) 訊息來自訂排序行為。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

