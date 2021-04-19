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
# <a name="updateimpactlevel-enumeration"></a>UpdateImpactLevel 列舉

表示執行過時 OS 的裝置有高、中或低的影響。 這個列舉通常是由 [**microsoft.intelligencepacks.updateassessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment)結構所使用，而這種結構接著會在 [**GetOSUpdateAssessment**](/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment)的傳回 [**OSUpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment)內進行嵌套。

## <a name="syntax"></a>Syntax


```C++
typedef enum TagUpdateImpactLevel { 
      UpdateImpactLevel_None    = 0,
  UpdateImpactLevel_Low         = 1,
      UpdateImpactLevel_Medium  = 2,
  UpdateImpactLevel_High        = 3
} UpdateImpactLevel;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="____UpdateImpactLevel_None"></span><span id="____updateimpactlevel_none"></span><span id="____UPDATEIMPACTLEVEL_NONE"></span>**UpdateImpactLevel \_無**
</dt> <dd>

您的裝置沒有可預見的影響。 這可能是因為裝置處於最新狀態或不是最新狀態，因為裝置正在接受其商務用 Windows Update 延遲期間，或已過期，但尚未達到 **daysOutOfDate** 閾值以達到較高的影響層級。

</dd> <dt>

<span id="UpdateImpactLevel_Low"></span><span id="updateimpactlevel_low"></span><span id="UPDATEIMPACTLEVEL_LOW"></span>**UpdateImpactLevel \_ 低**
</dt> <dd>

裝置不是執行最新的作業系統，但有最近的更新。

</dd> <dt>

<span id="____UpdateImpactLevel_Medium"></span><span id="____updateimpactlevel_medium"></span><span id="____UPDATEIMPACTLEVEL_MEDIUM"></span>**UpdateImpactLevel \_中**
</dt> <dd>

裝置正在執行最新的作業系統，但有較新的更新。

</dd> <dt>

<span id="UpdateImpactLevel_High"></span><span id="updateimpactlevel_high"></span><span id="UPDATEIMPACTLEVEL_HIGH"></span>**UpdateImpactLevel \_ High**
</dt> <dd>

裝置已過期一段時間。 此裝置可能有安全性弱點，可能會遺失讓 Windows 執行更好的重要修正。 當裝置正在執行不再支援的 Windows 版本時，一律會傳回 **UpdateImpactLevel \_ High** 。

</dd> </dl>

## <a name="remarks"></a>備註

呼叫 [**GetOSUpdateAssessment**](/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment) 時，會傳回 [**OSUpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) 結構。 結構內有一個 **assessmentForCurrent** 和 **assessmentForUpToDate**。 這兩種都是 [**microsoft.intelligencepacks.updateassessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) 結構。 這兩個成員都有 **UpdateImpactLevel** 列舉，表示執行過時 OS 之裝置的高、中、低或無影響。 這些層級取決於 **daysOutOfDate** 的值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1703版桌面應用程式\]<br/>                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2016 \[ desktop 應用程式\]<br/>                                   |
| Idl<br/>                      | <dl> <dt>WaaSAPI .idl</dt> </dl> |



 

 




