---
description: 描述裝置上作業系統的最新狀態。
ms.assetid: 157E241E-E8D8-41F8-9565-5C9298DCD1BE
title: UpdateAssessmentStatus 列舉
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UpdateAssessmentStatus
api_type:
- HeaderDef
api_location:
- waasapitypes.h
ms.openlocfilehash: 790077118db7704bdd04801758f44cbb50cc54b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974943"
---
# <a name="updateassessmentstatus-enumeration"></a><span data-ttu-id="0b43b-103">UpdateAssessmentStatus 列舉</span><span class="sxs-lookup"><span data-stu-id="0b43b-103">UpdateAssessmentStatus enumeration</span></span>

<span data-ttu-id="0b43b-104">描述裝置上作業系統的最新狀態。</span><span class="sxs-lookup"><span data-stu-id="0b43b-104">Describes how up-to-date the OS on a device is.</span></span> <span data-ttu-id="0b43b-105">**UpdateAssessmentStatus** 可供 [**microsoft.intelligencepacks.updateassessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) 和 [**OSUpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) 結構、 **assessmentForCurrent**、 **assessmentForUpToDate** 和 **securityStatus** 成員使用。</span><span class="sxs-lookup"><span data-stu-id="0b43b-105">**UpdateAssessmentStatus** is used by the [**UpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) and [**OSUpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) structures, in the **assessmentForCurrent**, **assessmentForUpToDate**, and **securityStatus** members.</span></span> <span data-ttu-id="0b43b-106">只會傳回一個常數。</span><span class="sxs-lookup"><span data-stu-id="0b43b-106">Exactly one constant is returned.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b43b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0b43b-107">Syntax</span></span>


```C++
typedef enum TagUpdateAssessmentStatus { 
      UpdateAssessmentStatus_Latest                    = 0,
      UpdateAssessmentStatus_NotLatestSoftRestriction  = 1,
      UpdateAssessmentStatus_NotLatestHardRestriction  = 2,
      UpdateAssessmentStatus_NotLatestEndOfSupport     = 3,
      UpdateAssessmentStatus_NotLatestServicingTrain   = 4,
      UpdateAssessmentStatus_NotLatestDeferredFeature  = 5,
      UpdateAssessmentStatus_NotLatestDeferredQuality  = 6,
      UpdateAssessmentStatus_NotLatestPausedFeature    = 7,
      UpdateAssessmentStatus_NotLatestPausedQuality    = 8,
      UpdateAssessmentStatus_NotLatestManaged          = 9,
      UpdateAssessmentStatus_NotLatestUnknown          = 10,
      UpdateAssessmentStatus_NotLatestTargetedVersion  = 11
} UpdateAssessmentStatus;
```



## <a name="constants"></a><span data-ttu-id="0b43b-108">常數</span><span class="sxs-lookup"><span data-stu-id="0b43b-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="0b43b-109"><span id="____UpdateAssessmentStatus_Latest"></span><span id="____updateassessmentstatus_latest"></span><span id="____UPDATEASSESSMENTSTATUS_LATEST"></span>**UpdateAssessmentStatus \_最新**</span><span class="sxs-lookup"><span data-stu-id="0b43b-109"><span id="____UpdateAssessmentStatus_Latest"></span><span id="____updateassessmentstatus_latest"></span><span id="____UPDATEASSESSMENTSTATUS_LATEST"></span> **UpdateAssessmentStatus\_Latest**</span></span>
</dt> <dd>

<span data-ttu-id="0b43b-110">**AssessmentForCurrent** 中的這項結果表示裝置處於適用于該裝置的最新功能更新和品質更新。</span><span class="sxs-lookup"><span data-stu-id="0b43b-110">This result within **assessmentForCurrent** implies that the device is on the latest feature update and quality update available for that device.</span></span> <span data-ttu-id="0b43b-111">在 **assessmentForUpToDate** 中，此結果表示裝置處於正在執行之 Windows 版本的最新品質更新。</span><span class="sxs-lookup"><span data-stu-id="0b43b-111">Within **assessmentForUpToDate**, this result implies that the device is on the latest quality update for the release of Windows it is running.</span></span>

</dd> <dt>

