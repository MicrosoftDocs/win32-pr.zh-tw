---
title: 'TVM_SORTCHILDRENCB 訊息 (Commctrl .h) '
description: 使用會比較專案的應用程式定義回呼函式，來排序樹狀檢視專案。 您可以使用 TreeView SortChildrenCB 宏明確地傳送此訊息 \_ 。
ms.assetid: 1669e576-5e57-49f6-8097-7d6547306014
keywords:
- TVM_SORTCHILDRENCB message Windows 控制項
topic_type:
- apiref
api_name:
- TVM_SORTCHILDRENCB
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b1dab4abbbc019a81d7a066c81dbb3537a0d80d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466793"
---
# <a name="tvm_sortchildrencb-message"></a>TVM \_ SORTCHILDRENCB 訊息

使用會比較專案的應用程式定義回呼函式，來排序樹狀檢視專案。 您可以使用 [**TreeView \_ SortChildrenCB**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sortchildrencb) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

保留的。 必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

[**TVSORTCB**](/windows/win32/api/commctrl/ns-commctrl-tvsortcb)結構的指標。 **LpfnCompare** 成員是應用程式定義的回呼函式的位址，每次需要比較兩個清單專案的相對順序時，就會在排序作業期間呼叫此函數。 如需回呼函數的詳細資訊，請參閱 **TVSORTCB** 的描述。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





