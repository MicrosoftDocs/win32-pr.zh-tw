---
description: Win32 \_ StartupCommand&\# 8194;WMI 類別代表當使用者登入電腦系統時自動執行的命令。
ms.assetid: 7184ade8-fcc9-47b3-af04-8054b2fca937
ms.tgt_platform: multiple
title: Win32_StartupCommand 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_StartupCommand
- Win32_StartupCommand.Caption
- Win32_StartupCommand.Description
- Win32_StartupCommand.SettingID
- Win32_StartupCommand.Command
- Win32_StartupCommand.Location
- Win32_StartupCommand.Name
- Win32_StartupCommand.User
- Win32_StartupCommand.UserSID
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1c38ec84b9df38687a32211f3294258fd58efb96
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847522"
---
# <a name="win32_startupcommand-class"></a><span data-ttu-id="fc4ce-103">Win32 \_ StartupCommand 類別</span><span class="sxs-lookup"><span data-stu-id="fc4ce-103">Win32\_StartupCommand class</span></span>

<span data-ttu-id="fc4ce-104">**Win32 \_ StartupCommand** [WMI 類別](../wmisdk/retrieving-a-class.md)代表當使用者登入電腦系統時自動執行的命令。</span><span class="sxs-lookup"><span data-stu-id="fc4ce-104">The **Win32\_StartupCommand** [WMI class](../wmisdk/retrieving-a-class.md) represents a command that runs automatically when a user logs onto the computer system.</span></span>

