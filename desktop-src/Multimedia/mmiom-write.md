---
title: 'MMIOM_WRITE 訊息 (Mmsystem .h) '
description: MmioWrite 函 \_ 式會將 MMIOM 寫入訊息傳送至 i/o 程式，以要求將資料寫入至開啟的檔案。
ms.assetid: 46e2dd9a-c4a7-4c99-86e4-a67b424411d1
keywords:
- MMIOM_WRITE message Windows 多媒體
topic_type:
- apiref
api_name:
- MMIOM_WRITE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c27cf96827f803608c369cc9022faa6235add9ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934993"
---
# <a name="mmiom_write-message"></a>MMIOM \_ 寫入訊息

[**MmioWrite**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite)函式會將 **MMIOM \_ 寫入** 訊息傳送至 i/o 程式，以要求將資料寫入至開啟的檔案。


```C++
MMIOM_WRITE 
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

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Mmsystem (包含) 的 Windows。h </dt> </dl> |



 

