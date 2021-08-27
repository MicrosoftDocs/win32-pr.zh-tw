---
title: 'LVM_GETNUMBEROFWORKAREAS 訊息 (Commctrl .h) '
description: 抓取清單視圖控制項中的工作區數目。 您可以明確地傳送此訊息，或使用 ListView \_ GetNumberOfWorkAreas 宏。
ms.assetid: ce0bcccd-62a2-45a4-959e-9959c9ca0c46
keywords:
- LVM_GETNUMBEROFWORKAREAS 訊息 Windows 控制項
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
ms.openlocfilehash: 735dbb808755857df3dec4c5e8a021b9fe873e555607dc547bc77e67e123b948
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088878"
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
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[使用 List-View 控制項](using-list-view-controls.md)
</dt> </dl>

 

 





