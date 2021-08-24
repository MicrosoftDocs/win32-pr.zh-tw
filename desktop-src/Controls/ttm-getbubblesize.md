---
title: 'TTM_GETBUBBLESIZE 訊息 (Commctrl .h) '
description: 傳回工具提示控制項的寬度和高度。
ms.assetid: 6afb971e-f05d-4b7a-b63d-3672bfcc32dc
keywords:
- TTM_GETBUBBLESIZE 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TTM_GETBUBBLESIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8354a93521b6adac9306374f5bfbc99e84738ac87f0471a22f199b7b611f100b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769378"
---
# <a name="ttm_getbubblesize-message"></a>TTM \_ GETBUBBLESIZE 訊息

傳回工具提示控制項的寬度和高度。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

工具提示 [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) 結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回低字組中的工具提示寬度和高單字中的高度。 否則，它會傳回 **FALSE**。

## <a name="remarks"></a>備註

如果 TTF \_ TRACK 和 TTF \_ 絕對旗標是在工具提示 [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa)結構的 **uFlags** 成員中設定，則可以使用此訊息來協助正確定位工具提示。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





