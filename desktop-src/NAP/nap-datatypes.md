---
title: 'NAP 資料類型 (NapTypes .h) '
description: 請注意，從 Windows 10 網路存取保護的資料類型 (NAP) API 之後，就無法使用網路存取保護平臺，如下所示。
ms.assetid: 54f2866b-4333-4fc8-bb25-b7d4ae72b7dc
keywords:
- ProbationTime
- ProtocolMaxSize
- NapComponentId
- SystemHealthEntityId
- EnforcementEntityId
- SystemHealthEntityCount
- EnforcementEntityCount
- StringCorrelationId
- ConnectionId
- 百分比
- MessageId
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5780d73701354a12b244c5e5ea6167c2cfba70d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934874"
---
# <a name="nap-datatypes"></a><span data-ttu-id="2af0b-114">NAP 資料類型</span><span class="sxs-lookup"><span data-stu-id="2af0b-114">NAP Datatypes</span></span>

> [!Note]  
> <span data-ttu-id="2af0b-115">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="2af0b-115">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="2af0b-116">網路存取保護 (NAP) API 的資料類型如下所示。</span><span class="sxs-lookup"><span data-stu-id="2af0b-116">The datatypes for the Network Access Protection (NAP) API are as follows.</span></span>


```C++
typedef FILETIME ProbationTime;
typedef UINT32 ProtocolMaxSize;
typedef UINT32 NapComponentId;
typedef NapComponentId SystemHealthEntityId;
typedef NapComponentId EnforcementEntityId;
typedef UINT16 SystemHealthEntityCount;
typedef UINT16 EnforcementEntityCount;
typedef CountedString StringCorrelationId;
typedef GUID ConnectionId;
typedef UINT8 Percentage;
typedef UINT32 MessageId;
```



<dl> <dt>

<span data-ttu-id="2af0b-117">**ProbationTime**</span><span class="sxs-lookup"><span data-stu-id="2af0b-117">**ProbationTime**</span></span>
</dt> <dd>

