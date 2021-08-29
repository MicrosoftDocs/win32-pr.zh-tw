---
title: 'PBM_STEPIT 訊息 (Commctrl .h) '
description: 將進度列的目前位置往前移，並重新繪製橫條以反映新的位置。 應用程式會藉由傳送 PBM SETSTEP 訊息來設定步驟增量 \_ 。
ms.assetid: fd9947f6-7a48-4207-b691-b7db78eb8a85
keywords:
- PBM_STEPIT 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- PBM_STEPIT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71b43bb50390fff3813b4dd52fe7b2099d707a8636565b5efd4c99bcb8754511
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018746"
---
# <a name="pbm_stepit-message"></a>PBM \_ STEPIT 訊息

將進度列的目前位置往前移，並重新繪製橫條以反映新的位置。 應用程式會藉由傳送 [**PBM \_ SETSTEP**](pbm-setstep.md) 訊息來設定步驟增量。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回先前的位置。

## <a name="remarks"></a>備註

當位置超過最大範圍值時，此訊息會重設目前的位置，使進度指示器會從頭開始。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





