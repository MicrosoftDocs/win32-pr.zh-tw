---
title: 'DTM_GETDATETIMEPICKERINFO 訊息 (Commctrl .h) '
description: 取得 (DTP) 控制項之日期和時間選擇器的資訊。
ms.assetid: 04847b68-ac45-4b28-8f62-2cd68ffe48d4
keywords:
- DTM_GETDATETIMEPICKERINFO message Windows 控制項
topic_type:
- apiref
api_name:
- DTM_GETDATETIMEPICKERINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2398a2543caa6d7104339fb8debd83fcee3ac71f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464433"
---
# <a name="dtm_getdatetimepickerinfo-message"></a>DTM \_ GETDATETIMEPICKERINFO 訊息

取得 (DTP) 控制項之日期和時間選擇器的資訊。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

必須為零。

</dd> <dt>

*lParam* \[在\]
</dt> <dd> 要接收資訊的 <a href="/windows/win32/api/commctrl/ns-commctrl-datetimepickerinfo">**DATETIMEPICKERINFO**</a> 指標。 呼叫端負責配置此結構的記憶體。 將結構的 **cbSize** 成員設定為 SIZEOF (DATETIMEPICKERINFO) ，然後再傳送此訊息。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值會被忽略。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





