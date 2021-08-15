---
title: 'CBEN_DRAGBEGIN (Commctrl 的通知碼) '
description: 當使用者開始拖曳顯示在控制項編輯部分的專案影像時傳送。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: bdab2700-a605-48af-aee3-bbf573408e3f
keywords:
- CBEN_DRAGBEGIN 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- CBEN_DRAGBEGIN
- CBEN_DRAGBEGINA
- CBEN_DRAGBEGINW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 626ad4d6abbcaaeb6f647aa94657ee1a681801a3ce13a9b5539216b1b67565a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118414058"
---
# <a name="cben_dragbegin-notification-code"></a>CBEN \_ DRAGBEGIN 通知碼

當使用者開始拖曳顯示在控制項編輯部分的專案影像時傳送。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
CBEN_DRAGBEGIN

    lpnmdb = (LPNMCBEDRAGBEGIN) lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMCBEDRAGBEGIN**](/windows/desktop/api/Commctrl/ns-commctrl-nmcbedragbegina)結構的指標，其中包含通知碼的相關資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值會被忽略。

## <a name="remarks"></a>備註

如果接收應用程式會從控制項中執行拖放功能，應用程式就會開始拖放作業來回應此通知碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **CBEN \_DRAGBEGINW** (Unicode) 和 **CBEN \_ DRAGBEGINA** (ANSI) <br/>             |



 

 





