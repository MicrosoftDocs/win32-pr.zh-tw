---
description: 表示隔離設定資料。
ms.assetid: f6bf5fcf-61c4-4e69-8ba0-fff4c4873368
title: Msvm_EthernetSwitchPortIsolationSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortIsolationSettingData
- Msvm_EthernetSwitchPortIsolationSettingData.IsolationMode
- Msvm_EthernetSwitchPortIsolationSettingData.AllowUntaggedTraffic
- Msvm_EthernetSwitchPortIsolationSettingData.DefaultIsolationId
- Msvm_EthernetSwitchPortIsolationSettingData.EnableMultiTenantStack
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3d7761b090cfd3bf2ae6aaaa92e9c5d09d55eae6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987598"
---
# <a name="msvm_ethernetswitchportisolationsettingdata-class"></a>Msvm \_ EthernetSwitchPortIsolationSettingData 類別

表示隔離設定資料。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("83AF2CCB-72C9-4479-A285-94E58A98CAA6"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Isolation Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortIsolationSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  uint32  IsolationMode = 0;
  boolean AllowUntaggedTraffic = FALSE;
  uint32  DefaultIsolationId = 0;
  Boolean EnableMultiTenantStack = FALSE;
};
```

## <a name="members"></a>成員

**Msvm \_ EthernetSwitchPortIsolationSettingData** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ EthernetSwitchPortIsolationSettingData** 類別具有這些屬性。

<dl> <dt>

**AllowUntaggedTraffic**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： **WmiDataId** (2) 、 [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 、 [**修訂**](/windows/desktop/WmiSdk/standard-qualifiers) (0) 
</dt> </dl>

是否允許埠傳送/接收未標記的流量。

</dd> <dt>

**DefaultIsolationId**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： **WmiDataId** (3) 、 [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 、 [**修訂**](/windows/desktop/WmiSdk/standard-qualifiers) (0) 
</dt> </dl>

當 **AllowedUntaggedTraffic** 為 **true** 時，將在所有傳送/接收流量上設定的預設 VirtualSubnetId 或 VLAN。

</dd> <dt>

**EnableMultiTenantStack**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： **WmiDataId** (4) 、 [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 、 [**修訂**](/windows/desktop/WmiSdk/standard-qualifiers) (0) 
</dt> </dl>

若 **為 true**，VM 中的網路堆疊將能夠存取隔離設定。 預設值為 **false**。

</dd> <dt>

**IsolationMode**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： **WmiDataId** (1) 、 [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 、 [**修訂**](/windows/desktop/WmiSdk/standard-qualifiers) (0) 
</dt> </dl>

埠是否使用 **VLAN** 或 **VirtualSubnetId** 進行隔離。 **NativeVirtualSubnetId** 可用於 WNV VirtualSubnetId 型網路。

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**無** (0) 


</dt> <dd></dd> <dt>

<span id="NativeVirtualSubnetId"></span><span id="nativevirtualsubnetid"></span><span id="NATIVEVIRTUALSUBNETID"></span>

**NativeVirtualSubnetId** (1) 


</dt> <dd></dd> <dt>

<span id="ExternalVirtualSubnetId"></span><span id="externalvirtualsubnetid"></span><span id="EXTERNALVIRTUALSUBNETID"></span>

**ExternalVirtualSubnetId** (2) 


</dt> <dd></dd> <dt>

<span id="VLAN"></span><span id="vlan"></span>

**VLAN** (3) 


</dt> <dd></dd> </dl>

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

 

