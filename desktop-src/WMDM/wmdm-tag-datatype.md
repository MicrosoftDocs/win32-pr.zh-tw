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
# <a name="wmdm_tag_datatype-enumeration"></a><span data-ttu-id="8c2fe-104">WMDM \_ 標記 \_ DATATYPE 列舉</span><span class="sxs-lookup"><span data-stu-id="8c2fe-104">WMDM\_TAG\_DATATYPE enumeration</span></span>

<span data-ttu-id="8c2fe-105">**WMDM \_ 標記 \_ DATATYPE** 列舉型別會定義資料型別。</span><span class="sxs-lookup"><span data-stu-id="8c2fe-105">The **WMDM\_TAG\_DATATYPE** enumeration type defines a data type.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c2fe-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="8c2fe-106">Syntax</span></span>


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



## <a name="constants"></a><span data-ttu-id="8c2fe-107">常數</span><span class="sxs-lookup"><span data-stu-id="8c2fe-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="8c2fe-108"><span id="WMDM_TYPE_DWORD"></span><span id="wmdm_type_dword"></span>**WMDM \_ 類型 \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="8c2fe-108"><span id="WMDM_TYPE_DWORD"></span><span id="wmdm_type_dword"></span>**WMDM\_TYPE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="8c2fe-109">指定4位元組的 **DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="8c2fe-109">Specifies a 4-byte **DWORD** value.</span></span>

</dd> <dt>

<span data-ttu-id="8c2fe-110"><span id="WMDM_TYPE_STRING"></span><span id="wmdm_type_string"></span>**WMDM \_ 類型 \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="8c2fe-110"><span id="WMDM_TYPE_STRING"></span><span id="wmdm_type_string"></span>**WMDM\_TYPE\_STRING**</span></span>
</dt> <dd>

<span data-ttu-id="8c2fe-111">指定以 null 終止的 Unicode 字串，每個字元)  (2 個位元組。</span><span class="sxs-lookup"><span data-stu-id="8c2fe-111">Specifies a null-terminated Unicode string (2 bytes per character).</span></span>

</dd> <dt>

<span data-ttu-id="8c2fe-112"><span id="WMDM_TYPE_BINARY"></span><span id="wmdm_type_binary"></span>**WMDM \_ 類型 \_ 二進位**</span><span class="sxs-lookup"><span data-stu-id="8c2fe-112"><span id="WMDM_TYPE_BINARY"></span><span id="wmdm_type_binary"></span>**WMDM\_TYPE\_BINARY**</span></span>
</dt> <dd>

<span data-ttu-id="8c2fe-113">指定位元組陣列。</span><span class="sxs-lookup"><span data-stu-id="8c2fe-113">Specifies an array of bytes.</span></span>

</dd> <dt>

<span data-ttu-id="8c2fe-114"><span id="WMDM_TYPE_BOOL"></span><span id="wmdm_type_bool"></span>**WMDM \_ 類型 \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="8c2fe-114"><span id="WMDM_TYPE_BOOL"></span><span id="wmdm_type_bool"></span>**WMDM\_TYPE\_BOOL**</span></span>
</dt> <dd>

<span data-ttu-id="8c2fe-115">指定4位元組布林值。</span><span class="sxs-lookup"><span data-stu-id="8c2fe-115">Specifies a 4-byte Boolean value.</span></span>

</dd> <dt>

<span data-ttu-id="8c2fe-116"><span id="WMDM_TYPE_QWORD"></span><span id="wmdm_type_qword"></span>**WMDM \_ 類型 \_ QWORD**</span><span class="sxs-lookup"><span data-stu-id="8c2fe-116"><span id="WMDM_TYPE_QWORD"></span><span id="wmdm_type_qword"></span>**WMDM\_TYPE\_QWORD**</span></span>
</dt> <dd>

<span data-ttu-id="8c2fe-117">指定8位元組的 **QWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="8c2fe-117">Specifies an 8-byte **QWORD** value.</span></span>

</dd> <dt>

<span data-ttu-id="8c2fe-118"><span id="WMDM_TYPE_WORD"></span><span id="wmdm_type_word"></span>**WMDM \_ 類型 \_ 文字**</span><span class="sxs-lookup"><span data-stu-id="8c2fe-118"><span id="WMDM_TYPE_WORD"></span><span id="wmdm_type_word"></span>**WMDM\_TYPE\_WORD**</span></span>
</dt> <dd>

<span data-ttu-id="8c2fe-119">指定2個位元組的 **文字** 值。</span><span class="sxs-lookup"><span data-stu-id="8c2fe-119">Specifies a 2-byte **WORD** value.</span></span>

</dd> <dt>

<span data-ttu-id="8c2fe-120"><span id="WMDM_TYPE_GUID"></span><span id="wmdm_type_guid"></span>**WMDM \_ 類型 \_ GUID**</span><span class="sxs-lookup"><span data-stu-id="8c2fe-120"><span id="WMDM_TYPE_GUID"></span><span id="wmdm_type_guid"></span>**WMDM\_TYPE\_GUID**</span></span>
</dt> <dd>

<span data-ttu-id="8c2fe-121">指定128位 (16 位元組) GUID。</span><span class="sxs-lookup"><span data-stu-id="8c2fe-121">Specifies a 128-bit (16-byte) GUID.</span></span>

</dd> <dt>

<span data-ttu-id="8c2fe-122"><span id="WMDM_TYPE_DATE"></span><span id="wmdm_type_date"></span>**WMDM \_ 類型 \_ 日期**</span><span class="sxs-lookup"><span data-stu-id="8c2fe-122"><span id="WMDM_TYPE_DATE"></span><span id="wmdm_type_date"></span>**WMDM\_TYPE\_DATE**</span></span>
</dt> <dd>

<span data-ttu-id="8c2fe-123">指定日期。</span><span class="sxs-lookup"><span data-stu-id="8c2fe-123">Specifies a date.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8c2fe-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="8c2fe-124">Requirements</span></span>



| <span data-ttu-id="8c2fe-125">需求</span><span class="sxs-lookup"><span data-stu-id="8c2fe-125">Requirement</span></span> | <span data-ttu-id="8c2fe-126">值</span><span class="sxs-lookup"><span data-stu-id="8c2fe-126">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8c2fe-127">標頭</span><span class="sxs-lookup"><span data-stu-id="8c2fe-127">Header</span></span><br/> | <dl> <span data-ttu-id="8c2fe-128"><dt>Wmdm .idl</dt></span><span class="sxs-lookup"><span data-stu-id="8c2fe-128"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c2fe-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8c2fe-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c2fe-130">**列舉類型**</span><span class="sxs-lookup"><span data-stu-id="8c2fe-130">**Enumeration Types**</span></span>](enumeration-types.md)
</dt> </dl>

 

 





