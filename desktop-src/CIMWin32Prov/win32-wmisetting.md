---
description: Win32 \_ WMISetting 單一 wmi 類別包含 wmi 服務的指令引數。 這個類別只能有一個實例，每個 Windows 系統一律會有一個實例，而且無法刪除。 無法建立其他實例。
ms.assetid: d33cd4f3-969b-46ce-baff-466f1a464906
ms.tgt_platform: multiple
title: Win32_WMISetting 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_WMISetting
- Win32_WMISetting.Caption
- Win32_WMISetting.Description
- Win32_WMISetting.SettingID
- Win32_WMISetting.ASPScriptDefaultNamespace
- Win32_WMISetting.ASPScriptEnabled
- Win32_WMISetting.AutorecoverMofs
- Win32_WMISetting.AutoStartWin9X
- Win32_WMISetting.BackupInterval
- Win32_WMISetting.BackupLastTime
- Win32_WMISetting.BuildVersion
- Win32_WMISetting.DatabaseDirectory
- Win32_WMISetting.DatabaseMaxSize
- Win32_WMISetting.EnableAnonWin9xConnections
- Win32_WMISetting.EnableEvents
- Win32_WMISetting.EnableStartupHeapPreallocation
- Win32_WMISetting.HighThresholdOnClientObjects
- Win32_WMISetting.HighThresholdOnEvents
- Win32_WMISetting.InstallationDirectory
- Win32_WMISetting.LastStartupHeapPreallocation
- Win32_WMISetting.LoggingDirectory
- Win32_WMISetting.LoggingLevel
- Win32_WMISetting.LowThresholdOnClientObjects
- Win32_WMISetting.LowThresholdOnEvents
- Win32_WMISetting.MaxLogFileSize
- Win32_WMISetting.MaxWaitOnClientObjects
- Win32_WMISetting.MaxWaitOnEvents
- Win32_WMISetting.MofSelfInstallDirectory
api_type:
- DllExport
api_location:
- Wbemcore.dll
ms.openlocfilehash: 8f94524d18074e3a35c7bcad09e9b9fba80e8470
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847073"
---
# <a name="win32_wmisetting-class"></a><span data-ttu-id="8c9e9-105">Win32 \_ WMISetting 類別</span><span class="sxs-lookup"><span data-stu-id="8c9e9-105">Win32\_WMISetting class</span></span>

<span data-ttu-id="8c9e9-106">**Win32 \_ WMISetting** 單一 [wmi 類別](../wmisdk/retrieving-a-class.md)包含 wmi 服務的指令引數。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-106">The **Win32\_WMISetting** singleton [WMI class](../wmisdk/retrieving-a-class.md) contains the operational parameters for the WMI service.</span></span> <span data-ttu-id="8c9e9-107">這個類別只能有一個實例，每個 Windows 系統一律會有一個實例，而且無法刪除。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-107">This class can only have one instance, which always exists for each Windows system and cannot be deleted.</span></span> <span data-ttu-id="8c9e9-108">無法建立其他實例。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-108">Additional instances cannot be created.</span></span>

<span data-ttu-id="8c9e9-109">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="8c9e9-110">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-110">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c9e9-111">語法</span><span class="sxs-lookup"><span data-stu-id="8c9e9-111">Syntax</span></span>

``` syntax
[Singleton, Dynamic, Provider("WBEMCORE"), UUID("{A83EF166-CA8D-11d2-B33D-00104BCC4B4A}"), AMENDMENT]
class Win32_WMISetting : CIM_Setting
{
  string   Caption;
  string   Description;
  string   SettingID;
  string   ASPScriptDefaultNamespace = "\\\\root\\cimv2";
  boolean  ASPScriptEnabled;
  string   AutorecoverMofs[];
  uint32   AutoStartWin9X;
  uint32   BackupInterval;
  datetime BackupLastTime;
  string   BuildVersion;
  string   DatabaseDirectory;
  uint32   DatabaseMaxSize;
  boolean  EnableAnonWin9xConnections;
  boolean  EnableEvents;
  boolean  EnableStartupHeapPreallocation;
  uint32   HighThresholdOnClientObjects;
  uint32   HighThresholdOnEvents;
  string   InstallationDirectory;
  uint32   LastStartupHeapPreallocation;
  string   LoggingDirectory;
  uint32   LoggingLevel;
  uint32   LowThresholdOnClientObjects;
  uint32   LowThresholdOnEvents;
  uint32   MaxLogFileSize;
  uint32   MaxWaitOnClientObjects;
  uint32   MaxWaitOnEvents;
  string   MofSelfInstallDirectory;
};
```

## <a name="members"></a><span data-ttu-id="8c9e9-112">成員</span><span class="sxs-lookup"><span data-stu-id="8c9e9-112">Members</span></span>

<span data-ttu-id="8c9e9-113">**Win32 \_ WMISetting** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="8c9e9-113">The **Win32\_WMISetting** class has these types of members:</span></span>

-   [<span data-ttu-id="8c9e9-114">屬性</span><span class="sxs-lookup"><span data-stu-id="8c9e9-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8c9e9-115">屬性</span><span class="sxs-lookup"><span data-stu-id="8c9e9-115">Properties</span></span>

<span data-ttu-id="8c9e9-116">**Win32 \_ WMISetting** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-116">The **Win32\_WMISetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8c9e9-117">**ASPScriptDefaultNamespace**</span><span class="sxs-lookup"><span data-stu-id="8c9e9-117">**ASPScriptDefaultNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c9e9-118">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8c9e9-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c9e9-119">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8c9e9-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8c9e9-120">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ 腳本 \| 預設命名空間" ) </span><span class="sxs-lookup"><span data-stu-id="8c9e9-120">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\scripting\|Default Namespace")</span></span>
</dt> </dl>

<span data-ttu-id="8c9e9-121">預設腳本命名空間。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-121">Default script namespace.</span></span> <span data-ttu-id="8c9e9-122">如果呼叫端未指定，則此屬性包含從 WMI 的腳本 API 呼叫所使用的命名空間。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-122">This property contains the namespace used by calls from the Scripting API for WMI if none is specified by the caller.</span></span>

<span data-ttu-id="8c9e9-123">這個屬性會反映登錄機碼中的值。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-123">This property reflects the value in the registry key.</span></span>

<span data-ttu-id="8c9e9-124">**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **WBEM** \\ **腳本 \| 預設命名空間**    </span><span class="sxs-lookup"><span data-stu-id="8c9e9-124">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM**\\    **scripting\|Default Namespace**</span></span>

