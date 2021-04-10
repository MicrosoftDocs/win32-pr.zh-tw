---
title: 'TB_GETPADDING 訊息 (Commctrl .h) '
description: 抓取工具列控制項的邊框距離。
ms.assetid: dde0f44d-5d22-4cab-a7f8-48d84b8995d3
keywords:
- TB_GETPADDING message Windows 控制項
topic_type:
- apiref
api_name:
- TB_GETPADDING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b15babf2fd5d97377991d1827ea8947e9d794600
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025438"
---
# <a name="tb_getpadding-message"></a>TB \_ GETPADDING 訊息

抓取工具列控制項的邊框距離。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **DWORD** 值，其中包含低字組中的水準填補，以及高單字中的垂直填補（以圖元為單位）。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TB \_ SETPADDING**](tb-setpadding.md)
</dt> </dl>

 

 





