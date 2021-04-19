---
description: 代表來賓服務介面元件的狀態，它提供了一種機制，可讓您從主機系統上的管理介面與虛擬機器進行互動。
ms.assetid: 9A158B42-052B-42B3-8539-00927056306D
title: Msvm_GuestServiceInterfaceComponent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestServiceInterfaceComponent
- Msvm_GuestServiceInterfaceComponent.Availability
- Msvm_GuestServiceInterfaceComponent.Caption
- Msvm_GuestServiceInterfaceComponent.ConfigManagerErrorCode
- Msvm_GuestServiceInterfaceComponent.ConfigManagerUserConfig
- Msvm_GuestServiceInterfaceComponent.CreationClassName
- Msvm_GuestServiceInterfaceComponent.Description
- Msvm_GuestServiceInterfaceComponent.DeviceID
- Msvm_GuestServiceInterfaceComponent.ErrorCleared
- Msvm_GuestServiceInterfaceComponent.ErrorDescription
- Msvm_GuestServiceInterfaceComponent.InstallDate
- Msvm_GuestServiceInterfaceComponent.LastErrorCode
- Msvm_GuestServiceInterfaceComponent.Name
- Msvm_GuestServiceInterfaceComponent.PNPDeviceID
- Msvm_GuestServiceInterfaceComponent.PowerManagementCapabilities
- Msvm_GuestServiceInterfaceComponent.PowerManagementSupported
- Msvm_GuestServiceInterfaceComponent.Status
- Msvm_GuestServiceInterfaceComponent.StatusInfo
- Msvm_GuestServiceInterfaceComponent.SystemCreationClassName
- Msvm_GuestServiceInterfaceComponent.SystemName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4c55417edeee6d9a9fb15c474ba4ee9ca2dd93f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971440"
---
# <a name="msvm_guestserviceinterfacecomponent-class"></a>Msvm \_ GuestServiceInterfaceComponent 類別

代表來賓服務介面元件的狀態，它提供了一種機制，可讓您從主機系統上的管理介面與虛擬機器進行互動。 此類別衍生自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) 類別。