<span data-ttu-id="8c9e9-125">範例：根 \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="8c9e9-125">Example: root\\cimv2</span></span>

<span data-ttu-id="8c9e9-126">如需使用這個屬性的範例腳本，請參閱「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-126">For an example script that uses this property, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="8c9e9-127">**ASPScriptEnabled**</span><span class="sxs-lookup"><span data-stu-id="8c9e9-127">**ASPScriptEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c9e9-128">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="8c9e9-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8c9e9-129">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8c9e9-129">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8c9e9-130">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ 腳本 \| 啟用 ASP" ) </span><span class="sxs-lookup"><span data-stu-id="8c9e9-130">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\scripting\|Enable for ASP")</span></span>
</dt> </dl>

<span data-ttu-id="8c9e9-131">若 **為 True，則** 可在 Active Server PAGES (ASP) 上使用 WMI 腳本。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-131">If **True**, WMI scripting can be used on Active Server Pages (ASP).</span></span> <span data-ttu-id="8c9e9-132">這個屬性在執行不支援之 Windows 版本的系統上是有效的。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-132">This property is valid on systems running unsupported versions of Windows only.</span></span> <span data-ttu-id="8c9e9-133">針對支援的 Windows 系統，ASP 上一律允許 WMI 腳本處理。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-133">For supported Windows systems, WMI scripting is always allowed on ASP.</span></span>

</dd> <dt>

<span data-ttu-id="8c9e9-134">**AutorecoverMofs**</span><span class="sxs-lookup"><span data-stu-id="8c9e9-134">**AutorecoverMofs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c9e9-135">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="8c9e9-135">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8c9e9-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8c9e9-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c9e9-137">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| mof" ) </span><span class="sxs-lookup"><span data-stu-id="8c9e9-137">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|Autorecover MOFs")</span></span>
</dt> </dl>

<span data-ttu-id="8c9e9-138">用來初始化或復原 WMI 儲存機制的完整 MOF 檔案名清單。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-138">List of fully qualified MOF file names used to initialize or recover the WMI repository.</span></span> <span data-ttu-id="8c9e9-139">此清單決定 MOF 檔案的編譯順序。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-139">The list determines the order in which MOF files are compiled.</span></span>

<span data-ttu-id="8c9e9-140">這個屬性會反映登錄機碼中的值。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-140">This property reflects the value in the registry key.</span></span>

<span data-ttu-id="8c9e9-141">**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **WBEM** \\ **CIMOM \| 自動回復 mof**    </span><span class="sxs-lookup"><span data-stu-id="8c9e9-141">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM**\\    **CIMOM\|Autorecover MOFs**</span></span>

</dd> <dt>

<span data-ttu-id="8c9e9-142">**AutoStartWin9X**</span><span class="sxs-lookup"><span data-stu-id="8c9e9-142">**AutoStartWin9X**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c9e9-143">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8c9e9-143">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8c9e9-144">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8c9e9-144">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8c9e9-145">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| AutostartWin9X" ) </span><span class="sxs-lookup"><span data-stu-id="8c9e9-145">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|AutostartWin9X")</span></span>
</dt> </dl>

<span data-ttu-id="8c9e9-146">不支援。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-146">Not supported.</span></span>

<dt>

<span id="Don_t_start"></span><span id="don_t_start"></span><span id="DON_T_START"></span>

<span data-ttu-id="8c9e9-147">**請勿開始** (0) </span><span class="sxs-lookup"><span data-stu-id="8c9e9-147">**Don't start** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Autostart"></span><span id="autostart"></span><span id="AUTOSTART"></span>

<span data-ttu-id="8c9e9-148">**Autostart** (1) </span><span class="sxs-lookup"><span data-stu-id="8c9e9-148">**Autostart** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Start_on_reboot"></span><span id="start_on_reboot"></span><span id="START_ON_REBOOT"></span>

<span data-ttu-id="8c9e9-149">**在重新開機時開始** (2) </span><span class="sxs-lookup"><span data-stu-id="8c9e9-149">**Start on reboot** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8c9e9-150">**BackupInterval**</span><span class="sxs-lookup"><span data-stu-id="8c9e9-150">**BackupInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c9e9-151">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8c9e9-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8c9e9-152">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8c9e9-152">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8c9e9-153">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| 備份間隔閾值」 ) ，[**單位**](../wmisdk/standard-qualifiers.md) ( 「分鐘」 ) </span><span class="sxs-lookup"><span data-stu-id="8c9e9-153">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|Backup Interval Threshold"), [**Units**](../wmisdk/standard-qualifiers.md) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="8c9e9-154">不支援。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-154">Not supported.</span></span> <span data-ttu-id="8c9e9-155">請改以手動方式備份 WMI 存放庫。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-155">Instead, backup the WMI repository manually.</span></span>

</dd> <dt>

<span data-ttu-id="8c9e9-156">**BackupLastTime**</span><span class="sxs-lookup"><span data-stu-id="8c9e9-156">**BackupLastTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c9e9-157">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="8c9e9-157">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8c9e9-158">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8c9e9-158">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8c9e9-159">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Time 函數 \| GetTimeZoneInformation" ) </span><span class="sxs-lookup"><span data-stu-id="8c9e9-159">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Functions\|GetTimeZoneInformation")</span></span>
</dt> </dl>

<span data-ttu-id="8c9e9-160">上次執行備份的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-160">Date and time the last backup was performed.</span></span>

</dd> <dt>

<span data-ttu-id="8c9e9-161">**BuildVersion**</span><span class="sxs-lookup"><span data-stu-id="8c9e9-161">**BuildVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c9e9-162">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8c9e9-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c9e9-163">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8c9e9-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c9e9-164">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \| Build" ) </span><span class="sxs-lookup"><span data-stu-id="8c9e9-164">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\|Build")</span></span>
</dt> </dl>

<span data-ttu-id="8c9e9-165">目前已安裝之 WMI 服務的版本資訊。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-165">Version information for the currently installed WMI service.</span></span>

<span data-ttu-id="8c9e9-166">在 WMI 資料庫的備份之間經過的時間長度。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-166">Length of time that elapses between backups of the WMI database.</span></span>

<span data-ttu-id="8c9e9-167">這個屬性會反映登錄機碼中的值。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-167">This property reflects the value in the registry key.</span></span>

