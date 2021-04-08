---
title: 'PBM_SETRANGE32 訊息 (Commctrl .h) '
description: 將進度列的最小值和最大值設定為32位值，並重新繪製橫條以反映新的範圍。
ms.assetid: 7958ea14-17b4-4c0e-97ec-b09fa0d36e8b
keywords:
- PBM_SETRANGE32 message Windows 控制項
topic_type:
- apiref
api_name:
- PBM_SETRANGE32
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55fcf91c794ec9ae3880d67f8df947f87fec413d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686165"
---
# <a name="pbm_setrange32-message"></a>PBM \_ SETRANGE32 訊息

將進度列的最小值和最大值設定為32位值，並重新繪製橫條以反映新的範圍。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

最小範圍值。 根據預設，最小值為零。

</dd> <dt>

*lParam* 
</dt> <dd>

最大範圍值。 此值必須大於 *wParam*。 根據預設，最大值為100。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **DWORD** 值，此值會在其 [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) 中保留先前的16位低限制，並在其 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))中保留先前的16位高限制。 如果先前的範圍是32位的值，則傳回值是由兩個32位限制的 **LOWORD** 所組成。

## <a name="remarks"></a>備註

若要取出整個最高和最低的32位值，請使用 [**PBM \_ GETRANGE**](pbm-getrange.md) 訊息。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

