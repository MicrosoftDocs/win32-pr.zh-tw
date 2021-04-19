---
description: TSP 會使用這些常數來識別 QoS (服務品質) 要求的類型。 目前只支援服務層級要求。 請參閱 LINEQOSSERVICELEVEL \_ 常數。
ms.assetid: 128fcaf8-a54d-4633-9f44-188b02e21709
title: 'LINEQOSREQUESTTYPE_ 常數 (Tspi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7795ddc70ea4fc6719578a38896a292ee1df9da3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998859"
---
# <a name="lineqosrequesttype_-constants"></a><span data-ttu-id="3135a-105">LINEQOSREQUESTTYPE \_ 常數</span><span class="sxs-lookup"><span data-stu-id="3135a-105">LINEQOSREQUESTTYPE\_ Constants</span></span>

<span data-ttu-id="3135a-106">TSP 會使用這些常數來識別 QoS (服務品質) 要求的類型。</span><span class="sxs-lookup"><span data-stu-id="3135a-106">These constants are used by a TSP to identify the type of a QoS (Quality of Service) request being made.</span></span> <span data-ttu-id="3135a-107">目前只支援服務層級要求。</span><span class="sxs-lookup"><span data-stu-id="3135a-107">Currently, only a service level request is supported.</span></span> <span data-ttu-id="3135a-108">請參閱 [LINEQOSSERVICELEVEL \_ 常數](lineqosservicelevel--constants.md)。</span><span class="sxs-lookup"><span data-stu-id="3135a-108">See [LINEQOSSERVICELEVEL\_ Constants](lineqosservicelevel--constants.md).</span></span>

<dl> <dt>

<span data-ttu-id="3135a-109"><span id="LINEQOSREQUESTTYPE_SERVICELEVEL"></span><span id="lineqosrequesttype_servicelevel"></span>**LINEQOSREQUESTTYPE \_ SERVICELEVEL**</span><span class="sxs-lookup"><span data-stu-id="3135a-109"><span id="LINEQOSREQUESTTYPE_SERVICELEVEL"></span><span id="lineqosrequesttype_servicelevel"></span>**LINEQOSREQUESTTYPE\_SERVICELEVEL**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="3135a-110">0x00000001</span><span class="sxs-lookup"><span data-stu-id="3135a-110">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="3135a-111">所提出的 QoS 要求是針對特定的服務層級。</span><span class="sxs-lookup"><span data-stu-id="3135a-111">The QoS request being made is for a particular service level.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3135a-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="3135a-112">Requirements</span></span>



| <span data-ttu-id="3135a-113">需求</span><span class="sxs-lookup"><span data-stu-id="3135a-113">Requirement</span></span> | <span data-ttu-id="3135a-114">值</span><span class="sxs-lookup"><span data-stu-id="3135a-114">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="3135a-115">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="3135a-115">TAPI version</span></span><br/> | <span data-ttu-id="3135a-116">需要 TAPI 2。2</span><span class="sxs-lookup"><span data-stu-id="3135a-116">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="3135a-117">標頭</span><span class="sxs-lookup"><span data-stu-id="3135a-117">Header</span></span><br/>       | <dl> <span data-ttu-id="3135a-118"><dt>Tspi。h</dt></span><span class="sxs-lookup"><span data-stu-id="3135a-118"><dt>Tspi.h</dt></span></span> </dl> |



 

 




