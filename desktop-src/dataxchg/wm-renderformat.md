---
title: 'WM_RENDERFORMAT 訊息 (Winuser .h) '
description: 如果已延遲轉譯特定的剪貼簿格式，且應用程式已要求該格式的資料，則傳送給剪貼簿擁有者。
ms.assetid: 81638109-4c5e-4b4c-b2db-4208b6ee83cc
keywords:
- WM_RENDERFORMAT 訊息資料 Exchange
topic_type:
- apiref
api_name:
- WM_RENDERFORMAT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2885e056577656d6cabb8ea78f48a02a19f3c3c40bb3c30b1e5ca25c72cdf39b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118545307"
---
# <a name="wm_renderformat-message"></a>WM \_ RENDERFORMAT 訊息

如果已延遲轉譯特定的剪貼簿格式，且應用程式已要求該格式的資料，則傳送給剪貼簿擁有者。 剪貼簿擁有者必須以指定的格式轉譯資料，並藉由呼叫 [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) 函式將其放在剪貼簿上。


```C++
#define WM_RENDERFORMAT                 0x0305
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

要呈現的 [剪貼簿格式](standard-clipboard-formats.md) 。

</dd> <dt>

*lParam* 
</dt> <dd>

不使用這個參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式處理此訊息，它應該會傳回零。

## <a name="remarks"></a>備註

回應 **WM \_ RENDERFORMAT** 訊息時，剪貼簿擁有者必須先開啟剪貼簿，然後再呼叫 [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata)。 在將資料放入資料以回應 **WM \_ RENDERFORMAT** 之前，不需要開啟剪貼簿，而任何開啟剪貼簿的嘗試都會失敗，因為剪貼簿目前正由要求轉譯格式的應用程式開啟。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata)
</dt> <dt>

[**WM \_ RENDERALLFORMATS**](wm-renderallformats.md)
</dt> <dt>

**概念**
</dt> <dt>

[剪貼簿](clipboard.md)
</dt> </dl>

 

 