<span data-ttu-id="8c9e9-168">**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **WBEM \| 組建**</span><span class="sxs-lookup"><span data-stu-id="8c9e9-168">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM\|Build**</span></span>

</dd> <dt>

<span data-ttu-id="8c9e9-169">**標題**</span><span class="sxs-lookup"><span data-stu-id="8c9e9-169">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c9e9-170">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8c9e9-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c9e9-171">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8c9e9-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c9e9-172">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) </span><span class="sxs-lookup"><span data-stu-id="8c9e9-172">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="8c9e9-173">目前物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-173">Short textual description of the current object.</span></span>

<span data-ttu-id="8c9e9-174">這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-174">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="8c9e9-175">**DatabaseDirectory**</span><span class="sxs-lookup"><span data-stu-id="8c9e9-175">**DatabaseDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c9e9-176">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8c9e9-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c9e9-177">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8c9e9-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c9e9-178">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| Repository Directory" ) </span><span class="sxs-lookup"><span data-stu-id="8c9e9-178">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|Repository Directory")</span></span>
</dt> </dl>

<span data-ttu-id="8c9e9-179">包含 WMI 存放庫的目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-179">Directory path that contains the WMI repository.</span></span>

</dd> <dt>

<span data-ttu-id="8c9e9-180">**DatabaseMaxSize**</span><span class="sxs-lookup"><span data-stu-id="8c9e9-180">**DatabaseMaxSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c9e9-181">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8c9e9-181">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8c9e9-182">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8c9e9-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c9e9-183">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| Max DB Size" ) ，[**單位**](../wmisdk/standard-qualifiers.md) ( "kb" ) </span><span class="sxs-lookup"><span data-stu-id="8c9e9-183">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|Max DB Size"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="8c9e9-184">WMI 存放庫的大小上限。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-184">Maximum size of the WMI repository.</span></span>

</dd> <dt>

<span data-ttu-id="8c9e9-185">**說明**</span><span class="sxs-lookup"><span data-stu-id="8c9e9-185">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c9e9-186">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8c9e9-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c9e9-187">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8c9e9-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8c9e9-188">目前物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-188">Textual description of the current object.</span></span>

<span data-ttu-id="8c9e9-189">這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-189">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="8c9e9-190">**EnableAnonWin9xConnections**</span><span class="sxs-lookup"><span data-stu-id="8c9e9-190">**EnableAnonWin9xConnections**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c9e9-191">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="8c9e9-191">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8c9e9-192">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8c9e9-192">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8c9e9-193">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| EnableAnonConnections" ) </span><span class="sxs-lookup"><span data-stu-id="8c9e9-193">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|EnableAnonConnections")</span></span>
</dt> </dl>

<span data-ttu-id="8c9e9-194">不支援。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-194">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="8c9e9-195">**EnableEvents**</span><span class="sxs-lookup"><span data-stu-id="8c9e9-195">**EnableEvents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c9e9-196">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="8c9e9-196">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8c9e9-197">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8c9e9-197">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8c9e9-198">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| EnableEvents" ) </span><span class="sxs-lookup"><span data-stu-id="8c9e9-198">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|EnableEvents")</span></span>
</dt> </dl>

<span data-ttu-id="8c9e9-199">若 **為 True**，則應啟用 WMI 事件子系統。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-199">If **True**, the WMI event subsystem should be enabled.</span></span>

<span data-ttu-id="8c9e9-200">這個屬性會反映登錄機碼中的值。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-200">This property reflects the value in the registry key.</span></span>

<span data-ttu-id="8c9e9-201">**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **WBEM \| CIMOM \| EnableEvents**</span><span class="sxs-lookup"><span data-stu-id="8c9e9-201">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM\|CIMOM\|EnableEvents**</span></span>

</dd> <dt>

<span data-ttu-id="8c9e9-202">**EnableStartupHeapPreallocation**</span><span class="sxs-lookup"><span data-stu-id="8c9e9-202">**EnableStartupHeapPreallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c9e9-203">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="8c9e9-203">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8c9e9-204">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8c9e9-204">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8c9e9-205">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| EnableStartupHeapPreallocation" ) </span><span class="sxs-lookup"><span data-stu-id="8c9e9-205">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|EnableStartupHeapPreallocation")</span></span>
</dt> </dl>

<span data-ttu-id="8c9e9-206">若 **為 True**，當 wmi 初始化時，wmi 會使用 **LastStartupHeapPreallocation** 值的大小來建立預先配置的堆積。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-206">If **True**, WMI creates a pre-allocated heap with the size of the **LastStartupHeapPreallocation** value when WMI is initialized.</span></span>

</dd> <dt>

<span data-ttu-id="8c9e9-207">**HighThresholdOnClientObjects**</span><span class="sxs-lookup"><span data-stu-id="8c9e9-207">**HighThresholdOnClientObjects**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c9e9-208">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8c9e9-208">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8c9e9-209">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8c9e9-209">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8c9e9-210">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ \| 在用戶端物件上的高閾值」 ) ，[**單位**](../wmisdk/standard-qualifiers.md) ( 「每秒的物件數」 ) </span><span class="sxs-lookup"><span data-stu-id="8c9e9-210">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|High Threshold On Client Objects"), [**Units**](../wmisdk/standard-qualifiers.md) ("objects per second")</span></span>
</dt> </dl>

<span data-ttu-id="8c9e9-211">提供者建立的物件可以傳遞至用戶端的最大速率。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-211">Maximum rate at which provider-created objects can be delivered to clients.</span></span> <span data-ttu-id="8c9e9-212">為了配合提供者與用戶端之間的速度差異，WMI 會將物件保留在佇列中，再將它們傳遞給取用者。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-212">To accommodate speed differentials between providers and clients, WMI holds objects in queues before delivering them to consumers.</span></span> <span data-ttu-id="8c9e9-213">為了提高效率，取用者必須以符合提供者的步調來收集物件。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-213">For more efficiency, consumers must collect the objects at a pace that matches the provider.</span></span> <span data-ttu-id="8c9e9-214">如果未回收物件所持有的記憶體達到 **LowThresholdOnObjects**，WMI 就會減緩將新物件排入佇列中的速度。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-214">If the memory held by uncollected objects reaches **LowThresholdOnObjects**, then WMI slows down the addition of new objects into the queue.</span></span> <span data-ttu-id="8c9e9-215">如果未回收事件持續累積，而且當使用的記憶體是在 **HighThresholdOnClientObjects** 中的值時，就會達到 **MaxWaitOnClientObjects** 中傳遞事件的最大等待時間，然後 WMI 不會接受來自提供者的物件，並將 **WBEM \_ E \_ \_ 的 \_ 記憶體** 傳回給用戶端。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-215">If uncollected events continue to accumulate and the maximum wait to deliver events in **MaxWaitOnClientObjects** is reached while the memory used is at the value in **HighThresholdOnClientObjects**, then WMI accepts no more objects from providers and returns **WBEM\_E\_OUT\_OF\_MEMORY** to the clients.</span></span>

