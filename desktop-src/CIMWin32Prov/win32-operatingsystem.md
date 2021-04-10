---
description: 代表安裝在電腦上的 Windows 作業系統。
ms.assetid: eb6a8cff-20a0-4211-b46a-3084e9c39246
ms.tgt_platform: multiple
title: Win32_OperatingSystem 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystem
- Win32_OperatingSystem.BootDevice
- Win32_OperatingSystem.BuildNumber
- Win32_OperatingSystem.BuildType
- Win32_OperatingSystem.Caption
- Win32_OperatingSystem.CodeSet
- Win32_OperatingSystem.CountryCode
- Win32_OperatingSystem.CreationClassName
- Win32_OperatingSystem.CSCreationClassName
- Win32_OperatingSystem.CSDVersion
- Win32_OperatingSystem.CSName
- Win32_OperatingSystem.CurrentTimeZone
- Win32_OperatingSystem.DataExecutionPrevention_Available
- Win32_OperatingSystem.DataExecutionPrevention_32BitApplications
- Win32_OperatingSystem.DataExecutionPrevention_Drivers
- Win32_OperatingSystem.DataExecutionPrevention_SupportPolicy
- Win32_OperatingSystem.Debug
- Win32_OperatingSystem.Description
- Win32_OperatingSystem.Distributed
- Win32_OperatingSystem.EncryptionLevel
- Win32_OperatingSystem.ForegroundApplicationBoost
- Win32_OperatingSystem.FreePhysicalMemory
- Win32_OperatingSystem.FreeSpaceInPagingFiles
- Win32_OperatingSystem.FreeVirtualMemory
- Win32_OperatingSystem.InstallDate
- Win32_OperatingSystem.LargeSystemCache
- Win32_OperatingSystem.LastBootUpTime
- Win32_OperatingSystem.LocalDateTime
- Win32_OperatingSystem.Locale
- Win32_OperatingSystem.Manufacturer
- Win32_OperatingSystem.MaxNumberOfProcesses
- Win32_OperatingSystem.MaxProcessMemorySize
- Win32_OperatingSystem.MUILanguages
- Win32_OperatingSystem.Name
- Win32_OperatingSystem.NumberOfLicensedUsers
- Win32_OperatingSystem.NumberOfProcesses
- Win32_OperatingSystem.NumberOfUsers
- Win32_OperatingSystem.OperatingSystemSKU
- Win32_OperatingSystem.Organization
- Win32_OperatingSystem.OSArchitecture
- Win32_OperatingSystem.OSLanguage
- Win32_OperatingSystem.OSProductSuite
- Win32_OperatingSystem.OSType
- Win32_OperatingSystem.OtherTypeDescription
- Win32_OperatingSystem.PAEEnabled
- Win32_OperatingSystem.PlusProductID
- Win32_OperatingSystem.PlusVersionNumber
- Win32_OperatingSystem.PortableOperatingSystem
- Win32_OperatingSystem.Primary
- Win32_OperatingSystem.ProductType
- Win32_OperatingSystem.RegisteredUser
- Win32_OperatingSystem.SerialNumber
- Win32_OperatingSystem.ServicePackMajorVersion
- Win32_OperatingSystem.ServicePackMinorVersion
- Win32_OperatingSystem.SizeStoredInPagingFiles
- Win32_OperatingSystem.Status
- Win32_OperatingSystem.SuiteMask
- Win32_OperatingSystem.SystemDevice
- Win32_OperatingSystem.SystemDirectory
- Win32_OperatingSystem.SystemDrive
- Win32_OperatingSystem.TotalSwapSpaceSize
- Win32_OperatingSystem.TotalVirtualMemorySize
- Win32_OperatingSystem.TotalVisibleMemorySize
- Win32_OperatingSystem.Version
- Win32_OperatingSystem.WindowsDirectory
- Win32_OperatingSystem.QuantumLength
- Win32_OperatingSystem.QuantumType
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 15a6a1bf7bec8c830d1a15ec690b01ec9ea22e48
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191014"
---
# <a name="win32_operatingsystem-class"></a><span data-ttu-id="fffbd-103">Win32 \_ 作業系統類別</span><span class="sxs-lookup"><span data-stu-id="fffbd-103">Win32\_OperatingSystem class</span></span>

<span data-ttu-id="fffbd-104">**Win32 \_ 作業系統** [WMI 類別](../wmisdk/retrieving-a-class.md)代表安裝在電腦上的 Windows 作業系統。</span><span class="sxs-lookup"><span data-stu-id="fffbd-104">The **Win32\_OperatingSystem** [WMI class](../wmisdk/retrieving-a-class.md) represents a Windows-based operating system installed on a computer.</span></span>

<span data-ttu-id="fffbd-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="fffbd-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="fffbd-106">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="fffbd-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="fffbd-107">語法</span><span class="sxs-lookup"><span data-stu-id="fffbd-107">Syntax</span></span>

``` syntax
[Singleton, Dynamic, Provider("CIMWin32"), SupportsUpdate, UUID("{8502C4DE-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_OperatingSystem : CIM_OperatingSystem
{
  string   BootDevice;
  string   BuildNumber;
  string   BuildType;
  string   Caption;
  string   CodeSet;
  string   CountryCode;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSDVersion;
  string   CSName;
  sint16   CurrentTimeZone;
  boolean  DataExecutionPrevention_Available;
  boolean  DataExecutionPrevention_32BitApplications;
  boolean  DataExecutionPrevention_Drivers;
  uint8    DataExecutionPrevention_SupportPolicy;
  boolean  Debug;
  string   Description;
  boolean  Distributed;
  uint32   EncryptionLevel;
  uint8    ForegroundApplicationBoost = 2;
  uint64   FreePhysicalMemory;
  uint64   FreeSpaceInPagingFiles;
  uint64   FreeVirtualMemory;
  datetime InstallDate;
  uint32   LargeSystemCache;
  datetime LastBootUpTime;
  datetime LocalDateTime;
  string   Locale;
  string   Manufacturer;
  uint32   MaxNumberOfProcesses;
  uint64   MaxProcessMemorySize;
  string   MUILanguages[];
  string   Name;
  uint32   NumberOfLicensedUsers;
  uint32   NumberOfProcesses;
  uint32   NumberOfUsers;
  uint32   OperatingSystemSKU;
  string   Organization;
  string   OSArchitecture;
  uint32   OSLanguage;
  uint32   OSProductSuite;
  uint16   OSType;
  string   OtherTypeDescription;
  Boolean  PAEEnabled;
  string   PlusProductID;
  string   PlusVersionNumber;
  boolean  PortableOperatingSystem;
  boolean  Primary;
  uint32   ProductType;
  string   RegisteredUser;
  string   SerialNumber;
  uint16   ServicePackMajorVersion;
  uint16   ServicePackMinorVersion;
  uint64   SizeStoredInPagingFiles;
  string   Status;
  uint32   SuiteMask;
  string   SystemDevice;
  string   SystemDirectory;
  string   SystemDrive;
  uint64   TotalSwapSpaceSize;
  uint64   TotalVirtualMemorySize;
  uint64   TotalVisibleMemorySize;
  string   Version;
  string   WindowsDirectory;
  uint8    QuantumLength;
  uint8    QuantumType;
};
```

## <a name="members"></a><span data-ttu-id="fffbd-108">成員</span><span class="sxs-lookup"><span data-stu-id="fffbd-108">Members</span></span>

<span data-ttu-id="fffbd-109">**Win32 \_ 作業系統** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="fffbd-109">The **Win32\_OperatingSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="fffbd-110">方法</span><span class="sxs-lookup"><span data-stu-id="fffbd-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="fffbd-111">屬性</span><span class="sxs-lookup"><span data-stu-id="fffbd-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="fffbd-112">方法</span><span class="sxs-lookup"><span data-stu-id="fffbd-112">Methods</span></span>

<span data-ttu-id="fffbd-113">**Win32 \_ 作業系統** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="fffbd-113">The **Win32\_OperatingSystem** class has these methods.</span></span>



| <span data-ttu-id="fffbd-114">方法</span><span class="sxs-lookup"><span data-stu-id="fffbd-114">Method</span></span>                                                                                     | <span data-ttu-id="fffbd-115">描述</span><span class="sxs-lookup"><span data-stu-id="fffbd-115">Description</span></span>                                                                                                                                                                                                                                                            |
|:-------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fffbd-116">**重新啟動**</span><span class="sxs-lookup"><span data-stu-id="fffbd-116">**Reboot**</span></span>](reboot-method-in-class-win32-operatingsystem.md)                             | <span data-ttu-id="fffbd-117">關機後再重新開機電腦系統。</span><span class="sxs-lookup"><span data-stu-id="fffbd-117">Shuts down and then restarts the computer system.</span></span><br/>                                                                                                                                                                                                           |
| [<span data-ttu-id="fffbd-118">**SetDateTime**</span><span class="sxs-lookup"><span data-stu-id="fffbd-118">**SetDateTime**</span></span>](setdatetime-method-in-class-win32-operatingsystem.md)                   | <span data-ttu-id="fffbd-119">允許設定電腦日期和時間。</span><span class="sxs-lookup"><span data-stu-id="fffbd-119">Allows the computer date and time to be set.</span></span><br/>                                                                                                                                                                                                                |
| [<span data-ttu-id="fffbd-120">**關閉**</span><span class="sxs-lookup"><span data-stu-id="fffbd-120">**Shutdown**</span></span>](shutdown-method-in-class-win32-operatingsystem.md)                         | <span data-ttu-id="fffbd-121">將程式和 Dll 卸載至關閉電腦的安全點。</span><span class="sxs-lookup"><span data-stu-id="fffbd-121">Unloads programs and DLLs to the point where it is safe to turn off the computer.</span></span><br/>                                                                                                                                                                           |
| [<span data-ttu-id="fffbd-122">**Win32Shutdown**</span><span class="sxs-lookup"><span data-stu-id="fffbd-122">**Win32Shutdown**</span></span>](win32shutdown-method-in-class-win32-operatingsystem.md)               | <span data-ttu-id="fffbd-123">提供 Windows 作業系統所支援的一組完整關機選項。</span><span class="sxs-lookup"><span data-stu-id="fffbd-123">Provides the full set of shutdown options supported by Windows operating systems.</span></span><br/>                                                                                                                                                                           |
| [<span data-ttu-id="fffbd-124">**Win32ShutdownTracker**</span><span class="sxs-lookup"><span data-stu-id="fffbd-124">**Win32ShutdownTracker**</span></span>](win32shutdowntracker-method-in-class-win32-operatingsystem.md) | <span data-ttu-id="fffbd-125">提供 **Win32 \_ 作業系統** 中 [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md)方法所支援的相同關機選項組，但也可讓您指定批註、關機原因或超時。</span><span class="sxs-lookup"><span data-stu-id="fffbd-125">Provides the same set of shutdown options supported by the [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) method in **Win32\_OperatingSystem**, but also allows you to specify comments, a reason for shutdown, or a timeout.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="fffbd-126">屬性</span><span class="sxs-lookup"><span data-stu-id="fffbd-126">Properties</span></span>

<span data-ttu-id="fffbd-127">**Win32 \_ 作業系統** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="fffbd-127">The **Win32\_OperatingSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fffbd-128">**BootDevice**</span><span class="sxs-lookup"><span data-stu-id="fffbd-128">**BootDevice**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fffbd-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fffbd-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fffbd-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-131">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| DRIVE \_ MAP \_ INFO \| btInt13Unit" ) </span><span class="sxs-lookup"><span data-stu-id="fffbd-131">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|DRIVE\_MAP\_INFO\|btInt13Unit")</span></span>
</dt> </dl>

<span data-ttu-id="fffbd-132">Windows 作業系統啟動所在之磁片磁碟機的名稱。</span><span class="sxs-lookup"><span data-stu-id="fffbd-132">Name of the disk drive from which the Windows operating system starts.</span></span>

<span data-ttu-id="fffbd-133">範例： " \\ \\ Device \\ Harddisk0"</span><span class="sxs-lookup"><span data-stu-id="fffbd-133">Example: "\\\\Device\\Harddisk0"</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-134">**BuildNumber**</span><span class="sxs-lookup"><span data-stu-id="fffbd-134">**BuildNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fffbd-135">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fffbd-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fffbd-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-137">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| 系統資訊結構 \| [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) \| dwBuildNumber" ) </span><span class="sxs-lookup"><span data-stu-id="fffbd-137">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|System Information Structures\|[**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa)\|dwBuildNumber")</span></span>
</dt> </dl>

<span data-ttu-id="fffbd-138">作業系統的組建編號。</span><span class="sxs-lookup"><span data-stu-id="fffbd-138">Build number of an operating system.</span></span> <span data-ttu-id="fffbd-139">它可用於比產品發行版本號碼更精確的版本資訊。</span><span class="sxs-lookup"><span data-stu-id="fffbd-139">It can be used for more precise version information than product release version numbers.</span></span>

<span data-ttu-id="fffbd-140">範例： "1381"</span><span class="sxs-lookup"><span data-stu-id="fffbd-140">Example: "1381"</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-141">**BuildType**</span><span class="sxs-lookup"><span data-stu-id="fffbd-141">**BuildType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fffbd-142">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fffbd-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fffbd-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-144">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \| CurrentType" ) </span><span class="sxs-lookup"><span data-stu-id="fffbd-144">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\Windows\\\\CurrentVersion\|CurrentType")</span></span>
</dt> </dl>

<span data-ttu-id="fffbd-145">用於作業系統的組建類型。</span><span class="sxs-lookup"><span data-stu-id="fffbd-145">Type of build used for an operating system.</span></span>

<span data-ttu-id="fffbd-146">範例： "" retail build ""、"checked build" "</span><span class="sxs-lookup"><span data-stu-id="fffbd-146">Examples: ""retail build"", ""checked build""</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-147">**標題**</span><span class="sxs-lookup"><span data-stu-id="fffbd-147">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fffbd-148">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fffbd-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-149">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fffbd-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-150">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="fffbd-150">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="fffbd-151">物件的簡短描述（單行字串）。</span><span class="sxs-lookup"><span data-stu-id="fffbd-151">Short description of the object—a one-line string.</span></span> <span data-ttu-id="fffbd-152">字串包含作業系統版本。</span><span class="sxs-lookup"><span data-stu-id="fffbd-152">The string includes the operating system version.</span></span> <span data-ttu-id="fffbd-153">例如「Microsoft Windows 7 企業版」。</span><span class="sxs-lookup"><span data-stu-id="fffbd-153">For example, "Microsoft Windows 7 Enterprise ".</span></span> <span data-ttu-id="fffbd-154">這個屬性可以當地語系化。</span><span class="sxs-lookup"><span data-stu-id="fffbd-154">This property can be localized.</span></span>

<span data-ttu-id="fffbd-155">**Windows Vista 和 windows 7：** 這個屬性可包含尾端的字元。</span><span class="sxs-lookup"><span data-stu-id="fffbd-155">**Windows Vista and Windows 7:** This property may contain trailing characters.</span></span> <span data-ttu-id="fffbd-156">例如，包含的字串 "Microsoft Windows 7 企業版" (尾端空格) 可能需要使用這個屬性來取得資訊。</span><span class="sxs-lookup"><span data-stu-id="fffbd-156">For example, the string "Microsoft Windows 7 Enterprise " (trailing space included) may be necessary to retrieve information using this property.</span></span>

<span data-ttu-id="fffbd-157">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="fffbd-157">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-158">**CodeSet**</span><span class="sxs-lookup"><span data-stu-id="fffbd-158">**CodeSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fffbd-159">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fffbd-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-160">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fffbd-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-161">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (6) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API language \| Language Support 函數 \| [**GetLocaleInfo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa) \| LOCALE \_ IDEFAULTANSICODEPAGE" ) </span><span class="sxs-lookup"><span data-stu-id="fffbd-161">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (6), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|National Language Support Functions\|[**GetLocaleInfo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa)\|LOCALE\_IDEFAULTANSICODEPAGE")</span></span>
</dt> </dl>

<span data-ttu-id="fffbd-162">作業系統所使用的字碼頁值。</span><span class="sxs-lookup"><span data-stu-id="fffbd-162">Code page value an operating system uses.</span></span> <span data-ttu-id="fffbd-163">字碼頁包含作業系統用來轉譯不同語言之字串的字元資料表。</span><span class="sxs-lookup"><span data-stu-id="fffbd-163">A code page contains a character table that an operating system uses to translate strings for different languages.</span></span> <span data-ttu-id="fffbd-164">美國國家標準局 (ANSI) 會列出代表已定義字碼頁的值。</span><span class="sxs-lookup"><span data-stu-id="fffbd-164">The American National Standards Institute (ANSI) lists values that represent defined code pages.</span></span> <span data-ttu-id="fffbd-165">如果作業系統未使用 ANSI 字碼頁，此成員會設定為 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="fffbd-165">If an operating system does not use an ANSI code page, this member is set to 0 (zero).</span></span> <span data-ttu-id="fffbd-166">**CodeSet** 字串最多可以使用六個字元來定義字碼頁值。</span><span class="sxs-lookup"><span data-stu-id="fffbd-166">The **CodeSet** string can use a maximum of six characters to define the code page value.</span></span>

<span data-ttu-id="fffbd-167">範例： "1255"</span><span class="sxs-lookup"><span data-stu-id="fffbd-167">Example: "1255"</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-168">**CountryCode**</span><span class="sxs-lookup"><span data-stu-id="fffbd-168">**CountryCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fffbd-169">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fffbd-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-170">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fffbd-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-171">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| 國家語言支援函式 \| [**GetLocaleInfo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa) \| LOCALE \_ ICOUNTRY" ) </span><span class="sxs-lookup"><span data-stu-id="fffbd-171">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|National Language Support Functions\|[**GetLocaleInfo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa)\|LOCALE\_ICOUNTRY")</span></span>
</dt> </dl>

<span data-ttu-id="fffbd-172">作業系統使用的國家/地區代碼。</span><span class="sxs-lookup"><span data-stu-id="fffbd-172">Code for the country/region that an operating system uses.</span></span> <span data-ttu-id="fffbd-173">值是以國際電話撥號首碼為基礎，也稱為 IBM 國家/地區代碼。</span><span class="sxs-lookup"><span data-stu-id="fffbd-173">Values are based on international phone dialing prefixes—also referred to as IBM country/region codes.</span></span> <span data-ttu-id="fffbd-174">這個屬性可以使用最多六個字元來定義國家/地區代碼值。</span><span class="sxs-lookup"><span data-stu-id="fffbd-174">This property can use a maximum of six characters to define the country/region code value.</span></span>

<span data-ttu-id="fffbd-175">範例： "1" (美國) </span><span class="sxs-lookup"><span data-stu-id="fffbd-175">Example: "1" (United States)</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-176">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="fffbd-176">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fffbd-177">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fffbd-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-178">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fffbd-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-179">限定詞： [**CIM \_ 金鑰**](../wmisdk/standard-wmi-qualifiers.md)， [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) </span><span class="sxs-lookup"><span data-stu-id="fffbd-179">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="fffbd-180">第一個具象類別的名稱，這個類別會出現在建立實例時所用的繼承鏈中。</span><span class="sxs-lookup"><span data-stu-id="fffbd-180">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="fffbd-181">搭配類別的其他索引鍵屬性使用時，此屬性可讓這個類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="fffbd-181">When used with other key properties of the class, this property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="fffbd-182">這個屬性繼承自 [**CIM \_ 作業系統**](cim-operatingsystem.md)。</span><span class="sxs-lookup"><span data-stu-id="fffbd-182">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-183">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="fffbd-183">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fffbd-184">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fffbd-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-185">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fffbd-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-186">限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_**](cim-computersystem.md)未執行」。**CreationClassName**") ， [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md)， [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) </span><span class="sxs-lookup"><span data-stu-id="fffbd-186">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="fffbd-187">範圍電腦系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="fffbd-187">Creation class name of the scoping computer system.</span></span>

<span data-ttu-id="fffbd-188">這個屬性繼承自 [**CIM \_ 作業系統**](cim-operatingsystem.md)。</span><span class="sxs-lookup"><span data-stu-id="fffbd-188">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-189">**CSDVersion**</span><span class="sxs-lookup"><span data-stu-id="fffbd-189">**CSDVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fffbd-190">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fffbd-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-191">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fffbd-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-192">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| 系統資訊結構 \| [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) \| **szCSDVersion**" ) </span><span class="sxs-lookup"><span data-stu-id="fffbd-192">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|System Information Structures\|[**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa)\|**szCSDVersion**")</span></span>
</dt> </dl>

<span data-ttu-id="fffbd-193">以 **Null** 終止的字串，表示電腦上所安裝的最新 service pack。</span><span class="sxs-lookup"><span data-stu-id="fffbd-193">**NULL**-terminated string that indicates the latest service pack installed on a computer.</span></span> <span data-ttu-id="fffbd-194">如果未安裝 service pack，則字串為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="fffbd-194">If no service pack is installed, the string is **NULL**.</span></span>

<span data-ttu-id="fffbd-195">範例： "Service Pack 3"</span><span class="sxs-lookup"><span data-stu-id="fffbd-195">Example: "Service Pack 3"</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-196">**CSName**</span><span class="sxs-lookup"><span data-stu-id="fffbd-196">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fffbd-197">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fffbd-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-198">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fffbd-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-199">限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_**](cim-computersystem.md)未執行」。**Name**") 、 [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md)、 [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) </span><span class="sxs-lookup"><span data-stu-id="fffbd-199">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="fffbd-200">範圍電腦系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="fffbd-200">Name of the scoping computer system.</span></span>

<span data-ttu-id="fffbd-201">這個屬性繼承自 [**CIM \_ 作業系統**](cim-operatingsystem.md)。</span><span class="sxs-lookup"><span data-stu-id="fffbd-201">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-202">**CurrentTimeZone**</span><span class="sxs-lookup"><span data-stu-id="fffbd-202">**CurrentTimeZone**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fffbd-203">資料類型： **sint16**</span><span class="sxs-lookup"><span data-stu-id="fffbd-203">Data type: **sint16**</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-204">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fffbd-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-205">限定詞： [**單位**](../wmisdk/standard-qualifiers.md) ( "分鐘" ) </span><span class="sxs-lookup"><span data-stu-id="fffbd-205">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="fffbd-206">以分鐘為單位的作業系統與格林尼治平均時間 (GMT) 的位移。</span><span class="sxs-lookup"><span data-stu-id="fffbd-206">Number, in minutes, an operating system is offset from Greenwich mean time (GMT).</span></span> <span data-ttu-id="fffbd-207">此數位為正數、負數或零。</span><span class="sxs-lookup"><span data-stu-id="fffbd-207">The number is positive, negative, or zero.</span></span>

