---
description: TSP 會使用這些常數來識別 QoS (服務品質) 要求的結果。
ms.assetid: 617ddbf4-212f-4990-93c2-f38f04b035ab
title: 'LINEEQOSINFO_ 常數 (Tspi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 423cc6172a1c6c87c1f3bb38929f727a15dad5c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993609"
---
# <a name="lineeqosinfo_-constants"></a><span data-ttu-id="db347-103">LINEEQOSINFO \_ 常數</span><span class="sxs-lookup"><span data-stu-id="db347-103">LINEEQOSINFO\_ Constants</span></span>

<span data-ttu-id="db347-104">TSP 會使用這些常數來識別 QoS (服務品質) 要求的結果。</span><span class="sxs-lookup"><span data-stu-id="db347-104">These constants are used by a TSP to identify the result of a QoS (Quality of Service) request.</span></span>

<dl> <dt>

<span data-ttu-id="db347-105"><span id="LINEEQOSINFO_NOQOS"></span><span id="lineeqosinfo_noqos"></span>**LINEEQOSINFO \_ NOQOS**</span><span class="sxs-lookup"><span data-stu-id="db347-105"><span id="LINEEQOSINFO_NOQOS"></span><span id="lineeqosinfo_noqos"></span>**LINEEQOSINFO\_NOQOS**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="db347-106">0x00000001</span><span class="sxs-lookup"><span data-stu-id="db347-106">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="db347-107">無法使用 QoS。</span><span class="sxs-lookup"><span data-stu-id="db347-107">QoS is not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="db347-108"><span id="LINEEQOSINFO_ADMISSIONFAILURE"></span><span id="lineeqosinfo_admissionfailure"></span>**LINEEQOSINFO \_ ADMISSIONFAILURE**</span><span class="sxs-lookup"><span data-stu-id="db347-108"><span id="LINEEQOSINFO_ADMISSIONFAILURE"></span><span id="lineeqosinfo_admissionfailure"></span>**LINEEQOSINFO\_ADMISSIONFAILURE**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="db347-109">0x00000002</span><span class="sxs-lookup"><span data-stu-id="db347-109">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="db347-110">無法符合 QoS 要求。</span><span class="sxs-lookup"><span data-stu-id="db347-110">The QoS request could not be met.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="db347-111"><span id="LINEEQOSINFO_POLICYFAILURE"></span><span id="lineeqosinfo_policyfailure"></span>**LINEEQOSINFO \_ POLICYFAILURE**</span><span class="sxs-lookup"><span data-stu-id="db347-111"><span id="LINEEQOSINFO_POLICYFAILURE"></span><span id="lineeqosinfo_policyfailure"></span>**LINEEQOSINFO\_POLICYFAILURE**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="db347-112">0x00000003</span><span class="sxs-lookup"><span data-stu-id="db347-112">0x00000003</span></span>
</dt> <dt>



<span data-ttu-id="db347-113">不支援要求的 QoS 類型。</span><span class="sxs-lookup"><span data-stu-id="db347-113">The type of QoS requested is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="db347-114"><span id="LINEEQOSINFO_GENERICERROR"></span><span id="lineeqosinfo_genericerror"></span>**LINEEQOSINFO \_ GENERICERROR**</span><span class="sxs-lookup"><span data-stu-id="db347-114"><span id="LINEEQOSINFO_GENERICERROR"></span><span id="lineeqosinfo_genericerror"></span>**LINEEQOSINFO\_GENERICERROR**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="db347-115">0x00000004</span><span class="sxs-lookup"><span data-stu-id="db347-115">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="db347-116">未指定的 QoS 錯誤。</span><span class="sxs-lookup"><span data-stu-id="db347-116">Unspecified QoS error.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="db347-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="db347-117">Requirements</span></span>



| <span data-ttu-id="db347-118">需求</span><span class="sxs-lookup"><span data-stu-id="db347-118">Requirement</span></span> | <span data-ttu-id="db347-119">值</span><span class="sxs-lookup"><span data-stu-id="db347-119">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="db347-120">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="db347-120">TAPI version</span></span><br/> | <span data-ttu-id="db347-121">需要 TAPI 2。2</span><span class="sxs-lookup"><span data-stu-id="db347-121">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="db347-122">標頭</span><span class="sxs-lookup"><span data-stu-id="db347-122">Header</span></span><br/>       | <dl> <span data-ttu-id="db347-123"><dt>Tspi。h</dt></span><span class="sxs-lookup"><span data-stu-id="db347-123"><dt>Tspi.h</dt></span></span> </dl> |



 

 




