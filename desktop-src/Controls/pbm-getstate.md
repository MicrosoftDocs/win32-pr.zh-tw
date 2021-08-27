---
title: 'PBM_GETSTATE 訊息 (Commctrl .h) '
description: 取得進度列的狀態。
ms.assetid: ff240160-7db6-4711-8d4e-25a77dfba118
keywords:
- PBM_GETSTATE 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- PBM_GETSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cd157ccb6ab8a1fe4cd4a31bf1f8a033f0e591288338e21cc322a8ac10bfc41
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047008"
---
# <a name="pbm_getstate-message"></a>PBM \_ >getstate 訊息

取得進度列的狀態。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回進度列的目前狀態。 下列其中一個值。



| 傳回碼                                                                                 | 描述             |
|---------------------------------------------------------------------------------------------|-------------------------|
| <dl> <dt>**PBST \_ 正常**</dt> </dl> | 進行中。<br/> |
| <dl> <dt>**PBST \_ 錯誤**</dt> </dl>  | 錯誤。<br/>       |
| <dl> <dt>**PBST 已 \_ 暫停**</dt> </dl> | 已暫停。<br/>      |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