<span data-ttu-id="fc4ce-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="fc4ce-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="fc4ce-106">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="fc4ce-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc4ce-107">語法</span><span class="sxs-lookup"><span data-stu-id="fc4ce-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{8502C50A-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_StartupCommand : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  string Command;
  string Location;
  string Name;
  string User;
  string UserSID;
};
```

## <a name="members"></a><span data-ttu-id="fc4ce-108">成員</span><span class="sxs-lookup"><span data-stu-id="fc4ce-108">Members</span></span>

<span data-ttu-id="fc4ce-109">**Win32 \_ StartupCommand** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="fc4ce-109">The **Win32\_StartupCommand** class has these types of members:</span></span>

-   [<span data-ttu-id="fc4ce-110">屬性</span><span class="sxs-lookup"><span data-stu-id="fc4ce-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fc4ce-111">屬性</span><span class="sxs-lookup"><span data-stu-id="fc4ce-111">Properties</span></span>

<span data-ttu-id="fc4ce-112">**Win32 \_ StartupCommand** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="fc4ce-112">The **Win32\_StartupCommand** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fc4ce-113">**標題**</span><span class="sxs-lookup"><span data-stu-id="fc4ce-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc4ce-114">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fc4ce-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc4ce-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fc4ce-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc4ce-116">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) </span><span class="sxs-lookup"><span data-stu-id="fc4ce-116">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="fc4ce-117">目前物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="fc4ce-117">Short textual description of the current object.</span></span>

<span data-ttu-id="fc4ce-118">這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。</span><span class="sxs-lookup"><span data-stu-id="fc4ce-118">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc4ce-119">**命令**</span><span class="sxs-lookup"><span data-stu-id="fc4ce-119">**Command**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc4ce-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fc4ce-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc4ce-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fc4ce-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc4ce-122">限定詞： [**key**](../wmisdk/key-qualifier.md)、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SOFTWARE \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \\ \\ Run" ) </span><span class="sxs-lookup"><span data-stu-id="fc4ce-122">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SOFTWARE\\\\Microsoft\\\\Windows\\\\CurrentVersion\\\\Run")</span></span>
</dt> </dl>

<span data-ttu-id="fc4ce-123">啟動命令所執行的命令。</span><span class="sxs-lookup"><span data-stu-id="fc4ce-123">Command run by the startup command.</span></span>

<span data-ttu-id="fc4ce-124">WMI 從登錄機碼取得這項資料</span><span class="sxs-lookup"><span data-stu-id="fc4ce-124">WMI obtains this data from the registry key</span></span>

<span data-ttu-id="fc4ce-125">**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **執行**</span><span class="sxs-lookup"><span data-stu-id="fc4ce-125">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Run**</span></span>

<span data-ttu-id="fc4ce-126">範例： "C： \\ Windows \\notepad.exe myfile.txt"</span><span class="sxs-lookup"><span data-stu-id="fc4ce-126">Example: "C:\\Windows\\notepad.exe myfile.txt"</span></span>

</dd> <dt>

<span data-ttu-id="fc4ce-127">**說明**</span><span class="sxs-lookup"><span data-stu-id="fc4ce-127">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc4ce-128">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fc4ce-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc4ce-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fc4ce-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc4ce-130">目前物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="fc4ce-130">Textual description of the current object.</span></span>

<span data-ttu-id="fc4ce-131">這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。</span><span class="sxs-lookup"><span data-stu-id="fc4ce-131">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc4ce-132">**位置**</span><span class="sxs-lookup"><span data-stu-id="fc4ce-132">**Location**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc4ce-133">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fc4ce-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc4ce-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fc4ce-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc4ce-135">限定詞： [**key**](../wmisdk/key-qualifier.md)、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| \\ \\ SOFTWARE \\ \\ MICROSOFT \\ \\ windows \\ \\ CURRENTVERSION \\ \\ windows" ) </span><span class="sxs-lookup"><span data-stu-id="fc4ce-135">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|\\\\SOFTWARE\\\\MICROSOFT\\\\WINDOWS\\\\CURRENTVERSION\\\\Windows")</span></span>
</dt> </dl>

<span data-ttu-id="fc4ce-136">啟動命令位於磁片檔案系統上的路徑。</span><span class="sxs-lookup"><span data-stu-id="fc4ce-136">Path where the startup command resides on the disk file system.</span></span>

<span data-ttu-id="fc4ce-137">例如： HKLM \\ SOFTWARE \\ Microsoft \\ Windows \\ CurrentVersion \\ Run</span><span class="sxs-lookup"><span data-stu-id="fc4ce-137">For example: HKLM\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Run</span></span>

<dt>

<span id="Startup"></span><span id="startup"></span><span id="STARTUP"></span>

<span data-ttu-id="fc4ce-138">**啟動** ( 「啟動」 ) </span><span class="sxs-lookup"><span data-stu-id="fc4ce-138">**Startup** ("Startup")</span></span>


</dt> <dd></dd> <dt>

<span id="Common_Startup"></span><span id="common_startup"></span><span id="COMMON_STARTUP"></span>

<span data-ttu-id="fc4ce-139">**一般** 啟動 ( 「一般啟動」 ) </span><span class="sxs-lookup"><span data-stu-id="fc4ce-139">**Common Startup** ("Common Startup")</span></span>


</dt> <dd></dd> <dt>

<span id="HKLM__SOFTWARE__Microsoft__Windows__CurrentVersion__Run"></span><span id="hklm__software__microsoft__windows__currentversion__run"></span><span id="HKLM__SOFTWARE__MICROSOFT__WINDOWS__CURRENTVERSION__RUN"></span>

<span data-ttu-id="fc4ce-140">**\\ HKLM \\軟體 \\ \\ microsoft \\ \\ windows \\ \\ CurrentVersion \\ \\ run** ( "HKLM \\ \\ SOFTWARE \\ \\ Microsoft \\ \\ windows \\ \\ CurrentVersion \\ \\ run" ) </span><span class="sxs-lookup"><span data-stu-id="fc4ce-140">**HKLM\\\\SOFTWARE\\\\Microsoft\\\\Windows\\\\CurrentVersion\\\\Run** ("HKLM\\\\SOFTWARE\\\\Microsoft\\\\Windows\\\\CurrentVersion\\\\Run")</span></span>


</dt> <dd></dd> <dt>

<span id="HKLM__SOFTWARE__Microsoft__Windows__CurrentVersion__RunServices"></span><span id="hklm__software__microsoft__windows__currentversion__runservices"></span><span id="HKLM__SOFTWARE__MICROSOFT__WINDOWS__CURRENTVERSION__RUNSERVICES"></span>

<span data-ttu-id="fc4ce-141">**\\ HKLM \\SOFTWARE \\ \\ microsoft \\ \\ windows \\ \\ CurrentVersion \\ \\ RunServices** ( "HKLM \\ \\ SOFTWARE \\ \\ microsoft \\ \\ windows \\ \\ CurrentVersion \\ \\ RunServices" ) </span><span class="sxs-lookup"><span data-stu-id="fc4ce-141">**HKLM\\\\SOFTWARE\\\\Microsoft\\\\Windows\\\\CurrentVersion\\\\RunServices** ("HKLM\\\\SOFTWARE\\\\Microsoft\\\\Windows\\\\CurrentVersion\\\\RunServices")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="fc4ce-142">**名稱**</span><span class="sxs-lookup"><span data-stu-id="fc4ce-142">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc4ce-143">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fc4ce-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc4ce-144">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fc4ce-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc4ce-145">限定詞： [**key**](../wmisdk/key-qualifier.md)、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| File 結構 \| [**WIN32 \_ FIND \_ DATA**](/windows/win32/api/minwinbase/ns-minwinbase-win32_find_dataa) \| cFileName" ) </span><span class="sxs-lookup"><span data-stu-id="fc4ce-145">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|File Structures\|[**WIN32\_FIND\_DATA**](/windows/win32/api/minwinbase/ns-minwinbase-win32_find_dataa)\|cFileName")</span></span>
</dt> </dl>

<span data-ttu-id="fc4ce-146">啟動命令的檔案名。</span><span class="sxs-lookup"><span data-stu-id="fc4ce-146">File name of the startup command.</span></span>

<span data-ttu-id="fc4ce-147">範例： "FindFast"</span><span class="sxs-lookup"><span data-stu-id="fc4ce-147">Example: "FindFast"</span></span>

</dd> <dt>

<span data-ttu-id="fc4ce-148">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="fc4ce-148">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc4ce-149">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fc4ce-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc4ce-150">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fc4ce-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc4ce-151">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) </span><span class="sxs-lookup"><span data-stu-id="fc4ce-151">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="fc4ce-152">已知目前物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="fc4ce-152">Identifier by which the current object is known.</span></span>

<span data-ttu-id="fc4ce-153">這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。</span><span class="sxs-lookup"><span data-stu-id="fc4ce-153">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc4ce-154">**使用者**</span><span class="sxs-lookup"><span data-stu-id="fc4ce-154">**User**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc4ce-155">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fc4ce-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc4ce-156">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fc4ce-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc4ce-157">限定詞： [**key**](../wmisdk/key-qualifier.md)、 [**MAPPINGSTRINGS**](../wmisdk/standard-qualifiers.md) ( "WMI" ) </span><span class="sxs-lookup"><span data-stu-id="fc4ce-157">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="fc4ce-158">將執行這個啟動命令的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="fc4ce-158">User name for whom this startup command will run.</span></span>

<span data-ttu-id="fc4ce-159">範例： "mydomain \\ myname"</span><span class="sxs-lookup"><span data-stu-id="fc4ce-159">Example: "mydomain\\myname"</span></span>

</dd> <dt>

<span data-ttu-id="fc4ce-160">**UserSID**</span><span class="sxs-lookup"><span data-stu-id="fc4ce-160">**UserSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc4ce-161">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fc4ce-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc4ce-162">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fc4ce-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc4ce-163">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI" ) </span><span class="sxs-lookup"><span data-stu-id="fc4ce-163">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="fc4ce-164">UserSID 屬性會指出將執行這個啟動命令之使用者的 SID。</span><span class="sxs-lookup"><span data-stu-id="fc4ce-164">The UserSID property indicates the SID of the user for whom this startup command will run.</span></span> <span data-ttu-id="fc4ce-165">該使用者屬性可能是空的，但如果無法解析使用者名稱，UserSID 仍會有一個值 (例如已刪除的使用者) 。</span><span class="sxs-lookup"><span data-stu-id="fc4ce-165">That User property may be empty but UserSID still has a value if the user name can't be resolved (like in the case of a deleted user).</span></span> <span data-ttu-id="fc4ce-166">屬性有助於區分與兩個不同使用者（具有未解析名稱）相關聯的命令。</span><span class="sxs-lookup"><span data-stu-id="fc4ce-166">The property is helpful to distinguish between commands associated w/ two different users with unresolved names.</span></span> <span data-ttu-id="fc4ce-167">當命令與未實際識別使用者的專案（如所有使用者）相關聯時，它可能會是 Null。</span><span class="sxs-lookup"><span data-stu-id="fc4ce-167">It may be NULL when the command is associated with items not actually identifying a user like All Users.</span></span>

<span data-ttu-id="fc4ce-168">範例： S-1-5-21-1579938362-1064596589-3161144252-1006</span><span class="sxs-lookup"><span data-stu-id="fc4ce-168">Example:S-1-5-21-1579938362-1064596589-3161144252-1006</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fc4ce-169">備註</span><span class="sxs-lookup"><span data-stu-id="fc4ce-169">Remarks</span></span>

<span data-ttu-id="fc4ce-170">**Win32 \_ StartupCommand** 類別衍生自 [**CIM \_ 設定**](cim-setting.md)。</span><span class="sxs-lookup"><span data-stu-id="fc4ce-170">The **Win32\_StartupCommand** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

<span data-ttu-id="fc4ce-171">載入作業系統之後，電腦啟動不會結束。</span><span class="sxs-lookup"><span data-stu-id="fc4ce-171">Computer startup does not end after the operating system has been loaded.</span></span> <span data-ttu-id="fc4ce-172">相反地，您可以設定 Windows 作業系統，讓啟動命令在每次 Windows 啟動時執行。</span><span class="sxs-lookup"><span data-stu-id="fc4ce-172">Instead, the Windows operating system can be configured so that startup commands are run each time Windows starts.</span></span> <span data-ttu-id="fc4ce-173">啟動命令會儲存在登錄中或做為使用者設定檔的一部分，並在每次載入 Windows 時用來自動啟動指定的腳本或應用程式。</span><span class="sxs-lookup"><span data-stu-id="fc4ce-173">Startup commands are stored in the registry or as part of the user profile and are used to automatically start specified scripts or applications each time Windows is loaded.</span></span>

<span data-ttu-id="fc4ce-174">在大部分情況下，自動啟動程式很有用;它們可確保在每次載入 Windows 時，會自動啟動並執行某些應用程式，例如防病毒工具。</span><span class="sxs-lookup"><span data-stu-id="fc4ce-174">In most cases, autostart programs are useful; they ensure that certain applications, such as antivirus tools, are automatically started and run each time Windows is loaded.</span></span> <span data-ttu-id="fc4ce-175">不過，自動啟動程式也可以負責問題，例如：</span><span class="sxs-lookup"><span data-stu-id="fc4ce-175">However, autostart programs also can be responsible for problems such as:</span></span>

-   <span data-ttu-id="fc4ce-176">需要很長時間才能啟動的電腦。</span><span class="sxs-lookup"><span data-stu-id="fc4ce-176">Computers that take an exceptionally long time to start.</span></span> <span data-ttu-id="fc4ce-177">這可能是因為每次 Windows 啟動時都必須啟動的許多應用程式所造成的結果。</span><span class="sxs-lookup"><span data-stu-id="fc4ce-177">This might be the result of a large number of applications that must be started each time Windows starts.</span></span>
-   <span data-ttu-id="fc4ce-178">在工作列或工作管理員中表示的應用程式，即使使用者未啟動它們也是一樣。</span><span class="sxs-lookup"><span data-stu-id="fc4ce-178">Applications that are represented in the Taskbar or in Task Manager, even though the user did not start them.</span></span> <span data-ttu-id="fc4ce-179">雖然這些應用程式不一定會造成問題，但可能會導致來自不熟悉這些程式的使用者，以及其執行原因的使用者，可能會收到支援工程師的來電。</span><span class="sxs-lookup"><span data-stu-id="fc4ce-179">Although these applications do not necessarily cause problems, they can result in help desk calls from users who are confused as to where these programs came from and why they are running.</span></span>
-   <span data-ttu-id="fc4ce-180">即使電腦看似閒置也會發生問題。</span><span class="sxs-lookup"><span data-stu-id="fc4ce-180">Computers experiencing problems even when they seem idle.</span></span> <span data-ttu-id="fc4ce-181">這些問題通常是在沒有人察覺它們正在執行時執行的啟動命令所追蹤。</span><span class="sxs-lookup"><span data-stu-id="fc4ce-181">These problems are often traced to startup commands that are running when no one is aware that they are running.</span></span>

<span data-ttu-id="fc4ce-182">識別在啟動時自動執行的應用程式和腳本是很重要但很困難的系統管理工作，因為啟動命令可儲存在許多不同的位置：</span><span class="sxs-lookup"><span data-stu-id="fc4ce-182">Identifying the applications and scripts that automatically run at startup is an important but difficult administrative task, because startup commands can be stored in many different locations:</span></span>

-   <span data-ttu-id="fc4ce-183">HKLM \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ 執行</span><span class="sxs-lookup"><span data-stu-id="fc4ce-183">HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\Run</span></span>
-   <span data-ttu-id="fc4ce-184">HKLM \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ RunOnce</span><span class="sxs-lookup"><span data-stu-id="fc4ce-184">HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\RunOnce</span></span>
-   <span data-ttu-id="fc4ce-185">HKCU \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ 執行</span><span class="sxs-lookup"><span data-stu-id="fc4ce-185">HKCU\\Software\\Microsoft\\Windows\\CurrentVersion\\Run</span></span>
-   <span data-ttu-id="fc4ce-186">HKCU \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ RunOnce</span><span class="sxs-lookup"><span data-stu-id="fc4ce-186">HKCU\\Software\\Microsoft\\Windows\\CurrentVersion\\RunOnce</span></span>
-   <span data-ttu-id="fc4ce-187">HKU \\ ProgID \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Run</span><span class="sxs-lookup"><span data-stu-id="fc4ce-187">HKU\\ProgID\\Software\\Microsoft\\Windows\\CurrentVersion\\Run</span></span>
-   <span data-ttu-id="fc4ce-188">systemdrive \\ 檔和設定 \\ 所有使用者 \\ 開始功能表 \\ 程式 \\ 啟動</span><span class="sxs-lookup"><span data-stu-id="fc4ce-188">systemdrive\\Documents and Settings\\All Users\\Start Menu\\Programs\\Startup</span></span>
-   <span data-ttu-id="fc4ce-189">systemdrive \\ 檔和設定使用者 \\ 名稱使用者名稱 \\ 啟動功能表 \\ 程式 \\ 啟動</span><span class="sxs-lookup"><span data-stu-id="fc4ce-189">systemdrive\\Documents and Settings\\username\\Start Menu\\Programs\\Startup</span></span>

<span data-ttu-id="fc4ce-190">您可以使用 WMI Win32 \_ StartupCommand 類別來列舉 autostart 程式，而不論儲存資訊的位置為何。</span><span class="sxs-lookup"><span data-stu-id="fc4ce-190">You can use the WMI Win32\_StartupCommand class to enumerate autostart programs regardless of where the information is stored.</span></span>

<span data-ttu-id="fc4ce-191">使用這個類別的呼叫進程必須在登錄所在的電腦上具有「 **SE \_ 還原 \_ 名稱** 」許可權。</span><span class="sxs-lookup"><span data-stu-id="fc4ce-191">The calling process that uses this class must have the **SE\_RESTORE\_NAME** privilege on the computer in which the registry resides.</span></span> <span data-ttu-id="fc4ce-192">例如，如果您在本機電腦上列舉此類別，您的應用程式執行所在的帳戶必須具有此許可權。</span><span class="sxs-lookup"><span data-stu-id="fc4ce-192">For example, if you enumerate this class on the local computer, the account under which your application runs must have this privilege.</span></span> <span data-ttu-id="fc4ce-193">如需詳細資訊，請參閱 [執行特殊許可權作業](../wmisdk/executing-privileged-operations.md)。</span><span class="sxs-lookup"><span data-stu-id="fc4ce-193">For more information, see [Executing Privileged Operations](../wmisdk/executing-privileged-operations.md).</span></span>

<span data-ttu-id="fc4ce-194">您可以藉由呼叫腳本或 c + + 中的 WMI [系統登錄提供者](/previous-versions/windows/desktop/regprov/system-registry-provider)方法，來變更 **Win32 \_ StartupCommand** 取得資料的登錄值。</span><span class="sxs-lookup"><span data-stu-id="fc4ce-194">You can change the registry values where **Win32\_StartupCommand** obtains data by calling the WMI [System Registry Provider](/previous-versions/windows/desktop/regprov/system-registry-provider) methods in script or in C++.</span></span> <span data-ttu-id="fc4ce-195">如需詳細資訊，請參閱 [修改系統登錄](../wmisdk/modifying-the-system-registry.md)。</span><span class="sxs-lookup"><span data-stu-id="fc4ce-195">For more information, see [Modifying the System Registry](../wmisdk/modifying-the-system-registry.md).</span></span>

## <a name="examples"></a><span data-ttu-id="fc4ce-196">範例</span><span class="sxs-lookup"><span data-stu-id="fc4ce-196">Examples</span></span>

<span data-ttu-id="fc4ce-197">下列 VBScript 列舉電腦上的啟動命令。</span><span class="sxs-lookup"><span data-stu-id="fc4ce-197">The following VBScript enumerates the startup commands on a computer.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colStartupCommands = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_StartupCommand")
For Each objStartupCommand in colStartupCommands
 Wscript.Echo "Command: " & objStartupCommand.Command
 Wscript.Echo "Description: " & objStartupCommand.Description
 Wscript.Echo "Location: " & objStartupCommand.Location
 Wscript.Echo "Name: " & objStartupCommand.Name
 Wscript.Echo "SettingID: " & objStartupCommand.SettingID
 Wscript.Echo "User: " & objStartupCommand.User
Next
```



