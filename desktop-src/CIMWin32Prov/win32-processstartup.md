---
description: Win32 \_ ProcessStartup ABSTRACT WMI 類別代表以 Windows 為基礎之進程的啟動設定。
ms.assetid: 78508404-cab2-42fb-a0ed-0e6e7d21408c
ms.tgt_platform: multiple
title: Win32_ProcessStartup 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ProcessStartup
- Win32_ProcessStartup.CreateFlags
- Win32_ProcessStartup.EnvironmentVariables
- Win32_ProcessStartup.ErrorMode
- Win32_ProcessStartup.FillAttribute
- Win32_ProcessStartup.PriorityClass
- Win32_ProcessStartup.ShowWindow
- Win32_ProcessStartup.Title
- Win32_ProcessStartup.WinstationDesktop
- Win32_ProcessStartup.X
- Win32_ProcessStartup.XCountChars
- Win32_ProcessStartup.XSize
- Win32_ProcessStartup.Y
- Win32_ProcessStartup.YCountChars
- Win32_ProcessStartup.YSize
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b0be949b106c1fa88b37e0c7764dbddb0546ded7
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/02/2021
ms.locfileid: "106999412"
---
# <a name="win32_processstartup-class"></a><span data-ttu-id="8c527-103">Win32 \_ ProcessStartup 類別</span><span class="sxs-lookup"><span data-stu-id="8c527-103">Win32\_ProcessStartup class</span></span>

<span data-ttu-id="8c527-104">**Win32 \_ ProcessStartup** abstract [WMI 類別](../wmisdk/retrieving-a-class.md)代表以 Windows 為基礎之進程的啟動設定。</span><span class="sxs-lookup"><span data-stu-id="8c527-104">The **Win32\_ProcessStartup** abstract [WMI class](../wmisdk/retrieving-a-class.md) represents the startup configuration of a Windows-based process.</span></span> <span data-ttu-id="8c527-105">類別定義為方法類型定義，這表示它只會用來將資訊傳遞給 [**Win32 \_ 進程**](win32-process.md)類別的 [**Create**](create-method-in-class-win32-process.md)方法。</span><span class="sxs-lookup"><span data-stu-id="8c527-105">The class is defined as a method type definition, which means that it is only used for passing information to the [**Create**](create-method-in-class-win32-process.md) method of the [**Win32\_Process**](win32-process.md) class.</span></span>

