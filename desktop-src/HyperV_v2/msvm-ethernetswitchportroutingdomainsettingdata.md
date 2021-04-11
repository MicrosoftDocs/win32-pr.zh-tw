---
description: 表示路由網域設定資料。
ms.assetid: 6216cc4e-b2aa-4344-b8fa-489b986c14be
title: Msvm_EthernetSwitchPortRoutingDomainSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortRoutingDomainSettingData
- Msvm_EthernetSwitchPortRoutingDomainSettingData.RoutingDomainGuid
- Msvm_EthernetSwitchPortRoutingDomainSettingData.RoutingDomainName
- Msvm_EthernetSwitchPortRoutingDomainSettingData.IsolationIdList
- Msvm_EthernetSwitchPortRoutingDomainSettingData.IsolationIdNameList
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 40e16a3c952e63ab89c345201742dafe24cdde7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103853155"
---
# <a name="msvm_ethernetswitchportroutingdomainsettingdata-class"></a>Msvm \_ EthernetSwitchPortRoutingDomainSettingData 類別

表示路由網域設定資料。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("BF874DF0-F729-4312-A0FA-194271B88990"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Routing Domain Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortRoutingDomainSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string RoutingDomainGuid = "";
  string RoutingDomainName = "";
  uint32 IsolationIdList[] = {};
  string IsolationIdNameList[] = {};
};
```

## <a name="members"></a>成員

**Msvm \_ EthernetSwitchPortRoutingDomainSettingData** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ EthernetSwitchPortRoutingDomainSettingData** 類別具有這些屬性。

<dl> <dt>

**IsolationIdList**
</dt> <dd> <dl> <dt>

資料類型： **uint32** 陣列
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： **WmiDataId** (3) 、 [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 、 [**修訂**](/windows/desktop/WmiSdk/standard-qualifiers) (0) 
</dt> </dl>

路由網域的 VirtualSubnetId 或 VLAN 識別碼。

</dd> <dt>

**IsolationIdNameList**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： **WmiDataId** (4) 、 [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 、 [**修訂**](/windows/desktop/WmiSdk/standard-qualifiers) (0) 
</dt> </dl>

VirtualSubnetId 或 VLAN 的易記名稱陣列。

</dd> <dt>

**RoutingDomainGuid**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (38) 、 **WmiDataId** (1) 、 [**版本**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 、 [**修訂**](/windows/desktop/WmiSdk/standard-qualifiers) (0) 
</dt> </dl>

路由網域 GUID。

</dd> <dt>

**RoutingDomainName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (127) 、 **WmiDataId** (2) 、 [**版本**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 、 [**修訂**](/windows/desktop/WmiSdk/standard-qualifiers) (0) 
</dt> </dl>

路由網域的易記名稱。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1<br/>                                                                                  |
| 最低支援的伺服器<br/> | Windows Server 2012 R2<br/>                                                                       |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Msvm \_ EthernetSwitchPortFeatureSettingData**](msvm-ethernetswitchportfeaturesettingdata.md)
</dt> </dl>

 

