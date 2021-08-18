---
description: 代表綜合滑鼠裝置。
ms.assetid: c04b7aa1-44fe-41f5-943f-ff49ce64be96
title: Msvm_SyntheticMouse 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticMouse
- Msvm_SyntheticMouse.SetPowerState
- Msvm_SyntheticMouse.EnableDevice
- Msvm_SyntheticMouse.OnlineDevice
- Msvm_SyntheticMouse.QuiesceDevice
- Msvm_SyntheticMouse.SaveProperties
- Msvm_SyntheticMouse.RestoreProperties
- Msvm_SyntheticMouse.InstanceID
- Msvm_SyntheticMouse.Caption
- Msvm_SyntheticMouse.Description
- Msvm_SyntheticMouse.ElementName
- Msvm_SyntheticMouse.InstallDate
- Msvm_SyntheticMouse.Name
- Msvm_SyntheticMouse.OperationalStatus
- Msvm_SyntheticMouse.StatusDescriptions
- Msvm_SyntheticMouse.Status
- Msvm_SyntheticMouse.HealthState
- Msvm_SyntheticMouse.CommunicationStatus
- Msvm_SyntheticMouse.DetailedStatus
- Msvm_SyntheticMouse.OperatingStatus
- Msvm_SyntheticMouse.PrimaryStatus
- Msvm_SyntheticMouse.EnabledState
- Msvm_SyntheticMouse.OtherEnabledState
- Msvm_SyntheticMouse.RequestedState
- Msvm_SyntheticMouse.EnabledDefault
- Msvm_SyntheticMouse.TimeOfLastStateChange
- Msvm_SyntheticMouse.AvailableRequestedStates
- Msvm_SyntheticMouse.TransitioningToState
- Msvm_SyntheticMouse.SystemCreationClassName
- Msvm_SyntheticMouse.SystemName
- Msvm_SyntheticMouse.CreationClassName
- Msvm_SyntheticMouse.DeviceID
- Msvm_SyntheticMouse.PowerManagementSupported
- Msvm_SyntheticMouse.PowerManagementCapabilities
- Msvm_SyntheticMouse.Availability
- Msvm_SyntheticMouse.StatusInfo
- Msvm_SyntheticMouse.LastErrorCode
- Msvm_SyntheticMouse.ErrorDescription
- Msvm_SyntheticMouse.ErrorCleared
- Msvm_SyntheticMouse.OtherIdentifyingInfo
- Msvm_SyntheticMouse.PowerOnHours
- Msvm_SyntheticMouse.TotalPowerOnHours
- Msvm_SyntheticMouse.IdentifyingDescriptions
- Msvm_SyntheticMouse.AdditionalAvailability
- Msvm_SyntheticMouse.MaxQuiesceTime
- Msvm_SyntheticMouse.IsLocked
- Msvm_SyntheticMouse.PointingType
- Msvm_SyntheticMouse.NumberOfButtons
- Msvm_SyntheticMouse.Handedness
- Msvm_SyntheticMouse.Resolution
- Msvm_SyntheticMouse.AbsoluteCoordinates
- Msvm_SyntheticMouse.HorizontalPosition
- Msvm_SyntheticMouse.VerticalPosition
- Msvm_SyntheticMouse.ScrollPosition
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 98cad51066f95bf75829cffe4235c243aabb0c3d58a46f8eb3d4ce4db96c10fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148131"
---
# <a name="msvm_syntheticmouse-class"></a>Msvm \_ SyntheticMouse 類別

