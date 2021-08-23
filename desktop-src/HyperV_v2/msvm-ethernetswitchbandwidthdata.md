---
description: 代表切換頻寬資源狀態。
ms.assetid: 9aa3e57e-9452-4c60-a052-83ae35b3607c
title: Msvm_EthernetSwitchBandwidthData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchBandwidthData
- Msvm_EthernetSwitchBandwidthData.InstanceID
- Msvm_EthernetSwitchBandwidthData.Caption
- Msvm_EthernetSwitchBandwidthData.Description
- Msvm_EthernetSwitchBandwidthData.ElementName
- Msvm_EthernetSwitchBandwidthData.SystemCreationClassName
- Msvm_EthernetSwitchBandwidthData.SystemName
- Msvm_EthernetSwitchBandwidthData.CreationClassName
- Msvm_EthernetSwitchBandwidthData.Name
- Msvm_EthernetSwitchBandwidthData.Capacity
- Msvm_EthernetSwitchBandwidthData.Reservation
- Msvm_EthernetSwitchBandwidthData.DefaultFlowReservationPercentage
- Msvm_EthernetSwitchBandwidthData.DefaultFlowReservation
- Msvm_EthernetSwitchBandwidthData.DefaultFlowWeight
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 422efc93de56c520f0929ca9d7f0b53a5911bcc553f529e2efeb8fbc70d8cf3c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119524648"
---
# <a name="msvm_ethernetswitchbandwidthdata-class"></a>Msvm \_ EthernetSwitchBandwidthData 類別

代表切換頻寬資源狀態。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("8F425906-034D-42AB-BD16-EDB31CEC55EF"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Bandwidth data"), AMENDMENT]
class Msvm_EthernetSwitchBandwidthData : Msvm_EthernetSwitchData
{
  string InstanceID;
  string Caption = "Ethernet Switch Bandwidth data";
  string Description = "Represents the switch bandwidth resource status.";
  string ElementName = "Ethernet Switch Bandwidth data";
  string SystemCreationClassName = "Msvm_VirtualEthernetSwitch";
  string SystemName;
  string CreationClassName = "Msvm_EthernetSwitchBandwidthData";
  string Name;
  uint64 Capacity = 100000000;
  uint64 Reservation = 100000000;
  uint32 DefaultFlowReservationPercentage = 10;
  uint64 DefaultFlowReservation = 100000000;
  uint64 DefaultFlowWeight = 0;
};
```

## <a name="members"></a>成員

**Msvm \_ EthernetSwitchBandwidthData** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ EthernetSwitchBandwidthData** 類別具有這些屬性。

<dl> <dt>

**容量**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (1) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) 
</dt> </dl>

交換器可用的最大頻寬。

</dd> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的簡短描述。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **Key**、 **MaxLen** (256) 
</dt> </dl>

建立這個實例時所使用的類別或子類別名稱。

</dd> <dt>

**DefaultFlowReservation**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (4) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) 
</dt> </dl>

預設流程在交換器上保留的目前絕對頻寬。

</dd> <dt>

**DefaultFlowReservationPercentage**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (3) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) 
</dt> </dl>

預設流程在交換器上保留的目前頻寬百分比。

</dd> <dt>

**DefaultFlowWeight**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (5) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) 
</dt> </dl>

切換上預設流程的目前加權。

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

物件的顯示名稱。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。

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

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **Key**、 **Override**、 **MaxLen** (256) 
</dt> </dl>

資源的唯一名稱。

</dd> <dt>

**保留容量**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (2) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) 
</dt> </dl>

目前保留在交換器上的頻寬。

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **Key**、 **MaxLen** (256) 
</dt> </dl>

裝載系統的建立類別名稱。 這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)。

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **Key**、 **MaxLen** (256) 
</dt> </dl>

相關聯的資源實例所系結之虛擬交換器的名稱。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

