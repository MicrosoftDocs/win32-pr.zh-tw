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
# <a name="msvm_virtualsystemmanagementservicesettingdata-class"></a><span data-ttu-id="de6e4-103">Msvm \_ VirtualSystemManagementServiceSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="de6e4-103">Msvm\_VirtualSystemManagementServiceSettingData class</span></span>

<span data-ttu-id="de6e4-104">代表存在於單一主機系統上的虛擬化服務的設定。</span><span class="sxs-lookup"><span data-stu-id="de6e4-104">Represents the settings for the virtualization service present on a single host system.</span></span> <span data-ttu-id="de6e4-105">無法直接修改這個類別的屬性。</span><span class="sxs-lookup"><span data-stu-id="de6e4-105">The properties for this class cannot be modified directly.</span></span> <span data-ttu-id="de6e4-106">用戶端必須呼叫 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md)方法，才能修改這些屬性的任何一個。</span><span class="sxs-lookup"><span data-stu-id="de6e4-106">The client must call the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class to modify any of these properties.</span></span>

<span data-ttu-id="de6e4-107">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="de6e4-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="de6e4-108">語法</span><span class="sxs-lookup"><span data-stu-id="de6e4-108">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="de6e4-109">成員</span><span class="sxs-lookup"><span data-stu-id="de6e4-109">Members</span></span>

<span data-ttu-id="de6e4-110">**Msvm \_ VirtualSystemManagementServiceSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="de6e4-110">The **Msvm\_VirtualSystemManagementServiceSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="de6e4-111">屬性</span><span class="sxs-lookup"><span data-stu-id="de6e4-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="de6e4-112">屬性</span><span class="sxs-lookup"><span data-stu-id="de6e4-112">Properties</span></span>

<span data-ttu-id="de6e4-113">**Msvm \_ VirtualSystemManagementServiceSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="de6e4-113">The **Msvm\_VirtualSystemManagementServiceSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="de6e4-114">**BiosLockString**</span><span class="sxs-lookup"><span data-stu-id="de6e4-114">**BiosLockString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de6e4-115">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="de6e4-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de6e4-116">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="de6e4-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de6e4-117">限定詞： [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32) </span><span class="sxs-lookup"><span data-stu-id="de6e4-117">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32)</span></span>
</dt> </dl>

<span data-ttu-id="de6e4-118">Oem 用來允許 BIOS 鎖定的 Windows 作業系統在虛擬機器中執行。</span><span class="sxs-lookup"><span data-stu-id="de6e4-118">Used by OEMs to allow BIOS-locked Windows operating systems to run in the virtual machine.</span></span> <span data-ttu-id="de6e4-119">這個字串的長度必須剛好是32個字元。</span><span class="sxs-lookup"><span data-stu-id="de6e4-119">This string must be exactly 32 characters in length.</span></span>

<span data-ttu-id="de6e4-120">這是唯讀屬性，但是可以使用 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md)方法來變更。</span><span class="sxs-lookup"><span data-stu-id="de6e4-120">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="de6e4-121">**標題**</span><span class="sxs-lookup"><span data-stu-id="de6e4-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de6e4-122">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="de6e4-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de6e4-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="de6e4-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="de6e4-124">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="de6e4-124">A short description of the object.</span></span> <span data-ttu-id="de6e4-125">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「Hyper-v 虛擬系統管理服務」。</span><span class="sxs-lookup"><span data-stu-id="de6e4-125">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Virtual System Management Service".</span></span>

</dd> <dt>

<span data-ttu-id="de6e4-126">**CurrentWWNNAddress**</span><span class="sxs-lookup"><span data-stu-id="de6e4-126">**CurrentWWNNAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de6e4-127">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="de6e4-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de6e4-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="de6e4-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="de6e4-129">全球節點名稱 (WWNN) 位址，適用于綜合主機匯流排介面卡所用動態產生的全球名稱位址。</span><span class="sxs-lookup"><span data-stu-id="de6e4-129">The world wide node name (WWNN) address for dynamically generated world wide name addresses used for synthetic host bus adapters.</span></span>

