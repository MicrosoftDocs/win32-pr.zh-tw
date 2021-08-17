---
description: 定義對應至類別識別碼的方式。
ms.assetid: 1af170e3-1edd-411f-acba-d4b244107996
title: TYSPEC 列舉
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TYSPEC
api_type:
- IDLDef
api_location:
- Wtypes.idl
ms.openlocfilehash: 15e7ecdc06495c0fa68b2949ae159bbc76b8cababd2b8703d3ebbdebb874399b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075752"
---
# <a name="tyspec-enumeration"></a>TYSPEC 列舉

定義對應至類別識別碼的方式。

## <a name="syntax"></a>Syntax


```C++
typedef enum tagTYSPEC { 
  TYSPEC_CLSID,
  TYSPEC_FILEEXT,
  TYSPEC_MIMETYPE,
  TYSPEC_FILENAME,
  TYSPEC_PROGID,
  TYSPEC_PACKAGENAME,
  TYSPEC_OBJECTID
} TYSPEC;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="TYSPEC_CLSID"></span><span id="tyspec_clsid"></span>**TYSPEC \_ CLSID**
</dt> <dd>

CLSID。

</dd> <dt>

<span id="TYSPEC_FILEEXT"></span><span id="tyspec_fileext"></span>**TYSPEC \_ FILEEXT**
</dt> <dd>

副檔名。 目前不支援此值。

</dd> <dt>

<span id="TYSPEC_MIMETYPE"></span><span id="tyspec_mimetype"></span>**TYSPEC \_ MIMETYPE**
</dt> <dd>

MIME 類型。 目前不支援此值。

</dd> <dt>

<span id="TYSPEC_FILENAME"></span><span id="tyspec_filename"></span>**TYSPEC \_ 檔案名**
</dt> <dd>

檔案名稱。 目前不支援此值。

</dd> <dt>

<span id="TYSPEC_PROGID"></span><span id="tyspec_progid"></span>**TYSPEC \_ PROGID**
</dt> <dd>

PROGID。 目前不支援此值。

</dd> <dt>

<span id="TYSPEC_PACKAGENAME"></span><span id="tyspec_packagename"></span>**TYSPEC \_ PACKAGENAME**
</dt> <dd>

封裝名稱。 目前不支援此值。

</dd> <dt>

<span id="TYSPEC_OBJECTID"></span><span id="tyspec_objectid"></span>**TYSPEC \_ OBJECTID**
</dt> <dd>

物件識別碼。 目前不支援此值。

</dd> </dl>

## <a name="remarks"></a>備註

**UCLSSPEC** 聯集的定義如下：

``` syntax
typedef union switch(DWORD tyspec) {
    case TYSPEC_CLSID:
        CLSID clsid;
    case TYSPEC_FILEEXT:
        LPOLESTR pFileExt;
    case TYSPEC_MIMETYPE:
        LPOLESTR pMimeType;
    case TYSPEC_PROGID:
        LPOLESTR pProgId;
    case TYSPEC_FILENAME:
        LPOLESTR pFileName;
    case TYSPEC_PACKAGENAME:
        struct {
        LPOLESTR pPackageName;
        GUID PolicyId;
        } ByName;
    case TYSPEC_OBJECTID:
        struct {
        GUID ObjectId;
        GUID PolicyId;
        } ByObjectId;
} uCLSSPEC;
```

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|---------------------------------------------------------------------------------------|
| IDL<br/> | <dl> <dt>Wtypes.h .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CoInstall**](/windows/win32/api/objbase/nf-objbase-coinstall)
</dt> </dl>

 

 
