---
title: 'TB_GETTOOLTIPS 訊息 (Commctrl .h) '
description: 抓取與工具列相關聯之工具提示控制項（如果有的話）的控制碼。
ms.assetid: 1e0edfdc-d0cb-41f3-9178-1239d81d3034
keywords:
- TB_GETTOOLTIPS message Windows 控制項
topic_type:
- apiref
api_name:
- TB_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 488212b34f9f1816797f097a5a1f42d2ea4f68c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025178"
---
# <a name="tb_gettooltips-message"></a>TB \_ GETTOOLTIPS 訊息

抓取與工具列相關聯之工具提示控制項（如果有的話）的控制碼。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回工具提示控制項的控制碼; 如果工具列沒有相關聯的工具提示，則 **為 Null** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