<span data-ttu-id="fffbd-208">這個屬性繼承自 [**CIM \_ 作業系統**](cim-operatingsystem.md)。</span><span class="sxs-lookup"><span data-stu-id="fffbd-208">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-209">**DataExecutionPrevention \_ 32BitApplications**</span><span class="sxs-lookup"><span data-stu-id="fffbd-209">**DataExecutionPrevention\_32BitApplications**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fffbd-210">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="fffbd-210">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-211">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fffbd-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-212">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI" ) </span><span class="sxs-lookup"><span data-stu-id="fffbd-212">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="fffbd-213">當資料執行防止硬體功能可供使用時，此屬性會指出該功能已設定為適用于32位應用程式（如果 **為 True**）。</span><span class="sxs-lookup"><span data-stu-id="fffbd-213">When the data execution prevention hardware feature is available, this property indicates that the feature is set to work for 32-bit applications if **True**.</span></span> <span data-ttu-id="fffbd-214">在64位的電腦上，資料執行防止功能是在 [開機設定資料 (BCD)](/previous-versions/windows/desktop/bcd/boot-configuration-data-portal) 存放區中設定，而且 **Win32 \_ 作業系統** 中的屬性會據以進行設定。</span><span class="sxs-lookup"><span data-stu-id="fffbd-214">On 64-bit computers, the data execution prevention feature is configured in the [Boot Configuration Data (BCD)](/previous-versions/windows/desktop/bcd/boot-configuration-data-portal) store and the properties in **Win32\_OperatingSystem** are set accordingly.</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-215">**DataExecutionPrevention \_ 可用**</span><span class="sxs-lookup"><span data-stu-id="fffbd-215">**DataExecutionPrevention\_Available**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fffbd-216">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="fffbd-216">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-217">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fffbd-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-218">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI" ) </span><span class="sxs-lookup"><span data-stu-id="fffbd-218">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="fffbd-219">「資料執行防止」是一項硬體功能，可在資料類型記憶體頁面上停止執行程式碼，以防止緩衝區溢位的攻擊。</span><span class="sxs-lookup"><span data-stu-id="fffbd-219">Data execution prevention is a hardware feature to prevent buffer overrun attacks by stopping the execution of code on data-type memory pages.</span></span> <span data-ttu-id="fffbd-220">若 **為 True**，則可使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="fffbd-220">If **True**, then this feature is available.</span></span> <span data-ttu-id="fffbd-221">在64位的電腦上，會在 BCD 存放區中設定資料執行防止功能，並據此設定 **Win32 \_ 作業系統** 中的屬性。</span><span class="sxs-lookup"><span data-stu-id="fffbd-221">On 64-bit computers, the data execution prevention feature is configured in the BCD store and the properties in **Win32\_OperatingSystem** are set accordingly.</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-222">**DataExecutionPrevention \_ 驅動程式**</span><span class="sxs-lookup"><span data-stu-id="fffbd-222">**DataExecutionPrevention\_Drivers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fffbd-223">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="fffbd-223">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-224">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fffbd-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-225">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI" ) </span><span class="sxs-lookup"><span data-stu-id="fffbd-225">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="fffbd-226">當資料執行防止硬體功能可供使用時，此屬性會指出該功能已設定為適用于驅動程式（如果 **為 True**）。</span><span class="sxs-lookup"><span data-stu-id="fffbd-226">When the data execution prevention hardware feature is available, this property indicates that the feature is set to work for drivers if **True**.</span></span> <span data-ttu-id="fffbd-227">在64位的電腦上，會在 BCD 存放區中設定資料執行防止功能，並據此設定 **Win32 \_ 作業系統** 中的屬性。</span><span class="sxs-lookup"><span data-stu-id="fffbd-227">On 64-bit computers, the data execution prevention feature is configured in the BCD store and the properties in **Win32\_OperatingSystem** are set accordingly.</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-228">**DataExecutionPrevention \_ SupportPolicy**</span><span class="sxs-lookup"><span data-stu-id="fffbd-228">**DataExecutionPrevention\_SupportPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fffbd-229">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="fffbd-229">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-230">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fffbd-230">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-231">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI" ) </span><span class="sxs-lookup"><span data-stu-id="fffbd-231">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="fffbd-232">指出套用 (DEP) 設定的資料執行防止。</span><span class="sxs-lookup"><span data-stu-id="fffbd-232">Indicates which Data Execution Prevention (DEP) setting is applied.</span></span> <span data-ttu-id="fffbd-233">DEP 設定會指定 DEP 套用至系統上32位應用程式的範圍。</span><span class="sxs-lookup"><span data-stu-id="fffbd-233">The DEP setting specifies the extent to which DEP applies to 32-bit applications on the system.</span></span> <span data-ttu-id="fffbd-234">DEP 一律會套用至 Windows 核心。</span><span class="sxs-lookup"><span data-stu-id="fffbd-234">DEP is always applied to the Windows kernel.</span></span>

<dt>

<span id="Always_Off"></span><span id="always_off"></span><span id="ALWAYS_OFF"></span>

<span data-ttu-id="fffbd-235"><span id="Always_Off"></span><span id="always_off"></span><span id="ALWAYS_OFF"></span>**一律關閉** (0) </span><span class="sxs-lookup"><span data-stu-id="fffbd-235"><span id="Always_Off"></span><span id="always_off"></span><span id="ALWAYS_OFF"></span>**Always Off** (0)</span></span>


</dt> <dd>

<span data-ttu-id="fffbd-236">電腦上所有32位應用程式的 DEP 都會關閉，且不會發生例外狀況。</span><span class="sxs-lookup"><span data-stu-id="fffbd-236">DEP is turned off for all 32-bit applications on the computer with no exceptions.</span></span> <span data-ttu-id="fffbd-237">使用者介面無法使用此設定。</span><span class="sxs-lookup"><span data-stu-id="fffbd-237">This setting is not available for the user interface.</span></span>

</dd> <dt>

<span id="Always_On"></span><span id="always_on"></span><span id="ALWAYS_ON"></span>

<span data-ttu-id="fffbd-238"><span id="Always_On"></span><span id="always_on"></span><span id="ALWAYS_ON"></span>**Always On** (1) </span><span class="sxs-lookup"><span data-stu-id="fffbd-238"><span id="Always_On"></span><span id="always_on"></span><span id="ALWAYS_ON"></span>**Always On** (1)</span></span>


</dt> <dd>

<span data-ttu-id="fffbd-239">電腦上的所有32位應用程式都已啟用 DEP。</span><span class="sxs-lookup"><span data-stu-id="fffbd-239">DEP is enabled for all 32-bit applications on the computer.</span></span> <span data-ttu-id="fffbd-240">使用者介面無法使用此設定。</span><span class="sxs-lookup"><span data-stu-id="fffbd-240">This setting is not available for the user interface.</span></span>

</dd> <dt>

<span id="Opt_In"></span><span id="opt_in"></span><span id="OPT_IN"></span>

<span data-ttu-id="fffbd-241"><span id="Opt_In"></span><span id="opt_in"></span><span id="OPT_IN"></span>**加入宣告** (2) </span><span class="sxs-lookup"><span data-stu-id="fffbd-241"><span id="Opt_In"></span><span id="opt_in"></span><span id="OPT_IN"></span>**Opt In** (2)</span></span>


</dt> <dd>

<span data-ttu-id="fffbd-242">DEP 已啟用有限的二進位檔、核心和所有 Windows 服務的數目。</span><span class="sxs-lookup"><span data-stu-id="fffbd-242">DEP is enabled for a limited number of binaries, the kernel, and all Windows-based services.</span></span> <span data-ttu-id="fffbd-243">不過，它預設會針對所有32位應用程式關閉。</span><span class="sxs-lookup"><span data-stu-id="fffbd-243">However, it is off by default for all 32-bit applications.</span></span> <span data-ttu-id="fffbd-244">使用者或系統管理員必須明確選擇 **Always On** 或選擇 **退出** 設定，才能將 DEP 套用至32位應用程式。</span><span class="sxs-lookup"><span data-stu-id="fffbd-244">A user or administrator must explicitly choose either the **Always On** or the **Opt Out** setting before DEP can be applied to 32-bit applications.</span></span>

</dd> <dt>

<span id="Opt_Out"></span><span id="opt_out"></span><span id="OPT_OUT"></span>

<span data-ttu-id="fffbd-245"><span id="Opt_Out"></span><span id="opt_out"></span><span id="OPT_OUT"></span>**退出** (3) </span><span class="sxs-lookup"><span data-stu-id="fffbd-245"><span id="Opt_Out"></span><span id="opt_out"></span><span id="OPT_OUT"></span>**Opt Out** (3)</span></span>


</dt> <dd>

<span data-ttu-id="fffbd-246">預設會針對所有32位應用程式啟用 DEP。</span><span class="sxs-lookup"><span data-stu-id="fffbd-246">DEP is enabled by default for all 32-bit applications.</span></span> <span data-ttu-id="fffbd-247">使用者或系統管理員可以將應用程式新增至例外狀況清單，以明確移除32位應用程式的支援。</span><span class="sxs-lookup"><span data-stu-id="fffbd-247">A user or administrator can explicitly remove support for a 32-bit application by adding the application to an exceptions list.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="fffbd-248">**偵錯**</span><span class="sxs-lookup"><span data-stu-id="fffbd-248">**Debug**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fffbd-249">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="fffbd-249">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-250">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fffbd-250">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-251">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) \| SM \_ DEBUG" ) </span><span class="sxs-lookup"><span data-stu-id="fffbd-251">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|[**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics)\|SM\_DEBUG")</span></span>
</dt> </dl>

<span data-ttu-id="fffbd-252">作業系統是已檢查的 () 組建的偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="fffbd-252">Operating system is a checked (debug) build.</span></span> <span data-ttu-id="fffbd-253">若 **為 True**，則會安裝偵錯工具版本。</span><span class="sxs-lookup"><span data-stu-id="fffbd-253">If **True**, the debugging version is installed.</span></span> <span data-ttu-id="fffbd-254">已檢查的組建提供錯誤檢查、引數驗證和系統偵錯工具代碼。</span><span class="sxs-lookup"><span data-stu-id="fffbd-254">Checked builds provide error checking, argument verification, and system debugging code.</span></span> <span data-ttu-id="fffbd-255">已檢查二進位檔中的其他程式碼會產生內核偵錯工具錯誤訊息，並中斷偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="fffbd-255">Additional code in a checked binary generates a kernel debugger error message and breaks into the debugger.</span></span> <span data-ttu-id="fffbd-256">這有助於立即判斷錯誤的原因和位置。</span><span class="sxs-lookup"><span data-stu-id="fffbd-256">This helps immediately determine the cause and location of the error.</span></span> <span data-ttu-id="fffbd-257">由於執行的額外程式碼，效能可能會受到已檢查組建的影響。</span><span class="sxs-lookup"><span data-stu-id="fffbd-257">Performance may be affected in a checked build due to the additional code that is executed.</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-258">**說明**</span><span class="sxs-lookup"><span data-stu-id="fffbd-258">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fffbd-259">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fffbd-259">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-260">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="fffbd-260">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-261">限定詞：覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "Description" ) ， [**MAPPINGSTRINGS**](../wmisdk/standard-qualifiers.md) ( "WMI" ) </span><span class="sxs-lookup"><span data-stu-id="fffbd-261">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Description"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="fffbd-262">Windows 作業系統的描述。</span><span class="sxs-lookup"><span data-stu-id="fffbd-262">Description of the Windows operating system.</span></span> <span data-ttu-id="fffbd-263">某些使用者介面（例如允許編輯此描述的使用者介面）會將其長度限制為48個字元。</span><span class="sxs-lookup"><span data-stu-id="fffbd-263">Some user interfaces for example, those that allow editing of this description, limit its length to 48 characters.</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-264">**分散式**</span><span class="sxs-lookup"><span data-stu-id="fffbd-264">**Distributed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fffbd-265">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="fffbd-265">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-266">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fffbd-266">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fffbd-267">若 **為 True**，則會將作業系統分散到數個電腦系統節點。</span><span class="sxs-lookup"><span data-stu-id="fffbd-267">If **True**, the operating system is distributed across several computer system nodes.</span></span> <span data-ttu-id="fffbd-268">如果是，則應該將這些節點分組為叢集。</span><span class="sxs-lookup"><span data-stu-id="fffbd-268">If so, these nodes should be grouped as a cluster.</span></span>

<span data-ttu-id="fffbd-269">這個屬性繼承自 [**CIM \_ 作業系統**](cim-operatingsystem.md)。</span><span class="sxs-lookup"><span data-stu-id="fffbd-269">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-270">**EncryptionLevel**</span><span class="sxs-lookup"><span data-stu-id="fffbd-270">**EncryptionLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fffbd-271">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="fffbd-271">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-272">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fffbd-272">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fffbd-273">安全交易的加密層級：40位、128位或 *n* 位。</span><span class="sxs-lookup"><span data-stu-id="fffbd-273">Encryption level for secure transactions: 40-bit, 128-bit, or *n*-bit.</span></span>

<dt>

<span id="40-bit"></span><span id="40-BIT"></span>

<span data-ttu-id="fffbd-274">**40** 位 (0) </span><span class="sxs-lookup"><span data-stu-id="fffbd-274">**40-bit** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="128-bit"></span><span id="128-BIT"></span>

<span data-ttu-id="fffbd-275">**128** 位 (1) </span><span class="sxs-lookup"><span data-stu-id="fffbd-275">**128-bit** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="n-bit"></span><span id="N-BIT"></span>

<span data-ttu-id="fffbd-276">**n 位** (2) </span><span class="sxs-lookup"><span data-stu-id="fffbd-276">**n-bit** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="fffbd-277">**ForegroundApplicationBoost**</span><span class="sxs-lookup"><span data-stu-id="fffbd-277">**ForegroundApplicationBoost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fffbd-278">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="fffbd-278">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-279">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="fffbd-279">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-280">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ PriorityControl \| Win32PrioritySeparation" ) </span><span class="sxs-lookup"><span data-stu-id="fffbd-280">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\PriorityControl\|Win32PrioritySeparation")</span></span>
</dt> </dl>

<span data-ttu-id="fffbd-281">提高優先順序會給予前景應用程式。</span><span class="sxs-lookup"><span data-stu-id="fffbd-281">Increase in priority is given to the foreground application.</span></span> <span data-ttu-id="fffbd-282">應用程式提升的執行方式，是讓應用程式更多的執行時間配量 (量子長度) 。</span><span class="sxs-lookup"><span data-stu-id="fffbd-282">Application boost is implemented by giving an application more execution time slices (quantum lengths).</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="fffbd-283"><span id="None"></span><span id="none"></span><span id="NONE"></span>**無** (0) </span><span class="sxs-lookup"><span data-stu-id="fffbd-283"><span id="None"></span><span id="none"></span><span id="NONE"></span>**None** (0)</span></span>


</dt> <dd>

<span data-ttu-id="fffbd-284">系統會將量子長度提升為6。</span><span class="sxs-lookup"><span data-stu-id="fffbd-284">The system boosts the quantum length by 6.</span></span>

</dd> <dt>

<span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>

<span data-ttu-id="fffbd-285"><span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>**最小** (1) </span><span class="sxs-lookup"><span data-stu-id="fffbd-285"><span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>**Minimum** (1)</span></span>


</dt> <dd>

<span data-ttu-id="fffbd-286">系統會將量子長度提高12。</span><span class="sxs-lookup"><span data-stu-id="fffbd-286">The system boosts the quantum length by 12.</span></span>

</dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

<span data-ttu-id="fffbd-287"><span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**最大** (2) </span><span class="sxs-lookup"><span data-stu-id="fffbd-287"><span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Maximum** (2)</span></span>


</dt> <dd>

<span data-ttu-id="fffbd-288">系統會將量子長度提高18。</span><span class="sxs-lookup"><span data-stu-id="fffbd-288">The system boosts the quantum length by 18.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="fffbd-289">**FreePhysicalMemory**</span><span class="sxs-lookup"><span data-stu-id="fffbd-289">**FreePhysicalMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fffbd-290">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="fffbd-290">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-291">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fffbd-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-292">限定詞： [**單位**](../wmisdk/standard-qualifiers.md) ( "kb" ) </span><span class="sxs-lookup"><span data-stu-id="fffbd-292">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="fffbd-293">目前未使用且可用的實體記憶體數目（以 kb 為單位）。</span><span class="sxs-lookup"><span data-stu-id="fffbd-293">Number, in kilobytes, of physical memory currently unused and available.</span></span>

<span data-ttu-id="fffbd-294">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="fffbd-294">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="fffbd-295">這個屬性繼承自 [**CIM \_ 作業系統**](cim-operatingsystem.md)。</span><span class="sxs-lookup"><span data-stu-id="fffbd-295">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-296">**FreeSpaceInPagingFiles**</span><span class="sxs-lookup"><span data-stu-id="fffbd-296">**FreeSpaceInPagingFiles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fffbd-297">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="fffbd-297">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-298">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fffbd-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-299">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 系統記憶體設定 \| 001.4 ") ， [**單位**](../wmisdk/standard-qualifiers.md) (" kb ") </span><span class="sxs-lookup"><span data-stu-id="fffbd-299">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|System Memory Settings\|001.4"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="fffbd-300">可以對應到作業系統分頁檔的數位（以 kb 為單位），而不會造成其他任何頁面交換。</span><span class="sxs-lookup"><span data-stu-id="fffbd-300">Number, in kilobytes, that can be mapped into the operating system paging files without causing any other pages to be swapped out.</span></span>

<span data-ttu-id="fffbd-301">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="fffbd-301">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="fffbd-302">這個屬性繼承自 [**CIM \_ 作業系統**](cim-operatingsystem.md)。</span><span class="sxs-lookup"><span data-stu-id="fffbd-302">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-303">**FreeVirtualMemory**</span><span class="sxs-lookup"><span data-stu-id="fffbd-303">**FreeVirtualMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fffbd-304">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="fffbd-304">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-305">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fffbd-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-306">限定詞： [**單位**](../wmisdk/standard-qualifiers.md) ( "kb" ) </span><span class="sxs-lookup"><span data-stu-id="fffbd-306">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="fffbd-307">目前未使用且可用的虛擬記憶體數目（以 kb 為單位）。</span><span class="sxs-lookup"><span data-stu-id="fffbd-307">Number, in kilobytes, of virtual memory currently unused and available.</span></span>

<span data-ttu-id="fffbd-308">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="fffbd-308">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="fffbd-309">這個屬性繼承自 [**CIM \_ 作業系統**](cim-operatingsystem.md)。</span><span class="sxs-lookup"><span data-stu-id="fffbd-309">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-310">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="fffbd-310">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fffbd-311">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="fffbd-311">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-312">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fffbd-312">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-313">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](../wmisdk/standard-qualifiers.md) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="fffbd-313">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="fffbd-314">已安裝日期物件。</span><span class="sxs-lookup"><span data-stu-id="fffbd-314">Date object was installed.</span></span> <span data-ttu-id="fffbd-315">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="fffbd-315">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="fffbd-316">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="fffbd-316">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-317">**LargeSystemCache**</span><span class="sxs-lookup"><span data-stu-id="fffbd-317">**LargeSystemCache**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fffbd-318">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="fffbd-318">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-319">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fffbd-319">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-320">限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="fffbd-320">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="fffbd-321">這個屬性已過時，不受支援。</span><span class="sxs-lookup"><span data-stu-id="fffbd-321">This property is obsolete and not supported.</span></span>

<dt>

<span id="Optimize_for_Applications"></span><span id="optimize_for_applications"></span><span id="OPTIMIZE_FOR_APPLICATIONS"></span>

<span data-ttu-id="fffbd-322"><span id="Optimize_for_Applications"></span><span id="optimize_for_applications"></span><span id="OPTIMIZE_FOR_APPLICATIONS"></span>**針對應用程式優化** (0) </span><span class="sxs-lookup"><span data-stu-id="fffbd-322"><span id="Optimize_for_Applications"></span><span id="optimize_for_applications"></span><span id="OPTIMIZE_FOR_APPLICATIONS"></span>**Optimize for Applications** (0)</span></span>


</dt> <dd>

<span data-ttu-id="fffbd-323">優化應用程式的記憶體。</span><span class="sxs-lookup"><span data-stu-id="fffbd-323">Optimize memory for applications.</span></span>

</dd> <dt>

<span id="Optimize_for_System_Performance"></span><span id="optimize_for_system_performance"></span><span id="OPTIMIZE_FOR_SYSTEM_PERFORMANCE"></span>

<span data-ttu-id="fffbd-324"><span id="Optimize_for_System_Performance"></span><span id="optimize_for_system_performance"></span><span id="OPTIMIZE_FOR_SYSTEM_PERFORMANCE"></span>**針對系統效能優化** (1) </span><span class="sxs-lookup"><span data-stu-id="fffbd-324"><span id="Optimize_for_System_Performance"></span><span id="optimize_for_system_performance"></span><span id="OPTIMIZE_FOR_SYSTEM_PERFORMANCE"></span>**Optimize for System Performance** (1)</span></span>


</dt> <dd>

<span data-ttu-id="fffbd-325">優化記憶體的系統效能。</span><span class="sxs-lookup"><span data-stu-id="fffbd-325">Optimize memory for system performance.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="fffbd-326">**LastBootUpTime**</span><span class="sxs-lookup"><span data-stu-id="fffbd-326">**LastBootUpTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fffbd-327">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="fffbd-327">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-328">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fffbd-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fffbd-329">作業系統上次重新開機的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="fffbd-329">Date and time the operating system was last restarted.</span></span>

<span data-ttu-id="fffbd-330">這個屬性繼承自 [**CIM \_ 作業系統**](cim-operatingsystem.md)。</span><span class="sxs-lookup"><span data-stu-id="fffbd-330">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-331">**>datetimeoffset.localdatetime**</span><span class="sxs-lookup"><span data-stu-id="fffbd-331">**LocalDateTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fffbd-332">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="fffbd-332">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-333">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fffbd-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-334">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIB。IETF \| 主機-RESOURCES-hrSystemDate "，" MIF。DMTF \| 一般資訊 \| 001.6 ") </span><span class="sxs-lookup"><span data-stu-id="fffbd-334">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|HOST-RESOURCES-MIB.hrSystemDate", "MIF.DMTF\|General Information\|001.6")</span></span>
</dt> </dl>

<span data-ttu-id="fffbd-335">本機日期和當日時間的作業系統版本。</span><span class="sxs-lookup"><span data-stu-id="fffbd-335">Operating system version of the local date and time-of-day.</span></span>

<span data-ttu-id="fffbd-336">這個屬性繼承自 [**CIM \_ 作業系統**](cim-operatingsystem.md)。</span><span class="sxs-lookup"><span data-stu-id="fffbd-336">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-337">**地區設定**</span><span class="sxs-lookup"><span data-stu-id="fffbd-337">**Locale**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fffbd-338">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fffbd-338">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-339">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fffbd-339">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-340">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| 國家語言支援函式 \| [**GetLocaleInfo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa) \| LOCALE \_ ILANGUAGE" ) </span><span class="sxs-lookup"><span data-stu-id="fffbd-340">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|National Language Support Functions\|[**GetLocaleInfo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa)\|LOCALE\_ILANGUAGE")</span></span>
</dt> </dl>

