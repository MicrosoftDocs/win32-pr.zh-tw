---
description: 指定服務的繼承關聯性。
ms.assetid: e7f5314a-75e8-4f36-8e18-d614eda7a097
title: 'WPD_SERVICE_INHERITANCE_TYPES 列舉 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_SERVICE_INHERITANCE_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: ad9115bf7bb0912362455986e77d5792cceec3b7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994589"
---
# <a name="wpd_service_inheritance_types-enumeration"></a><span data-ttu-id="3de77-103">WPD \_ 服務 \_ 繼承 \_ 類型列舉</span><span class="sxs-lookup"><span data-stu-id="3de77-103">WPD\_SERVICE\_INHERITANCE\_TYPES enumeration</span></span>

<span data-ttu-id="3de77-104">**WPD \_ 服務 \_ 繼承 \_ 類型** 列舉型別會指定服務的繼承關聯性。</span><span class="sxs-lookup"><span data-stu-id="3de77-104">The **WPD\_SERVICE\_INHERITANCE\_TYPES** enumeration type specifies the inheritance relationship for a service.</span></span>

## <a name="syntax"></a><span data-ttu-id="3de77-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3de77-105">Syntax</span></span>


```C++
typedef enum tagWPD_SERVICE_INHERITANCE_TYPES { 
  WPD_SERVICE_INHERITANCE_IMPLEMENTATION  = 0
} WPD_SERVICE_INHERITANCE_TYPES;
```



## <a name="constants"></a><span data-ttu-id="3de77-106">常數</span><span class="sxs-lookup"><span data-stu-id="3de77-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="3de77-107"><span id="WPD_SERVICE_INHERITANCE_IMPLEMENTATION"></span><span id="wpd_service_inheritance_implementation"></span>**WPD \_ 服務 \_ 繼承的 \_ 執行**</span><span class="sxs-lookup"><span data-stu-id="3de77-107"><span id="WPD_SERVICE_INHERITANCE_IMPLEMENTATION"></span><span id="wpd_service_inheritance_implementation"></span>**WPD\_SERVICE\_INHERITANCE\_IMPLEMENTATION**</span></span>
</dt> <dd>

<span data-ttu-id="3de77-108">服務會藉由執行抽象服務定義來繼承。</span><span class="sxs-lookup"><span data-stu-id="3de77-108">The service inherits by implementing an abstract service definition.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3de77-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="3de77-109">Requirements</span></span>



| <span data-ttu-id="3de77-110">需求</span><span class="sxs-lookup"><span data-stu-id="3de77-110">Requirement</span></span> | <span data-ttu-id="3de77-111">值</span><span class="sxs-lookup"><span data-stu-id="3de77-111">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="3de77-112">標頭</span><span class="sxs-lookup"><span data-stu-id="3de77-112">Header</span></span><br/> | <dl> <span data-ttu-id="3de77-113"><dt>PortableDevice。h</dt></span><span class="sxs-lookup"><span data-stu-id="3de77-113"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3de77-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3de77-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3de77-115">**IPortableDeviceServiceCapabilities::GetInheritedServices**</span><span class="sxs-lookup"><span data-stu-id="3de77-115">**IPortableDeviceServiceCapabilities::GetInheritedServices**</span></span>](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getinheritedservices)
</dt> </dl>

 

 




