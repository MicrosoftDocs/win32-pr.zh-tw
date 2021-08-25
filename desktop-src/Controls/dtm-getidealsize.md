---
title: 'DTM_GETIDEALSIZE 訊息 (Commctrl .h) '
description: 取得在不剪切的情況下顯示控制項所需的大小。 請明確地傳送此訊息，或使用 DateTime \_ GetIdealSize 宏。
ms.assetid: 15ec26a1-645b-4a96-af66-1031e1a46c6c
keywords:
- DTM_GETIDEALSIZE 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- DTM_GETIDEALSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 639fbbb25fbf61695f83b54f106f45ff3dd421f528807120be52edd7031e4f66
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119878228"
---
# <a name="dtm_getidealsize-message"></a>DTM \_ GETIDEALSIZE 訊息

取得在不剪切的情況下顯示控制項所需的大小。 請明確地傳送此訊息，或使用 [**DateTime \_ GetIdealSize**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getidealsize) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

未使用。 必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

要接收理想大小的 [**大小**](/previous-versions//dd145106(v=vs.85)) 結構指標。 呼叫應用程式負責配置此結構。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **TRUE**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

