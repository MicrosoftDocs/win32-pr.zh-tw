---
description: 代表存在於單一主機系統上的虛擬化服務的設定。
ms.assetid: E3265AFE-0117-4F59-9A6B-34CEA7A61EDD
title: Msvm_VirtualSystemManagementServiceSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementServiceSettingData
- Msvm_VirtualSystemManagementServiceSettingData.InstanceID
- Msvm_VirtualSystemManagementServiceSettingData.Caption
- Msvm_VirtualSystemManagementServiceSettingData.Description
- Msvm_VirtualSystemManagementServiceSettingData.ElementName
- Msvm_VirtualSystemManagementServiceSettingData.BiosLockString
- Msvm_VirtualSystemManagementServiceSettingData.DefaultExternalDataRoot
- Msvm_VirtualSystemManagementServiceSettingData.DefaultVirtualHardDiskPath
- Msvm_VirtualSystemManagementServiceSettingData.MaximumMacAddress
- Msvm_VirtualSystemManagementServiceSettingData.MinimumMacAddress
- Msvm_VirtualSystemManagementServiceSettingData.NumaSpanningEnabled
- Msvm_VirtualSystemManagementServiceSettingData.PrimaryOwnerContact
- Msvm_VirtualSystemManagementServiceSettingData.PrimaryOwnerName
- Msvm_VirtualSystemManagementServiceSettingData.HbaLunTimeout
- Msvm_VirtualSystemManagementServiceSettingData.MaximumWWPNAddress
- Msvm_VirtualSystemManagementServiceSettingData.MinimumWWPNAddress
- Msvm_VirtualSystemManagementServiceSettingData.CurrentWWNNAddress
- Msvm_VirtualSystemManagementServiceSettingData.DefaultVirtualHardDiskCachingMode
- Msvm_VirtualSystemManagementServiceSettingData.HypervisorRootSchedulerEnabled
- Msvm_VirtualSystemManagementServiceSettingData.EnhancedSessionModeEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 782f196fdbd3a09126a7b4d14be6789bb633f043
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106998226"
---
# <a name="msvm_virtualsystemmanagementservicesettingdata-class"></a>Msvm \_ VirtualSystemManagementServiceSettingData 類別

