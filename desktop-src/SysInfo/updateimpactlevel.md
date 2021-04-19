---
description: 表示執行過時 OS 的裝置有高、中或低的影響。
ms.assetid: C7F30B63-66B0-4F37-A05B-7D366A12B640
title: UpdateImpactLevel 列舉
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UpdateImpactLevel
api_type:
- HeaderDef
api_location:
- waasapitypes.h
ms.openlocfilehash: c18cc7916abbc1dce595df9a21d2fdef3976af11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970225"
---
# <a name="updateimpactlevel-enumeration"></a><span data-ttu-id="dec6a-103">UpdateImpactLevel 列舉</span><span class="sxs-lookup"><span data-stu-id="dec6a-103">UpdateImpactLevel enumeration</span></span>

<span data-ttu-id="dec6a-104">表示執行過時 OS 的裝置有高、中或低的影響。</span><span class="sxs-lookup"><span data-stu-id="dec6a-104">Indicates a high, medium, or low impact of a device running an out-of-date OS.</span></span> <span data-ttu-id="dec6a-105">這個列舉通常是由 [**microsoft.intelligencepacks.updateassessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment)結構所使用，而這種結構接著會在 [**GetOSUpdateAssessment**](/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment)的傳回 [**OSUpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment)內進行嵌套。</span><span class="sxs-lookup"><span data-stu-id="dec6a-105">This enumeration is generally used by [**UpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) structures, which is in turn nested inside the returned [**OSUpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) from [**GetOSUpdateAssessment**](/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment).</span></span>

## <a name="syntax"></a><span data-ttu-id="dec6a-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="dec6a-106">Syntax</span></span>


```C++
typedef enum TagUpdateImpactLevel { 
      UpdateImpactLevel_None    = 0,
  UpdateImpactLevel_Low         = 1,
      UpdateImpactLevel_Medium  = 2,
  UpdateImpactLevel_High        = 3
} UpdateImpactLevel;
```



## <a name="constants"></a><span data-ttu-id="dec6a-107">常數</span><span class="sxs-lookup"><span data-stu-id="dec6a-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="dec6a-108"><span id="____UpdateImpactLevel_None"></span><span id="____updateimpactlevel_none"></span><span id="____UPDATEIMPACTLEVEL_NONE"></span>**UpdateImpactLevel \_無**</span><span class="sxs-lookup"><span data-stu-id="dec6a-108"><span id="____UpdateImpactLevel_None"></span><span id="____updateimpactlevel_none"></span><span id="____UPDATEIMPACTLEVEL_NONE"></span> **UpdateImpactLevel\_None**</span></span>
</dt> <dd>

<span data-ttu-id="dec6a-109">您的裝置沒有可預見的影響。</span><span class="sxs-lookup"><span data-stu-id="dec6a-109">There is no foreseeable impact to your device.</span></span> <span data-ttu-id="dec6a-110">這可能是因為裝置處於最新狀態或不是最新狀態，因為裝置正在接受其商務用 Windows Update 延遲期間，或已過期，但尚未達到 **daysOutOfDate** 閾值以達到較高的影響層級。</span><span class="sxs-lookup"><span data-stu-id="dec6a-110">This can be because the device is up-to-date, or is not up-to-date because the device is honoring its Windows Update for Business deferral periods, or is out-of-date but has not yet reached the **daysOutOfDate** threshold to reach a higher impact level.</span></span>

</dd> <dt>

<span data-ttu-id="dec6a-111"><span id="UpdateImpactLevel_Low"></span><span id="updateimpactlevel_low"></span><span id="UPDATEIMPACTLEVEL_LOW"></span>**UpdateImpactLevel \_ 低**</span><span class="sxs-lookup"><span data-stu-id="dec6a-111"><span id="UpdateImpactLevel_Low"></span><span id="updateimpactlevel_low"></span><span id="UPDATEIMPACTLEVEL_LOW"></span>**UpdateImpactLevel\_Low**</span></span>
</dt> <dd>

<span data-ttu-id="dec6a-112">裝置不是執行最新的作業系統，但有最近的更新。</span><span class="sxs-lookup"><span data-stu-id="dec6a-112">The device is not running the latest OS, but has a recent update.</span></span>

</dd> <dt>

