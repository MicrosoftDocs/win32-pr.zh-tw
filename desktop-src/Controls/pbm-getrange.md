---
title: 'PBM_GETRANGE 訊息 (Commctrl .h) '
description: 抓取指定進度列控制項目前最高和最低限制的相關資訊。
ms.assetid: 676b7a37-bdde-4307-9888-9a0cf40db2db
keywords:
- PBM_GETRANGE 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- PBM_GETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 007a62386180e7b47edca201236cd1dacc86df696b5705d02ec1da0acb89761c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986398"
---
# <a name="pbm_getrange-message"></a>PBM \_ GETRANGE 訊息

抓取指定進度列控制項目前最高和最低限制的相關資訊。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

旗標值，指定要使用哪個限制值做為訊息的傳回值。 這個參數可以是下列其中一個值：



| 值                                                                                                                                    | 意義                           |
|------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <dt>TRUE * * * *</dt> </dl>    | 傳回低限制。<br/>  |
| <span id="FALSE"></span><span id="false"></span><dl> <dt>FALSE * * * *</dt> </dl> | 傳回高限制。<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

[**PBRANGE**](/windows/desktop/api/Commctrl/ns-commctrl-pbrange)結構的指標，此結構會以進度列控制項的高度和下限來填滿。 如果此參數設定為 **Null**，則控制項只會傳回 *wParam* 所指定的限制。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回整數，表示 *wParam* 所指定的限制值。 如果 *lParam* 不是 **Null**，則 *lParam* 必須指向要使用兩個限制值填滿的 [**PBRANGE**](/windows/desktop/api/Commctrl/ns-commctrl-pbrange) 結構。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





