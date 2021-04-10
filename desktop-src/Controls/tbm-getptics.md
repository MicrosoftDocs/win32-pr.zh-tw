---
title: 'TBM_GETPTICS 訊息 (Commctrl .h) '
description: 抓取陣列的位址，這個陣列包含了刻度的刻度位置。
ms.assetid: d15a4b4d-2ced-40a4-9351-ed7ecc5a5751
keywords:
- TBM_GETPTICS message Windows 控制項
topic_type:
- apiref
api_name:
- TBM_GETPTICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d5d81e67156c0118310017413b8e73714246b7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934409"
---
# <a name="tbm_getptics-message"></a>TBM \_ GETPTICS 訊息

抓取陣列的位址，這個陣列包含了刻度的刻度位置。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **DWORD** 值陣列的位址。 陣列的元素會指定這些標頭的刻度的邏輯位置，而不包含由並排標示所建立的第一個和最後一個刻度。 邏輯位置可以是 [最小值] 和 [最大值] 滑杆位置範圍中的任何整數值。

## <a name="remarks"></a>備註

陣列中的元素數目是兩個小於 [**TBM \_ GETNUMTICS**](tbm-getnumtics.md) 訊息所傳回之滴答計數的兩個專案。 請注意，陣列中的值可能包含重複的位置，而且可能不是順序。 傳回的指標會一直有效，直到您變更了這些標記的刻度。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





