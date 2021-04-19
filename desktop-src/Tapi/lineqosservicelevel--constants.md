---
description: TSP 會使用這些常數來識別 QoS (所需服務品質) 層級的類型。
ms.assetid: 9fc3f6eb-7103-43c5-84f8-3842757e5be7
title: 'LINEQOSSERVICELEVEL_ 常數 (Tspi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c0629715e461a15e21e1730f86edb61d83d60db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001610"
---
# <a name="lineqosservicelevel_-constants"></a><span data-ttu-id="9c08e-103">LINEQOSSERVICELEVEL \_ 常數</span><span class="sxs-lookup"><span data-stu-id="9c08e-103">LINEQOSSERVICELEVEL\_ Constants</span></span>

<span data-ttu-id="9c08e-104">TSP 會使用這些常數來識別 QoS (所需服務品質) 層級的類型。</span><span class="sxs-lookup"><span data-stu-id="9c08e-104">These constants are used by a TSP to identify the type of a QoS (Quality of Service) level required.</span></span>

<dl> <dt>

<span data-ttu-id="9c08e-105"><span id="LINEQOSSERVICELEVEL_NEEDED"></span><span id="lineqosservicelevel_needed"></span>**\_需要 LINEQOSSERVICELEVEL**</span><span class="sxs-lookup"><span data-stu-id="9c08e-105"><span id="LINEQOSSERVICELEVEL_NEEDED"></span><span id="lineqosservicelevel_needed"></span>**LINEQOSSERVICELEVEL\_NEEDED**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="9c08e-106">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9c08e-106">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="9c08e-107">要求的服務層級品質是必要條件。</span><span class="sxs-lookup"><span data-stu-id="9c08e-107">The quality of service level requested is a requirement.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9c08e-108"><span id="LINEQOSSERVICELEVEL_IFAVAILABLE"></span><span id="lineqosservicelevel_ifavailable"></span>**LINEQOSSERVICELEVEL \_ IFAVAILABLE**</span><span class="sxs-lookup"><span data-stu-id="9c08e-108"><span id="LINEQOSSERVICELEVEL_IFAVAILABLE"></span><span id="lineqosservicelevel_ifavailable"></span>**LINEQOSSERVICELEVEL\_IFAVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="9c08e-109">0x00000002</span><span class="sxs-lookup"><span data-stu-id="9c08e-109">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="9c08e-110">需要的服務層級品質（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="9c08e-110">The quality of service level required, if available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9c08e-111"><span id="LINEQOSSERVICELEVEL_BESTEFFORT"></span><span id="lineqosservicelevel_besteffort"></span>**LINEQOSSERVICELEVEL \_ BESTEFFORT**</span><span class="sxs-lookup"><span data-stu-id="9c08e-111"><span id="LINEQOSSERVICELEVEL_BESTEFFORT"></span><span id="lineqosservicelevel_besteffort"></span>**LINEQOSSERVICELEVEL\_BESTEFFORT**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="9c08e-112">0x00000003</span><span class="sxs-lookup"><span data-stu-id="9c08e-112">0x00000003</span></span>
</dt> <dt>



<span data-ttu-id="9c08e-113">所需的服務等級品質是「最佳的努力」。</span><span class="sxs-lookup"><span data-stu-id="9c08e-113">The quality of service level required is "best effort."</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9c08e-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="9c08e-114">Requirements</span></span>



| <span data-ttu-id="9c08e-115">需求</span><span class="sxs-lookup"><span data-stu-id="9c08e-115">Requirement</span></span> | <span data-ttu-id="9c08e-116">值</span><span class="sxs-lookup"><span data-stu-id="9c08e-116">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="9c08e-117">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="9c08e-117">TAPI version</span></span><br/> | <span data-ttu-id="9c08e-118">需要 TAPI 2。2</span><span class="sxs-lookup"><span data-stu-id="9c08e-118">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="9c08e-119">標頭</span><span class="sxs-lookup"><span data-stu-id="9c08e-119">Header</span></span><br/>       | <dl> <span data-ttu-id="9c08e-120"><dt>Tspi。h</dt></span><span class="sxs-lookup"><span data-stu-id="9c08e-120"><dt>Tspi.h</dt></span></span> </dl> |



 

 




