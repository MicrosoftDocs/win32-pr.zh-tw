---
title: 'UDM_GETRANGE32 訊息 (Commctrl .h) '
description: 抓取上下按鈕控制項的32位範圍。
ms.assetid: a94b50c9-cd2f-430d-875f-720e51f544f1
keywords:
- UDM_GETRANGE32 message Windows 控制項
topic_type:
- apiref
api_name:
- UDM_GETRANGE32
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca418cd08dc4c81b3ff734d74f3ca9deeef7d848
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465024"
---
# <a name="udm_getrange32-message"></a>UDM \_ GETRANGE32 訊息

抓取上下按鈕控制項的32位範圍。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

帶正負號之整數的指標，該整數會接收最小的最小值控制項範圍。 這個參數可以是 **Null**。

</dd> <dt>

*lParam* 
</dt> <dd>

帶正負號之整數的指標，該整數會接收上下按鈕控制項範圍的上限。 這個參數可以是 **Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

未使用此訊息的傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





