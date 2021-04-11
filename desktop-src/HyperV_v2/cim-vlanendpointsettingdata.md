---
description: 表示 VLAN 端點的設定資料。
ms.assetid: 5ef3cc55-cf27-40b4-9e94-2e2b42ca41c5
title: CIM_VLANEndpointSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VLANEndpointSettingData
- CIM_VLANEndpointSettingData.PruneEligibleVLANList
- CIM_VLANEndpointSettingData.NativeVLAN
- CIM_VLANEndpointSettingData.DefaultVLAN
- CIM_VLANEndpointSettingData.TrunkedVLANList
- CIM_VLANEndpointSettingData.AccessVLAN
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a510c4195c538ab9735e7544acec2c88beeaa1de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103853164"
---
# <a name="cim_vlanendpointsettingdata-class"></a>CIM \_ VLANEndpointSettingData 類別

表示 VLAN 端點的設定資料。

## <a name="syntax"></a>語法

``` syntax
[Experimental, Abstract, Version("2.11.0"), UMLPackagePath("CIM::Network::VLAN")]
class CIM_VLANEndpointSettingData : CIM_SettingData
{
  uint16 PruneEligibleVLANList[];
  uint16 NativeVLAN;
  uint16 DefaultVLAN;
  uint16 TrunkedVLANList[];
  uint16 AccessVLAN;
};
```

## <a name="members"></a>成員

**CIM \_ VLANEndpointSettingData** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ VLANEndpointSettingData** 類別具有這些屬性。

<dl> <dt>

**AccessVLAN**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**") 
</dt> </dl>

端點的存取 VLAN。

</dd> <dt>

**DefaultVLAN**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**") 
</dt> </dl>

主幹端點上原生 VLAN 的預設值。

> [!Note]  
> 只有當 VLAN 端點在 **OperationalEndpointMode** 屬性中指定的中繼模式下運作時，才會使用此屬性。

 

</dd> <dt>

**NativeVLAN**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**") 
</dt> </dl>

用來標記在主幹端點上收到之未標記流量的 VLAN ID。

> [!Note]  
> 只有當 VLAN 端點在 **SwitchEndpointMode** 屬性中指定的中繼模式下運作時，才會使用此屬性。

 

</dd> <dt>

**PruneEligibleVLANList**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**") 
</dt> </dl>

陣列，包含系統可能會從主幹端點移除的 Vlan 識別碼。

> [!Note]  
> 只有當 VLAN 端點在 **OperationalEndpointMode** 屬性中指定的中繼模式下運作時，才會使用此屬性。

 

</dd> <dt>

**TrunkedVLANList**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**") 
</dt> </dl>

陣列，其中包含已啟用中繼之 VLAN 端點的識別碼。

> [!Note]  
> 只有當 VLAN 端點在 **OperationalEndpointMode** 屬性中指定的中繼模式下運作時，才會使用此屬性。

 

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

[**CIM \_ SettingData**](cim-settingdata.md)
</dt> </dl>

 

