---
title: 'PBM_STEPIT 訊息 (Commctrl .h) '
description: 將進度列的目前位置往前移，並重新繪製橫條以反映新的位置。 應用程式會藉由傳送 PBM SETSTEP 訊息來設定步驟增量 \_ 。
ms.assetid: fd9947f6-7a48-4207-b691-b7db78eb8a85
keywords:
- PBM_STEPIT message Windows 控制項
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
ms.openlocfilehash: aa0d4aee387e8f929aaaaf19d947422b95ca9528
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934716"
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
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





