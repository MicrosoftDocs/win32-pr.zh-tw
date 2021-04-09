---
title: 'TCM_GETITEMRECT 訊息 (Commctrl .h) '
description: 抓取索引標籤控制項中索引標籤的周框。 您可以使用 TabCtrl GetItemRect 宏明確地傳送此訊息 \_ 。
ms.assetid: 6abd8cdf-5f19-4b7e-800e-970097bc891b
keywords:
- TCM_GETITEMRECT message Windows 控制項
topic_type:
- apiref
api_name:
- TCM_GETITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa6c214efbeeaf58d1ff3def9f50f10011b41dfc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844180"
---
# <a name="tcm_getitemrect-message"></a>TCM \_ GETITEMRECT 訊息

抓取索引標籤控制項中索引標籤的周框。 您可以使用 [**TabCtrl \_ GetItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getitemrect) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

索引標籤的索引。

</dd> <dt>

*lParam* 
</dt> <dd>

[**矩形**](/previous-versions//dd162897(v=vs.85))結構的指標，此結構會接收索引標籤的周框座標（以區座標表示）。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

