---
title: MDM_Policy_Config01_DeviceLock02 類別
description: MDM \_ Policy \_ Config01 \_ DeviceLock02 類別代表可用的裝置鎖定原則。
ms.assetid: 222081ec-c38f-481d-ae38-941fd1317197
keywords:
- MDM_Policy_Config01_DeviceLock02 類別
- MDM_Policy_Config01_DeviceLock02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_DeviceLock02
- MDM_Policy_Config01_DeviceLock02.InstanceID
- MDM_Policy_Config01_DeviceLock02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80bfd2f08b048ef16aaa03de2e9a0c1c809e493b00f5ff84e7c24e1b9edb4f83
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119967518"
---
# <a name="mdm_policy_config01_devicelock02-class"></a>MDM \_ 原則 \_ Config01 \_ DeviceLock02 類別

\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。 Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]

**MDM \_ Policy \_ Config01 \_ DeviceLock02** 類別代表可用的裝置鎖定原則。

下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_DeviceLock02
{
  string InstanceID;
  string ParentID;
  sint32 AllowScreenTimeoutWhileLockedUserConfig;
  sint32 AllowSimpleDevicePassword;
  sint32 AlphanumericDevicePasswordRequired;
  sint32 DevicePasswordEnabled;
  sint32 DevicePasswordExpiration;
  sint32 DevicePasswordHistory;
  string EnforceLockScreenAndLogonImage;
  string EnforceLockScreenProvider;
  sint32 MinimumPasswordAge;
  sint32 MaxDevicePasswordFailedAttempts;
  sint32 MaxInactivityTimeDeviceLock;
  sint32 MinDevicePasswordComplexCharacters;
  sint32 MinDevicePasswordLength;
  sint32 ScreenTimeoutWhileLocked;
  string PreventLockScreenSlideShow;
};
```

## <a name="members"></a>成員

**MDM \_ Policy \_ Config01 \_ DeviceLock02** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**MDM \_ Policy \_ Config01 \_ DeviceLock02** 類別具有這些屬性。

<dl> <dt>

AllowScreenTimeoutWhileLockedUserConfig
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[AllowSimpleDevicePassword](/windows/client-management/mdm/policy-csp-devicelock#devicelock-allowsimpledevicepassword)
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[AlphanumericDevicePasswordRequired](/windows/client-management/mdm/policy-csp-devicelock#devicelock-alphanumericdevicepasswordrequired)
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[DevicePasswordEnabled](/windows/client-management/mdm/policy-csp-devicelock#devicelock-devicepasswordenabled)
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

當使用 WMI 來設定 EAS DeviceLock 原則時，不應該將 DevicePasswordEnabled 設定為啟用 (0) ，因為它在原則 CSP 中預設為啟用，以提供與 Windows 8 的回溯相容性。 如果 DevicePasswordEnabled 設為 Enabled (0) 則原則 CSP 將會傳回錯誤，指出 DevicePasswordEnabled 已經存在。 Windows 8. x 不支援 DevicePassword 原則。 停用 DevicePasswordEnabled (1) 之後，這應該是從下面的原則 DeviceLock 群組中唯一設定的原則。 原則列示如下： >-DevicePasswordEnabled 是下列的父原則：

-   DevicePasswordEnabled 是下列的父原則：
    -   AllowSimpleDevicePassword
    -   MinDevicePasswordLength
    -   AlphanumericDevicePasswordRequired 是的父原則：
        -   MinDevicePasswordComplexCharacters 
    -   MaxDevicePasswordFailedAttempts
    -   MaxInactivityTimeDeviceLock

</dd> <dt>

[DevicePasswordExpiration](/windows/client-management/mdm/policy-csp-devicelock#devicelock-devicepasswordexpiration)
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[DevicePasswordHistory](/windows/client-management/mdm/policy-csp-devicelock#devicelock-devicepasswordhistory)
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[EnforceLockScreenAndLogonImage](/windows/client-management/mdm/policy-csp-devicelock#devicelock-enforcelockscreenandlogonimage)
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

EnforceLockScreenProvider
</dt> <dd> <dl> <dt>

資料類型： **字串**
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

識別父節點的名稱。 此類別的字串為 "DeviceLock"。

</dd> <dt>

[MaxDevicePasswordFailedAttempts](/windows/client-management/mdm/policy-csp-devicelock#devicelock-maxdevicepasswordfailedattempts)
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[MaxInactivityTimeDeviceLock](/windows/client-management/mdm/policy-csp-devicelock#devicelock-maxinactivitytimedevicelock)
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[MinDevicePasswordComplexCharacters](/windows/client-management/mdm/policy-csp-devicelock#devicelock-mindevicepasswordcomplexcharacters)
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[MinDevicePasswordLength](/windows/client-management/mdm/policy-csp-devicelock#devicelock-mindevicepasswordlength)
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

[Msds-minimumpasswordage](/windows/client-management/mdm/policy-csp-devicelock#devicelock-minimumpasswordage)
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

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

[PreventLockScreenSlideShow](/windows/client-management/mdm/policy-csp-devicelock#devicelock-preventlockscreenslideshow)
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

ScreenTimeoutWhileLocked
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

 

