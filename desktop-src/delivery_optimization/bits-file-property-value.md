---
title: 'BITS_FILE_PROPERTY_VALUE 結構 (>deliveryoptimization .h) '
description: BITS_FILE_PROPERTY_VALUE 聯集會根據 BITS_FILE_PROPERTY_ID 列舉中的值，提供 DO 檔案的屬性值。
ms.assetid: 56A634F9-FB30-49D5-BD03-DD59AEF702C1
keywords:
- BITS_FILE_PROPERTY_VALUE 結構
topic_type:
- apiref
api_name:
- BITS_FILE_PROPERTY_VALUE
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 639ea0523c5b92d9764671cb573497223ef968fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966090"
---
# <a name="bits_file_property_value-structure"></a>BITS_FILE_PROPERTY_VALUE 結構

**BITS_FILE_PROPERTY_VALUE** 聯集會根據 [**BITS_FILE_PROPERTY_ID**](bits-file-property-id-.md)列舉中的值，提供 DO 檔案的屬性值。

## <a name="syntax"></a>語法


```C++
typedef struct {
  LPWSTR String;
} BITS_FILE_PROPERTY_VALUE;
```



## <a name="members"></a>成員

<dl> <dt>

**String**
</dt> <dd>

使用屬性識別碼列舉值 **BITS_FILE_PROPERTY_ID_HTTP_RESPONSE_HEADERS** 時，會使用這個值。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1709版桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | 僅限 Windows Server，版本 1709 \[ 桌面應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>>deliveryoptimization。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**BITS_FILE_PROPERTY_ID**](bits-file-property-id-.md)
</dt> <dt>

[**IBackgroundCopyFile5. GetProperty**](ibackgroundcopyfile5-getproperty.md)
</dt> <dt>

[**IBackgroundCopyFile5**](ibackgroundcopyfile5-setproperty.md)
</dt> </dl>

 

 





