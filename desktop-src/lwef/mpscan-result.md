---
title: 'MPSCAN_RESULT 結構 (MpClient .h) '
description: 掃描的結果。
ms.assetid: 9031A371-092A-4175-BE1D-90442A5BED2D
keywords:
- MPSCAN_RESULT 結構舊版 Windows 環境功能
- PMPSCAN_RESULT 結構指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPSCAN_RESULT
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7be60df7993732bafcd7c44ac2fb581c111aed6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104187315"
---
# <a name="mpscan_result-structure"></a><span data-ttu-id="6b60a-105">MPSCAN \_ 結果結構</span><span class="sxs-lookup"><span data-stu-id="6b60a-105">MPSCAN\_RESULT structure</span></span>

<span data-ttu-id="6b60a-106">掃描的結果。</span><span class="sxs-lookup"><span data-stu-id="6b60a-106">The results of a scan.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b60a-107">語法</span><span class="sxs-lookup"><span data-stu-id="6b60a-107">Syntax</span></span>


```C++
typedef struct tagMPSCAN_RESULT {
  MPSCAN_TYPE      ScanType;
  MPSOURCE         Source;
  GUID             ScanGuid;
  ULARGE_INTEGER   StartTime;
  ULARGE_INTEGER   EndTime;
  MPTHREAT_STATS   ThreatStats;
  MPRESOURCE_STATS ResourceStats;
  ULONGLONG        SignatureVersion;
} MPSCAN_RESULT, *PMPSCAN_RESULT;
```



## <a name="members"></a><span data-ttu-id="6b60a-108">成員</span><span class="sxs-lookup"><span data-stu-id="6b60a-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="6b60a-109">**ScanType**</span><span class="sxs-lookup"><span data-stu-id="6b60a-109">**ScanType**</span></span>
</dt> <dd>

