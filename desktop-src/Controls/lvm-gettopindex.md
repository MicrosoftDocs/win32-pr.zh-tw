---
title: 'LVM_GETTOPINDEX 訊息 (Commctrl .h) '
description: 在清單或報表檢視中，抓取最上層可見專案的索引。 您可以明確地傳送此訊息，或使用 ListView \_ GetTopIndex 宏來傳送。
ms.assetid: vs|controls|~\controls\listview\messages\lvm_gettopindex.htm
keywords:
- LVM_GETTOPINDEX 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETTOPINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6434aa2c7382a4a4d54fc3a76edd5eb4b70ccae858b8d9fcf41547590a8bc69c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119920038"
---
# <a name="lvm_gettopindex-message"></a>LVM \_ GETTOPINDEX 訊息

在清單或報表檢視中，抓取最上層可見專案的索引。 您可以明確地傳送此訊息，或使用 [**ListView \_ GetTopIndex**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettopindex) 宏來傳送。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回專案的索引。 如果清單視圖控制項在圖示或小型圖示視圖中，或如果清單視圖控制項在已啟用群組的詳細資料檢視中，則傳回零。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





