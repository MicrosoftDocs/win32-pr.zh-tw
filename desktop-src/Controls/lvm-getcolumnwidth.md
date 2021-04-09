---
title: 'LVM_GETCOLUMNWIDTH 訊息 (Commctrl .h) '
description: 取得報表或清單視圖中資料行的寬度。 您可以明確地傳送此訊息，或使用 ListView \_ GetColumnWidth 宏來傳送。
ms.assetid: 06e8ec36-3bc5-4516-ac29-17c36fb6d962
keywords:
- LVM_GETCOLUMNWIDTH message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETCOLUMNWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0577e7cb2a589c432d4b5ca62f640de61d67dc75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104093848"
---
# <a name="lvm_getcolumnwidth-message"></a>LVM \_ GETCOLUMNWIDTH 訊息

取得報表或清單視圖中資料行的寬度。 您可以明確地傳送此訊息，或使用 [**ListView \_ GetColumnWidth**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcolumnwidth) 宏來傳送。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

資料行的索引。 清單視圖中會忽略此參數。

</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回資料行寬度，否則傳回零。 如果此訊息傳送至具有 [**lvs) \_ 報表**](list-view-window-styles.md) 樣式的清單視圖控制項，而且指定的資料行不存在，則傳回值為未定義。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





