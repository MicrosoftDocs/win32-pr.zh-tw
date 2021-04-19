---
description: 代表虛擬機器的磁片合併設定的設定狀態。
ms.assetid: b4c0afeb-ce37-4eec-8aba-0d74115c463f
title: Msvm_DiskMergeSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DiskMergeSettingData
- Msvm_DiskMergeSettingData.InstanceID
- Msvm_DiskMergeSettingData.Caption
- Msvm_DiskMergeSettingData.Description
- Msvm_DiskMergeSettingData.ElementName
- Msvm_DiskMergeSettingData.EnabledState
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: fe702c382fb0636579a8ab1355bfd1299657b214
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979332"
---
# <a name="msvm_diskmergesettingdata-class"></a>Msvm \_ DiskMergeSettingData 類別

代表虛擬機器的磁片合併設定的設定狀態。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_DiskMergeSettingData : CIM_SettingData
{
  string InstanceID = "Microsoft:GUID\DeviceSpecificData";
  string Caption = "Disk Merge Setting Data";
  string Description = "Microsoft Disk Merge Setting Data";
  string ElementName = "Disk Merge Setting Data";
  uint32 EnabledState = 1;
};
```

## <a name="members"></a>成員

**Msvm \_ DiskMergeSettingData** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ DiskMergeSettingData** 類別具有這些屬性。

<dl> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的簡短描述。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) 類別，一律設定為「磁片合併設定資料」。

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

對物件的描述。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設為「Microsoft 磁片合併設定資料」。

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的顯示名稱。 這個屬性繼承自 [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))，一律設為「磁片合併設定資料」。 變更這個屬性將會變更相關聯之 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)衍生的 **ElementName** 屬性。

這是唯讀屬性，但是可以使用 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md)方法來變更。

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定磁片合併功能的啟用狀態。

<dt>

<span id="Temporarily_disabled"></span><span id="temporarily_disabled"></span><span id="TEMPORARILY_DISABLED"></span>

**暫時停用** (0) 


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**已啟用** (1) 


</dt> <dd></dd> </dl>

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 **鍵**
</dt> </dl>

唯一識別此類別的實例。 這個屬性繼承自 [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)) ，一律設定為 "Microsoft：*GUID* \\ *DeviceSpecificData*"。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

