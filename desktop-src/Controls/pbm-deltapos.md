---
title: 'PBM_DELTAPOS 訊息 (Commctrl .h) '
description: 依指定的遞增量將進度列的目前位置往前移，並重新繪製橫條以反映新的位置。
ms.assetid: 92c89434-d50b-45e7-b686-42e9297518b9
keywords:
- PBM_DELTAPOS message Windows 控制項
topic_type:
- apiref
api_name:
- PBM_DELTAPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19d0c36bbfdf5a812c8a7ffb2b2cdda6720fb757
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025287"
---
# <a name="pbm_deltapos-message"></a>PBM \_ DELTAPOS 訊息

依指定的遞增量將進度列的目前位置往前移，並重新繪製橫條以反映新的位置。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

要預先放置位置的數量。

</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回先前的位置。

## <a name="remarks"></a>備註

如果增量產生的值超出控制項範圍，則位置會設定為最接近的界限。

如果傳送給具有 [**PBS \_ 天棚**](progress-bar-control-styles.md) 樣式的控制項，則不會定義此訊息的行為。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





