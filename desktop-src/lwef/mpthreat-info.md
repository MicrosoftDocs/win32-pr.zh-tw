---
title: 'MPTHREAT_INFO 結構 (MpClient .h) '
description: 包含威脅的相關資訊。
ms.assetid: ED2A0BDB-0E7C-479D-ADA1-95B9A259F57E
keywords:
- MPTHREAT_INFO 結構舊版 Windows 環境功能
- PMPTHREAT_INFO 結構指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPTHREAT_INFO
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfa850a4293006a2f4b107a3f2579fdc14c1ea6e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466656"
---
# <a name="mpthreat_info-structure"></a><span data-ttu-id="187f3-105">MPTHREAT \_ 資訊結構</span><span class="sxs-lookup"><span data-stu-id="187f3-105">MPTHREAT\_INFO structure</span></span>

<span data-ttu-id="187f3-106">包含威脅的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="187f3-106">Contains information about a threat.</span></span>

## <a name="syntax"></a><span data-ttu-id="187f3-107">語法</span><span class="sxs-lookup"><span data-stu-id="187f3-107">Syntax</span></span>


```C++
typedef struct tagMPTHREAT_INFO {
  MPTHREAT_ID           ThreatID;
  GUID                  DetectionID;
  MP_MIDL_STRING LPWSTR Name;
  MPTHREAT_TYPE         ThreatType;
  MPTHREAT_SEVERITY     ThreatCriticality;
  MPTHREAT_CATEGORY     ThreatCategory;
  DWORD                 ThreatShortDescriptionID;
  DWORD                 ThreatAdviseDescriptionID;
  MPTHREAT_STATUS       ThreatStatus;
  DWORD                 SuggestedActionCount;
  MPTHREAT_ACTION       SuggestedActionArray[MP_MAX_SUGGESTIONS];
  DWORD                 ResourceCount;
  PMPRESOURCE_INFO      *ResourceList[ResourceCount];
  ULARGE_INTEGER        ThreatStatusTime;
  HRESULT               ThreatStatusCode;
  MPTHREAT_DETECTION    ThreatDetection;
  GUID                  QuarantineGuid;
  MPEXECUTION_STATUS    ExecutionStatus;
  union {
    PMPTHREAT_INFOEX_UNUSED   pKnownBad;
    PMPTHREAT_INFOEX_BEHAVIOR pBehavior;
    PMPTHREAT_INFOEX_UNUSED   pUnknown;
    PMPTHREAT_INFOEX_UNUSED   pKnownGood;
    PMPTHREAT_INFOEX_NIS      pNis;
  } Data;
  MPDETECTION_STATE     State;
  MP_MIDL_STRING LPWSTR DetectionUser;
  MPSOURCE              DetectionSource;
  MP_MIDL_STRING LPWSTR ProcessName;
  MPDETECTION_ORIGIN    DetectionOrigin;
  DWORD                 reserved1;
  ULARGE_INTEGER        DetectionTime;
  MPEXECUTION_STATUS    PreExecutionStatus;
  ULARGE_INTEGER        RemediationTime;
  MPEXECUTION_STATUS    PostExecutionStatus;
  BOOL                  CriticalFailure;
  DWORD                 NonCriticalReason;
  MP_MIDL_STRING LPWSTR RemediationUser;
  DWORD                 RemediationResourceCount;
  PMPRESOURCE_INFO      RemediationResourceList[RemediationResourceCount];
  BOOL                  FailureResolved;
  MPRESOLVED_REASON     ResolvedReason;
  DWORD                 AdditionalActions;
  DWORD                 ResolvedActions;
  DWORD                 dwThreatStatusFlag;
} MPTHREAT_INFO, *PMPTHREAT_INFO;
```



## <a name="members"></a><span data-ttu-id="187f3-108">成員</span><span class="sxs-lookup"><span data-stu-id="187f3-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="187f3-109">**ThreatID**</span><span class="sxs-lookup"><span data-stu-id="187f3-109">**ThreatID**</span></span>
</dt> <dd>

<span data-ttu-id="187f3-110">類型： **MPTHREAT \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="187f3-110">Type: **MPTHREAT\_ID**</span></span>

</dd> <dd>

<span data-ttu-id="187f3-111">威脅識別碼。</span><span class="sxs-lookup"><span data-stu-id="187f3-111">Threat identifier.</span></span> <span data-ttu-id="187f3-112">設定用來識別防毒軟體相關威脅的位位。</span><span class="sxs-lookup"><span data-stu-id="187f3-112">Upper bit is set to identify antivirus-related threats.</span></span>

</dd> <dt>

<span data-ttu-id="187f3-113">**DetectionID**</span><span class="sxs-lookup"><span data-stu-id="187f3-113">**DetectionID**</span></span>
</dt> <dd>

<span data-ttu-id="187f3-114">類型： **GUID**</span><span class="sxs-lookup"><span data-stu-id="187f3-114">Type: **GUID**</span></span>

</dd> <dd>

<span data-ttu-id="187f3-115">偵測識別碼。</span><span class="sxs-lookup"><span data-stu-id="187f3-115">Detection ID.</span></span>

</dd> <dt>

<span data-ttu-id="187f3-116">**名稱**</span><span class="sxs-lookup"><span data-stu-id="187f3-116">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="187f3-117">類型： **MP \_ MIDL \_ STRING LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="187f3-117">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="187f3-118">威脅名稱。</span><span class="sxs-lookup"><span data-stu-id="187f3-118">Threat name.</span></span>

