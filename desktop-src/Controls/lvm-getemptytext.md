---
title: 'LVM_GETEMPTYTEXT 訊息 (Commctrl .h) '
description: 取得當清單視圖控制項顯示為空白時，所要顯示的文字。 明確地傳送此訊息，或使用 ListView \_ GetEmptyText 宏。
ms.assetid: aa6cb0ae-0c6c-42b7-80c5-c086c9579c81
keywords:
- LVM_GETEMPTYTEXT 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETEMPTYTEXT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9dd1dc1df7b0a558adda37938849b5383bbfee304d807a22a329e4f7301889b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118411467"
---
# <a name="lvm_getemptytext-message"></a>LVM \_ GETEMPTYTEXT 訊息

取得當清單視圖控制項顯示為空白時，所要顯示的文字。 明確地傳送此訊息，或使用 [**ListView \_ GetEmptyText**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getemptytext) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* \[在\]
</dt> <dd>

*LParam* 所指向的緩衝區大小，包括終止的 **Null**。

</dd> <dt>

*lParam* \[in、out\]
</dt> <dd>

以 null 終止的 Unicode 緩衝區指標， *wParam* 指定的大小，以接收文字。 呼叫端負責配置緩衝區。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





