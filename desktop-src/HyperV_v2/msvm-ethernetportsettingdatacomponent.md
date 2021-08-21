---
description: 用來建立 &\# 0034 的關聯、&0034 的一部分、 \# Msvm EthernetPortAllocationSettingData 的一個實例之間的關聯性 \_ ，以及一個或多個 Msvm \_ EthernetSwitchFeatureSettingData 實例之間的關聯性。
ms.assetid: fab15342-a134-4d4a-9668-1272041614b9
title: Msvm_EthernetPortSettingDataComponent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetPortSettingDataComponent
- Msvm_EthernetPortSettingDataComponent.GroupComponent
- Msvm_EthernetPortSettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 989d734d4c59d710c737c218b22591517347a8f5e434ff99e195887cbb4b6774
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119524838"
---
# <a name="msvm_ethernetportsettingdatacomponent-class"></a>Msvm \_ EthernetPortSettingDataComponent 類別

用來建立一個 [**Msvm \_ EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) 實例與一個或多個 [**Msvm \_ EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md)實例之間「部分」關聯性的關聯。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetPortSettingDataComponent : CIM_Component
{
  Msvm_EthernetPortAllocationSettingData    REF GroupComponent;
  Msvm_EthernetSwitchPortFeatureSettingData REF PartComponent;
};
```

## <a name="members"></a>成員

**Msvm \_ EthernetPortSettingDataComponent** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ EthernetPortSettingDataComponent** 類別具有這些屬性。

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

資料類型： **[ **Msvm \_ EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md)**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)、覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "GroupComponent" ) 、 [**匯總**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

代表 Ethernet 埠之 [**Msvm \_ EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) 類別實例的參考。

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

資料類型： **[ **Msvm \_ EthernetSwitchPortFeatureSettingData**](msvm-ethernetswitchportfeaturesettingdata.md)**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "PartComponent" ) 
</dt> </dl>

[**Msvm \_ EthernetSwitchPortFeatureSettingData**](msvm-ethernetswitchportfeaturesettingdata.md)類別實例的參考，代表套用至埠的功能設定。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

