---
title: 'MMIOM_CLOSE 訊息 (Mmsystem .h) '
description: MmioClose 函 \_ 式會將 MMIOM CLOSE 訊息傳送至 i/o 程式，以要求關閉檔案。
ms.assetid: 9d0dad5b-fd0a-4948-a4cf-9d138e353c76
keywords:
- MMIOM_CLOSE 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- MMIOM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17a26b8b2ffa80c7c522fa5cdcbfc5da3334e0d2b5e258e090932147bf85438c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065388"
---
# <a name="mmiom_close-message"></a>MMIOM \_ 關閉訊息

[**MmioClose**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose)函式會將 **MMIOM \_ CLOSE** 訊息傳送至 i/o 程式，以要求關閉檔案。


```C++
MMIOM_CLOSE 
lParam1 = (LPARAM) lCloseFlags 
lParam2 = reserved 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="lCloseFlags"></span><span id="lcloseflags"></span><span id="LCLOSEFLAGS"></span>*lCloseFlags*
</dt> <dd>

**MmioClose** 的 **wFlags** 參數中所包含的旗標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果檔案已成功關閉，則傳回零，否則會傳回錯誤。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Mmsystem (包含 Windows .h) </dt> </dl> |



 

