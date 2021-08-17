---
description: 提供虛擬硬碟的設定資料。
ms.assetid: 492a0b81-86b2-4d7d-a118-6ec14e3971ed
title: Msvm_VirtualHardDiskSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualHardDiskSettingData
- Msvm_VirtualHardDiskSettingData.InstanceID
- Msvm_VirtualHardDiskSettingData.Caption
- Msvm_VirtualHardDiskSettingData.Description
- Msvm_VirtualHardDiskSettingData.ElementName
- Msvm_VirtualHardDiskSettingData.Type
- Msvm_VirtualHardDiskSettingData.Format
- Msvm_VirtualHardDiskSettingData.Path
- Msvm_VirtualHardDiskSettingData.ParentPath
- Msvm_VirtualHardDiskSettingData.ParentTimestamp
- Msvm_VirtualHardDiskSettingData.ParentIdentifier
- Msvm_VirtualHardDiskSettingData.MaxInternalSize
- Msvm_VirtualHardDiskSettingData.BlockSize
- Msvm_VirtualHardDiskSettingData.LogicalSectorSize
- Msvm_VirtualHardDiskSettingData.PhysicalSectorSize
- Msvm_VirtualHardDiskSettingData.VirtualDiskId
- Msvm_VirtualHardDiskSettingData.DataAlignment
- Msvm_VirtualHardDiskSettingData.PmemAddressAbstractionType
- Msvm_VirtualHardDiskSettingData.IsPmemCompatible
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b7f87ba072aaff03ab415ccabe803546a89192ecb1e28d85b628dd0655d47421
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068418"
---
# <a name="msvm_virtualharddisksettingdata-class"></a>Msvm \_ VirtualHardDiskSettingData 類別

