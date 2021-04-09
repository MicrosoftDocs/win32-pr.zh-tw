---
title: 'RB_GETBANDBORDERS 訊息 (Commctrl .h) '
description: 抓取寬線的框線。 此訊息的結果可以用來計算頻外的可用區域。
ms.assetid: 45f2ae7e-636e-474b-a0d0-5235c6401e6a
keywords:
- RB_GETBANDBORDERS message Windows 控制項
topic_type:
- apiref
api_name:
- RB_GETBANDBORDERS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 521dfecaf5e2573b30f606b7b4d7ecdec9bd896d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934708"
---
# <a name="rb_getbandborders-message"></a>RB \_ GETBANDBORDERS 訊息

抓取寬線的框線。 此訊息的結果可以用來計算頻外的可用區域。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

以零為基底的寬線索引，將會取出框線。

</dd> <dt>

*lParam* 
</dt> <dd>

將會接收帶框線的 [**矩形**](/previous-versions//dd162897(v=vs.85)) 結構指標。 如果 Rebar 控制項有 [**RBS \_ BANDBORDERS**](rebar-control-styles.md) 樣式，則此結構的每個成員都會收到組成框線之帶狀邊的圖元數。 如果 Rebar 控制項沒有 **RBS \_ BANDBORDERS** 樣式，則只有此結構的 **左側** 成員會收到有效的資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

未使用傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

