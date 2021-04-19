---
description: Win32 \_ OSRecoveryConfiguration&\# 8194;WMI 類別代表當作業系統失敗時，將會從記憶體收集的資訊類型。 這包括開機失敗和系統損毀。
ms.assetid: 0c8a2aeb-2fd9-44b7-8f91-d19afb8d2de6
ms.tgt_platform: multiple
title: Win32_OSRecoveryConfiguration 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OSRecoveryConfiguration
- Win32_OSRecoveryConfiguration.Caption
- Win32_OSRecoveryConfiguration.Description
- Win32_OSRecoveryConfiguration.SettingID
- Win32_OSRecoveryConfiguration.AutoReboot
- Win32_OSRecoveryConfiguration.DebugFilePath
- Win32_OSRecoveryConfiguration.DebugInfoType
- Win32_OSRecoveryConfiguration.ExpandedDebugFilePath
- Win32_OSRecoveryConfiguration.ExpandedMiniDumpDirectory
- Win32_OSRecoveryConfiguration.KernelDumpOnly
- Win32_OSRecoveryConfiguration.MiniDumpDirectory
- Win32_OSRecoveryConfiguration.Name
- Win32_OSRecoveryConfiguration.OverwriteExistingDebugFile
- Win32_OSRecoveryConfiguration.SendAdminAlert
- Win32_OSRecoveryConfiguration.WriteDebugInfo
- Win32_OSRecoveryConfiguration.WriteToSystemLog
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e2371ba7ee449497e2d695e60d75c59454282d54
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106966642"
---
# <a name="win32_osrecoveryconfiguration-class"></a><span data-ttu-id="b8aa7-104">Win32 \_ OSRecoveryConfiguration 類別</span><span class="sxs-lookup"><span data-stu-id="b8aa7-104">Win32\_OSRecoveryConfiguration class</span></span>

<span data-ttu-id="b8aa7-105">**Win32 \_ OSRecoveryConfiguration** [WMI 類別](../wmisdk/retrieving-a-class.md)代表當作業系統失敗時，將會從記憶體收集的資訊類型。</span><span class="sxs-lookup"><span data-stu-id="b8aa7-105">The **Win32\_OSRecoveryConfiguration** [WMI class](../wmisdk/retrieving-a-class.md) represents the types of information that will be gathered from memory when the operating system fails.</span></span> <span data-ttu-id="b8aa7-106">這包括開機失敗和系統損毀。</span><span class="sxs-lookup"><span data-stu-id="b8aa7-106">This includes boot failures and system crashes.</span></span>

