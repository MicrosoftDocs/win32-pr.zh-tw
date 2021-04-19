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
# <a name="msvm_guestserviceinterfacecomponent-class"></a><span data-ttu-id="b17a8-103">Msvm \_ GuestServiceInterfaceComponent 類別</span><span class="sxs-lookup"><span data-stu-id="b17a8-103">Msvm\_GuestServiceInterfaceComponent class</span></span>

<span data-ttu-id="b17a8-104">代表來賓服務介面元件的狀態，它提供了一種機制，可讓您從主機系統上的管理介面與虛擬機器進行互動。</span><span class="sxs-lookup"><span data-stu-id="b17a8-104">Represents the state of the guest service interface component, which provides a mechanism to interact with the virtual machine from the management interfaces on the host system.</span></span> <span data-ttu-id="b17a8-105">此類別衍生自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) 類別。</span><span class="sxs-lookup"><span data-stu-id="b17a8-105">This class derives from the [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) class.</span></span>

<span data-ttu-id="b17a8-106">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="b17a8-106">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b17a8-107">語法</span><span class="sxs-lookup"><span data-stu-id="b17a8-107">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="b17a8-108">成員</span><span class="sxs-lookup"><span data-stu-id="b17a8-108">Members</span></span>

<span data-ttu-id="b17a8-109">**Msvm \_ GuestServiceInterfaceComponent** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b17a8-109">The **Msvm\_GuestServiceInterfaceComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="b17a8-110">方法</span><span class="sxs-lookup"><span data-stu-id="b17a8-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="b17a8-111">屬性</span><span class="sxs-lookup"><span data-stu-id="b17a8-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b17a8-112">方法</span><span class="sxs-lookup"><span data-stu-id="b17a8-112">Methods</span></span>

<span data-ttu-id="b17a8-113">**Msvm \_ GuestServiceInterfaceComponent** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="b17a8-113">The **Msvm\_GuestServiceInterfaceComponent** class has these methods.</span></span>



| <span data-ttu-id="b17a8-114">方法</span><span class="sxs-lookup"><span data-stu-id="b17a8-114">Method</span></span>                                                                               | <span data-ttu-id="b17a8-115">描述</span><span class="sxs-lookup"><span data-stu-id="b17a8-115">Description</span></span>                                                                                                                              |
|:-------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b17a8-116">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="b17a8-116">**RequestStateChange**</span></span>](requeststatechange-msvm-guestserviceinterfacecomponent.md) | <span data-ttu-id="b17a8-117">要求 guest 服務介面元件的狀態變更為指定的值。</span><span class="sxs-lookup"><span data-stu-id="b17a8-117">Requests that the state of the guest service interface component be changed to the specified value.</span></span><br/>                           |
| [<span data-ttu-id="b17a8-118">**重設**</span><span class="sxs-lookup"><span data-stu-id="b17a8-118">**Reset**</span></span>](/windows/desktop/CIMWin32Prov/reset-method-in-class-cim-logicaldevice)                        | <span data-ttu-id="b17a8-119">要求重設邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="b17a8-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="b17a8-120">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="b17a8-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="b17a8-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="b17a8-121">**SetPowerState**</span></span>](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-logicaldevice)        | <span data-ttu-id="b17a8-122">定義邏輯裝置的預期電源狀態，以及何時應將裝置置於該狀態。</span><span class="sxs-lookup"><span data-stu-id="b17a8-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="b17a8-123">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="b17a8-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="b17a8-124">屬性</span><span class="sxs-lookup"><span data-stu-id="b17a8-124">Properties</span></span>

<span data-ttu-id="b17a8-125">**Msvm \_ GuestServiceInterfaceComponent** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="b17a8-125">The **Msvm\_GuestServiceInterfaceComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b17a8-126">**可用性**</span><span class="sxs-lookup"><span data-stu-id="b17a8-126">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b17a8-127">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="b17a8-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b17a8-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b17a8-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b17a8-129">裝置的可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="b17a8-129">Availability and status of the device.</span></span>