提供虛擬硬碟的設定資料。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[AMENDMENT]
class Msvm_VirtualHardDiskSettingData : CIM_SettingData
{
  string   InstanceID;
  string   Caption = "Virtual Hard Disk Setting Data";
  string   Description = "Setting Data for a Virtual Hard Disk";
  string   ElementName;
  uint16   Type;
  uint16   Format;
  string   Path;
  string   ParentPath;
  DATETIME ParentTimestamp;
  string   ParentIdentifier;
  uint64   MaxInternalSize;
  uint32   BlockSize;
  uint32   LogicalSectorSize;
  uint32   PhysicalSectorSize;
  string   VirtualDiskId;
  uint64   DataAlignment;
  uint16   PmemAddressAbstractionType;
  boolean  IsPmemCompatible;
};
```

## <a name="members"></a>成員

**Msvm \_ VirtualHardDiskSettingData** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ VirtualHardDiskSettingData** 類別具有這些屬性。

<dl> <dt>

**BlockSize**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

虛擬硬碟使用的區塊大小（以位元組為單位）。

</dd> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的簡短描述。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設為「虛擬硬碟設定資料」。

</dd> <dt>

**DataAlignment**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

針對虛擬磁片的資料裝載，指定所需的對齊（以位元組為單位）

> [!Note]  
> 在 Windows 10 1709 版中新增。

 

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

對物件的描述。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「設定虛擬硬碟的資料」。

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的顯示名稱。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。

</dd> <dt>

**格式**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

虛擬硬碟的格式。 這會是下列其中一個值。

<dt>

<span id="VHD"></span><span id="vhd"></span>

<span id="VHD"></span><span id="vhd"></span>**VHD** (2) 


</dt> <dd></dd> <dt>

<span id="VHDX"></span><span id="vhdx"></span>

<span id="VHDX"></span><span id="vhdx"></span>**VHDX** (3) 


</dt> <dd></dd> <dt>

<span id="VHDSet"></span><span id="vhdset"></span><span id="VHDSET"></span>

<span id="VHDSet"></span><span id="vhdset"></span><span id="VHDSET"></span>**VHDSet** (4) 


</dt> <dd>

> [!Note]  
> 加入 Windows 10 和 Windows Server 2016。

 

</dd> </dl>

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 **鍵**
</dt> </dl>

唯一識別此類別的實例。 這個屬性繼承自 [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))。

</dd> <dt>

**IsPmemCompatible**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指定是否可使用虛擬磁片做為持續性記憶體裝置的備份存放區。

> [!Note]  
> 在 Windows 10 1709 版中新增。

 

</dd> <dt>

**LogicalSectorSize**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

虛擬硬碟使用的邏輯磁區大小（以位元組為單位）。

</dd> <dt>

**MaxInternalSize**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

虛擬機器可看見的虛擬硬碟大小上限（以位元組為單位）。 此大小將會四捨五入到磁區大小的下一個最大倍數。

</dd> <dt>

**ParentIdentifier**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

用來唯一識別虛擬硬碟父系的 GUID。 如果虛擬硬碟沒有父系，則此欄位為空白。

> [!Note]  
> 加入 Windows 10 和 Windows Server 2016。

 

</dd> <dt>

**ParentPath**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

虛擬硬碟的父系。 如果虛擬硬碟沒有父系，則這個屬性是空的。

</dd> <dt>

**ParentTimestamp**
</dt> <dd> <dl> <dt>

資料類型： **DATETIME**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

虛擬硬碟父系的時間戳記。 如果虛擬硬碟沒有父系，則此欄位為空白。

> [!Note]  
> 加入 Windows 10 和 Windows Server 2016。

 

</dd> <dt>

**路徑**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

虛擬硬碟的完整路徑。

</dd> <dt>

**PhysicalSectorSize**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

虛擬硬碟使用的實體磁區大小（以位元組為單位）。

</dd> <dt>

**PmemAddressAbstractionType**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

要搭配此虛擬磁片使用的持續性記憶體位址抽象方法。

> [!Note]  
> 在 Windows 10 1709 版中新增。

 

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**無** (0) 


</dt> <dd></dd> <dt>

<span id="BTT"></span><span id="btt"></span>

**.Btt** (1) 


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 (65535) 


</dt> <dd></dd> </dl>

</dd> <dt>

**類型**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

虛擬硬碟的類型。 這會是下列其中一個值。

<dt>

<span id="Fixed"></span><span id="fixed"></span><span id="FIXED"></span>

已 **修正** (2) 


</dt> <dd></dd> <dt>

<span id="Dynamic"></span><span id="dynamic"></span><span id="DYNAMIC"></span>

**Dynamic** (3) 


</dt> <dd></dd> <dt>

<span id="Differencing"></span><span id="differencing"></span><span id="DIFFERENCING"></span>

**差異** (4) 


</dt> <dd></dd> </dl>

</dd> <dt>

**VirtualDiskId**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

用來唯一識別虛擬磁片的 GUID。

當 [**Msvm \_ ImageManagementService. GetVirtualHardDiskSettingData**](getvirtualharddisksettingdata-msvm-imagemanagementservice.md) 方法傳回 **Msvm \_ VirtualHardDiskSettingData** 的實例時，用戶端可以使用此屬性來取得 VHD 的唯一磁片識別碼。

在衝突偵測或其他情況下，用戶端可以將 **VirtualDiskId** 值設定為新的 GUID，並將此 **Msvm \_ VirtualHardDiskSettingData** 實例傳遞至 [**Msvm \_ ImageManagementService. SETVIRTUALHARDDISKSETTINGDATA**](setvirtualharddisksettingdata-msvm-imagemanagementservice.md) 方法來變更 VHD 的磁片識別碼。 如果 VHD 不是 VHDX VHD，或 VHD 已附加，則作業會失敗。 如果傳遞的值格式不正確，也就是不是 GUID 或全部都是0，則作業也會失敗。 如果傳遞的值與目前的磁片識別碼相同，則作業會以無訊息模式成功。

[**SetVirtualDiskInformation**](/windows/win32/api/virtdisk/nf-virtdisk-setvirtualdiskinformation)函式所產生的錯誤會透過這個屬性向上反升。 用戶端也可以使用相同的機制，透過相同命名空間中的 [**Msvm \_ ImageManagementService. CreateVirtualHardDisk**](createvirtualharddisk-msvm-imagemanagementservice.md)方法，在建立 VHD 時提供 **VirtualDiskId** 值。 這可以用來建立 VHD1 或 VHD2 Vhd。

**Windows 8.1：** 在 Windows 8.1 和 Windows Server 2012 R2 之前，不支援這個值。

</dd> </dl>

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

[**CIM \_ SettingData**](cim-settingdata.md)
</dt> <dt>

[**GetVirtualHardDiskSettingData**](getvirtualharddisksettingdata-msvm-imagemanagementservice.md)
</dt> </dl>

 

