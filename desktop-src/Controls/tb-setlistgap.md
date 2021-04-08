---
title: 'TB_SETLISTGAP 訊息 (Commctrl .h) '
description: 設定特定工具列上工具列按鈕之間的距離。
ms.assetid: ca8ba6e4-cf70-41ca-ac61-cd13671d4010
keywords:
- TB_SETLISTGAP message Windows 控制項
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
ms.openlocfilehash: 224a709b7beefcfdf49ea7838f905977487aca8d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843052"
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
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





