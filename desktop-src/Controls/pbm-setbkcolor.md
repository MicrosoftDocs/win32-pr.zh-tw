---
title: 'PBM_SETBKCOLOR 訊息 (Commctrl .h) '
description: 設定進度列中的背景色彩。
ms.assetid: e28af958-babb-4c2e-9202-89b608c22f8e
keywords:
- PBM_SETBKCOLOR message Windows 控制項
topic_type:
- apiref
api_name:
- PBM_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ddfaf84695221cf998275d76a9d2d67773150da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686167"
---
# <a name="pbm_setbkcolor-message"></a>PBM \_ SETBKCOLOR 訊息

設定進度列中的背景色彩。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

**COLORREF** 值，指定新的背景色彩。 指定 CLR \_ 預設值，使進度列使用其預設背景色彩。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回先前的背景色彩，或 \_ 如果背景色彩為預設色彩，則為 CLR 預設值。

## <a name="remarks"></a>備註

啟用視覺化樣式時，此訊息不會有任何作用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





