---
title: 'LVM_INSERTGROUP 訊息 (Commctrl .h) '
description: 將群組插入清單視圖控制項。
ms.assetid: d43e21bc-e212-42dd-af88-48813d40cd50
keywords:
- LVM_INSERTGROUP 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- LVM_INSERTGROUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f31504226663b0df91e0297ed29abf784ff239dfcee5f323e8617f73dff65acc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019246"
---
# <a name="lvm_insertgroup-message"></a>LVM \_ INSERTGROUP 訊息

將群組插入清單視圖控制項。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>要加入群組的索引。 如果這是-1，則會將群組新增至清單結尾。</dd> <dt>

*lParam* 
</dt> <dd><a href="/windows/win32/api/commctrl/ns-commctrl-lvgroup">**LVGROUP**</a>結構的指標，其中包含要加入的群組。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回群組已加入之專案的索引，如果作業失敗，則為-1。

## <a name="remarks"></a>備註

若要開啟群組模式，請呼叫 [**LVM \_ ENABLEGROUPVIEW**](lvm-enablegroupview.md) 或 [**ListView \_ ENABLEGROUPVIEW**](/windows/desktop/api/Commctrl/nf-commctrl-listview_enablegroupview)。

無法將群組插入空白的清單視圖控制項。

請務必在新增群組 () 的專案中設定 **iGroupId** 。 否則，當 [**LVM \_ ENABLEGROUPVIEW**](lvm-enablegroupview.md) 訊息處理為 **TRUE** 時，listview 控制項將不會顯示任何專案。

> [!Note]  
> 若要使用此訊息，您必須提供指定 Comclt32 6.0 版的資訊清單。 如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