<span data-ttu-id="8c527-106">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="8c527-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c527-107">語法</span><span class="sxs-lookup"><span data-stu-id="8c527-107">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C4DB-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_ProcessStartup : Win32_MethodParameterClass
{
  uint32 CreateFlags;
  string EnvironmentVariables[];
  uint16 ErrorMode = 1;
  uint32 FillAttribute;
  uint32 PriorityClass;
  uint16 ShowWindow;
  string Title;
  string WinstationDesktop;
  uint32 X;
  uint32 XCountChars;
  uint32 XSize;
  uint32 Y;
  uint32 YCountChars;
  uint32 YSize;
};
```

## <a name="members"></a><span data-ttu-id="8c527-108">成員</span><span class="sxs-lookup"><span data-stu-id="8c527-108">Members</span></span>

<span data-ttu-id="8c527-109">**Win32 \_ ProcessStartup** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="8c527-109">The **Win32\_ProcessStartup** class has these types of members:</span></span>

-   [<span data-ttu-id="8c527-110">屬性</span><span class="sxs-lookup"><span data-stu-id="8c527-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8c527-111">屬性</span><span class="sxs-lookup"><span data-stu-id="8c527-111">Properties</span></span>

<span data-ttu-id="8c527-112">**Win32 \_ ProcessStartup** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="8c527-112">The **Win32\_ProcessStartup** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8c527-113">**CreateFlags**</span><span class="sxs-lookup"><span data-stu-id="8c527-113">**CreateFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c527-114">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8c527-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8c527-115">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8c527-115">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8c527-116">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| 進程和執行緒函數 \| [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) \| dwCreationFlags" ) </span><span class="sxs-lookup"><span data-stu-id="8c527-116">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Functions\|[**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)\|dwCreationFlags")</span></span>
</dt> </dl>

<span data-ttu-id="8c527-117">控制優先權類別和建立進程的其他值。</span><span class="sxs-lookup"><span data-stu-id="8c527-117">Additional values that control the priority class and the creation of the process.</span></span> <span data-ttu-id="8c527-118">您可以依照任何組合來指定下列建立值（如所述）。</span><span class="sxs-lookup"><span data-stu-id="8c527-118">The following creation values can be specified in any combination, except as noted.</span></span>

<dt>

<span id="Debug_Process"></span><span id="debug_process"></span><span id="DEBUG_PROCESS"></span>

<span data-ttu-id="8c527-119"><span id="Debug_Process"></span><span id="debug_process"></span><span id="DEBUG_PROCESS"></span>**Debug \_進程** (1) </span><span class="sxs-lookup"><span data-stu-id="8c527-119"><span id="Debug_Process"></span><span id="debug_process"></span><span id="DEBUG_PROCESS"></span>**Debug\_Process** (1)</span></span>


</dt> <dd>

<span data-ttu-id="8c527-120">如果設定此旗標，則會將呼叫進程視為偵錯工具，並正在調試新的進程。</span><span class="sxs-lookup"><span data-stu-id="8c527-120">If this flag is set, the calling process is treated as a debugger, and the new process is being debugged.</span></span> <span data-ttu-id="8c527-121">系統會向偵錯工具通知在正在進行的進程中發生的所有偵錯工具事件。</span><span class="sxs-lookup"><span data-stu-id="8c527-121">The system notifies the debugger of all debug events that occur in the process being debugged.</span></span>

</dd> <dt>

<span id="Debug_Only_This_Process"></span><span id="debug_only_this_process"></span><span id="DEBUG_ONLY_THIS_PROCESS"></span>

<span data-ttu-id="8c527-122"><span id="Debug_Only_This_Process"></span><span id="debug_only_this_process"></span><span id="DEBUG_ONLY_THIS_PROCESS"></span>**Debug \_只有 \_ 這個 \_ 進程** (2) </span><span class="sxs-lookup"><span data-stu-id="8c527-122"><span id="Debug_Only_This_Process"></span><span id="debug_only_this_process"></span><span id="DEBUG_ONLY_THIS_PROCESS"></span>**Debug\_Only\_This\_Process** (2)</span></span>


</dt> <dd>

<span data-ttu-id="8c527-123">如果未設定此旗標，而且正在調試呼叫進程，新進程會成為另一個正在進行調試的進程。</span><span class="sxs-lookup"><span data-stu-id="8c527-123">If this flag is not set and the calling process is being debugged, the new process becomes another process being debugged.</span></span> <span data-ttu-id="8c527-124">如果呼叫進程不是正在進行調試的進程，就不會發生任何與偵錯工具相關的動作。</span><span class="sxs-lookup"><span data-stu-id="8c527-124">If the calling process is not a process of being debugged, no debugging-related actions occur.</span></span>

</dd> <dt>

<span id="Create_Suspended"></span><span id="create_suspended"></span><span id="CREATE_SUSPENDED"></span>

<span data-ttu-id="8c527-125"><span id="Create_Suspended"></span><span id="create_suspended"></span><span id="CREATE_SUSPENDED"></span>**建立 \_已暫** 止 (4) </span><span class="sxs-lookup"><span data-stu-id="8c527-125"><span id="Create_Suspended"></span><span id="create_suspended"></span><span id="CREATE_SUSPENDED"></span>**Create\_Suspended** (4)</span></span>


</dt> <dd>

<span data-ttu-id="8c527-126">新進程的主要執行緒是以暫停狀態建立的，而且在呼叫 [**ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) 方法之前，不會執行。</span><span class="sxs-lookup"><span data-stu-id="8c527-126">The primary thread of the new process is created in a suspended state and does not run until the [**ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) method is called.</span></span>

</dd> <dt>

<span id="Detached_Process"></span><span id="detached_process"></span><span id="DETACHED_PROCESS"></span>

<span data-ttu-id="8c527-127"><span id="Detached_Process"></span><span id="detached_process"></span><span id="DETACHED_PROCESS"></span>卸 **離 \_進程** (8) </span><span class="sxs-lookup"><span data-stu-id="8c527-127"><span id="Detached_Process"></span><span id="detached_process"></span><span id="DETACHED_PROCESS"></span>**Detached\_Process** (8)</span></span>


</dt> <dd>

<span data-ttu-id="8c527-128">針對主控台進程，新進程無法存取父進程的主控台。</span><span class="sxs-lookup"><span data-stu-id="8c527-128">For console processes, the new process does not have access to the console of the parent process.</span></span> <span data-ttu-id="8c527-129">如果已設定 [ **建立 \_ 新的 \_ 主控台** ] 旗標，則無法使用此旗標。</span><span class="sxs-lookup"><span data-stu-id="8c527-129">This flag cannot be used if the **Create\_New\_Console** flag is set.</span></span>

</dd> <dt>

<span id="Create_New_Console"></span><span id="create_new_console"></span><span id="CREATE_NEW_CONSOLE"></span>

<span data-ttu-id="8c527-130"><span id="Create_New_Console"></span><span id="create_new_console"></span><span id="CREATE_NEW_CONSOLE"></span>**建立 \_ (\_** 16) 的新主控台</span><span class="sxs-lookup"><span data-stu-id="8c527-130"><span id="Create_New_Console"></span><span id="create_new_console"></span><span id="CREATE_NEW_CONSOLE"></span>**Create\_New\_Console** (16)</span></span>


</dt> <dd>

<span data-ttu-id="8c527-131">這個新的進程有新的主控台，而不是繼承父主控台。</span><span class="sxs-lookup"><span data-stu-id="8c527-131">This new process has a new console, instead of inheriting the parent console.</span></span> <span data-ttu-id="8c527-132">此旗標不可與卸 **離的 \_ 進程** 旗標一起使用。</span><span class="sxs-lookup"><span data-stu-id="8c527-132">This flag cannot be used with the **Detached\_Process** flag.</span></span>

</dd> <dt>

<span id="Create_New_Process_Group"></span><span id="create_new_process_group"></span><span id="CREATE_NEW_PROCESS_GROUP"></span>

<span data-ttu-id="8c527-133"><span id="Create_New_Process_Group"></span><span id="create_new_process_group"></span><span id="CREATE_NEW_PROCESS_GROUP"></span>**建立 \_新的 \_ 進程 \_ 群組** (512) </span><span class="sxs-lookup"><span data-stu-id="8c527-133"><span id="Create_New_Process_Group"></span><span id="create_new_process_group"></span><span id="CREATE_NEW_PROCESS_GROUP"></span>**Create\_New\_Process\_Group** (512)</span></span>


</dt> <dd>

<span data-ttu-id="8c527-134">這個新的程式是新進程群組的根進程。</span><span class="sxs-lookup"><span data-stu-id="8c527-134">This new process is the root process of a new process group.</span></span> <span data-ttu-id="8c527-135">進程群組包含此根進程下階的所有進程。</span><span class="sxs-lookup"><span data-stu-id="8c527-135">The process group includes all of the processes that are descendants of this root process.</span></span> <span data-ttu-id="8c527-136">新進程群組的處理序識別碼與 [**Win32 \_ 進程**](win32-process.md)類別的 **ProcessID** 屬性中所傳回的進程識別碼相同。</span><span class="sxs-lookup"><span data-stu-id="8c527-136">The process identifier of the new process group is the same as the process identifier that is returned in the **ProcessID** property of the [**Win32\_Process**](win32-process.md) class.</span></span> <span data-ttu-id="8c527-137">[**GenerateConsoleCtrlEvent**](/windows/console/generateconsolectrlevent)方法會使用進程群組來啟用將 Ctrl + C 信號或 CTRL + BREAK 信號傳送給一組主控台進程的作業。</span><span class="sxs-lookup"><span data-stu-id="8c527-137">Process groups are used by the [**GenerateConsoleCtrlEvent**](/windows/console/generateconsolectrlevent) method to enable the sending of either a CTRL+C signal or a CTRL+BREAK signal to a group of console processes.</span></span>

</dd> <dt>

<span id="Create_Unicode_Environment"></span><span id="create_unicode_environment"></span><span id="CREATE_UNICODE_ENVIRONMENT"></span>

<span data-ttu-id="8c527-138"><span id="Create_Unicode_Environment"></span><span id="create_unicode_environment"></span><span id="CREATE_UNICODE_ENVIRONMENT"></span>**建立 \_Unicode \_ 環境** (1024) </span><span class="sxs-lookup"><span data-stu-id="8c527-138"><span id="Create_Unicode_Environment"></span><span id="create_unicode_environment"></span><span id="CREATE_UNICODE_ENVIRONMENT"></span>**Create\_Unicode\_Environment** (1024)</span></span>


</dt> <dd>

<span data-ttu-id="8c527-139">**EnvironmentVariables** 屬性中所列的環境設定會使用 Unicode 字元。</span><span class="sxs-lookup"><span data-stu-id="8c527-139">The environment settings listed in the **EnvironmentVariables** property use Unicode characters.</span></span> <span data-ttu-id="8c527-140">如果未設定此旗標，則環境區塊會使用 ANSI 字元。</span><span class="sxs-lookup"><span data-stu-id="8c527-140">If this flag is not set, the environment block uses ANSI characters.</span></span>

</dd> <dt>

<span id="Create_Default_Error_Mode"></span><span id="create_default_error_mode"></span><span id="CREATE_DEFAULT_ERROR_MODE"></span>

<span data-ttu-id="8c527-141"><span id="Create_Default_Error_Mode"></span><span id="create_default_error_mode"></span><span id="CREATE_DEFAULT_ERROR_MODE"></span>**建立 \_預設 \_ 錯誤 \_ 模式** (67108864) </span><span class="sxs-lookup"><span data-stu-id="8c527-141"><span id="Create_Default_Error_Mode"></span><span id="create_default_error_mode"></span><span id="CREATE_DEFAULT_ERROR_MODE"></span>**Create\_Default\_Error\_Mode** (67108864)</span></span>


</dt> <dd>

<span data-ttu-id="8c527-142">新建立的進程會獲得呼叫進程的系統預設錯誤模式，而不是繼承父進程的錯誤模式。</span><span class="sxs-lookup"><span data-stu-id="8c527-142">Newly created processes are given the system default error mode of the calling process instead of inheriting the error mode of the parent process.</span></span> <span data-ttu-id="8c527-143">此旗標適用于在停用硬性錯誤的情況下執行的多執行緒 shell 應用程式。</span><span class="sxs-lookup"><span data-stu-id="8c527-143">This flag is useful for multithreaded shell applications that run with hard errors disabled.</span></span>

</dd> <dt>

<span id="CREATE_BREAKAWAY_FROM_JOB"></span><span id="create_breakaway_from_job"></span>

<span data-ttu-id="8c527-144"><span id="CREATE_BREAKAWAY_FROM_JOB"></span><span id="create_breakaway_from_job"></span>**建立 \_\_從 \_ 作業** (16777216) BREAKAWAY</span><span class="sxs-lookup"><span data-stu-id="8c527-144"><span id="CREATE_BREAKAWAY_FROM_JOB"></span><span id="create_breakaway_from_job"></span>**CREATE\_BREAKAWAY\_FROM\_JOB** (16777216)</span></span>


</dt> <dd>

<span data-ttu-id="8c527-145">用來建立的進程不會受到工作物件的限制。</span><span class="sxs-lookup"><span data-stu-id="8c527-145">Used for the created process not to be limited by the job object.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8c527-146">**EnvironmentVariables**</span><span class="sxs-lookup"><span data-stu-id="8c527-146">**EnvironmentVariables**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c527-147">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="8c527-147">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8c527-148">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8c527-148">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8c527-149">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| HKEY \_ 目前的 \_ 使用者 \\ \\ 環境" ) </span><span class="sxs-lookup"><span data-stu-id="8c527-149">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|HKEY\_CURRENT\_USER\\\\Environment")</span></span>
</dt> </dl>

<span data-ttu-id="8c527-150">電腦設定的設定清單。</span><span class="sxs-lookup"><span data-stu-id="8c527-150">List of settings for the configuration of a computer.</span></span> <span data-ttu-id="8c527-151">環境變數會指定檔案的搜尋路徑、暫存檔的目錄、應用程式特定的選項，以及其他類似的資訊。</span><span class="sxs-lookup"><span data-stu-id="8c527-151">Environment variables specify search paths for files, directories for temporary files, application-specific options, and other similar information.</span></span> <span data-ttu-id="8c527-152">系統會維護每個使用者的環境設定區塊，以及一部電腦的環境設定。</span><span class="sxs-lookup"><span data-stu-id="8c527-152">The system maintains a block of environment settings for each user and one for the computer.</span></span> <span data-ttu-id="8c527-153">系統內容區塊代表特定電腦之所有使用者的環境變數。</span><span class="sxs-lookup"><span data-stu-id="8c527-153">The system environment block represents environment variables for all of the users of a specific computer.</span></span> <span data-ttu-id="8c527-154">使用者的環境區塊代表系統為特定使用者維護的環境變數，並包含系統內容變數集。</span><span class="sxs-lookup"><span data-stu-id="8c527-154">A user's environment block represents the environment variables that the system maintains for a specific user, and includes the set of system environment variables.</span></span> <span data-ttu-id="8c527-155">根據預設，每個進程都會收到其父進程的環境區塊複本。</span><span class="sxs-lookup"><span data-stu-id="8c527-155">By default, each process receives a copy of the environment block for its parent process.</span></span> <span data-ttu-id="8c527-156">一般來說，這是登入之使用者的環境區塊。</span><span class="sxs-lookup"><span data-stu-id="8c527-156">Typically, this is the environment block for the user who is logged on.</span></span> <span data-ttu-id="8c527-157">進程可以針對其子進程指定不同的環境區塊。</span><span class="sxs-lookup"><span data-stu-id="8c527-157">A process can specify different environment blocks for its child processes.</span></span>

</dd> <dt>

<span data-ttu-id="8c527-158">**ErrorMode**</span><span class="sxs-lookup"><span data-stu-id="8c527-158">**ErrorMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c527-159">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="8c527-159">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8c527-160">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8c527-160">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8c527-161">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Error 函數 \| SetErrorMode" ) </span><span class="sxs-lookup"><span data-stu-id="8c527-161">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Error Functions\|SetErrorMode")</span></span>
</dt> </dl>

<span data-ttu-id="8c527-162">在某些非 x86 處理器上，未對齊的記憶體參考會導致對齊錯誤例外狀況。</span><span class="sxs-lookup"><span data-stu-id="8c527-162">On some non-x86 processors, misaligned memory references cause an alignment fault exception.</span></span> <span data-ttu-id="8c527-163">沒有旗標的 **\_ 對齊 \_ 錯誤 \_** （旗標）可讓您控制作業系統是否自動修正這類對齊錯誤，或讓應用程式看得到它們。</span><span class="sxs-lookup"><span data-stu-id="8c527-163">The **No\_Alignment\_Fault\_Except** flag lets you control whether or not an operating system automatically fixes such alignment faults, or makes them visible to an application.</span></span> <span data-ttu-id="8c527-164">在每秒數百萬個指令 (MIPS) 平臺上，應用程式必須明確地呼叫 [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) ，但 **不含 \_ 對齊 \_ 錯誤 \_** ，因為旗標會讓作業系統自動修正對齊錯誤。</span><span class="sxs-lookup"><span data-stu-id="8c527-164">On a millions of instructions per second (MIPS) platform, an application must explicitly call [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) with the **No\_Alignment\_Fault\_Except** flag to have the operating system automatically fix alignment faults.</span></span>

<span data-ttu-id="8c527-165">作業系統處理數種嚴重錯誤類型的方式。</span><span class="sxs-lookup"><span data-stu-id="8c527-165">How an operating system processes several types of serious errors.</span></span> <span data-ttu-id="8c527-166">您可以指定作業系統進程錯誤，或應用程式可以接收和處理錯誤。</span><span class="sxs-lookup"><span data-stu-id="8c527-166">You can specify that the operating system process errors, or an application can receive and process errors.</span></span>

<span data-ttu-id="8c527-167">預設設定是讓作業系統能夠看見應用程式的對齊錯誤。</span><span class="sxs-lookup"><span data-stu-id="8c527-167">The default setting is for the operating system to make alignment faults visible to an application.</span></span> <span data-ttu-id="8c527-168">因為 x86 平臺不會讓應用程式看見對齊錯誤，所以旗標 **除了旗標 \_ \_ \_ 以外** ，不會造成作業系統引發對齊錯誤的錯誤，即使未設定旗標。</span><span class="sxs-lookup"><span data-stu-id="8c527-168">Because the x86 platform does not make alignment faults visible to an application, the **No\_Alignment\_Fault\_Except** flag does not make the operating system raise an alignment fault error—even if the flag is not set.</span></span> <span data-ttu-id="8c527-169">[**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode)的預設狀態是將所有旗標設定為 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="8c527-169">The default state for [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) is to set all of the flags to 0 (zero).</span></span>

<dt>



 <span data-ttu-id="8c527-170">(1)</span><span class="sxs-lookup"><span data-stu-id="8c527-170">(1)</span></span>


</dt> <dd>

<span data-ttu-id="8c527-171">預設</span><span class="sxs-lookup"><span data-stu-id="8c527-171">Default</span></span>

</dd> <dt>

<span id="Fail_Critical_Errors"></span><span id="fail_critical_errors"></span><span id="FAIL_CRITICAL_ERRORS"></span>

<span data-ttu-id="8c527-172"><span id="Fail_Critical_Errors"></span><span id="fail_critical_errors"></span><span id="FAIL_CRITICAL_ERRORS"></span>**失敗 \_嚴重 \_ 錯誤** (2) </span><span class="sxs-lookup"><span data-stu-id="8c527-172"><span id="Fail_Critical_Errors"></span><span id="fail_critical_errors"></span><span id="FAIL_CRITICAL_ERRORS"></span>**Fail\_Critical\_Errors** (2)</span></span>


</dt> <dd>

<span data-ttu-id="8c527-173">如果設定此旗標，當發生這類錯誤時，作業系統不會顯示 [重大錯誤處理常式] 訊息方塊。</span><span class="sxs-lookup"><span data-stu-id="8c527-173">If this flag is set, the operating system does not display the critical error handler message box when such an error occurs.</span></span> <span data-ttu-id="8c527-174">相反地，作業系統會將錯誤傳送到呼叫的進程。</span><span class="sxs-lookup"><span data-stu-id="8c527-174">Instead, the operating system sends the error to the calling process.</span></span>

</dd> <dt>

<span id="No_Alignment_Fault_Except"></span><span id="no_alignment_fault_except"></span><span id="NO_ALIGNMENT_FAULT_EXCEPT"></span>

<span data-ttu-id="8c527-175"><span id="No_Alignment_Fault_Except"></span><span id="no_alignment_fault_except"></span><span id="NO_ALIGNMENT_FAULT_EXCEPT"></span>**否 \_ (4) \_ \_ 以外的對齊錯誤**</span><span class="sxs-lookup"><span data-stu-id="8c527-175"><span id="No_Alignment_Fault_Except"></span><span id="no_alignment_fault_except"></span><span id="NO_ALIGNMENT_FAULT_EXCEPT"></span>**No\_Alignment\_Fault\_Except** (4)</span></span>


</dt> <dd>

<span data-ttu-id="8c527-176">如果設定此旗標，作業系統會自動修正記憶體對齊錯誤，並讓應用程式看不到這些錯誤。</span><span class="sxs-lookup"><span data-stu-id="8c527-176">If this flag is set, the operating system automatically fixes memory alignment faults and makes them invisible to the application.</span></span> <span data-ttu-id="8c527-177">它會針對呼叫和子系進程執行此工作。</span><span class="sxs-lookup"><span data-stu-id="8c527-177">It does this for the calling and descendant processes.</span></span> <span data-ttu-id="8c527-178">此旗標適用于精簡的指令集運算 (RISC) ，而且對 x86 處理器沒有任何影響。</span><span class="sxs-lookup"><span data-stu-id="8c527-178">This flag applies to reduced instruction set computing (RISC) only, and has no effect on x86 processors.</span></span>

</dd> <dt>

<span id="No_GP_Fault_Error_Box"></span><span id="no_gp_fault_error_box"></span><span id="NO_GP_FAULT_ERROR_BOX"></span>

<span data-ttu-id="8c527-179"><span id="No_GP_Fault_Error_Box"></span><span id="no_gp_fault_error_box"></span><span id="NO_GP_FAULT_ERROR_BOX"></span>**否 \_GP \_ 錯誤 \_ \_** 方塊 (8) </span><span class="sxs-lookup"><span data-stu-id="8c527-179"><span id="No_GP_Fault_Error_Box"></span><span id="no_gp_fault_error_box"></span><span id="NO_GP_FAULT_ERROR_BOX"></span>**No\_GP\_Fault\_Error\_Box** (8)</span></span>


</dt> <dd>

<span data-ttu-id="8c527-180">如果設定此旗標，作業系統不會在發生 GP 錯誤時， (GP) 錯誤訊息框中顯示一般保護。</span><span class="sxs-lookup"><span data-stu-id="8c527-180">If this flag is set, the operating system does not display the general protection (GP) fault message box when a GP error occurs.</span></span> <span data-ttu-id="8c527-181">此旗標只能透過可處理 GP 錯誤的應用程式來設定。</span><span class="sxs-lookup"><span data-stu-id="8c527-181">This flag should only be set by debugging applications that handle GP errors.</span></span>

</dd> <dt>

<span id="No_Open_File_Error_Box"></span><span id="no_open_file_error_box"></span><span id="NO_OPEN_FILE_ERROR_BOX"></span>

<span data-ttu-id="8c527-182"><span id="No_Open_File_Error_Box"></span><span id="no_open_file_error_box"></span><span id="NO_OPEN_FILE_ERROR_BOX"></span>**否 \_開啟 \_ 檔案 \_ 錯誤 \_** 方塊 (16) </span><span class="sxs-lookup"><span data-stu-id="8c527-182"><span id="No_Open_File_Error_Box"></span><span id="no_open_file_error_box"></span><span id="NO_OPEN_FILE_ERROR_BOX"></span>**No\_Open\_File\_Error\_Box** (16)</span></span>


</dt> <dd>

<span data-ttu-id="8c527-183">如果設定此旗標，作業系統不會在找不到檔案時顯示訊息方塊。</span><span class="sxs-lookup"><span data-stu-id="8c527-183">If this flag is set, the operating system does not display a message box when it fails to find a file.</span></span> <span data-ttu-id="8c527-184">相反地，錯誤會傳回給呼叫的進程。</span><span class="sxs-lookup"><span data-stu-id="8c527-184">Instead, the error is returned to the calling process.</span></span> <span data-ttu-id="8c527-185">目前忽略此旗標。</span><span class="sxs-lookup"><span data-stu-id="8c527-185">This flag is currently ignored.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8c527-186">**FillAttribute**</span><span class="sxs-lookup"><span data-stu-id="8c527-186">**FillAttribute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c527-187">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8c527-187">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8c527-188">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8c527-188">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8c527-189">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| 進程和執行緒結構 \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| dwFillAttribute" ) </span><span class="sxs-lookup"><span data-stu-id="8c527-189">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|dwFillAttribute")</span></span>
</dt> </dl>

<span data-ttu-id="8c527-190">如果在主控台應用程式中建立新的主控台視窗，則為文字和背景色彩。</span><span class="sxs-lookup"><span data-stu-id="8c527-190">The text and background colors if a new console window is created in a console application.</span></span> <span data-ttu-id="8c527-191">這些值會在圖形化使用者介面中忽略， (GUI) 應用程式。</span><span class="sxs-lookup"><span data-stu-id="8c527-191">These values are ignored in graphical user interface (GUI) applications.</span></span> <span data-ttu-id="8c527-192">若要同時指定前景和背景色彩，請將值相加。</span><span class="sxs-lookup"><span data-stu-id="8c527-192">To specify both foreground and background colors, add the values together.</span></span> <span data-ttu-id="8c527-193">例如，若要在藍色背景上 (4) 的紅色類型 (16) ，請將 FillAttribute 設定為20。</span><span class="sxs-lookup"><span data-stu-id="8c527-193">For example, to have red type (4) on a blue background (16), set the FillAttribute to 20.</span></span>

<dt>

<span data-ttu-id="8c527-194">1</span><span class="sxs-lookup"><span data-stu-id="8c527-194">1</span></span>
</dt> <dd>

<span data-ttu-id="8c527-195">前景 \_ 藍色</span><span class="sxs-lookup"><span data-stu-id="8c527-195">Foreground\_Blue</span></span>

</dd> <dt>

<span data-ttu-id="8c527-196">2</span><span class="sxs-lookup"><span data-stu-id="8c527-196">2</span></span>
</dt> <dd>

<span data-ttu-id="8c527-197">前景 \_ 綠色</span><span class="sxs-lookup"><span data-stu-id="8c527-197">Foreground\_Green</span></span>

</dd> <dt>

<span data-ttu-id="8c527-198">4</span><span class="sxs-lookup"><span data-stu-id="8c527-198">4</span></span>
</dt> <dd>

<span data-ttu-id="8c527-199">前景 \_ 紅色</span><span class="sxs-lookup"><span data-stu-id="8c527-199">Foreground\_Red</span></span>

</dd> <dt>

<span data-ttu-id="8c527-200">8</span><span class="sxs-lookup"><span data-stu-id="8c527-200">8</span></span>
</dt> <dd>

<span data-ttu-id="8c527-201">前景 \_ 濃度</span><span class="sxs-lookup"><span data-stu-id="8c527-201">Foreground\_Intensity</span></span>

</dd> <dt>

<span data-ttu-id="8c527-202">16</span><span class="sxs-lookup"><span data-stu-id="8c527-202">16</span></span>
</dt> <dd>

<span data-ttu-id="8c527-203">背景 \_ 藍色</span><span class="sxs-lookup"><span data-stu-id="8c527-203">Background\_Blue</span></span>

</dd> <dt>

<span data-ttu-id="8c527-204">32</span><span class="sxs-lookup"><span data-stu-id="8c527-204">32</span></span>
</dt> <dd>

<span data-ttu-id="8c527-205">背景 \_ 綠色</span><span class="sxs-lookup"><span data-stu-id="8c527-205">Background\_Green</span></span>

</dd> <dt>

<span data-ttu-id="8c527-206">64</span><span class="sxs-lookup"><span data-stu-id="8c527-206">64</span></span>
</dt> <dd>

<span data-ttu-id="8c527-207">背景 \_ 紅色</span><span class="sxs-lookup"><span data-stu-id="8c527-207">Background\_Red</span></span>

</dd> <dt>

<span data-ttu-id="8c527-208">128</span><span class="sxs-lookup"><span data-stu-id="8c527-208">128</span></span>
</dt> <dd>

<span data-ttu-id="8c527-209">背景 \_ 濃度</span><span class="sxs-lookup"><span data-stu-id="8c527-209">Background\_Intensity</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8c527-210">**PriorityClass**</span><span class="sxs-lookup"><span data-stu-id="8c527-210">**PriorityClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c527-211">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8c527-211">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8c527-212">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8c527-212">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8c527-213">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 進程和執行緒結構 \| [**JOBOBJECT \_ 基本 \_ 限制 \_ 資訊**](/windows/win32/api/winnt/ns-winnt-jobobject_basic_limit_information) \| PriorityClass」 ) </span><span class="sxs-lookup"><span data-stu-id="8c527-213">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**JOBOBJECT\_BASIC\_LIMIT\_INFORMATION**](/windows/win32/api/winnt/ns-winnt-jobobject_basic_limit_information)\|PriorityClass")</span></span>
</dt> </dl>

<span data-ttu-id="8c527-214">新進程的 Priority 類別。</span><span class="sxs-lookup"><span data-stu-id="8c527-214">Priority class of the new process.</span></span> <span data-ttu-id="8c527-215">您可以使用這個屬性來判斷進程中線程的排程優先權。</span><span class="sxs-lookup"><span data-stu-id="8c527-215">Use this property to determine the schedule priorities of the threads in the process.</span></span> <span data-ttu-id="8c527-216">如果屬性是空的，除非建立進程的 priority 類別處於閒置或低於正常狀態，否則優先權類別會預設為 [正常] \_ 。</span><span class="sxs-lookup"><span data-stu-id="8c527-216">If the property is left null, the priority class defaults to Normal—unless the priority class of the creating process is Idle or Below\_Normal.</span></span> <span data-ttu-id="8c527-217">在這些情況下，子進程會接收呼叫進程的預設優先權類別。</span><span class="sxs-lookup"><span data-stu-id="8c527-217">In these cases, the child process receives the default priority class of the calling process.</span></span>

<dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="8c527-218"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**一般** (32) </span><span class="sxs-lookup"><span data-stu-id="8c527-218"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (32)</span></span>


</dt> <dd>

<span data-ttu-id="8c527-219">表示不需要特殊排程的一般進程。</span><span class="sxs-lookup"><span data-stu-id="8c527-219">Indicates a normal process with no special schedule needs.</span></span>

</dd> <dt>

<span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>

<span data-ttu-id="8c527-220"><span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>**閒置** (64) </span><span class="sxs-lookup"><span data-stu-id="8c527-220"><span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>**Idle** (64)</span></span>


</dt> <dd>

<span data-ttu-id="8c527-221">表示只有當系統閒置時才會執行的進程，並由在較高優先順序類別中執行之進程的執行緒佔用。</span><span class="sxs-lookup"><span data-stu-id="8c527-221">Indicates a process with threads that run only when the system is idle and are preempted by the threads of any process running in a higher priority class.</span></span> <span data-ttu-id="8c527-222">螢幕保護裝置是一個例子。</span><span class="sxs-lookup"><span data-stu-id="8c527-222">An example is a screen saver.</span></span> <span data-ttu-id="8c527-223">閒置優先權類別是由子進程繼承。</span><span class="sxs-lookup"><span data-stu-id="8c527-223">The idle priority class is inherited by child processes.</span></span>

</dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

<span data-ttu-id="8c527-224"><span id="High"></span><span id="high"></span><span id="HIGH"></span>**高** (128) </span><span class="sxs-lookup"><span data-stu-id="8c527-224"><span id="High"></span><span id="high"></span><span id="HIGH"></span>**High** (128)</span></span>


</dt> <dd>

<span data-ttu-id="8c527-225">表示執行必須立即執行才能正確執行之時間關鍵工作的進程。</span><span class="sxs-lookup"><span data-stu-id="8c527-225">Indicates a process that performs time-critical tasks that must be executed immediately to run correctly.</span></span> <span data-ttu-id="8c527-226">高優先順序類別進程的執行緒會優先處理一般優先順序或閒置優先順序類別進程的執行緒。</span><span class="sxs-lookup"><span data-stu-id="8c527-226">The threads of a high-priority class process preempt the threads of normal-priority or idle-priority class processes.</span></span> <span data-ttu-id="8c527-227">其中一個範例是 Windows 工作清單，當使用者呼叫時必須快速回應，不論作業系統上的負載為何。</span><span class="sxs-lookup"><span data-stu-id="8c527-227">An example is Windows Task List, which must respond quickly when called by the user, regardless of the load on the operating system.</span></span> <span data-ttu-id="8c527-228">使用高優先順序類別時請特別小心，因為高優先順序類別的 CPU 系結應用程式幾乎可以使用所有可用的迴圈。</span><span class="sxs-lookup"><span data-stu-id="8c527-228">Use extreme care when using the high-priority class, because a high-priority class CPU-bound application can use nearly all of the available cycles.</span></span> <span data-ttu-id="8c527-229">只有設定為此層級的即時優先權 shutdown 執行緒。</span><span class="sxs-lookup"><span data-stu-id="8c527-229">Only a real-time priority preempts threads set to this level.</span></span>

</dd> <dt>

<span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>

<span data-ttu-id="8c527-230"><span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>**即時** (256) </span><span class="sxs-lookup"><span data-stu-id="8c527-230"><span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>**Realtime** (256)</span></span>


</dt> <dd>

<span data-ttu-id="8c527-231">表示具有最高可能優先順序的進程。</span><span class="sxs-lookup"><span data-stu-id="8c527-231">Indicates a process that has the highest possible priority.</span></span> <span data-ttu-id="8c527-232">即時優先權類別進程的執行緒會優先處理所有其他進程的執行緒，包括執行重要工作的高優先順序執行緒和作業系統進程。</span><span class="sxs-lookup"><span data-stu-id="8c527-232">The threads of a real-time priority class process preempt the threads of all other processes—including high-priority threads and operating system processes performing important tasks.</span></span> <span data-ttu-id="8c527-233">例如，執行超過一小段時間間隔的即時程式可能會導致磁碟快取無法排清，或造成滑鼠沒有回應。</span><span class="sxs-lookup"><span data-stu-id="8c527-233">For example, a real-time process that executes for more than a very brief interval can cause disk caches not to flush, or cause a mouse to be unresponsive.</span></span>

</dd> <dt>

<span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>

<span data-ttu-id="8c527-234"><span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>**以下 \_一般** (16384) </span><span class="sxs-lookup"><span data-stu-id="8c527-234"><span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>**Below\_Normal** (16384)</span></span>


</dt> <dd>

<span data-ttu-id="8c527-235">表示優先順序高於閒置但低於正常的進程。</span><span class="sxs-lookup"><span data-stu-id="8c527-235">Indicates a process that has a priority higher than Idle but lower than Normal.</span></span>

</dd> <dt>

<span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>

<span data-ttu-id="8c527-236"><span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>**以上 \_一般** (32768) </span><span class="sxs-lookup"><span data-stu-id="8c527-236"><span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>**Above\_Normal** (32768)</span></span>


</dt> <dd>

<span data-ttu-id="8c527-237">表示優先順序高於正常但低於高的進程。</span><span class="sxs-lookup"><span data-stu-id="8c527-237">Indicates a process that has a priority higher than Normal but lower than High.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8c527-238">**ShowWindow**</span><span class="sxs-lookup"><span data-stu-id="8c527-238">**ShowWindow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c527-239">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="8c527-239">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8c527-240">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8c527-240">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8c527-241">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| 進程和執行緒結構 \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| wShowWindow" ) </span><span class="sxs-lookup"><span data-stu-id="8c527-241">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|wShowWindow")</span></span>
</dt> </dl>

<span data-ttu-id="8c527-242">視窗顯示給使用者的方式。</span><span class="sxs-lookup"><span data-stu-id="8c527-242">How the window is displayed to the user.</span></span> <span data-ttu-id="8c527-243">它可以是任何可在 [ShowWindow](/windows/desktop/api/winuser/nf-winuser-showwindow)函數的 *nCmdShow* 參數中指定的值。</span><span class="sxs-lookup"><span data-stu-id="8c527-243">It can be any of the values that can be specified in the *nCmdShow* parameter for the [ShowWindow](/windows/desktop/api/winuser/nf-winuser-showwindow) function.</span></span>

</dd> <dt>

<span data-ttu-id="8c527-244">**標題**</span><span class="sxs-lookup"><span data-stu-id="8c527-244">**Title**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c527-245">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8c527-245">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c527-246">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8c527-246">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8c527-247">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| 進程和執行緒結構 \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| lpTitle" ) </span><span class="sxs-lookup"><span data-stu-id="8c527-247">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|lpTitle")</span></span>
</dt> </dl>

<span data-ttu-id="8c527-248">建立新的主控台視窗時，標題列中顯示的文字;用於主控台進程。</span><span class="sxs-lookup"><span data-stu-id="8c527-248">Text displayed in the title bar when a new console window is created; used for console processes.</span></span> <span data-ttu-id="8c527-249">如果是 **Null**，就會使用可執行檔的名稱做為視窗標題。</span><span class="sxs-lookup"><span data-stu-id="8c527-249">If **NULL**, the name of the executable file is used as the window title.</span></span> <span data-ttu-id="8c527-250">如果 GUI 或主控台進程未建立新的主控台視窗，此屬性必須是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="8c527-250">This property must be **NULL** for GUI or console processes that do not create a new console window.</span></span>

</dd> <dt>

<span data-ttu-id="8c527-251">**WinstationDesktop**</span><span class="sxs-lookup"><span data-stu-id="8c527-251">**WinstationDesktop**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c527-252">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8c527-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c527-253">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8c527-253">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8c527-254">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| 進程和執行緒結構 \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| lpDesktop" ) </span><span class="sxs-lookup"><span data-stu-id="8c527-254">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|lpDesktop")</span></span>
</dt> </dl>

<span data-ttu-id="8c527-255">電腦的名稱或桌上型電腦和視窗的名稱。</span><span class="sxs-lookup"><span data-stu-id="8c527-255">The name of the desktop or the name of both the desktop and window station for the process.</span></span> <span data-ttu-id="8c527-256">字串中的反斜線表示字串同時包含桌面和視窗工作站名稱。</span><span class="sxs-lookup"><span data-stu-id="8c527-256">A backslash in the string indicates that the string includes both desktop and window station names.</span></span> <span data-ttu-id="8c527-257">如果 **WinstationDesktop** 為 **Null**，則新的進程會繼承其父進程的桌面和視窗工作站。</span><span class="sxs-lookup"><span data-stu-id="8c527-257">If **WinstationDesktop** is **NULL**, the new process inherits the desktop and window station of its parent process.</span></span> <span data-ttu-id="8c527-258">如果 **WinstationDesktop** 是空字串，進程就不會繼承其父進程的桌面和視窗。</span><span class="sxs-lookup"><span data-stu-id="8c527-258">If **WinstationDesktop** is an empty string, the process does not inherit the desktop and window station of its parent process.</span></span> <span data-ttu-id="8c527-259">系統會決定是否必須建立新的桌面和視窗工作站。</span><span class="sxs-lookup"><span data-stu-id="8c527-259">The system determines if a new desktop and window station must be created.</span></span> <span data-ttu-id="8c527-260">視窗工作站是安全的物件，其中包含剪貼簿、一組全域原子，以及一組桌面物件。</span><span class="sxs-lookup"><span data-stu-id="8c527-260">A window station is a secure object that contains a clipboard, a set of global atoms, and a group of desktop objects.</span></span> <span data-ttu-id="8c527-261">指派給互動式使用者登入會話的互動式視窗工作站也包含鍵盤、滑鼠和顯示裝置。</span><span class="sxs-lookup"><span data-stu-id="8c527-261">The interactive window station that is assigned to the logon session of the interactive user also contains the keyboard, mouse, and display device.</span></span> <span data-ttu-id="8c527-262">桌面是包含在視窗工作站內的安全物件。</span><span class="sxs-lookup"><span data-stu-id="8c527-262">A desktop is a secure object contained within a window station.</span></span> <span data-ttu-id="8c527-263">桌面具有邏輯顯示介面，並且包含視窗、功能表和勾點。</span><span class="sxs-lookup"><span data-stu-id="8c527-263">A desktop has a logical display surface and contains windows, menus, and hooks.</span></span> <span data-ttu-id="8c527-264">視窗工作站可以有多個桌面。</span><span class="sxs-lookup"><span data-stu-id="8c527-264">A window station can have multiple desktops.</span></span> <span data-ttu-id="8c527-265">只有互動式視窗工作站的桌面可以看見，並接收使用者輸入。</span><span class="sxs-lookup"><span data-stu-id="8c527-265">Only the desktops of the interactive window station can be visible and receive user input.</span></span>

</dd> <dt>

<span data-ttu-id="8c527-266">**X**</span><span class="sxs-lookup"><span data-stu-id="8c527-266">**X**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c527-267">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8c527-267">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8c527-268">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8c527-268">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8c527-269">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| 進程和執行緒結構 \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| dwX" ) </span><span class="sxs-lookup"><span data-stu-id="8c527-269">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|dwX")</span></span>
</dt> </dl>

<span data-ttu-id="8c527-270">視窗左上角的 X 位移（如果建立新視窗）（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="8c527-270">The X offset of the upper left corner of a window if a new window is created—in pixels.</span></span> <span data-ttu-id="8c527-271">位移是從畫面的左上角。</span><span class="sxs-lookup"><span data-stu-id="8c527-271">The offsets are from the upper left corner of the screen.</span></span> <span data-ttu-id="8c527-272">若是 GUI 進程，當 **CreateWindow** 的 *X* 參數是 **CW \_ USEDEFAULT** 時，新的進程第一次呼叫 [**createwindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)來建立重迭的視窗時，就會使用指定的位置。</span><span class="sxs-lookup"><span data-stu-id="8c527-272">For GUI processes, the specified position is used the first time the new process calls [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) to create an overlapped window if the *X* parameter of **CreateWindow** is **CW\_USEDEFAULT**.</span></span>

> <span data-ttu-id="8c527-273">\[!附注 X\]</span><span class="sxs-lookup"><span data-stu-id="8c527-273">\[!Note  X\]</span></span>  
> <span data-ttu-id="8c527-274">和 **Y** 不能獨立指定。</span><span class="sxs-lookup"><span data-stu-id="8c527-274">and **Y** cannot be specified independently.</span></span>

 

</dd> <dt>

<span data-ttu-id="8c527-275">**XCountChars**</span><span class="sxs-lookup"><span data-stu-id="8c527-275">**XCountChars**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c527-276">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8c527-276">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8c527-277">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8c527-277">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8c527-278">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| 進程和執行緒結構 \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| XCountChars" ) </span><span class="sxs-lookup"><span data-stu-id="8c527-278">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|XCountChars")</span></span>
</dt> </dl>

<span data-ttu-id="8c527-279">字元資料行中的螢幕緩衝區寬度。</span><span class="sxs-lookup"><span data-stu-id="8c527-279">Screen buffer width in character columns.</span></span> <span data-ttu-id="8c527-280">這個屬性會用於建立主控台視窗的進程，而且在 GUI 進程中會被忽略。</span><span class="sxs-lookup"><span data-stu-id="8c527-280">This property is used for processes that create a console window, and is ignored in GUI processes.</span></span>

> [!Note]  
> <span data-ttu-id="8c527-281">**XCountChars** 和 **YCountChars** 不能獨立指定。</span><span class="sxs-lookup"><span data-stu-id="8c527-281">**XCountChars** and **YCountChars** cannot be specified independently.</span></span>

 

</dd> <dt>

<span data-ttu-id="8c527-282">**XSize**</span><span class="sxs-lookup"><span data-stu-id="8c527-282">**XSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c527-283">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8c527-283">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8c527-284">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8c527-284">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8c527-285">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| 進程和執行緒結構 \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| dwXSize" ) </span><span class="sxs-lookup"><span data-stu-id="8c527-285">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|dwXSize")</span></span>
</dt> </dl>

<span data-ttu-id="8c527-286">視窗的圖元寬度（如果已建立新視窗）。</span><span class="sxs-lookup"><span data-stu-id="8c527-286">Pixel width of a window if a new window is created.</span></span> <span data-ttu-id="8c527-287">若是 GUI 進程，只有在新的進程第一次呼叫 [**createwindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) 來建立重迭的視窗時，才會使用此程式，如果 **CreateWindow** 的 nWidth 參數是 **CW \_ USEDEFAULT**。</span><span class="sxs-lookup"><span data-stu-id="8c527-287">For GUI processes, this is only used the first time the new process calls [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) to create an overlapped window if the nWidth parameter of **CreateWindow** is **CW\_USEDEFAULT**.</span></span>

> [!Note]  
> <span data-ttu-id="8c527-288">**XSize** 和 **YSize** 不能獨立指定。</span><span class="sxs-lookup"><span data-stu-id="8c527-288">**XSize** and **YSize** cannot be specified independently.</span></span>

 

</dd> <dt>

<span data-ttu-id="8c527-289">**Y**</span><span class="sxs-lookup"><span data-stu-id="8c527-289">**Y**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c527-290">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8c527-290">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8c527-291">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8c527-291">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8c527-292">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| 進程和執行緒結構 \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| dwY" ) </span><span class="sxs-lookup"><span data-stu-id="8c527-292">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|dwY")</span></span>
</dt> </dl>

<span data-ttu-id="8c527-293">當建立新視窗時，視窗左上角的圖元位移。</span><span class="sxs-lookup"><span data-stu-id="8c527-293">Pixel offset of the upper-left corner of a window if a new window is created.</span></span> <span data-ttu-id="8c527-294">位移是從畫面的左上角。</span><span class="sxs-lookup"><span data-stu-id="8c527-294">The offsets are from the upper-left corner of the screen.</span></span> <span data-ttu-id="8c527-295">若是 GUI 進程，當 **CreateWindow** 的 *y* 參數是 **CW \_ USEDEFAULT** 時，新的進程第一次呼叫 [**createwindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)來建立重迭的視窗時，就會使用指定的位置。</span><span class="sxs-lookup"><span data-stu-id="8c527-295">For GUI processes, the specified position is used the first time the new process calls [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) to create an overlapped window if the *y* parameter of **CreateWindow** is **CW\_USEDEFAULT**.</span></span>

> <span data-ttu-id="8c527-296">\[!附注 X\]</span><span class="sxs-lookup"><span data-stu-id="8c527-296">\[!Note  X\]</span></span>  
> <span data-ttu-id="8c527-297">和 **Y** 不能獨立指定。</span><span class="sxs-lookup"><span data-stu-id="8c527-297">and **Y** cannot be specified independently.</span></span>

 

</dd> <dt>

<span data-ttu-id="8c527-298">**YCountChars**</span><span class="sxs-lookup"><span data-stu-id="8c527-298">**YCountChars**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c527-299">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8c527-299">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8c527-300">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8c527-300">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8c527-301">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| 進程和執行緒結構 \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| YCountChars" ) </span><span class="sxs-lookup"><span data-stu-id="8c527-301">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|YCountChars")</span></span>
</dt> </dl>

<span data-ttu-id="8c527-302">字元資料列中的螢幕緩衝區高度。</span><span class="sxs-lookup"><span data-stu-id="8c527-302">Screen buffer height in character rows.</span></span> <span data-ttu-id="8c527-303">這個屬性會用於建立主控台視窗的進程，但是 GUI 進程會忽略此屬性。</span><span class="sxs-lookup"><span data-stu-id="8c527-303">This property is used for processes that create a console window, but is ignored in GUI processes.</span></span>

> [!Note]  
> <span data-ttu-id="8c527-304">**XCountChars** 和 **YCountChars** 不能獨立指定。</span><span class="sxs-lookup"><span data-stu-id="8c527-304">**XCountChars** and **YCountChars** cannot be specified independently.</span></span>

 

</dd> <dt>

<span data-ttu-id="8c527-305">**YSize**</span><span class="sxs-lookup"><span data-stu-id="8c527-305">**YSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c527-306">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8c527-306">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8c527-307">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8c527-307">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8c527-308">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| 進程和執行緒結構 \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| dwYSize" ) </span><span class="sxs-lookup"><span data-stu-id="8c527-308">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|dwYSize")</span></span>
</dt> </dl>

<span data-ttu-id="8c527-309">如果建立新視窗，則為視窗的圖元高度。</span><span class="sxs-lookup"><span data-stu-id="8c527-309">Pixel height of a window if a new window is created.</span></span> <span data-ttu-id="8c527-310">若是 GUI 進程，只有在新的進程第一次呼叫 [**createwindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)來建立重 **迭的視窗** 時，才會使用此程式，如果 *nWidth* 參數是 **CW \_ USEDEFAULT**。</span><span class="sxs-lookup"><span data-stu-id="8c527-310">For GUI processes, this is used only the first time the new process calls [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) to create an overlapped window if the *nWidth* parameter of **CreateWindow** is **CW\_USEDEFAULT**.</span></span>

> [!Note]  
> <span data-ttu-id="8c527-311">**XSize** 和 **YSize** 不能獨立指定。</span><span class="sxs-lookup"><span data-stu-id="8c527-311">**XSize** and **YSize** cannot be specified independently.</span></span>

 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8c527-312">備註</span><span class="sxs-lookup"><span data-stu-id="8c527-312">Remarks</span></span>

<span data-ttu-id="8c527-313">這個類別衍生自 [**Win32 \_ MethodParameterClass**](win32-methodparameterclass.md)。</span><span class="sxs-lookup"><span data-stu-id="8c527-313">This class is derived from [**Win32\_MethodParameterClass**](win32-methodparameterclass.md).</span></span>

<span data-ttu-id="8c527-314">概觀</span><span class="sxs-lookup"><span data-stu-id="8c527-314">Overview</span></span>

<span data-ttu-id="8c527-315">[**Win32 \_ Process**](win32-process.md) [**Create**](create-method-in-class-win32-process.md)方法可讓您針對在電腦上執行的任何新進程設定啟動選項。</span><span class="sxs-lookup"><span data-stu-id="8c527-315">The [**Win32\_Process**](win32-process.md) [**Create**](create-method-in-class-win32-process.md) method enables you to configure startup options for any new process running on a computer.</span></span> <span data-ttu-id="8c527-316">例如，您可以設定一個進程，讓它從「隱藏」視窗開始，以防止使用者看到，也可能會中斷。</span><span class="sxs-lookup"><span data-stu-id="8c527-316">For example, you can configure a process so that it starts in a "hidden" window, which prevents a user from seeing, and possibly interrupting, it.</span></span> <span data-ttu-id="8c527-317">如果進程是在命令視窗中執行，您可以設定視窗的大小、標題和前景和背景色彩。</span><span class="sxs-lookup"><span data-stu-id="8c527-317">If the process runs in a command window, you can configure the size, title, and foreground and background colors of the window.</span></span>

<span data-ttu-id="8c527-318">啟動選項是使用 **Win32 \_ ProcessStartup** 類別來設定。</span><span class="sxs-lookup"><span data-stu-id="8c527-318">Startup options are configured using the **Win32\_ProcessStartup** class.</span></span> <span data-ttu-id="8c527-319">**Win32 \_ProcessStartup** 是方法類型類別;方法類型類別僅存在於將資訊傳遞給方法。</span><span class="sxs-lookup"><span data-stu-id="8c527-319">**Win32\_ProcessStartup** is a Method Type class; the Method Type class exists solely to pass information to a method.</span></span> <span data-ttu-id="8c527-320">在此情況下， **win32 \_ ProcessStartup** 實例的所有屬性都會傳遞給 [**win32 \_ 進程**](win32-process.md)的實例。</span><span class="sxs-lookup"><span data-stu-id="8c527-320">In this case, all the properties of an instance of **Win32\_ProcessStartup** are passed to an instance of [**Win32\_Process**](win32-process.md).</span></span>

<span data-ttu-id="8c527-321">**使用 Win32 \_ ProcessStartup**</span><span class="sxs-lookup"><span data-stu-id="8c527-321">**Using Win32\_ProcessStartup**</span></span>

1.  <span data-ttu-id="8c527-322">建立 **Win32 \_ ProcessStartup** 的實例。</span><span class="sxs-lookup"><span data-stu-id="8c527-322">Create an instance of **Win32\_ProcessStartup**.</span></span>
2.  <span data-ttu-id="8c527-323">設定新實例的屬性。</span><span class="sxs-lookup"><span data-stu-id="8c527-323">Configure the properties of the new instance.</span></span>
3.  <span data-ttu-id="8c527-324">將此實例包含為 [**Win32 \_ 進程**](win32-process.md) Create 方法的一部分。</span><span class="sxs-lookup"><span data-stu-id="8c527-324">Include the instance as part of the [**Win32\_Process**](win32-process.md) Create method.</span></span>

<span data-ttu-id="8c527-325">例如，如果您已建立名為 objConfig 的 **Win32 \_ ProcessStartup** 實例，則會在 Create 方法中傳遞物件名稱，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8c527-325">For example, if you have created a **Win32\_ProcessStartup** instance named objConfig, you would pass the object name in the Create method as follows:</span></span>

`errReturn = objProcess.Create("Database.exe", null, objConfig, intProcessID)`

## <a name="examples"></a><span data-ttu-id="8c527-326">範例</span><span class="sxs-lookup"><span data-stu-id="8c527-326">Examples</span></span>

<span data-ttu-id="8c527-327">您可以使用 **Win32 \_ ProcessStartup** 類別來設定進程的各種啟動選項。</span><span class="sxs-lookup"><span data-stu-id="8c527-327">You can use the **Win32\_ProcessStartup** class to configure various startup options for a process.</span></span> <span data-ttu-id="8c527-328">這些選項包括（但不限於）在隱藏視窗中建立進程，以及建立更高優先順序的程式等事項。</span><span class="sxs-lookup"><span data-stu-id="8c527-328">These options include, but are not limited to, such things as creating a process in a hidden window and creating a higher-priority process.</span></span> <span data-ttu-id="8c527-329">下列 VBScript 會在隱藏視窗中建立處理常式。</span><span class="sxs-lookup"><span data-stu-id="8c527-329">The following VBScript creates a process in a hidden window.</span></span>


```VB
Const HIDDEN_WINDOW = 12
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set objStartup = objWMIService.Get("Win32_ProcessStartup")
Set objConfig = objStartup.SpawnInstance_
objConfig.ShowWindow = HIDDEN_WINDOW
Set objProcess = GetObject("winmgmts:root\cimv2:Win32_Process")
errReturn = objProcess.Create("Notepad.exe", null, objConfig, intProcessID)
```



<span data-ttu-id="8c527-330">下列 VBScript 會建立較高優先順序的進程。</span><span class="sxs-lookup"><span data-stu-id="8c527-330">The following VBScript creates a higher-priority process.</span></span>


```VB
Const ABOVE_NORMAL = 32768
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set objStartup = objWMIService.Get("Win32_ProcessStartup")
Set objConfig = objStartup.SpawnInstance_
objConfig.PriorityClass = ABOVE_NORMAL
Set objProcess = GetObject("winmgmts:root\cimv2:Win32_Process")
objProcess.Create "Database.exe", Null, objConfig, intProcessID
```



<span data-ttu-id="8c527-331">下列 VBScript 程式碼範例會在本機電腦上建立「記事本」處理常式。</span><span class="sxs-lookup"><span data-stu-id="8c527-331">The following VBScript code example creates a Notepad process on the local computer.</span></span> <span data-ttu-id="8c527-332">**Win32 \_ProcessStartup** 用來設定處理常式設定。</span><span class="sxs-lookup"><span data-stu-id="8c527-332">**Win32\_ProcessStartup** is used to configure the process settings.</span></span>


```VB
Const SW_NORMAL = 1
strComputer = "."
strCommand = "Notepad.exe" 
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

