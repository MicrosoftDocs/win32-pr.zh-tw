---
title: 'PBM_GETSTATE 訊息 (Commctrl .h) '
description: 取得進度列的狀態。
ms.assetid: ff240160-7db6-4711-8d4e-25a77dfba118
keywords:
- PBM_GETSTATE message Windows 控制項
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
ms.openlocfilehash: 07d4f7029fca46a046545efd1cea8e0eab99c757
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934721"
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



| 傳回碼                                                                                 | Description             |
|---------------------------------------------------------------------------------------------|-------------------------|
| <dl> <dt>**PBST \_ 正常**</dt> </dl> | 進行中。<br/> |
| <dl> <dt>**PBST \_ 錯誤**</dt> </dl>  | 錯誤。<br/>       |
| <dl> <dt>**PBST 已 \_ 暫停**</dt> </dl> | 已暫停。<br/>      |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





