---
description: Win32 \_ BOOTCONFIGURATION WMI 類別代表執行 Windows 之電腦系統的開機設定。
ms.assetid: c2db28dd-3feb-44bb-a532-c91cab980ba3
ms.tgt_platform: multiple
title: Win32_BootConfiguration 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BootConfiguration
- Win32_BootConfiguration.Caption
- Win32_BootConfiguration.Description
- Win32_BootConfiguration.SettingID
- Win32_BootConfiguration.BootDirectory
- Win32_BootConfiguration.ConfigurationPath
- Win32_BootConfiguration.LastDrive
- Win32_BootConfiguration.Name
- Win32_BootConfiguration.ScratchDirectory
- Win32_BootConfiguration.TempDirectory
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 556688d7c80038f04dd5b94b7c61c5d6dfef3199
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973179"
---
# <a name="win32_bootconfiguration-class"></a><span data-ttu-id="7f401-103">Win32 \_ BootConfiguration 類別</span><span class="sxs-lookup"><span data-stu-id="7f401-103">Win32\_BootConfiguration class</span></span>

<span data-ttu-id="7f401-104">**Win32 \_ BootConfiguration** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)代表執行 Windows 之電腦系統的開機設定。</span><span class="sxs-lookup"><span data-stu-id="7f401-104">The **Win32\_BootConfiguration** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the boot configuration of a computer system running Windows.</span></span>

