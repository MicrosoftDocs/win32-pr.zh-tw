---
title: 'MMIOM_RENAME 訊息 (Mmsystem .h) '
description: MmioRename 函 \_ 式會將 MMIOM 重新命名訊息傳送至 i/o 程式，以要求重新命名指定的檔案。
ms.assetid: 38a746c8-3a6f-4cb2-a5b4-c11bd1e73c8a
keywords:
- MMIOM_RENAME 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- MMIOM_RENAME
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcfd90b53f1cc42030bd00e6553d52de0f036ff274b3d4ff942c48667e4347b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065308"
---
# <a name="mmiom_rename-message"></a>MMIOM \_ 重新命名訊息

[**MmioRename**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiorename)函式會將 **MMIOM \_ 重新命名** 訊息傳送至 I/o 程式，以要求重新命名指定的檔案。


```C++
MMIOM_RENAME 
lParam1 = (LPARAM) lpszOldFilename 
lParam2 = (LPARAM) lpszNewFilename 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="lpszOldFilename"></span><span id="lpszoldfilename"></span><span id="LPSZOLDFILENAME"></span>*lpszOldFilename*
</dt> <dd>

字串的指標，其中包含要重新命名的檔案名。

</dd> <dt>

<span id="lpszNewFilename"></span><span id="lpsznewfilename"></span><span id="LPSZNEWFILENAME"></span>*lpszNewFilename*
</dt> <dd>

包含新檔案名之字串的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果檔案已成功重新命名，則傳回值為零。 如果找不到指定的檔案，則傳回值為 MMIOERR \_ FILENOTFOUND。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Mmsystem (包含 Windows .h) </dt> </dl> |



 

