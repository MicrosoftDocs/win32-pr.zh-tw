---
description: 表示之安全性設定的設定狀態。
ms.assetid: c57ab966-591e-4dd9-87be-0d2b81611d5d
title: Msvm_SecuritySettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecuritySettingData
- Msvm_SecuritySettingData.TpmEnabled
- Msvm_SecuritySettingData.KsdEnabled
- Msvm_SecuritySettingData.ShieldingRequested
- Msvm_SecuritySettingData.DataProtectionRequested
- Msvm_SecuritySettingData.EncryptStateAndVmMigrationTraffic
- Msvm_SecuritySettingData.VirtualizationBasedSecurityOptOut
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b7125e06ad4ce33e70a8cf84b24933e7390e7a74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106986960"
---
# <a name="msvm_securitysettingdata-class"></a>Msvm \_ SecuritySettingData 類別

代表虛擬機器之安全性設定的設定狀態。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SecuritySettingData : CIM_SettingData
{
  boolean TpmEnabled;
  boolean KsdEnabled;
  boolean ShieldingRequested;
  boolean DataProtectionRequested;
  boolean EncryptStateAndVmMigrationTraffic;
  boolean VirtualizationBasedSecurityOptOut;
};
```

## <a name="members"></a>成員

**Msvm \_ SecuritySettingData** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ SecuritySettingData** 類別具有這些屬性。

<dl> <dt>

**DataProtectionRequested**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**必要**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

**true** 表示要求 VM 的資料保護;否則 **為 false**。 預設值為 **false**。

</dd> <dt>

**EncryptStateAndVmMigrationTraffic**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**必要**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

**true** 表示已加密 VM 的狀態和遷移流量;否則 **為 false**。 新建立之 VM 的預設值為 **false**。

</dd> <dt>

**KsdEnabled**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**必要**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

**true** 表示為此虛擬機器啟用金鑰存放裝置 (KSD) ;否則 **為 false**。 新建立的 VM 具有停用的 KSD。

</dd> <dt>

**ShieldingRequested**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**必要**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

**true** 表示要求防護 VM;否則 **為 false**。 新建立的 VM 具有要求的初始防護狀態 **false**。

</dd> <dt>

**TpmEnabled**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**必要**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

**true** 表示啟用受信任的平臺 nodule (此虛擬機器的 TPM) ;否則 **為 false**。 新建立的 VM 具有停用 TPM。

</dd> <dt>

**VirtualizationBasedSecurityOptOut**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**必要**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

**true** 表示不提供 VM 虛擬化型安全性;否則 **為 false**。 新建立的 VM 退出狀態預設設定為 **false**。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1703版桌面應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows Server 2016<br/>                                                                          |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ SettingData**](cim-settingdata.md)
</dt> </dl>

 

