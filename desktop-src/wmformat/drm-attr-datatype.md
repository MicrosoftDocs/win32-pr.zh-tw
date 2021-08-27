---
title: 'DRM_ATTR_DATATYPE 列舉 (Wmdrmsdk .h) '
description: DRM \_ ATTR \_ DATATYPE 列舉定義用於 drm 屬性和屬性的資料類型。
ms.assetid: ccad16e2-475d-4cc7-b773-f17038d2754a
keywords:
- DRM_ATTR_DATATYPE 列舉 windows 媒體格式
- 列舉 windows 媒體格式
topic_type:
- apiref
api_name:
- DRM_ATTR_DATATYPE
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09f55c3d218aa86c33f699d4cb762e752a0bf4e1029e8ca42eee797aaf8ac721
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110528"
---
# <a name="drm_attr_datatype-enumeration"></a>DRM \_ ATTR \_ DATATYPE 列舉

**Drm \_ ATTR \_ DATATYPE** 列舉定義用於 drm 屬性和屬性的資料類型。

## <a name="syntax"></a>Syntax


```C++
typedef enum DRM_ATTR_DATATYPE { 
  DRM_TYPE_DWORD   = 0,
  DRM_TYPE_STRING  = 1,
  DRM_TYPE_BINARY  = 2,
  DRM_TYPE_BOOL    = 3,
  DRM_TYPE_QWORD   = 4,
  DRM_TYPE_WORD    = 5,
  DRM_TYPE_GUID    = 6
} ;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="DRM_TYPE_DWORD"></span><span id="drm_type_dword"></span>**DRM \_ 類型 \_ DWORD**
</dt> <dd>

屬性是4位元組的 **DWORD** 值。

</dd> <dt>

<span id="DRM_TYPE_STRING"></span><span id="drm_type_string"></span>**DRM \_ 類型 \_ 字串**
</dt> <dd>

屬性是以 null 結束的 Unicode 字串。

</dd> <dt>

<span id="DRM_TYPE_BINARY"></span><span id="drm_type_binary"></span>**DRM \_ 類型 \_ 二進位**
</dt> <dd>

屬性是位元組陣列。

</dd> <dt>

<span id="DRM_TYPE_BOOL"></span><span id="drm_type_bool"></span>**DRM \_ 類型 \_ BOOL**
</dt> <dd>

屬性是4位元組的布林值。

</dd> <dt>

<span id="DRM_TYPE_QWORD"></span><span id="drm_type_qword"></span>**DRM \_ 類型 \_ QWORD**
</dt> <dd>

屬性是8位元組的 **QWORD** 值。

</dd> <dt>

<span id="DRM_TYPE_WORD"></span><span id="drm_type_word"></span>**DRM \_ 類型 \_ WORD**
</dt> <dd>

屬性是2個位元組的 **文字** 值。

</dd> <dt>

<span id="DRM_TYPE_GUID"></span><span id="drm_type_guid"></span>**DRM \_ 類型 \_ GUID**
</dt> <dd>

屬性是128位 (6 位元組) GUID 值。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmdrmsdk。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**列舉類型**](drm-enumeration-types.md)
</dt> </dl>

 

 