<span data-ttu-id="6b60a-110">類型： **[ **MPSCAN \_ 類型**](mpscan-type.md)**</span><span class="sxs-lookup"><span data-stu-id="6b60a-110">Type: **[**MPSCAN\_TYPE**](mpscan-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6b60a-111">掃描類型。</span><span class="sxs-lookup"><span data-stu-id="6b60a-111">Scan type.</span></span> <span data-ttu-id="6b60a-112">請參閱 [**MPSCAN \_ 類型**](mpscan-type.md)。</span><span class="sxs-lookup"><span data-stu-id="6b60a-112">See [**MPSCAN\_TYPE**](mpscan-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b60a-113">**來源**</span><span class="sxs-lookup"><span data-stu-id="6b60a-113">**Source**</span></span>
</dt> <dd>

<span data-ttu-id="6b60a-114">類型： **[ **MPSOURCE**](mpsource.md)**</span><span class="sxs-lookup"><span data-stu-id="6b60a-114">Type: **[**MPSOURCE**](mpsource.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6b60a-115">掃描來源，例如使用者或系統起始。</span><span class="sxs-lookup"><span data-stu-id="6b60a-115">Scan source, such as user or system initiated.</span></span> <span data-ttu-id="6b60a-116">請參閱 [**MPSOURCE**](mpsource.md)。</span><span class="sxs-lookup"><span data-stu-id="6b60a-116">See [**MPSOURCE**](mpsource.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b60a-117">**ScanGuid**</span><span class="sxs-lookup"><span data-stu-id="6b60a-117">**ScanGuid**</span></span>
</dt> <dd>

<span data-ttu-id="6b60a-118">類型： **GUID**</span><span class="sxs-lookup"><span data-stu-id="6b60a-118">Type: **GUID**</span></span>

</dd> <dd>

<span data-ttu-id="6b60a-119">掃描識別碼。</span><span class="sxs-lookup"><span data-stu-id="6b60a-119">Scan identifier.</span></span>

</dd> <dt>

<span data-ttu-id="6b60a-120">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="6b60a-120">**StartTime**</span></span>
</dt> <dd>

<span data-ttu-id="6b60a-121">類型： **ULARGE \_ 整數**</span><span class="sxs-lookup"><span data-stu-id="6b60a-121">Type: **ULARGE\_INTEGER**</span></span>

</dd> <dd>

<span data-ttu-id="6b60a-122">掃描開始時間。</span><span class="sxs-lookup"><span data-stu-id="6b60a-122">Scan start time.</span></span>

</dd> <dt>

<span data-ttu-id="6b60a-123">**EndTime**</span><span class="sxs-lookup"><span data-stu-id="6b60a-123">**EndTime**</span></span>
</dt> <dd>

<span data-ttu-id="6b60a-124">類型： **ULARGE \_ 整數**</span><span class="sxs-lookup"><span data-stu-id="6b60a-124">Type: **ULARGE\_INTEGER**</span></span>

</dd> <dd>

<span data-ttu-id="6b60a-125">掃描結束時間。</span><span class="sxs-lookup"><span data-stu-id="6b60a-125">Scan end time.</span></span>

</dd> <dt>

<span data-ttu-id="6b60a-126">**ThreatStats**</span><span class="sxs-lookup"><span data-stu-id="6b60a-126">**ThreatStats**</span></span>
</dt> <dd>

<span data-ttu-id="6b60a-127">類型： **[ **MPTHREAT \_ 統計** 資料](mpthreat-stats.md)**</span><span class="sxs-lookup"><span data-stu-id="6b60a-127">Type: **[**MPTHREAT\_STATS**](mpthreat-stats.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6b60a-128">威脅相關的統計資料。</span><span class="sxs-lookup"><span data-stu-id="6b60a-128">Threat-related statistics.</span></span> <span data-ttu-id="6b60a-129">請參閱 [**MPTHREAT \_ 統計**](mpthreat-stats.md)資料。</span><span class="sxs-lookup"><span data-stu-id="6b60a-129">See [**MPTHREAT\_STATS**](mpthreat-stats.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b60a-130">**ResourceStats**</span><span class="sxs-lookup"><span data-stu-id="6b60a-130">**ResourceStats**</span></span>
</dt> <dd>

<span data-ttu-id="6b60a-131">類型： **[ **MPRESOURCE \_ 統計** 資料](mpresource-stats.md)**</span><span class="sxs-lookup"><span data-stu-id="6b60a-131">Type: **[**MPRESOURCE\_STATS**](mpresource-stats.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6b60a-132">與資源相關的統計資料。</span><span class="sxs-lookup"><span data-stu-id="6b60a-132">Resource-related statistics.</span></span> <span data-ttu-id="6b60a-133">請參閱 [**MPRESOURCE \_ 統計**](mpresource-stats.md)資料。</span><span class="sxs-lookup"><span data-stu-id="6b60a-133">See [**MPRESOURCE\_STATS**](mpresource-stats.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b60a-134">**SignatureVersion**</span><span class="sxs-lookup"><span data-stu-id="6b60a-134">**SignatureVersion**</span></span>
</dt> <dd>

<span data-ttu-id="6b60a-135">類型： **ULONGLONG**</span><span class="sxs-lookup"><span data-stu-id="6b60a-135">Type: **ULONGLONG**</span></span>

</dd> <dd>

<span data-ttu-id="6b60a-136">用於掃描的簽章版本。</span><span class="sxs-lookup"><span data-stu-id="6b60a-136">Version of signature used for scan.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6b60a-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="6b60a-137">Requirements</span></span>



| <span data-ttu-id="6b60a-138">需求</span><span class="sxs-lookup"><span data-stu-id="6b60a-138">Requirement</span></span> | <span data-ttu-id="6b60a-139">值</span><span class="sxs-lookup"><span data-stu-id="6b60a-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6b60a-140">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6b60a-140">Minimum supported client</span></span><br/> | <span data-ttu-id="6b60a-141">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6b60a-141">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="6b60a-142">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6b60a-142">Minimum supported server</span></span><br/> | <span data-ttu-id="6b60a-143">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6b60a-143">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6b60a-144">標頭</span><span class="sxs-lookup"><span data-stu-id="6b60a-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b60a-145"><dt>MpClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="6b60a-145"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b60a-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6b60a-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b60a-147">**MPRESOURCE \_ 統計資料**</span><span class="sxs-lookup"><span data-stu-id="6b60a-147">**MPRESOURCE\_STATS**</span></span>](mpresource-stats.md)
</dt> <dt>

[<span data-ttu-id="6b60a-148">**MPSCAN \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="6b60a-148">**MPSCAN\_TYPE**</span></span>](mpscan-type.md)
</dt> <dt>

[<span data-ttu-id="6b60a-149">**MPSOURCE**</span><span class="sxs-lookup"><span data-stu-id="6b60a-149">**MPSOURCE**</span></span>](mpsource.md)
</dt> <dt>

[<span data-ttu-id="6b60a-150">**MPTHREAT \_ 統計資料**</span><span class="sxs-lookup"><span data-stu-id="6b60a-150">**MPTHREAT\_STATS**</span></span>](mpthreat-stats.md)
</dt> </dl>

 

 





