---
title: 'TB_SETLISTGAP 訊息 (Commctrl .h) '
description: 設定特定工具列上工具列按鈕之間的距離。
ms.assetid: ca8ba6e4-cf70-41ca-ac61-cd13671d4010
keywords:
- TB_SETLISTGAP 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TB_SETLISTGAP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6192a002fcc2aec52c6c294b9eaad3fc55af3bfa3d01a092ae44f5c6d4087559
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078172"
---
# <a name="tb_setlistgap-message"></a>TB \_ SETLISTGAP 訊息

設定特定工具列上工具列按鈕之間的距離。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

工具列上按鈕之間的間距（以圖元為單位）。

</dd> <dt>

*lParam* 
</dt> <dd>

忽略。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

按鈕之間的間距只適用于接收此訊息的工具列控制項視窗。 如果工具列目前是可見的，則接收此訊息會觸發工具列的重新繪製。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