## <a name="requirements"></a><span data-ttu-id="fc4ce-198">規格需求</span><span class="sxs-lookup"><span data-stu-id="fc4ce-198">Requirements</span></span>



| <span data-ttu-id="fc4ce-199">需求</span><span class="sxs-lookup"><span data-stu-id="fc4ce-199">Requirement</span></span> | <span data-ttu-id="fc4ce-200">值</span><span class="sxs-lookup"><span data-stu-id="fc4ce-200">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fc4ce-201">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fc4ce-201">Minimum supported client</span></span><br/> | <span data-ttu-id="fc4ce-202">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fc4ce-202">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fc4ce-203">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fc4ce-203">Minimum supported server</span></span><br/> | <span data-ttu-id="fc4ce-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fc4ce-204">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fc4ce-205">命名空間</span><span class="sxs-lookup"><span data-stu-id="fc4ce-205">Namespace</span></span><br/>                | <span data-ttu-id="fc4ce-206">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="fc4ce-206">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fc4ce-207">MOF</span><span class="sxs-lookup"><span data-stu-id="fc4ce-207">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fc4ce-208"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="fc4ce-208"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fc4ce-209">DLL</span><span class="sxs-lookup"><span data-stu-id="fc4ce-209">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fc4ce-210"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fc4ce-210"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc4ce-211">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fc4ce-211">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc4ce-212">**CIM \_ 設定**</span><span class="sxs-lookup"><span data-stu-id="fc4ce-212">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="fc4ce-213">作業系統類別</span><span class="sxs-lookup"><span data-stu-id="fc4ce-213">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
