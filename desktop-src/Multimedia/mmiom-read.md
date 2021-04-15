---
title: 'MMIOM_READ 訊息 (Mmsystem .h) '
description: MmioRead 函 \_ 式會將 MMIOM 讀取訊息傳送至 i/o 程式，以要求從開啟的檔案讀取指定的位元組數目。
ms.assetid: db769a68-f0ac-4a79-931e-6174e438439d
keywords:
- MMIOM_READ message Windows 多媒體
topic_type:
- apiref
api_name:
- MMIOM_READ
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5715bf8db51017c16997530256c6dfb83b3b3fc5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104467080"
---
# <a name="mmiom_read-message"></a>MMIOM \_ 讀取訊息

[**MmioRead**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioread)函式會將 **MMIOM \_ 讀取** 訊息傳送至 i/o 程式，以要求從開啟的檔案讀取指定的位元組數目。


```C++
MMIOM_READ 
lParam1 = (LPARAM) lBuffer 
lParam2 = (LPARAM) cbRead 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="lBuffer"></span><span id="lbuffer"></span><span id="LBUFFER"></span>*lBuffer*
</dt> <dd>

要填入從檔案讀取之資料的緩衝區指標。

</dd> <dt>

<span id="cbRead"></span><span id="cbread"></span><span id="CBREAD"></span>*cbRead*
</dt> <dd>

要從檔案讀取的位元組數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回實際從檔案讀取的位元組數目。 如果沒有更多的位元組可以讀取，則傳回值為0。 如果發生錯誤，則傳回值為1。

## <a name="remarks"></a>備註

I/o 程式負責更新 [**MMIOINFO**](/previous-versions//dd757322(v=vs.85))結構的 **lDiskOffset** 成員，以反映讀取作業之後的新檔案位置。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Mmsystem (包含) 的 Windows。h </dt> </dl> |



 

