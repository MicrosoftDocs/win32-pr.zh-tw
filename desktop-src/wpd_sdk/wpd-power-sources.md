---
description: WPD \_ 電源 \_ 來源列舉類型會描述裝置使用的電源來源。
ms.assetid: feebf213-052d-4315-84db-2109cab5f179
title: 'WPD_POWER_SOURCES 列舉 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_POWER_SOURCES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: bf9a153d4d41a64b639f796ea2ba0eeb9e567a32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987024"
---
# <a name="wpd_power_sources-enumeration"></a><span data-ttu-id="31dcd-103">WPD \_ 電源 \_ 來源列舉</span><span class="sxs-lookup"><span data-stu-id="31dcd-103">WPD\_POWER\_SOURCES enumeration</span></span>

<span data-ttu-id="31dcd-104">**WPD \_ 電源 \_ 來源** 列舉類型會描述裝置使用的電源來源。</span><span class="sxs-lookup"><span data-stu-id="31dcd-104">The **WPD\_POWER\_SOURCES** enumeration type describes the power source that a device is using.</span></span>

## <a name="syntax"></a><span data-ttu-id="31dcd-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="31dcd-105">Syntax</span></span>


```C++
typedef enum WPD_POWER_SOURCES { 
  WPD_POWER_SOURCE_BATTERY   = 0,
  WPD_POWER_SOURCE_EXTERNAL  = 1
} ;
```



## <a name="constants"></a><span data-ttu-id="31dcd-106">常數</span><span class="sxs-lookup"><span data-stu-id="31dcd-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="31dcd-107"><span id="WPD_POWER_SOURCE_BATTERY"></span><span id="wpd_power_source_battery"></span>**WPD \_ 電源 \_ 來源 \_ 電池**</span><span class="sxs-lookup"><span data-stu-id="31dcd-107"><span id="WPD_POWER_SOURCE_BATTERY"></span><span id="wpd_power_source_battery"></span>**WPD\_POWER\_SOURCE\_BATTERY**</span></span>
</dt> <dd>

<span data-ttu-id="31dcd-108">裝置電源來源為電池。</span><span class="sxs-lookup"><span data-stu-id="31dcd-108">The device power source is a battery.</span></span>

</dd> <dt>

<span data-ttu-id="31dcd-109"><span id="WPD_POWER_SOURCE_EXTERNAL"></span><span id="wpd_power_source_external"></span>**WPD \_ 電源 \_ 來源 \_ 外部**</span><span class="sxs-lookup"><span data-stu-id="31dcd-109"><span id="WPD_POWER_SOURCE_EXTERNAL"></span><span id="wpd_power_source_external"></span>**WPD\_POWER\_SOURCE\_EXTERNAL**</span></span>
</dt> <dd>

<span data-ttu-id="31dcd-110">裝置使用外部電源來源。</span><span class="sxs-lookup"><span data-stu-id="31dcd-110">The device uses an external power source.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="31dcd-111">備註</span><span class="sxs-lookup"><span data-stu-id="31dcd-111">Remarks</span></span>

<span data-ttu-id="31dcd-112">此列舉是由 [WPD \_ 裝置 \_ 電源 \_ 來源](device-properties.md) 屬性所使用。</span><span class="sxs-lookup"><span data-stu-id="31dcd-112">This enumeration is used by the [WPD\_DEVICE\_POWER\_SOURCE](device-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="31dcd-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="31dcd-113">Requirements</span></span>



| <span data-ttu-id="31dcd-114">需求</span><span class="sxs-lookup"><span data-stu-id="31dcd-114">Requirement</span></span> | <span data-ttu-id="31dcd-115">值</span><span class="sxs-lookup"><span data-stu-id="31dcd-115">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="31dcd-116">標頭</span><span class="sxs-lookup"><span data-stu-id="31dcd-116">Header</span></span><br/> | <dl> <span data-ttu-id="31dcd-117"><dt>PortableDevice。h</dt></span><span class="sxs-lookup"><span data-stu-id="31dcd-117"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31dcd-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="31dcd-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31dcd-119">**結構和列舉類型**</span><span class="sxs-lookup"><span data-stu-id="31dcd-119">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