代表存在於單一主機系統上的虛擬化服務的設定。 無法直接修改這個類別的屬性。 用戶端必須呼叫 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md)方法，才能修改這些屬性的任何一個。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemManagementServiceSettingData : CIM_SettingData
{
  string  InstanceID = "Microsoft:host";
  string  Caption = "Hyper-V Virtual System Management Service";
  string  Description = "Settings for the Virtual System Management Service";
  string  ElementName = "Hyper-V Virtual System Management Service";
  string  BiosLockString;
  string  DefaultExternalDataRoot = "root\ProgramData\Microsoft\Windows\Virtualization";
  string  DefaultVirtualHardDiskPath = "root\Users\Public\Documents\Virtual Hard Disks";
  string  MaximumMacAddress;
  string  MinimumMacAddress;
  boolean NumaSpanningEnabled;
  string  PrimaryOwnerContact = "";
  string  PrimaryOwnerName = "Administrators";
  uint32  HbaLunTimeout;
  string  MaximumWWPNAddress;
  string  MinimumWWPNAddress;
  string  CurrentWWNNAddress;
  uint16  DefaultVirtualHardDiskCachingMode;
  boolean HypervisorRootSchedulerEnabled;
  boolean EnhancedSessionModeEnabled;
};
```

## <a name="members"></a>成員

**Msvm \_ VirtualSystemManagementServiceSettingData** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ VirtualSystemManagementServiceSettingData** 類別具有這些屬性。

<dl> <dt>

**BiosLockString**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32) 
</dt> </dl>

Oem 用來允許 BIOS 鎖定的 Windows 作業系統在虛擬機器中執行。 這個字串的長度必須剛好是32個字元。

這是唯讀屬性，但是可以使用 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md)方法來變更。

</dd> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的簡短描述。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「Hyper-v 虛擬系統管理服務」。

</dd> <dt>

**CurrentWWNNAddress**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

全球節點名稱 (WWNN) 位址，適用于綜合主機匯流排介面卡所用動態產生的全球名稱位址。

這是唯讀屬性，但是可以使用 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md)方法來變更。

</dd> <dt>

**DefaultExternalDataRoot**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)。**ConfigurationDataRoot**") 
</dt> </dl>

預設的外部資料根目錄。 根據預設，「*root* \\ ProgramData \\ Microsoft \\ Windows \\ 虛擬化」。

這是唯讀屬性，但是可以使用 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md)方法來變更。

</dd> <dt>

**DefaultVirtualHardDiskCachingMode**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出預設是否應將記憶體中的檔案快取用於磁片。 您可以在 [**Msvm \_ StorageAllocationSettingData**](msvm-storageallocationsettingdata.md)類別的 **CachingMode** 欄位中，以每個磁片為基礎覆寫此值。

> [!Note]  
> 在 Windows 10 和 Windows Server 2016 中新增。

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 (0) 


</dt> <dd></dd> <dt>

<span id="No_Caching"></span><span id="no_caching"></span><span id="NO_CACHING"></span>

**沒有** 快取 (3) 


</dt> <dd></dd> <dt>

<span id="Cache_Sharable_Parents"></span><span id="cache_sharable_parents"></span><span id="CACHE_SHARABLE_PARENTS"></span>

快取可 **共用** 的父系 (4) 


</dt> <dd></dd> </dl>

</dd> <dt>

**DefaultVirtualHardDiskPath**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

預設虛擬硬碟路徑。 依預設，「*根* \\ 使用者 \\ 公用 \\ 檔 \\ 虛擬硬碟」。

這是唯讀屬性，但是可以使用 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md)方法來變更。

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

對物件的描述。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「虛擬系統管理服務的設定」。

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的顯示名稱。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「Hyper-v 虛擬系統管理服務」。 變更這個屬性將會變更相關聯之 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)衍生的 **ElementName** 屬性。

</dd> <dt>

**EnhancedSessionModeEnabled**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出伺服器是否允許增強的會話模式。 **True** 表示允許，否則 **為 False**。

**Windows 8.1：** 在 Windows 8.1 和 Windows Server 2012 R2 之前，不支援這個值。

</dd> <dt>

**HbaLunTimeout**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定綜合光纖通道虛擬裝置在啟動虛擬機器之前，會等待邏輯單元編號 (LUN) 出現的時間量。

這是唯讀屬性，但是可以使用 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md)方法來變更。

</dd> <dt>

**HypervisorRootSchedulerEnabled**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

是否啟用虛擬程式根排程器。

> [!Note]  
> 在 Windows 10 1709 版中新增。

 

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 **鍵**
</dt> </dl>

唯一識別此類別的實例。 這個屬性繼承自 [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))，而且一律設定為 "Microsoft：*host*"，其中 *Host* 是主控電腦系統的 NetBIOS 名稱。

</dd> <dt>

**MaximumMacAddress**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

動態產生的 MAC 位址之 MAC 位址的上限。

這是唯讀屬性，但是可以使用 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md)方法來變更。

</dd> <dt>

**MaximumWWPNAddress**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

最大全球埠名稱 (WWPN) 位址，適用于綜合主機匯流排介面卡所用的動態產生全球名稱位址。

這是唯讀屬性，但是可以使用 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md)方法來變更。

</dd> <dt>

**MinimumMacAddress**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

動態產生的 MAC 位址之 MAC 位址的最小值。

這是唯讀屬性，但是可以使用 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md)方法來變更。

</dd> <dt>

**MinimumWWPNAddress**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

動態產生的全球通訊埠名稱位址，用於綜合主機匯流排介面卡。

這是唯讀屬性，但是可以使用 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md)方法來變更。

</dd> <dt>

**NumaSpanningEnabled**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定當啟動虛擬機器時，或是將記憶體指派給虛擬機器的動態記憶體時，是否可以從遠端非統一記憶體存取 (NUMA) 節點配置記憶體。 這可以是下列其中一個值。



| 值                                                                                | 意義                                                                                     |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <dt>**對**</dt> </dl>  | 您可以從本機和遠端 NUMA 節點配置記憶體。<br/>                   |
| <dl> <dt>**否**</dt> </dl> | 記憶體只能從指派給虛擬機器的 NUMA 節點進行配置。<br/> |



 

這是唯讀屬性，但是可以使用 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md)方法來變更。

</dd> <dt>

**PrimaryOwnerContact**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| 一般資訊 \| 001.4 ") 
</dt> </dl>

說明如何聯繫主要系統擁有者 (例如電話號碼或電子郵件地址) 。 預設為空白。 此名稱的長度不得超過256個字元。

這是唯讀屬性，但是可以使用 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md)方法來變更。

</dd> <dt>

**PrimaryOwnerName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| 一般資訊 \| 001.3 ") 
</dt> </dl>

主要系統擁有者的名稱。 依預設，「系統管理員」。 此值的長度不得超過64個字元。

這是唯讀屬性，但是可以使用 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md)方法來變更。

</dd> </dl>

## <a name="remarks"></a>備註

存取 **Msvm \_ VirtualSystemManagementServiceSettingData** 類別可能受 UAC 篩選所限制。 如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。

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

[**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md)
</dt> <dt>

[**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))
</dt> <dt>

[虛擬系統管理類別](virtual-system-management-classes.md)
</dt> </dl>

 