<span data-ttu-id="2af0b-118">[FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime)結構，包含與用戶端電腦的試用期相關的時間。</span><span class="sxs-lookup"><span data-stu-id="2af0b-118">A [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure that contains a time related to a client machine's probation.</span></span>

</dd> <dt>

<span data-ttu-id="2af0b-119">**ProtocolMaxSize**</span><span class="sxs-lookup"><span data-stu-id="2af0b-119">**ProtocolMaxSize**</span></span>
</dt> <dd>

<span data-ttu-id="2af0b-120">值，指定 [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) 封包的最大大小（以位元組為單位）的可能值範圍，如範圍 ([**minProtocolMaxSize，maxProtocolMaxSize**](nap-type-constants.md)) 的定義。</span><span class="sxs-lookup"><span data-stu-id="2af0b-120">A value that specifies the range of possible values for the maximum size, in bytes, of an [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) packet as defined by range([**minProtocolMaxSize, maxProtocolMaxSize**](nap-type-constants.md)).</span></span>

</dd> <dt>

<span data-ttu-id="2af0b-121">**NapComponentId**</span><span class="sxs-lookup"><span data-stu-id="2af0b-121">**NapComponentId**</span></span>
</dt> <dd>

<span data-ttu-id="2af0b-122">Sha、Shv 和強制用戶端用來識別本身的唯一4位元組識別碼。</span><span class="sxs-lookup"><span data-stu-id="2af0b-122">A unique 4-byte identifier used by SHAs, SHVs and enforcement clients to identify themselves.</span></span> <span data-ttu-id="2af0b-123">前三個位元組是供應商的 IETF 指派 SMI-S 碼，最後一個位元組會識別元件本身。</span><span class="sxs-lookup"><span data-stu-id="2af0b-123">The first three bytes are the IETF-assigned SMI code of the vendor, and the last byte identifies the component itself.</span></span>

</dd> <dt>

<span data-ttu-id="2af0b-124">**SystemHealthEntityId**</span><span class="sxs-lookup"><span data-stu-id="2af0b-124">**SystemHealthEntityId**</span></span>
</dt> <dd>

<span data-ttu-id="2af0b-125">用來識別 SHA/SHV 配對的 **NapComponentId** 值。</span><span class="sxs-lookup"><span data-stu-id="2af0b-125">A **NapComponentId** value used to identify SHA/SHV pairs.</span></span>

</dd> <dt>

<span data-ttu-id="2af0b-126">**EnforcementEntityId**</span><span class="sxs-lookup"><span data-stu-id="2af0b-126">**EnforcementEntityId**</span></span>
</dt> <dd>

<span data-ttu-id="2af0b-127">用來識別強制用戶端的 **NapComponentId** 值。</span><span class="sxs-lookup"><span data-stu-id="2af0b-127">A **NapComponentId** value used to identify enforcement clients.</span></span>

</dd> <dt>

<span data-ttu-id="2af0b-128">**SystemHealthEntityCount**</span><span class="sxs-lookup"><span data-stu-id="2af0b-128">**SystemHealthEntityCount**</span></span>
</dt> <dd>

<span data-ttu-id="2af0b-129">值，這個值會指定要 [**maxSystemHealthEntityCount**](nap-type-constants.md)的) 範圍 0 (零零的 NAP 系統中已註冊的 sha 數目。</span><span class="sxs-lookup"><span data-stu-id="2af0b-129">A value that specifies the number of registered SHAs in the NAP system in the range 0 (zero) to [**maxSystemHealthEntityCount**](nap-type-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="2af0b-130">**EnforcementEntityCount**</span><span class="sxs-lookup"><span data-stu-id="2af0b-130">**EnforcementEntityCount**</span></span>
</dt> <dd>

<span data-ttu-id="2af0b-131">值，指定 NAP 系統中的強制用戶端數目，範圍介於 0 (零) [**maxEnforcerCount**](nap-type-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="2af0b-131">A value that specifies the number of enforcement clients in the NAP system in the range 0 (zero) to [**maxEnforcerCount**](nap-type-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="2af0b-132">**StringCorrelationId**</span><span class="sxs-lookup"><span data-stu-id="2af0b-132">**StringCorrelationId**</span></span>
</dt> <dd>

<span data-ttu-id="2af0b-133">用來將 [**SoHRequests**](/windows/win32/api/naptypes/ns-naptypes-soh)配對至 **SoHResponses** 之 [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid)結構的 [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring)版本。</span><span class="sxs-lookup"><span data-stu-id="2af0b-133">The [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) version of a [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) structure used to pair [**SoHRequests**](/windows/win32/api/naptypes/ns-naptypes-soh) to **SoHResponses**.</span></span>

</dd> <dt>

<span data-ttu-id="2af0b-134">**ConnectionId**</span><span class="sxs-lookup"><span data-stu-id="2af0b-134">**ConnectionId**</span></span>
</dt> <dd>

<span data-ttu-id="2af0b-135">唯一的全域唯一識別碼 (GUID) 用來識別強制用戶端所維護的 NAP 連接。</span><span class="sxs-lookup"><span data-stu-id="2af0b-135">A unique Globally Unique Identifier (GUID) used to identify a NAP connections maintained by enforcement clients.</span></span>

</dd> <dt>

<span data-ttu-id="2af0b-136">**百分比**</span><span class="sxs-lookup"><span data-stu-id="2af0b-136">**Percentage**</span></span>
</dt> <dd>

<span data-ttu-id="2af0b-137">值，其中包含 0 (零) 的百分比，以及已完成的補救措施100</span><span class="sxs-lookup"><span data-stu-id="2af0b-137">A value that contains the percentage between 0 (zero) and 100 of remediation that is complete</span></span>

</dd> <dt>

<span data-ttu-id="2af0b-138">**MessageId**</span><span class="sxs-lookup"><span data-stu-id="2af0b-138">**MessageId**</span></span>
</dt> <dd>

<span data-ttu-id="2af0b-139">用來識別 NAP 系統訊息的唯一值。</span><span class="sxs-lookup"><span data-stu-id="2af0b-139">A unique value used to identify NAP system messages.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2af0b-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="2af0b-140">Requirements</span></span>



| <span data-ttu-id="2af0b-141">需求</span><span class="sxs-lookup"><span data-stu-id="2af0b-141">Requirement</span></span> | <span data-ttu-id="2af0b-142">值</span><span class="sxs-lookup"><span data-stu-id="2af0b-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2af0b-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2af0b-143">Minimum supported client</span></span><br/> | <span data-ttu-id="2af0b-144">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2af0b-144">Windows Vista \[desktop apps only\]</span></span><br/>                                                                                                                      |
| <span data-ttu-id="2af0b-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2af0b-145">Minimum supported server</span></span><br/> | <span data-ttu-id="2af0b-146">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2af0b-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                                |
| <span data-ttu-id="2af0b-147">標頭</span><span class="sxs-lookup"><span data-stu-id="2af0b-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="2af0b-148"><dt>NapTypes .h;</dt><dt>NapEnforcementClient .h</dt></span><span class="sxs-lookup"><span data-stu-id="2af0b-148"><dt>NapTypes.h; </dt> <dt>NapEnforcementClient.h</dt></span></span> </dl> |



 