</dd> <dt>

<span data-ttu-id="8c9e9-216">**HighThresholdOnEvents**</span><span class="sxs-lookup"><span data-stu-id="8c9e9-216">**HighThresholdOnEvents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c9e9-217">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8c9e9-217">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8c9e9-218">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8c9e9-218">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8c9e9-219">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ \| ) 事件上的高臨界值"，[**單位**](../wmisdk/standard-qualifiers.md) ( 「每秒事件數」 ) </span><span class="sxs-lookup"><span data-stu-id="8c9e9-219">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|High Threshold On Events"), [**Units**](../wmisdk/standard-qualifiers.md) ("events per second")</span></span>
</dt> </dl>

<span data-ttu-id="8c9e9-220">事件傳遞至用戶端的最大速率。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-220">Maximum rate at which events are to be delivered to clients.</span></span> <span data-ttu-id="8c9e9-221">為了配合提供者與用戶端之間的速度差異，WMI 會將事件排入佇列，然後再傳遞給取用者。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-221">To accommodate speed differentials between providers and clients, WMI queues events before delivering them to consumers.</span></span> <span data-ttu-id="8c9e9-222">為了提高效率，取用者必須以符合提供者的步調來收集事件。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-222">For more efficiency, consumers must collect the events at a pace that matches the provider.</span></span> <span data-ttu-id="8c9e9-223">如果未回收事件所保留的記憶體達到 **LowThresholdOnObjects**，WMI 就會減緩將新事件排入佇列中的速度。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-223">If the memory held by uncollected events reaches **LowThresholdOnObjects**, then WMI slows down the addition of new events into the queue.</span></span> <span data-ttu-id="8c9e9-224">如果未回收事件持續累積，而且當使用的記憶體是在 **HighThresholdOnEvents** 中的值時，就會達到 **MaxWaitOnEvents** 中傳遞事件的最大等待時間，WMI 不接受來自提供者的其他事件，並將 **WBEM \_ E \_ \_ 的 \_ 記憶體** 傳回給用戶端。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-224">If uncollected events continue to accumulate and the maximum wait to deliver events in **MaxWaitOnEvents** is reached while the memory used is at the value in **HighThresholdOnEvents**, WMI accepts no more events from providers and returns **WBEM\_E\_OUT\_OF\_MEMORY** to the clients.</span></span>

> [!Note]  
> <span data-ttu-id="8c9e9-225">節流只適用于永久事件取用者，因此當事件在 WMI 內部事件佇列中備份時，暫時取用者不應預期進行節流。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-225">Throttling is only done for Permanent Event consumers, so temporary consumers should not expect throttling when events get backed up in the WMI internal event queue.</span></span>

 

<span data-ttu-id="8c9e9-226">這個屬性會反映登錄機碼中的值。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-226">This property reflects the value in the registry key.</span></span>

<span data-ttu-id="8c9e9-227">**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **WBEM** \\ **\| 的用戶端物件上的高閾值 (B)**    </span><span class="sxs-lookup"><span data-stu-id="8c9e9-227">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM**\\    **CIMOM\|High Threshold On Client Objects (B)**</span></span>

</dd> <dt>

<span data-ttu-id="8c9e9-228">**InstallationDirectory**</span><span class="sxs-lookup"><span data-stu-id="8c9e9-228">**InstallationDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c9e9-229">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8c9e9-229">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c9e9-230">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8c9e9-230">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c9e9-231">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \| 安裝目錄" ) </span><span class="sxs-lookup"><span data-stu-id="8c9e9-231">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\|Installation Directory")</span></span>
</dt> </dl>

<span data-ttu-id="8c9e9-232">已安裝 WMI 軟體的目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-232">Directory path where the WMI software has been installed.</span></span> <span data-ttu-id="8c9e9-233">預設位置為 \\ System32 \\ Wbem。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-233">The default location is \\System32\\Wbem.</span></span>

<span data-ttu-id="8c9e9-234">這個屬性會反映登錄機碼中的值。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-234">This property reflects the value in the registry key.</span></span>

<span data-ttu-id="8c9e9-235">**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **WBEM \| 安裝目錄**</span><span class="sxs-lookup"><span data-stu-id="8c9e9-235">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM\|Installation Directory**</span></span>

</dd> <dt>

<span data-ttu-id="8c9e9-236">**LastStartupHeapPreallocation**</span><span class="sxs-lookup"><span data-stu-id="8c9e9-236">**LastStartupHeapPreallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c9e9-237">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8c9e9-237">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8c9e9-238">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8c9e9-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c9e9-239">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| LastStartupHeapPreallocation" ) ，[**單位**](../wmisdk/standard-qualifiers.md) ( "bytes" ) </span><span class="sxs-lookup"><span data-stu-id="8c9e9-239">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|LastStartupHeapPreallocation"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="8c9e9-240">WMI 在初始化期間所建立之預先配置堆積的大小。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-240">Size of the pre-allocated heap created by WMI during initialization.</span></span>

<span data-ttu-id="8c9e9-241">這個屬性會反映登錄機碼中的值。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-241">This property reflects the value in the registry key.</span></span>

<span data-ttu-id="8c9e9-242">**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **WBEM \| CIMOM \| LastStartupHeapPreallocation**</span><span class="sxs-lookup"><span data-stu-id="8c9e9-242">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM\|CIMOM\|LastStartupHeapPreallocation**</span></span>

</dd> <dt>

<span data-ttu-id="8c9e9-243">**LoggingDirectory**</span><span class="sxs-lookup"><span data-stu-id="8c9e9-243">**LoggingDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c9e9-244">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8c9e9-244">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c9e9-245">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8c9e9-245">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8c9e9-246">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| 記錄目錄" ) </span><span class="sxs-lookup"><span data-stu-id="8c9e9-246">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|Logging Directory")</span></span>
</dt> </dl>

<span data-ttu-id="8c9e9-247">目錄路徑，其中包含 WMI 系統記錄檔的位置。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-247">Directory path that contains the location of the WMI system log files.</span></span>