' Configure the Notepad process to show a window
Set objStartup = objWMIService.Get("Win32_ProcessStartup")
Set objConfig = objStartup.SpawnInstance_
objConfig.ShowWindow = SW_NORMAL

' Create Notepad process
Set objProcess = objWMIService.Get("Win32_Process")
intReturn = objProcess.Create _
    (strCommand, Null, objConfig, intProcessID)
If intReturn <> 0 Then
    Wscript.Echo "Process could not be created." & vbNewLine & _
                 "Command line: " & strCommand & vbNewLine & _
                 "Return value: " & intReturn
Else
    Wscript.Echo "Process created." & vbNewLine & _
                 "Command line: " & strCommand & vbNewLine & _
                 "Process ID: " & intProcessID
End If
```



## <a name="requirements"></a><span data-ttu-id="8c527-333">規格需求</span><span class="sxs-lookup"><span data-stu-id="8c527-333">Requirements</span></span>



| <span data-ttu-id="8c527-334">需求</span><span class="sxs-lookup"><span data-stu-id="8c527-334">Requirement</span></span> | <span data-ttu-id="8c527-335">值</span><span class="sxs-lookup"><span data-stu-id="8c527-335">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8c527-336">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8c527-336">Minimum supported client</span></span><br/> | <span data-ttu-id="8c527-337">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8c527-337">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8c527-338">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8c527-338">Minimum supported server</span></span><br/> | <span data-ttu-id="8c527-339">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8c527-339">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8c527-340">命名空間</span><span class="sxs-lookup"><span data-stu-id="8c527-340">Namespace</span></span><br/>                | <span data-ttu-id="8c527-341">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="8c527-341">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8c527-342">MOF</span><span class="sxs-lookup"><span data-stu-id="8c527-342">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8c527-343"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="8c527-343"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8c527-344">DLL</span><span class="sxs-lookup"><span data-stu-id="8c527-344">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8c527-345"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c527-345"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c527-346">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8c527-346">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c527-347">**Win32 \_ MethodParameterClass**</span><span class="sxs-lookup"><span data-stu-id="8c527-347">**Win32\_MethodParameterClass**</span></span>](win32-methodparameterclass.md)
</dt> <dt>

[<span data-ttu-id="8c527-348">作業系統類別</span><span class="sxs-lookup"><span data-stu-id="8c527-348">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> <dt>

[<span data-ttu-id="8c527-349">**Win32 \_ 進程**</span><span class="sxs-lookup"><span data-stu-id="8c527-349">**Win32\_Process**</span></span>](win32-process.md)
</dt> <dt>

[<span data-ttu-id="8c527-350">**\_\_ProviderHostQuotaConfiguration**</span><span class="sxs-lookup"><span data-stu-id="8c527-350">**\_\_ProviderHostQuotaConfiguration**</span></span>](../wmisdk/--providerhostquotaconfiguration.md)
</dt> <dt>

[<span data-ttu-id="8c527-351">WMI 工作：進程</span><span class="sxs-lookup"><span data-stu-id="8c527-351">WMI Tasks: Processes</span></span>](../wmisdk/wmi-tasks--processes.md)
</dt> </dl>

 

 