<span data-ttu-id="fffbd-341">作業系統所使用的語言識別項。</span><span class="sxs-lookup"><span data-stu-id="fffbd-341">Language identifier used by the operating system.</span></span> <span data-ttu-id="fffbd-342">語言識別項是國家/地區的標準國際數位縮寫。</span><span class="sxs-lookup"><span data-stu-id="fffbd-342">A language identifier is a standard international numeric abbreviation for a country/region.</span></span> <span data-ttu-id="fffbd-343">每種語言都有唯一的語言識別項 (LANGID) ，它是由主要語言識別項和次要語言識別項組成的16位值。</span><span class="sxs-lookup"><span data-stu-id="fffbd-343">Each language has a unique language identifier (LANGID), a 16-bit value that consists of a primary language identifier and a secondary language identifier.</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-344">**製造商**</span><span class="sxs-lookup"><span data-stu-id="fffbd-344">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fffbd-345">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fffbd-345">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-346">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fffbd-346">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-347">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI" ) </span><span class="sxs-lookup"><span data-stu-id="fffbd-347">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="fffbd-348">作業系統製造商的名稱。</span><span class="sxs-lookup"><span data-stu-id="fffbd-348">Name of the operating system manufacturer.</span></span> <span data-ttu-id="fffbd-349">如果是以 Windows 為基礎的系統，此值會是 "Microsoft Corporation"。</span><span class="sxs-lookup"><span data-stu-id="fffbd-349">For Windows-based systems, this value is "Microsoft Corporation".</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-350">**MaxNumberOfProcesses**</span><span class="sxs-lookup"><span data-stu-id="fffbd-350">**MaxNumberOfProcesses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fffbd-351">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="fffbd-351">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-352">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fffbd-352">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-353">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIB。IETF \| 主機-RESOURCES-hrSystemMaxProcesses ") </span><span class="sxs-lookup"><span data-stu-id="fffbd-353">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|HOST-RESOURCES-MIB.hrSystemMaxProcesses")</span></span>
</dt> </dl>

<span data-ttu-id="fffbd-354">作業系統可支援的進程內容數目上限。</span><span class="sxs-lookup"><span data-stu-id="fffbd-354">Maximum number of process contexts the operating system can support.</span></span> <span data-ttu-id="fffbd-355">提供者所設定的預設值為 4294967295 (0xFFFFFFFF) 。</span><span class="sxs-lookup"><span data-stu-id="fffbd-355">The default value set by the provider is 4294967295 (0xFFFFFFFF).</span></span> <span data-ttu-id="fffbd-356">如果沒有固定的最大值，此值應為 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="fffbd-356">If there is no fixed maximum, the value should be 0 (zero).</span></span> <span data-ttu-id="fffbd-357">在具有固定最大值的系統上，此物件可協助診斷到達最大值時所發生的失敗，如果不明，請輸入 4294967295 (0xFFFFFFFF) 。</span><span class="sxs-lookup"><span data-stu-id="fffbd-357">On systems that have a fixed maximum, this object can help diagnose failures that occur when the maximum is reached—if unknown, enter 4294967295 (0xFFFFFFFF).</span></span>

<span data-ttu-id="fffbd-358">這個屬性繼承自 [**CIM \_ 作業系統**](cim-operatingsystem.md)。</span><span class="sxs-lookup"><span data-stu-id="fffbd-358">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-359">**MaxProcessMemorySize**</span><span class="sxs-lookup"><span data-stu-id="fffbd-359">**MaxProcessMemorySize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fffbd-360">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="fffbd-360">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-361">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fffbd-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-362">限定詞： [**單位**](../wmisdk/standard-qualifiers.md) ( "kb" ) </span><span class="sxs-lookup"><span data-stu-id="fffbd-362">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="fffbd-363">可以配置給進程的最大記憶體數目（以 kb 為單位）。</span><span class="sxs-lookup"><span data-stu-id="fffbd-363">Maximum number, in kilobytes, of memory that can be allocated to a process.</span></span> <span data-ttu-id="fffbd-364">對於沒有虛擬記憶體的作業系統，通常此值等於實體記憶體的總數量減去 BIOS 和作業系統所使用的記憶體。</span><span class="sxs-lookup"><span data-stu-id="fffbd-364">For operating systems with no virtual memory, typically this value is equal to the total amount of physical memory minus the memory used by the BIOS and the operating system.</span></span> <span data-ttu-id="fffbd-365">對於某些作業系統而言，這個值可能是無限大的，在此情況下，應該輸入 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="fffbd-365">For some operating systems, this value may be infinity, in which case 0 (zero) should be entered.</span></span> <span data-ttu-id="fffbd-366">在其他情況下，此值可以是常數，例如2G 或4G。</span><span class="sxs-lookup"><span data-stu-id="fffbd-366">In other cases, this value could be a constant, for example, 2G or 4G.</span></span>

<span data-ttu-id="fffbd-367">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="fffbd-367">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="fffbd-368">這個屬性繼承自 [**CIM \_ 作業系統**](cim-operatingsystem.md)。</span><span class="sxs-lookup"><span data-stu-id="fffbd-368">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-369">**MUILanguages**</span><span class="sxs-lookup"><span data-stu-id="fffbd-369">**MUILanguages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fffbd-370">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="fffbd-370">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-371">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fffbd-371">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-372">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI" ) </span><span class="sxs-lookup"><span data-stu-id="fffbd-372">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="fffbd-373">電腦上安裝的多語系消費者介面套件 (MUI 套件 ) 語言。</span><span class="sxs-lookup"><span data-stu-id="fffbd-373">Multilingual User Interface Pack (MUI Pack ) languages installed on the computer.</span></span> <span data-ttu-id="fffbd-374">例如，"en-us"。</span><span class="sxs-lookup"><span data-stu-id="fffbd-374">For example, "en-us".</span></span> <span data-ttu-id="fffbd-375">MUI 套件語言是可安裝在英文版作業系統上的資源檔。</span><span class="sxs-lookup"><span data-stu-id="fffbd-375">MUI Pack languages are resource files that can be installed on the English version of the operating system.</span></span> <span data-ttu-id="fffbd-376">安裝 MUI 套件之後，您可以將使用者介面語言變更為33支援的語言之一。</span><span class="sxs-lookup"><span data-stu-id="fffbd-376">When an MUI Pack is installed, you can can change the user interface language to one of 33 supported languages.</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-377">**名稱**</span><span class="sxs-lookup"><span data-stu-id="fffbd-377">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fffbd-378">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fffbd-378">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-379">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fffbd-379">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fffbd-380">電腦系統內的作業系統實例。</span><span class="sxs-lookup"><span data-stu-id="fffbd-380">Operating system instance within a computer system.</span></span>

<span data-ttu-id="fffbd-381">這個屬性繼承自 [**CIM \_ 作業系統**](cim-operatingsystem.md)。</span><span class="sxs-lookup"><span data-stu-id="fffbd-381">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-382">**NumberOfLicensedUsers**</span><span class="sxs-lookup"><span data-stu-id="fffbd-382">**NumberOfLicensedUsers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fffbd-383">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="fffbd-383">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-384">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fffbd-384">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fffbd-385">作業系統的使用者授權數目。</span><span class="sxs-lookup"><span data-stu-id="fffbd-385">Number of user licenses for the operating system.</span></span> <span data-ttu-id="fffbd-386">如果沒有限制，請輸入 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="fffbd-386">If unlimited, enter 0 (zero).</span></span> <span data-ttu-id="fffbd-387">如果不明，請輸入-1。</span><span class="sxs-lookup"><span data-stu-id="fffbd-387">If unknown, enter -1.</span></span>

<span data-ttu-id="fffbd-388">這個屬性繼承自 [**CIM \_ 作業系統**](cim-operatingsystem.md)。</span><span class="sxs-lookup"><span data-stu-id="fffbd-388">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-389">**NumberOfProcesses**</span><span class="sxs-lookup"><span data-stu-id="fffbd-389">**NumberOfProcesses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fffbd-390">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="fffbd-390">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-391">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fffbd-391">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-392">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIB。IETF \| 主機-RESOURCES-hrSystemProcesses ") </span><span class="sxs-lookup"><span data-stu-id="fffbd-392">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|HOST-RESOURCES-MIB.hrSystemProcesses")</span></span>
</dt> </dl>

<span data-ttu-id="fffbd-393">目前已載入或正在作業系統上執行的進程內容數目。</span><span class="sxs-lookup"><span data-stu-id="fffbd-393">Number of process contexts currently loaded or running on the operating system.</span></span>

<span data-ttu-id="fffbd-394">這個屬性繼承自 [**CIM \_ 作業系統**](cim-operatingsystem.md)。</span><span class="sxs-lookup"><span data-stu-id="fffbd-394">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-395">**Numberofusers 位**</span><span class="sxs-lookup"><span data-stu-id="fffbd-395">**NumberOfUsers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fffbd-396">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="fffbd-396">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-397">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fffbd-397">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-398">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIB。IETF \| 主機-RESOURCES-hrSystemNumUsers ") </span><span class="sxs-lookup"><span data-stu-id="fffbd-398">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|HOST-RESOURCES-MIB.hrSystemNumUsers")</span></span>
</dt> </dl>

<span data-ttu-id="fffbd-399">作業系統目前儲存狀態資訊的使用者會話數目。</span><span class="sxs-lookup"><span data-stu-id="fffbd-399">Number of user sessions for which the operating system is storing state information currently.</span></span>

<span data-ttu-id="fffbd-400">這個屬性繼承自 [**CIM \_ 作業系統**](cim-operatingsystem.md)。</span><span class="sxs-lookup"><span data-stu-id="fffbd-400">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-401">**OperatingSystemSKU**</span><span class="sxs-lookup"><span data-stu-id="fffbd-401">**OperatingSystemSKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fffbd-402">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="fffbd-402">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-403">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fffbd-403">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-404">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI" ) </span><span class="sxs-lookup"><span data-stu-id="fffbd-404">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="fffbd-405">作業系統的庫存單位 (SKU) 號碼。</span><span class="sxs-lookup"><span data-stu-id="fffbd-405">Stock Keeping Unit (SKU) number for the operating system.</span></span> <span data-ttu-id="fffbd-406">這些值與在 WinNT 中定義的 \*\* \_ \* PRODUCT\* _ 常數相同，與 [_ *GetProductInfo* \*](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getproductinfo)函數搭配使用。</span><span class="sxs-lookup"><span data-stu-id="fffbd-406">These values are the same as the \**PRODUCT\_\** _ constants defined in WinNT.h that are used with the [_ *GetProductInfo*\*](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getproductinfo) function.</span></span>

<span data-ttu-id="fffbd-407">下列清單列出可能的 SKU 值。</span><span class="sxs-lookup"><span data-stu-id="fffbd-407">The following list lists possible SKU values.</span></span>

<dt>

<span id="PRODUCT_UNDEFINED"></span><span id="product_undefined"></span>

<span data-ttu-id="fffbd-408"><span id="PRODUCT_UNDEFINED"></span><span id="product_undefined"></span>**產品 \_未定義** (0) </span><span class="sxs-lookup"><span data-stu-id="fffbd-408"><span id="PRODUCT_UNDEFINED"></span><span id="product_undefined"></span>**PRODUCT\_UNDEFINED** (0)</span></span>


</dt> <dd>

<span data-ttu-id="fffbd-409">未定義</span><span class="sxs-lookup"><span data-stu-id="fffbd-409">Undefined</span></span>

</dd> <dt>

<span id="PRODUCT_ULTIMATE"></span><span id="product_ultimate"></span>

<span data-ttu-id="fffbd-410"><span id="PRODUCT_ULTIMATE"></span><span id="product_ultimate"></span>**產品 \_旗艦** (1) </span><span class="sxs-lookup"><span data-stu-id="fffbd-410"><span id="PRODUCT_ULTIMATE"></span><span id="product_ultimate"></span>**PRODUCT\_ULTIMATE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="fffbd-411">旗艦版，例如 Windows Vista 旗艦版。</span><span class="sxs-lookup"><span data-stu-id="fffbd-411">Ultimate Edition, e.g. Windows Vista Ultimate.</span></span>

</dd> <dt>

<span id="PRODUCT_HOME_BASIC"></span><span id="product_home_basic"></span>

<span data-ttu-id="fffbd-412"><span id="PRODUCT_HOME_BASIC"></span><span id="product_home_basic"></span>**產品 \_HOME \_ BASIC** (2) </span><span class="sxs-lookup"><span data-stu-id="fffbd-412"><span id="PRODUCT_HOME_BASIC"></span><span id="product_home_basic"></span>**PRODUCT\_HOME\_BASIC** (2)</span></span>


</dt> <dd>

<span data-ttu-id="fffbd-413">Home Basic 版</span><span class="sxs-lookup"><span data-stu-id="fffbd-413">Home Basic Edition</span></span>

</dd> <dt>

<span id="PRODUCT_HOME_PREMIUM"></span><span id="product_home_premium"></span>

<span data-ttu-id="fffbd-414"><span id="PRODUCT_HOME_PREMIUM"></span><span id="product_home_premium"></span>**產品 \_HOME \_ PREMIUM** (3) </span><span class="sxs-lookup"><span data-stu-id="fffbd-414"><span id="PRODUCT_HOME_PREMIUM"></span><span id="product_home_premium"></span>**PRODUCT\_HOME\_PREMIUM** (3)</span></span>


</dt> <dd>

<span data-ttu-id="fffbd-415">Home Premium Edition</span><span class="sxs-lookup"><span data-stu-id="fffbd-415">Home Premium Edition</span></span>

</dd> <dt>

<span id="PRODUCT_ENTERPRISE"></span><span id="product_enterprise"></span>

<span data-ttu-id="fffbd-416"><span id="PRODUCT_ENTERPRISE"></span><span id="product_enterprise"></span>**產品 \_ENTERPRISE** (4) </span><span class="sxs-lookup"><span data-stu-id="fffbd-416"><span id="PRODUCT_ENTERPRISE"></span><span id="product_enterprise"></span>**PRODUCT\_ENTERPRISE** (4)</span></span>


</dt> <dd>

<span data-ttu-id="fffbd-417">企業版</span><span class="sxs-lookup"><span data-stu-id="fffbd-417">Enterprise Edition</span></span>

</dd> <dt>

<span id="PRODUCT_BUSINESS"></span><span id="product_business"></span>

<span data-ttu-id="fffbd-418"><span id="PRODUCT_BUSINESS"></span><span id="product_business"></span>**產品 \_BUSINESS** (6) </span><span class="sxs-lookup"><span data-stu-id="fffbd-418"><span id="PRODUCT_BUSINESS"></span><span id="product_business"></span>**PRODUCT\_BUSINESS** (6)</span></span>


</dt> <dd>

<span data-ttu-id="fffbd-419">Business Edition</span><span class="sxs-lookup"><span data-stu-id="fffbd-419">Business Edition</span></span>

</dd> <dt>

<span id="PRODUCT_STANDARD_SERVER"></span><span id="product_standard_server"></span>

<span data-ttu-id="fffbd-420"><span id="PRODUCT_STANDARD_SERVER"></span><span id="product_standard_server"></span>**產品 \_標準 \_ 伺服器** (7) </span><span class="sxs-lookup"><span data-stu-id="fffbd-420"><span id="PRODUCT_STANDARD_SERVER"></span><span id="product_standard_server"></span>**PRODUCT\_STANDARD\_SERVER** (7)</span></span>


</dt> <dd>

<span data-ttu-id="fffbd-421">Windows Server Standard Edition (桌面體驗安裝) </span><span class="sxs-lookup"><span data-stu-id="fffbd-421">Windows Server Standard Edition (Desktop Experience installation)</span></span>

</dd> <dt>

<span id="PRODUCT_DATACENTER_SERVER"></span><span id="product_datacenter_server"></span>

<span data-ttu-id="fffbd-422"><span id="PRODUCT_DATACENTER_SERVER"></span><span id="product_datacenter_server"></span>**產品 \_DATACENTER \_ SERVER** (8) </span><span class="sxs-lookup"><span data-stu-id="fffbd-422"><span id="PRODUCT_DATACENTER_SERVER"></span><span id="product_datacenter_server"></span>**PRODUCT\_DATACENTER\_SERVER** (8)</span></span>


</dt> <dd>

<span data-ttu-id="fffbd-423">Windows Server Datacenter Edition (桌面體驗安裝) </span><span class="sxs-lookup"><span data-stu-id="fffbd-423">Windows Server Datacenter Edition (Desktop Experience installation)</span></span>

</dd> <dt>

<span id="PRODUCT_SMALLBUSINESS_SERVER"></span><span id="product_smallbusiness_server"></span>

<span data-ttu-id="fffbd-424"><span id="PRODUCT_SMALLBUSINESS_SERVER"></span><span id="product_smallbusiness_server"></span>**產品 \_SMALLBUSINESS \_ SERVER** (9) </span><span class="sxs-lookup"><span data-stu-id="fffbd-424"><span id="PRODUCT_SMALLBUSINESS_SERVER"></span><span id="product_smallbusiness_server"></span>**PRODUCT\_SMALLBUSINESS\_SERVER** (9)</span></span>


</dt> <dd>

<span data-ttu-id="fffbd-425">Small Business Server 版本</span><span class="sxs-lookup"><span data-stu-id="fffbd-425">Small Business Server Edition</span></span>

</dd> <dt>

<span id="PRODUCT_ENTERPRISE_SERVER"></span><span id="product_enterprise_server"></span>

<span data-ttu-id="fffbd-426"><span id="PRODUCT_ENTERPRISE_SERVER"></span><span id="product_enterprise_server"></span>**產品 \_企業 \_ 伺服器** (10) </span><span class="sxs-lookup"><span data-stu-id="fffbd-426"><span id="PRODUCT_ENTERPRISE_SERVER"></span><span id="product_enterprise_server"></span>**PRODUCT\_ENTERPRISE\_SERVER** (10)</span></span>


</dt> <dd>

<span data-ttu-id="fffbd-427">Enterprise Server Edition</span><span class="sxs-lookup"><span data-stu-id="fffbd-427">Enterprise Server Edition</span></span>

</dd> <dt>

<span id="PRODUCT_STARTER"></span><span id="product_starter"></span>

<span data-ttu-id="fffbd-428"><span id="PRODUCT_STARTER"></span><span id="product_starter"></span>**產品 \_入門** (11) </span><span class="sxs-lookup"><span data-stu-id="fffbd-428"><span id="PRODUCT_STARTER"></span><span id="product_starter"></span>**PRODUCT\_STARTER** (11)</span></span>


</dt> <dd>

<span data-ttu-id="fffbd-429"> Starter Edition</span><span class="sxs-lookup"><span data-stu-id="fffbd-429">Starter Edition</span></span>

</dd> <dt>

<span id="PRODUCT_DATACENTER_SERVER_CORE"></span><span id="product_datacenter_server_core"></span>

<span data-ttu-id="fffbd-430"><span id="PRODUCT_DATACENTER_SERVER_CORE"></span><span id="product_datacenter_server_core"></span>**產品 \_DATACENTER \_ SERVER \_ CORE** (12) </span><span class="sxs-lookup"><span data-stu-id="fffbd-430"><span id="PRODUCT_DATACENTER_SERVER_CORE"></span><span id="product_datacenter_server_core"></span>**PRODUCT\_DATACENTER\_SERVER\_CORE** (12)</span></span>


</dt> <dd>

<span data-ttu-id="fffbd-431">Datacenter Server Core Edition</span><span class="sxs-lookup"><span data-stu-id="fffbd-431">Datacenter Server Core Edition</span></span>

</dd> <dt>

<span id="PRODUCT_STANDARD_SERVER_CORE"></span><span id="product_standard_server_core"></span>

<span data-ttu-id="fffbd-432"><span id="PRODUCT_STANDARD_SERVER_CORE"></span><span id="product_standard_server_core"></span>**產品 \_標準 \_ SERVER \_ CORE** (13) </span><span class="sxs-lookup"><span data-stu-id="fffbd-432"><span id="PRODUCT_STANDARD_SERVER_CORE"></span><span id="product_standard_server_core"></span>**PRODUCT\_STANDARD\_SERVER\_CORE** (13)</span></span>


</dt> <dd>

<span data-ttu-id="fffbd-433">標準 Server Core 版本</span><span class="sxs-lookup"><span data-stu-id="fffbd-433">Standard Server Core Edition</span></span>

</dd> <dt>

<span id="PRODUCT_ENTERPRISE_SERVER_CORE"></span><span id="product_enterprise_server_core"></span>

<span data-ttu-id="fffbd-434"><span id="PRODUCT_ENTERPRISE_SERVER_CORE"></span><span id="product_enterprise_server_core"></span>**產品 \_ENTERPRISE \_ SERVER \_ CORE** (14) </span><span class="sxs-lookup"><span data-stu-id="fffbd-434"><span id="PRODUCT_ENTERPRISE_SERVER_CORE"></span><span id="product_enterprise_server_core"></span>**PRODUCT\_ENTERPRISE\_SERVER\_CORE** (14)</span></span>


</dt> <dd>

<span data-ttu-id="fffbd-435">Enterprise Server Core 版</span><span class="sxs-lookup"><span data-stu-id="fffbd-435">Enterprise Server Core Edition</span></span>

</dd> <dt>

<span id="PRODUCT_WEB_SERVER"></span><span id="product_web_server"></span>

<span data-ttu-id="fffbd-436"><span id="PRODUCT_WEB_SERVER"></span><span id="product_web_server"></span>**產品 \_WEB \_ 伺服器** (17) </span><span class="sxs-lookup"><span data-stu-id="fffbd-436"><span id="PRODUCT_WEB_SERVER"></span><span id="product_web_server"></span>**PRODUCT\_WEB\_SERVER** (17)</span></span>


</dt> <dd>

<span data-ttu-id="fffbd-437">Web 服務器版本</span><span class="sxs-lookup"><span data-stu-id="fffbd-437">Web Server Edition</span></span>

</dd> <dt>

<span id="PRODUCT_HOME_SERVER"></span><span id="product_home_server"></span>

<span data-ttu-id="fffbd-438"><span id="PRODUCT_HOME_SERVER"></span><span id="product_home_server"></span>**產品 \_HOME \_ SERVER** (19) </span><span class="sxs-lookup"><span data-stu-id="fffbd-438"><span id="PRODUCT_HOME_SERVER"></span><span id="product_home_server"></span>**PRODUCT\_HOME\_SERVER** (19)</span></span>


</dt> <dd>

<span data-ttu-id="fffbd-439">Home Server Edition</span><span class="sxs-lookup"><span data-stu-id="fffbd-439">Home Server Edition</span></span>

</dd> <dt>

<span id="PRODUCT_STORAGE_EXPRESS_SERVER"></span><span id="product_storage_express_server"></span>

<span data-ttu-id="fffbd-440"><span id="PRODUCT_STORAGE_EXPRESS_SERVER"></span><span id="product_storage_express_server"></span>**產品 \_STORAGE \_ EXPRESS \_ SERVER** (20) </span><span class="sxs-lookup"><span data-stu-id="fffbd-440"><span id="PRODUCT_STORAGE_EXPRESS_SERVER"></span><span id="product_storage_express_server"></span>**PRODUCT\_STORAGE\_EXPRESS\_SERVER** (20)</span></span>