<span data-ttu-id="0b43b-112"><span id="____UpdateAssessmentStatus_NotLatestSoftRestriction"></span><span id="____updateassessmentstatus_notlatestsoftrestriction"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTSOFTRESTRICTION"></span>**UpdateAssessmentStatus \_NotLatestSoftRestriction**</span><span class="sxs-lookup"><span data-stu-id="0b43b-112"><span id="____UpdateAssessmentStatus_NotLatestSoftRestriction"></span><span id="____updateassessmentstatus_notlatestsoftrestriction"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTSOFTRESTRICTION"></span> **UpdateAssessmentStatus\_NotLatestSoftRestriction**</span></span>
</dt> <dd>

<span data-ttu-id="0b43b-113">因為有軟限制，所以尚未安裝最新的功能更新。</span><span class="sxs-lookup"><span data-stu-id="0b43b-113">The latest feature update has not been installed due to a soft restriction.</span></span> <span data-ttu-id="0b43b-114">將軟限制放置於更新時，將不會自動安裝更新;使用者必須在 Update UX 內自行起始下載。</span><span class="sxs-lookup"><span data-stu-id="0b43b-114">When a soft restriction has been placed on an update, the update will not be automatically installed; a user must self-initiate the download within the Update UX.</span></span> <span data-ttu-id="0b43b-115">此狀態只適用于 **assessmentForCurrent**。</span><span class="sxs-lookup"><span data-stu-id="0b43b-115">This status only applies to **assessmentForCurrent**.</span></span>

</dd> <dt>

<span data-ttu-id="0b43b-116"><span id="____UpdateAssessmentStatus_NotLatestHardRestriction"></span><span id="____updateassessmentstatus_notlatesthardrestriction"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTHARDRESTRICTION"></span>**UpdateAssessmentStatus \_NotLatestHardRestriction**</span><span class="sxs-lookup"><span data-stu-id="0b43b-116"><span id="____UpdateAssessmentStatus_NotLatestHardRestriction"></span><span id="____updateassessmentstatus_notlatesthardrestriction"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTHARDRESTRICTION"></span> **UpdateAssessmentStatus\_NotLatestHardRestriction**</span></span>
</dt> <dd>

<span data-ttu-id="0b43b-117">尚未安裝最新的功能更新，因為有硬性限制。</span><span class="sxs-lookup"><span data-stu-id="0b43b-117">The latest feature update has not been installed due to a hard restriction.</span></span> <span data-ttu-id="0b43b-118">當對更新進行硬性限制時，該更新就不適用裝置。</span><span class="sxs-lookup"><span data-stu-id="0b43b-118">When a hard restriction has been placed on an update, the update is not applicable to the device.</span></span> <span data-ttu-id="0b43b-119">此狀態只適用于 **assessmentForCurrent**。</span><span class="sxs-lookup"><span data-stu-id="0b43b-119">This status only applies to **assessmentForCurrent**.</span></span>

</dd> <dt>

<span data-ttu-id="0b43b-120"><span id="____UpdateAssessmentStatus_NotLatestEndOfSupport"></span><span id="____updateassessmentstatus_notlatestendofsupport"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTENDOFSUPPORT"></span>**UpdateAssessmentStatus \_NotLatestEndOfSupport**</span><span class="sxs-lookup"><span data-stu-id="0b43b-120"><span id="____UpdateAssessmentStatus_NotLatestEndOfSupport"></span><span id="____updateassessmentstatus_notlatestendofsupport"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTENDOFSUPPORT"></span> **UpdateAssessmentStatus\_NotLatestEndOfSupport**</span></span>
</dt> <dd>

<span data-ttu-id="0b43b-121">裝置不在最新的更新中，因為 Microsoft 已不再支援裝置的功能更新。</span><span class="sxs-lookup"><span data-stu-id="0b43b-121">The device is not on the latest update because the device's feature update is no longer supported by Microsoft.</span></span> <span data-ttu-id="0b43b-122">當 Microsoft 停止支援功能版本時， **assessmentForCurrent** 和 **assessmentForUpToDate** 都會傳回此狀態。</span><span class="sxs-lookup"><span data-stu-id="0b43b-122">When Microsoft stops supporting a feature release, this status will be returned for both **assessmentForCurrent** and **assessmentForUpToDate**.</span></span>

