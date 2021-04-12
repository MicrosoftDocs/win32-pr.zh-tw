---
title: 'TVN_SINGLEEXPAND (Commctrl 的通知碼) '
description: '\_當使用者使用滑鼠按一下來開啟或關閉樹狀專案時，由具有電視 SINGLEEXPAND 樣式的樹狀檢視控制項所傳送。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。'
ms.assetid: ae738237-172a-400b-b9fe-33832224e299
keywords:
- TVN_SINGLEEXPAND 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TVN_SINGLEEXPAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 976c0e8acfee1f024e4ee7f88d9f745e4029ec82
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464660"
---
# <a name="tvn_singleexpand-notification-code"></a>IZDEBSKI \_ SINGLEEXPAND 通知碼

當使用者使用滑鼠按一下來開啟或關閉樹狀專案時，由具有 [**電視 \_ SINGLEEXPAND**](tree-view-control-window-styles.md) 樣式的樹狀檢視控制項所傳送。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
TVN_SINGLEEXPAND

    lpnmtv = (LPNMTREEVIEW)lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa)結構的指標，其中包含此通知碼的相關資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 TVNRET \_ 預設值，以允許發生預設行為。 若要修改預設行為，請傳回：



| 傳回碼                                                                                    | Description                                                      |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <dt>**TVNRET \_ SKIPOLD**</dt> </dl> | 略過未選取專案的預設處理。<br/> |
| <dl> <dt>**TVNRET \_ SKIPNEW**</dt> </dl> | 略過選取專案的預設處理。<br/>   |



 

## <a name="remarks"></a>備註

若要略過選取和未選取專案的預設處理，請將 TVNRET \_ SKIPOLD 和 TVNRET \_ SKIPNEW 與邏輯 OR 結合來傳回。

只有具有 [**電視 \_ SINGLEEXPAND**](tree-view-control-window-styles.md) 樣式的樹狀檢視控制項才會傳送此通知碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