</dd> <dt>

<span data-ttu-id="187f3-119">**ThreatType**</span><span class="sxs-lookup"><span data-stu-id="187f3-119">**ThreatType**</span></span>
</dt> <dd>

<span data-ttu-id="187f3-120">類型： **[ **MPTHREAT \_ 類型**](mpthreat-type.md)**</span><span class="sxs-lookup"><span data-stu-id="187f3-120">Type: **[**MPTHREAT\_TYPE**](mpthreat-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="187f3-121">威脅類型。</span><span class="sxs-lookup"><span data-stu-id="187f3-121">Threat type.</span></span> <span data-ttu-id="187f3-122">用來區分不同的威脅類型，例如已知的不良、不明或已知良好。</span><span class="sxs-lookup"><span data-stu-id="187f3-122">Used to differentiate among different threat types such as known bad, unknown, or known good.</span></span> <span data-ttu-id="187f3-123">請參閱 [**MPTHREAT \_ 類型**](mpthreat-type.md)。</span><span class="sxs-lookup"><span data-stu-id="187f3-123">See [**MPTHREAT\_TYPE**](mpthreat-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="187f3-124">**ThreatCriticality**</span><span class="sxs-lookup"><span data-stu-id="187f3-124">**ThreatCriticality**</span></span>
</dt> <dd>

<span data-ttu-id="187f3-125">類型： **[ **MPTHREAT \_ 嚴重性**](mpthreat-severity.md)**</span><span class="sxs-lookup"><span data-stu-id="187f3-125">Type: **[**MPTHREAT\_SEVERITY**](mpthreat-severity.md)**</span></span>

</dd> <dd>

<span data-ttu-id="187f3-126">威脅重要性。</span><span class="sxs-lookup"><span data-stu-id="187f3-126">Threat criticality.</span></span> <span data-ttu-id="187f3-127">請參閱 [**MPTHREAT \_ 嚴重性**](mpthreat-severity.md)。</span><span class="sxs-lookup"><span data-stu-id="187f3-127">See [**MPTHREAT\_SEVERITY**](mpthreat-severity.md).</span></span>

</dd> <dt>

<span data-ttu-id="187f3-128">**ThreatCategory**</span><span class="sxs-lookup"><span data-stu-id="187f3-128">**ThreatCategory**</span></span>
</dt> <dd>

<span data-ttu-id="187f3-129">類型： **[ **MPTHREAT \_ 類別**](mpthreat-category.md)**</span><span class="sxs-lookup"><span data-stu-id="187f3-129">Type: **[**MPTHREAT\_CATEGORY**](mpthreat-category.md)**</span></span>

</dd> <dd>

<span data-ttu-id="187f3-130">威脅類別，例如特洛伊程式或 keylogger。</span><span class="sxs-lookup"><span data-stu-id="187f3-130">Threat category, such as a trojan or a keylogger.</span></span> <span data-ttu-id="187f3-131">請參閱 [**MPTHREAT \_ 類別**](mpthreat-category.md)。</span><span class="sxs-lookup"><span data-stu-id="187f3-131">See [**MPTHREAT\_CATEGORY**](mpthreat-category.md).</span></span>

</dd> <dt>

<span data-ttu-id="187f3-132">**ThreatShortDescriptionID**</span><span class="sxs-lookup"><span data-stu-id="187f3-132">**ThreatShortDescriptionID**</span></span>
</dt> <dd>

<span data-ttu-id="187f3-133">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="187f3-133">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="187f3-134">威脅簡短描述識別碼。</span><span class="sxs-lookup"><span data-stu-id="187f3-134">Threat short description ID.</span></span>

</dd> <dt>

<span data-ttu-id="187f3-135">**ThreatAdviseDescriptionID**</span><span class="sxs-lookup"><span data-stu-id="187f3-135">**ThreatAdviseDescriptionID**</span></span>
</dt> <dd>

<span data-ttu-id="187f3-136">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="187f3-136">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="187f3-137">威脅建議描述識別碼。</span><span class="sxs-lookup"><span data-stu-id="187f3-137">Threat advise description ID.</span></span>

</dd> <dt>

<span data-ttu-id="187f3-138">**ThreatStatus**</span><span class="sxs-lookup"><span data-stu-id="187f3-138">**ThreatStatus**</span></span>
</dt> <dd>

<span data-ttu-id="187f3-139">類型： **[ **MPTHREAT \_ 狀態**](mpthreat-status.md)**</span><span class="sxs-lookup"><span data-stu-id="187f3-139">Type: **[**MPTHREAT\_STATUS**](mpthreat-status.md)**</span></span>

</dd> <dd>

<span data-ttu-id="187f3-140">威脅狀態，例如偵測、清除或隔離。</span><span class="sxs-lookup"><span data-stu-id="187f3-140">Threat status such as detected, cleaned, or quarantined.</span></span> <span data-ttu-id="187f3-141">請參閱 [**MPTHREAT \_ 狀態**](mpthreat-status.md)。</span><span class="sxs-lookup"><span data-stu-id="187f3-141">See [**MPTHREAT\_STATUS**](mpthreat-status.md).</span></span>

</dd> <dt>

<span data-ttu-id="187f3-142">**SuggestedActionCount**</span><span class="sxs-lookup"><span data-stu-id="187f3-142">**SuggestedActionCount**</span></span>
</dt> <dd>

<span data-ttu-id="187f3-143">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="187f3-143">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="187f3-144">**SuggestedActionArray** 中的建議動作計數。</span><span class="sxs-lookup"><span data-stu-id="187f3-144">Count of suggested actions in **SuggestedActionArray**.</span></span>

</dd> <dt>

<span data-ttu-id="187f3-145">**SuggestedActionArray**</span><span class="sxs-lookup"><span data-stu-id="187f3-145">**SuggestedActionArray**</span></span>
</dt> <dd>

<span data-ttu-id="187f3-146">類型： **[**MPTHREAT \_ 動作**](mpthreat-action.md) \[ MP 的 \_ 最大 \_ 建議\]**</span><span class="sxs-lookup"><span data-stu-id="187f3-146">Type: **[**MPTHREAT\_ACTION**](mpthreat-action.md)\[MP\_MAX\_SUGGESTIONS\]**</span></span>

</dd> <dd>

<span data-ttu-id="187f3-147">建議動作的陣列。</span><span class="sxs-lookup"><span data-stu-id="187f3-147">Array of suggested actions.</span></span> <span data-ttu-id="187f3-148">請參閱 [**MPTHREAT \_ 動作**](mpthreat-action.md)。</span><span class="sxs-lookup"><span data-stu-id="187f3-148">See [**MPTHREAT\_ACTION**](mpthreat-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="187f3-149">**ResourceCount**</span><span class="sxs-lookup"><span data-stu-id="187f3-149">**ResourceCount**</span></span>
</dt> <dd>

<span data-ttu-id="187f3-150">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="187f3-150">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="187f3-151">**ResourceList** 中的資源計數。</span><span class="sxs-lookup"><span data-stu-id="187f3-151">Count of resources in **ResourceList**.</span></span>

</dd> <dt>

<span data-ttu-id="187f3-152">**ResourceList**</span><span class="sxs-lookup"><span data-stu-id="187f3-152">**ResourceList**</span></span>
</dt> <dd>

<span data-ttu-id="187f3-153">類型： \**PMPRESOURCE \_ INFO \** _</span><span class="sxs-lookup"><span data-stu-id="187f3-153">Type: \**PMPRESOURCE\_INFO\** _</span></span>

</dd> <dd>

<span data-ttu-id="187f3-154">已識別威脅的資源清單。</span><span class="sxs-lookup"><span data-stu-id="187f3-154">List of resources identified with the threat.</span></span> <span data-ttu-id="187f3-155">請參閱 [_ *MPRESOURCE \_ 資訊* \*](mpresource-info.md)。</span><span class="sxs-lookup"><span data-stu-id="187f3-155">See [_ *MPRESOURCE\_INFO*\*](mpresource-info.md).</span></span>

</dd> <dt>

<span data-ttu-id="187f3-156">**ThreatStatusTime**</span><span class="sxs-lookup"><span data-stu-id="187f3-156">**ThreatStatusTime**</span></span>
</dt> <dd>

<span data-ttu-id="187f3-157">類型： **ULARGE \_ 整數**</span><span class="sxs-lookup"><span data-stu-id="187f3-157">Type: **ULARGE\_INTEGER**</span></span>

</dd> <dd>

<span data-ttu-id="187f3-158">上次變更威脅狀態的時間。</span><span class="sxs-lookup"><span data-stu-id="187f3-158">Time when threat status last changed.</span></span>

</dd> <dt>

<span data-ttu-id="187f3-159">**ThreatStatusCode**</span><span class="sxs-lookup"><span data-stu-id="187f3-159">**ThreatStatusCode**</span></span>
</dt> <dd>

<span data-ttu-id="187f3-160">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="187f3-160">Type: **HRESULT**</span></span>

</dd> <dd>

<span data-ttu-id="187f3-161">與威脅狀態相關聯的狀態碼。</span><span class="sxs-lookup"><span data-stu-id="187f3-161">Status code associated with the threat status.</span></span>

</dd> <dt>

<span data-ttu-id="187f3-162">**ThreatDetection**</span><span class="sxs-lookup"><span data-stu-id="187f3-162">**ThreatDetection**</span></span>
</dt> <dd>

<span data-ttu-id="187f3-163">類型： **[ **MPTHREAT \_ 偵測**](mpthreat-detection.md)**</span><span class="sxs-lookup"><span data-stu-id="187f3-163">Type: **[**MPTHREAT\_DETECTION**](mpthreat-detection.md)**</span></span>

</dd> <dd>

<span data-ttu-id="187f3-164">威脅偵測類型，例如具體、可疑或泛型。</span><span class="sxs-lookup"><span data-stu-id="187f3-164">Threat detection type, such as concrete, suspicious, or generic.</span></span> <span data-ttu-id="187f3-165">請參閱 [**MPTHREAT \_ 偵測**](mpthreat-detection.md)。</span><span class="sxs-lookup"><span data-stu-id="187f3-165">See [**MPTHREAT\_DETECTION**](mpthreat-detection.md).</span></span>

</dd> <dt>

<span data-ttu-id="187f3-166">**QuarantineGuid**</span><span class="sxs-lookup"><span data-stu-id="187f3-166">**QuarantineGuid**</span></span>
</dt> <dd>

<span data-ttu-id="187f3-167">類型： **GUID**</span><span class="sxs-lookup"><span data-stu-id="187f3-167">Type: **GUID**</span></span>

</dd> <dd>

<span data-ttu-id="187f3-168">隔離 guid。</span><span class="sxs-lookup"><span data-stu-id="187f3-168">Quarantine guid.</span></span>

</dd> <dt>

<span data-ttu-id="187f3-169">**ExecutionStatus**</span><span class="sxs-lookup"><span data-stu-id="187f3-169">**ExecutionStatus**</span></span>
</dt> <dd>

<span data-ttu-id="187f3-170">類型： **[ **MPEXECUTION \_ 狀態**](mpexecution-status.md)**</span><span class="sxs-lookup"><span data-stu-id="187f3-170">Type: **[**MPEXECUTION\_STATUS**](mpexecution-status.md)**</span></span>

</dd> <dd>

<span data-ttu-id="187f3-171">威脅的執行狀態，例如「未知」、「已封鎖」或「作用中」。</span><span class="sxs-lookup"><span data-stu-id="187f3-171">Execution status of the threat, such as not known, blocked, or active.</span></span> <span data-ttu-id="187f3-172">請參閱 [**MPEXECUTION \_ 狀態**](mpexecution-status.md)。</span><span class="sxs-lookup"><span data-stu-id="187f3-172">See [**MPEXECUTION\_STATUS**](mpexecution-status.md).</span></span>

</dd> <dt>

<span data-ttu-id="187f3-173">**資料**</span><span class="sxs-lookup"><span data-stu-id="187f3-173">**Data**</span></span>
</dt> <dd>

<span data-ttu-id="187f3-174">額外資訊。</span><span class="sxs-lookup"><span data-stu-id="187f3-174">Extra information.</span></span> <span data-ttu-id="187f3-175">適當結構的指標取決於 **ThreatType** 的值。</span><span class="sxs-lookup"><span data-stu-id="187f3-175">The pointer to the appropriate structure depends on the value of **ThreatType**.</span></span>

<dl> <dt>

<span data-ttu-id="187f3-176">**pKnownBad**</span><span class="sxs-lookup"><span data-stu-id="187f3-176">**pKnownBad**</span></span>
</dt> <dd>

<span data-ttu-id="187f3-177">類型： **\_ \_ 未使用的 PMPTHREAT INFOEX**</span><span class="sxs-lookup"><span data-stu-id="187f3-177">Type: **PMPTHREAT\_INFOEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="187f3-178">當 **ThreatType**  ==  **MPTHREAT \_ 類型 \_ KNOWNBAD** 時。</span><span class="sxs-lookup"><span data-stu-id="187f3-178">When **ThreatType** == **MPTHREAT\_TYPE\_KNOWNBAD**.</span></span> <span data-ttu-id="187f3-179">請參閱 [**MPTHREAT \_ INFOEX \_ 未使用**](mpthreat-infoex-unused.md)。</span><span class="sxs-lookup"><span data-stu-id="187f3-179">See [**MPTHREAT\_INFOEX\_UNUSED**](mpthreat-infoex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="187f3-180">**pBehavior**</span><span class="sxs-lookup"><span data-stu-id="187f3-180">**pBehavior**</span></span>
</dt> <dd>

<span data-ttu-id="187f3-181">類型： **PMPTHREAT \_ INFOEX \_ 行為**</span><span class="sxs-lookup"><span data-stu-id="187f3-181">Type: **PMPTHREAT\_INFOEX\_BEHAVIOR**</span></span>

</dd> <dd>

<span data-ttu-id="187f3-182">**ThreatType**  ==  **MPTHREAT \_ 類型 \_ 行為** 時。</span><span class="sxs-lookup"><span data-stu-id="187f3-182">When **ThreatType** == **MPTHREAT\_TYPE\_BEHAVIOR**.</span></span> <span data-ttu-id="187f3-183">請參閱 [**MPTHREAT \_ INFOEX \_ 行為**](mpthreat-infoex-behavior.md)。</span><span class="sxs-lookup"><span data-stu-id="187f3-183">See [**MPTHREAT\_INFOEX\_BEHAVIOR**](mpthreat-infoex-behavior.md).</span></span>

</dd> <dt>

<span data-ttu-id="187f3-184">**pUnknown**</span><span class="sxs-lookup"><span data-stu-id="187f3-184">**pUnknown**</span></span>
</dt> <dd>

<span data-ttu-id="187f3-185">類型： **\_ \_ 未使用的 PMPTHREAT INFOEX**</span><span class="sxs-lookup"><span data-stu-id="187f3-185">Type: **PMPTHREAT\_INFOEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="187f3-186">當 **ThreatType**  ==  **MPTHREAT \_ 類型 \_ 未知** 時。</span><span class="sxs-lookup"><span data-stu-id="187f3-186">When **ThreatType** == **MPTHREAT\_TYPE\_UNKNOWN**.</span></span> <span data-ttu-id="187f3-187">請參閱 [**MPTHREAT \_ INFOEX \_ 未使用**](mpthreat-infoex-unused.md)。</span><span class="sxs-lookup"><span data-stu-id="187f3-187">See [**MPTHREAT\_INFOEX\_UNUSED**](mpthreat-infoex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="187f3-188">**pKnownGood**</span><span class="sxs-lookup"><span data-stu-id="187f3-188">**pKnownGood**</span></span>
</dt> <dd>

<span data-ttu-id="187f3-189">類型： **\_ \_ 未使用的 PMPTHREAT INFOEX**</span><span class="sxs-lookup"><span data-stu-id="187f3-189">Type: **PMPTHREAT\_INFOEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="187f3-190">當 **ThreatType** = = MPTHREAT \_ 類型 \_ KNOWNGOOD 時。</span><span class="sxs-lookup"><span data-stu-id="187f3-190">When **ThreatType** == MPTHREAT\_TYPE\_KNOWNGOOD.</span></span> <span data-ttu-id="187f3-191">請參閱 [**MPTHREAT \_ INFOEX \_ 未使用**](mpthreat-infoex-unused.md)。</span><span class="sxs-lookup"><span data-stu-id="187f3-191">See [**MPTHREAT\_INFOEX\_UNUSED**](mpthreat-infoex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="187f3-192">**pNis**</span><span class="sxs-lookup"><span data-stu-id="187f3-192">**pNis**</span></span>
</dt> <dd>

<span data-ttu-id="187f3-193">類型： **PMPTHREAT \_ INFOEX \_ NIS**</span><span class="sxs-lookup"><span data-stu-id="187f3-193">Type: **PMPTHREAT\_INFOEX\_NIS**</span></span>

</dd> <dd>

<span data-ttu-id="187f3-194">當 **ThreatType**  ==  **MPTHREAT \_ 類型 \_ NIS** 時。</span><span class="sxs-lookup"><span data-stu-id="187f3-194">When **ThreatType** == **MPTHREAT\_TYPE\_NIS**.</span></span> <span data-ttu-id="187f3-195">請參閱 [**MPTHREAT \_ INFOEX \_ NIS**](mpthreat-infoex-nis.md)。</span><span class="sxs-lookup"><span data-stu-id="187f3-195">See [**MPTHREAT\_INFOEX\_NIS**](mpthreat-infoex-nis.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="187f3-196">**State**</span><span class="sxs-lookup"><span data-stu-id="187f3-196">**State**</span></span>
</dt> <dd>

<span data-ttu-id="187f3-197">類型： **[ **MPDETECTION \_ 狀態**](mpdetection-state.md)**</span><span class="sxs-lookup"><span data-stu-id="187f3-197">Type: **[**MPDETECTION\_STATE**](mpdetection-state.md)**</span></span>

</dd> <dd>

<span data-ttu-id="187f3-198">偵測的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="187f3-198">The current state of the detection.</span></span> <span data-ttu-id="187f3-199">請參閱 [**MPDETECTION \_ 狀態**](mpdetection-state.md)。</span><span class="sxs-lookup"><span data-stu-id="187f3-199">See [**MPDETECTION\_STATE**](mpdetection-state.md).</span></span>

</dd> <dt>

<span data-ttu-id="187f3-200">**DetectionUser**</span><span class="sxs-lookup"><span data-stu-id="187f3-200">**DetectionUser**</span></span>
</dt> <dd>

<span data-ttu-id="187f3-201">類型： **MP \_ MIDL \_ STRING LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="187f3-201">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="187f3-202">與偵測相關聯的使用者，格式為 "domain/user"。</span><span class="sxs-lookup"><span data-stu-id="187f3-202">The user associated with the detection, in the format "domain/user".</span></span>

</dd> <dt>

<span data-ttu-id="187f3-203">**DetectionSource**</span><span class="sxs-lookup"><span data-stu-id="187f3-203">**DetectionSource**</span></span>
</dt> <dd>

<span data-ttu-id="187f3-204">類型： **[ **MPSOURCE**](mpsource.md)**</span><span class="sxs-lookup"><span data-stu-id="187f3-204">Type: **[**MPSOURCE**](mpsource.md)**</span></span>

</dd> <dd>

<span data-ttu-id="187f3-205">偵測的來源。</span><span class="sxs-lookup"><span data-stu-id="187f3-205">The source of the detection.</span></span> <span data-ttu-id="187f3-206">請參閱 [**MPSOURCE**](mpsource.md)。</span><span class="sxs-lookup"><span data-stu-id="187f3-206">See [**MPSOURCE**](mpsource.md).</span></span>

</dd> <dt>

<span data-ttu-id="187f3-207">**ProcessName**</span><span class="sxs-lookup"><span data-stu-id="187f3-207">**ProcessName**</span></span>
</dt> <dd>

<span data-ttu-id="187f3-208">類型： **MP \_ MIDL \_ STRING LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="187f3-208">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="187f3-209">與偵測相關聯的處理常式名稱。</span><span class="sxs-lookup"><span data-stu-id="187f3-209">Process name associated with the detection.</span></span>

</dd> <dt>

<span data-ttu-id="187f3-210">**DetectionOrigin**</span><span class="sxs-lookup"><span data-stu-id="187f3-210">**DetectionOrigin**</span></span>
</dt> <dd>

<span data-ttu-id="187f3-211">類型： **[ **MPDETECTION \_ 來源**](mpdetection-origin.md)**</span><span class="sxs-lookup"><span data-stu-id="187f3-211">Type: **[**MPDETECTION\_ORIGIN**](mpdetection-origin.md)**</span></span>

</dd> <dd>

<span data-ttu-id="187f3-212">偵測的來源，例如本機或網路。</span><span class="sxs-lookup"><span data-stu-id="187f3-212">The origin of the detection, such as local or network.</span></span> <span data-ttu-id="187f3-213">請參閱 [**MPDETECTION \_ 來源**](mpdetection-origin.md)。</span><span class="sxs-lookup"><span data-stu-id="187f3-213">See [**MPDETECTION\_ORIGIN**](mpdetection-origin.md).</span></span>

</dd> <dt>

<span data-ttu-id="187f3-214">**reserved1**</span><span class="sxs-lookup"><span data-stu-id="187f3-214">**reserved1**</span></span>
</dt> <dd>

<span data-ttu-id="187f3-215">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="187f3-215">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="187f3-216">關於偵測的保留中繼資料。</span><span class="sxs-lookup"><span data-stu-id="187f3-216">Reserved metadata about the detection.</span></span>

</dd> <dt>

<span data-ttu-id="187f3-217">**DetectionTime**</span><span class="sxs-lookup"><span data-stu-id="187f3-217">**DetectionTime**</span></span>
</dt> <dd>

<span data-ttu-id="187f3-218">類型： **ULARGE \_ 整數**</span><span class="sxs-lookup"><span data-stu-id="187f3-218">Type: **ULARGE\_INTEGER**</span></span>

</dd> <dd>

<span data-ttu-id="187f3-219">初始偵測的時間。</span><span class="sxs-lookup"><span data-stu-id="187f3-219">The time of the initial detection.</span></span>

</dd> <dt>

<span data-ttu-id="187f3-220">**PreExecutionStatus**</span><span class="sxs-lookup"><span data-stu-id="187f3-220">**PreExecutionStatus**</span></span>
</dt> <dd>

<span data-ttu-id="187f3-221">類型： **[ **MPEXECUTION \_ 狀態**](mpexecution-status.md)**</span><span class="sxs-lookup"><span data-stu-id="187f3-221">Type: **[**MPEXECUTION\_STATUS**](mpexecution-status.md)**</span></span>

</dd> <dd>

<span data-ttu-id="187f3-222">補救之前的執行狀態。</span><span class="sxs-lookup"><span data-stu-id="187f3-222">Execution status right before remediation.</span></span> <span data-ttu-id="187f3-223">請參閱 [**MPEXECUTION \_ 狀態**](mpexecution-status.md)。</span><span class="sxs-lookup"><span data-stu-id="187f3-223">See [**MPEXECUTION\_STATUS**](mpexecution-status.md).</span></span>

</dd> <dt>

<span data-ttu-id="187f3-224">**RemediationTime**</span><span class="sxs-lookup"><span data-stu-id="187f3-224">**RemediationTime**</span></span>
</dt> <dd>

<span data-ttu-id="187f3-225">類型： **ULARGE \_ 整數**</span><span class="sxs-lookup"><span data-stu-id="187f3-225">Type: **ULARGE\_INTEGER**</span></span>

</dd> <dd>

<span data-ttu-id="187f3-226">發生補救的時間。</span><span class="sxs-lookup"><span data-stu-id="187f3-226">The time remediation occured.</span></span>

</dd> <dt>

<span data-ttu-id="187f3-227">**PostExecutionStatus**</span><span class="sxs-lookup"><span data-stu-id="187f3-227">**PostExecutionStatus**</span></span>
</dt> <dd>

<span data-ttu-id="187f3-228">類型： **[ **MPEXECUTION \_ 狀態**](mpexecution-status.md)**</span><span class="sxs-lookup"><span data-stu-id="187f3-228">Type: **[**MPEXECUTION\_STATUS**](mpexecution-status.md)**</span></span>

</dd> <dd>

<span data-ttu-id="187f3-229">補救後的執行狀態。</span><span class="sxs-lookup"><span data-stu-id="187f3-229">Execution status after remediation.</span></span> <span data-ttu-id="187f3-230">請參閱 [**MPEXECUTION \_ 狀態**](mpexecution-status.md)。</span><span class="sxs-lookup"><span data-stu-id="187f3-230">See [**MPEXECUTION\_STATUS**](mpexecution-status.md).</span></span>

</dd> <dt>

<span data-ttu-id="187f3-231">**CriticalFailure**</span><span class="sxs-lookup"><span data-stu-id="187f3-231">**CriticalFailure**</span></span>
</dt> <dd>

<span data-ttu-id="187f3-232">類型： **BOOL**</span><span class="sxs-lookup"><span data-stu-id="187f3-232">Type: **BOOL**</span></span>

</dd> <dd>

<span data-ttu-id="187f3-233">如果補救失敗是嚴重的，則為 True。</span><span class="sxs-lookup"><span data-stu-id="187f3-233">True if the remediation failure was critical.</span></span>

</dd> <dt>

<span data-ttu-id="187f3-234">**NonCriticalReason**</span><span class="sxs-lookup"><span data-stu-id="187f3-234">**NonCriticalReason**</span></span>
</dt> <dd>

<span data-ttu-id="187f3-235">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="187f3-235">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="187f3-236">補救失敗的原因不重要。</span><span class="sxs-lookup"><span data-stu-id="187f3-236">The reason the remediation failure is not critical.</span></span> <span data-ttu-id="187f3-237">未來不一定會支援此功能。</span><span class="sxs-lookup"><span data-stu-id="187f3-237">This is not guaranteed to be supported in the future.</span></span>

</dd> <dt>

<span data-ttu-id="187f3-238">**RemediationUser**</span><span class="sxs-lookup"><span data-stu-id="187f3-238">**RemediationUser**</span></span>
</dt> <dd>

<span data-ttu-id="187f3-239">類型： **MP \_ MIDL \_ STRING LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="187f3-239">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="187f3-240">要求補救的使用者，格式為 "domain/user"。</span><span class="sxs-lookup"><span data-stu-id="187f3-240">User that requested the remediation, in the format "domain/user".</span></span>

</dd> <dt>

<span data-ttu-id="187f3-241">**RemediationResourceCount**</span><span class="sxs-lookup"><span data-stu-id="187f3-241">**RemediationResourceCount**</span></span>
</dt> <dd>

<span data-ttu-id="187f3-242">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="187f3-242">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="187f3-243">**RemediationResourceList** 中的資源計數。</span><span class="sxs-lookup"><span data-stu-id="187f3-243">Count of resources in **RemediationResourceList**.</span></span>

</dd> <dt>

<span data-ttu-id="187f3-244">**RemediationResourceList**</span><span class="sxs-lookup"><span data-stu-id="187f3-244">**RemediationResourceList**</span></span>
</dt> <dd>

<span data-ttu-id="187f3-245">類型： **PMPRESOURCE \_ INFO \[ RemediationResourceCount \]**</span><span class="sxs-lookup"><span data-stu-id="187f3-245">Type: **PMPRESOURCE\_INFO\[RemediationResourceCount\]**</span></span>

</dd> <dd>

<span data-ttu-id="187f3-246">修復期間失敗的資源清單。</span><span class="sxs-lookup"><span data-stu-id="187f3-246">List of resources that failed during remediation.</span></span> <span data-ttu-id="187f3-247">請參閱 [**MPRESOURCE \_ 資訊**](mpresource-info.md)。</span><span class="sxs-lookup"><span data-stu-id="187f3-247">See [**MPRESOURCE\_INFO**](mpresource-info.md).</span></span>

</dd> <dt>

<span data-ttu-id="187f3-248">**FailureResolved**</span><span class="sxs-lookup"><span data-stu-id="187f3-248">**FailureResolved**</span></span>
</dt> <dd>

<span data-ttu-id="187f3-249">類型： **BOOL**</span><span class="sxs-lookup"><span data-stu-id="187f3-249">Type: **BOOL**</span></span>

</dd> <dd>

<span data-ttu-id="187f3-250">如果已解決補救失敗，則為 True。</span><span class="sxs-lookup"><span data-stu-id="187f3-250">True if remediation failure been resolved.</span></span> <span data-ttu-id="187f3-251">這會將 bucket 移至完成或執行其他動作。</span><span class="sxs-lookup"><span data-stu-id="187f3-251">This will move the bucket to either complete or an additional action.</span></span>

</dd> <dt>

<span data-ttu-id="187f3-252">**ResolvedReason**</span><span class="sxs-lookup"><span data-stu-id="187f3-252">**ResolvedReason**</span></span>
</dt> <dd>

<span data-ttu-id="187f3-253">類型： **[ **MPRESOLVED \_ 原因**](mpresolved-reason.md)**</span><span class="sxs-lookup"><span data-stu-id="187f3-253">Type: **[**MPRESOLVED\_REASON**](mpresolved-reason.md)**</span></span>

</dd> <dd>

<span data-ttu-id="187f3-254">解決補救失敗的原因。</span><span class="sxs-lookup"><span data-stu-id="187f3-254">Reason for remediation failure being resolved.</span></span> <span data-ttu-id="187f3-255">這是偵測的移動原因無法執行其他動作或已完成。</span><span class="sxs-lookup"><span data-stu-id="187f3-255">This is the reason the detection moved from failed to additional action or finished.</span></span> <span data-ttu-id="187f3-256">請參閱 [**MPRESOLVED \_ 原因**](mpresolved-reason.md)。</span><span class="sxs-lookup"><span data-stu-id="187f3-256">See [**MPRESOLVED\_REASON**](mpresolved-reason.md).</span></span>

</dd> <dt>

<span data-ttu-id="187f3-257">**AdditionalActions**</span><span class="sxs-lookup"><span data-stu-id="187f3-257">**AdditionalActions**</span></span>
</dt> <dd>

<span data-ttu-id="187f3-258">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="187f3-258">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="187f3-259">需要額外的動作。</span><span class="sxs-lookup"><span data-stu-id="187f3-259">Are additional actions required.</span></span>

</dd> <dt>

<span data-ttu-id="187f3-260">**ResolvedActions**</span><span class="sxs-lookup"><span data-stu-id="187f3-260">**ResolvedActions**</span></span>
</dt> <dd>

<span data-ttu-id="187f3-261">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="187f3-261">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="187f3-262">已執行的任何其他動作。</span><span class="sxs-lookup"><span data-stu-id="187f3-262">Any additional actions that have been performed.</span></span>

</dd> <dt>

<span data-ttu-id="187f3-263">**dwThreatStatusFlag**</span><span class="sxs-lookup"><span data-stu-id="187f3-263">**dwThreatStatusFlag**</span></span>
</dt> <dd>

<span data-ttu-id="187f3-264">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="187f3-264">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="187f3-265">威脅偵測的額外資訊。</span><span class="sxs-lookup"><span data-stu-id="187f3-265">Additonal information about the threat detection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="187f3-266">規格需求</span><span class="sxs-lookup"><span data-stu-id="187f3-266">Requirements</span></span>



| <span data-ttu-id="187f3-267">需求</span><span class="sxs-lookup"><span data-stu-id="187f3-267">Requirement</span></span> | <span data-ttu-id="187f3-268">值</span><span class="sxs-lookup"><span data-stu-id="187f3-268">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="187f3-269">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="187f3-269">Minimum supported client</span></span><br/> | <span data-ttu-id="187f3-270">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="187f3-270">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="187f3-271">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="187f3-271">Minimum supported server</span></span><br/> | <span data-ttu-id="187f3-272">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="187f3-272">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="187f3-273">標頭</span><span class="sxs-lookup"><span data-stu-id="187f3-273">Header</span></span><br/>                   | <dl> <span data-ttu-id="187f3-274"><dt>MpClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="187f3-274"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="187f3-275">另請參閱</span><span class="sxs-lookup"><span data-stu-id="187f3-275">See also</span></span>

<dl> <dt>

[<span data-ttu-id="187f3-276">**MpFreeMemory**</span><span class="sxs-lookup"><span data-stu-id="187f3-276">**MpFreeMemory**</span></span>](mpfreememory.md)
</dt> <dt>

[<span data-ttu-id="187f3-277">**MpThreatEnumerate**</span><span class="sxs-lookup"><span data-stu-id="187f3-277">**MpThreatEnumerate**</span></span>](mpthreatenumerate.md)
</dt> <dt>

[<span data-ttu-id="187f3-278">**MpThreatQuery**</span><span class="sxs-lookup"><span data-stu-id="187f3-278">**MpThreatQuery**</span></span>](mpthreatquery.md)
</dt> <dt>

[<span data-ttu-id="187f3-279">**MPDETECTION \_ 來源**</span><span class="sxs-lookup"><span data-stu-id="187f3-279">**MPDETECTION\_ORIGIN**</span></span>](mpdetection-origin.md)
</dt> <dt>

[<span data-ttu-id="187f3-280">**MPDETECTION \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="187f3-280">**MPDETECTION\_STATE**</span></span>](mpdetection-state.md)
</dt> <dt>

[<span data-ttu-id="187f3-281">**MPEXECUTION \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="187f3-281">**MPEXECUTION\_STATUS**</span></span>](mpexecution-status.md)
</dt> <dt>

[<span data-ttu-id="187f3-282">**MPRESOLVED \_ 原因**</span><span class="sxs-lookup"><span data-stu-id="187f3-282">**MPRESOLVED\_REASON**</span></span>](mpresolved-reason.md)
</dt> <dt>

[<span data-ttu-id="187f3-283">**MPRESOURCE \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="187f3-283">**MPRESOURCE\_INFO**</span></span>](mpresource-info.md)
</dt> <dt>

[<span data-ttu-id="187f3-284">**MPSOURCE**</span><span class="sxs-lookup"><span data-stu-id="187f3-284">**MPSOURCE**</span></span>](mpsource.md)
</dt> <dt>

[<span data-ttu-id="187f3-285">**MPTHREAT \_ 動作**</span><span class="sxs-lookup"><span data-stu-id="187f3-285">**MPTHREAT\_ACTION**</span></span>](mpthreat-action.md)
</dt> <dt>

[<span data-ttu-id="187f3-286">**MPTHREAT \_ 類別**</span><span class="sxs-lookup"><span data-stu-id="187f3-286">**MPTHREAT\_CATEGORY**</span></span>](mpthreat-category.md)
</dt> <dt>

[<span data-ttu-id="187f3-287">**MPTHREAT \_ 偵測**</span><span class="sxs-lookup"><span data-stu-id="187f3-287">**MPTHREAT\_DETECTION**</span></span>](mpthreat-detection.md)
</dt> <dt>

[<span data-ttu-id="187f3-288">**MPTHREAT \_ INFOEX \_ 行為**</span><span class="sxs-lookup"><span data-stu-id="187f3-288">**MPTHREAT\_INFOEX\_BEHAVIOR**</span></span>](mpthreat-infoex-behavior.md)
</dt> <dt>

[<span data-ttu-id="187f3-289">**MPTHREAT \_ INFOEX \_ NIS**</span><span class="sxs-lookup"><span data-stu-id="187f3-289">**MPTHREAT\_INFOEX\_NIS**</span></span>](mpthreat-infoex-nis.md)
</dt> <dt>

[<span data-ttu-id="187f3-290">**\_ \_ 未使用的 MPTHREAT INFOEX**</span><span class="sxs-lookup"><span data-stu-id="187f3-290">**MPTHREAT\_INFOEX\_UNUSED**</span></span>](mpthreat-infoex-unused.md)
</dt> <dt>

[<span data-ttu-id="187f3-291">**MPTHREAT \_ 嚴重性**</span><span class="sxs-lookup"><span data-stu-id="187f3-291">**MPTHREAT\_SEVERITY**</span></span>](mpthreat-severity.md)
</dt> <dt>

[<span data-ttu-id="187f3-292">**MPTHREAT \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="187f3-292">**MPTHREAT\_STATUS**</span></span>](mpthreat-status.md)
</dt> <dt>

[<span data-ttu-id="187f3-293">**MPTHREAT \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="187f3-293">**MPTHREAT\_TYPE**</span></span>](mpthreat-type.md)
</dt> </dl>

 

 





