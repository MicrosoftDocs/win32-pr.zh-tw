---
description: 提供有關手動掛接之儲存體映射的詳細資訊。
ms.assetid: 40b94c5f-c277-40c8-a55d-ebc64cb231ca
title: Msvm_MountedStorageImage 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MountedStorageImage
- Msvm_MountedStorageImage.InstanceID
- Msvm_MountedStorageImage.Caption
- Msvm_MountedStorageImage.Description
- Msvm_MountedStorageImage.ElementName
- Msvm_MountedStorageImage.InstallDate
- Msvm_MountedStorageImage.Name
- Msvm_MountedStorageImage.OperationalStatus
- Msvm_MountedStorageImage.StatusDescriptions
- Msvm_MountedStorageImage.Status
- Msvm_MountedStorageImage.HealthState
- Msvm_MountedStorageImage.CommunicationStatus
- Msvm_MountedStorageImage.DetailedStatus
- Msvm_MountedStorageImage.OperatingStatus
- Msvm_MountedStorageImage.PrimaryStatus
- Msvm_MountedStorageImage.Type
- Msvm_MountedStorageImage.Access
- Msvm_MountedStorageImage.PortNumber
- Msvm_MountedStorageImage.PathId
- Msvm_MountedStorageImage.TargetId
- Msvm_MountedStorageImage.Lun
- Msvm_MountedStorageImage.PnpDevicePath
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ad8f4d8542c7478dffbc87463f9bfe1ff4c2dc31fcc0ecc3bce2d293caa3a8b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119521188"
---
# <a name="msvm_mountedstorageimage-class"></a>Msvm \_ MountedStorageImage 類別

提供有關手動掛接之儲存體映射的詳細資訊。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MountedStorageImage : CIM_LogicalElement
{
  string   InstanceID;
  string   Caption = "Mounted Storage Image";
  string   Description = "Information about a mounted storage image.";
  string   ElementName = "Mounted Storage Image";
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[] = { "OK" };
  string   Status = "OK";
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   Type;
  uint16   Access;
  UINT8    PortNumber;
  UINT8    PathId;
  UINT8    TargetId;
  UINT8    Lun;
  string   PnpDevicePath;
};
```

## <a name="members"></a>成員

**Msvm \_ MountedStorageImage** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**Msvm \_ MountedStorageImage** 類別具有這些方法。



| 方法                                                                          | 描述                                    |
|:--------------------------------------------------------------------------------|:-----------------------------------------------|
| [**DetachVirtualHardDisk**](detachvirtualharddisk-msvm-mountedstorageimage.md) | 卸離掛接的存放裝置映射。<br/> |



 

### <a name="properties"></a>屬性

**Msvm \_ MountedStorageImage** 類別具有這些屬性。

<dl> <dt>

**存取**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

用來裝載儲存體映射的存取權。

<dt>

<span id="Read-only"></span><span id="read-only"></span><span id="READ-ONLY"></span>

**唯讀** (1) 


</dt> <dd></dd> <dt>

<span id="Read_Write"></span><span id="read_write"></span><span id="READ_WRITE"></span>

**讀取/寫入** (2) 


</dt> <dd></dd> </dl>

</dd> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的簡短描述。 這個屬性會繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，而且一律會包含「已掛接的儲存體映射」。

</dd> <dt>

**CommunicationStatus**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出檢測與基礎受管理元素通訊的能力。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且一律設定為 **Null**。

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

對物件的描述。 這個屬性是從 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)繼承而來，而且一律會包含「掛接的儲存映射相關資訊」。

</dd> <dt>

**DetailedStatus**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

補充 **PrimaryStatus** 屬性與其他狀態詳細資料。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且一律設定為 **Null**。

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的顯示名稱。 這個屬性會繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，而且一律會包含「已掛接的儲存體映射」。

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

專案目前的健康情況。 這個屬性會表示此元素的健全狀況，但不一定是它的子元件。 可能的值為0到30，其中5表示元素完全狀況良好，而30表示元素完全無法正常運作。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且一律設定為5。

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

建立虛擬機器設定的日期和時間。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 **鍵**
</dt> </dl>

唯一識別此類別的實例。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，且一律為 **Null**。

</dd> <dt>

**倫**
</dt> <dd> <dl> <dt>

資料類型： **UINT8**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

SCSI 位址 LUN 識別碼。

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

裝載之 VHD 的路徑。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

</dd> <dt>

**OperatingStatus**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

提供專案操作條件的目前狀態資訊，並可用於提供關於 **EnabledState** 屬性值的詳細資料。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且一律設定為 **Null**。

</dd> <dt>

**OperationalStatus**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的目前狀態。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且每個陣列元素一律設定為 **Null**。

</dd> <dt>

**PathId**
</dt> <dd> <dl> <dt>

資料類型： **UINT8**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

SCSI 位址路徑識別碼。

</dd> <dt>

**PnpDevicePath**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

PNP 裝置路徑。

**Windows 8.1：** 在 Windows 8.1 和 Windows Server 2012 R2 之前，不支援這個值。

</dd> <dt>

**PortNumber**
</dt> <dd> <dl> <dt>

資料類型： **UINT8**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

SCSI 位址埠號碼。

</dd> <dt>

**PrimaryStatus**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

提供高層級的狀態資訊。 這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且一律設定為 **Null**。

</dd> <dt>

**狀態**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且一律設定為 "OK"。

</dd> <dt>

**StatusDescriptions**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

描述各種 **OperationalStatus** 陣列值的字串。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且每個陣列元素一律設定為 "OK"。

</dd> <dt>

**TargetId**
</dt> <dd> <dl> <dt>

資料類型： **UINT8**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

SCSI 位址目標識別碼。

</dd> <dt>

**類型**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

裝載的儲存體映射類型。

<dt>

<span id="Virtual_Hard_Disk"></span><span id="virtual_hard_disk"></span><span id="VIRTUAL_HARD_DISK"></span>

**虛擬硬碟** (0) 


</dt> <dd></dd> <dt>

<span id="ISO_Image"></span><span id="iso_image"></span><span id="ISO_IMAGE"></span>

**ISO 映像** (1) 


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="remarks"></a>備註

存取 **Msvm \_ MountedStorageImage** 類別可能受 UAC 篩選所限制。 如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ LogicalElement**](cim-logicalelement.md)
</dt> <dt>

[**CIM \_ LogicalElement**](/windows/desktop/CIMWin32Prov/cim-logicalelement)
</dt> <dt>

[儲存體類](storage-classes.md)
</dt> </dl>

 