| <span data-ttu-id="b17a8-130">值</span><span class="sxs-lookup"><span data-stu-id="b17a8-130">Value</span></span>                                                                                                                                                                                                                                                                                                              | <span data-ttu-id="b17a8-131">意義</span><span class="sxs-lookup"><span data-stu-id="b17a8-131">Meaning</span></span>                                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="b17a8-132"><dt>**其他**</dt> <dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="b17a8-132"><dt>**Other**</dt> <dt>1 (0x1)</dt></span></span> </dl>                                                                                          |                                                                                                             |
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="b17a8-133"><dt>**未知**</dt>的 <dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="b17a8-133"><dt>**Unknown**</dt> <dt>2 (0x2)</dt></span></span> </dl>                                                                                  |                                                                                                             |
| <span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span><dl> <span data-ttu-id="b17a8-134">執行中 <dt>**/完整電源**</dt> <dt>3 (0x3)</dt></span><span class="sxs-lookup"><span data-stu-id="b17a8-134"><dt>**Running/Full Power**</dt> <dt>3 (0x3)</dt></span></span> </dl>                                      |                                                                                                             |
| <span id="Warning"></span><span id="warning"></span><span id="WARNING"></span><dl> <span data-ttu-id="b17a8-135"><dt>**警告**</dt> <dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="b17a8-135"><dt>**Warning**</dt> <dt>4 (0x4)</dt></span></span> </dl>                                                                                  |                                                                                                             |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="b17a8-136"><dt>**在測試**</dt> <dt>5 (0x5)</dt></span><span class="sxs-lookup"><span data-stu-id="b17a8-136"><dt>**In Test**</dt> <dt>5 (0x5)</dt></span></span> </dl>                                                                                  |                                                                                                             |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="b17a8-137"><dt>**不適用**</dt> <dt>6 (0x6)</dt></span><span class="sxs-lookup"><span data-stu-id="b17a8-137"><dt>**Not Applicable**</dt> <dt>6 (0x6)</dt></span></span> </dl>                                                      |                                                                                                             |
| <span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span><dl> <span data-ttu-id="b17a8-138"><dt>**關閉**</dt> <dt>7 (0x7)</dt></span><span class="sxs-lookup"><span data-stu-id="b17a8-138"><dt>**Power Off**</dt> <dt>7 (0x7)</dt></span></span> </dl>                                                                          |                                                                                                             |
| <span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span><dl> <span data-ttu-id="b17a8-139"><dt>**Off 行**</dt> <dt>8 (0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="b17a8-139"><dt>**Off Line**</dt> <dt>8 (0x8)</dt></span></span> </dl>                                                                              |                                                                                                             |
| <span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span><dl> <span data-ttu-id="b17a8-140"><dt>**Off**</dt> <dt> (0x9)</dt></span><span class="sxs-lookup"><span data-stu-id="b17a8-140"><dt>**Off Duty**</dt> <dt>9 (0x9)</dt></span></span> </dl>                                                                              |                                                                                                             |
| <span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dl> <span data-ttu-id="b17a8-141">已 <dt>**降級**</dt> <dt>10 (0xA)</dt></span><span class="sxs-lookup"><span data-stu-id="b17a8-141"><dt>**Degraded**</dt> <dt>10 (0xA)</dt></span></span> </dl>                                                                             |                                                                                                             |
| <span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span><dl> <span data-ttu-id="b17a8-142"><dt>**未安裝**</dt> <dt>11 (0xB)</dt></span><span class="sxs-lookup"><span data-stu-id="b17a8-142"><dt>**Not Installed**</dt> <dt>11 (0xB)</dt></span></span> </dl>                                                         |                                                                                                             |
| <span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span><dl> <span data-ttu-id="b17a8-143"><dt>**安裝錯誤**</dt> <dt>12 (0xC)</dt></span><span class="sxs-lookup"><span data-stu-id="b17a8-143"><dt>**Install Error**</dt> <dt>12 (0xC)</dt></span></span> </dl>                                                         |                                                                                                             |
| <span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span><dl> <span data-ttu-id="b17a8-144"><dt>**省電-未知的**</dt> <dt>13 (0xD)</dt></span><span class="sxs-lookup"><span data-stu-id="b17a8-144"><dt>**Power Save - Unknown**</dt> <dt>13 (0xD)</dt></span></span> </dl>                             | <span data-ttu-id="b17a8-145">裝置已知處於省電模式，但其確切狀態不明。</span><span class="sxs-lookup"><span data-stu-id="b17a8-145">The device is known to be in a power save mode, but its exact status is unknown.</span></span><br/>                 |
| <span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span><dl> <span data-ttu-id="b17a8-146">省 <dt>**電-低電源模式**</dt> <dt>14 (0xE)</dt></span><span class="sxs-lookup"><span data-stu-id="b17a8-146"><dt>**Power Save - Low Power Mode**</dt> <dt>14 (0xE)</dt></span></span> </dl> | <span data-ttu-id="b17a8-147">裝置處於省電狀態，但仍在運作中，而且可能會出現效能降低的情況。</span><span class="sxs-lookup"><span data-stu-id="b17a8-147">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span><br/> |
| <span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span><dl> <span data-ttu-id="b17a8-148">省 <dt>**電-待命**</dt> <dt>15 (0xF)</dt></span><span class="sxs-lookup"><span data-stu-id="b17a8-148"><dt>**Power Save - Standby**</dt> <dt>15 (0xF)</dt></span></span> </dl>                             | <span data-ttu-id="b17a8-149">裝置無法正常運作，但可快速進入完整電源。</span><span class="sxs-lookup"><span data-stu-id="b17a8-149">The device is not functioning but could be brought to full power quickly.</span></span><br/>                        |
| <span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span><dl> <span data-ttu-id="b17a8-150"><dt>**電源週期**</dt> <dt>16 (0x10)</dt></span><span class="sxs-lookup"><span data-stu-id="b17a8-150"><dt>**Power Cycle**</dt> <dt>16 (0x10)</dt></span></span> </dl>                                                                |                                                                                                             |
| <span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span><dl> <span data-ttu-id="b17a8-151">省 <dt>**電-警告**</dt> <dt>17 (0x11)</dt></span><span class="sxs-lookup"><span data-stu-id="b17a8-151"><dt>**Power Save - Warning**</dt> <dt>17 (0x11)</dt></span></span> </dl>                            | <span data-ttu-id="b17a8-152">裝置處於警告狀態，但也處於省電模式。</span><span class="sxs-lookup"><span data-stu-id="b17a8-152">The device is in a warning state, though also in a power save mode.</span></span><br/>                              |



 

</dd> <dt>

<span data-ttu-id="b17a8-153">**標題**</span><span class="sxs-lookup"><span data-stu-id="b17a8-153">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b17a8-154">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b17a8-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b17a8-155">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b17a8-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b17a8-156">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="b17a8-156">Short textual description of the object.</span></span> <span data-ttu-id="b17a8-157">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="b17a8-157">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="b17a8-158">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="b17a8-158">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b17a8-159">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="b17a8-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b17a8-160">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b17a8-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b17a8-161">Win32 設定管理員錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b17a8-161">Win32 Configuration Manager error code.</span></span>



| <span data-ttu-id="b17a8-162">值</span><span class="sxs-lookup"><span data-stu-id="b17a8-162">Value</span></span>                                                                                | <span data-ttu-id="b17a8-163">意義</span><span class="sxs-lookup"><span data-stu-id="b17a8-163">Meaning</span></span>                                                                                                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b17a8-164"><dt>0 (0x0) </dt></span><span class="sxs-lookup"><span data-stu-id="b17a8-164"><dt>0 (0x0)</dt></span></span> </dl>   | <span data-ttu-id="b17a8-165">裝置運作正常。</span><span class="sxs-lookup"><span data-stu-id="b17a8-165">Device is working properly.</span></span><br/>                                                                                                   |
| <dl> <span data-ttu-id="b17a8-166"><dt>1 (0x1) </dt></span><span class="sxs-lookup"><span data-stu-id="b17a8-166"><dt>1 (0x1)</dt></span></span> </dl>   | <span data-ttu-id="b17a8-167">裝置未正確設定。</span><span class="sxs-lookup"><span data-stu-id="b17a8-167">Device is not configured correctly.</span></span><br/>                                                                                           |
| <dl> <span data-ttu-id="b17a8-168"><dt>2 (0x2) </dt></span><span class="sxs-lookup"><span data-stu-id="b17a8-168"><dt>2 (0x2)</dt></span></span> </dl>   | <span data-ttu-id="b17a8-169">Windows 無法載入此裝置的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="b17a8-169">Windows cannot load the driver for this device.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="b17a8-170"><dt>3 (0x3) </dt></span><span class="sxs-lookup"><span data-stu-id="b17a8-170"><dt>3 (0x3)</dt></span></span> </dl>   | <span data-ttu-id="b17a8-171">此裝置的驅動程式可能已損毀，或系統的記憶體或其他資源可能不足。</span><span class="sxs-lookup"><span data-stu-id="b17a8-171">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span><br/>                             |
| <dl> <span data-ttu-id="b17a8-172"><dt>4 (0x4) </dt></span><span class="sxs-lookup"><span data-stu-id="b17a8-172"><dt>4 (0x4)</dt></span></span> </dl>   | <span data-ttu-id="b17a8-173">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="b17a8-173">Device is not working properly.</span></span> <span data-ttu-id="b17a8-174">其中一個驅動程式或登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="b17a8-174">One of its drivers or the registry might be corrupted.</span></span><br/>                                        |
| <dl> <span data-ttu-id="b17a8-175"><dt>5 (0x5) </dt></span><span class="sxs-lookup"><span data-stu-id="b17a8-175"><dt>5 (0x5)</dt></span></span> </dl>   | <span data-ttu-id="b17a8-176">裝置的驅動程式需要 Windows 無法管理的資源。</span><span class="sxs-lookup"><span data-stu-id="b17a8-176">Driver for the device requires a resource that Windows cannot manage.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="b17a8-177"><dt>6 (0x6) </dt></span><span class="sxs-lookup"><span data-stu-id="b17a8-177"><dt>6 (0x6)</dt></span></span> </dl>   | <span data-ttu-id="b17a8-178">裝置的開機設定與其他裝置發生衝突。</span><span class="sxs-lookup"><span data-stu-id="b17a8-178">Boot configuration for the device conflicts with other devices.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="b17a8-179"><dt>7 (0x7) </dt></span><span class="sxs-lookup"><span data-stu-id="b17a8-179"><dt>7 (0x7)</dt></span></span> </dl>   | <span data-ttu-id="b17a8-180">無法篩選。</span><span class="sxs-lookup"><span data-stu-id="b17a8-180">Cannot filter.</span></span><br/>                                                                                                                |
| <dl> <span data-ttu-id="b17a8-181"><dt>8 (0x8) </dt></span><span class="sxs-lookup"><span data-stu-id="b17a8-181"><dt>8 (0x8)</dt></span></span> </dl>   | <span data-ttu-id="b17a8-182">遺漏裝置的驅動程式載入器。</span><span class="sxs-lookup"><span data-stu-id="b17a8-182">Driver loader for the device is missing.</span></span><br/>                                                                                      |
| <dl> <span data-ttu-id="b17a8-183"><dt>9 (0x9) </dt></span><span class="sxs-lookup"><span data-stu-id="b17a8-183"><dt>9 (0x9)</dt></span></span> </dl>   | <span data-ttu-id="b17a8-184">裝置無法正常運作;控制的固件未正確報告裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="b17a8-184">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span><br/>               |
| <dl> <span data-ttu-id="b17a8-185"><dt>10 (0xA) </dt></span><span class="sxs-lookup"><span data-stu-id="b17a8-185"><dt>10 (0xA)</dt></span></span> </dl>  | <span data-ttu-id="b17a8-186">裝置無法啟動。</span><span class="sxs-lookup"><span data-stu-id="b17a8-186">Device cannot start.</span></span><br/>                                                                                                          |
| <dl> <span data-ttu-id="b17a8-187"><dt>11 (0xB) </dt></span><span class="sxs-lookup"><span data-stu-id="b17a8-187"><dt>11 (0xB)</dt></span></span> </dl>  | <span data-ttu-id="b17a8-188">裝置失敗。</span><span class="sxs-lookup"><span data-stu-id="b17a8-188">Device failed.</span></span><br/>                                                                                                                |
| <dl> <span data-ttu-id="b17a8-189"><dt>12 (0xC) </dt></span><span class="sxs-lookup"><span data-stu-id="b17a8-189"><dt>12 (0xC)</dt></span></span> </dl>  | <span data-ttu-id="b17a8-190">裝置找不到足夠的可用資源。</span><span class="sxs-lookup"><span data-stu-id="b17a8-190">Device cannot find enough free resources to use.</span></span><br/>                                                                              |
| <dl> <span data-ttu-id="b17a8-191"><dt>13 (0xD) </dt></span><span class="sxs-lookup"><span data-stu-id="b17a8-191"><dt>13 (0xD)</dt></span></span> </dl>  | <span data-ttu-id="b17a8-192">Windows 無法驗證裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="b17a8-192">Windows cannot verify the device's resources.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="b17a8-193"><dt>14 (0xE) </dt></span><span class="sxs-lookup"><span data-stu-id="b17a8-193"><dt>14 (0xE)</dt></span></span> </dl>  | <span data-ttu-id="b17a8-194">裝置在重新開機電腦之前無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="b17a8-194">Device cannot work properly until the computer is restarted.</span></span><br/>                                                                  |
| <dl> <span data-ttu-id="b17a8-195"><dt>15 (0xF) </dt></span><span class="sxs-lookup"><span data-stu-id="b17a8-195"><dt>15 (0xF)</dt></span></span> </dl>  | <span data-ttu-id="b17a8-196">裝置因可能的重新列舉問題而無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="b17a8-196">Device is not working properly due to a possible re-enumeration problem.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="b17a8-197"><dt>16 (0x10) </dt></span><span class="sxs-lookup"><span data-stu-id="b17a8-197"><dt>16 (0x10)</dt></span></span> </dl> | <span data-ttu-id="b17a8-198">Windows 無法識別裝置使用的所有資源。</span><span class="sxs-lookup"><span data-stu-id="b17a8-198">Windows cannot identify all of the resources that the device uses.</span></span><br/>                                                            |
| <dl> <span data-ttu-id="b17a8-199"><dt>17 (0x11) </dt></span><span class="sxs-lookup"><span data-stu-id="b17a8-199"><dt>17 (0x11)</dt></span></span> </dl> | <span data-ttu-id="b17a8-200">裝置正在要求未知的資源類型。</span><span class="sxs-lookup"><span data-stu-id="b17a8-200">Device is requesting an unknown resource type.</span></span><br/>                                                                                |
| <dl> <span data-ttu-id="b17a8-201"><dt>18 (0x12) </dt></span><span class="sxs-lookup"><span data-stu-id="b17a8-201"><dt>18 (0x12)</dt></span></span> </dl> | <span data-ttu-id="b17a8-202">必須重新安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="b17a8-202">Device drivers must be reinstalled.</span></span><br/>                                                                                           |
| <dl> <span data-ttu-id="b17a8-203"><dt>19 (0x13) </dt></span><span class="sxs-lookup"><span data-stu-id="b17a8-203"><dt>19 (0x13)</dt></span></span> </dl> | <span data-ttu-id="b17a8-204">使用 VxD 載入器失敗。</span><span class="sxs-lookup"><span data-stu-id="b17a8-204">Failure using the VxD loader.</span></span><br/>                                                                                                 |
| <dl> <span data-ttu-id="b17a8-205"><dt>20 (0x14) </dt></span><span class="sxs-lookup"><span data-stu-id="b17a8-205"><dt>20 (0x14)</dt></span></span> </dl> | <span data-ttu-id="b17a8-206">登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="b17a8-206">Registry might be corrupted.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="b17a8-207"><dt>21 (0x15) </dt></span><span class="sxs-lookup"><span data-stu-id="b17a8-207"><dt>21 (0x15)</dt></span></span> </dl> | <span data-ttu-id="b17a8-208">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="b17a8-208">System failure.</span></span> <span data-ttu-id="b17a8-209">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="b17a8-209">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="b17a8-210">Windows 正在移除裝置。</span><span class="sxs-lookup"><span data-stu-id="b17a8-210">Windows is removing the device.</span></span><br/> |
| <dl> <span data-ttu-id="b17a8-211"><dt>22 (0x16) </dt></span><span class="sxs-lookup"><span data-stu-id="b17a8-211"><dt>22 (0x16)</dt></span></span> </dl> | <span data-ttu-id="b17a8-212">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="b17a8-212">Device is disabled.</span></span><br/>                                                                                                           |
| <dl> <span data-ttu-id="b17a8-213"><dt>23 (0x17) </dt></span><span class="sxs-lookup"><span data-stu-id="b17a8-213"><dt>23 (0x17)</dt></span></span> </dl> | <span data-ttu-id="b17a8-214">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="b17a8-214">System failure.</span></span> <span data-ttu-id="b17a8-215">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="b17a8-215">If changing the device driver is ineffective, see the hardware documentation.</span></span><br/>                                 |
| <dl> <span data-ttu-id="b17a8-216"><dt>24 (0x18) </dt></span><span class="sxs-lookup"><span data-stu-id="b17a8-216"><dt>24 (0x18)</dt></span></span> </dl> | <span data-ttu-id="b17a8-217">裝置不存在、無法正常運作，或未安裝所有的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="b17a8-217">Device is not present, not working properly, or does not have all of its drivers installed.</span></span><br/>                                   |
| <dl> <span data-ttu-id="b17a8-218"><dt>25 (0x19) </dt></span><span class="sxs-lookup"><span data-stu-id="b17a8-218"><dt>25 (0x19)</dt></span></span> </dl> | <span data-ttu-id="b17a8-219">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="b17a8-219">Windows is still setting up the device.</span></span><br/>                                                                                       |
| <dl> <span data-ttu-id="b17a8-220"><dt>26 (0x1A) </dt></span><span class="sxs-lookup"><span data-stu-id="b17a8-220"><dt>26 (0x1A)</dt></span></span> </dl> | <span data-ttu-id="b17a8-221">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="b17a8-221">Windows is still setting up the device.</span></span><br/>                                                                                       |
| <dl> <span data-ttu-id="b17a8-222"><dt>27 (0x1B) </dt></span><span class="sxs-lookup"><span data-stu-id="b17a8-222"><dt>27 (0x1B)</dt></span></span> </dl> | <span data-ttu-id="b17a8-223">裝置沒有有效的記錄檔設定。</span><span class="sxs-lookup"><span data-stu-id="b17a8-223">Device does not have valid log configuration.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="b17a8-224"><dt>28 (0x1C) </dt></span><span class="sxs-lookup"><span data-stu-id="b17a8-224"><dt>28 (0x1C)</dt></span></span> </dl> | <span data-ttu-id="b17a8-225">未安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="b17a8-225">Device drivers are not installed.</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="b17a8-226"><dt>29 (Bugcheck 0x1d) </dt></span><span class="sxs-lookup"><span data-stu-id="b17a8-226"><dt>29 (0x1D)</dt></span></span> </dl> | <span data-ttu-id="b17a8-227">裝置已停用;裝置固件未提供所需的資源。</span><span class="sxs-lookup"><span data-stu-id="b17a8-227">Device is disabled; the device firmware did not provide the required resources.</span></span><br/>                                               |
| <dl> <span data-ttu-id="b17a8-228"><dt>30 (0x1E) </dt></span><span class="sxs-lookup"><span data-stu-id="b17a8-228"><dt>30 (0x1E)</dt></span></span> </dl> | <span data-ttu-id="b17a8-229">裝置正在使用其他裝置正在使用的 IRQ 資源。</span><span class="sxs-lookup"><span data-stu-id="b17a8-229">Device is using an IRQ resource that another device is using.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="b17a8-230"><dt>31 (0x1F) </dt></span><span class="sxs-lookup"><span data-stu-id="b17a8-230"><dt>31 (0x1F)</dt></span></span> </dl> | <span data-ttu-id="b17a8-231">裝置無法正常運作;Windows 無法載入所需的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="b17a8-231">Device is not working properly; Windows cannot load the required device drivers.</span></span><br/>                                              |



 

</dd> <dt>

<span data-ttu-id="b17a8-232">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="b17a8-232">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b17a8-233">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="b17a8-233">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b17a8-234">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b17a8-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b17a8-235">若 **為 TRUE**，則裝置會使用使用者定義的設定。</span><span class="sxs-lookup"><span data-stu-id="b17a8-235">If **TRUE**, the device is using a user-defined configuration.</span></span>

</dd> <dt>

<span data-ttu-id="b17a8-236">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b17a8-236">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b17a8-237">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b17a8-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b17a8-238">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b17a8-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b17a8-239">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="b17a8-239">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="b17a8-240">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="b17a8-240">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="b17a8-241">**說明**</span><span class="sxs-lookup"><span data-stu-id="b17a8-241">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b17a8-242">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b17a8-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b17a8-243">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b17a8-243">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b17a8-244">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="b17a8-244">Textual description of the object.</span></span> <span data-ttu-id="b17a8-245">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="b17a8-245">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="b17a8-246">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="b17a8-246">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b17a8-247">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b17a8-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b17a8-248">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b17a8-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b17a8-249">用來唯一命名邏輯裝置的位址或其他識別資訊。</span><span class="sxs-lookup"><span data-stu-id="b17a8-249">Address or other identifying information to uniquely name the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="b17a8-250">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="b17a8-250">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b17a8-251">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="b17a8-251">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b17a8-252">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b17a8-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b17a8-253">若 **為 TRUE**，則表示 **LastErrorCode** 屬性中報告的錯誤現在已清除。</span><span class="sxs-lookup"><span data-stu-id="b17a8-253">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

</dd> <dt>

<span data-ttu-id="b17a8-254">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="b17a8-254">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b17a8-255">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b17a8-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b17a8-256">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b17a8-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b17a8-257">自由格式的字串，提供 **LastErrorCode** 屬性中所記錄之錯誤的相關資訊，以及要執行的更正動作。</span><span class="sxs-lookup"><span data-stu-id="b17a8-257">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

</dd> <dt>

<span data-ttu-id="b17a8-258">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b17a8-258">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b17a8-259">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="b17a8-259">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b17a8-260">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b17a8-260">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b17a8-261">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="b17a8-261">Date and time the object was installed.</span></span> <span data-ttu-id="b17a8-262">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="b17a8-262">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="b17a8-263">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="b17a8-263">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="b17a8-264">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="b17a8-264">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b17a8-265">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="b17a8-265">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b17a8-266">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b17a8-266">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b17a8-267">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b17a8-267">Last error code reported by the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="b17a8-268">**名稱**</span><span class="sxs-lookup"><span data-stu-id="b17a8-268">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b17a8-269">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b17a8-269">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b17a8-270">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b17a8-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b17a8-271">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="b17a8-271">Label by which the object is known.</span></span> <span data-ttu-id="b17a8-272">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="b17a8-272">When subclassed, this property can be overridden to be a key property.</span></span> <span data-ttu-id="b17a8-273">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="b17a8-273">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="b17a8-274">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="b17a8-274">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b17a8-275">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b17a8-275">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b17a8-276">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b17a8-276">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b17a8-277">指出邏輯裝置的 Win32 隨插即用裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="b17a8-277">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="b17a8-278">範例： " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="b17a8-278">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="b17a8-279">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="b17a8-279">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b17a8-280">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="b17a8-280">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b17a8-281">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b17a8-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b17a8-282">邏輯裝置的特定電源相關功能陣列。</span><span class="sxs-lookup"><span data-stu-id="b17a8-282">Array of the specific power-related capabilities of a logical device.</span></span> <span data-ttu-id="b17a8-283">這個屬性繼承自 **CIM \_ LogicalDevice**。</span><span class="sxs-lookup"><span data-stu-id="b17a8-283">This property is inherited from **CIM\_LogicalDevice**.</span></span>



| <span data-ttu-id="b17a8-284">值</span><span class="sxs-lookup"><span data-stu-id="b17a8-284">Value</span></span>                                                                                                                                                                                                                                                                                                                                                                 | <span data-ttu-id="b17a8-285">意義</span><span class="sxs-lookup"><span data-stu-id="b17a8-285">Meaning</span></span>                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="b17a8-286"><dt>**未知**</dt>的 <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="b17a8-286"><dt>**Unknown**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                                                                                                                     |                                                                                                                                                                                                                                                                                                                                      |
| <span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span><dl> <span data-ttu-id="b17a8-287"><dt>**不支援**</dt> <dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="b17a8-287"><dt>**Not Supported**</dt> <dt>1 (0x1)</dt></span></span> </dl>                                                                                                             |                                                                                                                                                                                                                                                                                                                                      |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="b17a8-288"><dt>**停用**</dt> <dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="b17a8-288"><dt>**Disabled**</dt> <dt>2 (0x2)</dt></span></span> </dl>                                                                                                                                 |                                                                                                                                                                                                                                                                                                                                      |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="b17a8-289"><dt>**已啟用**</dt> <dt>3 (0x3)</dt></span><span class="sxs-lookup"><span data-stu-id="b17a8-289"><dt>**Enabled**</dt> <dt>3 (0x3)</dt></span></span> </dl>                                                                                                                                     | <span data-ttu-id="b17a8-290">電源管理功能目前已啟用，但實際的功能組不明，或資訊無法使用。</span><span class="sxs-lookup"><span data-stu-id="b17a8-290">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span><br/>                                                                                                                                                                                               |
| <span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span><dl> <span data-ttu-id="b17a8-291"><dt>**自動輸入**</dt> <dt>4 (0X4</dt>的省電模式) </span><span class="sxs-lookup"><span data-stu-id="b17a8-291"><dt>**Power Saving Modes Entered Automatically**</dt> <dt>4 (0x4)</dt></span></span> </dl> | <span data-ttu-id="b17a8-292">裝置可以根據使用方式或其他準則來變更其電源狀態。</span><span class="sxs-lookup"><span data-stu-id="b17a8-292">The device can change its power state based on usage or other criteria.</span></span><br/>                                                                                                                                                                                                                                                   |
| <span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span><dl> <span data-ttu-id="b17a8-293"><dt>**電源狀態可設定**</dt> <dt>5 (0x5)</dt></span><span class="sxs-lookup"><span data-stu-id="b17a8-293"><dt>**Power State Settable**</dt> <dt>5 (0x5)</dt></span></span> </dl>                                                                                 | <span data-ttu-id="b17a8-294">支援 [**SetPowerState**](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-controller) 方法。</span><span class="sxs-lookup"><span data-stu-id="b17a8-294">The [**SetPowerState**](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-controller) method is supported.</span></span> <span data-ttu-id="b17a8-295">這個方法可在父 **CIM \_ LogicalDevice** 類別上找到，並且可以實作為。</span><span class="sxs-lookup"><span data-stu-id="b17a8-295">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="b17a8-296">如需詳細資訊，請參閱 [設計受控物件格式 (MOF) 類別](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes)。</span><span class="sxs-lookup"><span data-stu-id="b17a8-296">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span><br/> |
| <span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span><dl> <span data-ttu-id="b17a8-297"><dt>**電源迴圈支援**</dt> <dt>6 (0x6)</dt></span><span class="sxs-lookup"><span data-stu-id="b17a8-297"><dt>**Power Cycling Supported**</dt> <dt>6 (0x6)</dt></span></span> </dl>                                                                     | <span data-ttu-id="b17a8-298">您可以叫用 [**SetPowerState**](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-controller) 方法，並將 *>powerstate* 參數設定為 5 ( 「電源週期」 ) 。</span><span class="sxs-lookup"><span data-stu-id="b17a8-298">The [**SetPowerState**](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-controller) method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span><br/>                                                                                                                                                            |
| <span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span><dl> <span data-ttu-id="b17a8-299"><dt>**支援的**</dt> <dt>7 (0X7)</dt>的計時電源</span><span class="sxs-lookup"><span data-stu-id="b17a8-299"><dt>**Timed Power On Supported**</dt> <dt>7 (0x7)</dt></span></span> </dl>                                                                 | <span data-ttu-id="b17a8-300">您可以叫用 [**SetPowerState**](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-controller) 方法，並將 *>powerstate* 參數設定為 5 ( 「電源週期」 ) ，並將 *時間* 設定為特定日期和時間（或時間間隔），以進行電源開啟。</span><span class="sxs-lookup"><span data-stu-id="b17a8-300">The [**SetPowerState**](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-controller) method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and *Time* set to a specific date and time, or interval, for power-on.</span></span><br/>                                                                                       |



 

</dd> <dt>

<span data-ttu-id="b17a8-301">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="b17a8-301">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b17a8-302">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="b17a8-302">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b17a8-303">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b17a8-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b17a8-304">若 **為 TRUE**，則裝置可以受電源管理，也就是進入省電狀態。</span><span class="sxs-lookup"><span data-stu-id="b17a8-304">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="b17a8-305">如果 **為 FALSE**，則整數值 1 ( 「不支援」 ) 應該是 **PowerManagementCapabilities** 陣列中的唯一專案。</span><span class="sxs-lookup"><span data-stu-id="b17a8-305">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="b17a8-306">這個屬性不會指出電源管理功能目前是否已啟用，或啟用時支援哪些功能。</span><span class="sxs-lookup"><span data-stu-id="b17a8-306">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="b17a8-307">如需詳細資訊，請參閱 **PowerManagementCapabilities** 陣列。</span><span class="sxs-lookup"><span data-stu-id="b17a8-307">For more information, see the **PowerManagementCapabilities** array.</span></span>

</dd> <dt>

<span data-ttu-id="b17a8-308">**狀態**</span><span class="sxs-lookup"><span data-stu-id="b17a8-308">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b17a8-309">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b17a8-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b17a8-310">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b17a8-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b17a8-311">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="b17a8-311">Current status of the object.</span></span> <span data-ttu-id="b17a8-312">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="b17a8-312">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="b17a8-313">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="b17a8-313">Values include the following:</span></span>

<dl><span id="OK"></span><span id="ok"></span><dt>

<span data-ttu-id="b17a8-314">**正常**</span><span class="sxs-lookup"><span data-stu-id="b17a8-314">**"OK"**</span></span>
</dt><span id="Error"></span><span id="error"></span><span id="ERROR"></span><dt>

<span data-ttu-id="b17a8-315">**錯誤**</span><span class="sxs-lookup"><span data-stu-id="b17a8-315">**"Error"**</span></span>
</dt><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dt>

<span data-ttu-id="b17a8-316">**降級**</span><span class="sxs-lookup"><span data-stu-id="b17a8-316">**"Degraded"**</span></span>
</dt><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dt>

<span data-ttu-id="b17a8-317">**不明**</span><span class="sxs-lookup"><span data-stu-id="b17a8-317">**"Unknown"**</span></span>
</dt><span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span><dt>

<span data-ttu-id="b17a8-318">**「Pred 失敗」**</span><span class="sxs-lookup"><span data-stu-id="b17a8-318">**"Pred Fail"**</span></span>
</dt><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dt>

<span data-ttu-id="b17a8-319">**入門**</span><span class="sxs-lookup"><span data-stu-id="b17a8-319">**"Starting"**</span></span>
</dt><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span><dt>

<span data-ttu-id="b17a8-320">**從而**</span><span class="sxs-lookup"><span data-stu-id="b17a8-320">**"Stopping"**</span></span>
</dt><span id="Service"></span><span id="service"></span><span id="SERVICE"></span><dt>

<span data-ttu-id="b17a8-321">**維護**</span><span class="sxs-lookup"><span data-stu-id="b17a8-321">**"Service"**</span></span>
</dt><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span><dt>

<span data-ttu-id="b17a8-322">**強調**</span><span class="sxs-lookup"><span data-stu-id="b17a8-322">**"Stressed"**</span></span>
</dt><span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span><dt>

<span data-ttu-id="b17a8-323">**"NonRecover"**</span><span class="sxs-lookup"><span data-stu-id="b17a8-323">**"NonRecover"**</span></span>
</dt><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span><dt>

<span data-ttu-id="b17a8-324">**「無連絡人」**</span><span class="sxs-lookup"><span data-stu-id="b17a8-324">**"No Contact"**</span></span>
</dt><span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span><dt>

<span data-ttu-id="b17a8-325">**「遺失通訊」**</span><span class="sxs-lookup"><span data-stu-id="b17a8-325">**"Lost Comm"**</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b17a8-326">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="b17a8-326">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b17a8-327">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="b17a8-327">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b17a8-328">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b17a8-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b17a8-329">邏輯裝置的狀態。</span><span class="sxs-lookup"><span data-stu-id="b17a8-329">State of the logical device.</span></span> <span data-ttu-id="b17a8-330">如果此屬性不適用於邏輯裝置，則應該使用值 5 ( 「不適用」 ) 。</span><span class="sxs-lookup"><span data-stu-id="b17a8-330">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span> <span data-ttu-id="b17a8-331">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="b17a8-331">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

<dl> <dt>

<span data-ttu-id="b17a8-332"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1 (0x1) ) </span><span class="sxs-lookup"><span data-stu-id="b17a8-332"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1 (0x1))</span></span>
</dt> <dt>

