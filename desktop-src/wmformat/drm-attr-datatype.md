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
ms.openlocfilehash: e684ba1c09a86c65a13adbd189bb185f65598b77
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979557"
---
# <a name="drm_attr_datatype-enumeration"></a><span data-ttu-id="dc8b4-105">DRM \_ ATTR \_ DATATYPE 列舉</span><span class="sxs-lookup"><span data-stu-id="dc8b4-105">DRM\_ATTR\_DATATYPE enumeration</span></span>

<span data-ttu-id="dc8b4-106">**Drm \_ ATTR \_ DATATYPE** 列舉定義用於 drm 屬性和屬性的資料類型。</span><span class="sxs-lookup"><span data-stu-id="dc8b4-106">The **DRM\_ATTR\_DATATYPE** enumeration defines the data types used for DRM attributes and properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc8b4-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="dc8b4-107">Syntax</span></span>


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



## <a name="constants"></a><span data-ttu-id="dc8b4-108">常數</span><span class="sxs-lookup"><span data-stu-id="dc8b4-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="dc8b4-109"><span id="DRM_TYPE_DWORD"></span><span id="drm_type_dword"></span>**DRM \_ 類型 \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="dc8b4-109"><span id="DRM_TYPE_DWORD"></span><span id="drm_type_dword"></span>**DRM\_TYPE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="dc8b4-110">屬性是4位元組的 **DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="dc8b4-110">The property is a 4-byte **DWORD** value.</span></span>

</dd> <dt>

<span data-ttu-id="dc8b4-111"><span id="DRM_TYPE_STRING"></span><span id="drm_type_string"></span>**DRM \_ 類型 \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="dc8b4-111"><span id="DRM_TYPE_STRING"></span><span id="drm_type_string"></span>**DRM\_TYPE\_STRING**</span></span>
</dt> <dd>

<span data-ttu-id="dc8b4-112">屬性是以 null 結束的 Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="dc8b4-112">The property is a null-terminated Unicode string.</span></span>

</dd> <dt>

<span data-ttu-id="dc8b4-113"><span id="DRM_TYPE_BINARY"></span><span id="drm_type_binary"></span>**DRM \_ 類型 \_ 二進位**</span><span class="sxs-lookup"><span data-stu-id="dc8b4-113"><span id="DRM_TYPE_BINARY"></span><span id="drm_type_binary"></span>**DRM\_TYPE\_BINARY**</span></span>
</dt> <dd>

<span data-ttu-id="dc8b4-114">屬性是位元組陣列。</span><span class="sxs-lookup"><span data-stu-id="dc8b4-114">The property is an array of bytes.</span></span>

</dd> <dt>

<span data-ttu-id="dc8b4-115"><span id="DRM_TYPE_BOOL"></span><span id="drm_type_bool"></span>**DRM \_ 類型 \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="dc8b4-115"><span id="DRM_TYPE_BOOL"></span><span id="drm_type_bool"></span>**DRM\_TYPE\_BOOL**</span></span>
</dt> <dd>

<span data-ttu-id="dc8b4-116">屬性是4位元組的布林值。</span><span class="sxs-lookup"><span data-stu-id="dc8b4-116">The property is a 4-byte Boolean value.</span></span>

</dd> <dt>

<span data-ttu-id="dc8b4-117"><span id="DRM_TYPE_QWORD"></span><span id="drm_type_qword"></span>**DRM \_ 類型 \_ QWORD**</span><span class="sxs-lookup"><span data-stu-id="dc8b4-117"><span id="DRM_TYPE_QWORD"></span><span id="drm_type_qword"></span>**DRM\_TYPE\_QWORD**</span></span>
</dt> <dd>

<span data-ttu-id="dc8b4-118">屬性是8位元組的 **QWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="dc8b4-118">The property is an 8-byte **QWORD** value.</span></span>

</dd> <dt>

<span data-ttu-id="dc8b4-119"><span id="DRM_TYPE_WORD"></span><span id="drm_type_word"></span>**DRM \_ 類型 \_ WORD**</span><span class="sxs-lookup"><span data-stu-id="dc8b4-119"><span id="DRM_TYPE_WORD"></span><span id="drm_type_word"></span>**DRM\_TYPE\_WORD**</span></span>
</dt> <dd>

<span data-ttu-id="dc8b4-120">屬性是2個位元組的 **文字** 值。</span><span class="sxs-lookup"><span data-stu-id="dc8b4-120">The property is a 2-byte **WORD** value.</span></span>

</dd> <dt>

<span data-ttu-id="dc8b4-121"><span id="DRM_TYPE_GUID"></span><span id="drm_type_guid"></span>**DRM \_ 類型 \_ GUID**</span><span class="sxs-lookup"><span data-stu-id="dc8b4-121"><span id="DRM_TYPE_GUID"></span><span id="drm_type_guid"></span>**DRM\_TYPE\_GUID**</span></span>
</dt> <dd>

<span data-ttu-id="dc8b4-122">屬性是128位 (6 位元組) GUID 值。</span><span class="sxs-lookup"><span data-stu-id="dc8b4-122">The property is a 128-bit (6-byte) GUID value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dc8b4-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="dc8b4-123">Requirements</span></span>



| <span data-ttu-id="dc8b4-124">需求</span><span class="sxs-lookup"><span data-stu-id="dc8b4-124">Requirement</span></span> | <span data-ttu-id="dc8b4-125">值</span><span class="sxs-lookup"><span data-stu-id="dc8b4-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dc8b4-126">標頭</span><span class="sxs-lookup"><span data-stu-id="dc8b4-126">Header</span></span><br/> | <dl> <span data-ttu-id="dc8b4-127"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="dc8b4-127"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc8b4-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dc8b4-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc8b4-129">**列舉類型**</span><span class="sxs-lookup"><span data-stu-id="dc8b4-129">**Enumeration Types**</span></span>](drm-enumeration-types.md)
</dt> </dl>

 

 





