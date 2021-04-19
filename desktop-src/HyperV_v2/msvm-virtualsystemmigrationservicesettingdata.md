---
description: 代表主機上虛擬系統移轉服務的設定。
ms.assetid: 56711134-9a4a-49bd-8a0e-ce679b959adf
title: Msvm_VirtualSystemMigrationServiceSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationServiceSettingData
- Msvm_VirtualSystemMigrationServiceSettingData.InstanceID
- Msvm_VirtualSystemMigrationServiceSettingData.Caption
- Msvm_VirtualSystemMigrationServiceSettingData.Description
- Msvm_VirtualSystemMigrationServiceSettingData.ElementName
- Msvm_VirtualSystemMigrationServiceSettingData.EnableVirtualSystemMigration
- Msvm_VirtualSystemMigrationServiceSettingData.MaximumActiveVirtualSystemMigration
- Msvm_VirtualSystemMigrationServiceSettingData.MaximumActiveStorageMigration
- Msvm_VirtualSystemMigrationServiceSettingData.AuthenticationType
- Msvm_VirtualSystemMigrationServiceSettingData.EnableCompression
- Msvm_VirtualSystemMigrationServiceSettingData.EnableSmbTransport
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8c8685e468d60983408c52a985169c61be91f632
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973609"
---
# <a name="msvm_virtualsystemmigrationservicesettingdata-class"></a>Msvm \_ VirtualSystemMigrationServiceSettingData 類別

代表主機上虛擬系統移轉服務的設定。 無法直接修改這個類別的屬性。 用戶端必須呼叫 **Msvm \_ VirtualSystemMigrationService. ModifyServiceSettings** 方法來修改任何這些屬性。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemMigrationServiceSettingData : CIM_SettingData
{
  string  InstanceID;
  string  Caption;
  string  Description;
  string  ElementName;
  boolean EnableVirtualSystemMigration;
  uint32  MaximumActiveVirtualSystemMigration;
  uint32  MaximumActiveStorageMigration;
  uint32  AuthenticationType;
  boolean EnableCompression = True;
  boolean EnableSmbTransport = False;
};
```

## <a name="members"></a>成員

**Msvm \_ VirtualSystemMigrationServiceSettingData** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ VirtualSystemMigrationServiceSettingData** 類別具有這些屬性。

<dl> <dt>

**AuthenticationType**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定用於虛擬系統移轉網路連接的驗證機制。 這是唯讀屬性，但是可以使用 [**Msvm \_ VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md)類別的 [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md)方法來變更。

<dt>

<span id="CredSSP"></span><span id="credssp"></span><span id="CREDSSP"></span>

**CredSSP** (0) 


</dt> <dd></dd> <dt>

<span id="Kerberos"></span><span id="kerberos"></span><span id="KERBEROS"></span>

**Kerberos** (1) 


</dt> <dd></dd> </dl>

</dd> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的簡短描述。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) 類別。

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

對物件的描述。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的顯示名稱。 這個屬性繼承自 [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))。

</dd> <dt>

**EnableCompression**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指出是否啟用或停用即時移轉流量的壓縮。 True 表示已啟用。

這是唯讀屬性，但是可以使用 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md)方法來變更。

**Windows 8.1：** 在 Windows 8.1 和 Windows Server 2012 R2 之前，不支援這個值。

</dd> <dt>

**EnableSmbTransport**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指出是否在啟用或停用虛擬系統移轉期間，使用 SMB 做為傳輸類型，以在 Hyper-v 主機之間傳輸 VM 狀態。 **True** 表示已啟用。 如果 RDMA Nic 是在 VM 即時移轉期間設定為 SMB 傳輸，則會達到較高的效能。 如果 **EnableSmbTransport** 值為 true，則會忽略 **EnableCompression** 的值。

這是唯讀屬性，但是可以使用 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md)方法來變更。

**Windows 8.1：** 在 Windows 8.1 和 Windows Server 2012 R2 之前，不支援這個值。

</dd> <dt>

**EnableVirtualSystemMigration**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定虛擬系統移轉是否已啟用或停用。 儲存體遷移一律為啟用狀態。 這是唯讀屬性，但是可以使用 [**Msvm \_ VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md)類別的 [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md)方法來變更。

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 **鍵**
</dt> </dl>

唯一識別此類別的實例。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。

</dd> <dt>

**MaximumActiveStorageMigration**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定允許的主動式儲存體遷移數目上限。 這是唯讀屬性，但是可以使用 [**Msvm \_ VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md)類別的 [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md)方法來變更。

</dd> <dt>

**MaximumActiveVirtualSystemMigration**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定允許的主動式虛擬系統移轉數目上限。 這是唯讀屬性，但是可以使用 [**Msvm \_ VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md)類別的 [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md)方法來變更。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ SettingData**](cim-settingdata.md)
</dt> <dt>

[**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

