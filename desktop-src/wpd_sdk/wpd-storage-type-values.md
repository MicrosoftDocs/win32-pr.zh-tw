---
description: WPD \_ 儲存體 \_ 類型 \_ 值列舉類型會描述不同的 Windows 可攜式裝置儲存類型。
ms.assetid: 52c34458-e64e-4355-9231-7457a6dff5c5
title: 'WPD_STORAGE_TYPE_VALUES 列舉 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_STORAGE_TYPE_VALUES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: b741feb1cb9a834e16a35627fe98718ac8acf30f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989639"
---
# <a name="wpd_storage_type_values-enumeration"></a><span data-ttu-id="751c2-103">WPD \_ 儲存體 \_ 類型 \_ 值列舉</span><span class="sxs-lookup"><span data-stu-id="751c2-103">WPD\_STORAGE\_TYPE\_VALUES enumeration</span></span>

<span data-ttu-id="751c2-104">**WPD \_ 儲存體 \_ 類型 \_ 值** 列舉類型會描述不同的 Windows 可攜式裝置儲存類型。</span><span class="sxs-lookup"><span data-stu-id="751c2-104">The **WPD\_STORAGE\_TYPE\_VALUES** enumeration type describes the different Windows Portable Device storage types.</span></span>

## <a name="syntax"></a><span data-ttu-id="751c2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="751c2-105">Syntax</span></span>


```C++
typedef enum tagWPD_STORAGE_TYPE_VALUES { 
  WPD_STORAGE_TYPE_UNDEFINED      = 0,
  WPD_STORAGE_TYPE_FIXED_ROM      = 1,
  WPD_STORAGE_TYPE_REMOVABLE_ROM  = 2,
  WPD_STORAGE_TYPE_FIXED_RAM      = 3,
  WPD_STORAGE_TYPE_REMOVABLE_RAM  = 4
} WPD_STORAGE_TYPE_VALUES;
```



## <a name="constants"></a><span data-ttu-id="751c2-106">常數</span><span class="sxs-lookup"><span data-stu-id="751c2-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="751c2-107"><span id="WPD_STORAGE_TYPE_UNDEFINED"></span><span id="wpd_storage_type_undefined"></span>**WPD \_ 儲存體 \_ 類型 \_ 未定義**</span><span class="sxs-lookup"><span data-stu-id="751c2-107"><span id="WPD_STORAGE_TYPE_UNDEFINED"></span><span id="wpd_storage_type_undefined"></span>**WPD\_STORAGE\_TYPE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="751c2-108">儲存體是未定義的類型。</span><span class="sxs-lookup"><span data-stu-id="751c2-108">The storage is of an undefined type.</span></span>

</dd> <dt>

<span data-ttu-id="751c2-109"><span id="WPD_STORAGE_TYPE_FIXED_ROM"></span><span id="wpd_storage_type_fixed_rom"></span>**WPD \_ 儲存體 \_ 類型 \_ 固定 \_ ROM**</span><span class="sxs-lookup"><span data-stu-id="751c2-109"><span id="WPD_STORAGE_TYPE_FIXED_ROM"></span><span id="wpd_storage_type_fixed_rom"></span>**WPD\_STORAGE\_TYPE\_FIXED\_ROM**</span></span>
</dt> <dd>

<span data-ttu-id="751c2-110">儲存體為非卸載式和唯讀。</span><span class="sxs-lookup"><span data-stu-id="751c2-110">The storage is non-removable and read-only.</span></span>

</dd> <dt>

<span data-ttu-id="751c2-111"><span id="WPD_STORAGE_TYPE_REMOVABLE_ROM"></span><span id="wpd_storage_type_removable_rom"></span>**WPD \_ 存放裝置 \_ 類型的 \_ 可移動 \_ ROM**</span><span class="sxs-lookup"><span data-stu-id="751c2-111"><span id="WPD_STORAGE_TYPE_REMOVABLE_ROM"></span><span id="wpd_storage_type_removable_rom"></span>**WPD\_STORAGE\_TYPE\_REMOVABLE\_ROM**</span></span>
</dt> <dd>

<span data-ttu-id="751c2-112">儲存體是可移動的，而且是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="751c2-112">The storage is removable and is read-only.</span></span>

</dd> <dt>

<span data-ttu-id="751c2-113"><span id="WPD_STORAGE_TYPE_FIXED_RAM"></span><span id="wpd_storage_type_fixed_ram"></span>**WPD \_ 儲存體 \_ 類型 \_ 固定 \_ RAM**</span><span class="sxs-lookup"><span data-stu-id="751c2-113"><span id="WPD_STORAGE_TYPE_FIXED_RAM"></span><span id="wpd_storage_type_fixed_ram"></span>**WPD\_STORAGE\_TYPE\_FIXED\_RAM**</span></span>
</dt> <dd>

<span data-ttu-id="751c2-114">儲存體是不可卸載的，且可讀/寫功能。</span><span class="sxs-lookup"><span data-stu-id="751c2-114">The storage is non-removable and is read/write capable.</span></span>

</dd> <dt>

<span data-ttu-id="751c2-115"><span id="WPD_STORAGE_TYPE_REMOVABLE_RAM"></span><span id="wpd_storage_type_removable_ram"></span>**WPD \_ 儲存體 \_ 類型的 \_ 可移動 \_ RAM**</span><span class="sxs-lookup"><span data-stu-id="751c2-115"><span id="WPD_STORAGE_TYPE_REMOVABLE_RAM"></span><span id="wpd_storage_type_removable_ram"></span>**WPD\_STORAGE\_TYPE\_REMOVABLE\_RAM**</span></span>
</dt> <dd>

<span data-ttu-id="751c2-116">儲存體是可移動的，且可讀/寫功能。</span><span class="sxs-lookup"><span data-stu-id="751c2-116">The storage is removable and is read/write capable.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="751c2-117">備註</span><span class="sxs-lookup"><span data-stu-id="751c2-117">Remarks</span></span>

<span data-ttu-id="751c2-118">無。</span><span class="sxs-lookup"><span data-stu-id="751c2-118">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="751c2-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="751c2-119">Requirements</span></span>



| <span data-ttu-id="751c2-120">需求</span><span class="sxs-lookup"><span data-stu-id="751c2-120">Requirement</span></span> | <span data-ttu-id="751c2-121">值</span><span class="sxs-lookup"><span data-stu-id="751c2-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="751c2-122">標頭</span><span class="sxs-lookup"><span data-stu-id="751c2-122">Header</span></span><br/> | <dl> <span data-ttu-id="751c2-123"><dt>PortableDevice。h</dt></span><span class="sxs-lookup"><span data-stu-id="751c2-123"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="751c2-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="751c2-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="751c2-125">**結構和列舉類型**</span><span class="sxs-lookup"><span data-stu-id="751c2-125">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




