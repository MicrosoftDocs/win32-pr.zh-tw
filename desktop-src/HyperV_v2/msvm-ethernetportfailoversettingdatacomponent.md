---
description: 用來建立一個 Msvm EmulatedEthernetPortSettingData 實例之間關聯性的關聯 \_ ，以及一個或多個 Msvm EthernetSwitchFeatureSettingData 實例之間的關聯性 \_ 。
ms.assetid: A2929D81-ED86-4C5A-9280-276204EDE89B
title: Msvm_EthernetPortFailoverSettingDataComponent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetPortFailoverSettingDataComponent
- Msvm_EthernetPortFailoverSettingDataComponent.GroupComponent
- Msvm_EthernetPortFailoverSettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 50fff8688beea91495014dd75b1f1c33020869f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513500"
---
# <a name="msvm_ethernetportfailoversettingdatacomponent-class"></a>Msvm \_ EthernetPortFailoverSettingDataComponent 類別

用來建立一個 [**Msvm \_ EmulatedEthernetPortSettingData**](msvm-emulatedethernetportsettingdata.md) 實例之間關聯性的關聯，以及一個或多個 [**Msvm \_ EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md)實例之間的關聯性。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetPortFailoverSettingDataComponent : CIM_Component
{
  CIM_ResourceAllocationSettingData      REF GroupComponent;
  Msvm_FailoverNetworkAdapterSettingData REF PartComponent;
};
```

## <a name="members"></a>成員

**Msvm \_ EthernetPortFailoverSettingDataComponent** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ EthernetPortFailoverSettingDataComponent** 類別具有這些屬性。

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

資料類型： **[ **CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)、覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "GroupComponent" ) 、 [**匯總**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

代表 Ethernet 埠之 [**Msvm \_ EmulatedEthernetPortSettingData**](msvm-emulatedethernetportsettingdata.md) 或 [**Msvm \_ SyntheticEthernetPortSettingData**](msvm-syntheticethernetportsettingdata.md) 類別實例的參考。

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

資料類型： **[ **Msvm \_ FailoverNetworkAdapterSettingData**](msvm-failovernetworkadaptersettingdata.md)**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "PartComponent" ) 
</dt> </dl>

代表來賓網路介面卡設定之 [**Msvm \_ FailoverNetworkAdapterSettingData**](msvm-failovernetworkadaptersettingdata.md) 類別實例的參考。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

