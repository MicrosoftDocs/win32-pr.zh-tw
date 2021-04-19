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
# <a name="updateassessmentstatus-enumeration"></a>UpdateAssessmentStatus 列舉

描述裝置上作業系統的最新狀態。 **UpdateAssessmentStatus** 可供 [**microsoft.intelligencepacks.updateassessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) 和 [**OSUpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) 結構、 **assessmentForCurrent**、 **assessmentForUpToDate** 和 **securityStatus** 成員使用。 只會傳回一個常數。

## <a name="syntax"></a>Syntax


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



## <a name="constants"></a>常數

<dl> <dt>

<span id="____UpdateAssessmentStatus_Latest"></span><span id="____updateassessmentstatus_latest"></span><span id="____UPDATEASSESSMENTSTATUS_LATEST"></span>**UpdateAssessmentStatus \_最新**
</dt> <dd>

**AssessmentForCurrent** 中的這項結果表示裝置處於適用于該裝置的最新功能更新和品質更新。 在 **assessmentForUpToDate** 中，此結果表示裝置處於正在執行之 Windows 版本的最新品質更新。

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestSoftRestriction"></span><span id="____updateassessmentstatus_notlatestsoftrestriction"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTSOFTRESTRICTION"></span>**UpdateAssessmentStatus \_NotLatestSoftRestriction**
</dt> <dd>

因為有軟限制，所以尚未安裝最新的功能更新。 將軟限制放置於更新時，將不會自動安裝更新;使用者必須在 Update UX 內自行起始下載。 此狀態只適用于 **assessmentForCurrent**。

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestHardRestriction"></span><span id="____updateassessmentstatus_notlatesthardrestriction"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTHARDRESTRICTION"></span>**UpdateAssessmentStatus \_NotLatestHardRestriction**
</dt> <dd>

尚未安裝最新的功能更新，因為有硬性限制。 當對更新進行硬性限制時，該更新就不適用裝置。 此狀態只適用于 **assessmentForCurrent**。

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestEndOfSupport"></span><span id="____updateassessmentstatus_notlatestendofsupport"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTENDOFSUPPORT"></span>**UpdateAssessmentStatus \_NotLatestEndOfSupport**
</dt> <dd>

裝置不在最新的更新中，因為 Microsoft 已不再支援裝置的功能更新。 當 Microsoft 停止支援功能版本時， **assessmentForCurrent** 和 **assessmentForUpToDate** 都會傳回此狀態。

> [!Note]  
> 傳回 **UpdateAssessmentStatus \_ NotLatestEndOfSupport** 時，評量的 **UpdateImpactLevel** 一律 **UpdateImpactLevel \_ High**。

 

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestServicingTrain"></span><span id="____updateassessmentstatus_notlatestservicingtrain"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTSERVICINGTRAIN"></span>**UpdateAssessmentStatus \_NotLatestServicingTrain**
</dt> <dd>

裝置不在最新的功能更新上，因為裝置的服務訓練會限制裝置無法更新至最新的功能更新。 例如：如果裝置位於最新商務分支 (CBB) 且已針對最新分支 (CB) 發行新的功能更新，將會傳回這項功能。 此狀態只適用于 **assessmentForCurrent**。

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestDeferredFeature"></span><span id="____updateassessmentstatus_notlatestdeferredfeature"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTDEFERREDFEATURE"></span>**UpdateAssessmentStatus \_NotLatestDeferredFeature**
</dt> <dd>

由於裝置的商務用 Windows Update 功能更新延遲原則，尚未安裝最新的功能更新。 判斷 **daysOutOfDate** 會考慮延遲原則;在延遲期間過期之前， **daysOutOfDate** 不會開始遞增。 此狀態只適用于 **assessmentForCurrent**。

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestDeferredQuality"></span><span id="____updateassessmentstatus_notlatestdeferredquality"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTDEFERREDQUALITY"></span>**UpdateAssessmentStatus \_NotLatestDeferredQuality**
</dt> <dd>

裝置因為裝置的商務用 Windows Update 品質更新延遲原則，而不是最新的品質更新。 判斷 **daysOutOfDate** 會考慮延遲原則;在延遲期間過期之前， **daysOutOfDate** 不會開始遞增。

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestPausedFeature"></span><span id="____updateassessmentstatus_notlatestpausedfeature"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTPAUSEDFEATURE"></span>**UpdateAssessmentStatus \_NotLatestPausedFeature**
</dt> <dd>

因為裝置已暫停功能更新，所以裝置不在最新的功能更新中。 在 **daysOutOfDate** 的計算中，是否要暫停裝置。 此狀態只適用于 **assessmentForCurrent**。

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestPausedQuality"></span><span id="____updateassessmentstatus_notlatestpausedquality"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTPAUSEDQUALITY"></span>**UpdateAssessmentStatus \_NotLatestPausedQuality**
</dt> <dd>

裝置不在最新品質更新，因為裝置已暫停品質更新。 在 **daysOutOfDate** 的計算中，是否要暫停裝置。 **daysOutOfDate** 不會考慮裝置是否會暫停到其計算中。

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestManaged"></span><span id="____updateassessmentstatus_notlatestmanaged"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTMANAGED"></span>**UpdateAssessmentStatus \_NotLatestManaged**
</dt> <dd>

裝置不在最新的更新中，因為不會透過 Windows Update 來核准更新。

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestUnknown"></span><span id="____updateassessmentstatus_notlatestunknown"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTUNKNOWN"></span>**UpdateAssessmentStatus \_NotLatestUnknown**
</dt> <dd>

裝置不在最新的更新，因為評量無法判斷其原因。

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestTargetedVersion"></span><span id="____updateassessmentstatus_notlatesttargetedversion"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTTARGETEDVERSION"></span>**UpdateAssessmentStatus \_NotLatestTargetedVersion**
</dt> <dd>

裝置因為裝置的商務用 Windows Update 目標版本原則，而不是最新的功能更新。 此原則會將裝置保持在目標功能發行版本上。

</dd> </dl>

## <a name="remarks"></a>備註

此列舉最常搭配 [**microsoft.intelligencepacks.updateassessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment)和 [**OSUpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment)結構使用，後者接著會與 [**IWaaSAssessor**](/windows/desktop/api/waasapi/nn-waasapi-iwaasassessor)的 [**GetOSUpdateAssessment**](/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment)方法搭配使用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1703版桌面應用程式\]<br/>                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2016 \[ desktop 應用程式\]<br/>                                   |
| Idl<br/>                      | <dl> <dt>WaaSAPI .idl</dt> </dl> |



 

 