</dt> <dd>

<span data-ttu-id="fffbd-441">Storage Express Server 版本</span><span class="sxs-lookup"><span data-stu-id="fffbd-441">Storage Express Server Edition</span></span>

</dd> <dt>

<span id="PRODUCT_STORAGE_STANDARD_SERVER"></span><span id="product_storage_standard_server"></span>

<span data-ttu-id="fffbd-442"><span id="PRODUCT_STORAGE_STANDARD_SERVER"></span><span id="product_storage_standard_server"></span>**產品 \_STORAGE \_ STANDARD \_ SERVER** (21) </span><span class="sxs-lookup"><span data-stu-id="fffbd-442"><span id="PRODUCT_STORAGE_STANDARD_SERVER"></span><span id="product_storage_standard_server"></span>**PRODUCT\_STORAGE\_STANDARD\_SERVER** (21)</span></span>


</dt> <dd>

<span data-ttu-id="fffbd-443">Windows Storage Server Standard Edition (桌面體驗安裝) </span><span class="sxs-lookup"><span data-stu-id="fffbd-443">Windows Storage Server Standard Edition (Desktop Experience installation)</span></span>

</dd> <dt>

<span id="PRODUCT_STORAGE_WORKGROUP_SERVER"></span><span id="product_storage_workgroup_server"></span>

<span data-ttu-id="fffbd-444"><span id="PRODUCT_STORAGE_WORKGROUP_SERVER"></span><span id="product_storage_workgroup_server"></span>**產品 \_STORAGE \_ WORKGROUP \_ SERVER** (22) </span><span class="sxs-lookup"><span data-stu-id="fffbd-444"><span id="PRODUCT_STORAGE_WORKGROUP_SERVER"></span><span id="product_storage_workgroup_server"></span>**PRODUCT\_STORAGE\_WORKGROUP\_SERVER** (22)</span></span>


</dt> <dd>

<span data-ttu-id="fffbd-445">Windows Storage Server Workgroup Edition (桌面體驗安裝) </span><span class="sxs-lookup"><span data-stu-id="fffbd-445">Windows Storage Server Workgroup Edition (Desktop Experience installation)</span></span>

</dd> <dt>

<span id="PRODUCT_STORAGE_ENTERPRISE_SERVER"></span><span id="product_storage_enterprise_server"></span>

<span data-ttu-id="fffbd-446"><span id="PRODUCT_STORAGE_ENTERPRISE_SERVER"></span><span id="product_storage_enterprise_server"></span>**產品 \_STORAGE \_ ENTERPRISE \_ SERVER** (23) </span><span class="sxs-lookup"><span data-stu-id="fffbd-446"><span id="PRODUCT_STORAGE_ENTERPRISE_SERVER"></span><span id="product_storage_enterprise_server"></span>**PRODUCT\_STORAGE\_ENTERPRISE\_SERVER** (23)</span></span>


</dt> <dd>

<span data-ttu-id="fffbd-447">Storage Enterprise Server Edition</span><span class="sxs-lookup"><span data-stu-id="fffbd-447">Storage Enterprise Server Edition</span></span>

</dd> <dt>

<span id="PRODUCT_SERVER_FOR_SMALLBUSINESS"></span><span id="product_server_for_smallbusiness"></span>

<span data-ttu-id="fffbd-448"><span id="PRODUCT_SERVER_FOR_SMALLBUSINESS"></span><span id="product_server_for_smallbusiness"></span>**產品 \_SERVER \_ FOR \_ SMALLBUSINESS** (24) </span><span class="sxs-lookup"><span data-stu-id="fffbd-448"><span id="PRODUCT_SERVER_FOR_SMALLBUSINESS"></span><span id="product_server_for_smallbusiness"></span>**PRODUCT\_SERVER\_FOR\_SMALLBUSINESS** (24)</span></span>


</dt> <dd>

<span data-ttu-id="fffbd-449">適用于 Small Business Edition 的伺服器</span><span class="sxs-lookup"><span data-stu-id="fffbd-449">Server For Small Business Edition</span></span>

</dd> <dt>

<span id="PRODUCT_SMALLBUSINESS_SERVER_PREMIUM"></span><span id="product_smallbusiness_server_premium"></span>

<span data-ttu-id="fffbd-450"><span id="PRODUCT_SMALLBUSINESS_SERVER_PREMIUM"></span><span id="product_smallbusiness_server_premium"></span>**產品 \_SMALLBUSINESS \_ SERVER \_ PREMIUM** (25) </span><span class="sxs-lookup"><span data-stu-id="fffbd-450"><span id="PRODUCT_SMALLBUSINESS_SERVER_PREMIUM"></span><span id="product_smallbusiness_server_premium"></span>**PRODUCT\_SMALLBUSINESS\_SERVER\_PREMIUM** (25)</span></span>


</dt> <dd>

<span data-ttu-id="fffbd-451">Small Business Server Premium Edition</span><span class="sxs-lookup"><span data-stu-id="fffbd-451">Small Business Server Premium Edition</span></span>

</dd> <dt>

<span id="PRODUCT_ENTERPRISE_N"></span><span id="product_enterprise_n"></span>

<span data-ttu-id="fffbd-452"><span id="PRODUCT_ENTERPRISE_N"></span><span id="product_enterprise_n"></span>**產品 \_企業 \_ N** (27) </span><span class="sxs-lookup"><span data-stu-id="fffbd-452"><span id="PRODUCT_ENTERPRISE_N"></span><span id="product_enterprise_n"></span>**PRODUCT\_ENTERPRISE\_N** (27)</span></span>


</dt> <dd>

<span data-ttu-id="fffbd-453">Windows Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="fffbd-453">Windows Enterprise Edition</span></span>

</dd> <dt>

<span id="PRODUCT_ULTIMATE_N"></span><span id="product_ultimate_n"></span>

<span data-ttu-id="fffbd-454"><span id="PRODUCT_ULTIMATE_N"></span><span id="product_ultimate_n"></span>**產品 \_終極 \_ N** (28) </span><span class="sxs-lookup"><span data-stu-id="fffbd-454"><span id="PRODUCT_ULTIMATE_N"></span><span id="product_ultimate_n"></span>**PRODUCT\_ULTIMATE\_N** (28)</span></span>


</dt> <dd>

<span data-ttu-id="fffbd-455">Windows 旗艦版</span><span class="sxs-lookup"><span data-stu-id="fffbd-455">Windows Ultimate Edition</span></span>

</dd> <dt>

<span id="PRODUCT_WEB_SERVER_CORE"></span><span id="product_web_server_core"></span>

<span data-ttu-id="fffbd-456"><span id="PRODUCT_WEB_SERVER_CORE"></span><span id="product_web_server_core"></span>**產品 \_WEB \_ SERVER \_ CORE** (29) </span><span class="sxs-lookup"><span data-stu-id="fffbd-456"><span id="PRODUCT_WEB_SERVER_CORE"></span><span id="product_web_server_core"></span>**PRODUCT\_WEB\_SERVER\_CORE** (29)</span></span>


</dt> <dd>

<span data-ttu-id="fffbd-457">Windows Server Web Server Edition (Server Core 安裝) </span><span class="sxs-lookup"><span data-stu-id="fffbd-457">Windows Server Web Server Edition (Server Core installation)</span></span>

</dd> <dt>

<span id="PRODUCT_STANDARD_SERVER_V"></span><span id="product_standard_server_v"></span>

<span data-ttu-id="fffbd-458"><span id="PRODUCT_STANDARD_SERVER_V"></span><span id="product_standard_server_v"></span>**產品 \_STANDARD \_ SERVER \_ V** (36) </span><span class="sxs-lookup"><span data-stu-id="fffbd-458"><span id="PRODUCT_STANDARD_SERVER_V"></span><span id="product_standard_server_v"></span>**PRODUCT\_STANDARD\_SERVER\_V** (36)</span></span>


</dt> <dd>

<span data-ttu-id="fffbd-459">不含 Hyper-v 的 Windows Server Standard Edition</span><span class="sxs-lookup"><span data-stu-id="fffbd-459">Windows Server Standard Edition without Hyper-V</span></span>

</dd> <dt>

<span id="PRODUCT_DATACENTER_SERVER_V"></span><span id="product_datacenter_server_v"></span>

<span data-ttu-id="fffbd-460"><span id="PRODUCT_DATACENTER_SERVER_V"></span><span id="product_datacenter_server_v"></span>**產品 \_DATACENTER \_ SERVER \_ V** (37) </span><span class="sxs-lookup"><span data-stu-id="fffbd-460"><span id="PRODUCT_DATACENTER_SERVER_V"></span><span id="product_datacenter_server_v"></span>**PRODUCT\_DATACENTER\_SERVER\_V** (37)</span></span>


</dt> <dd>

<span data-ttu-id="fffbd-461">沒有 Hyper-v 的 Windows Server Datacenter Edition (完整安裝) </span><span class="sxs-lookup"><span data-stu-id="fffbd-461">Windows Server Datacenter Edition without Hyper-V (full installation)</span></span>

</dd> <dt>

<span id="PRODUCT_ENTERPRISE_SERVER_V"></span><span id="product_enterprise_server_v"></span>

<span data-ttu-id="fffbd-462"><span id="PRODUCT_ENTERPRISE_SERVER_V"></span><span id="product_enterprise_server_v"></span>**產品 \_ENTERPRISE \_ SERVER \_ V** (38) </span><span class="sxs-lookup"><span data-stu-id="fffbd-462"><span id="PRODUCT_ENTERPRISE_SERVER_V"></span><span id="product_enterprise_server_v"></span>**PRODUCT\_ENTERPRISE\_SERVER\_V** (38)</span></span>


</dt> <dd>

<span data-ttu-id="fffbd-463">沒有 Hyper-v 的 Windows Server Enterprise Edition (完整安裝) </span><span class="sxs-lookup"><span data-stu-id="fffbd-463">Windows Server Enterprise Edition without Hyper-V (full installation)</span></span>

</dd> <dt>

<span id="PRODUCT_DATACENTER_SERVER_CORE_V"></span><span id="product_datacenter_server_core_v"></span>

<span data-ttu-id="fffbd-464"><span id="PRODUCT_DATACENTER_SERVER_CORE_V"></span><span id="product_datacenter_server_core_v"></span>**產品 \_DATACENTER \_ SERVER \_ CORE \_ V** (39) </span><span class="sxs-lookup"><span data-stu-id="fffbd-464"><span id="PRODUCT_DATACENTER_SERVER_CORE_V"></span><span id="product_datacenter_server_core_v"></span>**PRODUCT\_DATACENTER\_SERVER\_CORE\_V** (39)</span></span>


</dt> <dd>

<span data-ttu-id="fffbd-465">沒有 Hyper-v 的 Windows Server Datacenter Edition (Server Core 安裝) </span><span class="sxs-lookup"><span data-stu-id="fffbd-465">Windows Server Datacenter Edition without Hyper-V (Server Core installation)</span></span>

</dd> <dt>

<span id="PRODUCT_STANDARD_SERVER_CORE_V"></span><span id="product_standard_server_core_v"></span>

<span data-ttu-id="fffbd-466"><span id="PRODUCT_STANDARD_SERVER_CORE_V"></span><span id="product_standard_server_core_v"></span>**產品 \_標準 \_ SERVER \_ CORE \_ V** (40) </span><span class="sxs-lookup"><span data-stu-id="fffbd-466"><span id="PRODUCT_STANDARD_SERVER_CORE_V"></span><span id="product_standard_server_core_v"></span>**PRODUCT\_STANDARD\_SERVER\_CORE\_V** (40)</span></span>


</dt> <dd>

<span data-ttu-id="fffbd-467">沒有 Hyper-v 的 Windows Server Standard Edition (Server Core 安裝) </span><span class="sxs-lookup"><span data-stu-id="fffbd-467">Windows Server Standard Edition without Hyper-V (Server Core installation)</span></span>

</dd> <dt>

<span id="PRODUCT_ENTERPRISE_SERVER_CORE_V"></span><span id="product_enterprise_server_core_v"></span>

<span data-ttu-id="fffbd-468"><span id="PRODUCT_ENTERPRISE_SERVER_CORE_V"></span><span id="product_enterprise_server_core_v"></span>**產品 \_ENTERPRISE \_ SERVER \_ CORE \_ V** (41) </span><span class="sxs-lookup"><span data-stu-id="fffbd-468"><span id="PRODUCT_ENTERPRISE_SERVER_CORE_V"></span><span id="product_enterprise_server_core_v"></span>**PRODUCT\_ENTERPRISE\_SERVER\_CORE\_V** (41)</span></span>


</dt> <dd>

<span data-ttu-id="fffbd-469">沒有 Hyper-v 的 Windows Server Enterprise Edition (Server Core 安裝) </span><span class="sxs-lookup"><span data-stu-id="fffbd-469">Windows Server Enterprise Edition without Hyper-V (Server Core installation)</span></span>

</dd> <dt>

<span id="PRODUCT_HYPERV"></span><span id="product_hyperv"></span>

<span data-ttu-id="fffbd-470"><span id="PRODUCT_HYPERV"></span><span id="product_hyperv"></span>**產品 \_HYPERV** (42) </span><span class="sxs-lookup"><span data-stu-id="fffbd-470"><span id="PRODUCT_HYPERV"></span><span id="product_hyperv"></span>**PRODUCT\_HYPERV** (42)</span></span>


</dt> <dd>

<span data-ttu-id="fffbd-471">Microsoft Hyper-V Server</span><span class="sxs-lookup"><span data-stu-id="fffbd-471">Microsoft Hyper-V Server</span></span>

</dd> <dt>

<span id="PRODUCT_STORAGE_EXPRESS_SERVER_CORE"></span><span id="product_storage_express_server_core"></span>

<span data-ttu-id="fffbd-472"><span id="PRODUCT_STORAGE_EXPRESS_SERVER_CORE"></span><span id="product_storage_express_server_core"></span>**產品 \_STORAGE \_ EXPRESS \_ SERVER \_ CORE** (43) </span><span class="sxs-lookup"><span data-stu-id="fffbd-472"><span id="PRODUCT_STORAGE_EXPRESS_SERVER_CORE"></span><span id="product_storage_express_server_core"></span>**PRODUCT\_STORAGE\_EXPRESS\_SERVER\_CORE** (43)</span></span>


</dt> <dd>

<span data-ttu-id="fffbd-473">Storage Server Express Edition (Server Core 安裝) </span><span class="sxs-lookup"><span data-stu-id="fffbd-473">Storage Server Express Edition (Server Core installation)</span></span>

</dd> <dt>

<span id="PRODUCT_STORAGE_STANDARD_SERVER_CORE"></span><span id="product_storage_standard_server_core"></span>

<span data-ttu-id="fffbd-474"><span id="PRODUCT_STORAGE_STANDARD_SERVER_CORE"></span><span id="product_storage_standard_server_core"></span>**產品 \_STORAGE \_ STANDARD \_ SERVER \_ CORE** (44) </span><span class="sxs-lookup"><span data-stu-id="fffbd-474"><span id="PRODUCT_STORAGE_STANDARD_SERVER_CORE"></span><span id="product_storage_standard_server_core"></span>**PRODUCT\_STORAGE\_STANDARD\_SERVER\_CORE** (44)</span></span>


</dt> <dd>

<span data-ttu-id="fffbd-475">Storage Server Standard Edition (Server Core 安裝) </span><span class="sxs-lookup"><span data-stu-id="fffbd-475">Storage Server Standard Edition (Server Core installation)</span></span>

</dd> <dt>

<span id="PRODUCT_STORAGE_WORKGROUP_SERVER_CORE"></span><span id="product_storage_workgroup_server_core"></span>

<span data-ttu-id="fffbd-476"><span id="PRODUCT_STORAGE_WORKGROUP_SERVER_CORE"></span><span id="product_storage_workgroup_server_core"></span>**產品 \_STORAGE \_ WORKGROUP \_ SERVER \_ CORE** (45) </span><span class="sxs-lookup"><span data-stu-id="fffbd-476"><span id="PRODUCT_STORAGE_WORKGROUP_SERVER_CORE"></span><span id="product_storage_workgroup_server_core"></span>**PRODUCT\_STORAGE\_WORKGROUP\_SERVER\_CORE** (45)</span></span>


</dt> <dd>

<span data-ttu-id="fffbd-477">Storage Server Workgroup Edition (Server Core 安裝) </span><span class="sxs-lookup"><span data-stu-id="fffbd-477">Storage Server Workgroup Edition (Server Core installation)</span></span>

</dd> <dt>

<span id="PRODUCT_STORAGE_ENTERPRISE_SERVER_CORE"></span><span id="product_storage_enterprise_server_core"></span>

<span data-ttu-id="fffbd-478"><span id="PRODUCT_STORAGE_ENTERPRISE_SERVER_CORE"></span><span id="product_storage_enterprise_server_core"></span>**產品 \_STORAGE \_ ENTERPRISE \_ SERVER \_ CORE** (46) </span><span class="sxs-lookup"><span data-stu-id="fffbd-478"><span id="PRODUCT_STORAGE_ENTERPRISE_SERVER_CORE"></span><span id="product_storage_enterprise_server_core"></span>**PRODUCT\_STORAGE\_ENTERPRISE\_SERVER\_CORE** (46)</span></span>


</dt> <dd>

<span data-ttu-id="fffbd-479">Storage Server Workgroup Edition (Server Core 安裝) </span><span class="sxs-lookup"><span data-stu-id="fffbd-479">Storage Server Workgroup Edition (Server Core installation)</span></span>

</dd> <dt>

<span id="PRODUCT_PROFESSIONAL"></span><span id="product_professional"></span>

<span data-ttu-id="fffbd-480"><span id="PRODUCT_PROFESSIONAL"></span><span id="product_professional"></span>**產品 \_PROFESSIONAL** (48) </span><span class="sxs-lookup"><span data-stu-id="fffbd-480"><span id="PRODUCT_PROFESSIONAL"></span><span id="product_professional"></span>**PRODUCT\_PROFESSIONAL** (48)</span></span>


</dt> <dd>

<span data-ttu-id="fffbd-481">Windows 專業版</span><span class="sxs-lookup"><span data-stu-id="fffbd-481">Windows Professional</span></span>

</dd> <dt>

<span id="PRODUCT_SB_SOLUTION_SERVER"></span><span id="product_sb_solution_server"></span>

<span data-ttu-id="fffbd-482"><span id="PRODUCT_SB_SOLUTION_SERVER"></span><span id="product_sb_solution_server"></span>**產品 \_SB \_ 解決方案 \_ 伺服器** (50) </span><span class="sxs-lookup"><span data-stu-id="fffbd-482"><span id="PRODUCT_SB_SOLUTION_SERVER"></span><span id="product_sb_solution_server"></span>**PRODUCT\_SB\_SOLUTION\_SERVER** (50)</span></span>


</dt> <dd>

<span data-ttu-id="fffbd-483">Windows Server Essentials (桌面體驗安裝) </span><span class="sxs-lookup"><span data-stu-id="fffbd-483">Windows Server Essentials (Desktop Experience installation)</span></span>

</dd> <dt>

<span id="PRODUCT_SMALLBUSINESS_SERVER_PREMIUM_CORE"></span><span id="product_smallbusiness_server_premium_core"></span>

<span data-ttu-id="fffbd-484"><span id="PRODUCT_SMALLBUSINESS_SERVER_PREMIUM_CORE"></span><span id="product_smallbusiness_server_premium_core"></span>**產品 \_SMALLBUSINESS \_ SERVER \_ PREMIUM \_ CORE** (63) </span><span class="sxs-lookup"><span data-stu-id="fffbd-484"><span id="PRODUCT_SMALLBUSINESS_SERVER_PREMIUM_CORE"></span><span id="product_smallbusiness_server_premium_core"></span>**PRODUCT\_SMALLBUSINESS\_SERVER\_PREMIUM\_CORE** (63)</span></span>


</dt> <dd>

<span data-ttu-id="fffbd-485">Small Business Server Premium (Server Core 安裝) </span><span class="sxs-lookup"><span data-stu-id="fffbd-485">Small Business Server Premium (Server Core installation)</span></span>

</dd> <dt>

<span id="PRODUCT_CLUSTER_SERVER_V"></span><span id="product_cluster_server_v"></span>

<span data-ttu-id="fffbd-486"><span id="PRODUCT_CLUSTER_SERVER_V"></span><span id="product_cluster_server_v"></span>**產品 \_CLUSTER \_ SERVER \_ V** (64) </span><span class="sxs-lookup"><span data-stu-id="fffbd-486"><span id="PRODUCT_CLUSTER_SERVER_V"></span><span id="product_cluster_server_v"></span>**PRODUCT\_CLUSTER\_SERVER\_V** (64)</span></span>


</dt> <dd>

<span data-ttu-id="fffbd-487">不含 Hyper-v 的 Windows Compute Cluster Server</span><span class="sxs-lookup"><span data-stu-id="fffbd-487">Windows Compute Cluster Server without Hyper-V</span></span>

</dd> <dt>

<span id="PRODUCT_CORE_ARM"></span><span id="product_core_arm"></span>

<span data-ttu-id="fffbd-488"><span id="PRODUCT_CORE_ARM"></span><span id="product_core_arm"></span>**產品 \_核心 \_ ARM** (97) </span><span class="sxs-lookup"><span data-stu-id="fffbd-488"><span id="PRODUCT_CORE_ARM"></span><span id="product_core_arm"></span>**PRODUCT\_CORE\_ARM** (97)</span></span>


</dt> <dd>

<span data-ttu-id="fffbd-489">Windows RT</span><span class="sxs-lookup"><span data-stu-id="fffbd-489">Windows RT</span></span>

</dd> <dt>

<span id="PRODUCT_CORE"></span><span id="product_core"></span>

<span data-ttu-id="fffbd-490"><span id="PRODUCT_CORE"></span><span id="product_core"></span>**產品 \_CORE** (101) </span><span class="sxs-lookup"><span data-stu-id="fffbd-490"><span id="PRODUCT_CORE"></span><span id="product_core"></span>**PRODUCT\_CORE** (101)</span></span>


</dt> <dd>

<span data-ttu-id="fffbd-491">Windows 首頁</span><span class="sxs-lookup"><span data-stu-id="fffbd-491">Windows Home</span></span>

</dd> <dt>

<span id="PRODUCT_PROFESSIONAL_WMC"></span><span id="product_professional_wmc"></span>

<span data-ttu-id="fffbd-492"><span id="PRODUCT_PROFESSIONAL_WMC"></span><span id="product_professional_wmc"></span>**產品 \_PROFESSIONAL \_ WMC** (103) </span><span class="sxs-lookup"><span data-stu-id="fffbd-492"><span id="PRODUCT_PROFESSIONAL_WMC"></span><span id="product_professional_wmc"></span>**PRODUCT\_PROFESSIONAL\_WMC** (103)</span></span>