<span data-ttu-id="8c9e9-248">這個屬性會反映登錄機碼中的值。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-248">This property reflects the value in the registry key.</span></span>

<span data-ttu-id="8c9e9-249">**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **WBEM \| CIMOM \| 記錄目錄**</span><span class="sxs-lookup"><span data-stu-id="8c9e9-249">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM\|CIMOM\|Logging Directory**</span></span>

</dd> <dt>

<span data-ttu-id="8c9e9-250">**Logginglevel.information**</span><span class="sxs-lookup"><span data-stu-id="8c9e9-250">**LoggingLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c9e9-251">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8c9e9-251">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8c9e9-252">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8c9e9-252">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8c9e9-253">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| 記錄" ) </span><span class="sxs-lookup"><span data-stu-id="8c9e9-253">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|Logging")</span></span>
</dt> </dl>

<span data-ttu-id="8c9e9-254">啟用事件記錄和使用的記錄詳細程度。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-254">Enabling of event logging and the verbosity level of logging used.</span></span>

<span data-ttu-id="8c9e9-255">這個屬性會反映登錄機碼中的值。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-255">This property reflects the value in the registry key.</span></span>

<span data-ttu-id="8c9e9-256">**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **WBEM \| CIMOM \| 記錄**</span><span class="sxs-lookup"><span data-stu-id="8c9e9-256">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM\|CIMOM\|Logging**</span></span>

<dt>

<span id="Off"></span><span id="off"></span><span id="OFF"></span>

<span data-ttu-id="8c9e9-257">**Off** (0) </span><span class="sxs-lookup"><span data-stu-id="8c9e9-257">**Off** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Error_logging"></span><span id="error_logging"></span><span id="ERROR_LOGGING"></span>

<span data-ttu-id="8c9e9-258">**錯誤記錄** (1) </span><span class="sxs-lookup"><span data-stu-id="8c9e9-258">**Error logging** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Verbose_Error_logging"></span><span id="verbose_error_logging"></span><span id="VERBOSE_ERROR_LOGGING"></span>

<span data-ttu-id="8c9e9-259">**詳細的錯誤記錄** (2) </span><span class="sxs-lookup"><span data-stu-id="8c9e9-259">**Verbose Error logging** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8c9e9-260">**LowThresholdOnClientObjects**</span><span class="sxs-lookup"><span data-stu-id="8c9e9-260">**LowThresholdOnClientObjects**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c9e9-261">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8c9e9-261">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8c9e9-262">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8c9e9-262">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8c9e9-263">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ \| 的用戶端物件上的低臨界值" ) ，[**單位**](../wmisdk/standard-qualifiers.md) ( 「每秒的物件數」 ) </span><span class="sxs-lookup"><span data-stu-id="8c9e9-263">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|Low Threshold On Client Objects"), [**Units**](../wmisdk/standard-qualifiers.md) ("objects per second")</span></span>
</dt> </dl>

<span data-ttu-id="8c9e9-264">WMI 開始為用戶端建立的新物件建立速度變慢的速率。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-264">Rate at which WMI starts to slow the creation of new objects created for clients.</span></span> <span data-ttu-id="8c9e9-265">為了配合提供者與用戶端之間的速度差異，WMI 會將物件保留在佇列中，再將它們傳遞給取用者。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-265">To accommodate speed differentials between providers and clients, WMI holds objects in queues before delivering them to consumers.</span></span> <span data-ttu-id="8c9e9-266">為了提高效率，取用者必須以符合提供者的步調來收集物件。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-266">For more efficiency, consumers must collect the objects at a pace that matches the provider.</span></span> <span data-ttu-id="8c9e9-267">如果物件要求的速率達到 **LowThresholdOnClientObjects**，WMI 就會逐漸降低建立新物件的速度，以符合用戶端的使用率。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-267">If the rate of requests for objects reaches **LowThresholdOnClientObjects**, then WMI gradually slows down the creation of new objects to match the client's rate of use.</span></span> <span data-ttu-id="8c9e9-268">當建立物件的速率超過此屬性的值時，就會導致這個緩慢的啟動。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-268">This slowdown starts when the rate at which objects are being created exceeds the value of this property.</span></span> <span data-ttu-id="8c9e9-269">請參閱 **HighThresholdOnClientObjects**。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-269">See **HighThresholdOnClientObjects**.</span></span>

<span data-ttu-id="8c9e9-270">這個屬性會反映登錄值。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-270">This property reflects the registry value.</span></span>

<span data-ttu-id="8c9e9-271">**金鑰 \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **WBEM** \\ **\| 的用戶端物件上的高閾值 (B)**    </span><span class="sxs-lookup"><span data-stu-id="8c9e9-271">**KEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM**\\    **CIMOM\|High Threshold On Client Objects (B)**</span></span>

</dd> <dt>

<span data-ttu-id="8c9e9-272">**LowThresholdOnEvents**</span><span class="sxs-lookup"><span data-stu-id="8c9e9-272">**LowThresholdOnEvents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c9e9-273">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8c9e9-273">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8c9e9-274">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8c9e9-274">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8c9e9-275">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ \| ) 事件的低閾值"，[**單位**](../wmisdk/standard-qualifiers.md) ( 「每秒事件數」 ) </span><span class="sxs-lookup"><span data-stu-id="8c9e9-275">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|Low Threshold On Events"), [**Units**](../wmisdk/standard-qualifiers.md) ("events per second")</span></span>
</dt> </dl>

<span data-ttu-id="8c9e9-276">WMI 開始減緩新事件傳遞速度的速率。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-276">Rate at which WMI starts to slow the delivery of new events.</span></span> <span data-ttu-id="8c9e9-277">為了配合提供者與用戶端之間的速度差異，WMI 會將事件排入佇列，然後再傳遞給取用者。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-277">To accommodate speed differentials between providers and clients, WMI queues events before delivering them to consumers.</span></span> <span data-ttu-id="8c9e9-278">為了提高效率，取用者必須以符合提供者的步調來收集物件。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-278">For more efficiency, consumers must collect the objects at a pace that matches the provider.</span></span> <span data-ttu-id="8c9e9-279">如果佇列的控制權超出控制權，WMI 節流會使事件的傳遞逐漸下降，以符合用戶端的速率。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-279">If the queue grows out of control, WMI throttles—slows down—the delivery of events gradually to align with the client rate.</span></span> <span data-ttu-id="8c9e9-280">當產生事件的速率超過此屬性的值時，就會啟動此緩慢。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-280">This slowdown starts when the rate at which events are generated exceeds the value of this property.</span></span> <span data-ttu-id="8c9e9-281">請參閱 **HighThresholdOnEvents**。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-281">See **HighThresholdOnEvents**.</span></span>

