---
title: 'MCM_GETCURRENTVIEW 訊息 (Commctrl .h) '
description: 取得行事曆的目前視圖。 您可以使用 MonthCal GetCurrentView 宏明確地傳送此訊息 \_ 。
ms.assetid: 9c42ebf6-611e-4e50-9dcc-cf7fd63b32eb
keywords:
- MCM_GETCURRENTVIEW 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- MCM_GETCURRENTVIEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50f7fce3c1a22ec14ec34e849bd2e3fc4634118b11613913da4e6fae0b9b7b51
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119319678"
---
# <a name="mcm_getcurrentview-message"></a>MCM \_ GETCURRENTVIEW 訊息

取得行事曆的目前視圖。 您可以使用 [**MonthCal \_ GetCurrentView**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcurrentview) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

目前的觀點。 下列其中一個值。



| 傳回碼                                                                                  | 描述              |
|----------------------------------------------------------------------------------------------|--------------------------|
| <dl> <dt>**MCMV \_ 月份**</dt> </dl>   | 每月的觀點。<br/> |
| <dl> <dt>**MCMV \_ 年**</dt> </dl>    | 年度觀點。<br/>  |
| <dl> <dt>**MCMV \_ 十年**</dt> </dl>  | 十年的觀點。<br/>  |
| <dl> <dt>**MCMV \_ 世紀**</dt> </dl> | 世紀的觀點。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





