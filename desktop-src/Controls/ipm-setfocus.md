---
title: 'IPM_SETFOCUS 訊息 (Commctrl .h) '
description: 將鍵盤焦點設定為 IP 位址控制項中的指定欄位。 將會選取該欄位中的所有文字。
ms.assetid: 4b975eb2-85e1-4e33-a803-99b48d2ff5e8
keywords:
- IPM_SETFOCUS 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- IPM_SETFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a74d98aa4d4259d11d7fef6e0bfdad2bfe741447ddffab27fa41545e7eda515
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085568"
---
# <a name="ipm_setfocus-message"></a>IPM \_ SETFOCUS 訊息

將鍵盤焦點設定為 IP 位址控制項中的指定欄位。 將會選取該欄位中的所有文字。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

以零為基底的欄位索引，應設定焦點。 如果這個值大於欄位數目，則焦點會設定為第一個空白欄位。 如果所有欄位都是非空白的，則焦點會設定為第一個欄位。

</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

未使用傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





