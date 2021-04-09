---
title: 'LVM_GETCOUNTPERPAGE 訊息 (Commctrl .h) '
description: 當在清單或報表檢視中時，計算可在清單視圖控制項可見區域中垂直容納的專案數。 只會計算完全可見的專案。 您可以明確地傳送此訊息，或使用 ListView \_ GetCountPerPage 宏來傳送。
ms.assetid: 2ffd2bb1-cddf-4a4a-a4a8-087c9dc3fec0
keywords:
- LVM_GETCOUNTPERPAGE message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETCOUNTPERPAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 734d460754f9ae8a11c3a42d8eacebf31d0b6fc0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024594"
---
# <a name="lvm_getcountperpage-message"></a>LVM \_ GETCOUNTPERPAGE 訊息

當在清單或報表檢視中時，計算可在清單視圖控制項可見區域中垂直容納的專案數。 只會計算完全可見的專案。 您可以明確地傳送此訊息，或使用 [**ListView \_ GetCountPerPage**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcountperpage) 宏來傳送。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回完整可見專案的數目。 如果目前的視圖是圖示或小型圖示視圖，則傳回值是清單視圖控制項中的專案總數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





