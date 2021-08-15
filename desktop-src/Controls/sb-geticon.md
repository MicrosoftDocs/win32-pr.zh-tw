---
title: 'SB_GETICON 訊息 (Commctrl .h) '
description: 抓取狀態列中元件的圖示。
ms.assetid: f99508e3-afa8-48fd-b87a-fce41c4410ff
keywords:
- SB_GETICON 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- SB_GETICON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3df97598c1b002a794badb54f727632d58cc915f216947c019e452f5632a09fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118168764"
---
# <a name="sb_geticon-message"></a>SB \_ GETICON 訊息

抓取狀態列中元件的圖示。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

元件以零為起始的索引，其中包含要取出的圖示。 如果此參數為-1，則會假設狀態列為 [簡單模式](status-bars.md) 的狀態列。

</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回圖示的控制碼; 否則傳回 **Null** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





