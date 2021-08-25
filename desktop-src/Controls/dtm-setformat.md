---
title: 'DTM_SETFORMAT 訊息 (Commctrl .h) '
description: 根據指定的格式字串，設定日期和時間選擇器的顯示 (DTP) 控制項。 您可以明確地傳送此訊息，或使用 DateTime \_ SetFormat 宏。
ms.assetid: a89fa3ad-9894-4c52-ab56-fb62208e39b3
keywords:
- DTM_SETFORMAT 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- DTM_SETFORMAT
- DTM_SETFORMATA
- DTM_SETFORMATW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17d4bb08694b63c21f1790d0a1366dd34d1083592bdeb62d532a32a96be3857a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877858"
---
# <a name="dtm_setformat-message"></a>DTM \_ SETFORMAT 訊息

根據指定的格式字串，設定日期和時間選擇器的顯示 (DTP) 控制項。 您可以明確地傳送此訊息，或使用 [**DateTime \_ SetFormat**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setformat) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

以零結束的 [格式字串](date-and-time-picker-controls.md) 指標，可定義所需的顯示。 將此參數設定為 **Null** ，會將控制項重設為目前樣式的預設格式字串。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回非零，否則傳回零。

## <a name="remarks"></a>備註

您可以在格式字串中包含額外的字元，以產生更豐富的顯示。 不過，任何非字元都必須括在單引號內。 例如，Today 格式字串 "' Today： ' hh '： '： ' ddddMMMdd '，' yyy" 會產生像是 "Today：04:22:31 星期二3月23日，1996" 的輸出。

> [!Note]  
> 當 DTP 控制項使用預設格式字串時，會追蹤地區設定的變更。 如果您設定自訂格式字串，將不會更新它以回應地區設定變更。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **DTM \_SETFORMATW** (Unicode) 和 **DTM \_ SETFORMATA** (ANSI) <br/>               |



 

 





