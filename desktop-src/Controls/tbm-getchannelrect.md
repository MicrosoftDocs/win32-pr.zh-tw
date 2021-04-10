---
title: 'TBM_GETCHANNELRECT 訊息 (Commctrl .h) '
description: 抓取的區域框之頻道的大小與位置。
ms.assetid: 353edae3-1a26-4e85-8a32-ba8b5a976d24
keywords:
- TBM_GETCHANNELRECT message Windows 控制項
topic_type:
- apiref
api_name:
- TBM_GETCHANNELRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02982e9ce417b9fcf3e16d0e14d061e3ffd97a8a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934090"
---
# <a name="tbm_getchannelrect-message"></a>TBM \_ GETCHANNELRECT 訊息

抓取的區域框之頻道的大小與位置。  (通道是滑杆移動的區域。 它包含選取範圍時的醒目提示。 ) 

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

[**矩形**](/previous-versions//dd162897(v=vs.85))結構的指標。 此訊息會以通道的周框為單位，在 [協調器] 視窗的用戶端座標中填滿此結構。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