<span data-ttu-id="de6e4-130">這是唯讀屬性，但是可以使用 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md)方法來變更。</span><span class="sxs-lookup"><span data-stu-id="de6e4-130">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="de6e4-131">**DefaultExternalDataRoot**</span><span class="sxs-lookup"><span data-stu-id="de6e4-131">**DefaultExternalDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de6e4-132">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="de6e4-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de6e4-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="de6e4-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de6e4-134">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)。**ConfigurationDataRoot**") </span><span class="sxs-lookup"><span data-stu-id="de6e4-134">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md).**ConfigurationDataRoot**")</span></span>
</dt> </dl>

<span data-ttu-id="de6e4-135">預設的外部資料根目錄。</span><span class="sxs-lookup"><span data-stu-id="de6e4-135">The default external data root.</span></span> <span data-ttu-id="de6e4-136">根據預設，「*root* \\ ProgramData \\ Microsoft \\ Windows \\ 虛擬化」。</span><span class="sxs-lookup"><span data-stu-id="de6e4-136">By default, "*root*\\ProgramData\\Microsoft\\Windows\\Virtualization".</span></span>

<span data-ttu-id="de6e4-137">這是唯讀屬性，但是可以使用 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md)方法來變更。</span><span class="sxs-lookup"><span data-stu-id="de6e4-137">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="de6e4-138">**DefaultVirtualHardDiskCachingMode**</span><span class="sxs-lookup"><span data-stu-id="de6e4-138">**DefaultVirtualHardDiskCachingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de6e4-139">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="de6e4-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="de6e4-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="de6e4-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="de6e4-141">指出預設是否應將記憶體中的檔案快取用於磁片。</span><span class="sxs-lookup"><span data-stu-id="de6e4-141">Indicates whether in-memory file caching should be used for disks by default.</span></span> <span data-ttu-id="de6e4-142">您可以在 [**Msvm \_ StorageAllocationSettingData**](msvm-storageallocationsettingdata.md)類別的 **CachingMode** 欄位中，以每個磁片為基礎覆寫此值。</span><span class="sxs-lookup"><span data-stu-id="de6e4-142">This value can be overridden on a per-disk basis in the **CachingMode** field of the [**Msvm\_StorageAllocationSettingData**](msvm-storageallocationsettingdata.md) class.</span></span>

> [!Note]  
> <span data-ttu-id="de6e4-143">在 Windows 10 和 Windows Server 2016 中新增。</span><span class="sxs-lookup"><span data-stu-id="de6e4-143">Added in Windows 10 and Windows Server 2016.</span></span>

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="de6e4-144">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="de6e4-144">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Caching"></span><span id="no_caching"></span><span id="NO_CACHING"></span>

<span data-ttu-id="de6e4-145">**沒有** 快取 (3) </span><span class="sxs-lookup"><span data-stu-id="de6e4-145">**No Caching** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Cache_Sharable_Parents"></span><span id="cache_sharable_parents"></span><span id="CACHE_SHARABLE_PARENTS"></span>

<span data-ttu-id="de6e4-146">快取可 **共用** 的父系 (4) </span><span class="sxs-lookup"><span data-stu-id="de6e4-146">**Cache Sharable Parents** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="de6e4-147">**DefaultVirtualHardDiskPath**</span><span class="sxs-lookup"><span data-stu-id="de6e4-147">**DefaultVirtualHardDiskPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de6e4-148">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="de6e4-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de6e4-149">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="de6e4-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="de6e4-150">預設虛擬硬碟路徑。</span><span class="sxs-lookup"><span data-stu-id="de6e4-150">The default virtual hard disk path.</span></span> <span data-ttu-id="de6e4-151">依預設，「*根* \\ 使用者 \\ 公用 \\ 檔 \\ 虛擬硬碟」。</span><span class="sxs-lookup"><span data-stu-id="de6e4-151">By default, "*root*\\Users\\Public\\Documents\\Virtual Hard Disks".</span></span>

<span data-ttu-id="de6e4-152">這是唯讀屬性，但是可以使用 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md)方法來變更。</span><span class="sxs-lookup"><span data-stu-id="de6e4-152">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="de6e4-153">**說明**</span><span class="sxs-lookup"><span data-stu-id="de6e4-153">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de6e4-154">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="de6e4-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de6e4-155">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="de6e4-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="de6e4-156">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="de6e4-156">A description of the object.</span></span> <span data-ttu-id="de6e4-157">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「虛擬系統管理服務的設定」。</span><span class="sxs-lookup"><span data-stu-id="de6e4-157">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Settings for the Virtual System Management Service".</span></span>

</dd> <dt>

