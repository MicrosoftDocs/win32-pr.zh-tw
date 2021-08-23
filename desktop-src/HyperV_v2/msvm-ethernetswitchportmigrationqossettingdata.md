---
description: 代表 VFP QOS 設定。
ms.assetid: e58a7a8d-0301-43ea-9338-18bc8c458e2d
title: Msvm_EthernetSwitchPortMigrationQosSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortMigrationQosSettingData
- Msvm_EthernetSwitchPortMigrationQosSettingData.QueueId
- Msvm_EthernetSwitchPortMigrationQosSettingData.Switch_ReservationMode
- Msvm_EthernetSwitchPortMigrationQosSettingData.Switch_LinkSpeedPercentage
- Msvm_EthernetSwitchPortMigrationQosSettingData.Switch_DefaultReservation
- Msvm_EthernetSwitchPortMigrationQosSettingData.Switch_EnableHardwareLimits
- Msvm_EthernetSwitchPortMigrationQosSettingData.Switch_EnableHardwareReservations
- Msvm_EthernetSwitchPortMigrationQosSettingData.Switch_EnableSoftwareReservations
- Msvm_EthernetSwitchPortMigrationQosSettingData.OutboundReservedValue
- Msvm_EthernetSwitchPortMigrationQosSettingData.OutboundMaximumMbps
- Msvm_EthernetSwitchPortMigrationQosSettingData.InboundMaximumMbps
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: fef4ef759b406facb5fbbb12d37eceb55a914d46c63a2485982f60fa151ccdaa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119524038"
---
# <a name="msvm_ethernetswitchportmigrationqossettingdata-class"></a>Msvm \_ EthernetSwitchPortMigrationQosSettingData 類別

代表 VFP QOS 設定。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, UUID("FD2A5DE3-DC6C-4320-82A5-234D3AF55297"), Provider("VmmsWmiInstanceAndMethodProvider"), ExtensionId("E9B59CFA-2BE1-4B21-828F-B6FBDBDDC017"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port VFP QOS Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortMigrationQosSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string  QueueId = "";
  uint8   Switch_ReservationMode = 0;
  uint8   Switch_LinkSpeedPercentage = 0;
  uint64  Switch_DefaultReservation = 0;
  boolean Switch_EnableHardwareLimits = FALSE;
  boolean Switch_EnableHardwareReservations = FALSE;
  boolean Switch_EnableSoftwareReservations = TRUE;
  uint64  OutboundReservedValue = 0;
  uint64  OutboundMaximumMbps = 0;
  uint64  InboundMaximumMbps = 0;
};
```

## <a name="members"></a>成員

**Msvm \_ EthernetSwitchPortMigrationQosSettingData** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ EthernetSwitchPortMigrationQosSettingData** 類別具有這些屬性。

<dl> <dt>

**InboundMaximumMbps**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： **WmiDataId** (10) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) 
</dt> </dl>

輸入流量的頻寬上限值。

</dd> <dt>

**OutboundMaximumMbps**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： **WmiDataId** (9) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) 
</dt> </dl>

輸出流量的頻寬上限值。

</dd> <dt>

**OutboundReservedValue**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： **WmiDataId** (8) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) 
</dt> </dl>

頻寬保留值。

</dd> <dt>

**QueueId**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) 、 **WmiDataId** (1) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) 
</dt> </dl>

QOS 佇列的識別碼。

</dd> <dt>

**切換 \_ DefaultReservation**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： **WmiDataId** (4) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) 
</dt> </dl>

預設保留值。

</dd> <dt>

**切換 \_ EnableHardwareLimits**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： **WmiDataId** (5) 、 [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 、 [**修訂**](/windows/desktop/WmiSdk/standard-qualifiers) (0) 
</dt> </dl>

指出是否會嘗試硬體卸載以取得限制（如果有的話）。

</dd> <dt>

**切換 \_ EnableHardwareReservations**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： **WmiDataId** (6) 、 [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 、 [**修訂**](/windows/desktop/WmiSdk/standard-qualifiers) (0) 
</dt> </dl>

指出是否會嘗試保留硬體卸載（如果有的話）。

</dd> <dt>

**切換 \_ EnableSoftwareReservations**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： **WmiDataId** (7) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) 
</dt> </dl>

指出以軟體為基礎的保留是否可用。

</dd> <dt>

**切換 \_ LinkSpeedPercentage**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： **WmiDataId** (3) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) 
</dt> </dl>

要用於保留的連結速度百分比。

</dd> <dt>

**切換 \_ ReservationMode**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： **WmiDataId** (2) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) 
</dt> </dl>

交換器上的 QOS 保留模式。

<dt>

<span id="Absolute"></span><span id="absolute"></span><span id="ABSOLUTE"></span>

**絕對** (0) 


</dt> <dd></dd> <dt>

<span id="Weight"></span><span id="weight"></span><span id="WEIGHT"></span>

**權數** (1) 


</dt> <dd></dd> </dl>

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

[**Msvm \_ EthernetSwitchPortFeatureSettingData**](msvm-ethernetswitchportfeaturesettingdata.md)
</dt> </dl>

 