<span data-ttu-id="7f401-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="7f401-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="7f401-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="7f401-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f401-107">語法</span><span class="sxs-lookup"><span data-stu-id="7f401-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4E2-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_BootConfiguration : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  string BootDirectory;
  string ConfigurationPath;
  string LastDrive;
  string Name;
  string ScratchDirectory;
  string TempDirectory;
};
```

## <a name="members"></a><span data-ttu-id="7f401-108">成員</span><span class="sxs-lookup"><span data-stu-id="7f401-108">Members</span></span>

<span data-ttu-id="7f401-109">**Win32 \_ BootConfiguration** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="7f401-109">The **Win32\_BootConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="7f401-110">屬性</span><span class="sxs-lookup"><span data-stu-id="7f401-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7f401-111">屬性</span><span class="sxs-lookup"><span data-stu-id="7f401-111">Properties</span></span>

<span data-ttu-id="7f401-112">**Win32 \_ BootConfiguration** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="7f401-112">The **Win32\_BootConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7f401-113">**BootDirectory**</span><span class="sxs-lookup"><span data-stu-id="7f401-113">**BootDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f401-114">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7f401-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f401-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f401-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f401-116">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| 進程和執行緒函數 \| [**GetEnvironmentVariable**](/windows/desktop/api/winbase/nf-winbase-getenvironmentvariable) \| WinBootDir" ) </span><span class="sxs-lookup"><span data-stu-id="7f401-116">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Process and Thread Functions\|[**GetEnvironmentVariable**](/windows/desktop/api/winbase/nf-winbase-getenvironmentvariable)\|WinBootDir")</span></span>
</dt> </dl>

<span data-ttu-id="7f401-117">啟動系統所需之系統檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="7f401-117">Path to the system files required for booting the system.</span></span>

<span data-ttu-id="7f401-118">範例： "C： \\ Windows"</span><span class="sxs-lookup"><span data-stu-id="7f401-118">Example: "C:\\Windows"</span></span>

</dd> <dt>

<span data-ttu-id="7f401-119">**標題**</span><span class="sxs-lookup"><span data-stu-id="7f401-119">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f401-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7f401-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f401-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f401-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f401-122">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="7f401-122">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="7f401-123">目前物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="7f401-123">Short textual description of the current object.</span></span>

<span data-ttu-id="7f401-124">這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。</span><span class="sxs-lookup"><span data-stu-id="7f401-124">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="7f401-125">**ConfigurationPath**</span><span class="sxs-lookup"><span data-stu-id="7f401-125">**ConfigurationPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f401-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7f401-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f401-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f401-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f401-128">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| 進程和執行緒函數 \| [**GetEnvironmentVariable**](/windows/desktop/api/winbase/nf-winbase-getenvironmentvariable) \| WinBootDir" ) </span><span class="sxs-lookup"><span data-stu-id="7f401-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Process and Thread Functions\|[**GetEnvironmentVariable**](/windows/desktop/api/winbase/nf-winbase-getenvironmentvariable)\|WinBootDir")</span></span>
</dt> </dl>

<span data-ttu-id="7f401-129">設定檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="7f401-129">Path to the configuration files.</span></span> <span data-ttu-id="7f401-130">這個值可能類似 **BootDirectory** 屬性中的值。</span><span class="sxs-lookup"><span data-stu-id="7f401-130">This value may be similar to the value in the **BootDirectory** property.</span></span>

</dd> <dt>

<span data-ttu-id="7f401-131">**說明**</span><span class="sxs-lookup"><span data-stu-id="7f401-131">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f401-132">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7f401-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f401-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f401-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f401-134">目前物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="7f401-134">Textual description of the current object.</span></span>

<span data-ttu-id="7f401-135">這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。</span><span class="sxs-lookup"><span data-stu-id="7f401-135">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="7f401-136">**LastDrive**</span><span class="sxs-lookup"><span data-stu-id="7f401-136">**LastDrive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f401-137">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7f401-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f401-138">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f401-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f401-139">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| File 函數 \| GetDriveType" ) </span><span class="sxs-lookup"><span data-stu-id="7f401-139">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Functions\|GetDriveType")</span></span>
</dt> </dl>

<span data-ttu-id="7f401-140">指派實體磁片磁碟機的最後一個磁碟機號。</span><span class="sxs-lookup"><span data-stu-id="7f401-140">Last drive letter to which a physical drive is assigned.</span></span>

<span data-ttu-id="7f401-141">範例： "E："</span><span class="sxs-lookup"><span data-stu-id="7f401-141">Example: "E:"</span></span>

</dd> <dt>

<span data-ttu-id="7f401-142">**名稱**</span><span class="sxs-lookup"><span data-stu-id="7f401-142">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f401-143">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7f401-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f401-144">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f401-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f401-145">限定詞： [**key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI" ) </span><span class="sxs-lookup"><span data-stu-id="7f401-145">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="7f401-146">開機設定的名稱。</span><span class="sxs-lookup"><span data-stu-id="7f401-146">Name of the boot configuration.</span></span> <span data-ttu-id="7f401-147">它是開機設定的識別碼。</span><span class="sxs-lookup"><span data-stu-id="7f401-147">It is an identifier for the boot configuration.</span></span>

</dd> <dt>

<span data-ttu-id="7f401-148">**ScratchDirectory**</span><span class="sxs-lookup"><span data-stu-id="7f401-148">**ScratchDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f401-149">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7f401-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f401-150">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f401-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f401-151">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| File 函數 \| GetTempPath" ) </span><span class="sxs-lookup"><span data-stu-id="7f401-151">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Functions\|GetTempPath")</span></span>
</dt> </dl>

<span data-ttu-id="7f401-152">暫存檔案可在開機期間存放的目錄。</span><span class="sxs-lookup"><span data-stu-id="7f401-152">Directory where temporary files can reside during boot time.</span></span>

</dd> <dt>

<span data-ttu-id="7f401-153">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="7f401-153">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f401-154">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7f401-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f401-155">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f401-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f401-156">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="7f401-156">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="7f401-157">已知目前物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="7f401-157">Identifier by which the current object is known.</span></span>

<span data-ttu-id="7f401-158">這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。</span><span class="sxs-lookup"><span data-stu-id="7f401-158">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="7f401-159">**TempDirectory**</span><span class="sxs-lookup"><span data-stu-id="7f401-159">**TempDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f401-160">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7f401-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f401-161">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7f401-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f401-162">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| File 函數 \| GetTempPath" ) </span><span class="sxs-lookup"><span data-stu-id="7f401-162">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Functions\|GetTempPath")</span></span>
</dt> </dl>

<span data-ttu-id="7f401-163">儲存暫存檔案的目錄。</span><span class="sxs-lookup"><span data-stu-id="7f401-163">Directory where temporary files are stored.</span></span>

<span data-ttu-id="7f401-164">範例： "C： \\ TEMP"</span><span class="sxs-lookup"><span data-stu-id="7f401-164">Example: "C:\\TEMP"</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7f401-165">備註</span><span class="sxs-lookup"><span data-stu-id="7f401-165">Remarks</span></span>

<span data-ttu-id="7f401-166">**Win32 \_ BootConfiguration** 類別衍生自 [**CIM \_ 設定**](cim-setting.md)。</span><span class="sxs-lookup"><span data-stu-id="7f401-166">The **Win32\_BootConfiguration** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

## <a name="examples"></a><span data-ttu-id="7f401-167">範例</span><span class="sxs-lookup"><span data-stu-id="7f401-167">Examples</span></span>

<span data-ttu-id="7f401-168">電腦 Perl 範例的 [開機設定屬性清單](https://Gallery.TechNet.Microsoft.Com/55c35de3-bb6a-47f0-89f9-d2c49ab4cf19) 會傳回電腦的開機設定資訊。</span><span class="sxs-lookup"><span data-stu-id="7f401-168">The [List the Boot Configuration Properties of a Computer](https://Gallery.TechNet.Microsoft.Com/55c35de3-bb6a-47f0-89f9-d2c49ab4cf19) Perl sample returns boot configuration information for a computer.</span></span>

<span data-ttu-id="7f401-169">下列 VBScript 範例會傳回電腦的開機設定資訊。</span><span class="sxs-lookup"><span data-stu-id="7f401-169">The following VBScript sample returns boot configuration information for a computer.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colItems = objWMIService.ExecQuery("Select * from Win32_BootConfiguration") 
 
For Each objItem in colItems 
    Wscript.Echo "Boot Directory: " & objItem.BootDirectory 
    Wscript.Echo "Configuration Path: " & objItem.ConfigurationPath 
    Wscript.Echo "Description: " & objItem.Description 
    Wscript.Echo "Last Drive: " & objItem.LastDrive 
    Wscript.Echo "Name: " & objItem.Name 
    Wscript.Echo "Scratch Directory: " & objItem.ScratchDirectory 
    Wscript.Echo "Setting ID: " & objItem.SettingID 
    Wscript.Echo "Temp Directory: " & objItem.TempDirectory 
Next 
```