下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestServiceInterfaceComponent : CIM_LogicalDevice
{
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a>成員

**Msvm \_ GuestServiceInterfaceComponent** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**Msvm \_ GuestServiceInterfaceComponent** 類別具有這些方法。



| 方法                                                                               | 描述                                                                                                                              |
|:-------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [**RequestStateChange**](requeststatechange-msvm-guestserviceinterfacecomponent.md) | 要求 guest 服務介面元件的狀態變更為指定的值。<br/>                           |
| [**重設**](/windows/desktop/CIMWin32Prov/reset-method-in-class-cim-logicaldevice)                        | 要求重設邏輯裝置。 不是由 WMI 所執行。<br/>                                                               |
| [**SetPowerState**](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-logicaldevice)        | 定義邏輯裝置的預期電源狀態，以及何時應將裝置置於該狀態。 不是由 WMI 所執行。<br/> |



 

### <a name="properties"></a>屬性

**Msvm \_ GuestServiceInterfaceComponent** 類別具有這些屬性。

<dl> <dt>

**可用性**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

裝置的可用性和狀態。



| 值                                                                                                                                                                                                                                                                                                              | 意義                                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <dt>**其他**</dt> <dt>1 (0x1)</dt> </dl>                                                                                          |                                                                                                             |
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**未知**</dt>的 <dt>2 (0x2)</dt> </dl>                                                                                  |                                                                                                             |
| <span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span><dl> 執行中 <dt>**/完整電源**</dt> <dt>3 (0x3)</dt> </dl>                                      |                                                                                                             |
| <span id="Warning"></span><span id="warning"></span><span id="WARNING"></span><dl> <dt>**警告**</dt> <dt>4 (0x4)</dt> </dl>                                                                                  |                                                                                                             |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <dt>**在測試**</dt> <dt>5 (0x5)</dt> </dl>                                                                                  |                                                                                                             |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <dt>**不適用**</dt> <dt>6 (0x6)</dt> </dl>                                                      |                                                                                                             |
| <span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span><dl> <dt>**關閉**</dt> <dt>7 (0x7)</dt> </dl>                                                                          |                                                                                                             |
| <span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span><dl> <dt>**Off 行**</dt> <dt>8 (0x8)</dt> </dl>                                                                              |                                                                                                             |
| <span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span><dl> <dt>**Off**</dt> <dt> (0x9)</dt> </dl>                                                                              |                                                                                                             |
| <span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dl> 已 <dt>**降級**</dt> <dt>10 (0xA)</dt> </dl>                                                                             |                                                                                                             |
| <span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span><dl> <dt>**未安裝**</dt> <dt>11 (0xB)</dt> </dl>                                                         |                                                                                                             |
| <span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span><dl> <dt>**安裝錯誤**</dt> <dt>12 (0xC)</dt> </dl>                                                         |                                                                                                             |
| <span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span><dl> <dt>**省電-未知的**</dt> <dt>13 (0xD)</dt> </dl>                             | 裝置已知處於省電模式，但其確切狀態不明。<br/>                 |
| <span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span><dl> 省 <dt>**電-低電源模式**</dt> <dt>14 (0xE)</dt> </dl> | 裝置處於省電狀態，但仍在運作中，而且可能會出現效能降低的情況。<br/> |
| <span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span><dl> 省 <dt>**電-待命**</dt> <dt>15 (0xF)</dt> </dl>                             | 裝置無法正常運作，但可快速進入完整電源。<br/>                        |
| <span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span><dl> <dt>**電源週期**</dt> <dt>16 (0x10)</dt> </dl>                                                                |                                                                                                             |
| <span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span><dl> 省 <dt>**電-警告**</dt> <dt>17 (0x11)</dt> </dl>                            | 裝置處於警告狀態，但也處於省電模式。<br/>                              |



 

</dd> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的簡短文字描述。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

</dd> <dt>

**ConfigManagerErrorCode**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

Win32 設定管理員錯誤碼。



| 值                                                                                | 意義                                                                                                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0 (0x0) </dt> </dl>   | 裝置運作正常。<br/>                                                                                                   |
| <dl> <dt>1 (0x1) </dt> </dl>   | 裝置未正確設定。<br/>                                                                                           |
| <dl> <dt>2 (0x2) </dt> </dl>   | Windows 無法載入此裝置的驅動程式。<br/>                                                                               |
| <dl> <dt>3 (0x3) </dt> </dl>   | 此裝置的驅動程式可能已損毀，或系統的記憶體或其他資源可能不足。<br/>                             |
| <dl> <dt>4 (0x4) </dt> </dl>   | 裝置無法正常運作。 其中一個驅動程式或登錄可能已損毀。<br/>                                        |
| <dl> <dt>5 (0x5) </dt> </dl>   | 裝置的驅動程式需要 Windows 無法管理的資源。<br/>                                                         |
| <dl> <dt>6 (0x6) </dt> </dl>   | 裝置的開機設定與其他裝置發生衝突。<br/>                                                               |
| <dl> <dt>7 (0x7) </dt> </dl>   | 無法篩選。<br/>                                                                                                                |
| <dl> <dt>8 (0x8) </dt> </dl>   | 遺漏裝置的驅動程式載入器。<br/>                                                                                      |
| <dl> <dt>9 (0x9) </dt> </dl>   | 裝置無法正常運作;控制的固件未正確報告裝置的資源。<br/>               |
| <dl> <dt>10 (0xA) </dt> </dl>  | 裝置無法啟動。<br/>                                                                                                          |
| <dl> <dt>11 (0xB) </dt> </dl>  | 裝置失敗。<br/>                                                                                                                |
| <dl> <dt>12 (0xC) </dt> </dl>  | 裝置找不到足夠的可用資源。<br/>                                                                              |
| <dl> <dt>13 (0xD) </dt> </dl>  | Windows 無法驗證裝置的資源。<br/>                                                                                 |
| <dl> <dt>14 (0xE) </dt> </dl>  | 裝置在重新開機電腦之前無法正常運作。<br/>                                                                  |
| <dl> <dt>15 (0xF) </dt> </dl>  | 裝置因可能的重新列舉問題而無法正常運作。<br/>                                                      |
| <dl> <dt>16 (0x10) </dt> </dl> | Windows 無法識別裝置使用的所有資源。<br/>                                                            |
| <dl> <dt>17 (0x11) </dt> </dl> | 裝置正在要求未知的資源類型。<br/>                                                                                |
| <dl> <dt>18 (0x12) </dt> </dl> | 必須重新安裝設備磁碟機。<br/>                                                                                           |
| <dl> <dt>19 (0x13) </dt> </dl> | 使用 VxD 載入器失敗。<br/>                                                                                                 |
| <dl> <dt>20 (0x14) </dt> </dl> | 登錄可能已損毀。<br/>                                                                                                  |
| <dl> <dt>21 (0x15) </dt> </dl> | 系統失敗。 如果變更設備磁碟機是不正確，請參閱硬體檔。 Windows 正在移除裝置。<br/> |
| <dl> <dt>22 (0x16) </dt> </dl> | 裝置已停用。<br/>                                                                                                           |
| <dl> <dt>23 (0x17) </dt> </dl> | 系統失敗。 如果變更設備磁碟機是不正確，請參閱硬體檔。<br/>                                 |
| <dl> <dt>24 (0x18) </dt> </dl> | 裝置不存在、無法正常運作，或未安裝所有的驅動程式。<br/>                                   |
| <dl> <dt>25 (0x19) </dt> </dl> | Windows 仍在設定裝置。<br/>                                                                                       |
| <dl> <dt>26 (0x1A) </dt> </dl> | Windows 仍在設定裝置。<br/>                                                                                       |
| <dl> <dt>27 (0x1B) </dt> </dl> | 裝置沒有有效的記錄檔設定。<br/>                                                                                 |
| <dl> <dt>28 (0x1C) </dt> </dl> | 未安裝設備磁碟機。<br/>                                                                                             |
| <dl> <dt>29 (Bugcheck 0x1d) </dt> </dl> | 裝置已停用;裝置固件未提供所需的資源。<br/>                                               |
| <dl> <dt>30 (0x1E) </dt> </dl> | 裝置正在使用其他裝置正在使用的 IRQ 資源。<br/>                                                                 |
| <dl> <dt>31 (0x1F) </dt> </dl> | 裝置無法正常運作;Windows 無法載入所需的設備磁碟機。<br/>                                              |



 

</dd> <dt>

**ConfigManagerUserConfig**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

若 **為 TRUE**，則裝置會使用使用者定義的設定。

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

建立實例時所使用之類別或子類別的名稱。 搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的文字描述。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

</dd> <dt>

**DeviceID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

用來唯一命名邏輯裝置的位址或其他識別資訊。

</dd> <dt>

**ErrorCleared**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

若 **為 TRUE**，則表示 **LastErrorCode** 屬性中報告的錯誤現在已清除。

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

自由格式的字串，提供 **LastErrorCode** 屬性中所記錄之錯誤的相關資訊，以及要執行的更正動作。

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的安裝日期和時間。 這個屬性不需要值來表示已安裝物件。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

</dd> <dt>

**LastErrorCode**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

邏輯裝置所報告的最後一個錯誤碼。

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

已知物件的標籤。 子類別化時，可以將這個屬性覆寫為索引鍵屬性。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

</dd> <dt>

**PNPDeviceID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出邏輯裝置的 Win32 隨插即用裝置識別碼。

範例： " \* PNP030b"

</dd> <dt>

**PowerManagementCapabilities**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

邏輯裝置的特定電源相關功能陣列。 這個屬性繼承自 **CIM \_ LogicalDevice**。



| 值                                                                                                                                                                                                                                                                                                                                                                 | 意義                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**未知**</dt>的 <dt>0 (0x0)</dt> </dl>                                                                                                                                     |                                                                                                                                                                                                                                                                                                                                      |
| <span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span><dl> <dt>**不支援**</dt> <dt>1 (0x1)</dt> </dl>                                                                                                             |                                                                                                                                                                                                                                                                                                                                      |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <dt>**停用**</dt> <dt>2 (0x2)</dt> </dl>                                                                                                                                 |                                                                                                                                                                                                                                                                                                                                      |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <dt>**已啟用**</dt> <dt>3 (0x3)</dt> </dl>                                                                                                                                     | 電源管理功能目前已啟用，但實際的功能組不明，或資訊無法使用。<br/>                                                                                                                                                                                               |
| <span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span><dl> <dt>**自動輸入**</dt> <dt>4 (0X4</dt>的省電模式)  </dl> | 裝置可以根據使用方式或其他準則來變更其電源狀態。<br/>                                                                                                                                                                                                                                                   |
| <span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span><dl> <dt>**電源狀態可設定**</dt> <dt>5 (0x5)</dt> </dl>                                                                                 | 支援 [**SetPowerState**](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-controller) 方法。 這個方法可在父 **CIM \_ LogicalDevice** 類別上找到，並且可以實作為。 如需詳細資訊，請參閱 [設計受控物件格式 (MOF) 類別](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes)。<br/> |
| <span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span><dl> <dt>**電源迴圈支援**</dt> <dt>6 (0x6)</dt> </dl>                                                                     | 您可以叫用 [**SetPowerState**](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-controller) 方法，並將 *>powerstate* 參數設定為 5 ( 「電源週期」 ) 。<br/>                                                                                                                                                            |
| <span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span><dl> <dt>**支援的**</dt> <dt>7 (0X7)</dt>的計時電源 </dl>                                                                 | 您可以叫用 [**SetPowerState**](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-controller) 方法，並將 *>powerstate* 參數設定為 5 ( 「電源週期」 ) ，並將 *時間* 設定為特定日期和時間（或時間間隔），以進行電源開啟。<br/>                                                                                       |



 

</dd> <dt>

**PowerManagementSupported**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

若 **為 TRUE**，則裝置可以受電源管理，也就是進入省電狀態。 如果 **為 FALSE**，則整數值 1 ( 「不支援」 ) 應該是 **PowerManagementCapabilities** 陣列中的唯一專案。

這個屬性不會指出電源管理功能目前是否已啟用，或啟用時支援哪些功能。 如需詳細資訊，請參閱 **PowerManagementCapabilities** 陣列。

</dd> <dt>

**狀態**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的目前狀態。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

包括下列值：

<dl><span id="OK"></span><span id="ok"></span><dt>

**正常**
</dt><span id="Error"></span><span id="error"></span><span id="ERROR"></span><dt>

**錯誤**
</dt><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dt>

**降級**
</dt><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dt>

**不明**
</dt><span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span><dt>

**「Pred 失敗」**
</dt><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dt>

**入門**
</dt><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span><dt>

**從而**
</dt><span id="Service"></span><span id="service"></span><span id="SERVICE"></span><dt>

**維護**
</dt><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span><dt>

**強調**
</dt><span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span><dt>

**"NonRecover"**
</dt><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span><dt>

**「無連絡人」**
</dt><span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span><dt>

**「遺失通訊」**
</dt> </dl>

</dd> <dt>

**StatusInfo**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

邏輯裝置的狀態。 如果此屬性不適用於邏輯裝置，則應該使用值 5 ( 「不適用」 ) 。 這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。

<dl> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1 (0x1) ) 
</dt> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2 (0x2) ) 
</dt> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (3 (0x3) ) 
</dt> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**停用** (4 (0x4) ) 
</dt> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (5 (0x5) ) 
</dt> </dl>

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

設定系統建立類別名稱的範圍。

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

設定系統名稱的範圍。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8.1 桌面應用程式\]<br/>                                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 R2 \[ desktop 應用程式\]<br/>                                                 |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ LogicalDevice**](cim-logicaldevice.md)
</dt> <dt>

[**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)
</dt> </dl>

 

