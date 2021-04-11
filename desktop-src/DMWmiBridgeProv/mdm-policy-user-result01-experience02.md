---
title: MDM_Policy_User_Result01_Experience02 類別
description: MDM \_ Policy \_ User \_ Result01 \_ Experience02 類別代表可用的體驗原則。
ms.assetid: 729dfc75-7458-426f-8173-9ba75b4ee306
keywords:
- MDM_Policy_User_Result01_Experience02 類別
- MDM_Policy_User_Result01_Experience02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Policy_User_Result01_Experience02
- MDM_Policy_User_Result01_Experience02.InstanceID
- MDM_Policy_User_Result01_Experience02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 320941108309264a2cce3be6e63edca305c1cd40
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843627"
---
# <a name="mdm_policy_user_result01_experience02-class"></a>MDM \_ 原則 \_ 使用者 \_ Result01 \_ Experience02 類別

\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。 Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]

**MDM \_ Policy \_ User \_ Result01 \_ Experience02** 類別代表可用的體驗原則。

下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Result01_Experience02
{
  string InstanceID;
  string ParentID;
  sint32 AllowTailoredExperiencesWithDiagnosticData;
  sint32 AllowWindowsConsumerFeatures;
  sint32 AllowWindowsSpotlight;
  sint32 AllowWindowsSpotlightWindowsWelcomeExperience;
  sint32 AllowWindowsSpotlightOnActionCenter;
  sint32 ConfigureWindowsSpotlightOnLockScreen;
  sint32 AllowThirdPartySuggestionsInWindowsSpotlight;
};
```

## <a name="members"></a>成員

**MDM \_ Policy \_ User \_ Result01 \_ Experience02** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**MDM \_ Policy \_ User \_ Result01 \_ Experience02** 類別具有這些屬性。

<dl> <dt>

[AllowTailoredExperiencesWithDiagnosticData](/windows/client-management/mdm/policy-csp-experience#experience-allowtailoredexperienceswithdiagnosticdata)
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[AllowThirdPartySuggestionsInWindowsSpotlight](/windows/client-management/mdm/policy-csp-experience#experience-allowthirdpartysuggestionsinwindowsspotlight)
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[AllowWindowsConsumerFeatures](/windows/client-management/mdm/policy-csp-experience#experience-allowwindowsconsumerfeatures)
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[AllowWindowsSpotlight](/windows/client-management/mdm/policy-csp-experience#experience-allowwindowsspotlight)
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[AllowWindowsSpotlightOnActionCenter](/windows/client-management/mdm/policy-csp-experience#experience-allowwindowsspotlightonactioncenter)
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[AllowWindowsSpotlightWindowsWelcomeExperience](/windows/client-management/mdm/policy-csp-experience#experience-allowwindowsspotlightwindowswelcomeexperience)
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[ConfigureWindowsSpotlightOnLockScreen](/windows/client-management/mdm/policy-csp-experience#experience-configurewindowsspotlightonlockscreen)
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

識別父節點的名稱。 針對此類別，字串為「經驗」。

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

描述父節點的完整路徑。 此類別的字串為 "./User/Vendor/MSFT/Policy/Result"

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 10 桌面應用程式\]<br/>                                                          |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                            |
| 命名空間<br/>                | 根 \\ cimv2 \\ mdm \\ dmmap<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv mof</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Mof \\DMWmiBridgeProv.dll</dt> </dl> |



 