<span data-ttu-id="7f401-170">下列程式碼範例將示範如何使用 **Win32 \_ BootConfiguration** WMI 類別。</span><span class="sxs-lookup"><span data-stu-id="7f401-170">The following code sample demonstrates the use of the **Win32\_BootConfiguration** WMI class.</span></span>


```PowerShell
# Get Boot configuration from WMI

$boot = Get-WMIObject Win32_BootConfiguration

# Display information

"Boot Directory     : {0}" -f $boot.bootdirectory
"Caption            : {0}" -f $boot.caption
"Description        : {0}" -f $boot.description
"Last Drive         : {0}" -f $boot.lastdrive
"Scratch Directory  : {0}" -f $boot.scratchdirectory
"Temp Directory     : {0}" -f $boot.tempdirectory

```



<span data-ttu-id="7f401-171">先前的程式碼範例會建立下列輸出：</span><span class="sxs-lookup"><span data-stu-id="7f401-171">The previous code sample creates the following output:</span></span>

``` syntax
Boot Directory     : \WINDOWS
Caption            : \Device\Harddisk0\Partition1
Description        : \Device\Harddisk0\Partition1
Last Drive         : K:
Scratch Directory  : C:\WINDOWS\system32\config\systemprofile\Local Settings\Temp
Temp Directory     : C:\WINDOWS\system32\config\systemprofile\Local Settings\Temp
```

## <a name="requirements"></a><span data-ttu-id="7f401-172">規格需求</span><span class="sxs-lookup"><span data-stu-id="7f401-172">Requirements</span></span>



| <span data-ttu-id="7f401-173">需求</span><span class="sxs-lookup"><span data-stu-id="7f401-173">Requirement</span></span> | <span data-ttu-id="7f401-174">值</span><span class="sxs-lookup"><span data-stu-id="7f401-174">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7f401-175">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7f401-175">Minimum supported client</span></span><br/> | <span data-ttu-id="7f401-176">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7f401-176">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7f401-177">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7f401-177">Minimum supported server</span></span><br/> | <span data-ttu-id="7f401-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7f401-178">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7f401-179">命名空間</span><span class="sxs-lookup"><span data-stu-id="7f401-179">Namespace</span></span><br/>                | <span data-ttu-id="7f401-180">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="7f401-180">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7f401-181">MOF</span><span class="sxs-lookup"><span data-stu-id="7f401-181">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7f401-182"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="7f401-182"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7f401-183">DLL</span><span class="sxs-lookup"><span data-stu-id="7f401-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7f401-184"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f401-184"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f401-185">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7f401-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f401-186">**CIM \_ 設定**</span><span class="sxs-lookup"><span data-stu-id="7f401-186">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

<span data-ttu-id="7f401-187">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7f401-187">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

