---
title: 'TBM_SETTICFREQ 訊息 (Commctrl .h) '
description: 設定在 [標記] 中刻度的間隔頻率。
ms.assetid: c391260c-d6c2-4b6a-84e8-7fe5d734035b
keywords:
- TBM_SETTICFREQ message Windows 控制項
topic_type:
- apiref
api_name:
- TBM_SETTICFREQ
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b68a555a7803e663fa1708fc02214deecbb05aad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024846"
---
# <a name="tbm_setticfreq-message"></a>TBM \_ SETTICFREQ 訊息

設定在 [標記] 中刻度的間隔頻率。 例如，如果 [頻率] 設定為 [二]，則會在 [顯示區] 範圍中顯示每個其他增量的刻度。 頻率的預設設定為 1;亦即，範圍中的每個遞增都會與刻度相關聯。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

刻度的頻率。

</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

您必須要有 [**TBS \_ AUTOTICKS**](trackbar-control-styles.md) 樣式才能使用此訊息。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