</dt> <dd>

<span data-ttu-id="fffbd-493">具有 Media Center 的 Windows 專業版</span><span class="sxs-lookup"><span data-stu-id="fffbd-493">Windows Professional with Media Center</span></span>

</dd> <dt>

<span id="PRODUCT_MOBILE_CORE"></span><span id="product_mobile_core"></span>

<span data-ttu-id="fffbd-494"><span id="PRODUCT_MOBILE_CORE"></span><span id="product_mobile_core"></span>**產品 \_MOBILE \_ CORE** (104) </span><span class="sxs-lookup"><span data-stu-id="fffbd-494"><span id="PRODUCT_MOBILE_CORE"></span><span id="product_mobile_core"></span>**PRODUCT\_MOBILE\_CORE** (104)</span></span>


</dt> <dd>

<span data-ttu-id="fffbd-495">Windows Mobile</span><span class="sxs-lookup"><span data-stu-id="fffbd-495">Windows Mobile</span></span>

</dd> <dt>

<span id="PRODUCT_IOTUAP"></span><span id="product_iotuap"></span>

<span data-ttu-id="fffbd-496"><span id="PRODUCT_IOTUAP"></span><span id="product_iotuap"></span>**產品 \_IOTUAP** (123) </span><span class="sxs-lookup"><span data-stu-id="fffbd-496"><span id="PRODUCT_IOTUAP"></span><span id="product_iotuap"></span>**PRODUCT\_IOTUAP** (123)</span></span>


</dt> <dd>

<span data-ttu-id="fffbd-497">Windows IoT (物聯網) 核心</span><span class="sxs-lookup"><span data-stu-id="fffbd-497">Windows IoT (Internet of Things) Core</span></span>

</dd> <dt>

<span id="PRODUCT_DATACENTER_NANO_SERVER"></span><span id="product_datacenter_nano_server"></span>

<span data-ttu-id="fffbd-498"><span id="PRODUCT_DATACENTER_NANO_SERVER"></span><span id="product_datacenter_nano_server"></span>**產品 \_DATACENTER \_ NANO \_ server** (143) </span><span class="sxs-lookup"><span data-stu-id="fffbd-498"><span id="PRODUCT_DATACENTER_NANO_SERVER"></span><span id="product_datacenter_nano_server"></span>**PRODUCT\_DATACENTER\_NANO\_SERVER** (143)</span></span>


</dt> <dd>

<span data-ttu-id="fffbd-499">Windows Server Datacenter Edition (Nano Server 安裝) </span><span class="sxs-lookup"><span data-stu-id="fffbd-499">Windows Server Datacenter Edition (Nano Server installation)</span></span>

</dd> <dt>

<span id="PRODUCT_STANDARD_NANO_SERVER"></span><span id="product_standard_nano_server"></span>

<span data-ttu-id="fffbd-500"><span id="PRODUCT_STANDARD_NANO_SERVER"></span><span id="product_standard_nano_server"></span>**產品 \_標準 \_ NANO \_ SERVER** (144) </span><span class="sxs-lookup"><span data-stu-id="fffbd-500"><span id="PRODUCT_STANDARD_NANO_SERVER"></span><span id="product_standard_nano_server"></span>**PRODUCT\_STANDARD\_NANO\_SERVER** (144)</span></span>


</dt> <dd>

<span data-ttu-id="fffbd-501">Windows Server Standard Edition (Nano Server 安裝) </span><span class="sxs-lookup"><span data-stu-id="fffbd-501">Windows Server Standard Edition (Nano Server installation)</span></span>

</dd> <dt>

<span id="PRODUCT_DATACENTER_WS_SERVER_CORE"></span><span id="product_datacenter_ws_server_core"></span>

<span data-ttu-id="fffbd-502"><span id="PRODUCT_DATACENTER_WS_SERVER_CORE"></span><span id="product_datacenter_ws_server_core"></span>**產品 \_DATACENTER \_ WS \_ SERVER \_ CORE** (147) </span><span class="sxs-lookup"><span data-stu-id="fffbd-502"><span id="PRODUCT_DATACENTER_WS_SERVER_CORE"></span><span id="product_datacenter_ws_server_core"></span>**PRODUCT\_DATACENTER\_WS\_SERVER\_CORE** (147)</span></span>


</dt> <dd>

<span data-ttu-id="fffbd-503">Windows Server Datacenter Edition (Server Core 安裝) </span><span class="sxs-lookup"><span data-stu-id="fffbd-503">Windows Server Datacenter Edition (Server Core installation)</span></span>

</dd> <dt>

<span id="PRODUCT_STANDARD_WS_SERVER_CORE"></span><span id="product_standard_ws_server_core"></span>

<span data-ttu-id="fffbd-504"><span id="PRODUCT_STANDARD_WS_SERVER_CORE"></span><span id="product_standard_ws_server_core"></span>**產品 \_標準 \_ WS \_ SERVER \_ CORE** (148) </span><span class="sxs-lookup"><span data-stu-id="fffbd-504"><span id="PRODUCT_STANDARD_WS_SERVER_CORE"></span><span id="product_standard_ws_server_core"></span>**PRODUCT\_STANDARD\_WS\_SERVER\_CORE** (148)</span></span>


</dt> <dd>

<span data-ttu-id="fffbd-505">Windows Server Standard Edition (Server Core 安裝) </span><span class="sxs-lookup"><span data-stu-id="fffbd-505">Windows Server Standard Edition (Server Core installation)</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="fffbd-506">組織</span><span class="sxs-lookup"><span data-stu-id="fffbd-506">**Organization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fffbd-507">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fffbd-507">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-508">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fffbd-508">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-509">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \| RegisteredOrganization" ) </span><span class="sxs-lookup"><span data-stu-id="fffbd-509">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\Windows\\\\CurrentVersion\|RegisteredOrganization")</span></span>
</dt> </dl>

<span data-ttu-id="fffbd-510">作業系統註冊使用者的公司名稱。</span><span class="sxs-lookup"><span data-stu-id="fffbd-510">Company name for the registered user of the operating system.</span></span>

<span data-ttu-id="fffbd-511">範例： "Microsoft Corporation"</span><span class="sxs-lookup"><span data-stu-id="fffbd-511">Example: "Microsoft Corporation"</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-512">**OSArchitecture**</span><span class="sxs-lookup"><span data-stu-id="fffbd-512">**OSArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fffbd-513">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fffbd-513">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-514">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fffbd-514">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fffbd-515">作業系統的架構，而不是處理器。</span><span class="sxs-lookup"><span data-stu-id="fffbd-515">Architecture of the operating system, as opposed to the processor.</span></span> <span data-ttu-id="fffbd-516">這個屬性可以當地語系化。</span><span class="sxs-lookup"><span data-stu-id="fffbd-516">This property can be localized.</span></span>

<span data-ttu-id="fffbd-517">範例：32位</span><span class="sxs-lookup"><span data-stu-id="fffbd-517">Example: 32-bit</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-518">**OSLanguage**</span><span class="sxs-lookup"><span data-stu-id="fffbd-518">**OSLanguage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fffbd-519">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="fffbd-519">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-520">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fffbd-520">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-521">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| DEFAULT \\ \\ 主控台 \\ \\ 國際 \| 地區設定" ) </span><span class="sxs-lookup"><span data-stu-id="fffbd-521">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|DEFAULT\\\\Control Panel\\\\International\|Locale")</span></span>
</dt> </dl>

<span data-ttu-id="fffbd-522">已安裝作業系統的語言版本。</span><span class="sxs-lookup"><span data-stu-id="fffbd-522">Language version of the operating system installed.</span></span> <span data-ttu-id="fffbd-523">下列清單列出可能的值。</span><span class="sxs-lookup"><span data-stu-id="fffbd-523">The following list lists the possible values.</span></span> <span data-ttu-id="fffbd-524">範例： 0x0807 (德文、瑞士) 。</span><span class="sxs-lookup"><span data-stu-id="fffbd-524">Example: 0x0807 (German, Switzerland).</span></span>

<dt>

