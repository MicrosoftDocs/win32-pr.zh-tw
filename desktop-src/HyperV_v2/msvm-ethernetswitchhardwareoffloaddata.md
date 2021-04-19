---
description: 代表交換器硬體卸載狀態。
ms.assetid: 77a34df7-e3c4-4d91-af5a-91a03dd8246d
title: Msvm_EthernetSwitchHardwareOffloadData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchHardwareOffloadData
- Msvm_EthernetSwitchHardwareOffloadData.InstanceID
- Msvm_EthernetSwitchHardwareOffloadData.Caption
- Msvm_EthernetSwitchHardwareOffloadData.Description
- Msvm_EthernetSwitchHardwareOffloadData.ElementName
- Msvm_EthernetSwitchHardwareOffloadData.SystemCreationClassName
- Msvm_EthernetSwitchHardwareOffloadData.SystemName
- Msvm_EthernetSwitchHardwareOffloadData.CreationClassName
- Msvm_EthernetSwitchHardwareOffloadData.Name
- Msvm_EthernetSwitchHardwareOffloadData.IovVfCapacity
- Msvm_EthernetSwitchHardwareOffloadData.IovVfUsage
- Msvm_EthernetSwitchHardwareOffloadData.VmqCapacity
- Msvm_EthernetSwitchHardwareOffloadData.VmqUsage
- Msvm_EthernetSwitchHardwareOffloadData.IPsecSACapacity
- Msvm_EthernetSwitchHardwareOffloadData.IPsecSAUsage
- Msvm_EthernetSwitchHardwareOffloadData.IovQueuePairCapacity
- Msvm_EthernetSwitchHardwareOffloadData.IovQueuePairUsage
- Msvm_EthernetSwitchHardwareOffloadData.PacketDirectInUse
- Msvm_EthernetSwitchHardwareOffloadData.DefaultQueueVmmqQueuePairs
- Msvm_EthernetSwitchHardwareOffloadData.DefaultQueueVrssIndependentHostSpreading
- Msvm_EthernetSwitchHardwareOffloadData.DefaultQueueVrssExcludePrimaryProcessor
- Msvm_EthernetSwitchHardwareOffloadData.DefaultQueueVrssQueueSchedulingMode
- Msvm_EthernetSwitchHardwareOffloadData.DefaultQueueVrssMinQueuePairs
- Msvm_EthernetSwitchHardwareOffloadData.DefaultQueueVmmqEnabled
- Msvm_EthernetSwitchHardwareOffloadData.DefaultQueueVrssEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b64762b824cea7d3b064636e7f7f87777e053daf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985167"
---
# <a name="msvm_ethernetswitchhardwareoffloaddata-class"></a>Msvm \_ EthernetSwitchHardwareOffloadData 類別