> [!Note]  
> <span data-ttu-id="8c9e9-282">節流只適用于永久事件取用者，因此當事件在 WMI 內部事件佇列中備份時，暫時取用者不應預期進行節流。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-282">Throttling is only done for permanent event consumers, so temporary consumers should not expect throttling when events get backed up in the WMI internal event queue.</span></span>

 

<span data-ttu-id="8c9e9-283">這個屬性會反映登錄值。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-283">This property reflects the registry value.</span></span>

<span data-ttu-id="8c9e9-284">**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **WBEM** \\ **\| 在用戶端物件上的高閾值 {B}**    </span><span class="sxs-lookup"><span data-stu-id="8c9e9-284">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM**\\    **CIMOM\|High Threshold On Client Objects {B}**</span></span>

</dd> <dt>

<span data-ttu-id="8c9e9-285">**MaxLogFileSize**</span><span class="sxs-lookup"><span data-stu-id="8c9e9-285">**MaxLogFileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c9e9-286">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8c9e9-286">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8c9e9-287">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8c9e9-287">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8c9e9-288">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| 記錄檔大小上限」 ) ，[**單位**](../wmisdk/standard-qualifiers.md) ( 「位元組」 ) </span><span class="sxs-lookup"><span data-stu-id="8c9e9-288">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|Log File Max Size"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="8c9e9-289">WMI 服務所產生之記錄檔的大小上限。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-289">Maximum size of the log files produced by the WMI service.</span></span>

<span data-ttu-id="8c9e9-290">這個屬性會反映登錄機碼中的值。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-290">This property reflects the value in the registry key.</span></span>

<span data-ttu-id="8c9e9-291">**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **WBEM \| CIMOM \| 記錄檔大小上限**</span><span class="sxs-lookup"><span data-stu-id="8c9e9-291">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM\|CIMOM\|Log File Max Size**</span></span>

</dd> <dt>

<span data-ttu-id="8c9e9-292">**MaxWaitOnClientObjects**</span><span class="sxs-lookup"><span data-stu-id="8c9e9-292">**MaxWaitOnClientObjects**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c9e9-293">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8c9e9-293">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8c9e9-294">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8c9e9-294">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8c9e9-295">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ \| Events Max Wait" ) ，[**單位**](../wmisdk/standard-qualifiers.md) ( "毫秒" ) </span><span class="sxs-lookup"><span data-stu-id="8c9e9-295">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|Max Wait On Events"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="8c9e9-296">新建立的物件在捨棄之前等候用戶端使用的時間量，並傳回錯誤值。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-296">Amount of time a newly created object waits to be used by the client before it is discarded and an error value is returned.</span></span> <span data-ttu-id="8c9e9-297">這個屬性會與 **LowThresholdOnClientObjects** 和 **HighThresholdOnClientObjects** 屬性互動以進行節流：當取用者接收物件的速度太慢時，將物件傳遞給取用者。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-297">This property interacts with the **LowThresholdOnClientObjects** and **HighThresholdOnClientObjects** properties to throttle—slow down—the delivery of objects to consumers when the consumer is receiving the objects too slowly.</span></span>

</dd> <dt>

<span data-ttu-id="8c9e9-298">**MaxWaitOnEvents**</span><span class="sxs-lookup"><span data-stu-id="8c9e9-298">**MaxWaitOnEvents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c9e9-299">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8c9e9-299">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8c9e9-300">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8c9e9-300">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8c9e9-301">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ \| Events Max Wait" ) ，[**單位**](../wmisdk/standard-qualifiers.md) ( "毫秒" ) </span><span class="sxs-lookup"><span data-stu-id="8c9e9-301">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|Max Wait On Events"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="8c9e9-302">傳送至用戶端的事件在被捨棄之前排入佇列的時間量。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-302">Amount of time for which an event sent to a client is queued before being discarded.</span></span> <span data-ttu-id="8c9e9-303">這個屬性會使用 **LowThresholdOnEvents** 和 **HighThresholdOnEvents** 來進行節流處理—當取用者接收物件的速度太慢時，將物件傳遞給取用者的速度會變慢。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-303">This property interacts0 with **LowThresholdOnEvents** and **HighThresholdOnEvents** to throttle—slow down—the delivery of objects to consumers when the consumer is receiving the objects too slowly.</span></span>

<span data-ttu-id="8c9e9-304">這個屬性會反映登錄值。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-304">This property reflects the registry value.</span></span>

<span data-ttu-id="8c9e9-305">**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **WBEM** \\ **\| 的最大等候事件等候 (ms)**    </span><span class="sxs-lookup"><span data-stu-id="8c9e9-305">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM**\\    **CIMOM\|Max Wait On Events (ms)**</span></span>

</dd> <dt>

<span data-ttu-id="8c9e9-306">**MofSelfInstallDirectory**</span><span class="sxs-lookup"><span data-stu-id="8c9e9-306">**MofSelfInstallDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c9e9-307">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8c9e9-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c9e9-308">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8c9e9-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c9e9-309">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \| MOF Self-Install Directory" ) </span><span class="sxs-lookup"><span data-stu-id="8c9e9-309">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\|MOF Self-Install Directory")</span></span>
</dt> </dl>

<span data-ttu-id="8c9e9-310">將 MOF 檔案安裝到 WMI 存放庫的應用程式目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-310">Directory path for applications that install MOF files to the WMI repository.</span></span> <span data-ttu-id="8c9e9-311">WMI 會自動編譯放在此目錄中的任何 MOF 檔案，而且根據其成功與否，會將 MOF 移至標示為「良好」或「不良」的子目錄。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-311">WMI automatically compiles any MOF files placed in this directory and, depending on its success, moves the MOF to a subdirectory labeled good or bad.</span></span> <span data-ttu-id="8c9e9-312">如果包含 \# [pragma 自動](../wmisdk/pragma-autorecover.md) 復原命令，則完整檔案名會新增至 WMI 初始化或復原存放庫時所使用的 **AutorecoverMofs** 清單。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-312">If the \# [pragma autorecover](../wmisdk/pragma-autorecover.md) command is included, the fully qualified file name is added to the **AutorecoverMofs** list used when WMI is initializing or recovering the repository.</span></span> <span data-ttu-id="8c9e9-313">此清單決定編譯 Mof 的順序。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-313">The list determines the order in which MOFs are compiled.</span></span>

