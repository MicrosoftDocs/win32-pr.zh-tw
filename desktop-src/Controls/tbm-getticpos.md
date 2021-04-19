---
title: 'TBM_GETTICPOS 訊息 (Commctrl .h) '
description: 抓取刻度中刻度標記目前的實體位置。
ms.assetid: a4b0ec32-ef4e-4607-ade1-5e2be02bebe4
keywords:
- TBM_GETTICPOS message Windows 控制項
topic_type:
- apiref
api_name:
- TBM_GETTICPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bb1346f63e9bb10b919c678373e0e8df0724861
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966114"
---
# <a name="tbm_getticpos-message"></a>TBM \_ GETTICPOS 訊息

抓取刻度中刻度標記目前的實體位置。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

以零為基底的索引，識別刻度。 第一個和最後一個刻度的位置無法透過此訊息直接使用。

</dd> <dt>

*lParam* 
</dt> <dd>

必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回用戶端座標中的距離（以客戶座標為單位），從頁首的工作區左邊或頂端到指定的刻度。 傳回值是水準交叉標記之刻度的 x 座標，或垂直橫條的 y 座標。 如果 *wParam* 不是有效的索引，則傳回值為-1。

## <a name="remarks"></a>備註

因為第一個和最後一個刻度無法透過這則訊息來使用，所以有效的索引會在其刻度上與其刻度位置位移。 如果 [**TBM \_ GETRANGEMIN**](tbm-getrangemin.md) 和 [**TBM \_ GETRANGEMAX**](tbm-getrangemax.md) 之間的差異小於二，則沒有有效的索引，而且此訊息將會失敗。

以下說明在顯示的刻度之間的關聯性、由此訊息提供的刻度，以及其以零為基底的索引。

``` syntax
0 1 2 3 4 5 6 7 8 9    // Tick positions seen on the trackbar.
  1 2 3 4 5 6 7 8      // Tick positions whose position can be identified.
  0 1 2 3 4 5 6 7      // Index numbers for the identifiable positions.
```

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





