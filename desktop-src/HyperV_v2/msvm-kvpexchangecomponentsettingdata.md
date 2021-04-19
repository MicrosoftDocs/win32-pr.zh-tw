---
description: 代表索引鍵/值組 exchange 服務的設定狀態。
ms.assetid: B7ED1091-E49A-4C38-9794-E074E6B9EF48
title: Msvm_KvpExchangeComponentSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_KvpExchangeComponentSettingData
- Msvm_KvpExchangeComponentSettingData.DisableHostKVPItems
- Msvm_KvpExchangeComponentSettingData.InstanceID
- Msvm_KvpExchangeComponentSettingData.Caption
- Msvm_KvpExchangeComponentSettingData.Description
- Msvm_KvpExchangeComponentSettingData.ElementName
- Msvm_KvpExchangeComponentSettingData.ResourceType
- Msvm_KvpExchangeComponentSettingData.OtherResourceType
- Msvm_KvpExchangeComponentSettingData.ResourceSubType
- Msvm_KvpExchangeComponentSettingData.PoolID
- Msvm_KvpExchangeComponentSettingData.ConsumerVisibility
- Msvm_KvpExchangeComponentSettingData.HostResource
- Msvm_KvpExchangeComponentSettingData.AllocationUnits
- Msvm_KvpExchangeComponentSettingData.VirtualQuantity
- Msvm_KvpExchangeComponentSettingData.Reservation
- Msvm_KvpExchangeComponentSettingData.Limit
- Msvm_KvpExchangeComponentSettingData.Weight
- Msvm_KvpExchangeComponentSettingData.AutomaticAllocation
- Msvm_KvpExchangeComponentSettingData.AutomaticDeallocation
- Msvm_KvpExchangeComponentSettingData.Parent
- Msvm_KvpExchangeComponentSettingData.Connection
- Msvm_KvpExchangeComponentSettingData.Address
- Msvm_KvpExchangeComponentSettingData.MappingBehavior
- Msvm_KvpExchangeComponentSettingData.AddressOnParent
- Msvm_KvpExchangeComponentSettingData.VirtualQuantityUnits
- Msvm_KvpExchangeComponentSettingData.EnabledState
- Msvm_KvpExchangeComponentSettingData.HostExchangeItems
- Msvm_KvpExchangeComponentSettingData.HostOnlyItems
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2fe2ef128d3212ba2dfd47a3d71f713c26ba2435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106988782"
---
# <a name="msvm_kvpexchangecomponentsettingdata-class"></a>Msvm \_ KvpExchangeComponentSettingData 類別

