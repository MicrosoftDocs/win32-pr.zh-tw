---
title: 'BITS_JOB_PROPERTY_VALUE 結構 (>deliveryoptimization .h) '
description: BITS_JOB_PROPERTY_VALUE 聯集會根據 BITS_JOB_PROPERTY_ID 列舉值，提供 DO 作業的屬性值。
ms.assetid: C24D9EA1-2E72-4403-939A-7B01D7133FE7
keywords:
- BITS_JOB_PROPERTY_VALUE 結構
- BITS_JOB_PROPERTY_VALUE 結構
topic_type:
- apiref
api_name:
- BITS_JOB_PROPERTY_VALUE
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c48c1fe550db51b6b838379d44df21c95fa95e41
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103662"
---
# <a name="bits_job_property_value-structure"></a>BITS_JOB_PROPERTY_VALUE 結構

**BITS_JOB_PROPERTY_VALUE** 聯集會根據 [**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md)列舉值，提供 DO 作業的屬性值。

## <a name="syntax"></a>語法


```C++
typedef struct {
  DWORD          Dword;
  GUID           ClsID;
  BOOL           Enable;
  UINT64         Uint64;
  BG_AUTH_TARGET Target;
} BITS_JOB_PROPERTY_VALUE;
```



## <a name="members"></a>成員

<dl> <dt>

**Dword**
</dt> <dd>

使用列舉屬性識別碼 **BITS_JOB_PROPERTY_ID_COST_FLAGS** 時，會傳回這個值，並套用為 DO 作業的 [傳輸原則](https://www.bing.com/search?q=transfer+policy) 。

</dd> <dt>

**Clsid**
</dt> <dd>

使用列舉屬性識別碼 **BITS_JOB_PROPERTY_NOTIFICATION_CLSID** 時，會傳回這個值，並表示要向 DO 作業註冊的回呼物件的 CLSID。

</dd> <dt>

**啟用**
</dt> <dd>

不支援。

</dd> <dt>

**Uint64**
</dt> <dd>

不支援。

</dd> <dt>

**Target**
</dt> <dd>

不支援。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1709版桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | 僅限 Windows Server，版本 1709 \[ 桌面應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>>deliveryoptimization。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md)
</dt> <dt>

[**BITS_JOB_TRANSFER_POLICY**](bits-job-transfer-policy-.md)
</dt> </dl>

 

 