<span data-ttu-id="fffbd-525">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="fffbd-525">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-526">阿拉伯文</span><span class="sxs-lookup"><span data-stu-id="fffbd-526">Arabic</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-527">4 (0x4) </span><span class="sxs-lookup"><span data-stu-id="fffbd-527">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-528">中文 (簡體) –中國</span><span class="sxs-lookup"><span data-stu-id="fffbd-528">Chinese (Simplified)– China</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-529">9 (0x9) </span><span class="sxs-lookup"><span data-stu-id="fffbd-529">9 (0x9)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-530">英文</span><span class="sxs-lookup"><span data-stu-id="fffbd-530">English</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-531">1025 (0x401) </span><span class="sxs-lookup"><span data-stu-id="fffbd-531">1025 (0x401)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-532">阿拉伯文-沙烏地阿拉伯</span><span class="sxs-lookup"><span data-stu-id="fffbd-532">Arabic – Saudi Arabia</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-533">1026 (0x402) </span><span class="sxs-lookup"><span data-stu-id="fffbd-533">1026 (0x402)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-534">保加利亞文</span><span class="sxs-lookup"><span data-stu-id="fffbd-534">Bulgarian</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-535">1027 (0x403) </span><span class="sxs-lookup"><span data-stu-id="fffbd-535">1027 (0x403)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-536">卡達隆尼亞文</span><span class="sxs-lookup"><span data-stu-id="fffbd-536">Catalan</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-537">1028 (0x404) </span><span class="sxs-lookup"><span data-stu-id="fffbd-537">1028 (0x404)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-538">繁體中文) -臺灣 (</span><span class="sxs-lookup"><span data-stu-id="fffbd-538">Chinese (Traditional) – Taiwan</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-539">1029 (0x405) </span><span class="sxs-lookup"><span data-stu-id="fffbd-539">1029 (0x405)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-540">捷克文</span><span class="sxs-lookup"><span data-stu-id="fffbd-540">Czech</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-541">1030 (0x406) </span><span class="sxs-lookup"><span data-stu-id="fffbd-541">1030 (0x406)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-542">丹麥文</span><span class="sxs-lookup"><span data-stu-id="fffbd-542">Danish</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-543">1031 (0x407) </span><span class="sxs-lookup"><span data-stu-id="fffbd-543">1031 (0x407)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-544">德文 – 德國</span><span class="sxs-lookup"><span data-stu-id="fffbd-544">German – Germany</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-545">1032 (0x408) </span><span class="sxs-lookup"><span data-stu-id="fffbd-545">1032 (0x408)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-546">希臘文</span><span class="sxs-lookup"><span data-stu-id="fffbd-546">Greek</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-547">1033 (0x409) </span><span class="sxs-lookup"><span data-stu-id="fffbd-547">1033 (0x409)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-548">英文-美國</span><span class="sxs-lookup"><span data-stu-id="fffbd-548">English – United States</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-549">1034 (0x40A) </span><span class="sxs-lookup"><span data-stu-id="fffbd-549">1034 (0x40A)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-550">西班牙文-傳統排序</span><span class="sxs-lookup"><span data-stu-id="fffbd-550">Spanish – Traditional Sort</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-551">1035 (0x40B) </span><span class="sxs-lookup"><span data-stu-id="fffbd-551">1035 (0x40B)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-552">芬蘭文</span><span class="sxs-lookup"><span data-stu-id="fffbd-552">Finnish</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-553">1036 (0x40C) </span><span class="sxs-lookup"><span data-stu-id="fffbd-553">1036 (0x40C)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-554">法文 – 法國</span><span class="sxs-lookup"><span data-stu-id="fffbd-554">French – France</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-555">1037 (0x40D) </span><span class="sxs-lookup"><span data-stu-id="fffbd-555">1037 (0x40D)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-556">Hebrew</span><span class="sxs-lookup"><span data-stu-id="fffbd-556">Hebrew</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-557">1038 (0x40E) </span><span class="sxs-lookup"><span data-stu-id="fffbd-557">1038 (0x40E)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-558">匈牙利文</span><span class="sxs-lookup"><span data-stu-id="fffbd-558">Hungarian</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-559">1039 (0x40F) </span><span class="sxs-lookup"><span data-stu-id="fffbd-559">1039 (0x40F)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-560">冰島文</span><span class="sxs-lookup"><span data-stu-id="fffbd-560">Icelandic</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-561">1040 (0x410) </span><span class="sxs-lookup"><span data-stu-id="fffbd-561">1040 (0x410)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-562">義大利文 – 義大利</span><span class="sxs-lookup"><span data-stu-id="fffbd-562">Italian – Italy</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-563">1041 (0x411) </span><span class="sxs-lookup"><span data-stu-id="fffbd-563">1041 (0x411)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-564">日文</span><span class="sxs-lookup"><span data-stu-id="fffbd-564">Japanese</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-565">1042 (0x412) </span><span class="sxs-lookup"><span data-stu-id="fffbd-565">1042 (0x412)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-566">韓文</span><span class="sxs-lookup"><span data-stu-id="fffbd-566">Korean</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-567">1043 (0x413) </span><span class="sxs-lookup"><span data-stu-id="fffbd-567">1043 (0x413)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-568">荷蘭文 – 荷蘭</span><span class="sxs-lookup"><span data-stu-id="fffbd-568">Dutch – Netherlands</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-569">1044 (0x414) </span><span class="sxs-lookup"><span data-stu-id="fffbd-569">1044 (0x414)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-570">挪威文–博克瑪律</span><span class="sxs-lookup"><span data-stu-id="fffbd-570">Norwegian – Bokmal</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-571">1045 (0x415) </span><span class="sxs-lookup"><span data-stu-id="fffbd-571">1045 (0x415)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-572">波蘭文</span><span class="sxs-lookup"><span data-stu-id="fffbd-572">Polish</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-573">1046 (0x416) </span><span class="sxs-lookup"><span data-stu-id="fffbd-573">1046 (0x416)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-574">葡萄牙文 – 巴西</span><span class="sxs-lookup"><span data-stu-id="fffbd-574">Portuguese – Brazil</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-575">1047 (0x417) </span><span class="sxs-lookup"><span data-stu-id="fffbd-575">1047 (0x417)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-576">Rhaeto-Romanic</span><span class="sxs-lookup"><span data-stu-id="fffbd-576">Rhaeto-Romanic</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-577">1048 (0x418) </span><span class="sxs-lookup"><span data-stu-id="fffbd-577">1048 (0x418)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-578">羅馬尼亞文</span><span class="sxs-lookup"><span data-stu-id="fffbd-578">Romanian</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-579">1049 (0x419) </span><span class="sxs-lookup"><span data-stu-id="fffbd-579">1049 (0x419)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-580">俄文</span><span class="sxs-lookup"><span data-stu-id="fffbd-580">Russian</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-581">1050 (0x41A) </span><span class="sxs-lookup"><span data-stu-id="fffbd-581">1050 (0x41A)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-582">克羅埃西亞文</span><span class="sxs-lookup"><span data-stu-id="fffbd-582">Croatian</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-583">1051 (0x41B) </span><span class="sxs-lookup"><span data-stu-id="fffbd-583">1051 (0x41B)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-584">斯洛伐克文</span><span class="sxs-lookup"><span data-stu-id="fffbd-584">Slovak</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-585">1052 (0x41C) </span><span class="sxs-lookup"><span data-stu-id="fffbd-585">1052 (0x41C)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-586">阿爾巴尼亞文</span><span class="sxs-lookup"><span data-stu-id="fffbd-586">Albanian</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-587">1053 (0x41D) </span><span class="sxs-lookup"><span data-stu-id="fffbd-587">1053 (0x41D)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-588">瑞典文</span><span class="sxs-lookup"><span data-stu-id="fffbd-588">Swedish</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-589">1054 (0x41E) </span><span class="sxs-lookup"><span data-stu-id="fffbd-589">1054 (0x41E)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-590">泰文</span><span class="sxs-lookup"><span data-stu-id="fffbd-590">Thai</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-591">1055 (0x41F) </span><span class="sxs-lookup"><span data-stu-id="fffbd-591">1055 (0x41F)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-592">土耳其文</span><span class="sxs-lookup"><span data-stu-id="fffbd-592">Turkish</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-593">1056 (0x420) </span><span class="sxs-lookup"><span data-stu-id="fffbd-593">1056 (0x420)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-594">烏都文</span><span class="sxs-lookup"><span data-stu-id="fffbd-594">Urdu</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-595">1057 (0x421) </span><span class="sxs-lookup"><span data-stu-id="fffbd-595">1057 (0x421)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-596">印尼文</span><span class="sxs-lookup"><span data-stu-id="fffbd-596">Indonesian</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-597">1058 (0x422) </span><span class="sxs-lookup"><span data-stu-id="fffbd-597">1058 (0x422)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-598">烏克蘭文</span><span class="sxs-lookup"><span data-stu-id="fffbd-598">Ukrainian</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-599">1059 (0x423) </span><span class="sxs-lookup"><span data-stu-id="fffbd-599">1059 (0x423)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-600">白俄羅斯文</span><span class="sxs-lookup"><span data-stu-id="fffbd-600">Belarusian</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-601">1060 (0x424) </span><span class="sxs-lookup"><span data-stu-id="fffbd-601">1060 (0x424)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-602">斯洛維尼亞文</span><span class="sxs-lookup"><span data-stu-id="fffbd-602">Slovenian</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-603">1061 (0x425) </span><span class="sxs-lookup"><span data-stu-id="fffbd-603">1061 (0x425)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-604">愛沙尼亞文</span><span class="sxs-lookup"><span data-stu-id="fffbd-604">Estonian</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-605">1062 (0x426) </span><span class="sxs-lookup"><span data-stu-id="fffbd-605">1062 (0x426)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-606">拉脫維亞文</span><span class="sxs-lookup"><span data-stu-id="fffbd-606">Latvian</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-607">1063 (0x427) </span><span class="sxs-lookup"><span data-stu-id="fffbd-607">1063 (0x427)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-608">立陶宛文</span><span class="sxs-lookup"><span data-stu-id="fffbd-608">Lithuanian</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-609">1065 (0x429) </span><span class="sxs-lookup"><span data-stu-id="fffbd-609">1065 (0x429)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-610">波斯文</span><span class="sxs-lookup"><span data-stu-id="fffbd-610">Persian</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-611">1066 (0x42A) </span><span class="sxs-lookup"><span data-stu-id="fffbd-611">1066 (0x42A)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-612">越南文</span><span class="sxs-lookup"><span data-stu-id="fffbd-612">Vietnamese</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-613">1069 (0x42D) </span><span class="sxs-lookup"><span data-stu-id="fffbd-613">1069 (0x42D)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-614">巴斯克文 (巴斯克)</span><span class="sxs-lookup"><span data-stu-id="fffbd-614">Basque (Basque)</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-615">1070 (0x42E) </span><span class="sxs-lookup"><span data-stu-id="fffbd-615">1070 (0x42E)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-616">塞爾維亞文</span><span class="sxs-lookup"><span data-stu-id="fffbd-616">Serbian</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-617">1071 (0x42F) </span><span class="sxs-lookup"><span data-stu-id="fffbd-617">1071 (0x42F)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-618">馬其頓 (北美洲馬其頓) </span><span class="sxs-lookup"><span data-stu-id="fffbd-618">Macedonian (North Macedonia)</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-619">1072 (0x430) </span><span class="sxs-lookup"><span data-stu-id="fffbd-619">1072 (0x430)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-620">Sutu</span><span class="sxs-lookup"><span data-stu-id="fffbd-620">Sutu</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-621">1073 (0x431) </span><span class="sxs-lookup"><span data-stu-id="fffbd-621">1073 (0x431)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-622">Tsonga</span><span class="sxs-lookup"><span data-stu-id="fffbd-622">Tsonga</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-623">1074 (0x432) </span><span class="sxs-lookup"><span data-stu-id="fffbd-623">1074 (0x432)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-624">茨瓦納語</span><span class="sxs-lookup"><span data-stu-id="fffbd-624">Tswana</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-625">1076 (0x434) </span><span class="sxs-lookup"><span data-stu-id="fffbd-625">1076 (0x434)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-626">科薩文</span><span class="sxs-lookup"><span data-stu-id="fffbd-626">Xhosa</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-627">1077 (0x435) </span><span class="sxs-lookup"><span data-stu-id="fffbd-627">1077 (0x435)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-628">祖魯文</span><span class="sxs-lookup"><span data-stu-id="fffbd-628">Zulu</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-629">1078 (0x436) </span><span class="sxs-lookup"><span data-stu-id="fffbd-629">1078 (0x436)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-630">南非荷蘭文</span><span class="sxs-lookup"><span data-stu-id="fffbd-630">Afrikaans</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-631">1080 (0x438) </span><span class="sxs-lookup"><span data-stu-id="fffbd-631">1080 (0x438)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-632">法羅文</span><span class="sxs-lookup"><span data-stu-id="fffbd-632">Faeroese</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-633">1081 (0x439) </span><span class="sxs-lookup"><span data-stu-id="fffbd-633">1081 (0x439)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-634">Hindi</span><span class="sxs-lookup"><span data-stu-id="fffbd-634">Hindi</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-635">1082 (0x43A) </span><span class="sxs-lookup"><span data-stu-id="fffbd-635">1082 (0x43A)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-636">馬爾他文</span><span class="sxs-lookup"><span data-stu-id="fffbd-636">Maltese</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-637">1084 (0x43C) </span><span class="sxs-lookup"><span data-stu-id="fffbd-637">1084 (0x43C)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-638">蘇格蘭蓋爾文 (英國) </span><span class="sxs-lookup"><span data-stu-id="fffbd-638">Scottish Gaelic (United Kingdom)</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-639">1085 (0x43D) </span><span class="sxs-lookup"><span data-stu-id="fffbd-639">1085 (0x43D)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-640">意第緒文</span><span class="sxs-lookup"><span data-stu-id="fffbd-640">Yiddish</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-641">1086 (0x43E) </span><span class="sxs-lookup"><span data-stu-id="fffbd-641">1086 (0x43E)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-642">馬來–馬來西亞</span><span class="sxs-lookup"><span data-stu-id="fffbd-642">Malay – Malaysia</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-643">2049 (0x801) </span><span class="sxs-lookup"><span data-stu-id="fffbd-643">2049 (0x801)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-644">阿拉伯文–伊拉克</span><span class="sxs-lookup"><span data-stu-id="fffbd-644">Arabic – Iraq</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-645">2052 (0x804) </span><span class="sxs-lookup"><span data-stu-id="fffbd-645">2052 (0x804)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-646">中文 (簡化) –中國</span><span class="sxs-lookup"><span data-stu-id="fffbd-646">Chinese (Simplified) – PRC</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-647">2055 (0x807) </span><span class="sxs-lookup"><span data-stu-id="fffbd-647">2055 (0x807)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-648">德文–瑞士</span><span class="sxs-lookup"><span data-stu-id="fffbd-648">German – Switzerland</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-649">2057 (0x809) </span><span class="sxs-lookup"><span data-stu-id="fffbd-649">2057 (0x809)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-650">英文-英國</span><span class="sxs-lookup"><span data-stu-id="fffbd-650">English – United Kingdom</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-651">2058 (0x80A) </span><span class="sxs-lookup"><span data-stu-id="fffbd-651">2058 (0x80A)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-652">西班牙文–墨西哥</span><span class="sxs-lookup"><span data-stu-id="fffbd-652">Spanish – Mexico</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-653">2060 (0x80C) </span><span class="sxs-lookup"><span data-stu-id="fffbd-653">2060 (0x80C)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-654">法文-比利時</span><span class="sxs-lookup"><span data-stu-id="fffbd-654">French – Belgium</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-655">2064 (0x810) </span><span class="sxs-lookup"><span data-stu-id="fffbd-655">2064 (0x810)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-656">義大利文–瑞士</span><span class="sxs-lookup"><span data-stu-id="fffbd-656">Italian – Switzerland</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-657">2067 (0x813) </span><span class="sxs-lookup"><span data-stu-id="fffbd-657">2067 (0x813)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-658">荷蘭文–比利時</span><span class="sxs-lookup"><span data-stu-id="fffbd-658">Dutch – Belgium</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-659">2068 (0x814) </span><span class="sxs-lookup"><span data-stu-id="fffbd-659">2068 (0x814)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-660">挪威文–挪威文</span><span class="sxs-lookup"><span data-stu-id="fffbd-660">Norwegian – Nynorsk</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-661">2070 (0x816) </span><span class="sxs-lookup"><span data-stu-id="fffbd-661">2070 (0x816)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-662">葡萄牙文 (葡萄牙)</span><span class="sxs-lookup"><span data-stu-id="fffbd-662">Portuguese – Portugal</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-663">2072 (0x818) </span><span class="sxs-lookup"><span data-stu-id="fffbd-663">2072 (0x818)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-664">羅馬尼亞文–摩爾多瓦</span><span class="sxs-lookup"><span data-stu-id="fffbd-664">Romanian – Moldova</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-665">2073 (0x819) </span><span class="sxs-lookup"><span data-stu-id="fffbd-665">2073 (0x819)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-666">俄文–摩爾多瓦</span><span class="sxs-lookup"><span data-stu-id="fffbd-666">Russian – Moldova</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-667">2074 (0x81A) </span><span class="sxs-lookup"><span data-stu-id="fffbd-667">2074 (0x81A)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-668">塞爾維亞文-拉丁</span><span class="sxs-lookup"><span data-stu-id="fffbd-668">Serbian – Latin</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-669">2077 (0x81D) </span><span class="sxs-lookup"><span data-stu-id="fffbd-669">2077 (0x81D)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-670">瑞典文–芬蘭</span><span class="sxs-lookup"><span data-stu-id="fffbd-670">Swedish – Finland</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-671">3073 (0xC01) </span><span class="sxs-lookup"><span data-stu-id="fffbd-671">3073 (0xC01)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-672">阿拉伯文-埃及</span><span class="sxs-lookup"><span data-stu-id="fffbd-672">Arabic – Egypt</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-673">3076 (0xC04) </span><span class="sxs-lookup"><span data-stu-id="fffbd-673">3076 (0xC04)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-674">中文 (傳統) –香港特別行政區</span><span class="sxs-lookup"><span data-stu-id="fffbd-674">Chinese (Traditional) – Hong Kong SAR</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-675">3079 (0xC07) </span><span class="sxs-lookup"><span data-stu-id="fffbd-675">3079 (0xC07)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-676">德文–奧地利</span><span class="sxs-lookup"><span data-stu-id="fffbd-676">German – Austria</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-677">3081 (0xC09) </span><span class="sxs-lookup"><span data-stu-id="fffbd-677">3081 (0xC09)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-678">英文-澳大利亞</span><span class="sxs-lookup"><span data-stu-id="fffbd-678">English – Australia</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-679">3082 (0xC0A) </span><span class="sxs-lookup"><span data-stu-id="fffbd-679">3082 (0xC0A)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-680">西班牙文-國際排序</span><span class="sxs-lookup"><span data-stu-id="fffbd-680">Spanish – International Sort</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-681">3084 (0xC0C) </span><span class="sxs-lookup"><span data-stu-id="fffbd-681">3084 (0xC0C)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-682">法文-加拿大</span><span class="sxs-lookup"><span data-stu-id="fffbd-682">French – Canada</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-683">3098 (0xC1A) </span><span class="sxs-lookup"><span data-stu-id="fffbd-683">3098 (0xC1A)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-684">塞爾維亞文–斯拉夫</span><span class="sxs-lookup"><span data-stu-id="fffbd-684">Serbian – Cyrillic</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-685">4097 (0x1001) </span><span class="sxs-lookup"><span data-stu-id="fffbd-685">4097 (0x1001)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-686">阿拉伯文–利比亞</span><span class="sxs-lookup"><span data-stu-id="fffbd-686">Arabic – Libya</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-687">4100 (0x1004) </span><span class="sxs-lookup"><span data-stu-id="fffbd-687">4100 (0x1004)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-688">中文 (簡體) -新加坡</span><span class="sxs-lookup"><span data-stu-id="fffbd-688">Chinese (Simplified) – Singapore</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-689">4103 (0x1007) </span><span class="sxs-lookup"><span data-stu-id="fffbd-689">4103 (0x1007)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-690">德文–盧森堡</span><span class="sxs-lookup"><span data-stu-id="fffbd-690">German – Luxembourg</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-691">4105 (0x1009) </span><span class="sxs-lookup"><span data-stu-id="fffbd-691">4105 (0x1009)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-692">英文-加拿大</span><span class="sxs-lookup"><span data-stu-id="fffbd-692">English – Canada</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-693">4106 (0x100A) </span><span class="sxs-lookup"><span data-stu-id="fffbd-693">4106 (0x100A)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-694">西班牙文-瓜地馬拉</span><span class="sxs-lookup"><span data-stu-id="fffbd-694">Spanish – Guatemala</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-695">4108 (0x100C) </span><span class="sxs-lookup"><span data-stu-id="fffbd-695">4108 (0x100C)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-696">法文-瑞士</span><span class="sxs-lookup"><span data-stu-id="fffbd-696">French – Switzerland</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-697">5121 (0x1401) </span><span class="sxs-lookup"><span data-stu-id="fffbd-697">5121 (0x1401)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-698">阿拉伯文-阿爾及利亞</span><span class="sxs-lookup"><span data-stu-id="fffbd-698">Arabic – Algeria</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-699">5127 (0x1407) </span><span class="sxs-lookup"><span data-stu-id="fffbd-699">5127 (0x1407)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-700">德文–列支敦斯登</span><span class="sxs-lookup"><span data-stu-id="fffbd-700">German – Liechtenstein</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-701">5129 (0x1409) </span><span class="sxs-lookup"><span data-stu-id="fffbd-701">5129 (0x1409)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-702">英文–紐西蘭</span><span class="sxs-lookup"><span data-stu-id="fffbd-702">English – New Zealand</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-703">5130 (0x140A) </span><span class="sxs-lookup"><span data-stu-id="fffbd-703">5130 (0x140A)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-704">西班牙文–哥斯大黎加</span><span class="sxs-lookup"><span data-stu-id="fffbd-704">Spanish – Costa Rica</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-705">5132 (0x140C) </span><span class="sxs-lookup"><span data-stu-id="fffbd-705">5132 (0x140C)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-706">法文–盧森堡</span><span class="sxs-lookup"><span data-stu-id="fffbd-706">French – Luxembourg</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-707">6145 (0x1801) </span><span class="sxs-lookup"><span data-stu-id="fffbd-707">6145 (0x1801)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-708">阿拉伯文–摩洛哥</span><span class="sxs-lookup"><span data-stu-id="fffbd-708">Arabic – Morocco</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-709">6153 (0x1809) </span><span class="sxs-lookup"><span data-stu-id="fffbd-709">6153 (0x1809)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-710">英文-愛爾蘭</span><span class="sxs-lookup"><span data-stu-id="fffbd-710">English – Ireland</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-711">6154 (0x180A) </span><span class="sxs-lookup"><span data-stu-id="fffbd-711">6154 (0x180A)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-712">西班牙文–巴拿馬</span><span class="sxs-lookup"><span data-stu-id="fffbd-712">Spanish – Panama</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-713">7169 (0x1C01) </span><span class="sxs-lookup"><span data-stu-id="fffbd-713">7169 (0x1C01)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-714">阿拉伯文–突尼斯</span><span class="sxs-lookup"><span data-stu-id="fffbd-714">Arabic – Tunisia</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-715">7177 (0x1C09) </span><span class="sxs-lookup"><span data-stu-id="fffbd-715">7177 (0x1C09)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-716">英文-南非</span><span class="sxs-lookup"><span data-stu-id="fffbd-716">English – South Africa</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-717">7178 (0x1C0A) </span><span class="sxs-lookup"><span data-stu-id="fffbd-717">7178 (0x1C0A)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-718">西班牙文–多明尼加共和國</span><span class="sxs-lookup"><span data-stu-id="fffbd-718">Spanish – Dominican Republic</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-719">8193 (0x2001) </span><span class="sxs-lookup"><span data-stu-id="fffbd-719">8193 (0x2001)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-720">阿拉伯文-阿曼</span><span class="sxs-lookup"><span data-stu-id="fffbd-720">Arabic – Oman</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-721">8201 (0x2009) </span><span class="sxs-lookup"><span data-stu-id="fffbd-721">8201 (0x2009)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-722">英文–牙買加</span><span class="sxs-lookup"><span data-stu-id="fffbd-722">English – Jamaica</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-723">8202 (0x200A) </span><span class="sxs-lookup"><span data-stu-id="fffbd-723">8202 (0x200A)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-724">西班牙文–委內瑞拉</span><span class="sxs-lookup"><span data-stu-id="fffbd-724">Spanish – Venezuela</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-725">9217 (0x2401) </span><span class="sxs-lookup"><span data-stu-id="fffbd-725">9217 (0x2401)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-726">阿拉伯文–葉門</span><span class="sxs-lookup"><span data-stu-id="fffbd-726">Arabic – Yemen</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-727">9226 (0x240A) </span><span class="sxs-lookup"><span data-stu-id="fffbd-727">9226 (0x240A)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-728">西班牙文–哥倫比亞</span><span class="sxs-lookup"><span data-stu-id="fffbd-728">Spanish – Colombia</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-729">10241 (0x2801) </span><span class="sxs-lookup"><span data-stu-id="fffbd-729">10241 (0x2801)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-730">阿拉伯文–敘利亞</span><span class="sxs-lookup"><span data-stu-id="fffbd-730">Arabic – Syria</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-731">10249 (0x2809) </span><span class="sxs-lookup"><span data-stu-id="fffbd-731">10249 (0x2809)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-732">英文-貝里斯</span><span class="sxs-lookup"><span data-stu-id="fffbd-732">English – Belize</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-733">10250 (0x280A) </span><span class="sxs-lookup"><span data-stu-id="fffbd-733">10250 (0x280A)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-734">西班牙文–秘魯</span><span class="sxs-lookup"><span data-stu-id="fffbd-734">Spanish – Peru</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-735">11265 (0x2C01) </span><span class="sxs-lookup"><span data-stu-id="fffbd-735">11265 (0x2C01)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-736">阿拉伯文–約旦</span><span class="sxs-lookup"><span data-stu-id="fffbd-736">Arabic – Jordan</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-737">11273 (0x2C09) </span><span class="sxs-lookup"><span data-stu-id="fffbd-737">11273 (0x2C09)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-738">英文–特立尼達</span><span class="sxs-lookup"><span data-stu-id="fffbd-738">English – Trinidad</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-739">11274 (0x2C0A) </span><span class="sxs-lookup"><span data-stu-id="fffbd-739">11274 (0x2C0A)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-740">西班牙文-阿根廷</span><span class="sxs-lookup"><span data-stu-id="fffbd-740">Spanish – Argentina</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-741">12289 (0x3001) </span><span class="sxs-lookup"><span data-stu-id="fffbd-741">12289 (0x3001)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-742">阿拉伯文-黎巴嫩</span><span class="sxs-lookup"><span data-stu-id="fffbd-742">Arabic – Lebanon</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-743">12298 (0x300A) </span><span class="sxs-lookup"><span data-stu-id="fffbd-743">12298 (0x300A)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-744">西班牙文–厄瓜多爾</span><span class="sxs-lookup"><span data-stu-id="fffbd-744">Spanish – Ecuador</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-745">13313 (0x3401) </span><span class="sxs-lookup"><span data-stu-id="fffbd-745">13313 (0x3401)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-746">阿拉伯文–科威特</span><span class="sxs-lookup"><span data-stu-id="fffbd-746">Arabic – Kuwait</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-747">13322 (0x340A) </span><span class="sxs-lookup"><span data-stu-id="fffbd-747">13322 (0x340A)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-748">西班牙文–智利</span><span class="sxs-lookup"><span data-stu-id="fffbd-748">Spanish – Chile</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-749">14337 (0x3801) </span><span class="sxs-lookup"><span data-stu-id="fffbd-749">14337 (0x3801)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-750">阿拉伯文–阿拉伯聯合大公國</span><span class="sxs-lookup"><span data-stu-id="fffbd-750">Arabic – U.A.E.</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-751">14346 (0x380A) </span><span class="sxs-lookup"><span data-stu-id="fffbd-751">14346 (0x380A)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-752">西班牙文-烏拉圭</span><span class="sxs-lookup"><span data-stu-id="fffbd-752">Spanish – Uruguay</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-753">15361 (0x3C01) </span><span class="sxs-lookup"><span data-stu-id="fffbd-753">15361 (0x3C01)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-754">阿拉伯文–巴林</span><span class="sxs-lookup"><span data-stu-id="fffbd-754">Arabic – Bahrain</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-755">15370 (0x3C0A) </span><span class="sxs-lookup"><span data-stu-id="fffbd-755">15370 (0x3C0A)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-756">西班牙文–巴拉圭</span><span class="sxs-lookup"><span data-stu-id="fffbd-756">Spanish – Paraguay</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-757">16385 (0x4001) </span><span class="sxs-lookup"><span data-stu-id="fffbd-757">16385 (0x4001)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-758">阿拉伯文-卡塔爾</span><span class="sxs-lookup"><span data-stu-id="fffbd-758">Arabic – Qatar</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-759">16394 (0x400A) </span><span class="sxs-lookup"><span data-stu-id="fffbd-759">16394 (0x400A)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-760">西班牙文–玻利維亞</span><span class="sxs-lookup"><span data-stu-id="fffbd-760">Spanish – Bolivia</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-761">17418 (0x440A) </span><span class="sxs-lookup"><span data-stu-id="fffbd-761">17418 (0x440A)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-762">西班牙文-薩爾瓦多</span><span class="sxs-lookup"><span data-stu-id="fffbd-762">Spanish – El Salvador</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-763">18442 (0x480A) </span><span class="sxs-lookup"><span data-stu-id="fffbd-763">18442 (0x480A)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-764">西班牙文–宏都拉斯</span><span class="sxs-lookup"><span data-stu-id="fffbd-764">Spanish – Honduras</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-765">19466 (0x4C0A) </span><span class="sxs-lookup"><span data-stu-id="fffbd-765">19466 (0x4C0A)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-766">西班牙文–尼加拉瓜</span><span class="sxs-lookup"><span data-stu-id="fffbd-766">Spanish – Nicaragua</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-767">20490 (0x500A) </span><span class="sxs-lookup"><span data-stu-id="fffbd-767">20490 (0x500A)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-768">西班牙文-波多黎各</span><span class="sxs-lookup"><span data-stu-id="fffbd-768">Spanish – Puerto Rico</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="fffbd-769">**OSProductSuite**</span><span class="sxs-lookup"><span data-stu-id="fffbd-769">**OSProductSuite**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fffbd-770">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="fffbd-770">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-771">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fffbd-771">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-772">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ ProductOptions \| ProductSuite" ) 、 [**BitValues**](../wmisdk/standard-qualifiers.md) ( "Small Business"、"Enterprise"、"BackOffice"、"Communication Server"、"Terminal server"、"Small Business (受限的) "、"Embedded NT"、"Data Center" ) </span><span class="sxs-lookup"><span data-stu-id="fffbd-772">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\ProductOptions\|ProductSuite"), [**BitValues**](../wmisdk/standard-qualifiers.md) ("Small Business", "Enterprise", "BackOffice", "Communication Server", "Terminal Server", "Small Business(Restricted)", "Embedded NT", "Data Center")</span></span>
</dt> </dl>

<span data-ttu-id="fffbd-773">已安裝並授權系統產品新增至作業系統。</span><span class="sxs-lookup"><span data-stu-id="fffbd-773">Installed and licensed system product additions to the operating system.</span></span> <span data-ttu-id="fffbd-774">例如， **OSProductSuite** (0x92) 的146值表示企業、終端機服務和資料中心 (位1、四和七組) 。</span><span class="sxs-lookup"><span data-stu-id="fffbd-774">For example, the value of 146 (0x92) for **OSProductSuite** indicates Enterprise, Terminal Services, and Data Center (bits one, four, and seven set).</span></span> <span data-ttu-id="fffbd-775">下列清單列出可能的值。</span><span class="sxs-lookup"><span data-stu-id="fffbd-775">The following list lists possible values.</span></span>

<dt>

<span data-ttu-id="fffbd-776">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="fffbd-776">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-777">Microsoft Small Business Server 已安裝完成，但可能已升級至另一個版本的 Windows。</span><span class="sxs-lookup"><span data-stu-id="fffbd-777">Microsoft Small Business Server was once installed, but may have been upgraded to another version of Windows.</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-778">2 (0x2) </span><span class="sxs-lookup"><span data-stu-id="fffbd-778">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-779">已安裝 Windows Server 2008 Enterprise。</span><span class="sxs-lookup"><span data-stu-id="fffbd-779">Windows Server 2008 Enterprise is installed.</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-780">4 (0x4) </span><span class="sxs-lookup"><span data-stu-id="fffbd-780">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-781">已安裝 Windows BackOffice 元件。</span><span class="sxs-lookup"><span data-stu-id="fffbd-781">Windows BackOffice components are installed.</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-782">8 (0x8) </span><span class="sxs-lookup"><span data-stu-id="fffbd-782">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-783">已安裝通訊伺服器。</span><span class="sxs-lookup"><span data-stu-id="fffbd-783">Communication Server is installed.</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-784">16 (0x10) </span><span class="sxs-lookup"><span data-stu-id="fffbd-784">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-785">已安裝終端機服務。</span><span class="sxs-lookup"><span data-stu-id="fffbd-785">Terminal Services is installed.</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-786">32 (0x20) </span><span class="sxs-lookup"><span data-stu-id="fffbd-786">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-787">Microsoft Small Business Server 已安裝了嚴格的用戶端授權。</span><span class="sxs-lookup"><span data-stu-id="fffbd-787">Microsoft Small Business Server is installed with the restrictive client license.</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-788">64 (0x40) </span><span class="sxs-lookup"><span data-stu-id="fffbd-788">64 (0x40)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-789">已安裝 Windows Embedded。</span><span class="sxs-lookup"><span data-stu-id="fffbd-789">Windows Embedded is installed.</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-790">128 (0x80) </span><span class="sxs-lookup"><span data-stu-id="fffbd-790">128 (0x80)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-791">已安裝 Datacenter edition。</span><span class="sxs-lookup"><span data-stu-id="fffbd-791">A Datacenter edition is installed.</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-792">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="fffbd-792">256 (0x100)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-793">已安裝終端機服務，但只支援一個互動式會話。</span><span class="sxs-lookup"><span data-stu-id="fffbd-793">Terminal Services is installed, but only one interactive session is supported.</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-794">512 (0x200) </span><span class="sxs-lookup"><span data-stu-id="fffbd-794">512 (0x200)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-795">已安裝 Windows Home Edition。</span><span class="sxs-lookup"><span data-stu-id="fffbd-795">Windows Home Edition is installed.</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-796">1024 (0x400) </span><span class="sxs-lookup"><span data-stu-id="fffbd-796">1024 (0x400)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-797">已安裝 Web 服務器版本。</span><span class="sxs-lookup"><span data-stu-id="fffbd-797">Web Server Edition is installed.</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-798">8192 (0x2000) </span><span class="sxs-lookup"><span data-stu-id="fffbd-798">8192 (0x2000)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-799">已安裝 Storage Server Edition。</span><span class="sxs-lookup"><span data-stu-id="fffbd-799">Storage Server Edition is installed.</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-800">16384 (0x4000) </span><span class="sxs-lookup"><span data-stu-id="fffbd-800">16384 (0x4000)</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-801">已安裝 Compute Cluster Edition。</span><span class="sxs-lookup"><span data-stu-id="fffbd-801">Compute Cluster Edition is installed.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="fffbd-802">**OSType**</span><span class="sxs-lookup"><span data-stu-id="fffbd-802">**OSType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fffbd-803">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="fffbd-803">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-804">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fffbd-804">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-805">限定詞： [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 作業系統**](cim-operatingsystem.md)」。**OtherTypeDescription**") </span><span class="sxs-lookup"><span data-stu-id="fffbd-805">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**OtherTypeDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="fffbd-806">作業系統的類型。</span><span class="sxs-lookup"><span data-stu-id="fffbd-806">Type of operating system.</span></span> <span data-ttu-id="fffbd-807">下列清單會識別可能的值。</span><span class="sxs-lookup"><span data-stu-id="fffbd-807">The following list identifies the possible values.</span></span>

