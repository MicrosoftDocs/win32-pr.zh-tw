---
description: 表示埠卸載功能設定資料。
ms.assetid: 7b8d8bee-86f3-4c55-bb32-987bf840d995
title: Msvm_EthernetSwitchPortOffloadSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortOffloadSettingData
- Msvm_EthernetSwitchPortOffloadSettingData.InstanceID
- Msvm_EthernetSwitchPortOffloadSettingData.Caption
- Msvm_EthernetSwitchPortOffloadSettingData.Description
- Msvm_EthernetSwitchPortOffloadSettingData.ElementName
- Msvm_EthernetSwitchPortOffloadSettingData.IPSecOffloadLimit
- Msvm_EthernetSwitchPortOffloadSettingData.VMQOffloadWeight
- Msvm_EthernetSwitchPortOffloadSettingData.IOVOffloadWeight
- Msvm_EthernetSwitchPortOffloadSettingData.IOVQueuePairsRequested
- Msvm_EthernetSwitchPortOffloadSettingData.IOVInterruptModeration
- Msvm_EthernetSwitchPortOffloadSettingData.PacketDirectModerationInterval
- Msvm_EthernetSwitchPortOffloadSettingData.VmmqQueuePairs
- Msvm_EthernetSwitchPortOffloadSettingData.VrssVmbusChannelAffinityPolicy
- Msvm_EthernetSwitchPortOffloadSettingData.VrssIndependentHostSpreading
- Msvm_EthernetSwitchPortOffloadSettingData.VrssExcludePrimaryProcessor
- Msvm_EthernetSwitchPortOffloadSettingData.VrssQueueSchedulingMode
- Msvm_EthernetSwitchPortOffloadSettingData.VrssMinQueuePairs
- Msvm_EthernetSwitchPortOffloadSettingData.VmmqEnabled
- Msvm_EthernetSwitchPortOffloadSettingData.VrssEnabled
- Msvm_EthernetSwitchPortOffloadSettingData.PacketDirectModerationCount
- Msvm_EthernetSwitchPortOffloadSettingData.PacketDirectNumProcs
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ddf58a10e85003a00e0d757f29db55a49f98f0ba22e8c3124b83a593f2a3908f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118148297"
---
# <a name="msvm_ethernetswitchportoffloadsettingdata-class"></a>Msvm \_ EthernetSwitchPortOffloadSettingData 類別

