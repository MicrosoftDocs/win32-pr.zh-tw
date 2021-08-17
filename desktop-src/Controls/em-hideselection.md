---
title: 'EM_HIDESELECTION 訊息 (Richedit .h) '
description: EM \_ HIDESELECTION 訊息會隱藏或顯示在 rich edit 控制項中的選取專案。
ms.assetid: 1245618f-c9e6-4876-9133-6009370cdb97
keywords:
- EM_HIDESELECTION 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- EM_HIDESELECTION
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d9e33ba0fd8f9a97dcc7ef9ba0a76acfd76110a4d718fa282f3ba66d8f1ef6d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119437928"
---
# <a name="em_hideselection-message"></a>EM \_ HIDESELECTION 訊息

**EM \_ HIDESELECTION** 訊息會隱藏或顯示在 rich edit 控制項中的選取專案。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

指定是否要隱藏或顯示選取範圍的值。 如果此參數為零，則會顯示選取範圍。 否則，就會隱藏選取範圍。

</dd> <dt>

*lParam* 
</dt> <dd>

未使用此參數;它必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

此訊息不會傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



 

 





