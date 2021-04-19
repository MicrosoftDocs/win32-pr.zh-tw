---
title: 'MMIOM_SEEK 訊息 (Mmsystem .h) '
description: '\_MmioSeek 函數會將 MMIOM 搜尋訊息傳送至 i/o 程式，以要求移動目前的檔案位置。'
ms.assetid: 428b231a-6e00-4458-9ba2-e9b0b028843a
keywords:
- MMIOM_SEEK message Windows 多媒體
topic_type:
- apiref
api_name:
- MMIOM_SEEK
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4855ec4e610f1456e1bf26ee05800e31933f05fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967761"
---
# <a name="mmiom_seek-message"></a>MMIOM \_ 搜尋訊息

[**MmioSeek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek)函數會將 **MMIOM \_ 搜尋** 訊息傳送至 i/o 程式，以要求移動目前的檔案位置。


```C++
MMIOM_SEEK 
lParam1 = (LPARAM) lNewFilePos 
lParam2 = (LPARAM) lChangeFlag 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="lNewFilePos"></span><span id="lnewfilepos"></span><span id="LNEWFILEPOS"></span>*lNewFilePos*
</dt> <dd>

新檔案位置。 此值的意義取決於在 **lChangeFlag** 中指定的旗標。

</dd> <dt>

<span id="lChangeFlag"></span><span id="lchangeflag"></span><span id="LCHANGEFLAG"></span>*lChangeFlag*
</dt> <dd>

指定檔案位置變更方式的旗標。 系統會定義下列值：



| 需求 | 值 |
|-----------|------------------------------------------------------------------------------------------------------------------------|
| 搜尋到 \_ 當前 | 將檔案位置從目前的位置移至 *lNewFilePos* 的位元組。 *lNewFilePos* 可以是正數或負數。 |
| 搜尋 \_ 結束 | 將檔案位置從檔案結尾移到 *lNewFilePos* 的位元組。                                             |
| 搜尋 \_ 集 | 將檔案位置從檔案的開頭移動到 *lNewFilePos* 的位元組。                                       |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回新的檔案位置。 如果發生錯誤，則傳回值為1。

## <a name="remarks"></a>備註

I/o 程式負責維護 [**MMIOINFO**](/previous-versions//dd757322(v=vs.85))結構之 **lDiskOffset** 成員中的目前檔案位置。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Mmsystem (包含) 的 Windows。h </dt> </dl> |



 