> [!Note]  
> <span data-ttu-id="0b43b-123">傳回 **UpdateAssessmentStatus \_ NotLatestEndOfSupport** 時，評量的 **UpdateImpactLevel** 一律 **UpdateImpactLevel \_ High**。</span><span class="sxs-lookup"><span data-stu-id="0b43b-123">When **UpdateAssessmentStatus\_NotLatestEndOfSupport** is returned, the assessment's **UpdateImpactLevel** is always **UpdateImpactLevel\_High**.</span></span>

 

</dd> <dt>

<span data-ttu-id="0b43b-124"><span id="____UpdateAssessmentStatus_NotLatestServicingTrain"></span><span id="____updateassessmentstatus_notlatestservicingtrain"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTSERVICINGTRAIN"></span>**UpdateAssessmentStatus \_NotLatestServicingTrain**</span><span class="sxs-lookup"><span data-stu-id="0b43b-124"><span id="____UpdateAssessmentStatus_NotLatestServicingTrain"></span><span id="____updateassessmentstatus_notlatestservicingtrain"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTSERVICINGTRAIN"></span> **UpdateAssessmentStatus\_NotLatestServicingTrain**</span></span>
</dt> <dd>

<span data-ttu-id="0b43b-125">裝置不在最新的功能更新上，因為裝置的服務訓練會限制裝置無法更新至最新的功能更新。</span><span class="sxs-lookup"><span data-stu-id="0b43b-125">The device is not on the latest feature update because the device's servicing train limits the device from updating to the latest feature update.</span></span> <span data-ttu-id="0b43b-126">例如：如果裝置位於最新商務分支 (CBB) 且已針對最新分支 (CB) 發行新的功能更新，將會傳回這項功能。</span><span class="sxs-lookup"><span data-stu-id="0b43b-126">For example: if a device is on Current Branch for Business (CBB) and a new feature update has been released for Current Branch (CB), this will be returned.</span></span> <span data-ttu-id="0b43b-127">此狀態只適用于 **assessmentForCurrent**。</span><span class="sxs-lookup"><span data-stu-id="0b43b-127">This status only applies to **assessmentForCurrent**.</span></span>

</dd> <dt>

<span data-ttu-id="0b43b-128"><span id="____UpdateAssessmentStatus_NotLatestDeferredFeature"></span><span id="____updateassessmentstatus_notlatestdeferredfeature"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTDEFERREDFEATURE"></span>**UpdateAssessmentStatus \_NotLatestDeferredFeature**</span><span class="sxs-lookup"><span data-stu-id="0b43b-128"><span id="____UpdateAssessmentStatus_NotLatestDeferredFeature"></span><span id="____updateassessmentstatus_notlatestdeferredfeature"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTDEFERREDFEATURE"></span> **UpdateAssessmentStatus\_NotLatestDeferredFeature**</span></span>
</dt> <dd>

<span data-ttu-id="0b43b-129">由於裝置的商務用 Windows Update 功能更新延遲原則，尚未安裝最新的功能更新。</span><span class="sxs-lookup"><span data-stu-id="0b43b-129">The latest feature update has not been installed due to the device's Windows Update for Business Feature Update Deferral policy.</span></span> <span data-ttu-id="0b43b-130">判斷 **daysOutOfDate** 會考慮延遲原則;在延遲期間過期之前， **daysOutOfDate** 不會開始遞增。</span><span class="sxs-lookup"><span data-stu-id="0b43b-130">Determining **daysOutOfDate** takes into account deferral policies; **daysOutOfDate** will not begin incrementing until the deferral period has expired.</span></span> <span data-ttu-id="0b43b-131">此狀態只適用于 **assessmentForCurrent**。</span><span class="sxs-lookup"><span data-stu-id="0b43b-131">This status only applies to **assessmentForCurrent**.</span></span>

</dd> <dt>

<span data-ttu-id="0b43b-132"><span id="____UpdateAssessmentStatus_NotLatestDeferredQuality"></span><span id="____updateassessmentstatus_notlatestdeferredquality"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTDEFERREDQUALITY"></span>**UpdateAssessmentStatus \_NotLatestDeferredQuality**</span><span class="sxs-lookup"><span data-stu-id="0b43b-132"><span id="____UpdateAssessmentStatus_NotLatestDeferredQuality"></span><span id="____updateassessmentstatus_notlatestdeferredquality"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTDEFERREDQUALITY"></span> **UpdateAssessmentStatus\_NotLatestDeferredQuality**</span></span>
</dt> <dd>