<span data-ttu-id="fffbd-808">這個屬性繼承自 [**CIM \_ 作業系統**](cim-operatingsystem.md)。</span><span class="sxs-lookup"><span data-stu-id="fffbd-808">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fffbd-809"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="fffbd-809"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="fffbd-810"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="fffbd-810"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="fffbd-811"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2) </span><span class="sxs-lookup"><span data-stu-id="fffbd-811"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="fffbd-812">宏</span><span class="sxs-lookup"><span data-stu-id="fffbd-812">MACROS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="fffbd-813"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3) </span><span class="sxs-lookup"><span data-stu-id="fffbd-813"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="fffbd-814"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4) </span><span class="sxs-lookup"><span data-stu-id="fffbd-814"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="fffbd-815"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5) </span><span class="sxs-lookup"><span data-stu-id="fffbd-815"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="fffbd-816"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**數位 Unix** (6) </span><span class="sxs-lookup"><span data-stu-id="fffbd-816"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="fffbd-817"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7) </span><span class="sxs-lookup"><span data-stu-id="fffbd-817"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="fffbd-818"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8) </span><span class="sxs-lookup"><span data-stu-id="fffbd-818"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="fffbd-819"><span id="AIX"></span><span id="aix"></span>**AIX** (9) </span><span class="sxs-lookup"><span data-stu-id="fffbd-819"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="fffbd-820"><span id="MVS"></span><span id="mvs"></span>**MVS** (10) </span><span class="sxs-lookup"><span data-stu-id="fffbd-820"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="fffbd-821"><span id="OS400"></span><span id="os400"></span>**OS400** (11) </span><span class="sxs-lookup"><span data-stu-id="fffbd-821"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="fffbd-822"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12) </span><span class="sxs-lookup"><span data-stu-id="fffbd-822"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="fffbd-823"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JAVAVM** (13) </span><span class="sxs-lookup"><span data-stu-id="fffbd-823"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="fffbd-824"><span id="MSDOS"></span><span id="msdos"></span>**Msdos.sys** (14) </span><span class="sxs-lookup"><span data-stu-id="fffbd-824"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="fffbd-825"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15) </span><span class="sxs-lookup"><span data-stu-id="fffbd-825"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="fffbd-826"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16) </span><span class="sxs-lookup"><span data-stu-id="fffbd-826"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="fffbd-827"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17) </span><span class="sxs-lookup"><span data-stu-id="fffbd-827"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="fffbd-828"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18) </span><span class="sxs-lookup"><span data-stu-id="fffbd-828"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="fffbd-829"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19) </span><span class="sxs-lookup"><span data-stu-id="fffbd-829"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="fffbd-830"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20) </span><span class="sxs-lookup"><span data-stu-id="fffbd-830"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="fffbd-831"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21) </span><span class="sxs-lookup"><span data-stu-id="fffbd-831"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="fffbd-832"><span id="OSF"></span><span id="osf"></span>**憑證** (22) </span><span class="sxs-lookup"><span data-stu-id="fffbd-832"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="fffbd-833"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23) </span><span class="sxs-lookup"><span data-stu-id="fffbd-833"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="fffbd-834"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>相依 **UNIX** (24) </span><span class="sxs-lookup"><span data-stu-id="fffbd-834"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="fffbd-835"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25) </span><span class="sxs-lookup"><span data-stu-id="fffbd-835"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="fffbd-836"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26) </span><span class="sxs-lookup"><span data-stu-id="fffbd-836"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="fffbd-837"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27) </span><span class="sxs-lookup"><span data-stu-id="fffbd-837"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="fffbd-838"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28) </span><span class="sxs-lookup"><span data-stu-id="fffbd-838"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="fffbd-839"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29) </span><span class="sxs-lookup"><span data-stu-id="fffbd-839"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd>

<span data-ttu-id="fffbd-840">Solaris</span><span class="sxs-lookup"><span data-stu-id="fffbd-840">Solaris</span></span>

</dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="fffbd-841"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30) </span><span class="sxs-lookup"><span data-stu-id="fffbd-841"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="fffbd-842"><span id="U6000"></span><span id="u6000"></span>**U6000** (31) </span><span class="sxs-lookup"><span data-stu-id="fffbd-842"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="fffbd-843"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32) </span><span class="sxs-lookup"><span data-stu-id="fffbd-843"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="fffbd-844"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33) </span><span class="sxs-lookup"><span data-stu-id="fffbd-844"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="fffbd-845"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34) </span><span class="sxs-lookup"><span data-stu-id="fffbd-845"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="fffbd-846"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35) </span><span class="sxs-lookup"><span data-stu-id="fffbd-846"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="fffbd-847"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36) </span><span class="sxs-lookup"><span data-stu-id="fffbd-847"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="fffbd-848"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37) </span><span class="sxs-lookup"><span data-stu-id="fffbd-848"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="fffbd-849"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38) </span><span class="sxs-lookup"><span data-stu-id="fffbd-849"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="fffbd-850"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39) </span><span class="sxs-lookup"><span data-stu-id="fffbd-850"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="fffbd-851"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**互動式 UNIX** (40) </span><span class="sxs-lookup"><span data-stu-id="fffbd-851"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="fffbd-852"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41) </span><span class="sxs-lookup"><span data-stu-id="fffbd-852"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="fffbd-853"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42) </span><span class="sxs-lookup"><span data-stu-id="fffbd-853"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="fffbd-854"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43) </span><span class="sxs-lookup"><span data-stu-id="fffbd-854"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="fffbd-855"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44) </span><span class="sxs-lookup"><span data-stu-id="fffbd-855"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="fffbd-856"><span id="OS9"></span><span id="os9"></span>**OS9** (45) </span><span class="sxs-lookup"><span data-stu-id="fffbd-856"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="fffbd-857"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**符合 Kernel** (46) </span><span class="sxs-lookup"><span data-stu-id="fffbd-857"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="fffbd-858"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47) </span><span class="sxs-lookup"><span data-stu-id="fffbd-858"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="fffbd-859"><span id="QNX"></span><span id="qnx"></span>**QNX** (48) </span><span class="sxs-lookup"><span data-stu-id="fffbd-859"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="fffbd-860"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49) </span><span class="sxs-lookup"><span data-stu-id="fffbd-860"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="fffbd-861"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50) </span><span class="sxs-lookup"><span data-stu-id="fffbd-861"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="fffbd-862"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51) </span><span class="sxs-lookup"><span data-stu-id="fffbd-862"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="fffbd-863"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52) </span><span class="sxs-lookup"><span data-stu-id="fffbd-863"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="fffbd-864"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53) </span><span class="sxs-lookup"><span data-stu-id="fffbd-864"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="fffbd-865"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54) </span><span class="sxs-lookup"><span data-stu-id="fffbd-865"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="fffbd-866"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55) </span><span class="sxs-lookup"><span data-stu-id="fffbd-866"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="fffbd-867"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56) </span><span class="sxs-lookup"><span data-stu-id="fffbd-867"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd></dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="fffbd-868"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57) </span><span class="sxs-lookup"><span data-stu-id="fffbd-868"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="fffbd-869"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58) </span><span class="sxs-lookup"><span data-stu-id="fffbd-869"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="fffbd-870"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**專用** (59) </span><span class="sxs-lookup"><span data-stu-id="fffbd-870"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_390"></span><span id="os_390"></span>

<span data-ttu-id="fffbd-871"><span id="OS_390"></span><span id="os_390"></span>**OS/390** (60) </span><span class="sxs-lookup"><span data-stu-id="fffbd-871"><span id="OS_390"></span><span id="os_390"></span>**OS/390** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="fffbd-872"><span id="VSE"></span><span id="vse"></span>**VSE** (61) </span><span class="sxs-lookup"><span data-stu-id="fffbd-872"><span id="VSE"></span><span id="vse"></span>**VSE** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="fffbd-873"><span id="TPF"></span><span id="tpf"></span>**TPF** (62) </span><span class="sxs-lookup"><span data-stu-id="fffbd-873"><span id="TPF"></span><span id="tpf"></span>**TPF** (62)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="fffbd-874">**OtherTypeDescription**</span><span class="sxs-lookup"><span data-stu-id="fffbd-874">**OtherTypeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fffbd-875">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fffbd-875">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-876">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fffbd-876">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-877">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) ， [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( "[**CIM \_ 作業系統**](cim-operatingsystem.md)。**OSType**") </span><span class="sxs-lookup"><span data-stu-id="fffbd-877">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**OSType**")</span></span>
</dt> </dl>

<span data-ttu-id="fffbd-878">目前作業系統版本的其他描述。</span><span class="sxs-lookup"><span data-stu-id="fffbd-878">Additional description for the current operating system version.</span></span>

<span data-ttu-id="fffbd-879">這個屬性繼承自 [**CIM \_ 作業系統**](cim-operatingsystem.md)。</span><span class="sxs-lookup"><span data-stu-id="fffbd-879">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-880">**PAEEnabled**</span><span class="sxs-lookup"><span data-stu-id="fffbd-880">**PAEEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fffbd-881">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="fffbd-881">Data type: **Boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-882">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fffbd-882">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fffbd-883">若 **為 True**，則會由在 Intel 處理器上執行的作業系統啟用 (PAE) 的實體位址延伸模組。</span><span class="sxs-lookup"><span data-stu-id="fffbd-883">If **True**, the physical address extensions (PAE) are enabled by the operating system running on Intel processors.</span></span> <span data-ttu-id="fffbd-884">PAE 可讓應用程式處理超過 4 GB 的實體記憶體。</span><span class="sxs-lookup"><span data-stu-id="fffbd-884">PAE allows applications to address more than 4 GB of physical memory.</span></span> <span data-ttu-id="fffbd-885">啟用 PAE 時，作業系統會使用三層級的線性位址轉譯，而不是兩個層級。</span><span class="sxs-lookup"><span data-stu-id="fffbd-885">When PAE is enabled, the operating system uses three-level linear address translation rather than two-level.</span></span> <span data-ttu-id="fffbd-886">為應用程式提供更多實體記憶體，可減少將記憶體交換至分頁檔的需求，並提升效能。</span><span class="sxs-lookup"><span data-stu-id="fffbd-886">Providing more physical memory to an application reduces the need to swap memory to the page file and increases performance.</span></span> <span data-ttu-id="fffbd-887">若要啟用，PAE，請使用 Boot.ini 檔案中的 "/PAE" 參數。</span><span class="sxs-lookup"><span data-stu-id="fffbd-887">To enable, PAE, use the "/PAE" switch in the Boot.ini file.</span></span> <span data-ttu-id="fffbd-888">如需實體位址延伸功能的詳細資訊，請參閱 <https://Go.Microsoft.Com/FWLink/p/?LinkID=45912> 。</span><span class="sxs-lookup"><span data-stu-id="fffbd-888">For more information about the Physical Address Extension feature, see <https://Go.Microsoft.Com/FWLink/p/?LinkID=45912>.</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-889">**PlusProductID**</span><span class="sxs-lookup"><span data-stu-id="fffbd-889">**PlusProductID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fffbd-890">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fffbd-890">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-891">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fffbd-891">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-892">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \| plus</span><span class="sxs-lookup"><span data-stu-id="fffbd-892">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\|Plus!</span></span> <span data-ttu-id="fffbd-893">ProductId ") </span><span class="sxs-lookup"><span data-stu-id="fffbd-893">ProductId")</span></span>
</dt> </dl>

<span data-ttu-id="fffbd-894">不支援。</span><span class="sxs-lookup"><span data-stu-id="fffbd-894">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-895">**PlusVersionNumber**</span><span class="sxs-lookup"><span data-stu-id="fffbd-895">**PlusVersionNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fffbd-896">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fffbd-896">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-897">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fffbd-897">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-898">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \| plus</span><span class="sxs-lookup"><span data-stu-id="fffbd-898">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\|Plus!</span></span> <span data-ttu-id="fffbd-899">VersionNumber ") </span><span class="sxs-lookup"><span data-stu-id="fffbd-899">VersionNumber")</span></span>
</dt> </dl>

<span data-ttu-id="fffbd-900">不支援。</span><span class="sxs-lookup"><span data-stu-id="fffbd-900">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-901">**PortableOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="fffbd-901">**PortableOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fffbd-902">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="fffbd-902">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-903">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fffbd-903">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fffbd-904">指定作業系統是否從外部 USB 裝置開機。</span><span class="sxs-lookup"><span data-stu-id="fffbd-904">Specifies whether the operating system booted from an external USB device.</span></span> <span data-ttu-id="fffbd-905">若為 true，表示作業系統偵測到在支援的本機連線存放裝置上開機。</span><span class="sxs-lookup"><span data-stu-id="fffbd-905">If true, the operating system has detected it is booting on a supported locally connected storage device.</span></span>

<span data-ttu-id="fffbd-906">**Windows server 2008 R2、windows 7、Windows server 2008 和 Windows Vista：** 在 Windows 8 和 Windows Server 2012 之前，不支援這個屬性。</span><span class="sxs-lookup"><span data-stu-id="fffbd-906">**Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 8 and Windows Server 2012.</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-907">**主要**</span><span class="sxs-lookup"><span data-stu-id="fffbd-907">**Primary**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fffbd-908">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="fffbd-908">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-909">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fffbd-909">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-910">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI" ) </span><span class="sxs-lookup"><span data-stu-id="fffbd-910">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="fffbd-911">指定這是否為主要作業系統。</span><span class="sxs-lookup"><span data-stu-id="fffbd-911">Specifies whether this is the primary operating system.</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-912">**ProductType**</span><span class="sxs-lookup"><span data-stu-id="fffbd-912">**ProductType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fffbd-913">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="fffbd-913">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-914">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fffbd-914">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fffbd-915">其他系統資訊。</span><span class="sxs-lookup"><span data-stu-id="fffbd-915">Additional system information.</span></span>

<dt>

<span id="Work_Station"></span><span id="work_station"></span><span id="WORK_STATION"></span>

<span data-ttu-id="fffbd-916">**工作站** (1) </span><span class="sxs-lookup"><span data-stu-id="fffbd-916">**Work Station** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Domain_Controller"></span><span id="domain_controller"></span><span id="DOMAIN_CONTROLLER"></span>

<span data-ttu-id="fffbd-917">**網域控制站** (2) </span><span class="sxs-lookup"><span data-stu-id="fffbd-917">**Domain Controller** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Server"></span><span id="server"></span><span id="SERVER"></span>

<span data-ttu-id="fffbd-918">**伺服器** (3) </span><span class="sxs-lookup"><span data-stu-id="fffbd-918">**Server** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="fffbd-919">**QuantumLength**</span><span class="sxs-lookup"><span data-stu-id="fffbd-919">**QuantumLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fffbd-920">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="fffbd-920">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-921">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="fffbd-921">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-922">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ PriorityControl \| Win32PrioritySeparation" ) </span><span class="sxs-lookup"><span data-stu-id="fffbd-922">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\PriorityControl\|Win32PrioritySeparation")</span></span>
</dt> </dl>

<span data-ttu-id="fffbd-923">不支援</span><span class="sxs-lookup"><span data-stu-id="fffbd-923">Not supported</span></span>

<span data-ttu-id="fffbd-924">\* \* Windows Server 2008 和 Windows Vista： \* \*</span><span class="sxs-lookup"><span data-stu-id="fffbd-924">\*\*Windows Server 2008 and Windows Vista:  \*\*</span></span>

<span data-ttu-id="fffbd-925">**QuantumLength** 屬性會定義每個量子的時鐘刻度數目。</span><span class="sxs-lookup"><span data-stu-id="fffbd-925">The **QuantumLength** property defines the number of clock ticks per quantum.</span></span> <span data-ttu-id="fffbd-926">量子是在切換至其他應用程式之前，允許排程器提供給應用程式的執行時間單位。</span><span class="sxs-lookup"><span data-stu-id="fffbd-926">A quantum is a unit of execution time that the scheduler is allowed to give to an application before switching to other applications.</span></span> <span data-ttu-id="fffbd-927">當執行緒執行一個量子時，核心會 shutdown 它，並將其移至具有相同優先順序的應用程式佇列結尾。</span><span class="sxs-lookup"><span data-stu-id="fffbd-927">When a thread runs one quantum, the kernel preempts it and moves it to the end of a queue for applications with equal priorities.</span></span> <span data-ttu-id="fffbd-928">執行緒的量子的實際長度會因不同的 Windows 平臺而異。</span><span class="sxs-lookup"><span data-stu-id="fffbd-928">The actual length of a thread's quantum varies across different Windows platforms.</span></span> <span data-ttu-id="fffbd-929">僅限 Windows NT/Windows 2000。</span><span class="sxs-lookup"><span data-stu-id="fffbd-929">For Windows NT/Windows 2000 only.</span></span>

<span data-ttu-id="fffbd-930">可能的值為。</span><span class="sxs-lookup"><span data-stu-id="fffbd-930">The possible values are.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fffbd-931">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="fffbd-931">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="One_tick"></span><span id="one_tick"></span><span id="ONE_TICK"></span>

<span data-ttu-id="fffbd-932">**一個刻度** (1) </span><span class="sxs-lookup"><span data-stu-id="fffbd-932">**One tick** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Two_ticks"></span><span id="two_ticks"></span><span id="TWO_TICKS"></span>

<span data-ttu-id="fffbd-933">**兩個刻度** (2) </span><span class="sxs-lookup"><span data-stu-id="fffbd-933">**Two ticks** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="fffbd-934">**QuantumType**</span><span class="sxs-lookup"><span data-stu-id="fffbd-934">**QuantumType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fffbd-935">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="fffbd-935">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-936">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="fffbd-936">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="fffbd-937">不支援</span><span class="sxs-lookup"><span data-stu-id="fffbd-937">Not supported</span></span>

<span data-ttu-id="fffbd-938">\* \* Windows Server 2008 和 Windows Vista： \* \*</span><span class="sxs-lookup"><span data-stu-id="fffbd-938">\*\*Windows Server 2008 and Windows Vista:  \*\*</span></span>

<span data-ttu-id="fffbd-939">**QuantumType** 屬性會指定固定或可變長度的量程。</span><span class="sxs-lookup"><span data-stu-id="fffbd-939">The **QuantumType** property specifies either fixed or variable length quantums.</span></span> <span data-ttu-id="fffbd-940">Windows 預設為可變長度的量子，其中前景應用程式的量子比背景應用程式更長。</span><span class="sxs-lookup"><span data-stu-id="fffbd-940">Windows defaults to variable length quantums where the foreground application has a longer quantum than the background applications.</span></span> <span data-ttu-id="fffbd-941">Windows Server 預設為固定長度的量程。</span><span class="sxs-lookup"><span data-stu-id="fffbd-941">Windows Server defaults to fixed-length quantums.</span></span> <span data-ttu-id="fffbd-942">量子是在切換到另一個應用程式之前，允許排程器提供給應用程式的執行時間單位。</span><span class="sxs-lookup"><span data-stu-id="fffbd-942">A quantum is a unit of execution time that the scheduler is allowed to give to an application before switching to another application.</span></span> <span data-ttu-id="fffbd-943">當執行緒執行一個量子時，核心會 shutdown 它，並將其移至具有相同優先順序的應用程式佇列結尾。</span><span class="sxs-lookup"><span data-stu-id="fffbd-943">When a thread runs one quantum, the kernel preempts it and moves it to the end of a queue for applications with equal priorities.</span></span> <span data-ttu-id="fffbd-944">執行緒的量子的實際長度會因不同的 Windows 平臺而異。</span><span class="sxs-lookup"><span data-stu-id="fffbd-944">The actual length of a thread's quantum varies across different Windows platforms.</span></span>

<span data-ttu-id="fffbd-945">可能的值為。</span><span class="sxs-lookup"><span data-stu-id="fffbd-945">The possible values are.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fffbd-946">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="fffbd-946">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Fixed"></span><span id="fixed"></span><span id="FIXED"></span>

<span data-ttu-id="fffbd-947">已 **修正** (1) </span><span class="sxs-lookup"><span data-stu-id="fffbd-947">**Fixed** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Variable"></span><span id="variable"></span><span id="VARIABLE"></span>

<span data-ttu-id="fffbd-948">**變數** (2) </span><span class="sxs-lookup"><span data-stu-id="fffbd-948">**Variable** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="fffbd-949">**RegisteredUser**</span><span class="sxs-lookup"><span data-stu-id="fffbd-949">**RegisteredUser**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fffbd-950">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fffbd-950">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-951">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fffbd-951">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-952">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \| >registeredowner" ) </span><span class="sxs-lookup"><span data-stu-id="fffbd-952">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\|RegisteredOwner")</span></span>
</dt> </dl>

<span data-ttu-id="fffbd-953">作業系統的已註冊使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="fffbd-953">Name of the registered user of the operating system.</span></span>

<span data-ttu-id="fffbd-954">範例： "Ben Smith"</span><span class="sxs-lookup"><span data-stu-id="fffbd-954">Example: "Ben Smith"</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-955">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="fffbd-955">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fffbd-956">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fffbd-956">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-957">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fffbd-957">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-958">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \| ProductId" ) </span><span class="sxs-lookup"><span data-stu-id="fffbd-958">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\|ProductId")</span></span>
</dt> </dl>

<span data-ttu-id="fffbd-959">作業系統產品序列識別碼。</span><span class="sxs-lookup"><span data-stu-id="fffbd-959">Operating system product serial identification number.</span></span>

<span data-ttu-id="fffbd-960">範例： "10497-OEM-0031416-71674"</span><span class="sxs-lookup"><span data-stu-id="fffbd-960">Example: "10497-OEM-0031416-71674"</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-961">**ServicePackMajorVersion**</span><span class="sxs-lookup"><span data-stu-id="fffbd-961">**ServicePackMajorVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fffbd-962">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="fffbd-962">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-963">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fffbd-963">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-964">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| 系統資訊結構 \| [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) \| **wServicePackMajor**" ) </span><span class="sxs-lookup"><span data-stu-id="fffbd-964">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|System Information Structures\|[**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa)\|**wServicePackMajor**")</span></span>
</dt> </dl>

<span data-ttu-id="fffbd-965">電腦系統上所安裝 service pack 的主要版本號碼。</span><span class="sxs-lookup"><span data-stu-id="fffbd-965">Major version number of the service pack installed on the computer system.</span></span> <span data-ttu-id="fffbd-966">如果未安裝 service pack，則值為 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="fffbd-966">If no service pack has been installed, the value is 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-967">**ServicePackMinorVersion**</span><span class="sxs-lookup"><span data-stu-id="fffbd-967">**ServicePackMinorVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fffbd-968">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="fffbd-968">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-969">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fffbd-969">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-970">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| 系統資訊結構 \| [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) \| **wServicePackMinor**" ) </span><span class="sxs-lookup"><span data-stu-id="fffbd-970">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|System Information Structures\|[**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa)\|**wServicePackMinor**")</span></span>
</dt> </dl>

<span data-ttu-id="fffbd-971">電腦系統上安裝之 service pack 的次要版本號碼。</span><span class="sxs-lookup"><span data-stu-id="fffbd-971">Minor version number of the service pack installed on the computer system.</span></span> <span data-ttu-id="fffbd-972">如果未安裝 service pack，則值為 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="fffbd-972">If no service pack has been installed, the value is 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-973">**SizeStoredInPagingFiles**</span><span class="sxs-lookup"><span data-stu-id="fffbd-973">**SizeStoredInPagingFiles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fffbd-974">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="fffbd-974">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-975">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fffbd-975">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-976">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 系統記憶體設定 \| 001.3 ") ， [**單位**](../wmisdk/standard-qualifiers.md) (" kb ") </span><span class="sxs-lookup"><span data-stu-id="fffbd-976">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|System Memory Settings\|001.3"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="fffbd-977">作業系統分頁檔案中可儲存的 kb 總數— 0 (零) 表示沒有分頁檔案。</span><span class="sxs-lookup"><span data-stu-id="fffbd-977">Total number of kilobytes that can be stored in the operating system paging files—0 (zero) indicates that there are no paging files.</span></span> <span data-ttu-id="fffbd-978">請注意，此數目不代表磁片上分頁檔案的實際實際大小。</span><span class="sxs-lookup"><span data-stu-id="fffbd-978">Be aware that this number does not represent the actual physical size of the paging file on disk.</span></span>

