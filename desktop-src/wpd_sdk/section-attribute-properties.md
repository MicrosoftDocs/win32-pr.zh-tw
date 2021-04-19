---
description: Windows 可攜式裝置支援下列區段資料屬性。
ms.assetid: 8760d963-fc07-4b54-aa24-5725f4b95ed2
title: '區段屬性屬性 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Section
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 383e2e50aa5d2a922ad50609e316b3dc9905cc38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999495"
---
# <a name="section-attribute-properties"></a><span data-ttu-id="51149-103">區段屬性屬性</span><span class="sxs-lookup"><span data-stu-id="51149-103">Section Attribute Properties</span></span>

<span data-ttu-id="51149-104">Windows 可攜式裝置支援下列區段資料屬性。</span><span class="sxs-lookup"><span data-stu-id="51149-104">Windows Portable Devices supports the following section data properties.</span></span>



| <span data-ttu-id="51149-105">屬性</span><span class="sxs-lookup"><span data-stu-id="51149-105">Property</span></span>                                             | <span data-ttu-id="51149-106">VarType</span><span class="sxs-lookup"><span data-stu-id="51149-106">VarType</span></span>         | <span data-ttu-id="51149-107">Description</span><span class="sxs-lookup"><span data-stu-id="51149-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51149-108">**WPD \_ 區段 \_ 資料 \_ 長度**</span><span class="sxs-lookup"><span data-stu-id="51149-108">**WPD\_SECTION\_DATA\_LENGTH**</span></span>                       | <span data-ttu-id="51149-109">**VT \_ UI8**</span><span class="sxs-lookup"><span data-stu-id="51149-109">**VT\_UI8**</span></span>     | <span data-ttu-id="51149-110">指定所參考物件的長度。</span><span class="sxs-lookup"><span data-stu-id="51149-110">Specifies the length of the referenced object.</span></span>                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="51149-111">**WPD \_ 區段 \_ 資料 \_ 位移**</span><span class="sxs-lookup"><span data-stu-id="51149-111">**WPD\_SECTION\_DATA\_OFFSET**</span></span>                       | <span data-ttu-id="51149-112">**VT \_ UI8**</span><span class="sxs-lookup"><span data-stu-id="51149-112">**VT\_UI8**</span></span>     | <span data-ttu-id="51149-113">指定所參考物件之資料的以零為基底的位移。</span><span class="sxs-lookup"><span data-stu-id="51149-113">Specifies the zero-based offset of the data for the referenced object.</span></span>                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="51149-114">**WPD \_ 區段 \_ 資料 \_ 參考的 \_ 物件 \_ 資源**</span><span class="sxs-lookup"><span data-stu-id="51149-114">**WPD\_SECTION\_DATA\_REFERENCED\_OBJECT\_RESOURCE**</span></span> | <span data-ttu-id="51149-115">**VT \_ 不明**</span><span class="sxs-lookup"><span data-stu-id="51149-115">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="51149-116">[**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) ，其中包含指定指定資源之索引鍵的單一值。此資源是 WPD \_ 區段 \_ 資料 \_ 位移和 WPD \_ 區段 \_ 資料 \_ 長度所參考的物件。</span><span class="sxs-lookup"><span data-stu-id="51149-116">An [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) containing a single value that specifies the key for a given resource.This resource is the object referenced by WPD\_SECTION\_DATA\_OFFSET and WPD\_SECTION\_DATA\_LENGTH.</span></span><br/> <span data-ttu-id="51149-117">如果這個屬性不存在， \_ \_ 則會假設為 WPD 資源預設值。</span><span class="sxs-lookup"><span data-stu-id="51149-117">If this property doesn't exist, WPD\_RESOURCE\_DEFAULT is assumed.</span></span><br/> |
| <span data-ttu-id="51149-118">**WPD \_ 區段 \_ 資料 \_ 單位**</span><span class="sxs-lookup"><span data-stu-id="51149-118">**WPD\_SECTION\_DATA\_UNITS**</span></span>                        | <span data-ttu-id="51149-119">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="51149-119">**VT\_UI4**</span></span>     | <span data-ttu-id="51149-120">指定用於此位移的單位，例如位元組、毫秒等等。這個屬性的可能值定義于 PortableDevice 檔案中的 **WPD \_ 區段 \_ 資料 \_ 單位 \_ 值** 列舉。</span><span class="sxs-lookup"><span data-stu-id="51149-120">Specifies the units used for this offset, for example, bytes, milliseconds, and so on.The possible values for this property are defined in the **WPD\_SECTION\_DATA\_UNITS\_VALUES** enumeration in the file PortableDevice.h.</span></span><br/> <span data-ttu-id="51149-121">如果未指定任何單位，則會假設為 bytes。</span><span class="sxs-lookup"><span data-stu-id="51149-121">If no units are specified, bytes are assumed.</span></span><br/>                                          |



 

## <a name="requirements"></a><span data-ttu-id="51149-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="51149-122">Requirements</span></span>



| <span data-ttu-id="51149-123">需求</span><span class="sxs-lookup"><span data-stu-id="51149-123">Requirement</span></span> | <span data-ttu-id="51149-124">值</span><span class="sxs-lookup"><span data-stu-id="51149-124">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="51149-125">標頭</span><span class="sxs-lookup"><span data-stu-id="51149-125">Header</span></span><br/> | <dl> <span data-ttu-id="51149-126"><dt>PortableDevice。h</dt></span><span class="sxs-lookup"><span data-stu-id="51149-126"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51149-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="51149-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51149-128">**WPD 屬性和屬性**</span><span class="sxs-lookup"><span data-stu-id="51149-128">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




