---
title: MDM_Policy_Config01_ApplicationManagement02 類別
description: MDM \_ Policy \_ Config01 \_ ApplicationManagement02 類別代表可用的應用程式管理原則。
ms.assetid: f05c4852-e694-4e0d-94e1-07531c879613
keywords:
- MDM_Policy_Config01_ApplicationManagement02 類別
- MDM_Policy_Config01_ApplicationManagement02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_ApplicationManagement02
- MDM_Policy_Config01_ApplicationManagement02.InstanceID
- MDM_Policy_Config01_ApplicationManagement02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1ecff562e5e51c2e998c1708afbd2a3460b77e5315050475327d8165540f953
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118165730"
---
# <a name="mdm_policy_config01_applicationmanagement02-class"></a>MDM \_ 原則 \_ Config01 \_ ApplicationManagement02 類別

\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。 Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]

**MDM \_ Policy \_ Config01 \_ ApplicationManagement02** 類別代表可用的應用程式管理原則。

下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_ApplicationManagement02
{
  string InstanceID;
  string ParentID;
  sint32 AllowAllTrustedApps;
  sint32 AllowAppStoreAutoUpdate;
  sint32 AllowDeveloperUnlock;
  sint32 AllowGameDVR;
  sint32 AllowSharedUserAppData;
  sint32 DisableStoreOriginatedApps;
  sint32 RestrictAppDataToSystemVolume;
  sint32 RestrictAppToSystemVolume;
};
```

## <a name="members"></a>成員

**MDM \_ Policy \_ Config01 \_ ApplicationManagement02** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**MDM \_ Policy \_ Config01 \_ ApplicationManagement02** 類別具有這些屬性。

<dl> <dt>

[AllowAllTrustedApps](/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-allowalltrustedapps)
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[AllowAppStoreAutoUpdate](/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-allowappstoreautoupdate)
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[AllowDeveloperUnlock](/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-allowdeveloperunlock)
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[AllowGameDVR](/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-allowgamedvr)
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[AllowSharedUserAppData](/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-allowshareduserappdata)
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[DisableStoreOriginatedApps](/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-disablestoreoriginatedapps)
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

識別父節點的名稱。 此類別的字串為 "ApplicationManagement"。

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

描述父節點的完整路徑。 此類別的字串為 "./Vendor/MSFT/Policy/Config"

</dd> <dt>

[RestrictAppDataToSystemVolume](/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-restrictappdatatosystemvolume)
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[RestrictAppToSystemVolume](/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-restrictapptosystemvolume)
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10 \[僅限桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                      |
| 命名空間<br/>                | 根 \\ CIMv2 \\ MDM \\ DMMap<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[使用 PowerShell 指令碼搭配 WMI 橋接器提供者](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