<span data-ttu-id="b17a8-333"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2 (0x2) ) </span><span class="sxs-lookup"><span data-stu-id="b17a8-333"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2 (0x2))</span></span>
</dt> <dt>

<span data-ttu-id="b17a8-334"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (3 (0x3) ) </span><span class="sxs-lookup"><span data-stu-id="b17a8-334"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3 (0x3))</span></span>
</dt> <dt>

<span data-ttu-id="b17a8-335"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**停用** (4 (0x4) ) </span><span class="sxs-lookup"><span data-stu-id="b17a8-335"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (4 (0x4))</span></span>
</dt> <dt>

<span data-ttu-id="b17a8-336"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (5 (0x5) ) </span><span class="sxs-lookup"><span data-stu-id="b17a8-336"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (5 (0x5))</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b17a8-337">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b17a8-337">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b17a8-338">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b17a8-338">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b17a8-339">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b17a8-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b17a8-340">設定系統建立類別名稱的範圍。</span><span class="sxs-lookup"><span data-stu-id="b17a8-340">Scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="b17a8-341">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="b17a8-341">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b17a8-342">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b17a8-342">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b17a8-343">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b17a8-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b17a8-344">設定系統名稱的範圍。</span><span class="sxs-lookup"><span data-stu-id="b17a8-344">Scoping system's name.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b17a8-345">規格需求</span><span class="sxs-lookup"><span data-stu-id="b17a8-345">Requirements</span></span>



