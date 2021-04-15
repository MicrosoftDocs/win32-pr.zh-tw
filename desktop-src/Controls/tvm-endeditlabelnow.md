---
title: 'TVM_ENDEDITLABELNOW 訊息 (Commctrl .h) '
description: 結束編輯樹狀檢視專案的標籤。 您可以使用 TreeView EndEditLabelNow 宏明確地傳送此訊息 \_ 。
ms.assetid: 68de2020-9311-4958-859a-de55f5e41fcf
keywords:
- TVM_ENDEDITLABELNOW message Windows 控制項
topic_type:
- apiref
api_name:
- TVM_ENDEDITLABELNOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f059be20560adeb8cbcb0c63a2555283f6b7051
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508448"
---
# <a name="tvm_endeditlabelnow-message"></a>TVM \_ ENDEDITLABELNOW 訊息

結束編輯樹狀檢視專案的標籤。 您可以使用 [**TreeView \_ EndEditLabelNow**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_endeditlabelnow) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

變數，指出編輯是否取消，而不儲存至標籤。 如果此參數為 **TRUE**，系統就會取消編輯，而不儲存變更。 否則，系統會將變更儲存至標籤。

</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

此訊息會使 [izdebski \_ ENDLABELEDIT](tvn-endlabeledit.md) 通知程式碼傳送至樹狀檢視控制項的父視窗。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





