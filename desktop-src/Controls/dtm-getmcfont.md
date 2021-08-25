---
title: 'DTM_GETMCFONT 訊息 (Commctrl .h) '
description: 取得日期和時間選擇器 (DTP) 控制項的子月曆控制項目前使用的字型。 您可以明確地傳送此訊息，或使用 DateTime \_ GetMonthCalFont 宏。
ms.assetid: 6687a1dc-6f6d-4684-80b2-f726b08d2f3a
keywords:
- DTM_GETMCFONT 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- DTM_GETMCFONT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2bf60f226e7fe5d309324bc517a7fd215abe4591fd5141ff149b14e162ac9be
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119878128"
---
# <a name="dtm_getmcfont-message"></a>DTM \_ GETMCFONT 訊息

取得日期和時間選擇器 (DTP) 控制項的子月曆控制項目前使用的字型。 您可以明確地傳送此訊息，或使用 [**DateTime \_ GetMonthCalFont**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalfont) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 HFONT 值，這個值是目前字型的控制碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





