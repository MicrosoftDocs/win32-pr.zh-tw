---
title: 'TTM_TRACKACTI加值稅E 訊息 (Commctrl .h) '
description: 啟用或停用追蹤工具提示。
ms.assetid: 6cf43377-a772-4749-81c4-a685998092e5
keywords:
- TTM_TRACKACTI加值稅E message Windows 控制項
topic_type:
- apiref
api_name:
- TTM_TRACKACTIVATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eb3d0a6caf110045d694208c63aa81d63c265c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934622"
---
# <a name="ttm_trackactivate-message"></a>TTM \_ TRACKACTI加值稅E 訊息

啟用或停用追蹤工具提示。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

值，指定是否要啟用或停用追蹤。 這個值可以是下列其中一個值：



| 值                                                                                                                                | 意義                         |
|--------------------------------------------------------------------------------------------------------------------------------------|---------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <dt>**真**</dt> </dl>    | 啟用追蹤。<br/>   |
| <span id="FALSE"></span><span id="false"></span><dl> <dt>**假**</dt> </dl> | 停用追蹤。<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

[**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa)結構的指標，此結構會識別要套用此訊息的工具。 **Hwnd** 和 **uId** 成員會識別工具，而 **cbSize** 成員會指定結構的大小。 所有其他成員都會被忽略。

</dd> </dl>

## <a name="return-value"></a>傳回值

未使用此訊息的傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**TTM \_ TRACKPOSITION**](ttm-trackposition.md)
</dt> <dt>

**概念**
</dt> <dt>

[使用工具提示控制項](using-tooltip-contro.md)
</dt> </dl>

 

 





