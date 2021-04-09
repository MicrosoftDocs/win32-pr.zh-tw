---
title: 'TBM_GETNUMTICS 訊息 (Commctrl .h) '
description: 抓取在一個標記中的刻度數目。
ms.assetid: 3c3f7ebb-a544-474c-ba14-68eae543ee38
keywords:
- TBM_GETNUMTICS message Windows 控制項
topic_type:
- apiref
api_name:
- TBM_GETNUMTICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 712e1a0190334ec279f28a68959f3e3d5d5ffd1d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934089"
---
# <a name="tbm_getnumtics-message"></a>TBM \_ GETNUMTICS 訊息

抓取在一個標記中的刻度數目。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

如果未設定 [滴答旗](trackbar-control-styles.md) 標，則會傳回2作為開始和結束刻度。 如果已設定 [**TBS \_ NOTICKS**](trackbar-control-styles.md) ，則會傳回零。 否則，它會採用範圍最小值和最大值之間的差異、除以滴答頻率，然後加上2。

## <a name="remarks"></a>備註

**TBM \_ GETNUMTICS** 訊息會計算所有的刻度，包括由顯示項所建立的第一個和最後一個刻度標記。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





