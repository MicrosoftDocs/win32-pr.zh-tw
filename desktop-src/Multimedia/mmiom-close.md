---
title: 'MMIOM_CLOSE 訊息 (Mmsystem .h) '
description: MmioClose 函 \_ 式會將 MMIOM CLOSE 訊息傳送至 i/o 程式，以要求關閉檔案。
ms.assetid: 9d0dad5b-fd0a-4948-a4cf-9d138e353c76
keywords:
- MMIOM_CLOSE message Windows 多媒體
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
ms.openlocfilehash: c7863698b99bcead8bc22e6194d213bbc663d5ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509486"
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
| 標頭<br/>                   | <dl> <dt>Mmsystem (包含) 的 Windows。h </dt> </dl> |



 