表示埠卸載功能設定資料。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("C885BFD1-ABB7-418F-8163-9F379C9F7166"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("4"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Offload Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortOffloadSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string  InstanceID;
  string  Caption = "Ethernet Switch Port Offload Settings";
  string  Description = "Represents the port offload feature setting data.";
  string  ElementName = "Ethernet Switch Port Offload Settings";
  uint32  IPSecOffloadLimit = 512;
  uint32  VMQOffloadWeight = 100;
  uint32  IOVOffloadWeight = 0;
  uint32  IOVQueuePairsRequested = 1;
  uint32  IOVInterruptModeration = 0;
  uint32  PacketDirectModerationInterval = 0;
  uint32  VmmqQueuePairs = 16;
  uint32  VrssVmbusChannelAffinityPolicy = 3;
  boolean VrssIndependentHostSpreading = FALSE;
  boolean VrssExcludePrimaryProcessor = FALSE;
  uint32  VrssQueueSchedulingMode = 2;
  uint32  VrssMinQueuePairs = 1;
  boolean VmmqEnabled = FALSE;
  boolean VrssEnabled = TRUE;
  uint32  PacketDirectModerationCount = 0;
  uint32  PacketDirectNumProcs = 1;
};
```

## <a name="members"></a>成員

**Msvm \_ EthernetSwitchPortOffloadSettingData** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ EthernetSwitchPortOffloadSettingData** 類別具有這些屬性。

<dl> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的簡短描述。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「乙太網路交換器埠卸載設定」。

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

對物件的描述。 這個屬性會繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，而且一律會設定為「代表埠卸載功能設定資料」。

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的顯示名稱。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「乙太網路交換器埠卸載設定」。

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

**IOVInterruptModeration**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： **WmiDataId** (5) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) 
</dt> </dl>

I/o 虛擬化的中斷仲裁值 (插) 卸載。 預設值是 0。

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

**預設** (0) 


</dt> <dd></dd> <dt>

<span id="Adaptive"></span><span id="adaptive"></span><span id="ADAPTIVE"></span>

**適應性** (1) 


</dt> <dd></dd> <dt>

<span id="Off"></span><span id="off"></span><span id="OFF"></span>

**關閉** (2) 


</dt> <dd></dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

**低** (100) 


</dt> <dd></dd> <dt>

<span id="Medium"></span><span id="medium"></span><span id="MEDIUM"></span>

**中型** (200) 


</dt> <dd></dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

**高** (300) 


</dt> <dd></dd> </dl>

</dd> <dt>

**IOVOffloadWeight**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： **WmiDataId** (3) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) 
</dt> </dl>

指派給此埠以進行 i/o 虛擬化 (的權數) 卸載。 權數是指派的 SR-IOV 資源時的相對重要性。 將 **IOVOffloadWeight** 屬性設定為0會停用埠上的 sr-iov 卸載。 預設值是 0。

</dd> <dt>

**IOVQueuePairsRequested**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： **WmiDataId** (4) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) 
</dt> </dl>

針對此埠 (的 i/o 虛擬化所要求的佇列配對數目) 卸載。 預設值是 1。

</dd> <dt>

**IPSecOffloadLimit**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： **WmiDataId** (1) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) 
</dt> </dl>

允許從埠 (SA) 卸載位置的安全性關聯數目上限。

</dd> <dt>

**PacketDirectModerationCount**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： **WmiDataId** (7) 、 **InterfaceVersion** (2) 、 **InterfaceRevision** (0) 
</dt> </dl>

封包直接 (PD) 的中斷仲裁計數值。預設值為0。

> [!Note]  
> 在 Windows 10 中新增的屬性。

 

</dd> <dt>

**PacketDirectModerationInterval**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： **WmiDataId** (8) 、 **InterfaceVersion** (2) 、 **InterfaceRevision** (0) 
</dt> </dl>

封包直接 (PD) 的中斷仲裁間隔值。預設值為0。

> [!Note]  
> 在 Windows 10 中新增的屬性。

 

</dd> <dt>

**PacketDirectNumProcs**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： **WmiDataId** (6) 、 **InterfaceVersion** (2) 、 **InterfaceRevision** (0) 
</dt> </dl>

主機用來處理封包直接模式中從此埠傳送之封包的處理器數目。 預設值是 1。

> [!Note]  
> 在 Windows 10 中新增的屬性。

 

</dd> <dt>

**VmmqEnabled**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： **WmiDataId** (10) 、 **InterfaceVersion** (3) 、 **InterfaceRevision** (0) 
</dt> </dl>

如果硬體支援，請啟用 VMMQ 卸載。預設值為 False。

> [!Note]  
> 這個屬性是在 Windows 10、1703版和 Windows Server 2016 中加入的。

 

</dd> <dt>

**VmmqQueuePairs**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： **WmiDataId** (11) 、 **InterfaceVersion** (3) 、 **InterfaceRevision** (0) 
</dt> </dl>

啟用 VRSS 時要配置的佇列數目。 預設值是 16。

> [!Note]  
> 這個屬性是在 Windows 10、1703版和 Windows Server 2016 中加入的。

 

</dd> <dt>

**VMQOffloadWeight**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： **WmiDataId** (2) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) 
</dt> </dl>

指派給此埠的虛擬機器佇列 (VMQ) 卸載的加權。 加權是指派 VMQ 資源時的相對重要性。 將 **VMQOffloadWeight** 屬性設定為0會停用埠上的 VMQ。 預設值為 100。

</dd> <dt>

**VrssEnabled**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： **WmiDataId** (9) 、 **InterfaceVersion** (3) 、 **InterfaceRevision** (0) 
</dt> </dl>

啟用 VRSS。 預設值是 true。

> [!Note]  
> 這個屬性是在 Windows 10、1703版和 Windows Server 2016 中加入的。

 

</dd> <dt>

**VrssExcludePrimaryProcessor**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： **WmiDataId** (14) 、 **InterfaceVersion** (4) 、 **InterfaceRevision** (0) 
</dt> </dl>

是否要在啟用 VRSS 時，從 VRSS 間接資料表中排除主要 VMQ 處理器。預設值為 false。

> [!Note]  
> 在 Windows 10 1709 版中新增。

 

</dd> <dt>

**VrssIndependentHostSpreading**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： **WmiDataId** (15) 、 **InterfaceVersion** (4) 、 **InterfaceRevision** (0) 
</dt> </dl>

無論虛擬 NIC 的 RSS 設定為何，都要在啟用 VRSS 時一律進行主機端 VRSS。預設值為 false。

> [!Note]  
> 在 Windows 10 1709 版中新增。

 

</dd> <dt>

**VrssMinQueuePairs**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： **WmiDataId** (12) 、 **InterfaceVersion** (4) 、 **InterfaceRevision** (0) 
</dt> </dl>

啟用 VRSS 時要配置的佇列數目下限。預設值為1。

> [!Note]  
> 在 Windows 10 1709 版中新增。

 

</dd> <dt>

**VrssQueueSchedulingMode**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： **WmiDataId** (13) 、 **InterfaceVersion** (4) 、 **InterfaceRevision** (0) 
</dt> </dl>

啟用 VRSS 時要使用的佇列排程模式。預設值為靜態排程。

> [!Note]  
> 在 Windows 10 1709 版中新增。

 

</dd> <dt>

**VrssVmbusChannelAffinityPolicy**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： **WmiDataId** (16) 、 **InterfaceVersion** (4) 、 **InterfaceRevision** (0) 
</dt> </dl>

啟用 VRSS 時要使用的 vmbus 通道親和性原則。預設值為 [強式]。

> [!Note]  
> 在 Windows 10 1709 版中新增。

 

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

