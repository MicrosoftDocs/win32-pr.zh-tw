---
description: 代表通訊埠設定檔設定。
ms.assetid: 43ddb0a3-8621-4993-b0a9-8ddcfb0eaad5
title: Msvm_EthernetSwitchPortProfileSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortProfileSettingData
- Msvm_EthernetSwitchPortProfileSettingData.InstanceID
- Msvm_EthernetSwitchPortProfileSettingData.Caption
- Msvm_EthernetSwitchPortProfileSettingData.Description
- Msvm_EthernetSwitchPortProfileSettingData.ElementName
- Msvm_EthernetSwitchPortProfileSettingData.ProfileName
- Msvm_EthernetSwitchPortProfileSettingData.ProfileId
- Msvm_EthernetSwitchPortProfileSettingData.VendorName
- Msvm_EthernetSwitchPortProfileSettingData.VendorId
- Msvm_EthernetSwitchPortProfileSettingData.ProfileData
- Msvm_EthernetSwitchPortProfileSettingData.NetCfgInstanceId
- Msvm_EthernetSwitchPortProfileSettingData.PciSegmentNumber
- Msvm_EthernetSwitchPortProfileSettingData.PciBusNumber
- Msvm_EthernetSwitchPortProfileSettingData.PciDeviceNumber
- Msvm_EthernetSwitchPortProfileSettingData.PciFunctionNumber
- Msvm_EthernetSwitchPortProfileSettingData.CdnLabelId
- Msvm_EthernetSwitchPortProfileSettingData.CdnLabelString
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 611fd40b14b961369a847d6bb7b7746ceec2bb85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988505"
---
# <a name="msvm_ethernetswitchportprofilesettingdata-class"></a>Msvm \_ EthernetSwitchPortProfileSettingData 類別

代表通訊埠設定檔設定。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, UUID("9940CD46-8B06-43BB-B9D5-93D50381FD56"), Provider("VmmsWmiInstanceAndMethodProvider"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Profile Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortProfileSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string InstanceID;
  string Caption = "Ethernet Switch Port Profile Settings";
  string Description = "Represents the port profile settings.";
  string ElementName = "Ethernet Switch Port Profile Settings";
  string ProfileName = "";
  string ProfileId = "";
  string VendorName = "";
  string VendorId = 00000000-0000-0000-0000-000000000000}";
  uint32 ProfileData = 0;
  string NetCfgInstanceId = 00000000-0000-0000-0000-000000000000}";
  uint32 PciSegmentNumber = 0;
  uint32 PciBusNumber = 0;
  uint32 PciDeviceNumber = 0;
  uint32 PciFunctionNumber = 0;
  uint32 CdnLabelId = 0;
  string CdnLabelString = 0;
};
```

## <a name="members"></a>成員

**Msvm \_ EthernetSwitchPortProfileSettingData** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ EthernetSwitchPortProfileSettingData** 類別具有這些屬性。

<dl> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的簡短描述。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「乙太網路交換器通訊埠設定檔設定」。

</dd> <dt>

**CdnLabelId**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： **WmiDataId** (11) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) 
</dt> </dl>

CDN 標籤識別碼。

</dd> <dt>

**CdnLabelString**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (127) 、 **WmiDataId** (12) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) 
</dt> </dl>

CDN 標籤字串。

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

對物件的描述。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設為「代表通訊埠設定檔設定」。

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的顯示名稱。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「乙太網路交換器通訊埠設定檔設定」。

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

**NetCfgInstanceId**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (38) 、 **WmiDataId** (6) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) 
</dt> </dl>

子介面的唯一裝置識別碼。

</dd> <dt>

**PciBusNumber**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： **WmiDataId** (8) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) 
</dt> </dl>

PCI 匯流排號碼。

</dd> <dt>

**PciDeviceNumber**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： **WmiDataId** (9) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) 
</dt> </dl>

PCI 裝置編號。

</dd> <dt>

**PciFunctionNumber**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： **WmiDataId** (10) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) 
</dt> </dl>

PCI 函數編號。

</dd> <dt>

**PciSegmentNumber**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： **WmiDataId** (7) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) 
</dt> </dl>

PCI 區段編號。

</dd> <dt>

**ProfileData**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： **WmiDataId** (5) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) 
</dt> </dl>

通訊埠設定檔的其他資料。

</dd> <dt>

**ProfileId**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (38) 、 **WmiDataId** (2) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) 
</dt> </dl>

通訊埠設定檔的識別碼。

</dd> <dt>

**ProfileName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (127) 、 **WmiDataId** (1) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) 
</dt> </dl>

通訊埠設定檔的名稱。

</dd> <dt>

**VendorId**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (38) 、 **WmiDataId** (4) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) 
</dt> </dl>

定義設定檔的供應商識別碼。

</dd> <dt>

**VendorName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (127) 、 **WmiDataId** (3) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) 
</dt> </dl>

定義設定檔的廠商名稱。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

