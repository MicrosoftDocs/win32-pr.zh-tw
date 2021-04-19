---
title: 'NM_NCHITTEST (Commctrl 的通知碼) '
description: 當控制項收到 WM NCHITTEST 訊息時，由 Rebar 控制項傳送 \_ 。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 0e088b14-b912-4f60-9d25-cd0a0ba264c3
keywords:
- NM_NCHITTEST 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- NM_NCHITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8af39fd792ecb9aeb463957f49f5722737e6ee5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969786"
---
# <a name="nm_nchittest-notification-code"></a>NM \_ NCHITTEST 通知碼

當控制項收到 [**WM \_ NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) 訊息時，由 Rebar 控制項傳送。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
NM_NCHITTEST
        
    lpnmmouse = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse)結構的指標，其中包含通知碼的相關資訊。 *Pt* 成員包含點擊測試訊息的滑鼠座標。

</dd> </dl>

## <a name="return-value"></a>傳回值

除非另有指定，否則會傳回零以允許控制項執行點擊測試訊息的預設處理，或傳回 \* 在 [**WM \_ NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) 下記載的其中一個 HT 值以覆寫預設的點擊測試處理。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

