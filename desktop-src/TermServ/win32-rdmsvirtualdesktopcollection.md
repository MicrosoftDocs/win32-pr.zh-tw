---
title: Win32_RDMSVirtualDesktopCollection 類別
description: 建立及管理虛擬桌面集合。
ms.assetid: fe0a484e-f9e3-4b99-8e69-da8f337ae957
ms.tgt_platform: multiple
keywords:
- Win32_RDMSVirtualDesktopCollection 類別遠端桌面服務
- Win32_RDMSVirtualDesktopCollection 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection
- Win32_RDMSVirtualDesktopCollection.Alias
- Win32_RDMSVirtualDesktopCollection.Type
- Win32_RDMSVirtualDesktopCollection.IsManaged
- Win32_RDMSVirtualDesktopCollection.Name
- Win32_RDMSVirtualDesktopCollection.CollectionDescription
- Win32_RDMSVirtualDesktopCollection.SecurityDescriptor
- Win32_RDMSVirtualDesktopCollection.VmFarmSettings
- Win32_RDMSVirtualDesktopCollection.UserVHDSetting
- Win32_RDMSVirtualDesktopCollection.IconContents
- Win32_RDMSVirtualDesktopCollection.ShowInPortal
- Win32_RDMSVirtualDesktopCollection.IsHA
- Win32_RDMSVirtualDesktopCollection.IsUserAdmin
- Win32_RDMSVirtualDesktopCollection.RollbackEnabled
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 580b5ae194a28726a06143dce0007eeedfbb8564b49a4cbc2e7c2d0d8507dfe4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119868068"
---
# <a name="win32_rdmsvirtualdesktopcollection-class"></a>Win32 \_ RDMSVirtualDesktopCollection 類別

