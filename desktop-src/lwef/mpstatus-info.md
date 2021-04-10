---
title: 'MPSTATUS_INFO 結構 (MpClient .h) '
description: 惡意程式碼防護管理員的狀態資訊。
ms.assetid: 614F14EC-64CC-4E3F-8A89-42AA1E0DC95D
keywords:
- MPSTATUS_INFO 結構舊版 Windows 環境功能
- PMPSTATUS_INFO 結構指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPSTATUS_INFO
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efe31981f819d85d13457553beb1ce3c869b98bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685565"
---
# <a name="mpstatus_info-structure"></a><span data-ttu-id="f0552-105">MPSTATUS \_ 資訊結構</span><span class="sxs-lookup"><span data-stu-id="f0552-105">MPSTATUS\_INFO structure</span></span>

<span data-ttu-id="f0552-106">惡意程式碼防護管理員的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="f0552-106">Status information for the malware protection manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0552-107">語法</span><span class="sxs-lookup"><span data-stu-id="f0552-107">Syntax</span></span>


```C++
typedef struct tagMPSTATUS_INFO {
  DWORD               ProductStatus;
  MPSCAN_RESULT       LastQuickScan;
  MPSCAN_RESULT       LastFullScan;
  MPTHREAT_STATS      ThreatStats;
  MPTHREAT_STATS_DATA ThreatState[MP_THREAT_STAT_MAX_VALUE+1];
  MPCOMPONENT_STATUS  Component[MPCOMPONENT_MAXVALUE+1];
  ULARGE_INTEGER      ProductExpirationTime;
} MPSTATUS_INFO, *PMPSTATUS_INFO;
```



## <a name="members"></a><span data-ttu-id="f0552-108">成員</span><span class="sxs-lookup"><span data-stu-id="f0552-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="f0552-109">**ProductStatus**</span><span class="sxs-lookup"><span data-stu-id="f0552-109">**ProductStatus**</span></span>
</dt> <dd>

<span data-ttu-id="f0552-110">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="f0552-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="f0552-111">整體產品狀態。</span><span class="sxs-lookup"><span data-stu-id="f0552-111">Overall product status.</span></span> <span data-ttu-id="f0552-112">這是 [**MPSTATUS \_ 旗**](mpstatus-flag.md)標的位旗標組合。</span><span class="sxs-lookup"><span data-stu-id="f0552-112">This is a combination of bit flags from [**MPSTATUS\_FLAG**](mpstatus-flag.md).</span></span>

</dd> <dt>

<span data-ttu-id="f0552-113">**LastQuickScan**</span><span class="sxs-lookup"><span data-stu-id="f0552-113">**LastQuickScan**</span></span>
</dt> <dd>

