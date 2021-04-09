---
description: 代表虛擬系統移轉服務接聽傳入虛擬系統移轉的網路。
ms.assetid: 24458602-ff5c-45c2-8053-00315b59d3bb
title: Msvm_VirtualSystemMigrationNetworkSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationNetworkSettingData
- Msvm_VirtualSystemMigrationNetworkSettingData.InstanceID
- Msvm_VirtualSystemMigrationNetworkSettingData.Caption
- Msvm_VirtualSystemMigrationNetworkSettingData.Description
- Msvm_VirtualSystemMigrationNetworkSettingData.ElementName
- Msvm_VirtualSystemMigrationNetworkSettingData.SubnetNumber
- Msvm_VirtualSystemMigrationNetworkSettingData.PrefixLength
- Msvm_VirtualSystemMigrationNetworkSettingData.Metric
- Msvm_VirtualSystemMigrationNetworkSettingData.Tags
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4f7c24bb754148fa8ede12292f308164512af646
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847761"
---
# <a name="msvm_virtualsystemmigrationnetworksettingdata-class"></a>Msvm \_ VirtualSystemMigrationNetworkSettingData 類別

代表虛擬系統移轉服務接聽傳入虛擬系統移轉的網路。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemMigrationNetworkSettingData : CIM_SettingData
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
  string SubnetNumber;
  uint8  PrefixLength;
  uint32 Metric;
  string Tags[];
};
```

## <a name="members"></a>成員

**Msvm \_ VirtualSystemMigrationNetworkSettingData** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ VirtualSystemMigrationNetworkSettingData** 類別具有這些屬性。

<dl> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的簡短描述。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) 類別。

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

物件的顯示名稱。 這個屬性繼承自 [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))。

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

**計量**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

此網路用於遷移的優先順序度量。 較低的值會在優先順序較高。

</dd> <dt>

**PrefixLength**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

遷移網路子網前置長度。

</dd> <dt>

**SubnetNumber**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

遷移網路子網號碼。

</dd> <dt>

**Tags** (標籤)
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

標記的陣列，代表哪個管理系統已為虛擬系統移轉服務設定此網路。

</dd> </dl>

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

[**CIM \_ SettingData**](cim-settingdata.md)
</dt> <dt>

[**ModifyNetworkSettings**](modifynetworksettings-msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