<span data-ttu-id="0b43b-133">裝置因為裝置的商務用 Windows Update 品質更新延遲原則，而不是最新的品質更新。</span><span class="sxs-lookup"><span data-stu-id="0b43b-133">The device is not on the latest quality update due to the device's Windows Update for Business Quality Update Deferral policy.</span></span> <span data-ttu-id="0b43b-134">判斷 **daysOutOfDate** 會考慮延遲原則;在延遲期間過期之前， **daysOutOfDate** 不會開始遞增。</span><span class="sxs-lookup"><span data-stu-id="0b43b-134">Determining **daysOutOfDate** takes into account deferral policies; **daysOutOfDate** will not begin incrementing until the deferral period has expired.</span></span>

</dd> <dt>

<span data-ttu-id="0b43b-135"><span id="____UpdateAssessmentStatus_NotLatestPausedFeature"></span><span id="____updateassessmentstatus_notlatestpausedfeature"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTPAUSEDFEATURE"></span>**UpdateAssessmentStatus \_NotLatestPausedFeature**</span><span class="sxs-lookup"><span data-stu-id="0b43b-135"><span id="____UpdateAssessmentStatus_NotLatestPausedFeature"></span><span id="____updateassessmentstatus_notlatestpausedfeature"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTPAUSEDFEATURE"></span> **UpdateAssessmentStatus\_NotLatestPausedFeature**</span></span>
</dt> <dd>

<span data-ttu-id="0b43b-136">因為裝置已暫停功能更新，所以裝置不在最新的功能更新中。</span><span class="sxs-lookup"><span data-stu-id="0b43b-136">The device is not on the latest feature update due to the device having paused Feature Updates.</span></span> <span data-ttu-id="0b43b-137">在 **daysOutOfDate** 的計算中，是否要暫停裝置。</span><span class="sxs-lookup"><span data-stu-id="0b43b-137">Whether a device is paused is not factored into the calculation of **daysOutOfDate**.</span></span> <span data-ttu-id="0b43b-138">此狀態只適用于 **assessmentForCurrent**。</span><span class="sxs-lookup"><span data-stu-id="0b43b-138">This status only applies to **assessmentForCurrent**.</span></span>

</dd> <dt>

<span data-ttu-id="0b43b-139"><span id="____UpdateAssessmentStatus_NotLatestPausedQuality"></span><span id="____updateassessmentstatus_notlatestpausedquality"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTPAUSEDQUALITY"></span>**UpdateAssessmentStatus \_NotLatestPausedQuality**</span><span class="sxs-lookup"><span data-stu-id="0b43b-139"><span id="____UpdateAssessmentStatus_NotLatestPausedQuality"></span><span id="____updateassessmentstatus_notlatestpausedquality"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTPAUSEDQUALITY"></span> **UpdateAssessmentStatus\_NotLatestPausedQuality**</span></span>
</dt> <dd>

<span data-ttu-id="0b43b-140">裝置不在最新品質更新，因為裝置已暫停品質更新。</span><span class="sxs-lookup"><span data-stu-id="0b43b-140">The device is not on the latest quality update due to the device having paused Quality Updates.</span></span> <span data-ttu-id="0b43b-141">在 **daysOutOfDate** 的計算中，是否要暫停裝置。</span><span class="sxs-lookup"><span data-stu-id="0b43b-141">Whether a device is paused is not factored into the calculation of **daysOutOfDate**.</span></span> <span data-ttu-id="0b43b-142">**daysOutOfDate** 不會考慮裝置是否會暫停到其計算中。</span><span class="sxs-lookup"><span data-stu-id="0b43b-142">**daysOutOfDate** does not factor whether a device is paused into its calculation.</span></span>

</dd> <dt>

<span data-ttu-id="0b43b-143"><span id="____UpdateAssessmentStatus_NotLatestManaged"></span><span id="____updateassessmentstatus_notlatestmanaged"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTMANAGED"></span>**UpdateAssessmentStatus \_NotLatestManaged**</span><span class="sxs-lookup"><span data-stu-id="0b43b-143"><span id="____UpdateAssessmentStatus_NotLatestManaged"></span><span id="____updateassessmentstatus_notlatestmanaged"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTMANAGED"></span> **UpdateAssessmentStatus\_NotLatestManaged**</span></span>
</dt> <dd>