| <span data-ttu-id="b17a8-346">需求</span><span class="sxs-lookup"><span data-stu-id="b17a8-346">Requirement</span></span> | <span data-ttu-id="b17a8-347">值</span><span class="sxs-lookup"><span data-stu-id="b17a8-347">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b17a8-348">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b17a8-348">Minimum supported client</span></span><br/> | <span data-ttu-id="b17a8-349">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b17a8-349">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="b17a8-350">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b17a8-350">Minimum supported server</span></span><br/> | <span data-ttu-id="b17a8-351">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b17a8-351">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b17a8-352">命名空間</span><span class="sxs-lookup"><span data-stu-id="b17a8-352">Namespace</span></span><br/>                | <span data-ttu-id="b17a8-353">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="b17a8-353">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b17a8-354">MOF</span><span class="sxs-lookup"><span data-stu-id="b17a8-354">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b17a8-355"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="b17a8-355"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b17a8-356">DLL</span><span class="sxs-lookup"><span data-stu-id="b17a8-356">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b17a8-357"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b17a8-357"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b17a8-358">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b17a8-358">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b17a8-359">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="b17a8-359">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> <dt>

[<span data-ttu-id="b17a8-360">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="b17a8-360">**CIM\_LogicalDevice**</span></span>](/windows/desktop/CIMWin32Prov/cim-logicaldevice)
</dt> </dl>

 