代表交換器硬體卸載狀態。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("1C37E01C-0CD6-496F-9076-90C131033DC2"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("4"), InterfaceRevision("0"), DisplayName("Ethernet Switch Offload Resource Status"), AMENDMENT]
class Msvm_EthernetSwitchHardwareOffloadData : Msvm_EthernetSwitchData
{
  string  InstanceID;
  string  Caption = Ethernet Switch Offload Resource Status;
  string  Description = Represents the switch hardware offload status.;
  string  ElementName = Ethernet Switch Offload Resource Status;
  string  SystemCreationClassName = "Msvm_VirtualEthernetSwitch";
  string  SystemName;
  string  CreationClassName = "Msvm_EthernetSwitchHardwareOffloadData";
  string  Name;
  uint32  IovVfCapacity = 0;
  uint32  IovVfUsage = 0;
  uint32  VmqCapacity = 0;
  uint32  VmqUsage = 0;
  uint32  IPsecSACapacity = 0;
  uint32  IPsecSAUsage = 0;
  uint32  IovQueuePairCapacity = 0;
  uint32  IovQueuePairUsage = 0;
  boolean PacketDirectInUse = FALSE;
  uint32  DefaultQueueVmmqQueuePairs = 0;
  boolean DefaultQueueVrssIndependentHostSpreading = TRUE;
  boolean DefaultQueueVrssExcludePrimaryProcessor = FALSE;
  uint32  DefaultQueueVrssQueueSchedulingMode = 0;
  uint32  DefaultQueueVrssMinQueuePairs = 0;
  boolean DefaultQueueVmmqEnabled = FALSE;
  boolean DefaultQueueVrssEnabled = FALSE;
};
```

## <a name="members"></a>成員

**Msvm \_ EthernetSwitchHardwareOffloadData** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ EthernetSwitchHardwareOffloadData** 類別具有這些屬性。

<dl> <dt>

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

建立這個實例時所使用的類別或子類別名稱。 這個屬性繼承自 [**Msvm \_ EthernetSwitchData**](msvm-ethernetswitchdata.md)。

</dd> <dt>

**DefaultQueueVmmqEnabled**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (11) 、 **InterfaceVersion** (3) 、 **InterfaceRevision** (0) 
</dt> </dl>

預設佇列的目前 VMMQ 設定

> [!Note]  
> 在 Windows 10 1703 版中加入的屬性。

 

</dd> <dt>

**DefaultQueueVmmqQueuePairs**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (12) 、 **InterfaceVersion** (3) 、 **InterfaceRevision** (0) 
</dt> </dl>

目前配置給預設佇列的佇列數目

> [!Note]  
> 在 Windows 10 1703 版中加入的屬性。

 

</dd> <dt>

**DefaultQueueVrssEnabled**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (10) 、 **InterfaceVersion** (3) 、 **InterfaceRevision** (0) 
</dt> </dl>

預設佇列的目前 VRss 設定

> [!Note]  
> 在 Windows 10 1703 版中加入的屬性。

 

</dd> <dt>

**DefaultQueueVrssExcludePrimaryProcessor**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (15) 、 **InterfaceVersion** (4) 、 **InterfaceRevision** (0) 
</dt> </dl>

指出是否從 VRSS/VMMQ 間接資料表排除主要 VMQ CPU。

> [!Note]  
> 在 Windows 10 1709 版中新增。

 

</dd> <dt>

**DefaultQueueVrssIndependentHostSpreading**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (16) 、 **InterfaceVersion** (4) 、 **InterfaceRevision** (0) 
</dt> </dl>

指出是否一律針對預設佇列進行 VRSS 分配，不論外部 vPort 的 RSS 狀態為何。

> [!Note]  
> 在 Windows 10 1709 版中新增。

 

</dd> <dt>

**DefaultQueueVrssMinQueuePairs**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (13) 、 **InterfaceVersion** (4) 、 **InterfaceRevision** (0) 
</dt> </dl>

指出用於 VRSS/VMMQ 的佇列數目下限。

> [!Note]  
> 在 Windows 10 1709 版中新增。

 

</dd> <dt>

**DefaultQueueVrssQueueSchedulingMode**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (14) 、 **InterfaceVersion** (4) 、 **InterfaceRevision** (0) 
</dt> </dl>

指出如何將 VRSS/VMMQ 佇列操縱至不同的主機處理器。

> [!Note]  
> 在 Windows 10 1709 版中新增。

 

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

**IovQueuePairCapacity**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (7) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) 
</dt> </dl>

參數所支援的佇列配對數目上限。

</dd> <dt>

**IovQueuePairUsage**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (8) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) 
</dt> </dl>

參數目前正在使用的佇列組數。

</dd> <dt>

**IovVfCapacity**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (1) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) 
</dt> </dl>

參數支援的虛擬函式數目上限。

</dd> <dt>

**IovVfUsage**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (2) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) 
</dt> </dl>

目前參數正在使用的虛擬函式數目。

</dd> <dt>

**IPsecSACapacity**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (5) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) 
</dt> </dl>

交換器支援的 IPsec 安全性關聯卸載數目上限。

</dd> <dt>

**IPsecSAUsage**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (6) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) 
</dt> </dl>

交換器正在使用的目前 IPsec 安全性關聯的數目。

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **Key**、 **Override**、 **MaxLen** (256) 
</dt> </dl>

資源的唯一名稱。 這個屬性繼承自 [**Msvm \_ EthernetSwitchData**](msvm-ethernetswitchdata.md)。

</dd> <dt>

**PacketDirectInUse**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (9) 、 **InterfaceVersion** (2) 、 **InterfaceRevision** (0) 
</dt> </dl>

指出交換器是否正在使用封包直接存取

> [!Note]  
> 在 Windows 10 中新增的屬性。

 

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **Key**、 **MaxLen** (256) 
</dt> </dl>

裝載系統的建立類別名稱。 這個屬性繼承自 [**Msvm \_ EthernetSwitchData**](msvm-ethernetswitchdata.md)。

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **Key**、 **MaxLen** (256) 
</dt> </dl>

相關聯的資源實例所系結之虛擬交換器的名稱。 這個屬性繼承自 [**Msvm \_ EthernetSwitchData**](msvm-ethernetswitchdata.md)。

</dd> <dt>

**VmqCapacity**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (3) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) 
</dt> </dl>

交換器支援的虛擬機器佇列卸載數目上限。

</dd> <dt>

**VmqUsage**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (4) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) 
</dt> </dl>

交換器正在使用的目前虛擬機器佇列數目。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