代表索引鍵/值組 exchange 服務的設定狀態。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_KvpExchangeComponentSettingData : CIM_ResourceAllocationSettingData
{
  boolean DisableHostKVPItems;
  string  InstanceID;
  string  Caption = "Key-Value Pair Exchange";
  string  Description = "Microsoft Key-Value Pair Exchange Service Setting Data";
  string  ElementName = "Key-Value Pair Exchange";
  uint16  ResourceType = 1;
  string  OtherResourceType = "Microsoft:Hyper-V:Key-Value Pair Exchange Component";
  string  ResourceSubType;
  string  PoolID;
  uint16  ConsumerVisibility = 3;
  string  HostResource[];
  string  AllocationUnits = "count";
  uint64  VirtualQuantity = 1;
  uint64  Reservation = 1;
  uint64  Limit = 1;
  uint32  Weight = 0;
  boolean AutomaticAllocation = True;
  boolean AutomaticDeallocation = True;
  string  Parent;
  string  Connection[];
  string  Address;
  uint16  MappingBehavior;
  string  AddressOnParent;
  string  VirtualQuantityUnits = "count";
  uint16  EnabledState = 2;
  String  HostExchangeItems[];
  String  HostOnlyItems[];
};
```

## <a name="members"></a>成員

**Msvm \_ KvpExchangeComponentSettingData** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ KvpExchangeComponentSettingData** 類別具有這些屬性。

<dl> <dt>

**位址**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

資源的位址。 這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) ，一律設為 **Null**。

</dd> <dt>

**AddressOnParent**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

描述此資源在父系內容中的位址。 **Parent** 和 **AddressOnParent** 屬性是用來描述控制器的關聯性，以及控制器上的裝置順序。 這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。

</dd> <dt>

**AllocationUnits**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

**保留** 和 **限制** 屬性所使用的配置單位。 這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。

</dd> <dt>

**AutomaticAllocation**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出是否會自動設定資源。 這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。

</dd> <dt>

**AutomaticDeallocation**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出是否會自動解除配置資源。 這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。

</dd> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的簡短描述。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。

</dd> <dt>

**[連接]**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

此資源所連接的目標。 這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) ，一律設為 **Null**。

</dd> <dt>

**ConsumerVisibility**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

取用者會看到已配置的資源。 這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。



| 值                                                                        | 意義                |
|------------------------------------------------------------------------------|------------------------|
| <dl> <dt>3</dt> </dl> | 虛擬<br/> |



 

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

對物件的描述。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。

</dd> <dt>

**DisableHostKVPItems**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

此屬性會停用主機，使其無法自動 populatinghost 來賓內的名稱和作業系統資訊。

> [!Note]  
> 這個屬性是在 Windows 10 1703 版中加入的。

 

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的顯示名稱。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

元素的啟用狀態。

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**已啟用** (2) 


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**停用** (3) 


</dt> <dd></dd> </dl>

</dd> <dt>

**HostExchangeItems**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Indexed" ) ， **HyperVEmbeddedInstance** ( "Msvm \_ KvpExchangeDataItem" ) 
</dt> </dl>

代表索引鍵/值組的內嵌 [**Msvm \_ KvpExchangeDataItem**](msvm-kvpexchangedataitem.md) 實例陣列。

</dd> <dt>

**HostOnlyItems**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Indexed" ) ， **HyperVEmbeddedInstance** ( "Msvm \_ KvpExchangeDataItem" ) 
</dt> </dl>

[**Msvm \_ KvpExchangeDataItem**](msvm-kvpexchangedataitem.md)實例的陣列，其中包含儲存在設定檔中但未與客體作業系統交換的索引鍵/值組。 這可讓應用程式儲存客體作業系統不需要看見的虛擬機器專屬資料。 專案的格式與 **HostExchangeItems** 屬性中的專案相同，不同之處在于 **Msvm \_ KvpExchangeDataItem** 實例的 [**來源**] 屬性設定為 [4]。 每個設定檔的限制為128個索引鍵/值組，其中每個值欄位的大小上限為 16 KB，而索引鍵欄位則允許最多512個位元組。

</dd> <dt>

**HostResource**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

公開特定指派給主機或基礎資源。 這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) ，一律設為 **Null**。

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

**限制**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

此配置將授與的上限或最大資源量。 這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。

</dd> <dt>

**MappingBehavior**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定此資源對應至基礎資源的方式。 這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) ，一律設為 **Null**。

</dd> <dt>

**OtherResourceType**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

描述資源類型的字串，當定義完善的值無法使用且 **ResourceType** 的值為1時 (其他) 。 這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。

</dd> <dt>

**父系**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

資源的父系。 這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) ，一律設為 **Null**。

</dd> <dt>

**PoolID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

從中配置資源的資源集區識別碼。 這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。

</dd> <dt>

**保留容量**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

保證可用於此配置的資源數量。 這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。

</dd> <dt>

**ResourceSubType**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

字串，描述此資源的執行特定子類型。 這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。

</dd> <dt>

**ResourceType**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

此配置設定所代表的資源類型。 這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。



| 值                                                                        | 意義          |
|------------------------------------------------------------------------------|------------------|
| <dl> <dt>1</dt> </dl> | 其他<br/> |



 

</dd> <dt>

**VirtualQuantity**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

向取用者呈現的資源數量。 這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。

</dd> <dt>

**VirtualQuantityUnits**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定此資源配置的度量單位。 這個屬性的值必須是程式設計單位辨識符號的合法值，如 DSP0004 2.5 或更新版本的附錄 C. 1 中所定義。 這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。

</dd> <dt>

**Weight**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

相對於相同資源集區中的其他配置，此配置的相對優先權。 這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。

</dd> </dl>

## <a name="remarks"></a>備註

存取 **Msvm \_ KvpExchangeComponentSettingData** 類別可能受 UAC 篩選所限制。 如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。

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

[**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md)
</dt> <dt>

[**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> </dl>

 