代表綜合滑鼠裝置。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SyntheticMouse : CIM_PointingDevice
{
  string   InstanceID;
  string   Caption = "Mouse";
  string   Description = "Microsoft Synthetic Mouse";
  string   ElementName = "Mouse";
  datetime InstallDate;
  string   Name = "Mouse";
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = {
                "OK"
              };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_SyntheticMouse";
  string   DeviceID;
  boolean  PowerManagementSupported;
  uint16   PowerManagementCapabilities[];
  uint16   Availability = 6;
  uint16   StatusInfo;
  uint32   LastErrorCode;
  string   ErrorDescription;
  boolean  ErrorCleared;
  string   OtherIdentifyingInfo[];
  uint64   PowerOnHours;
  uint64   TotalPowerOnHours;
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[] = {6};
  uint64   MaxQuiesceTime;
  boolean  IsLocked = False;
  uint16   PointingType = 3;
  uint8    NumberOfButtons = 5;
  uint16   Handedness = 2;
  uint32   Resolution;
  boolean  AbsoluteCoordinates = True;
  sint32   HorizontalPosition;
  sint32   VerticalPosition;
  sint32   ScrollPosition;
};
```

## <a name="members"></a>成員

**Msvm \_ SyntheticMouse** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**Msvm \_ SyntheticMouse** 類別具有這些方法。



| 方法                                                                 | 描述                                                                   |
|:-----------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [**ClickButton**](clickbutton-msvm-syntheticmouse.md)                 | 模擬指定裝置按鈕的按鈕點擊。<br/>           |
| **EnableDevice**                                                       | 不支援這個方法。<br/>                                      |
| [**GetButtonState**](getbuttonstate-msvm-syntheticmouse.md)           | 抓取指定裝置按鈕的目前狀態。<br/>        |
| **OnlineDevice**                                                       | 不支援這個方法。<br/>                                      |
| **QuiesceDevice**                                                      | 不支援這個方法。<br/>                                      |
| [**RequestStateChange**](msvm-syntheticmouse-requeststatechange.md)   | 要求狀態變更<br/>                                            |
| [**重設**](msvm-syntheticmouse-reset.md)                             | 重設裝置。<br/>                                                 |
| **RestoreProperties**                                                  | 不支援這個方法。<br/>                                      |
| **SaveProperties**                                                     | 不支援這個方法。<br/>                                      |
| [**SetAbsolutePosition**](setabsoluteposition-msvm-syntheticmouse.md) | 設定滑鼠游標的水準和垂直位置。<br/>     |
| [**SetButtonState**](setbuttonstate-msvm-syntheticmouse.md)           | 設定指定裝置按鈕的目前狀態。<br/>             |
| **SetPowerState**                                                      | 不支援這個方法。<br/>                                      |
| [**SetScrollPosition**](setscrollposition-msvm-syntheticmouse.md)     | 設定指向指標裝置之滾輪控制項的 z 座標。<br/> |



 

### <a name="properties"></a>屬性

**Msvm \_ SyntheticMouse** 類別具有這些屬性。

<dl> <dt>

**AbsoluteCoordinates**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出裝置是否在絕對或相對座標上運作。



| 值                                                                                | 意義                                           |
|--------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <dt>**是**</dt> </dl>  | 裝置的座標是絕對的。<br/> |
| <dl> <dt>**否**</dt> </dl> | 裝置的座標是相對的。<br/> |



 

</dd> <dt>

**AdditionalAvailability**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

裝置的任何額外可用性和狀態，超出 **可用性** 屬性中指定的範圍。 **Availability** 屬性代表裝置的主要狀態和可用性。 這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。



| 值                                                                          | 意義                   |
|--------------------------------------------------------------------------------|---------------------------|
| <dl> <dt>{6}</dt> </dl> | 不適用<br/> |



 

</dd> <dt>

**可用性**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

裝置的主要可用性和狀態。 這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。



| 值                                                                        | 意義                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <dt>6</dt> </dl> | 不適用<br/> |



 

</dd> <dt>

**AvailableRequestedStates**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出 **RequestStateChange** 方法的 *RequestedState* 參數可能的值。 這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。

</dd> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的簡短描述。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。

</dd> <dt>

**CommunicationStatus**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出檢測與基礎受管理元素通訊的能力。 **Null** 值表示不會執行此屬性。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) 
</dt> <dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**
</dt> <dt>

<span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**通訊正常** (2) 
</dt> <dt>

<span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**遺失通訊** (3) 
</dt> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**沒有連絡人** (4) 
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) 
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。 )
</dt> </dl>

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **MaxLen** (256) 
</dt> </dl>

建立實例時所使用之類別或子類別的名稱。 搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。 這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

對物件的描述。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。

</dd> <dt>

**DetailedStatus**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

補充 **PrimaryStatus** 屬性與其他狀態詳細資料。 **Null** 值表示不會執行此屬性。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

<dl> <dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (0) **無法使用**
</dt> <dt>

<span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**沒有其他資訊** (1) 
</dt> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**壓力** (2) 
</dt> <dt>

<span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**預測性失敗** (3) 
</dt> <dt>

<span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**無法復原的錯誤** (4) 
</dt> <dt>

<span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**錯誤中的支援實體** (5) 
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) 
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。 )
</dt> </dl>

</dd> <dt>

**DeviceID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **MaxLen** (64) 
</dt> </dl>

用來唯一命名邏輯裝置的位址或其他識別資訊。 這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，而且一律設定為 "Microsoft：*GUID*"。

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的顯示名稱。 除了索引鍵屬性、身分識別資料和描述資訊之外，此屬性還可讓每個實例定義顯示名稱。 **CIM \_ ManagedSystemElement** 類別的 [**Name**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)屬性也會定義為顯示名稱。 但是，它通常是一個重要的子類別。 相同的屬性可以同時傳達身分識別和顯示名稱，而不會有不一致的情況。 如果 [**名稱**](msvm-keyboard.md) 存在，而且不是索引鍵 (例如針對 LogicalDevice) 的實例，則 **名稱** 和 **ElementName** 屬性都可以同時存在相同的資訊。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。

</dd> <dt>

**EnabledDefault**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

系統管理員的預設或啟動設定，適用于元素的 **EnabledState** 。 這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

專案的已啟用和停用狀態。 這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。



| 值                                                                                                                                                                                                                           | 意義                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <dt>**已啟用**</dt> <dt>2</dt> </dl>     | 來賓虛擬機器支援綜合滑鼠。<br/>         |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <dt>**停用**</dt> <dt>3</dt> </dl> | 來賓虛擬機器不支援綜合滑鼠。<br/> |



 

</dd> <dt>

**ErrorCleared**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出現在是否已清除 **LastErrorCode** 中報告的錯誤。 這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

字串，提供 **LastErrorCode** 中所記錄錯誤的詳細資訊，以及可採取之任何矯正措施的相關資訊。 這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。

</dd> <dt>

**Handedness**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

適用于右手邊或左邊作業的指標裝置設定。 這個屬性繼承自 [**CIM \_ PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice)。



| 值                                                                        | 意義                            |
|------------------------------------------------------------------------------|------------------------------------|
| <dl> <dt>0</dt> </dl> | Unknown<br/>                 |
| <dl> <dt>1</dt> </dl> | 不適用。<br/>         |
| <dl> <dt>2</dt> </dl> | 右手操作。<br/> |
| <dl> <dt>3</dt> </dl> | 左手操作。<br/>  |



 

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

專案目前的健康情況。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

</dd> <dt>

**HorizontalPosition**
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指標裝置的絕對 x 座標。

</dd> <dt>

**IdentifyingDescriptions**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

自由格式字串的陣列，提供 [**OtherIdentifyingInfo**](msvm-keyboard.md) 陣列中專案背後的說明和詳細資料。 這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

建立虛擬機器的日期和時間。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

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

**IsLocked**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出裝置是否已鎖定，防止使用者輸入或輸出。 這個屬性繼承自 [**CIM \_ UserDevice**](/windows/desktop/CIMWin32Prov/cim-userdevice)。

</dd> <dt>

**LastErrorCode**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

邏輯裝置所報告的最後一個錯誤碼。 這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。

</dd> <dt>

**MaxQuiesceTime**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

這個屬性已被取代。 這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **MaxLen** (1024) 
</dt> </dl>

已知物件的標籤。 子類別化時，可以將這個屬性覆寫為索引鍵屬性。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

</dd> <dt>

**NumberOfButtons**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指標裝置上的按鈕數目。 這個屬性繼承自 [**CIM \_ PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice)。

</dd> <dt>

**OperatingStatus**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

提供專案操作條件的目前狀態資訊，並可用於提供關於 **EnabledState** 屬性值的詳細資料。 **Null** 值表示不會執行此屬性。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) 
</dt> <dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**
</dt> <dt>

<span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**服務** (2) 
</dt> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**開始** (3) 
</dt> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**停止** (4) 
</dt> <dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**已停止** (5) 
</dt> <dt>

<span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>已 **中止** (6) 
</dt> <dt>

<span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**休眠** (7) 
</dt> <dt>

<span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**已完成** (8) 
</dt> <dt>

<span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**遷移** (9) 
</dt> <dt>

<span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10) 
</dt> <dt>

<span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11) 
</dt> <dt>

<span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**快照** (12) 
</dt> <dt>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>正在 **關閉** (13) 
</dt> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (14) 
</dt> <dt>

<span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**轉換** (15) 
</dt> <dt>

<span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**在服務** (16) 
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) 
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。 )
</dt> </dl>

</dd> <dt>

**OperationalStatus**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

專案的目前狀態。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

</dd> <dt>

**OtherEnabledState**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

當 **EnabledState** 屬性設定為 1 (其他) 時，元素的啟用或停用狀態。 當 **EnabledState** 是1以外的任何值時，這個屬性必須設定為 **Null** 。 這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

除了裝置識別碼資訊以外的任何其他資料，可用來識別邏輯裝置。 這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。

</dd> <dt>

**PointingType**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指標裝置的類型。 這個屬性繼承自 [**CIM \_ PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice)。



| 值                                                                        | 意義          |
|------------------------------------------------------------------------------|------------------|
| <dl> <dt>3</dt> </dl> | 滑鼠<br/> |



 

</dd> <dt>

**PowerManagementCapabilities**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

裝置的電源管理功能。 這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。

</dd> <dt>

**PowerManagementSupported**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出裝置是否可以受電源管理。 這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。

</dd> <dt>

**PowerOnHours**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

此裝置自上一次電源週期起開啟電源的連續小時數。 這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。

</dd> <dt>

**PrimaryStatus**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

提供高層級的狀態資訊。 這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態。 **Null** 值表示不會執行此屬性。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) 
</dt> <dt>

<span id="OK"></span><span id="ok"></span>**確定** (1) 
</dt> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (2) **降級**
</dt> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>**錯誤** (3) 
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) 
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。 )
</dt> </dl>

</dd> <dt>

**RequestedState**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

上次要求或預期的專案狀態。 這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。



| 值                                                                         | 意義                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <dt>12</dt> </dl> | 不適用<br/> |



 

</dd> <dt>

**解決方法**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指標裝置的追蹤解析度（以每英寸計數計算）。 這個屬性繼承自 [**CIM \_ PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice)。

</dd> <dt>

**ScrollPosition**
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Mickeys" ) 
</dt> </dl>

滑鼠裝置的 z 座標位置。

</dd> <dt>

**狀態**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的目前狀態。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，但不會使用它。

</dd> <dt>

**StatusDescriptions**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

描述各種 [**OperationalStatus**](msvm-bioselement.md) 陣列值的字串。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

</dd> <dt>

**StatusInfo**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

邏輯裝置的目前狀態。 這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **MaxLen** (256) 
</dt> </dl>

範圍系統的建立類別名稱。 這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **MaxLen** (256) 
</dt> </dl>

範圍系統的名稱。 此值會對應至範圍虛擬機器之 Msvm 的非程式類型類別的 [**名稱**](msvm-computersystem.md)屬性值。 **\_** 這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。

</dd> <dt>

**TimeOfLastStateChange**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

專案的已啟用狀態上次變更的日期或時間。 如果未變更元素的狀態，且已填入此屬性，則必須將它設定為0間隔值。 如果已要求狀態變更，但遭到拒絕或尚未處理，則必須更新屬性。 這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。

</dd> <dt>

**TotalPowerOnHours**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

此裝置已獲得電源的總時數。 這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。

</dd> <dt>

**TransitioningToState**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出實例正在轉換的目標狀態。 這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。

</dd> <dt>

**VerticalPosition**
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指標裝置的絕對 y 座標。

</dd> </dl>

## <a name="remarks"></a>備註

存取 **Msvm \_ SyntheticMouse** 類別可能受 UAC 篩選所限制。 如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。

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

[**CIM \_ PointingDevice**](cim-pointingdevice.md)
</dt> <dt>

[**CIM \_ PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice)
</dt> <dt>

[輸入類別](input-classes.md)
</dt> </dl>

 

