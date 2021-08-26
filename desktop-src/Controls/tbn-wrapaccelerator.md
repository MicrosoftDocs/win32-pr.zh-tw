---
title: 'TBN_WRAPACCELERATOR (Commctrl 的通知碼) '
description: 要求一或多個工具列中，對應至指定之快速鍵的按鈕索引。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: fc2443fd-e1b3-4085-b65d-96c08f544944
keywords:
- TBN_WRAPACCELERATOR 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TBN_WRAPACCELERATOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c5ec222f387108e2cb4d240e6dddf0fcb904d814097a96624a177425eb805ad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105028"
---
# <a name="tbn_wrapaccelerator-notification-code"></a>TBN \_ WRAPACCELERATOR 通知碼

要求一或多個工具列中，對應至指定之快速鍵的按鈕索引。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
TBN_WRAPACCELERATOR

    lpnmtb = (NMTBWRAPACCELERATOR) lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

結構的指標，其中包含快速鍵字元，並會接收對應按鈕的索引。 如果快速鍵未對應至命令，則索引為-1。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果傳回索引，則 **為 TRUE** ，否則為 **FALSE**。

## <a name="remarks"></a>備註

具有一或多個工具列的應用程式可能會收到此通知碼。

**NMTBWRAPACCELERATOR** 結構必須由應用程式定義，如下所示：

``` syntax
typedef struct tagNMTBWRAPACCELERATOR {
    NMHDR hdr;
    UINT ch;
    int iButton;
} NMTBWRAPACCELERATOR, *LPNMTBWRAPACCELERATOR;
```

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





