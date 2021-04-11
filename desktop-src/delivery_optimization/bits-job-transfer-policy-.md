---
title: 'BITS_JOB_TRANSFER_POLICY 列舉 (>deliveryoptimization .h) '
description: BITS_JOB_TRANSFER_POLICY 列舉會定義對應至 DO 屬性的識別碼值。
ms.assetid: 4811ADBF-F097-4340-BFF2-52CC9556ACF6
keywords:
- BITS_JOB_TRANSFER_POLICY 列舉
- BITS_JOB_TRANSFER_POLICY 列舉
topic_type:
- apiref
api_name:
- BITS_JOB_TRANSFER_POLICY
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 455752375b76e574923ccdd96d1d05fc9142c16c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094192"
---
# <a name="bits_job_transfer_policy-enumeration"></a><span data-ttu-id="20c65-105">BITS_JOB_TRANSFER_POLICY 列舉</span><span class="sxs-lookup"><span data-stu-id="20c65-105">BITS_JOB_TRANSFER_POLICY enumeration</span></span>

<span data-ttu-id="20c65-106">**BITS_JOB_TRANSFER_POLICY** 列舉會定義對應至 DO 屬性的識別碼值。</span><span class="sxs-lookup"><span data-stu-id="20c65-106">The **BITS_JOB_TRANSFER_POLICY** enumeration defines ID values corresponding to DO properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="20c65-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="20c65-107">Syntax</span></span>


```C++
typedef enum _BITS_JOB_TRANSFER_POLICY { 
  BITS_JOB_TRANSFER_POLICY_ALWAYS        = 0x800000ff,
  BITS_JOB_TRANSFER_POLICY_NOT_ROAMING   = 0x8000007f,
  BITS_JOB_TRANSFER_POLICY_NO_SURCHARGE  = 0x8000006f,
  BITS_JOB_TRANSFER_POLICY_STANDARD      = 0x80000067,
  BITS_JOB_TRANSFER_POLICY_UNRESTRICTED  = 0x80000021
} BITS_JOB_TRANSFER_POLICY;
```



## <a name="constants"></a><span data-ttu-id="20c65-108">常數</span><span class="sxs-lookup"><span data-stu-id="20c65-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="20c65-109"><span id="BITS_JOB_TRANSFER_POLICY_ALWAYS"></span><span id="bits_job_transfer_policy_always"></span>**BITS_JOB_TRANSFER_POLICY_ALWAYS**</span><span class="sxs-lookup"><span data-stu-id="20c65-109"><span id="BITS_JOB_TRANSFER_POLICY_ALWAYS"></span><span id="bits_job_transfer_policy_always"></span>**BITS_JOB_TRANSFER_POLICY_ALWAYS**</span></span>
</dt> <dd>

<span data-ttu-id="20c65-110">指定不論成本為何，都可以使用連接時傳送作業。</span><span class="sxs-lookup"><span data-stu-id="20c65-110">Specifies that the job will be transferred when connectivity is available, regardless of the cost.</span></span>

</dd> <dt>

<span data-ttu-id="20c65-111"><span id="BITS_JOB_TRANSFER_POLICY_NOT_ROAMING"></span><span id="bits_job_transfer_policy_not_roaming"></span>**BITS_JOB_TRANSFER_POLICY_NOT_ROAMING**</span><span class="sxs-lookup"><span data-stu-id="20c65-111"><span id="BITS_JOB_TRANSFER_POLICY_NOT_ROAMING"></span><span id="bits_job_transfer_policy_not_roaming"></span>**BITS_JOB_TRANSFER_POLICY_NOT_ROAMING**</span></span>
</dt> <dd>

<span data-ttu-id="20c65-112">指定當連線可用時，將會傳送作業，除非該連線受限於漫遊的附加費。</span><span class="sxs-lookup"><span data-stu-id="20c65-112">Specifies that the job will be transferred when connectivity is available, unless that connectivity is subject to roaming surcharges.</span></span>

</dd> <dt>

<span data-ttu-id="20c65-113"><span id="BITS_JOB_TRANSFER_POLICY_NO_SURCHARGE"></span><span id="bits_job_transfer_policy_no_surcharge"></span>**BITS_JOB_TRANSFER_POLICY_NO_SURCHARGE**</span><span class="sxs-lookup"><span data-stu-id="20c65-113"><span id="BITS_JOB_TRANSFER_POLICY_NO_SURCHARGE"></span><span id="bits_job_transfer_policy_no_surcharge"></span>**BITS_JOB_TRANSFER_POLICY_NO_SURCHARGE**</span></span>
</dt> <dd>

<span data-ttu-id="20c65-114">指定只有在有可用的連線能力時，才會傳送作業，而不會有額外費用。</span><span class="sxs-lookup"><span data-stu-id="20c65-114">Specifies that the job will be transferred only when connectivity is available which is not subject to a surcharge.</span></span>

</dd> <dt>

<span data-ttu-id="20c65-115"><span id="BITS_JOB_TRANSFER_POLICY_STANDARD"></span><span id="bits_job_transfer_policy_standard"></span>**BITS_JOB_TRANSFER_POLICY_STANDARD**</span><span class="sxs-lookup"><span data-stu-id="20c65-115"><span id="BITS_JOB_TRANSFER_POLICY_STANDARD"></span><span id="bits_job_transfer_policy_standard"></span>**BITS_JOB_TRANSFER_POLICY_STANDARD**</span></span>
</dt> <dd>

<span data-ttu-id="20c65-116">指定只有在連線可供使用時，才會傳送作業，這不會受到額外費用或接近耗盡。</span><span class="sxs-lookup"><span data-stu-id="20c65-116">Specifies that the job will be transferred only when connectivity is available which is neither subject to a surcharge nor near exhaustion.</span></span>

</dd> <dt>

<span data-ttu-id="20c65-117"><span id="BITS_JOB_TRANSFER_POLICY_UNRESTRICTED"></span><span id="bits_job_transfer_policy_unrestricted"></span>**BITS_JOB_TRANSFER_POLICY_UNRESTRICTED**</span><span class="sxs-lookup"><span data-stu-id="20c65-117"><span id="BITS_JOB_TRANSFER_POLICY_UNRESTRICTED"></span><span id="bits_job_transfer_policy_unrestricted"></span>**BITS_JOB_TRANSFER_POLICY_UNRESTRICTED**</span></span>
</dt> <dd>

<span data-ttu-id="20c65-118">指定只有在可使用連線能力，而不會造成成本或流量限制時，才會傳送工作。</span><span class="sxs-lookup"><span data-stu-id="20c65-118">Specifies that the job will be transferred only when connectivity is available which does not impose costs or traffic limits.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="20c65-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="20c65-119">Requirements</span></span>



| <span data-ttu-id="20c65-120">需求</span><span class="sxs-lookup"><span data-stu-id="20c65-120">Requirement</span></span> | <span data-ttu-id="20c65-121">值</span><span class="sxs-lookup"><span data-stu-id="20c65-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20c65-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="20c65-122">Minimum supported client</span></span><br/> | <span data-ttu-id="20c65-123">Windows 10， \[ 僅限1709版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="20c65-123">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="20c65-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="20c65-124">Minimum supported server</span></span><br/> | <span data-ttu-id="20c65-125">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="20c65-125">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="20c65-126">標頭</span><span class="sxs-lookup"><span data-stu-id="20c65-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="20c65-127"><dt>>deliveryoptimization。h</dt></span><span class="sxs-lookup"><span data-stu-id="20c65-127"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



 

 





