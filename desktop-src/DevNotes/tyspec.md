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
ms.openlocfilehash: b4c8cf38a8f99458e76cabc726aa39ad01a71ebc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106974931"
---
# <a name="tyspec-enumeration"></a><span data-ttu-id="6136b-103">TYSPEC 列舉</span><span class="sxs-lookup"><span data-stu-id="6136b-103">TYSPEC enumeration</span></span>

<span data-ttu-id="6136b-104">定義對應至類別識別碼的方式。</span><span class="sxs-lookup"><span data-stu-id="6136b-104">Defines ways of mapping to a class ID.</span></span>

## <a name="syntax"></a><span data-ttu-id="6136b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6136b-105">Syntax</span></span>


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



## <a name="constants"></a><span data-ttu-id="6136b-106">常數</span><span class="sxs-lookup"><span data-stu-id="6136b-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="6136b-107"><span id="TYSPEC_CLSID"></span><span id="tyspec_clsid"></span>**TYSPEC \_ CLSID**</span><span class="sxs-lookup"><span data-stu-id="6136b-107"><span id="TYSPEC_CLSID"></span><span id="tyspec_clsid"></span>**TYSPEC\_CLSID**</span></span>
</dt> <dd>

<span data-ttu-id="6136b-108">CLSID。</span><span class="sxs-lookup"><span data-stu-id="6136b-108">A CLSID.</span></span>

</dd> <dt>

<span data-ttu-id="6136b-109"><span id="TYSPEC_FILEEXT"></span><span id="tyspec_fileext"></span>**TYSPEC \_ FILEEXT**</span><span class="sxs-lookup"><span data-stu-id="6136b-109"><span id="TYSPEC_FILEEXT"></span><span id="tyspec_fileext"></span>**TYSPEC\_FILEEXT**</span></span>
</dt> <dd>

<span data-ttu-id="6136b-110">副檔名。</span><span class="sxs-lookup"><span data-stu-id="6136b-110">A file name extension.</span></span> <span data-ttu-id="6136b-111">目前不支援此值。</span><span class="sxs-lookup"><span data-stu-id="6136b-111">This value is not currently supported.</span></span>

</dd> <dt>

<span data-ttu-id="6136b-112"><span id="TYSPEC_MIMETYPE"></span><span id="tyspec_mimetype"></span>**TYSPEC \_ MIMETYPE**</span><span class="sxs-lookup"><span data-stu-id="6136b-112"><span id="TYSPEC_MIMETYPE"></span><span id="tyspec_mimetype"></span>**TYSPEC\_MIMETYPE**</span></span>
</dt> <dd>

<span data-ttu-id="6136b-113">MIME 類型。</span><span class="sxs-lookup"><span data-stu-id="6136b-113">A MIME type.</span></span> <span data-ttu-id="6136b-114">目前不支援此值。</span><span class="sxs-lookup"><span data-stu-id="6136b-114">This value is not currently supported.</span></span>

</dd> <dt>

<span data-ttu-id="6136b-115"><span id="TYSPEC_FILENAME"></span><span id="tyspec_filename"></span>**TYSPEC \_ 檔案名**</span><span class="sxs-lookup"><span data-stu-id="6136b-115"><span id="TYSPEC_FILENAME"></span><span id="tyspec_filename"></span>**TYSPEC\_FILENAME**</span></span>
</dt> <dd>

<span data-ttu-id="6136b-116">檔案名稱。</span><span class="sxs-lookup"><span data-stu-id="6136b-116">A file name.</span></span> <span data-ttu-id="6136b-117">目前不支援此值。</span><span class="sxs-lookup"><span data-stu-id="6136b-117">This value is not currently supported.</span></span>

</dd> <dt>

<span data-ttu-id="6136b-118"><span id="TYSPEC_PROGID"></span><span id="tyspec_progid"></span>**TYSPEC \_ PROGID**</span><span class="sxs-lookup"><span data-stu-id="6136b-118"><span id="TYSPEC_PROGID"></span><span id="tyspec_progid"></span>**TYSPEC\_PROGID**</span></span>
</dt> <dd>

<span data-ttu-id="6136b-119">PROGID。</span><span class="sxs-lookup"><span data-stu-id="6136b-119">A PROGID.</span></span> <span data-ttu-id="6136b-120">目前不支援此值。</span><span class="sxs-lookup"><span data-stu-id="6136b-120">This value is not currently supported.</span></span>

</dd> <dt>

<span data-ttu-id="6136b-121"><span id="TYSPEC_PACKAGENAME"></span><span id="tyspec_packagename"></span>**TYSPEC \_ PACKAGENAME**</span><span class="sxs-lookup"><span data-stu-id="6136b-121"><span id="TYSPEC_PACKAGENAME"></span><span id="tyspec_packagename"></span>**TYSPEC\_PACKAGENAME**</span></span>
</dt> <dd>

<span data-ttu-id="6136b-122">封裝名稱。</span><span class="sxs-lookup"><span data-stu-id="6136b-122">A package name.</span></span> <span data-ttu-id="6136b-123">目前不支援此值。</span><span class="sxs-lookup"><span data-stu-id="6136b-123">This value is not currently supported.</span></span>

</dd> <dt>

<span data-ttu-id="6136b-124"><span id="TYSPEC_OBJECTID"></span><span id="tyspec_objectid"></span>**TYSPEC \_ OBJECTID**</span><span class="sxs-lookup"><span data-stu-id="6136b-124"><span id="TYSPEC_OBJECTID"></span><span id="tyspec_objectid"></span>**TYSPEC\_OBJECTID**</span></span>
</dt> <dd>

<span data-ttu-id="6136b-125">物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="6136b-125">An object ID.</span></span> <span data-ttu-id="6136b-126">目前不支援此值。</span><span class="sxs-lookup"><span data-stu-id="6136b-126">This value is not currently supported.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6136b-127">備註</span><span class="sxs-lookup"><span data-stu-id="6136b-127">Remarks</span></span>

<span data-ttu-id="6136b-128">**UCLSSPEC** 聯集的定義如下：</span><span class="sxs-lookup"><span data-stu-id="6136b-128">The **uCLSSPEC** union is defined as follows:</span></span>

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

## <a name="requirements"></a><span data-ttu-id="6136b-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="6136b-129">Requirements</span></span>



| <span data-ttu-id="6136b-130">需求</span><span class="sxs-lookup"><span data-stu-id="6136b-130">Requirement</span></span> | <span data-ttu-id="6136b-131">值</span><span class="sxs-lookup"><span data-stu-id="6136b-131">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6136b-132">Idl</span><span class="sxs-lookup"><span data-stu-id="6136b-132">IDL</span></span><br/> | <dl> <span data-ttu-id="6136b-133"><dt>Wtypes.h .idl</dt></span><span class="sxs-lookup"><span data-stu-id="6136b-133"><dt>Wtypes.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6136b-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6136b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6136b-135">**CoInstall**</span><span class="sxs-lookup"><span data-stu-id="6136b-135">**CoInstall**</span></span>](/windows/win32/api/objbase/nf-objbase-coinstall)
</dt> </dl>

 

 