<span data-ttu-id="8c9e9-314">這個屬性會反映登錄機碼中的值。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-314">This property reflects the value in the registry key.</span></span>

<span data-ttu-id="8c9e9-315">**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **WBEM \| CIMOM \| MOF Self = 安裝目錄**</span><span class="sxs-lookup"><span data-stu-id="8c9e9-315">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM\|CIMOM\|MOF Self=Install Directory**</span></span>

</dd> <dt>

<span data-ttu-id="8c9e9-316">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="8c9e9-316">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c9e9-317">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8c9e9-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c9e9-318">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8c9e9-318">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c9e9-319">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) </span><span class="sxs-lookup"><span data-stu-id="8c9e9-319">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="8c9e9-320">已知目前物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-320">Identifier by which the current object is known.</span></span>

<span data-ttu-id="8c9e9-321">這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-321">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8c9e9-322">備註</span><span class="sxs-lookup"><span data-stu-id="8c9e9-322">Remarks</span></span>

<span data-ttu-id="8c9e9-323">**Win32 \_ WMISetting** 類別衍生自 [**CIM \_ 設定**](cim-setting.md)。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-323">The **Win32\_WMISetting** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span> <span data-ttu-id="8c9e9-324">電腦上只能有一個這個類別的實例。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-324">Only one instance of this class can exist on a computer.</span></span>

<span data-ttu-id="8c9e9-325">當您要對 WMI 服務本身的腳本或疑難排解問題進行疑難排解時，瞭解 WMI 在電腦上的設定方式可能會非常有用。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-325">Knowing how WMI is configured on a computer can be very useful when you are debugging scripts or troubleshooting problems with the WMI service itself.</span></span> <span data-ttu-id="8c9e9-326">例如，許多 WMI 腳本是以假設根 \\ cimv2 是目的電腦上的預設命名空間來撰寫的。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-326">For example, many WMI scripts are written under the assumption that root\\cimv2 is the default namespace on the target computer.</span></span> <span data-ttu-id="8c9e9-327">如此一來，需要存取「根 CIMv2」中類別的腳本寫入器 \\ 通常無法在 GetObject 標記中包含命名空間，如下列程式碼範例所示：</span><span class="sxs-lookup"><span data-stu-id="8c9e9-327">As a result, script writers who need to access a class in "Root\\CIMv2" often fail to include the namespace in the GetObject moniker, as shown in the following code sample:</span></span>

`Set colServices = GetObject("winmgmts:").ExecQuery ("SELECT * FROM Win32_Service")`

<span data-ttu-id="8c9e9-328">如果根 \\ cimv2 不是目的電腦上的預設命名空間，此腳本將會失敗。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-328">If root\\cimv2 is not the default namespace on the target computer, this script will fail.</span></span> <span data-ttu-id="8c9e9-329">為了避免發生這種情況，命名空間根 \\ cimv2 必須包含在標記中，如下列程式碼範例所示：</span><span class="sxs-lookup"><span data-stu-id="8c9e9-329">To prevent this from happening, the namespace root\\cimv2 must be included in the moniker, as shown in the following code sample:</span></span>

`Set colServices = GetObject("winmgmts:root\cimv2").ExecQuery("SELECT * FROM Win32_Service")`

<span data-ttu-id="8c9e9-330">如果目的電腦上的預設命名空間與腳本所假設的命名空間不同，腳本將會失敗。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-330">If the default namespace on the target computer is different from the namespace assumed by a script, the script will fail.</span></span> <span data-ttu-id="8c9e9-331">最重要的是，使用者會看到一些誤導的錯誤訊息「不正確類別」。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-331">On top of that, the user will be presented with the somewhat misleading error message "Invalid class."</span></span> <span data-ttu-id="8c9e9-332">老實說，失敗是因為類別無效，但因為在預設命名空間中找不到類別。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-332">In truth, the failure is not because the class is invalid but because the class cannot be found in the default namespace.</span></span> <span data-ttu-id="8c9e9-333">這是很難排解的問題，因為您可能會調查類別的可能問題，而不是使用 (的命名空間問題，而在此情況下未) 指定。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-333">This is a difficult problem to troubleshoot, because you are likely to investigate possible problems with the class rather than problems with the namespace that was (or, in this case, was not) specified.</span></span>

<span data-ttu-id="8c9e9-334">您可以使用 **Win32 \_ WMISetting** 類別來判斷電腦上 WMI 的設定方式。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-334">You can use the **Win32\_WMISetting** class to determine how WMI has been configured on a computer.</span></span> <span data-ttu-id="8c9e9-335">設定詳細資料（例如，預設命名空間或 WMI 組建編號）有助於疑難排解腳本問題。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-335">Configuration details such as the default namespace or the WMI build number can be useful in troubleshooting script problems.</span></span> <span data-ttu-id="8c9e9-336">這些設定也提供重要的系統管理資訊，例如，WMI 錯誤是否記錄在電腦上，以及如果您需要重建 WMI 存放庫，哪些 WMI 提供者會自動重載。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-336">These settings also provide important administrative information such as how, or even whether, WMI errors are logged on a computer and which WMI providers will automatically be reloaded if you need to rebuild the WMI repository.</span></span>

## <a name="examples"></a><span data-ttu-id="8c9e9-337">範例</span><span class="sxs-lookup"><span data-stu-id="8c9e9-337">Examples</span></span>