<span data-ttu-id="fffbd-979">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="fffbd-979">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="fffbd-980">這個屬性繼承自 [**CIM \_ 作業系統**](cim-operatingsystem.md)。</span><span class="sxs-lookup"><span data-stu-id="fffbd-980">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-981">**狀態**</span><span class="sxs-lookup"><span data-stu-id="fffbd-981">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fffbd-982">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fffbd-982">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-983">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fffbd-983">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-984">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (10) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="fffbd-984">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="fffbd-985">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="fffbd-985">Current status of the object.</span></span> <span data-ttu-id="fffbd-986">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="fffbd-986">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="fffbd-987">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素，例如智慧型啟用的硬碟可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="fffbd-987">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive may function properly, but predicts a failure in the near future).</span></span> <span data-ttu-id="fffbd-988">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="fffbd-988">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="fffbd-989">服務狀態適用于系統管理工作，例如磁片的鏡像重新同步處理、重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="fffbd-989">The Service status applies to administrative work, such as mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="fffbd-990">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="fffbd-990">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="fffbd-991">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="fffbd-991">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="fffbd-992">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="fffbd-992">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="fffbd-993">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="fffbd-993">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="fffbd-994">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="fffbd-994">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fffbd-995">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="fffbd-995">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="fffbd-996">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="fffbd-996">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="fffbd-997">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="fffbd-997">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="fffbd-998">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="fffbd-998">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="fffbd-999">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="fffbd-999">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="fffbd-1000">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="fffbd-1000">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="fffbd-1001">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="fffbd-1001">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="fffbd-1002">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="fffbd-1002">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="fffbd-1003">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="fffbd-1003">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="fffbd-1004">**SuiteMask**</span><span class="sxs-lookup"><span data-stu-id="fffbd-1004">**SuiteMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fffbd-1005">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="fffbd-1005">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-1006">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fffbd-1006">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-1007">限定詞： [**BitMap**](../wmisdk/standard-qualifiers.md) ( "0"、"1"、"2"、"3"、"4"、"5"、"6"、"7"、"8"、"9"、"10" ) 、 [**BitValues**](../wmisdk/standard-qualifiers.md) ( "Windows Server Small Business Edition"、"Windows server、Enterprise Edition"、"Windows server，Backoffice Edition"、"Windows server，communication Edition"、"Microsoft Terminal Services"、"Windows Server，Small Business edition 限制"、"windows Embedded"、"Windows server、Datacenter Edition"、"Single User"、"Windows server、Datacenter edition"、"Windows server、Web edition" ) </span><span class="sxs-lookup"><span data-stu-id="fffbd-1007">Qualifiers: [**BitMap**](../wmisdk/standard-qualifiers.md) ("0", "1", "2", "3", "4", "5", "6", "7", "8", "9", "10"), [**BitValues**](../wmisdk/standard-qualifiers.md) ("Windows Server, Small Business Edition", "Windows Server, Enterprise Edition", "Windows Server, Backoffice Edition", "Windows Server, Communications Edition", "Microsoft Terminal Services", "Windows Server, Small Business Edition Restricted", "Windows Embedded", "Windows Server, Datacenter Edition", "Single User", "Windows Home Edition", "Windows Server, Web Edition")</span></span>
</dt> </dl>

<span data-ttu-id="fffbd-1008">識別系統上可用之產品套件的位旗標。</span><span class="sxs-lookup"><span data-stu-id="fffbd-1008">Bit flags that identify the product suites available on the system.</span></span>

<span data-ttu-id="fffbd-1009">例如，若要同時指定個人和 BackOffice，請將 **SuiteMask** 設定為 `4 | 512` 或 `516` 。</span><span class="sxs-lookup"><span data-stu-id="fffbd-1009">For example, to specify both Personal and BackOffice, set **SuiteMask** to `4 | 512` or `516`.</span></span>

<dt>

<span data-ttu-id="fffbd-1010">1</span><span class="sxs-lookup"><span data-stu-id="fffbd-1010">1</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-1011">小型企業</span><span class="sxs-lookup"><span data-stu-id="fffbd-1011">Small Business</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-1012">2</span><span class="sxs-lookup"><span data-stu-id="fffbd-1012">2</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-1013">Enterprise</span><span class="sxs-lookup"><span data-stu-id="fffbd-1013">Enterprise</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-1014">4</span><span class="sxs-lookup"><span data-stu-id="fffbd-1014">4</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-1015">BackOffice</span><span class="sxs-lookup"><span data-stu-id="fffbd-1015">BackOffice</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-1016">8</span><span class="sxs-lookup"><span data-stu-id="fffbd-1016">8</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-1017">通訊</span><span class="sxs-lookup"><span data-stu-id="fffbd-1017">Communications</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-1018">16</span><span class="sxs-lookup"><span data-stu-id="fffbd-1018">16</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-1019">終端機服務</span><span class="sxs-lookup"><span data-stu-id="fffbd-1019">Terminal Services</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-1020">32</span><span class="sxs-lookup"><span data-stu-id="fffbd-1020">32</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-1021">小型企業受限</span><span class="sxs-lookup"><span data-stu-id="fffbd-1021">Small Business Restricted</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-1022">64</span><span class="sxs-lookup"><span data-stu-id="fffbd-1022">64</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-1023">Embedded Edition</span><span class="sxs-lookup"><span data-stu-id="fffbd-1023">Embedded Edition</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-1024">128</span><span class="sxs-lookup"><span data-stu-id="fffbd-1024">128</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-1025">Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="fffbd-1025">Datacenter Edition</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-1026">256</span><span class="sxs-lookup"><span data-stu-id="fffbd-1026">256</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-1027">單一使用者</span><span class="sxs-lookup"><span data-stu-id="fffbd-1027">Single User</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-1028">512</span><span class="sxs-lookup"><span data-stu-id="fffbd-1028">512</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-1029">Home Edition</span><span class="sxs-lookup"><span data-stu-id="fffbd-1029">Home Edition</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-1030">1024</span><span class="sxs-lookup"><span data-stu-id="fffbd-1030">1024</span></span>
</dt> <dd>

<span data-ttu-id="fffbd-1031">Web 服務器版本</span><span class="sxs-lookup"><span data-stu-id="fffbd-1031">Web Server Edition</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="fffbd-1032">**SystemDevice**</span><span class="sxs-lookup"><span data-stu-id="fffbd-1032">**SystemDevice**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fffbd-1033">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fffbd-1033">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-1034">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fffbd-1034">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-1035">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Registry 函數 \| [**GetPrivateProfileString**](/windows/win32/api/winbase/nf-winbase-getprivateprofilestring) \| Paths \| TargetDevice" ) </span><span class="sxs-lookup"><span data-stu-id="fffbd-1035">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Registry Functions\|[**GetPrivateProfileString**](/windows/win32/api/winbase/nf-winbase-getprivateprofilestring)\|Paths\|TargetDevice")</span></span>
</dt> </dl>

<span data-ttu-id="fffbd-1036">作業系統安裝所在的實體磁碟分割。</span><span class="sxs-lookup"><span data-stu-id="fffbd-1036">Physical disk partition on which the operating system is installed.</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-1037">**SystemDirectory**</span><span class="sxs-lookup"><span data-stu-id="fffbd-1037">**SystemDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fffbd-1038">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fffbd-1038">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-1039">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fffbd-1039">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-1040">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| 系統資訊函數 [**GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya)) </span><span class="sxs-lookup"><span data-stu-id="fffbd-1040">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|System Information Functions [**GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya))</span></span>
</dt> </dl>

<span data-ttu-id="fffbd-1041">作業系統的系統目錄。</span><span class="sxs-lookup"><span data-stu-id="fffbd-1041">System directory of the operating system.</span></span>

<span data-ttu-id="fffbd-1042">範例： "C： \\ WINDOWS \\ SYSTEM32"</span><span class="sxs-lookup"><span data-stu-id="fffbd-1042">Example: "C:\\WINDOWS\\SYSTEM32"</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-1043">**SystemDrive**</span><span class="sxs-lookup"><span data-stu-id="fffbd-1043">**SystemDrive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fffbd-1044">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fffbd-1044">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-1045">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fffbd-1045">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fffbd-1046">作業系統所在磁片磁碟機的字母。</span><span class="sxs-lookup"><span data-stu-id="fffbd-1046">Letter of the disk drive on which the operating system resides.</span></span> <span data-ttu-id="fffbd-1047">範例： "C："</span><span class="sxs-lookup"><span data-stu-id="fffbd-1047">Example: "C:"</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-1048">**TotalSwapSpaceSize**</span><span class="sxs-lookup"><span data-stu-id="fffbd-1048">**TotalSwapSpaceSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fffbd-1049">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="fffbd-1049">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-1050">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fffbd-1050">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-1051">限定詞： [**單位**](../wmisdk/standard-qualifiers.md) ( "kb" ) </span><span class="sxs-lookup"><span data-stu-id="fffbd-1051">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="fffbd-1052">交換空間總計（以 kb 為單位）。</span><span class="sxs-lookup"><span data-stu-id="fffbd-1052">Total swap space in kilobytes.</span></span> <span data-ttu-id="fffbd-1053">如果交換空間與分頁檔不區分，則此值可能是 **Null** (未指定) 。</span><span class="sxs-lookup"><span data-stu-id="fffbd-1053">This value may be **NULL** (unspecified) if the swap space is not distinguished from page files.</span></span> <span data-ttu-id="fffbd-1054">不過，有些作業系統會區分這些概念。</span><span class="sxs-lookup"><span data-stu-id="fffbd-1054">However, some operating systems distinguish these concepts.</span></span> <span data-ttu-id="fffbd-1055">例如，在 UNIX 中，當免費頁面清單落在低於指定的數量時，可以將整個進程交換。</span><span class="sxs-lookup"><span data-stu-id="fffbd-1055">For example, in UNIX, whole processes can be swapped out when the free page list falls and remains below a specified amount.</span></span>

<span data-ttu-id="fffbd-1056">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="fffbd-1056">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="fffbd-1057">這個屬性繼承自 [**CIM \_ 作業系統**](cim-operatingsystem.md)。</span><span class="sxs-lookup"><span data-stu-id="fffbd-1057">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-1058">**TotalVirtualMemorySize**</span><span class="sxs-lookup"><span data-stu-id="fffbd-1058">**TotalVirtualMemorySize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fffbd-1059">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="fffbd-1059">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-1060">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fffbd-1060">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-1061">限定詞： [**單位**](../wmisdk/standard-qualifiers.md) ( "kb" ) </span><span class="sxs-lookup"><span data-stu-id="fffbd-1061">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="fffbd-1062">虛擬記憶體的數目（以 kb 為單位）。</span><span class="sxs-lookup"><span data-stu-id="fffbd-1062">Number, in kilobytes, of virtual memory.</span></span> <span data-ttu-id="fffbd-1063">例如，這可能是藉由將總 RAM 的數量新增至分頁空間量來計算，也就是將電腦系統的記憶體數量新增或匯總至屬性 **SizeStoredInPagingFiles**。</span><span class="sxs-lookup"><span data-stu-id="fffbd-1063">For example, this may be calculated by adding the amount of total RAM to the amount of paging space, that is, adding the amount of memory in or aggregated by the computer system to the property, **SizeStoredInPagingFiles**.</span></span>

<span data-ttu-id="fffbd-1064">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="fffbd-1064">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="fffbd-1065">這個屬性繼承自 [**CIM \_ 作業系統**](cim-operatingsystem.md)。</span><span class="sxs-lookup"><span data-stu-id="fffbd-1065">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-1066">**TotalVisibleMemorySize**</span><span class="sxs-lookup"><span data-stu-id="fffbd-1066">**TotalVisibleMemorySize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fffbd-1067">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="fffbd-1067">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-1068">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fffbd-1068">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-1069">限定詞： [**單位**](../wmisdk/standard-qualifiers.md) ( "kb" ) </span><span class="sxs-lookup"><span data-stu-id="fffbd-1069">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="fffbd-1070">作業系統可用的實體記憶體總量（以 kb 為單位）。</span><span class="sxs-lookup"><span data-stu-id="fffbd-1070">Total amount, in kilobytes, of physical memory available to the operating system.</span></span> <span data-ttu-id="fffbd-1071">此值不一定會指出真正的實體記憶體數量，而是向作業系統回報的可用記憶體。</span><span class="sxs-lookup"><span data-stu-id="fffbd-1071">This value does not necessarily indicate the true amount of physical memory, but what is reported to the operating system as available to it.</span></span>

<span data-ttu-id="fffbd-1072">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="fffbd-1072">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="fffbd-1073">這個屬性繼承自 [**CIM \_ 作業系統**](cim-operatingsystem.md)。</span><span class="sxs-lookup"><span data-stu-id="fffbd-1073">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-1074">**版本**</span><span class="sxs-lookup"><span data-stu-id="fffbd-1074">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fffbd-1075">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fffbd-1075">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-1076">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fffbd-1076">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-1077">限定詞：覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "Version" ) ， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| 系統資訊結構 \| [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) \| dwMajorVersion，dwMinorVersion" ) </span><span class="sxs-lookup"><span data-stu-id="fffbd-1077">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Version"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|System Information Structures\|[**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa)\|dwMajorVersion, dwMinorVersion")</span></span>
</dt> </dl>

<span data-ttu-id="fffbd-1078">作業系統的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="fffbd-1078">Version number of the operating system.</span></span>

<span data-ttu-id="fffbd-1079">範例： "4.0"</span><span class="sxs-lookup"><span data-stu-id="fffbd-1079">Example: "4.0"</span></span>

</dd> <dt>

<span data-ttu-id="fffbd-1080">**WindowsDirectory**</span><span class="sxs-lookup"><span data-stu-id="fffbd-1080">**WindowsDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fffbd-1081">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fffbd-1081">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-1082">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fffbd-1082">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fffbd-1083">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| 系統資訊函數 \| [**GetWindowsDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya)" ) </span><span class="sxs-lookup"><span data-stu-id="fffbd-1083">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|System Information Functions\|[**GetWindowsDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya)")</span></span>
</dt> </dl>

<span data-ttu-id="fffbd-1084">作業系統的 Windows 目錄。</span><span class="sxs-lookup"><span data-stu-id="fffbd-1084">Windows directory of the operating system.</span></span>

<span data-ttu-id="fffbd-1085">範例： "C： \\ WINDOWS"</span><span class="sxs-lookup"><span data-stu-id="fffbd-1085">Example: "C:\\WINDOWS"</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fffbd-1086">備註</span><span class="sxs-lookup"><span data-stu-id="fffbd-1086">Remarks</span></span>

<span data-ttu-id="fffbd-1087">**Win32 \_ 作業系統** 類別衍生自 [**CIM \_ 作業系統**](cim-operatingsystem.md)。</span><span class="sxs-lookup"><span data-stu-id="fffbd-1087">The **Win32\_OperatingSystem** class is derived from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

<span data-ttu-id="fffbd-1088">可以安裝在可執行 Windows 作業系統之電腦上的任何作業系統都是此類別的子系或成員。</span><span class="sxs-lookup"><span data-stu-id="fffbd-1088">Any operating system that can be installed on a computer that can run a Windows-based operating system is a descendant or member of this class.</span></span> <span data-ttu-id="fffbd-1089">**Win32 \_作業系統** 是單一類別。</span><span class="sxs-lookup"><span data-stu-id="fffbd-1089">**Win32\_OperatingSystem** is a singleton class.</span></span> <span data-ttu-id="fffbd-1090">若要取得單一實例，請使用 "@" 作為索引鍵。</span><span class="sxs-lookup"><span data-stu-id="fffbd-1090">To get the single instance, use "@" for the key.</span></span>

<span data-ttu-id="fffbd-1091">不同于 Mgmtclassgen.exe 所產生的其他大部分 WMI 類別， **作業系統 CreateInstance** () 方法會傳回空白的 **作業系統** 物件。</span><span class="sxs-lookup"><span data-stu-id="fffbd-1091">Unlike most of the other WMI classes generated by MgmtClassGen, the **OperatingSystem.CreateInstance**() method will return a blank **OperatingSystem** object.</span></span> <span data-ttu-id="fffbd-1092">因此，如果您使用 C 搭配 \# mgmtclassgen.exe，您可以使用下列程式碼：</span><span class="sxs-lookup"><span data-stu-id="fffbd-1092">Therefore, if you are using C\# with MgmtClassGen, you can use the following code:</span></span>


```CSharp
WMI.OperatingSystem os = new ROOT.CIMV2.win32.OperatingSystem();
```



## <a name="examples"></a><span data-ttu-id="fffbd-1093">範例</span><span class="sxs-lookup"><span data-stu-id="fffbd-1093">Examples</span></span>

<span data-ttu-id="fffbd-1094">您可以在 [**win32 \_ 處理器**](win32-processor.md)主題範例中找到 VBScript 範例，以取得 [**win32 \_**](win32-computersystem.md)系統、 [**win32 \_ 處理器**](win32-processor.md)和 **win32 作業系統 \_** 的作業系統和處理器資料。</span><span class="sxs-lookup"><span data-stu-id="fffbd-1094">You can find a VBScript example that obtains operating system and processor data from [**Win32\_ComputerSystem**](win32-computersystem.md), [**Win32\_Processor**](win32-processor.md), and **Win32\_OperatingSystem** in the [**Win32\_Processor**](win32-processor.md) topic examples.</span></span>

<span data-ttu-id="fffbd-1095">在 TechNet 資源庫上 [使用 powershell powershell 範例產生 Exchange 環境報告](https://Gallery.TechNet.Microsoft.Com/scriptcenter/Generate-Exchange-2388e7c9) ，會使用 **Win32 \_ 作業系統** 類別做為較大應用程式的一部分，以產生 Exchange 環境報告。</span><span class="sxs-lookup"><span data-stu-id="fffbd-1095">The [Generate Exchange Environment Reports using Powershell](https://Gallery.TechNet.Microsoft.Com/scriptcenter/Generate-Exchange-2388e7c9) PowerShell sample on TechNet Gallery uses a **Win32\_OperatingSystem** class as part of a larger application to generate exchange environment reports.</span></span>

<span data-ttu-id="fffbd-1096">TechNet 資源庫中的「 [使用 WMI 取得伺服器執行時間](https://Gallery.TechNet.Microsoft.Com/Get-Server-Uptime-Using-WMI-15aaa8ac) 」範例會使用 **LastBootupTime** 屬性來判斷伺服器的作用時間。</span><span class="sxs-lookup"><span data-stu-id="fffbd-1096">The [Get Server Uptime Using WMI](https://Gallery.TechNet.Microsoft.Com/Get-Server-Uptime-Using-WMI-15aaa8ac) sample in the TechNet Gallery uses the **LastBootupTime** property to determine how long the server has been active.</span></span> <span data-ttu-id="fffbd-1097">此範例也會使用 timeout 選項，以確保 WMI 呼叫不會停止回應。</span><span class="sxs-lookup"><span data-stu-id="fffbd-1097">The sample also uses the timeout option to ensure that the WMI call does not hang.</span></span>

<span data-ttu-id="fffbd-1098">TechNet 資源庫上的 [WMI 資訊](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) 取回程序 VBScript 程式碼範例會使用 **Win32 \_ 作業系統** 類別，從多部遠端電腦抓取作業系統資訊。</span><span class="sxs-lookup"><span data-stu-id="fffbd-1098">The [WMI Information Retriever](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) VBScript code example on the TechNet Gallery uses the **Win32\_OperatingSystem** class to retrieve OS information from a number of remote computers.</span></span>

<span data-ttu-id="fffbd-1099">下列腳本會取得預設「根 CIMv2」命名空間中的 **Win32 \_ 作業系統** 實例 \\ ，然後顯示作業系統的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="fffbd-1099">The following script obtains the instances of **Win32\_OperatingSystem** in the default "Root\\CIMv2" namespace, and then displays information about the operating system.</span></span>


```VB
On Error Resume Next
' Connect to WMI and obtain instances of Win32_OperatingSystem
For Each objOS in GetObject( _
    "winmgmts:").InstancesOf ("Win32_OperatingSystem")

WScript.Echo "Name = " & objOS.Caption & "Version = " & objOS.Version &VBCR _
           & "Registered User = " & objOS.RegisteredUser &VBCR _
           & "Manufacturer = " & objOS.Manufacturer      
Next

if Err <> 0 Then
    WScript.Echo Err.Description
    Err.Clear
End if
```



<span data-ttu-id="fffbd-1100">下列 PowerShell 程式碼範例會顯示有關目前作業系統的所有操作資訊。</span><span class="sxs-lookup"><span data-stu-id="fffbd-1100">The following PowerShell code sample displays all the operating information about the current OS.</span></span>


```PowerShell
# get instance
$os = Get-WmiObject Win32_OperatingSystem

# output information:
"The class has {0} properties" -f $os.properties.count
"Details on this class:"
$os | Format-List *
```



## <a name="requirements"></a><span data-ttu-id="fffbd-1101">規格需求</span><span class="sxs-lookup"><span data-stu-id="fffbd-1101">Requirements</span></span>



| <span data-ttu-id="fffbd-1102">需求</span><span class="sxs-lookup"><span data-stu-id="fffbd-1102">Requirement</span></span> | <span data-ttu-id="fffbd-1103">值</span><span class="sxs-lookup"><span data-stu-id="fffbd-1103">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fffbd-1104">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fffbd-1104">Minimum supported client</span></span><br/> | <span data-ttu-id="fffbd-1105">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fffbd-1105">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fffbd-1106">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fffbd-1106">Minimum supported server</span></span><br/> | <span data-ttu-id="fffbd-1107">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fffbd-1107">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fffbd-1108">命名空間</span><span class="sxs-lookup"><span data-stu-id="fffbd-1108">Namespace</span></span><br/>                | <span data-ttu-id="fffbd-1109">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="fffbd-1109">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fffbd-1110">MOF</span><span class="sxs-lookup"><span data-stu-id="fffbd-1110">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fffbd-1111"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="fffbd-1111"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fffbd-1112">DLL</span><span class="sxs-lookup"><span data-stu-id="fffbd-1112">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fffbd-1113"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fffbd-1113"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fffbd-1114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fffbd-1114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fffbd-1115">**CIM \_ 作業系統**</span><span class="sxs-lookup"><span data-stu-id="fffbd-1115">**CIM\_OperatingSystem**</span></span>](cim-operatingsystem.md)
</dt> <dt>

[<span data-ttu-id="fffbd-1116">作業系統類別</span><span class="sxs-lookup"><span data-stu-id="fffbd-1116">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> <dt>

[<span data-ttu-id="fffbd-1117">WMI 工作：作業系統</span><span class="sxs-lookup"><span data-stu-id="fffbd-1117">WMI Tasks: Operating Systems</span></span>](../wmisdk/wmi-tasks--operating-systems.md)
</dt> <dt>

[<span data-ttu-id="fffbd-1118">WMI 工作：電腦硬體</span><span class="sxs-lookup"><span data-stu-id="fffbd-1118">WMI Tasks: Computer Hardware</span></span>](../wmisdk/wmi-tasks--computer-hardware.md)
</dt> <dt>

[<span data-ttu-id="fffbd-1119">WMI 工作：桌面管理</span><span class="sxs-lookup"><span data-stu-id="fffbd-1119">WMI Tasks: Desktop Management</span></span>](../wmisdk/wmi-tasks--desktop-management.md)
</dt> </dl>

 

 
