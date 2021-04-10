---
description: 終止此作業和任何基礎進程，以及移除任何無關聯關聯的方法。 這個方法已被取代;請改用 RequestChangeState。
ms.assetid: b116631f-34b8-43ed-9c17-062b5e6058d0
title: CIM_Job 類別的 KillJob 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Job.KillJob
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 967e5e8510d4456a085f393291f8c41afb5be446
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944058"
---
# <a name="killjob-method-of-the-cim_job-class"></a><span data-ttu-id="9e487-104">CIM 作業類別的 KillJob 方法 \_</span><span class="sxs-lookup"><span data-stu-id="9e487-104">KillJob method of the CIM\_Job class</span></span>

<span data-ttu-id="9e487-105">終止此作業和任何基礎進程，以及移除任何「無關聯」關聯的方法。</span><span class="sxs-lookup"><span data-stu-id="9e487-105">A method to kill this job and any underlying processes, and to remove any 'dangling' associations.</span></span> <span data-ttu-id="9e487-106">這個方法已被取代;請改用 **RequestChangeState** 。</span><span class="sxs-lookup"><span data-stu-id="9e487-106">This method is deprecated; use **RequestChangeState** instead.</span></span> <span data-ttu-id="9e487-107">**KillJob** 即將被取代，因為有條理的關機和立即終止之間並沒有差別。</span><span class="sxs-lookup"><span data-stu-id="9e487-107">**KillJob** is being deprecated because there is no distinction made between an orderly shutdown and an immediate kill.</span></span> <span data-ttu-id="9e487-108">[**CIM \_ConcreteJob**](cim-concretejob.md)。**RequestStateChange** () 提供「終止」和「終止」選項，以允許這種差異。</span><span class="sxs-lookup"><span data-stu-id="9e487-108">[**CIM\_ConcreteJob**](cim-concretejob.md).**RequestStateChange**() provides 'Terminate' and 'Kill' options to allow this distinction.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e487-109">語法</span><span class="sxs-lookup"><span data-stu-id="9e487-109">Syntax</span></span>


```mof
uint32 KillJob(
  [in] boolean DeleteOnKill
);
```



## <a name="parameters"></a><span data-ttu-id="9e487-110">參數</span><span class="sxs-lookup"><span data-stu-id="9e487-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e487-111">*DeleteOnKill* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9e487-111">*DeleteOnKill* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e487-112">指出作業是否應該在終止時自動刪除。</span><span class="sxs-lookup"><span data-stu-id="9e487-112">Indicates whether or not the Job should be automatically deleted upon termination.</span></span> <span data-ttu-id="9e487-113">此參數優先于 **DeleteOnCompletion** 屬性。</span><span class="sxs-lookup"><span data-stu-id="9e487-113">This parameter takes precedence over the **DeleteOnCompletion** property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e487-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="9e487-114">Return value</span></span>

<span data-ttu-id="9e487-115">成功時傳回 0;否則，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="9e487-115">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="9e487-116">**成功** (0) </span><span class="sxs-lookup"><span data-stu-id="9e487-116">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9e487-117">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="9e487-117">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9e487-118">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="9e487-118">**Unknown** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9e487-119">**Timeout** (3) </span><span class="sxs-lookup"><span data-stu-id="9e487-119">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9e487-120">**失敗** (4) </span><span class="sxs-lookup"><span data-stu-id="9e487-120">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="9e487-121">**拒絕存取** (6) </span><span class="sxs-lookup"><span data-stu-id="9e487-121">**Access Denied** (6)</span></span>
</dt> <dt>

<span data-ttu-id="9e487-122">**找不到** (7) </span><span class="sxs-lookup"><span data-stu-id="9e487-122">**Not Found** (7)</span></span>
</dt> <dt>

<span data-ttu-id="9e487-123">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="9e487-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="9e487-124">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="9e487-124">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="9e487-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="9e487-125">Requirements</span></span>



| <span data-ttu-id="9e487-126">需求</span><span class="sxs-lookup"><span data-stu-id="9e487-126">Requirement</span></span> | <span data-ttu-id="9e487-127">值</span><span class="sxs-lookup"><span data-stu-id="9e487-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e487-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9e487-128">Minimum supported client</span></span><br/> | <span data-ttu-id="9e487-129">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="9e487-129">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="9e487-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9e487-130">Minimum supported server</span></span><br/> | <span data-ttu-id="9e487-131">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="9e487-131">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="9e487-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="9e487-132">Namespace</span></span><br/>                | <span data-ttu-id="9e487-133">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="9e487-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="9e487-134">MOF</span><span class="sxs-lookup"><span data-stu-id="9e487-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9e487-135"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="9e487-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9e487-136">DLL</span><span class="sxs-lookup"><span data-stu-id="9e487-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e487-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9e487-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9e487-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9e487-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e487-139">**CIM \_ 作業**</span><span class="sxs-lookup"><span data-stu-id="9e487-139">**CIM\_Job**</span></span>](cim-job.md)
</dt> </dl>

 

 




