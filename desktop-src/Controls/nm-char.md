---
title: 'NM_CHAR (Commctrl 的通知碼) '
description: '\_當處理字元鍵時，控制項會傳送 NM 字元通知碼。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。'
ms.assetid: b750f2a6-8642-4d76-96bb-bf58b00cd5c4
keywords:
- NM_CHAR 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- NM_CHAR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73c35871410244bfb69f67c7e0b2c960d0dd50d432ad9cdcfd8765c7df449bf8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018946"
---
# <a name="nm_char-notification-code"></a>NM \_ CHAR 通知碼

\_當處理字元鍵時，控制項會傳送 NM 字元通知碼。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
NM_CHAR

    lpnmc = (LPNMCHAR) lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMCHAR**](/windows/win32/api/commctrl/ns-commctrl-nmchar)結構的指標，其中包含造成通知碼之字元的其他相關資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

大部分的控制項都會忽略傳回值。 如需詳細資訊，請參閱個別控制項的檔。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[NM \_ 字元 (工具列) ](nm-char-toolbar.md)
</dt> </dl>

 

 