<span data-ttu-id="de6e4-158">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="de6e4-158">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de6e4-159">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="de6e4-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de6e4-160">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="de6e4-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="de6e4-161">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="de6e4-161">A display name for the object.</span></span> <span data-ttu-id="de6e4-162">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「Hyper-v 虛擬系統管理服務」。</span><span class="sxs-lookup"><span data-stu-id="de6e4-162">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Virtual System Management Service".</span></span> <span data-ttu-id="de6e4-163">變更這個屬性將會變更相關聯之 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)衍生的 **ElementName** 屬性。</span><span class="sxs-lookup"><span data-stu-id="de6e4-163">Changing this property will change the **ElementName** property of the associated [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) derivative.</span></span>

</dd> <dt>

<span data-ttu-id="de6e4-164">**EnhancedSessionModeEnabled**</span><span class="sxs-lookup"><span data-stu-id="de6e4-164">**EnhancedSessionModeEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de6e4-165">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="de6e4-165">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="de6e4-166">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="de6e4-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="de6e4-167">指出伺服器是否允許增強的會話模式。</span><span class="sxs-lookup"><span data-stu-id="de6e4-167">Indicates whether enhanced session mode is permitted on the server.</span></span> <span data-ttu-id="de6e4-168">**True** 表示允許，否則 **為 False**。</span><span class="sxs-lookup"><span data-stu-id="de6e4-168">**True** indicates permitted, otherwise **False**.</span></span>

<span data-ttu-id="de6e4-169">**Windows 8.1：** 在 Windows 8.1 和 Windows Server 2012 R2 之前，不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="de6e4-169">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="de6e4-170">**HbaLunTimeout**</span><span class="sxs-lookup"><span data-stu-id="de6e4-170">**HbaLunTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de6e4-171">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="de6e4-171">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="de6e4-172">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="de6e4-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="de6e4-173">指定綜合光纖通道虛擬裝置在啟動虛擬機器之前，會等待邏輯單元編號 (LUN) 出現的時間量。</span><span class="sxs-lookup"><span data-stu-id="de6e4-173">Specifies the amount of time that the synthetic Fibre Channel virtual device will wait for a logical unit number (LUN) to appear before starting a virtual machine.</span></span>

<span data-ttu-id="de6e4-174">這是唯讀屬性，但是可以使用 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md)方法來變更。</span><span class="sxs-lookup"><span data-stu-id="de6e4-174">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="de6e4-175">**HypervisorRootSchedulerEnabled**</span><span class="sxs-lookup"><span data-stu-id="de6e4-175">**HypervisorRootSchedulerEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de6e4-176">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="de6e4-176">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="de6e4-177">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="de6e4-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="de6e4-178">是否啟用虛擬程式根排程器。</span><span class="sxs-lookup"><span data-stu-id="de6e4-178">Whether or not the hypervisor root scheduler is enabled.</span></span>

> [!Note]  
> <span data-ttu-id="de6e4-179">在 Windows 10 1709 版中新增。</span><span class="sxs-lookup"><span data-stu-id="de6e4-179">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="de6e4-180">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="de6e4-180">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de6e4-181">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="de6e4-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de6e4-182">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="de6e4-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de6e4-183">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="de6e4-183">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="de6e4-184">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="de6e4-184">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="de6e4-185">這個屬性繼承自 [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))，而且一律設定為 "Microsoft：*host*"，其中 *Host* 是主控電腦系統的 NetBIOS 名稱。</span><span class="sxs-lookup"><span data-stu-id="de6e4-185">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)), and it is always set to "Microsoft:*host*", where *host* is the NetBIOS name of the hosting computer system.</span></span>

</dd> <dt>

<span data-ttu-id="de6e4-186">**MaximumMacAddress**</span><span class="sxs-lookup"><span data-stu-id="de6e4-186">**MaximumMacAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de6e4-187">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="de6e4-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de6e4-188">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="de6e4-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="de6e4-189">動態產生的 MAC 位址之 MAC 位址的上限。</span><span class="sxs-lookup"><span data-stu-id="de6e4-189">The maximum MAC address for dynamically generated MAC addresses.</span></span>