<span data-ttu-id="f0552-114">類型： **[ **MPSCAN \_ 結果**](mpscan-result.md)**</span><span class="sxs-lookup"><span data-stu-id="f0552-114">Type: **[**MPSCAN\_RESULT**](mpscan-result.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f0552-115">惡意程式碼防護管理員上次掃描的結果。</span><span class="sxs-lookup"><span data-stu-id="f0552-115">Results of the last scan by the malware protection manager.</span></span> <span data-ttu-id="f0552-116">請參閱 [**MPSCAN \_ 結果**](mpscan-result.md)。</span><span class="sxs-lookup"><span data-stu-id="f0552-116">See [**MPSCAN\_RESULT**](mpscan-result.md).</span></span>

</dd> <dt>

<span data-ttu-id="f0552-117">**LastFullScan**</span><span class="sxs-lookup"><span data-stu-id="f0552-117">**LastFullScan**</span></span>
</dt> <dd>

<span data-ttu-id="f0552-118">類型： **[ **MPSCAN \_ 結果**](mpscan-result.md)**</span><span class="sxs-lookup"><span data-stu-id="f0552-118">Type: **[**MPSCAN\_RESULT**](mpscan-result.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f0552-119">惡意程式碼防護管理員上次完整掃描的結果。</span><span class="sxs-lookup"><span data-stu-id="f0552-119">Results of the last full scan by the malware protection manager.</span></span> <span data-ttu-id="f0552-120">請參閱 [**MPSCAN \_ 結果**](mpscan-result.md)。</span><span class="sxs-lookup"><span data-stu-id="f0552-120">See [**MPSCAN\_RESULT**](mpscan-result.md).</span></span>

</dd> <dt>

<span data-ttu-id="f0552-121">**ThreatStats**</span><span class="sxs-lookup"><span data-stu-id="f0552-121">**ThreatStats**</span></span>
</dt> <dd>

<span data-ttu-id="f0552-122">類型： **[ **MPTHREAT \_ 統計** 資料](mpthreat-stats.md)**</span><span class="sxs-lookup"><span data-stu-id="f0552-122">Type: **[**MPTHREAT\_STATS**](mpthreat-stats.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f0552-123">作用中的威脅統計資料。</span><span class="sxs-lookup"><span data-stu-id="f0552-123">Active threat statistics.</span></span> <span data-ttu-id="f0552-124">請參閱 [**MPTHREAT \_ 統計**](mpthreat-stats.md)資料。</span><span class="sxs-lookup"><span data-stu-id="f0552-124">See [**MPTHREAT\_STATS**](mpthreat-stats.md).</span></span>

</dd> <dt>

<span data-ttu-id="f0552-125">**ThreatState**</span><span class="sxs-lookup"><span data-stu-id="f0552-125">**ThreatState**</span></span>
</dt> <dd>

<span data-ttu-id="f0552-126">類型： **[**MPTHREAT \_ STATS \_ DATA**](mpthreat-stats-data.md) \[ MP \_ 威脅 \_ STAT \_ 最大 \_ 值 + 1\]**</span><span class="sxs-lookup"><span data-stu-id="f0552-126">Type: **[**MPTHREAT\_STATS\_DATA**](mpthreat-stats-data.md)\[MP\_THREAT\_STAT\_MAX\_VALUE+1\]**</span></span>

</dd> <dd>

<span data-ttu-id="f0552-127">其他威脅統計資料，例如威脅數目。</span><span class="sxs-lookup"><span data-stu-id="f0552-127">Additional threat statistics data, such as the number of threats.</span></span> <span data-ttu-id="f0552-128">請參閱 [**MPTHREAT \_ 統計 \_ 資料**](mpthreat-stats-data.md)。</span><span class="sxs-lookup"><span data-stu-id="f0552-128">See [**MPTHREAT\_STATS\_DATA**](mpthreat-stats-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="f0552-129">**元件**</span><span class="sxs-lookup"><span data-stu-id="f0552-129">**Component**</span></span>
</dt> <dd>

<span data-ttu-id="f0552-130">類型： **[**MPCOMPONENT \_ STATUS**](mpcomponent-status.md) \[ MPCOMPONENT int32.maxvalue \_ + 1\]**</span><span class="sxs-lookup"><span data-stu-id="f0552-130">Type: **[**MPCOMPONENT\_STATUS**](mpcomponent-status.md)\[MPCOMPONENT\_MAXVALUE+1\]**</span></span>

</dd> <dd>

<span data-ttu-id="f0552-131">多個元件的狀態陣列。</span><span class="sxs-lookup"><span data-stu-id="f0552-131">An array of statuses for multiple components.</span></span> <span data-ttu-id="f0552-132">使用 [**MPCOMPONENT \_ ID**](mpcomponent-id.md) 列舉中的值做為陣列中的索引。</span><span class="sxs-lookup"><span data-stu-id="f0552-132">Use a value from the [**MPCOMPONENT\_ID**](mpcomponent-id.md) enumeration as an index into the array.</span></span>

</dd> <dt>

<span data-ttu-id="f0552-133">**ProductExpirationTime**</span><span class="sxs-lookup"><span data-stu-id="f0552-133">**ProductExpirationTime**</span></span>
</dt> <dd>

<span data-ttu-id="f0552-134">類型： **ULARGE \_ 整數**</span><span class="sxs-lookup"><span data-stu-id="f0552-134">Type: **ULARGE\_INTEGER**</span></span>

</dd> <dd>

<span data-ttu-id="f0552-135">UNC 中的產品到期時間戳記。</span><span class="sxs-lookup"><span data-stu-id="f0552-135">Product expiration timestamp in UNC.</span></span> <span data-ttu-id="f0552-136">只有在已設定到期狀態時，這才有效。</span><span class="sxs-lookup"><span data-stu-id="f0552-136">This is valid only if the expiration status is set.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f0552-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="f0552-137">Requirements</span></span>



| <span data-ttu-id="f0552-138">需求</span><span class="sxs-lookup"><span data-stu-id="f0552-138">Requirement</span></span> | <span data-ttu-id="f0552-139">值</span><span class="sxs-lookup"><span data-stu-id="f0552-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f0552-140">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f0552-140">Minimum supported client</span></span><br/> | <span data-ttu-id="f0552-141">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f0552-141">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="f0552-142">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f0552-142">Minimum supported server</span></span><br/> | <span data-ttu-id="f0552-143">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f0552-143">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f0552-144">標頭</span><span class="sxs-lookup"><span data-stu-id="f0552-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0552-145"><dt>MpClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="f0552-145"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0552-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f0552-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0552-147">**MPCOMPONENT \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="f0552-147">**MPCOMPONENT\_ID**</span></span>](mpcomponent-id.md)
</dt> <dt>

[<span data-ttu-id="f0552-148">**MPCOMPONENT \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="f0552-148">**MPCOMPONENT\_STATUS**</span></span>](mpcomponent-status.md)
</dt> <dt>

[<span data-ttu-id="f0552-149">**MPSCAN \_ 結果**</span><span class="sxs-lookup"><span data-stu-id="f0552-149">**MPSCAN\_RESULT**</span></span>](mpscan-result.md)
</dt> <dt>

[<span data-ttu-id="f0552-150">**MPSTATUS \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="f0552-150">**MPSTATUS\_FLAG**</span></span>](mpstatus-flag.md)
</dt> <dt>

[<span data-ttu-id="f0552-151">**MPTHREAT \_ 統計資料**</span><span class="sxs-lookup"><span data-stu-id="f0552-151">**MPTHREAT\_STATS**</span></span>](mpthreat-stats.md)
</dt> <dt>

[<span data-ttu-id="f0552-152">**MPTHREAT \_ 統計 \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="f0552-152">**MPTHREAT\_STATS\_DATA**</span></span>](mpthreat-stats-data.md)
</dt> </dl>

 

 





