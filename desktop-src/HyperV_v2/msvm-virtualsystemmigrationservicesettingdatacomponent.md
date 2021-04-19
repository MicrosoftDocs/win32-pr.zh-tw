---
description: 用來表示虛擬系統移轉服務之虛擬系統移轉網路設定的關聯。
ms.assetid: 5704dce7-1db3-4049-8c61-58bfa9596766
title: Msvm_VirtualSystemMigrationServiceSettingDataComponent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationServiceSettingDataComponent
- Msvm_VirtualSystemMigrationServiceSettingDataComponent.GroupComponent
- Msvm_VirtualSystemMigrationServiceSettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1ba69ebd6cfd50b30923db2ecc87e7e5aeebcaa5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106997482"
---
# <a name="msvm_virtualsystemmigrationservicesettingdatacomponent-class"></a>Msvm \_ VirtualSystemMigrationServiceSettingDataComponent 類別

用來表示虛擬系統移轉服務之虛擬系統移轉網路設定的關聯。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemMigrationServiceSettingDataComponent : CIM_Component
{
  Msvm_VirtualSystemMigrationServiceSettingData REF GroupComponent;
  Msvm_VirtualSystemMigrationNetworkSettingData REF PartComponent;
};
```

## <a name="members"></a>成員

**Msvm \_ VirtualSystemMigrationServiceSettingDataComponent** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ VirtualSystemMigrationServiceSettingDataComponent** 類別具有這些屬性。

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

資料類型： **Msvm \_ VirtualSystemMigrationServiceSettingData**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)、覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "GroupComponent" ) 、 [**匯總**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

代表遷移服務設定之 [**Msvm \_ VirtualSystemMigrationServiceSettingData**](msvm-virtualsystemmigrationservicesettingdata.md) 類別實例的參考。

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

資料類型： **Msvm \_ VirtualSystemMigrationNetworkSettingData**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "PartComponent" ) 
</dt> </dl>

代表遷移網路設定之 [**Msvm \_ VirtualSystemMigrationNetworkSettingData**](msvm-virtualsystemmigrationnetworksettingdata.md) 類別實例的參考。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