<span data-ttu-id="de6e4-190">這是唯讀屬性，但是可以使用 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md)方法來變更。</span><span class="sxs-lookup"><span data-stu-id="de6e4-190">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="de6e4-191">**MaximumWWPNAddress**</span><span class="sxs-lookup"><span data-stu-id="de6e4-191">**MaximumWWPNAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de6e4-192">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="de6e4-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de6e4-193">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="de6e4-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="de6e4-194">最大全球埠名稱 (WWPN) 位址，適用于綜合主機匯流排介面卡所用的動態產生全球名稱位址。</span><span class="sxs-lookup"><span data-stu-id="de6e4-194">The maximum world wide port name (WWPN) address for dynamically generated world wide name addresses used for synthetic host bus adapters.</span></span>

<span data-ttu-id="de6e4-195">這是唯讀屬性，但是可以使用 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md)方法來變更。</span><span class="sxs-lookup"><span data-stu-id="de6e4-195">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="de6e4-196">**MinimumMacAddress**</span><span class="sxs-lookup"><span data-stu-id="de6e4-196">**MinimumMacAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de6e4-197">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="de6e4-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de6e4-198">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="de6e4-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="de6e4-199">動態產生的 MAC 位址之 MAC 位址的最小值。</span><span class="sxs-lookup"><span data-stu-id="de6e4-199">The minimum MAC address for dynamically generated MAC addresses.</span></span>

<span data-ttu-id="de6e4-200">這是唯讀屬性，但是可以使用 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md)方法來變更。</span><span class="sxs-lookup"><span data-stu-id="de6e4-200">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="de6e4-201">**MinimumWWPNAddress**</span><span class="sxs-lookup"><span data-stu-id="de6e4-201">**MinimumWWPNAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de6e4-202">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="de6e4-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de6e4-203">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="de6e4-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="de6e4-204">動態產生的全球通訊埠名稱位址，用於綜合主機匯流排介面卡。</span><span class="sxs-lookup"><span data-stu-id="de6e4-204">The minimum world wide port name address for dynamically generated world wide name addresses used for synthetic host bus adapters.</span></span>

<span data-ttu-id="de6e4-205">這是唯讀屬性，但是可以使用 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md)方法來變更。</span><span class="sxs-lookup"><span data-stu-id="de6e4-205">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="de6e4-206">**NumaSpanningEnabled**</span><span class="sxs-lookup"><span data-stu-id="de6e4-206">**NumaSpanningEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de6e4-207">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="de6e4-207">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="de6e4-208">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="de6e4-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="de6e4-209">指定當啟動虛擬機器時，或是將記憶體指派給虛擬機器的動態記憶體時，是否可以從遠端非統一記憶體存取 (NUMA) 節點配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="de6e4-209">Specifies whether memory can be allocated from remote nonuniform memory access (NUMA) nodes when starting a virtual machine or when assigning memory to a virtual machine by dynamic memory.</span></span> <span data-ttu-id="de6e4-210">這可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="de6e4-210">This can be one of the following values.</span></span>



| <span data-ttu-id="de6e4-211">值</span><span class="sxs-lookup"><span data-stu-id="de6e4-211">Value</span></span>                                                                                | <span data-ttu-id="de6e4-212">意義</span><span class="sxs-lookup"><span data-stu-id="de6e4-212">Meaning</span></span>                                                                                     |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="de6e4-213"><dt>**對**</dt></span><span class="sxs-lookup"><span data-stu-id="de6e4-213"><dt>**True**</dt></span></span> </dl>  | <span data-ttu-id="de6e4-214">您可以從本機和遠端 NUMA 節點配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="de6e4-214">Memory can be allocated from both local and remote NUMA nodes.</span></span><br/>                   |
| <dl> <span data-ttu-id="de6e4-215"><dt>**否**</dt></span><span class="sxs-lookup"><span data-stu-id="de6e4-215"><dt>**False**</dt></span></span> </dl> | <span data-ttu-id="de6e4-216">記憶體只能從指派給虛擬機器的 NUMA 節點進行配置。</span><span class="sxs-lookup"><span data-stu-id="de6e4-216">Memory can be allocated only from the NUMA node assigned to the virtual machine.</span></span><br/> |



 

