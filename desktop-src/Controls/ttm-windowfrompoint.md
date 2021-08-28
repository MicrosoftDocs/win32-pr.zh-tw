---
title: 'TTM_WINDOWFROMPOINT 訊息 (Commctrl .h) '
description: 允許子類別程式使工具提示顯示滑鼠游標下方以外的視窗文字。
ms.assetid: f3bf6917-1745-4e4f-a9c1-8fe86b2b3906
keywords:
- TTM_WINDOWFROMPOINT 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TTM_WINDOWFROMPOINT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 572ce204fd9f0056ef77d62c7909a7281c478c38f6abeb95089ce86b0bdb1b8f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109538"
---
# <a name="ttm_windowfrompoint-message"></a>TTM \_ WINDOWFROMPOINT 訊息

允許子類別程式使工具提示顯示滑鼠游標下方以外的視窗文字。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

[**點**](/previous-versions//dd162805(v=vs.85))結構的指標，該結構定義要檢查的點。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是包含點之視窗的控制碼，如果指定的點沒有視窗存在，則為 **Null** 。

## <a name="remarks"></a>備註

此訊息的目的是要由子類別化工具提示的應用程式來處理。 它並不適合應用程式傳送。 工具提示會在顯示視窗的文字之前，將此訊息傳送給自己。 藉由變更 *lParam* 所指定之點的座標，子類別程式可能會導致工具提示顯示非滑鼠游標下的視窗文字。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

