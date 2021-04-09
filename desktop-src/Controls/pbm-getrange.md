---
title: 'PBM_GETRANGE 訊息 (Commctrl .h) '
description: 抓取指定進度列控制項目前最高和最低限制的相關資訊。
ms.assetid: 676b7a37-bdde-4307-9888-9a0cf40db2db
keywords:
- PBM_GETRANGE message Windows 控制項
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
ms.openlocfilehash: e0c4ffe9365686432a5e78cb1540055f41a838fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934722"
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
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





