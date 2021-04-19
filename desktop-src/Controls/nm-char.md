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
ms.openlocfilehash: e0910736bcb174c2f3ddb16174c153f4b22ac5bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968391"
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
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[NM \_ 字元 (工具列) ](nm-char-toolbar.md)
</dt> </dl>

 

 