建立及管理虛擬桌面集合。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSVirtualDesktopCollection
{
  string  Alias;
  uint32  Type;
  boolean IsManaged;
  string  Name;
  string  CollectionDescription;
  string  SecurityDescriptor;
  string  VmFarmSettings;
  string  UserVHDSetting;
  uint8   IconContents[];
  boolean ShowInPortal;
  boolean IsHA;
  boolean IsUserAdmin;
  boolean RollbackEnabled;
};
```

## <a name="members"></a>成員

**Win32 \_ RDMSVirtualDesktopCollection** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**Win32 \_ RDMSVirtualDesktopCollection** 類別具有這些方法。



| 方法                                                                                            | 描述                                                                                                                                     |
|:--------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddVirtualDesktop**](addvirtualdesktop-win32-rdmsvirtualdesktopcollection.md)                 | 將虛擬桌面新增至虛擬桌面集合。<br/>                                                                              |
| [**CancelPatch**](cancelpatch-win32-rdmsvirtualdesktopcollection.md)                             | 取消虛擬機器集合中虛擬機器的軟體更新布建作業。<br/>                                 |
| [**GetInt32Property**](getint32property-win32-rdmsvirtualdesktopcollection.md)                   | 從虛擬桌面集合抓取整數屬性值。<br/>                                                               |
| [**GetPatchProperties**](getpatchproperties-win32-rdmsvirtualdesktopcollection.md)               | 抓取虛擬桌面集合中虛擬機器的軟體更新布建作業屬性。<br/>             |
| [**GetStringProperty**](getstringproperty-win32-rdmsvirtualdesktopcollection.md)                 | 從虛擬桌面集合抓取字串屬性值。<br/>                                                                 |
| [**ProvisioningEnumerateJobs**](provisioningenumeratejobs-win32-rdmsvirtualdesktopcollection.md) | 列舉此服務的虛擬桌面布建作業。<br/>                                                                       |
| [**ProvisioningJobCancel**](provisioningjobcancel-win32-rdmsvirtualdesktopcollection.md)         | 取消虛擬桌面布建作業。<br/>                                                                                          |
| [**ProvisioningJobExecute**](provisioningjobexecute-win32-rdmsvirtualdesktopcollection.md)       | 執行虛擬桌面布建作業。<br/>                                                                                             |
| [**ProvisioningJobGetReport**](provisioningjobgetreport-win32-rdmsvirtualdesktopcollection.md)   | 取得虛擬桌面布建作業狀態的相關報告。<br/>                                                                |
| [**ProvisioningPrepJob**](win32-rdmsvirtualdesktopcollection-provisioningprepjob.md)             | 建立虛擬桌面布建作業。<br/>                                                                                          |
| [**RemoveVirtualDesktop**](removevirtualdesktop-win32-rdmsvirtualdesktopcollection.md)           | 從虛擬桌面集合移除虛擬桌面。<br/>                                                                         |
| [**SchedulePatch**](schedulepatch-win32-rdmsvirtualdesktopcollection.md)                         | 排程軟體更新布建作業，此作業會在虛擬桌面集合中的虛擬機器上安裝軟體更新。<br/> |
| [**SetInt32Property**](setint32property-win32-rdmsvirtualdesktopcollection.md)                   | 更新虛擬桌面集合的整數屬性值。<br/>                                                                   |
| [**SetStringProperty**](setstringproperty-win32-rdmsvirtualdesktopcollection.md)                 | 更新虛擬桌面集合的字串屬性值。<br/>                                                                     |



 

### <a name="properties"></a>屬性

**Win32 \_ RDMSVirtualDesktopCollection** 類別具有這些屬性。

<dl> <dt>

**別名**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

取得或設定集合的別名。

</dd> <dt>

**CollectionDescription**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**選擇性**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

取得或設定集合的描述。

</dd> <dt>

**IconContents**
</dt> <dd> <dl> <dt>

資料類型： **uint8** 陣列
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**選擇性**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

取得或設定值的陣列，這些值會指定集合的圖示。

</dd> <dt>

**IsHA**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

取得或設定值，這個值會指出集合是否包含高可用性 Vm。 如果集合包含高可用性 Vm，則 **為 TRUE** ;否則 **為 FALSE**。

</dd> <dt>

**IsManaged**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

取得或設定值，這個值會指出集合是否為 managed。 如果集合是受管理的，則為 **TRUE** ;否則 **為 FALSE**。

</dd> <dt>

**IsUserAdmin**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

取得或設定值，指出使用者是否為 VM 上的系統管理員。 如果使用者是 VM 上的系統管理員，則為 **TRUE** ;否則 **為 FALSE**。

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

取得或設定集合的名稱。

</dd> <dt>

**RollbackEnabled**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

取得或設定值，這個值會指出 VM 是否以 VM 快照集進行匯總。 如果 VM 是以 VM 快照集進行匯總，則為 **TRUE** ;否則 **為 FALSE**。

</dd> <dt>

**SecurityDescriptor**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**選擇性**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

取得或設定控制對集合之存取的 SSDL 格式化安全描述項。

</dd> <dt>

**ShowInPortal**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

取得或設定值，指出集合是否顯示在終端機服務中 Web 存取 (TS Web 存取) 。 **TRUE** 表示在 TS Web 存取中顯示集合;否則 **為 FALSE**。

</dd> <dt>

**類型**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

取得或設定值，這個值表示集合所裝載的虛擬機器會話類型。

此屬性包含下列其中一個值：

<dt>

<span id="TempVM"></span><span id="tempvm"></span><span id="TEMPVM"></span>

<span id="TempVM"></span><span id="tempvm"></span><span id="TEMPVM"></span>**TempVM** (1) 


</dt> <dd>

暫時的虛擬機器。

</dd> <dt>

<span id="ManualPersonalVM"></span><span id="manualpersonalvm"></span><span id="MANUALPERSONALVM"></span>

<span id="ManualPersonalVM"></span><span id="manualpersonalvm"></span><span id="MANUALPERSONALVM"></span>**ManualPersonalVM** (2) 


</dt> <dd>

手動建立的虛擬機器。

</dd> <dt>

<span id="AutoPersonalVM"></span><span id="autopersonalvm"></span><span id="AUTOPERSONALVM"></span>

<span id="AutoPersonalVM"></span><span id="autopersonalvm"></span><span id="AUTOPERSONALVM"></span>**AutoPersonalVM** (3) 


</dt> <dd>

自動產生的虛擬機器。

</dd> </dl>

</dd> <dt>

**UserVHDSetting**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**選擇性**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

取得或設定集合的使用者資料 VHD 設定。

</dd> <dt>

**VmFarmSettings**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**選擇性**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

取得或設定集合中虛擬機器的桌面設定。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                                   |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                              |
| 命名空間<br/>                | 根 \\ cimv2 \\ rdm<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[遠端桌面管理服務提供者](rdms-api-reference.md)
</dt> </dl>

 