<span data-ttu-id="b8aa7-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="b8aa7-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="b8aa7-108">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="b8aa7-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8aa7-109">語法</span><span class="sxs-lookup"><span data-stu-id="b8aa7-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsUpdate, UUID("{8502C4E8-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_OSRecoveryConfiguration : CIM_Setting
{
  string  Caption;
  string  Description;
  string  SettingID;
  boolean AutoReboot;
  string  DebugFilePath;
  uint32  DebugInfoType;
  string  ExpandedDebugFilePath;
  string  ExpandedMiniDumpDirectory;
  boolean KernelDumpOnly;
  string  MiniDumpDirectory;
  string  Name;
  boolean OverwriteExistingDebugFile;
  boolean SendAdminAlert;
  boolean WriteDebugInfo;
  boolean WriteToSystemLog;
};
```

## <a name="members"></a><span data-ttu-id="b8aa7-110">成員</span><span class="sxs-lookup"><span data-stu-id="b8aa7-110">Members</span></span>

<span data-ttu-id="b8aa7-111">**Win32 \_ OSRecoveryConfiguration** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b8aa7-111">The **Win32\_OSRecoveryConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="b8aa7-112">屬性</span><span class="sxs-lookup"><span data-stu-id="b8aa7-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b8aa7-113">屬性</span><span class="sxs-lookup"><span data-stu-id="b8aa7-113">Properties</span></span>

<span data-ttu-id="b8aa7-114">**Win32 \_ OSRecoveryConfiguration** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="b8aa7-114">The **Win32\_OSRecoveryConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b8aa7-115">**AutoReboot**</span><span class="sxs-lookup"><span data-stu-id="b8aa7-115">**AutoReboot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8aa7-116">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="b8aa7-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b8aa7-117">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b8aa7-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b8aa7-118">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ CrashControl \| AutoReboot" ) </span><span class="sxs-lookup"><span data-stu-id="b8aa7-118">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\CrashControl\|AutoReboot")</span></span>
</dt> </dl>

<span data-ttu-id="b8aa7-119">系統會在復原操作期間自動重新開機。</span><span class="sxs-lookup"><span data-stu-id="b8aa7-119">System will automatically reboot during a recovery operation.</span></span>

</dd> <dt>

<span data-ttu-id="b8aa7-120">**標題**</span><span class="sxs-lookup"><span data-stu-id="b8aa7-120">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8aa7-121">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b8aa7-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8aa7-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b8aa7-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8aa7-123">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) </span><span class="sxs-lookup"><span data-stu-id="b8aa7-123">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="b8aa7-124">目前物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="b8aa7-124">Short textual description of the current object.</span></span>

<span data-ttu-id="b8aa7-125">這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。</span><span class="sxs-lookup"><span data-stu-id="b8aa7-125">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8aa7-126">**DebugFilePath**</span><span class="sxs-lookup"><span data-stu-id="b8aa7-126">**DebugFilePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8aa7-127">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b8aa7-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8aa7-128">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b8aa7-128">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b8aa7-129">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ CrashControl \| DumpFile" ) </span><span class="sxs-lookup"><span data-stu-id="b8aa7-129">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\CrashControl\|DumpFile")</span></span>
</dt> </dl>

<span data-ttu-id="b8aa7-130">Debug 檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="b8aa7-130">Full path to the debug file.</span></span> <span data-ttu-id="b8aa7-131">在電腦發生故障後，會建立具有電腦記憶體狀態的偵錯工具檔。</span><span class="sxs-lookup"><span data-stu-id="b8aa7-131">A debug file is created with the memory state of the computer after a computer failure.</span></span>

<span data-ttu-id="b8aa7-132">範例： "C： \\ Windows \\ Memory dmp"</span><span class="sxs-lookup"><span data-stu-id="b8aa7-132">Example: "C:\\Windows\\Memory.dmp"</span></span>

</dd> <dt>

<span data-ttu-id="b8aa7-133">**DebugInfoType**</span><span class="sxs-lookup"><span data-stu-id="b8aa7-133">**DebugInfoType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8aa7-134">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="b8aa7-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b8aa7-135">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b8aa7-135">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b8aa7-136">寫入至記錄檔的偵錯工具類型。</span><span class="sxs-lookup"><span data-stu-id="b8aa7-136">Type of debugging information written to the log file.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="b8aa7-137">**無** (0) </span><span class="sxs-lookup"><span data-stu-id="b8aa7-137">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Complete_memory_dump"></span><span id="complete_memory_dump"></span><span id="COMPLETE_MEMORY_DUMP"></span>

<span data-ttu-id="b8aa7-138">**完成記憶體傾印** (1) </span><span class="sxs-lookup"><span data-stu-id="b8aa7-138">**Complete memory dump** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Kernel_memory_dump"></span><span id="kernel_memory_dump"></span><span id="KERNEL_MEMORY_DUMP"></span>

<span data-ttu-id="b8aa7-139">**核心記憶體傾印** (2) </span><span class="sxs-lookup"><span data-stu-id="b8aa7-139">**Kernel memory dump** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Small_memory_dump"></span><span id="small_memory_dump"></span><span id="SMALL_MEMORY_DUMP"></span>

<span data-ttu-id="b8aa7-140">**小型記憶體傾印** (3) </span><span class="sxs-lookup"><span data-stu-id="b8aa7-140">**Small memory dump** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b8aa7-141">**說明**</span><span class="sxs-lookup"><span data-stu-id="b8aa7-141">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8aa7-142">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b8aa7-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8aa7-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b8aa7-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8aa7-144">目前物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="b8aa7-144">Textual description of the current object.</span></span>

<span data-ttu-id="b8aa7-145">這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。</span><span class="sxs-lookup"><span data-stu-id="b8aa7-145">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8aa7-146">**ExpandedDebugFilePath**</span><span class="sxs-lookup"><span data-stu-id="b8aa7-146">**ExpandedDebugFilePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8aa7-147">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b8aa7-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8aa7-148">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b8aa7-148">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b8aa7-149">**DebugFilePath** 屬性的擴充版本。</span><span class="sxs-lookup"><span data-stu-id="b8aa7-149">Expanded version of the **DebugFilePath** property.</span></span>

<span data-ttu-id="b8aa7-150">範例： "C： \\ Windows \\ Memory dmp"</span><span class="sxs-lookup"><span data-stu-id="b8aa7-150">Example: "C:\\Windows\\Memory.dmp"</span></span>

</dd> <dt>

<span data-ttu-id="b8aa7-151">**ExpandedMiniDumpDirectory**</span><span class="sxs-lookup"><span data-stu-id="b8aa7-151">**ExpandedMiniDumpDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8aa7-152">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b8aa7-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8aa7-153">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b8aa7-153">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b8aa7-154">**MiniDumpDirectory** 屬性的擴充版本。</span><span class="sxs-lookup"><span data-stu-id="b8aa7-154">Expanded version of the **MiniDumpDirectory** property.</span></span>

<span data-ttu-id="b8aa7-155">範例： "C： \\ Windows \\ 小型傾印"</span><span class="sxs-lookup"><span data-stu-id="b8aa7-155">Example: "C:\\Windows\\MiniDump"</span></span>

</dd> <dt>

<span data-ttu-id="b8aa7-156">**KernelDumpOnly**</span><span class="sxs-lookup"><span data-stu-id="b8aa7-156">**KernelDumpOnly**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8aa7-157">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="b8aa7-157">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b8aa7-158">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b8aa7-158">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b8aa7-159">限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ CrashControl \| KernelDumpOnly" ) </span><span class="sxs-lookup"><span data-stu-id="b8aa7-159">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\CrashControl\|KernelDumpOnly")</span></span>
</dt> </dl>

<span data-ttu-id="b8aa7-160">只有內核調試資訊會寫入至 debug 記錄檔。</span><span class="sxs-lookup"><span data-stu-id="b8aa7-160">Only kernel debug information will be written to the debug log file.</span></span> <span data-ttu-id="b8aa7-161">若 **為 TRUE**，則只有當系統失敗時，才會將核心的狀態寫入至檔案。</span><span class="sxs-lookup"><span data-stu-id="b8aa7-161">If **TRUE**, then only the state of the kernel is written to a file in the event of a system failure.</span></span> <span data-ttu-id="b8aa7-162">如果 **為 FALSE**，系統將會嘗試記錄記憶體的狀態，以及可在失敗時提供系統相關資訊的任何裝置。</span><span class="sxs-lookup"><span data-stu-id="b8aa7-162">If **FALSE**, the system will try to log the state of the memory, and any devices that can provide information about the system when it failed.</span></span>

</dd> <dt>

<span data-ttu-id="b8aa7-163">**MiniDumpDirectory**</span><span class="sxs-lookup"><span data-stu-id="b8aa7-163">**MiniDumpDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8aa7-164">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b8aa7-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8aa7-165">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b8aa7-165">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b8aa7-166">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ CrashControl \| MiniDumpDir" ) </span><span class="sxs-lookup"><span data-stu-id="b8aa7-166">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\CrashControl\|MiniDumpDir")</span></span>
</dt> </dl>

<span data-ttu-id="b8aa7-167">將記錄和累積小型記憶體傾印檔案的目錄。</span><span class="sxs-lookup"><span data-stu-id="b8aa7-167">Directory where small memory dump files will be recorded and accumulated.</span></span>

<span data-ttu-id="b8aa7-168">範例： "% systemRoot% \\ 小型傾印"</span><span class="sxs-lookup"><span data-stu-id="b8aa7-168">Example: "%systemRoot%\\MiniDump"</span></span>

</dd> <dt>

<span data-ttu-id="b8aa7-169">**名稱**</span><span class="sxs-lookup"><span data-stu-id="b8aa7-169">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8aa7-170">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b8aa7-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8aa7-171">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b8aa7-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8aa7-172">限定詞： [**key**](../wmisdk/key-qualifier.md)、 [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI" ) </span><span class="sxs-lookup"><span data-stu-id="b8aa7-172">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="b8aa7-173">識別此 **Win32 \_ OSRecoveryConfiguration** 類別實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="b8aa7-173">Identifying name for this instance of the **Win32\_OSRecoveryConfiguration** class.</span></span>

</dd> <dt>

<span data-ttu-id="b8aa7-174">**OverwriteExistingDebugFile**</span><span class="sxs-lookup"><span data-stu-id="b8aa7-174">**OverwriteExistingDebugFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8aa7-175">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="b8aa7-175">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b8aa7-176">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b8aa7-176">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b8aa7-177">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ CrashControl \| Overwrite" ) </span><span class="sxs-lookup"><span data-stu-id="b8aa7-177">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\CrashControl\|Overwrite")</span></span>
</dt> </dl>

<span data-ttu-id="b8aa7-178">新的 debug 檔案將會覆寫現有的檔案。</span><span class="sxs-lookup"><span data-stu-id="b8aa7-178">New debug file will overwrite an existing one.</span></span>

</dd> <dt>

<span data-ttu-id="b8aa7-179">**SendAdminAlert**</span><span class="sxs-lookup"><span data-stu-id="b8aa7-179">**SendAdminAlert**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8aa7-180">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="b8aa7-180">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b8aa7-181">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b8aa7-181">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b8aa7-182">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ CrashControl \| SendAlert" ) </span><span class="sxs-lookup"><span data-stu-id="b8aa7-182">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\CrashControl\|SendAlert")</span></span>
</dt> </dl>

<span data-ttu-id="b8aa7-183">當作業系統失敗時，會將警示訊息傳送給系統管理員。</span><span class="sxs-lookup"><span data-stu-id="b8aa7-183">Alert message will be sent to the system administrator in the event of an operating system failure.</span></span>

</dd> <dt>

<span data-ttu-id="b8aa7-184">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="b8aa7-184">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8aa7-185">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b8aa7-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8aa7-186">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b8aa7-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8aa7-187">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) </span><span class="sxs-lookup"><span data-stu-id="b8aa7-187">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="b8aa7-188">已知目前物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b8aa7-188">Identifier by which the current object is known.</span></span>

<span data-ttu-id="b8aa7-189">這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。</span><span class="sxs-lookup"><span data-stu-id="b8aa7-189">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8aa7-190">**WriteDebugInfo**</span><span class="sxs-lookup"><span data-stu-id="b8aa7-190">**WriteDebugInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8aa7-191">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="b8aa7-191">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b8aa7-192">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b8aa7-192">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b8aa7-193">限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ CrashControl \| CrashDumpEnabled" ) </span><span class="sxs-lookup"><span data-stu-id="b8aa7-193">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\CrashControl\|CrashDumpEnabled")</span></span>
</dt> </dl>

<span data-ttu-id="b8aa7-194">偵錯工具資訊會寫入記錄檔。</span><span class="sxs-lookup"><span data-stu-id="b8aa7-194">Debugging information is to be written to a log file.</span></span>

</dd> <dt>

<span data-ttu-id="b8aa7-195">**WriteToSystemLog**</span><span class="sxs-lookup"><span data-stu-id="b8aa7-195">**WriteToSystemLog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8aa7-196">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="b8aa7-196">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b8aa7-197">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b8aa7-197">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b8aa7-198">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ CrashControl \| LogEvent" ) </span><span class="sxs-lookup"><span data-stu-id="b8aa7-198">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\CrashControl\|LogEvent")</span></span>
</dt> </dl>

<span data-ttu-id="b8aa7-199">事件會寫入系統記錄檔中。</span><span class="sxs-lookup"><span data-stu-id="b8aa7-199">Events will be written to a system log.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b8aa7-200">備註</span><span class="sxs-lookup"><span data-stu-id="b8aa7-200">Remarks</span></span>

<span data-ttu-id="b8aa7-201">**Win32 \_ OSRecoveryConfiguration** 類別衍生自 [**CIM \_ 設定**](cim-setting.md)。</span><span class="sxs-lookup"><span data-stu-id="b8aa7-201">The **Win32\_OSRecoveryConfiguration** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b8aa7-202">規格需求</span><span class="sxs-lookup"><span data-stu-id="b8aa7-202">Requirements</span></span>



| <span data-ttu-id="b8aa7-203">需求</span><span class="sxs-lookup"><span data-stu-id="b8aa7-203">Requirement</span></span> | <span data-ttu-id="b8aa7-204">值</span><span class="sxs-lookup"><span data-stu-id="b8aa7-204">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b8aa7-205">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b8aa7-205">Minimum supported client</span></span><br/> | <span data-ttu-id="b8aa7-206">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b8aa7-206">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b8aa7-207">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b8aa7-207">Minimum supported server</span></span><br/> | <span data-ttu-id="b8aa7-208">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b8aa7-208">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b8aa7-209">命名空間</span><span class="sxs-lookup"><span data-stu-id="b8aa7-209">Namespace</span></span><br/>                | <span data-ttu-id="b8aa7-210">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="b8aa7-210">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b8aa7-211">MOF</span><span class="sxs-lookup"><span data-stu-id="b8aa7-211">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b8aa7-212"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="b8aa7-212"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b8aa7-213">DLL</span><span class="sxs-lookup"><span data-stu-id="b8aa7-213">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8aa7-214"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8aa7-214"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8aa7-215">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b8aa7-215">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8aa7-216">**CIM \_ 設定**</span><span class="sxs-lookup"><span data-stu-id="b8aa7-216">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="b8aa7-217">作業系統類別</span><span class="sxs-lookup"><span data-stu-id="b8aa7-217">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
