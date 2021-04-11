---
title: 'LVM_GETSELECTEDCOUNT 訊息 (Commctrl .h) '
description: 決定清單視圖控制項中選取的專案數目。 您可以明確地傳送此訊息，或使用 ListView \_ GetSelectedCount 宏來傳送。
ms.assetid: 38916227-e6ca-4efa-9821-13f0fdb29834
keywords:
- LVM_GETSELECTEDCOUNT message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETSELECTEDCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b23f0e8d1d87e2cc7dd60d32ac3dd4943611a36f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844092"
---
# <a name="lvm_getselectedcount-message"></a>LVM \_ GETSELECTEDCOUNT 訊息

決定清單視圖控制項中選取的專案數目。 您可以明確地傳送此訊息，或使用 [**ListView \_ GetSelectedCount**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getselectedcount) 宏來傳送。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回選取之專案的數目。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





