---
title: 'TB_SETANCHORHIGHLIGHT 訊息 (Commctrl .h) '
description: 設定工具列的錨點醒目提示設定。
ms.assetid: d31652d5-e9cf-4bf3-8f90-818eb078fa87
keywords:
- TB_SETANCHORHIGHLIGHT 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TB_SETANCHORHIGHLIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77a66193aebee80a2ffde97b7e802b5bab750f0a9e2f1773b32d872211d52150
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118167981"
---
# <a name="tb_setanchorhighlight-message"></a>TB \_ SETANCHORHIGHLIGHT 訊息

設定工具列的錨點醒目提示設定。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

**布林** 值，指定是否啟用或停用錨點反白顯示。 如果此值為非零值，則會啟用錨點反白顯示。 如果此值為零，將會停用錨點反白顯示。

</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回上一個錨點醒目提示設定。 如果此值為非零值，則會啟用錨點反白顯示。 如果此值為零，則會停用錨點反白顯示。

## <a name="remarks"></a>備註

工具列中的錨點醒目提示表示最後一個反白顯示的專案會保持反白顯示，直到另一個專案反白顯示。 即使游標離開工具列控制項，也會發生這種情況。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





