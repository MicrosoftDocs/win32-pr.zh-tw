---
title: 'BG_FILE_RANGE 結構 (>deliveryoptimization .h) '
description: BG_FILE_RANGE 結構會識別要從檔案下載的位元組範圍。
ms.assetid: 58993C51-E42E-4E44-9E8A-15E982B25413
keywords:
- BG_FILE_RANGE 結構
topic_type:
- apiref
api_name:
- BG_FILE_RANGE
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cedabfb066a5905adb2ed8eac9996fd77c0e12be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385093"
---
# <a name="bg_file_range-structure"></a>BG_FILE_RANGE 結構

**BG_FILE_RANGE** 結構會識別要從檔案下載的位元組範圍。

## <a name="syntax"></a>語法


```C++
typedef struct {
  UINT64 InitialOffset;
  UINT64 Length;
} BG_FILE_RANGE;
```



## <a name="members"></a>成員

<dl> <dt>

**InitialOffset**
</dt> <dd>

從檔案下載的位元組範圍開頭以零為基底的位移。

</dd> <dt>

**長度**
</dt> <dd>

範圍的長度（以位元組為單位）。 請勿指定零位元組長度。 若要指出範圍延伸至檔案結尾，請指定 **BG_LENGTH_TO_EOF**。

</dd> </dl>

## <a name="remarks"></a>備註

範圍必須存在於檔案中，否則會產生 **DO_E_INVALID_RANGE** 錯誤。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1709版桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | 僅限 Windows Server，版本 1709 \[ 桌面應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>>deliveryoptimization。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IBackgroundCopyFile2::GetFileRanges**](ibackgroundcopyfile2-getfileranges-method.md)
</dt> </dl>

 

 