<span data-ttu-id="8c9e9-338">TechNet 資源庫上的 [修改 Wmi 設定](https://Gallery.TechNet.Microsoft.Com/aa80d174-3592-4fed-9c50-11f34e541445) VBScript 程式碼範例會 **使用 \_ Win32 WMISETTING** 類別來設定 WMI 備份間隔和記錄層級。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-338">The [Modify WMI Settings](https://Gallery.TechNet.Microsoft.Com/aa80d174-3592-4fed-9c50-11f34e541445) VBScript code example on the TechNet Gallery uses the **Win32\_WMISetting** class to configure the WMI backup interval and logging level.</span></span>

<span data-ttu-id="8c9e9-339">TechNet 資源庫上 [預設命名空間](https://Gallery.TechNet.Microsoft.Com/3fc69acd-ead0-4dd1-9ea1-e15a7331cfa0) VBScript 程式碼範例的清單，會使用 **Win32 \_ WMISetting** 類別來抓取和顯示目前的 WMI 「腳本的預設命名空間」設定。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-339">The [List the Default Namespace](https://Gallery.TechNet.Microsoft.Com/3fc69acd-ead0-4dd1-9ea1-e15a7331cfa0) VBScript code example on the TechNet Gallery uses the **Win32\_WMISetting** class to retrieve and display the current WMI "Default namespace for scripting" setting.</span></span>

<span data-ttu-id="8c9e9-340">TechNet 資源庫上的 [修改預設 Wmi 命名空間](https://Gallery.TechNet.Microsoft.Com/6dbb20e6-036d-43a2-ad6d-58325ada6a19) VBScript 程式碼範例會使用 **ASPScriptDefaultNamespace** 屬性，將 WMI 「腳本的預設命名空間」設定設為「根 \\ cimv2」。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-340">The [Modify the Default WMI Namespace](https://Gallery.TechNet.Microsoft.Com/6dbb20e6-036d-43a2-ad6d-58325ada6a19) VBScript code example on the TechNet Gallery uses the **ASPScriptDefaultNamespace** property to set the WMI "Default namespace for scripting" setting to "root\\cimv2".</span></span>

<span data-ttu-id="8c9e9-341">清單中的 [所有 Wmi 設定](https://Gallery.TechNet.Microsoft.Com/29c04301-e9b2-46d1-8714-2dbb51014c92) VBSCript 程式碼範例會使用 **Win32 \_ WMISetting** 上的許多屬性來傳回電腦上所設定的 wmi 設定清單。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-341">The [List All the WMI Settings](https://Gallery.TechNet.Microsoft.Com/29c04301-e9b2-46d1-8714-2dbb51014c92) VBSCript code example uses a number of properties on **Win32\_WMISetting** to return a list of WMI settings configured on a computer.</span></span>

<span data-ttu-id="8c9e9-342">[清單 Wmi 設定資訊](https://Gallery.TechNet.Microsoft.Com/0427cfde-4cd9-4a3d-9140-3bb622a1df5d)JavaScript 程式碼範例會在 **Win32 \_ WMISetting** 上使用一些屬性，以傳回電腦上所設定的 wmi 設定清單。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-342">The [List WMI Setting Information](https://Gallery.TechNet.Microsoft.Com/0427cfde-4cd9-4a3d-9140-3bb622a1df5d) JavaScript code example uses a number of properties on **Win32\_WMISetting** to return a list of WMI settings configured on a computer.</span></span>

<span data-ttu-id="8c9e9-343">[清單 Wmi 設定資訊](https://Gallery.TechNet.Microsoft.Com/370e7fbe-ea3c-4290-8a56-1e38519f518d)Python 程式碼範例會在 **Win32 \_ WMISetting** 上使用一些屬性，以傳回電腦上所設定的 wmi 設定清單。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-343">The [List WMI Setting Information](https://Gallery.TechNet.Microsoft.Com/370e7fbe-ea3c-4290-8a56-1e38519f518d) Python code example uses a number of properties on **Win32\_WMISetting** to return a list of WMI settings configured on a computer.</span></span>

<span data-ttu-id="8c9e9-344">[清單 WMI 設定資訊](https://Gallery.TechNet.Microsoft.Com/9309e4c5-2ca6-4662-9451-f1342d5171d2)物件 REXX 程式碼範例會使用 **Win32 \_ WMISetting** 上的一些屬性來傳回電腦上所設定的 wmi 設定清單。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-344">The [List WMI Setting Information](https://Gallery.TechNet.Microsoft.Com/9309e4c5-2ca6-4662-9451-f1342d5171d2) Object REXX code example uses a number of properties on **Win32\_WMISetting** to return a list of WMI settings configured on a computer.</span></span>

<span data-ttu-id="8c9e9-345">下列 VBScript 程式碼範例顯示如何取得在本機電腦上執行的 WMI 版本。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-345">The following VBScript code example shows how to obtain the version of WMI running on the local computer.</span></span> <span data-ttu-id="8c9e9-346">"Win32 \_ WMISetting = @" 表示類別的單一實例。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-346">The "Win32\_WMISetting=@" indicates the single instance of the class.</span></span> <span data-ttu-id="8c9e9-347">如需詳細資訊，請參閱 WMI 版本。</span><span class="sxs-lookup"><span data-stu-id="8c9e9-347">For more information, see WMI versions.</span></span>


```VB
set objWMIService = GetObject("winmgmts:{impersonationLevel=Impersonate}!/Root/CIMv2")

set objWMISetting = objWMIService.Get("Win32_WMISetting=@")

WScript.Echo  objWMISetting.BuildVersion
```



## <a name="requirements"></a><span data-ttu-id="8c9e9-348">規格需求</span><span class="sxs-lookup"><span data-stu-id="8c9e9-348">Requirements</span></span>



| <span data-ttu-id="8c9e9-349">需求</span><span class="sxs-lookup"><span data-stu-id="8c9e9-349">Requirement</span></span> | <span data-ttu-id="8c9e9-350">值</span><span class="sxs-lookup"><span data-stu-id="8c9e9-350">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8c9e9-351">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8c9e9-351">Minimum supported client</span></span><br/> | <span data-ttu-id="8c9e9-352">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8c9e9-352">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8c9e9-353">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8c9e9-353">Minimum supported server</span></span><br/> | <span data-ttu-id="8c9e9-354">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8c9e9-354">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8c9e9-355">命名空間</span><span class="sxs-lookup"><span data-stu-id="8c9e9-355">Namespace</span></span><br/>                | <span data-ttu-id="8c9e9-356">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="8c9e9-356">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8c9e9-357">MOF</span><span class="sxs-lookup"><span data-stu-id="8c9e9-357">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8c9e9-358"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="8c9e9-358"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8c9e9-359">DLL</span><span class="sxs-lookup"><span data-stu-id="8c9e9-359">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8c9e9-360"><dt>Wbemcore.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c9e9-360"><dt>Wbemcore.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c9e9-361">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8c9e9-361">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c9e9-362">**CIM \_ 設定**</span><span class="sxs-lookup"><span data-stu-id="8c9e9-362">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="8c9e9-363">WMI 服務管理類別</span><span class="sxs-lookup"><span data-stu-id="8c9e9-363">WMI Service Management Classes</span></span>](./wmi-service-management-classes.md)
</dt> </dl>

 

 
