---
title: 'TB_SETPARENT 訊息 (Commctrl .h) '
description: 設定工具列控制項傳送通知訊息的視窗。
ms.assetid: 4863bd9f-021b-4295-9483-459fc19325d9
keywords:
- TB_SETPARENT message Windows 控制項
topic_type:
- apiref
api_name:
- TB_SETPARENT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8137406c8e6854f86ed81d8d6b96293074ae67b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844195"
---
# <a name="tb_setparent-message"></a>TB \_ SETPARENT 訊息

設定工具列控制項傳送通知訊息的視窗。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

接收通知訊息的視窗控制碼。

</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是上一個通知視窗的控制碼; 如果沒有上一個通知視窗，則為 **Null** 。

## <a name="remarks"></a>備註

**TB 的 \_ SETPARENT** 訊息不會變更建立控制項時所指定的父視窗。 針對工具列控制項呼叫 [**GetParent**](/windows/desktop/api/winuser/nf-winuser-getparent) 函式會傳回實際的父視窗，而不是以 **TB \_ SETPARENT** 指定的視窗。 若要變更控制項的父視窗，請呼叫 [**SetParent**](/windows/desktop/api/winuser/nf-winuser-setparent) 函數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

