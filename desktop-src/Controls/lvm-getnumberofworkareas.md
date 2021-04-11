---
title: 'LVM_GETNUMBEROFWORKAREAS 訊息 (Commctrl .h) '
description: 抓取清單視圖控制項中的工作區數目。 您可以明確地傳送此訊息，或使用 ListView \_ GetNumberOfWorkAreas 宏。
ms.assetid: ce0bcccd-62a2-45a4-959e-9959c9ca0c46
keywords:
- LVM_GETNUMBEROFWORKAREAS message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETNUMBEROFWORKAREAS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a73c62b7184ba60b979356a98a93d2579c8f74a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934895"
---
# <a name="lvm_getnumberofworkareas-message"></a>LVM \_ GETNUMBEROFWORKAREAS 訊息

抓取清單視圖控制項中的工作區數目。 您可以明確地傳送此訊息，或使用 [**ListView \_ GetNumberOfWorkAreas**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getnumberofworkareas) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

UINT 值的指標，此值會接收清單視圖控制項中的工作區數目。 如果在這個變數中放置零，則目前未設定任何工作區域。 此值不可以是 **Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

未使用此訊息的傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[使用 List-View 控制項](using-list-view-controls.md)
</dt> </dl>

 

 





