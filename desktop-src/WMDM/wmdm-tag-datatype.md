---
title: WMDM_TAG_DATATYPE 列舉
description: WMDM \_ 標記 \_ DATATYPE 列舉型別會定義資料型別。
ms.assetid: 9c300814-5610-4e46-b441-e7f2fc78a47b
keywords:
- WMDM_TAG_DATATYPE 列舉 windows Media 裝置管理員
topic_type:
- apiref
api_name:
- WMDM_TAG_DATATYPE
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ad04f0d220809f6bd13d8ae29cc36d52ff6e599
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978605"
---
# <a name="wmdm_tag_datatype-enumeration"></a>WMDM \_ 標記 \_ DATATYPE 列舉

**WMDM \_ 標記 \_ DATATYPE** 列舉型別會定義資料型別。

## <a name="syntax"></a>Syntax


```C++
typedef enum tagWMDM_TAG_DATATYPE { 
  WMDM_TYPE_DWORD,
  WMDM_TYPE_STRING,
  WMDM_TYPE_BINARY,
  WMDM_TYPE_BOOL,
  WMDM_TYPE_QWORD,
  WMDM_TYPE_WORD,
  WMDM_TYPE_GUID,
  WMDM_TYPE_DATE
} WMDM_TAG_DATATYPE;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="WMDM_TYPE_DWORD"></span><span id="wmdm_type_dword"></span>**WMDM \_ 類型 \_ DWORD**
</dt> <dd>

指定4位元組的 **DWORD** 值。

</dd> <dt>

<span id="WMDM_TYPE_STRING"></span><span id="wmdm_type_string"></span>**WMDM \_ 類型 \_ 字串**
</dt> <dd>

指定以 null 終止的 Unicode 字串，每個字元)  (2 個位元組。

</dd> <dt>

<span id="WMDM_TYPE_BINARY"></span><span id="wmdm_type_binary"></span>**WMDM \_ 類型 \_ 二進位**
</dt> <dd>

指定位元組陣列。

</dd> <dt>

<span id="WMDM_TYPE_BOOL"></span><span id="wmdm_type_bool"></span>**WMDM \_ 類型 \_ BOOL**
</dt> <dd>

指定4位元組布林值。

</dd> <dt>

<span id="WMDM_TYPE_QWORD"></span><span id="wmdm_type_qword"></span>**WMDM \_ 類型 \_ QWORD**
</dt> <dd>

指定8位元組的 **QWORD** 值。

</dd> <dt>

<span id="WMDM_TYPE_WORD"></span><span id="wmdm_type_word"></span>**WMDM \_ 類型 \_ 文字**
</dt> <dd>

指定2個位元組的 **文字** 值。

</dd> <dt>

<span id="WMDM_TYPE_GUID"></span><span id="wmdm_type_guid"></span>**WMDM \_ 類型 \_ GUID**
</dt> <dd>

指定128位 (16 位元組) GUID。

</dd> <dt>

<span id="WMDM_TYPE_DATE"></span><span id="wmdm_type_date"></span>**WMDM \_ 類型 \_ 日期**
</dt> <dd>

指定日期。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmdm .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**列舉類型**](enumeration-types.md)
</dt> </dl>

 

 





