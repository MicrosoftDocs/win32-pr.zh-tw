---
title: 'MMIOM_WRITEFLUSH 訊息 (Mmsystem .h) '
description: MmioWrite 函 \_ 式會將 MMIOM WRITEFLUSH 訊息傳送至 i/o 程式，要求將該資料寫入至開啟的檔案，而且 i/o 程式所使用的任何內部緩衝區都會排清至磁片。
ms.assetid: e04acaef-9584-410c-a020-af09fb888490
keywords:
- MMIOM_WRITEFLUSH 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- MMIOM_WRITEFLUSH
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b274536e934f426ef5e545e758c2f7bf918d552c42085650fc7c81a6a47c842e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807088"
---
# <a name="mmiom_writeflush-message"></a>MMIOM \_ WRITEFLUSH 訊息

[**MmioWrite**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite)函式會將 **MMIOM \_ WRITEFLUSH** 訊息傳送至 i/o 程式，要求將該資料寫入至開啟的檔案，而且 i/o 程式所使用的任何內部緩衝區都會排清至磁片。


```C++
MMIOM_WRITEFLUSH 
lParam1 = (LPARAM) lpBuffer 
lParam2 = (LPARAM) cbWrite 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="lpBuffer"></span><span id="lpbuffer"></span><span id="LPBUFFER"></span>*lpBuffer*
</dt> <dd>

緩衝區的指標，其中包含要寫入檔案的資料。

</dd> <dt>

<span id="cbWrite"></span><span id="cbwrite"></span><span id="CBWRITE"></span>*cbWrite*
</dt> <dd>

要寫入檔案的位元組數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回實際寫入檔案的位元組數目。 如果發生錯誤，則傳回值為1。

## <a name="remarks"></a>備註

I/o 程式負責更新 [**MMIOINFO**](/previous-versions//dd757322(v=vs.85))結構的 **lDiskOffset** 成員，以反映寫入作業之後的新檔案位置。

這則訊息相當於 [**MMIOM \_ 寫入**](mmiom-write.md) 訊息，不同之處在于它會要求 i/o 程式排清其內部緩衝區（如果有的話）。 除非 i/o 程式執行內部緩衝處理，否則此訊息可以像 **MMIOM \_ 寫入** 訊息一樣處理。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Mmsystem (包含 Windows .h) </dt> </dl> |



 