<span data-ttu-id="dec6a-113"><span id="____UpdateImpactLevel_Medium"></span><span id="____updateimpactlevel_medium"></span><span id="____UPDATEIMPACTLEVEL_MEDIUM"></span>**UpdateImpactLevel \_中**</span><span class="sxs-lookup"><span data-stu-id="dec6a-113"><span id="____UpdateImpactLevel_Medium"></span><span id="____updateimpactlevel_medium"></span><span id="____UPDATEIMPACTLEVEL_MEDIUM"></span> **UpdateImpactLevel\_Medium**</span></span>
</dt> <dd>

<span data-ttu-id="dec6a-114">裝置正在執行最新的作業系統，但有較新的更新。</span><span class="sxs-lookup"><span data-stu-id="dec6a-114">The device is running the latest OS, but has a moderately recent update.</span></span>

</dd> <dt>

<span data-ttu-id="dec6a-115"><span id="UpdateImpactLevel_High"></span><span id="updateimpactlevel_high"></span><span id="UPDATEIMPACTLEVEL_HIGH"></span>**UpdateImpactLevel \_ High**</span><span class="sxs-lookup"><span data-stu-id="dec6a-115"><span id="UpdateImpactLevel_High"></span><span id="updateimpactlevel_high"></span><span id="UPDATEIMPACTLEVEL_HIGH"></span>**UpdateImpactLevel\_High**</span></span>
</dt> <dd>

<span data-ttu-id="dec6a-116">裝置已過期一段時間。</span><span class="sxs-lookup"><span data-stu-id="dec6a-116">The device has been out-of-date for a long time.</span></span> <span data-ttu-id="dec6a-117">此裝置可能有安全性弱點，可能會遺失讓 Windows 執行更好的重要修正。</span><span class="sxs-lookup"><span data-stu-id="dec6a-117">This device may have security vulnerabilities and may be missing important fixes that make Windows run better.</span></span> <span data-ttu-id="dec6a-118">當裝置正在執行不再支援的 Windows 版本時，一律會傳回 **UpdateImpactLevel \_ High** 。</span><span class="sxs-lookup"><span data-stu-id="dec6a-118">When a device is running a version of Windows that is no longer supported, **UpdateImpactLevel\_High** is always returned.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dec6a-119">備註</span><span class="sxs-lookup"><span data-stu-id="dec6a-119">Remarks</span></span>

<span data-ttu-id="dec6a-120">呼叫 [**GetOSUpdateAssessment**](/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment) 時，會傳回 [**OSUpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) 結構。</span><span class="sxs-lookup"><span data-stu-id="dec6a-120">When [**GetOSUpdateAssessment**](/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment) is called, an [**OSUpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) structure is returned.</span></span> <span data-ttu-id="dec6a-121">結構內有一個 **assessmentForCurrent** 和 **assessmentForUpToDate**。</span><span class="sxs-lookup"><span data-stu-id="dec6a-121">Within the structure there is an **assessmentForCurrent** and **assessmentForUpToDate**.</span></span> <span data-ttu-id="dec6a-122">這兩種都是 [**microsoft.intelligencepacks.updateassessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) 結構。</span><span class="sxs-lookup"><span data-stu-id="dec6a-122">Both of these are [**UpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) structures.</span></span> <span data-ttu-id="dec6a-123">這兩個成員都有 **UpdateImpactLevel** 列舉，表示執行過時 OS 之裝置的高、中、低或無影響。</span><span class="sxs-lookup"><span data-stu-id="dec6a-123">Both members have an **UpdateImpactLevel** enumeration, which indicates a high, medium, low or no impact for a device running an out-of-date OS.</span></span> <span data-ttu-id="dec6a-124">這些層級取決於 **daysOutOfDate** 的值。</span><span class="sxs-lookup"><span data-stu-id="dec6a-124">The These levels are determined by the value of **daysOutOfDate**.</span></span>

## <a name="requirements"></a><span data-ttu-id="dec6a-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="dec6a-125">Requirements</span></span>



| <span data-ttu-id="dec6a-126">需求</span><span class="sxs-lookup"><span data-stu-id="dec6a-126">Requirement</span></span> | <span data-ttu-id="dec6a-127">值</span><span class="sxs-lookup"><span data-stu-id="dec6a-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dec6a-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dec6a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="dec6a-129">Windows 10， \[ 僅限1703版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dec6a-129">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="dec6a-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dec6a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="dec6a-131">僅限 Windows Server 2016 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dec6a-131">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="dec6a-132">Idl</span><span class="sxs-lookup"><span data-stu-id="dec6a-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="dec6a-133"><dt>WaaSAPI .idl</dt></span><span class="sxs-lookup"><span data-stu-id="dec6a-133"><dt>WaaSAPI.idl</dt></span></span> </dl> |



 

 