<span data-ttu-id="0b43b-144">裝置不在最新的更新中，因為不會透過 Windows Update 來核准更新。</span><span class="sxs-lookup"><span data-stu-id="0b43b-144">The device is not on the latest update because the approval of updates is not done through Windows Update.</span></span>

</dd> <dt>

<span data-ttu-id="0b43b-145"><span id="____UpdateAssessmentStatus_NotLatestUnknown"></span><span id="____updateassessmentstatus_notlatestunknown"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTUNKNOWN"></span>**UpdateAssessmentStatus \_NotLatestUnknown**</span><span class="sxs-lookup"><span data-stu-id="0b43b-145"><span id="____UpdateAssessmentStatus_NotLatestUnknown"></span><span id="____updateassessmentstatus_notlatestunknown"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTUNKNOWN"></span> **UpdateAssessmentStatus\_NotLatestUnknown**</span></span>
</dt> <dd>

<span data-ttu-id="0b43b-146">裝置不在最新的更新，因為評量無法判斷其原因。</span><span class="sxs-lookup"><span data-stu-id="0b43b-146">The device is not on the latest update due to a reason that cannot be determined by the assessment.</span></span>

</dd> <dt>

<span data-ttu-id="0b43b-147"><span id="____UpdateAssessmentStatus_NotLatestTargetedVersion"></span><span id="____updateassessmentstatus_notlatesttargetedversion"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTTARGETEDVERSION"></span>**UpdateAssessmentStatus \_NotLatestTargetedVersion**</span><span class="sxs-lookup"><span data-stu-id="0b43b-147"><span id="____UpdateAssessmentStatus_NotLatestTargetedVersion"></span><span id="____updateassessmentstatus_notlatesttargetedversion"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTTARGETEDVERSION"></span> **UpdateAssessmentStatus\_NotLatestTargetedVersion**</span></span>
</dt> <dd>

<span data-ttu-id="0b43b-148">裝置因為裝置的商務用 Windows Update 目標版本原則，而不是最新的功能更新。</span><span class="sxs-lookup"><span data-stu-id="0b43b-148">The device is not on the latest feature update due to the device's Windows Update for Business Target Version policy.</span></span> <span data-ttu-id="0b43b-149">此原則會將裝置保持在目標功能發行版本上。</span><span class="sxs-lookup"><span data-stu-id="0b43b-149">This policy is keeping the device on the targeted feature release version.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0b43b-150">備註</span><span class="sxs-lookup"><span data-stu-id="0b43b-150">Remarks</span></span>

<span data-ttu-id="0b43b-151">此列舉最常搭配 [**microsoft.intelligencepacks.updateassessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment)和 [**OSUpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment)結構使用，後者接著會與 [**IWaaSAssessor**](/windows/desktop/api/waasapi/nn-waasapi-iwaasassessor)的 [**GetOSUpdateAssessment**](/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment)方法搭配使用。</span><span class="sxs-lookup"><span data-stu-id="0b43b-151">This enumeration is used most often with the [**UpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) and [**OSUpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) structures, which are in turn used with the [**GetOSUpdateAssessment**](/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment) method for [**IWaaSAssessor**](/windows/desktop/api/waasapi/nn-waasapi-iwaasassessor).</span></span>

## <a name="requirements"></a><span data-ttu-id="0b43b-152">規格需求</span><span class="sxs-lookup"><span data-stu-id="0b43b-152">Requirements</span></span>



| <span data-ttu-id="0b43b-153">需求</span><span class="sxs-lookup"><span data-stu-id="0b43b-153">Requirement</span></span> | <span data-ttu-id="0b43b-154">值</span><span class="sxs-lookup"><span data-stu-id="0b43b-154">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0b43b-155">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0b43b-155">Minimum supported client</span></span><br/> | <span data-ttu-id="0b43b-156">Windows 10， \[ 僅限1703版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0b43b-156">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="0b43b-157">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0b43b-157">Minimum supported server</span></span><br/> | <span data-ttu-id="0b43b-158">僅限 Windows Server 2016 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0b43b-158">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="0b43b-159">Idl</span><span class="sxs-lookup"><span data-stu-id="0b43b-159">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0b43b-160"><dt>WaaSAPI .idl</dt></span><span class="sxs-lookup"><span data-stu-id="0b43b-160"><dt>WaaSAPI.idl</dt></span></span> </dl> |



 

 




