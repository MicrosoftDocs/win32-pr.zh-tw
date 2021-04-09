---
title: 'TVM_SHOWINFOTIP 訊息 (Commctrl .h) '
description: 顯示樹狀檢視控制項中所指定專案的提示。 您可以明確地傳送此訊息，或使用 TreeView \_ ShowInfoTip 宏來傳送。
ms.assetid: ed5a1bda-5754-4bb3-aa22-8faaf1af1268
keywords:
- TVM_SHOWINFOTIP message Windows 控制項
topic_type:
- apiref
api_name:
- TVM_SHOWINFOTIP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76f147253800469a800677a242ff0ab0ccdbdfa4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844363"
---
# <a name="tvm_showinfotip-message"></a>TVM \_ SHOWINFOTIP 訊息

顯示樹狀檢視控制項中所指定專案的提示。 您可以明確地傳送此訊息，或使用 [**TreeView \_ ShowInfoTip**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_showinfotip) 宏來傳送。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* \[在\]
</dt> <dd>

專案的控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回零。

## <a name="remarks"></a>備註

大部分的應用程式都不會使用此訊息。 提示會自動顯示。 如需詳細資訊，請參閱 [關於 Tree-View 控制項](tree-view-controls.md) 總覽中的使用樹狀檢視提示。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