<span data-ttu-id="de6e4-217">這是唯讀屬性，但是可以使用 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md)方法來變更。</span><span class="sxs-lookup"><span data-stu-id="de6e4-217">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="de6e4-218">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="de6e4-218">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de6e4-219">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="de6e4-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de6e4-220">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="de6e4-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de6e4-221">限定詞： [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| 一般資訊 \| 001.4 ") </span><span class="sxs-lookup"><span data-stu-id="de6e4-221">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|General Information\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="de6e4-222">說明如何聯繫主要系統擁有者 (例如電話號碼或電子郵件地址) 。</span><span class="sxs-lookup"><span data-stu-id="de6e4-222">Describes how the primary system owner can be reached (for example, phone number or email address).</span></span> <span data-ttu-id="de6e4-223">預設為空白。</span><span class="sxs-lookup"><span data-stu-id="de6e4-223">By default, empty.</span></span> <span data-ttu-id="de6e4-224">此名稱的長度不得超過256個字元。</span><span class="sxs-lookup"><span data-stu-id="de6e4-224">This name may not exceed 256 characters in length.</span></span>

<span data-ttu-id="de6e4-225">這是唯讀屬性，但是可以使用 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md)方法來變更。</span><span class="sxs-lookup"><span data-stu-id="de6e4-225">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="de6e4-226">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="de6e4-226">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de6e4-227">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="de6e4-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de6e4-228">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="de6e4-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de6e4-229">限定詞： [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| 一般資訊 \| 001.3 ") </span><span class="sxs-lookup"><span data-stu-id="de6e4-229">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|General Information\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="de6e4-230">主要系統擁有者的名稱。</span><span class="sxs-lookup"><span data-stu-id="de6e4-230">The name of the primary system owner.</span></span> <span data-ttu-id="de6e4-231">依預設，「系統管理員」。</span><span class="sxs-lookup"><span data-stu-id="de6e4-231">By default, "Administrators".</span></span> <span data-ttu-id="de6e4-232">此值的長度不得超過64個字元。</span><span class="sxs-lookup"><span data-stu-id="de6e4-232">This value may not exceed 64 characters in length.</span></span>

<span data-ttu-id="de6e4-233">這是唯讀屬性，但是可以使用 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md)方法來變更。</span><span class="sxs-lookup"><span data-stu-id="de6e4-233">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="de6e4-234">備註</span><span class="sxs-lookup"><span data-stu-id="de6e4-234">Remarks</span></span>

<span data-ttu-id="de6e4-235">存取 **Msvm \_ VirtualSystemManagementServiceSettingData** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="de6e4-235">Access to the **Msvm\_VirtualSystemManagementServiceSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="de6e4-236">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="de6e4-236">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="de6e4-237">規格需求</span><span class="sxs-lookup"><span data-stu-id="de6e4-237">Requirements</span></span>



| <span data-ttu-id="de6e4-238">需求</span><span class="sxs-lookup"><span data-stu-id="de6e4-238">Requirement</span></span> | <span data-ttu-id="de6e4-239">值</span><span class="sxs-lookup"><span data-stu-id="de6e4-239">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de6e4-240">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="de6e4-240">Minimum supported client</span></span><br/> | <span data-ttu-id="de6e4-241">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="de6e4-241">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="de6e4-242">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="de6e4-242">Minimum supported server</span></span><br/> | <span data-ttu-id="de6e4-243">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="de6e4-243">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="de6e4-244">命名空間</span><span class="sxs-lookup"><span data-stu-id="de6e4-244">Namespace</span></span><br/>                | <span data-ttu-id="de6e4-245">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="de6e4-245">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="de6e4-246">MOF</span><span class="sxs-lookup"><span data-stu-id="de6e4-246">MOF</span></span><br/>                      | <dl> <span data-ttu-id="de6e4-247"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="de6e4-247"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="de6e4-248">DLL</span><span class="sxs-lookup"><span data-stu-id="de6e4-248">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de6e4-249"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="de6e4-249"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="de6e4-250">另請參閱</span><span class="sxs-lookup"><span data-stu-id="de6e4-250">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de6e4-251">**CIM \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="de6e4-251">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> <dt>

[<span data-ttu-id="de6e4-252">**ModifyServiceSettings**</span><span class="sxs-lookup"><span data-stu-id="de6e4-252">**ModifyServiceSettings**</span></span>](modifyservicesettings-msvm-virtualsystemmanagementservice.md)
</dt> <dt>

<span data-ttu-id="de6e4-253">[**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="de6e4-253">[**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="de6e4-254">虛擬系統管理類別</span><span class="sxs-lookup"><span data-stu-id="de6e4-254">Virtual System Management Classes</span></span>](virtual-system-management-classes.md)
</dt> </dl>

 

