---
description: 當事件傳遞給它時，CommandLineEventConsumer 類別會在本機系統中啟動任意進程。
ms.assetid: 0dcae783-1722-45a4-b5d4-3fcf455dacf8
ms.tgt_platform: multiple
title: CommandLineEventConsumer 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CommandLineEventConsumer
- CommandLineEventConsumer.CreatorSID
- CommandLineEventConsumer.MachineName
- CommandLineEventConsumer.MaximumQueueSize
- CommandLineEventConsumer.CommandLineTemplate
- CommandLineEventConsumer.CreateNewConsole
- CommandLineEventConsumer.CreateNewProcessGroup
- CommandLineEventConsumer.CreateSeparateWowVdm
- CommandLineEventConsumer.CreateSharedWowVdm
- CommandLineEventConsumer.DesktopName
- CommandLineEventConsumer.ExecutablePath
- CommandLineEventConsumer.FillAttributes
- CommandLineEventConsumer.ForceOffFeedback
- CommandLineEventConsumer.ForceOnFeedback
- CommandLineEventConsumer.KillTimeout
- CommandLineEventConsumer.Name
- CommandLineEventConsumer.Priority
- CommandLineEventConsumer.RunInteractively
- CommandLineEventConsumer.ShowWindowCommand
- CommandLineEventConsumer.UseDefaultErrorMode
- CommandLineEventConsumer.WindowTitle
- CommandLineEventConsumer.WorkingDirectory
- CommandLineEventConsumer.XCoordinate
- CommandLineEventConsumer.XNumCharacters
- CommandLineEventConsumer.XSize
- CommandLineEventConsumer.YCoordinate
- CommandLineEventConsumer.YNumCharacters
- CommandLineEventConsumer.YSize
- CommandLineEventConsumer.FillAttribute
api_type:
- DllExport
api_location:
- Wbemcons.dll
ms.openlocfilehash: 1784ba116417f6ed94aed2249a797cf8de4b3527
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/02/2021
ms.locfileid: "106976308"
---
# <a name="commandlineeventconsumer-class"></a><span data-ttu-id="10c32-103">CommandLineEventConsumer 類別</span><span class="sxs-lookup"><span data-stu-id="10c32-103">CommandLineEventConsumer class</span></span>

<span data-ttu-id="10c32-104">當事件傳遞給它時， **CommandLineEventConsumer** 類別會在本機系統中啟動任意進程。</span><span class="sxs-lookup"><span data-stu-id="10c32-104">The **CommandLineEventConsumer** class starts an arbitrary process in the local system when an event is delivered to it.</span></span> <span data-ttu-id="10c32-105">此類別是 WMI 提供的其中一個標準事件取用者。</span><span class="sxs-lookup"><span data-stu-id="10c32-105">This class is one of the standard event consumers that WMI provides.</span></span> <span data-ttu-id="10c32-106">如需詳細資訊，請參閱 [使用標準取用者監視及回應事件](monitoring-and-responding-to-events-with-standard-consumers.md)。</span><span class="sxs-lookup"><span data-stu-id="10c32-106">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

> [!Note]  
> <span data-ttu-id="10c32-107">使用 **CommandLineEventConsumer** 類別時，請保護您想要啟動的可執行檔。</span><span class="sxs-lookup"><span data-stu-id="10c32-107">When using the **CommandLineEventConsumer** class, secure the executable that you want to start.</span></span> <span data-ttu-id="10c32-108">如果可執行檔不在安全的位置，或使用強式存取控制清單來保護 (ACL) ，未經授權的使用者就可以使用惡意可執行檔來取代您的可執行檔。</span><span class="sxs-lookup"><span data-stu-id="10c32-108">If the executable is not in a secure location, or secured with a strong access control list (ACL), an unauthorized user can replace your executable with a malicious executable.</span></span> <span data-ttu-id="10c32-109">如需 Acl 的詳細資訊，請造訪 Microsoft Windows 軟體開發套件 (SDK) 的安全性一節，並參閱 [建立新物件的安全描述項](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--)。</span><span class="sxs-lookup"><span data-stu-id="10c32-109">For more information about ACLs, visit the Security section of the Microsoft Windows Software Development Kit (SDK), and see [Creating a Security Descriptor for a New Object](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="10c32-110">語法</span><span class="sxs-lookup"><span data-stu-id="10c32-110">Syntax</span></span>

``` syntax
[AMENDMENT]
class CommandLineEventConsumer : __EventConsumer
{
  uint8   CreatorSID[];
  string  MachineName;
  uint32  MaximumQueueSize;
  string  CommandLineTemplate;
  boolean CreateNewConsole = False;
  boolean CreateNewProcessGroup = True;
  boolean CreateSeparateWowVdm = False;
  boolean CreateSharedWowVdm = False;
  string  DesktopName;
  string  ExecutablePath;
  uint32  FillAttributes;
  boolean ForceOffFeedback = False;
  boolean ForceOnFeedback = False;
  uint32  KillTimeout = 0;
  string  Name;
  sint32  Priority = 0x20;
  boolean RunInteractively = False;
  uint32  ShowWindowCommand;
  boolean UseDefaultErrorMode = False;
  string  WindowTitle;
  string  WorkingDirectory;
  uint32  XCoordinate;
  uint32  XNumCharacters;
  uint32  XSize;
  uint32  YCoordinate;
  uint32  YNumCharacters;
  uint32  YSize;
  uint32  FillAttribute;
};
```

## <a name="members"></a><span data-ttu-id="10c32-111">成員</span><span class="sxs-lookup"><span data-stu-id="10c32-111">Members</span></span>

<span data-ttu-id="10c32-112">**CommandLineEventConsumer** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="10c32-112">The **CommandLineEventConsumer** class has these types of members:</span></span>

-   [<span data-ttu-id="10c32-113">屬性</span><span class="sxs-lookup"><span data-stu-id="10c32-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="10c32-114">屬性</span><span class="sxs-lookup"><span data-stu-id="10c32-114">Properties</span></span>

<span data-ttu-id="10c32-115">**CommandLineEventConsumer** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="10c32-115">The **CommandLineEventConsumer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="10c32-116">**CommandLineTemplate**</span><span class="sxs-lookup"><span data-stu-id="10c32-116">**CommandLineTemplate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10c32-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="10c32-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10c32-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10c32-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10c32-119">指定要啟動之進程的標準字串範本。</span><span class="sxs-lookup"><span data-stu-id="10c32-119">Standard string template that specifies the process to be started.</span></span> <span data-ttu-id="10c32-120">這個屬性可以是 **Null**，而且會使用 **ExecutablePath** 屬性做為命令列。</span><span class="sxs-lookup"><span data-stu-id="10c32-120">This property can be **NULL**, and the **ExecutablePath** property is used as the command line.</span></span>

</dd> <dt>

<span data-ttu-id="10c32-121">**CreateNewConsole**</span><span class="sxs-lookup"><span data-stu-id="10c32-121">**CreateNewConsole**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10c32-122">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="10c32-122">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="10c32-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10c32-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10c32-124">未使用。</span><span class="sxs-lookup"><span data-stu-id="10c32-124">Not used.</span></span> <span data-ttu-id="10c32-125">如果將值指派給這個屬性，就會產生追蹤訊息。</span><span class="sxs-lookup"><span data-stu-id="10c32-125">If a value is assigned to this property, a tracing message is generated.</span></span> <span data-ttu-id="10c32-126">如需詳細資訊，請參閱 [追蹤 WMI 活動](tracing-wmi-activity.md)。</span><span class="sxs-lookup"><span data-stu-id="10c32-126">For more information, see [Tracing WMI Activity](tracing-wmi-activity.md).</span></span>

</dd> <dt>

<span data-ttu-id="10c32-127">**CreateNewProcessGroup**</span><span class="sxs-lookup"><span data-stu-id="10c32-127">**CreateNewProcessGroup**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10c32-128">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="10c32-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="10c32-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10c32-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10c32-130">若 **為 True**，則新的進程是新進程群組的根進程。</span><span class="sxs-lookup"><span data-stu-id="10c32-130">If **True**, the new process is the root process of a new process group.</span></span> <span data-ttu-id="10c32-131">進程群組包含此根進程下階的所有進程。</span><span class="sxs-lookup"><span data-stu-id="10c32-131">The process group includes all processes that are descendants of this root process.</span></span> <span data-ttu-id="10c32-132">新進程群組的處理序識別碼與此進程識別碼相同。</span><span class="sxs-lookup"><span data-stu-id="10c32-132">The process identifier of the new process group is the same as this process identifier.</span></span> <span data-ttu-id="10c32-133">[**GenerateConsoleCtrlEvent**](/windows/console/generateconsolectrlevent)方法會使用進程群組來啟用將 Ctrl + C 或 CTRL + BREAK 信號傳送給一組主控台進程。</span><span class="sxs-lookup"><span data-stu-id="10c32-133">Process groups are used by the [**GenerateConsoleCtrlEvent**](/windows/console/generateconsolectrlevent) method to enable sending a CTRL+C or CTRL+BREAK signal to a group of console processes.</span></span>

</dd> <dt>

<span data-ttu-id="10c32-134">**CreateSeparateWowVdm**</span><span class="sxs-lookup"><span data-stu-id="10c32-134">**CreateSeparateWowVdm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10c32-135">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="10c32-135">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="10c32-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10c32-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10c32-137">若 **為 True**，新的進程會在 (VDM) 的私人虛擬 DOS 機器上執行。</span><span class="sxs-lookup"><span data-stu-id="10c32-137">If **True**, the new process runs in a private Virtual DOS Machine (VDM).</span></span> <span data-ttu-id="10c32-138">這只有在啟動在16位 Windows 作業系統上執行的應用程式時才有效。</span><span class="sxs-lookup"><span data-stu-id="10c32-138">This is only valid when starting an application running on a 16-bit Windows operating system.</span></span> <span data-ttu-id="10c32-139">如果設定為 **False**，在16位 Windows 作業系統上執行的所有應用程式都會在單一共用的 VDM 中以執行緒的形式執行。</span><span class="sxs-lookup"><span data-stu-id="10c32-139">If set to **False**, all applications running on a 16-bit Windows operating system run as threads in a single, shared VDM.</span></span> <span data-ttu-id="10c32-140">如需詳細資訊，請參閱本主題的「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="10c32-140">For more information, see the Remarks section of this topic.</span></span>

</dd> <dt>

<span data-ttu-id="10c32-141">**CreateSharedWowVdm**</span><span class="sxs-lookup"><span data-stu-id="10c32-141">**CreateSharedWowVdm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10c32-142">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="10c32-142">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="10c32-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10c32-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10c32-144">若 **為 True**， [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) 方法會在共用虛擬 DOS 機器 (VDM) 中執行新的進程。</span><span class="sxs-lookup"><span data-stu-id="10c32-144">If **True**, the [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) method runs the new process in the shared Virtual DOS Machine (VDM).</span></span> <span data-ttu-id="10c32-145">如果設定為 **True**，此屬性可以覆寫 Win.ini 的 Windows 區段中的 DefaultSeparateVDM 參數。</span><span class="sxs-lookup"><span data-stu-id="10c32-145">This property can override the DefaultSeparateVDM switch in the Windows section of Win.ini if set to **True**.</span></span> <span data-ttu-id="10c32-146">如需詳細資訊，請參閱本主題的「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="10c32-146">For more information, see the Remarks section of this topic.</span></span>

</dd> <dt>

<span data-ttu-id="10c32-147">**CreatorSID**</span><span class="sxs-lookup"><span data-stu-id="10c32-147">**CreatorSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10c32-148">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="10c32-148">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="10c32-149">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10c32-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10c32-150">安全識別碼 (SID) ，可唯一識別建立篩選的使用者。</span><span class="sxs-lookup"><span data-stu-id="10c32-150">Security identifier (SID) that uniquely identifies the user who creates a filter.</span></span> <span data-ttu-id="10c32-151">根據作業系統而定，WMI 會儲存建立 [**\_ \_ EventConsumer**](--eventconsumer.md)實例或系統管理員 SID 之使用者的 SID。</span><span class="sxs-lookup"><span data-stu-id="10c32-151">WMI stores the SID of the user who creates an instance of [**\_\_EventConsumer**](--eventconsumer.md) or the Administrator SID, depending on the operating system.</span></span> <span data-ttu-id="10c32-152">如需詳細資訊，請參閱使用邏輯取用者來系結 [事件篩選器](binding-an-event-filter-with-a-logical-consumer.md) ，以及 [使用標準取用者來監視和回應事件](monitoring-and-responding-to-events-with-standard-consumers.md)。</span><span class="sxs-lookup"><span data-stu-id="10c32-152">For more information, see [Binding an Event Filter with a Logical Consumer](binding-an-event-filter-with-a-logical-consumer.md) and [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

<span data-ttu-id="10c32-153">這個屬性繼承自 [**\_ \_ EventConsumer**](--eventconsumer.md)。</span><span class="sxs-lookup"><span data-stu-id="10c32-153">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="10c32-154">**DesktopName**</span><span class="sxs-lookup"><span data-stu-id="10c32-154">**DesktopName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10c32-155">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="10c32-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10c32-156">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10c32-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10c32-157">未使用。</span><span class="sxs-lookup"><span data-stu-id="10c32-157">Not used.</span></span> <span data-ttu-id="10c32-158">如果將值指派給這個屬性，就會產生追蹤訊息。</span><span class="sxs-lookup"><span data-stu-id="10c32-158">If a value is assigned to this property a tracing message is generated.</span></span> <span data-ttu-id="10c32-159">如需詳細資訊，請參閱 [追蹤 WMI 活動](tracing-wmi-activity.md)。</span><span class="sxs-lookup"><span data-stu-id="10c32-159">For more information, see [Tracing WMI Activity](tracing-wmi-activity.md).</span></span>

</dd> <dt>

<span data-ttu-id="10c32-160">**ExecutablePath**</span><span class="sxs-lookup"><span data-stu-id="10c32-160">**ExecutablePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10c32-161">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="10c32-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10c32-162">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10c32-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10c32-163">要執行的模組。</span><span class="sxs-lookup"><span data-stu-id="10c32-163">Module to execute.</span></span> <span data-ttu-id="10c32-164">此字串可以指定要執行之模組的完整路徑和檔案名，或者可以指定部分名稱。</span><span class="sxs-lookup"><span data-stu-id="10c32-164">The string can specify the full path and file name of the module to execute, or it can specify a partial name.</span></span> <span data-ttu-id="10c32-165">如果指定了部分名稱，則會假設為目前的磁片磁碟機和目前的目錄。</span><span class="sxs-lookup"><span data-stu-id="10c32-165">If a partial name is specified, the current drive and current directory are assumed.</span></span>

<span data-ttu-id="10c32-166">**ExecutablePath** 屬性可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="10c32-166">The **ExecutablePath** property can be **NULL**.</span></span> <span data-ttu-id="10c32-167">在此情況下，模組名稱必須是 **CommandLineTemplate** 屬性值中的第一個空白字元分隔標記。</span><span class="sxs-lookup"><span data-stu-id="10c32-167">In that case, the module name must be the first white space-delimited token in the **CommandLineTemplate** property value.</span></span> <span data-ttu-id="10c32-168">如果使用包含空格的長檔名，請使用加上引號的字串來指出檔案名的結尾，而引數則會開始闡明檔案名。</span><span class="sxs-lookup"><span data-stu-id="10c32-168">If using a long file name that contains a space, use quoted strings to indicate where the file name ends and the arguments begin to clarify the file name.</span></span>

> [!Note]  
> <span data-ttu-id="10c32-169">因為 **CommandLineTemplate** 屬性可以是要執行的模組所提供的範本，所以 **Null** **ExecutablePath** 屬性會允許在參數中指定的模組執行，然後不在您的控制項中。</span><span class="sxs-lookup"><span data-stu-id="10c32-169">Because the **CommandLineTemplate** property can be a template where the module to execute is supplied by a variable, a **NULL** **ExecutablePath** property permits the module that is specified in the parameter to execute, and then it is out of your control.</span></span> <span data-ttu-id="10c32-170">一律在 **CommandLineEventConsumer** 註冊中將 **ExecutablePath** 屬性設定為包含必要的可執行檔，以避免事件參數的覆寫。</span><span class="sxs-lookup"><span data-stu-id="10c32-170">Always set the **ExecutablePath** property in the **CommandLineEventConsumer** registration to include the required executable, which avoids overwriting by events parameters.</span></span> <span data-ttu-id="10c32-171">如果您必須使用範本和變數來指定要執行的模組，請小心將命名空間中的完整寫入權限授與誰。</span><span class="sxs-lookup"><span data-stu-id="10c32-171">If you must use a template and variable to specify the module to execute, be careful about who is granted full write privilege in the namespace.</span></span>

 

</dd> <dt>

<span data-ttu-id="10c32-172">**FillAttribute**</span><span class="sxs-lookup"><span data-stu-id="10c32-172">**FillAttribute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10c32-173">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="10c32-173">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10c32-174">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10c32-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10c32-175">指定在主控台應用程式中建立新的主控台視窗時的初始文字和背景色彩</span><span class="sxs-lookup"><span data-stu-id="10c32-175">Specifies the initial text and background colors if a new console window is created in a console application</span></span>

</dd> <dt>

<span data-ttu-id="10c32-176">**FillAttributes**</span><span class="sxs-lookup"><span data-stu-id="10c32-176">**FillAttributes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10c32-177">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="10c32-177">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10c32-178">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="10c32-178">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="10c32-179">初始文字和背景色彩，如果在主控台應用程式中建立新的主控台視窗。</span><span class="sxs-lookup"><span data-stu-id="10c32-179">Initial text and background colors, if a new console window is created in a console application.</span></span> <span data-ttu-id="10c32-180">GUI 應用程式會忽略這個屬性。</span><span class="sxs-lookup"><span data-stu-id="10c32-180">This property is ignored in a GUI application.</span></span> <span data-ttu-id="10c32-181">值可以是下列值的任何組合。</span><span class="sxs-lookup"><span data-stu-id="10c32-181">The value can be any combination of the following values.</span></span>

<dt>

<span data-ttu-id="10c32-182">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="10c32-182">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="10c32-183">藍色前景</span><span class="sxs-lookup"><span data-stu-id="10c32-183">blue foreground</span></span>

</dd> <dt>

<span data-ttu-id="10c32-184">2 (0x2) </span><span class="sxs-lookup"><span data-stu-id="10c32-184">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="10c32-185">綠色前景</span><span class="sxs-lookup"><span data-stu-id="10c32-185">green foreground</span></span>

</dd> <dt>

<span data-ttu-id="10c32-186">4 (0x4) </span><span class="sxs-lookup"><span data-stu-id="10c32-186">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="10c32-187">紅色前景</span><span class="sxs-lookup"><span data-stu-id="10c32-187">red foreground</span></span>

</dd> <dt>

<span data-ttu-id="10c32-188">8 (0x8) </span><span class="sxs-lookup"><span data-stu-id="10c32-188">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="10c32-189">前景濃度</span><span class="sxs-lookup"><span data-stu-id="10c32-189">foreground intensity</span></span>

</dd> <dt>

<span data-ttu-id="10c32-190">16 (0x10) </span><span class="sxs-lookup"><span data-stu-id="10c32-190">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="10c32-191">藍色背景</span><span class="sxs-lookup"><span data-stu-id="10c32-191">blue background</span></span>

</dd> <dt>

<span data-ttu-id="10c32-192">32 (0x20) </span><span class="sxs-lookup"><span data-stu-id="10c32-192">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="10c32-193">綠色背景</span><span class="sxs-lookup"><span data-stu-id="10c32-193">green background</span></span>

</dd> <dt>

<span data-ttu-id="10c32-194">64 (0x40) </span><span class="sxs-lookup"><span data-stu-id="10c32-194">64 (0x40)</span></span>
</dt> <dd>

<span data-ttu-id="10c32-195">紅色背景</span><span class="sxs-lookup"><span data-stu-id="10c32-195">red background</span></span>

</dd> <dt>

<span data-ttu-id="10c32-196">128 (0x80) </span><span class="sxs-lookup"><span data-stu-id="10c32-196">128 (0x80)</span></span>
</dt> <dd>

<span data-ttu-id="10c32-197">背景濃度</span><span class="sxs-lookup"><span data-stu-id="10c32-197">background intensity</span></span>

</dd> </dl>

<span data-ttu-id="10c32-198">例如，下列組合會在白色背景產生紅色文字：</span><span class="sxs-lookup"><span data-stu-id="10c32-198">For example, the following combinations produce red text on a white background:</span></span>


```mof
0x4 | 0x40 | 0x20 | 0x10
```



  <span data-ttu-id="10c32-199">或</span><span class="sxs-lookup"><span data-stu-id="10c32-199">or</span></span>  


```mof
0x74
```



</dd> <dt>

<span data-ttu-id="10c32-200">**ForceOffFeedback**</span><span class="sxs-lookup"><span data-stu-id="10c32-200">**ForceOffFeedback**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10c32-201">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="10c32-201">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="10c32-202">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10c32-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10c32-203">若 **為 True**，則會在進程啟動時強制關閉意見反應資料指標。</span><span class="sxs-lookup"><span data-stu-id="10c32-203">If **True**, the feedback cursor is forced off while the process is starting.</span></span> <span data-ttu-id="10c32-204">一般游標隨即顯示。</span><span class="sxs-lookup"><span data-stu-id="10c32-204">The normal cursor is displayed.</span></span>

</dd> <dt>

<span data-ttu-id="10c32-205">**ForceOnFeedback**</span><span class="sxs-lookup"><span data-stu-id="10c32-205">**ForceOnFeedback**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10c32-206">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="10c32-206">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="10c32-207">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10c32-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10c32-208">若 **為 True**，則在呼叫 [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) 之後，資料指標處於意見反應模式兩秒。</span><span class="sxs-lookup"><span data-stu-id="10c32-208">If **True**, the cursor is in feedback mode for two seconds after [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) is called.</span></span> <span data-ttu-id="10c32-209">在這兩秒鐘內，如果程式進行第一個 GUI 呼叫，系統會在進程中提供五秒鐘的時間。</span><span class="sxs-lookup"><span data-stu-id="10c32-209">During those two seconds, if the process makes the first GUI call, the system gives five more seconds to the process.</span></span> <span data-ttu-id="10c32-210">在這五秒內，如果進程顯示視窗，系統會為程式提供另五秒的時間，以完成視窗繪製。</span><span class="sxs-lookup"><span data-stu-id="10c32-210">During those five seconds, if the process shows a window, the system gives another five seconds to the process to finish drawing the window.</span></span>

</dd> <dt>

<span data-ttu-id="10c32-211">**KillTimeout**</span><span class="sxs-lookup"><span data-stu-id="10c32-211">**KillTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10c32-212">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="10c32-212">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10c32-213">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10c32-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10c32-214">WMI 服務在結束進程 0 (零之前等候的數目（以秒為單位）) 表示不終止進程。</span><span class="sxs-lookup"><span data-stu-id="10c32-214">Number, in seconds, that the WMI service waits before killing a process 0 (zero) indicates a process is not to be killed.</span></span> <span data-ttu-id="10c32-215">終止進程可防止進程無限期執行。</span><span class="sxs-lookup"><span data-stu-id="10c32-215">Killing a process prevents a process from running indefinitely.</span></span>

</dd> <dt>

<span data-ttu-id="10c32-216">**MachineName**</span><span class="sxs-lookup"><span data-stu-id="10c32-216">**MachineName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10c32-217">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="10c32-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10c32-218">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10c32-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10c32-219">Windows Management Instrumentation (WMI) 傳送事件的電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="10c32-219">Name of the computer to which Windows Management Instrumentation (WMI) sends events.</span></span>

<span data-ttu-id="10c32-220">這個屬性繼承自 [**\_ \_ EventConsumer**](--eventconsumer.md)。</span><span class="sxs-lookup"><span data-stu-id="10c32-220">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="10c32-221">**MaximumQueueSize**</span><span class="sxs-lookup"><span data-stu-id="10c32-221">**MaximumQueueSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10c32-222">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="10c32-222">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10c32-223">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10c32-223">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10c32-224">特定取用者的佇列上限，以位元組為單位。</span><span class="sxs-lookup"><span data-stu-id="10c32-224">Maximum queue for a specific consumer, in bytes.</span></span>

<span data-ttu-id="10c32-225">這個屬性繼承自 [**\_ \_ EventConsumer**](--eventconsumer.md)。</span><span class="sxs-lookup"><span data-stu-id="10c32-225">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="10c32-226">**名稱**</span><span class="sxs-lookup"><span data-stu-id="10c32-226">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10c32-227">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="10c32-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10c32-228">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10c32-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10c32-229">限定詞：索引 [**鍵**](key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="10c32-229">Qualifiers: [**key**](key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="10c32-230">取用者的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="10c32-230">Unique name of a consumer.</span></span>

</dd> <dt>

<span data-ttu-id="10c32-231">**優先順序**</span><span class="sxs-lookup"><span data-stu-id="10c32-231">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10c32-232">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="10c32-232">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="10c32-233">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10c32-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10c32-234">排程進程執行緒的優先權層級。</span><span class="sxs-lookup"><span data-stu-id="10c32-234">Scheduling priority level of the process threads.</span></span> <span data-ttu-id="10c32-235">下列清單列出可用的優先權層級。</span><span class="sxs-lookup"><span data-stu-id="10c32-235">The following list lists the priority levels available.</span></span>

<dt>

<span data-ttu-id="10c32-236">32 (0x20) </span><span class="sxs-lookup"><span data-stu-id="10c32-236">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="10c32-237">表示不需要排程的一般處理常式。</span><span class="sxs-lookup"><span data-stu-id="10c32-237">Indicates a normal process without scheduling needs.</span></span>

</dd> <dt>

<span data-ttu-id="10c32-238">64 (0x40) </span><span class="sxs-lookup"><span data-stu-id="10c32-238">64 (0x40)</span></span>
</dt> <dd>

<span data-ttu-id="10c32-239">指出只有在系統閒置時才會執行執行緒的進程，並由在較高優先順序類別中執行之進程的執行緒佔用。</span><span class="sxs-lookup"><span data-stu-id="10c32-239">Indicates a process whose threads run only when the system is idle, and are preempted by the threads of any process running in a higher priority class.</span></span> <span data-ttu-id="10c32-240">螢幕保護裝置是一個例子。</span><span class="sxs-lookup"><span data-stu-id="10c32-240">An example is a screen saver.</span></span> <span data-ttu-id="10c32-241">閒置優先權類別是由子進程繼承。</span><span class="sxs-lookup"><span data-stu-id="10c32-241">The idle priority class is inherited by child processes.</span></span>

</dd> <dt>

<span data-ttu-id="10c32-242">128 (0x80) </span><span class="sxs-lookup"><span data-stu-id="10c32-242">128 (0x80)</span></span>
</dt> <dd>

<span data-ttu-id="10c32-243">表示執行高優先順序、時間關鍵工作的進程。</span><span class="sxs-lookup"><span data-stu-id="10c32-243">Indicates a process that performs high-priority, time critical tasks.</span></span> <span data-ttu-id="10c32-244">高優先順序類別進程的執行緒會 shutdown 一般優先順序或閒置優先順序類別進程的執行緒。</span><span class="sxs-lookup"><span data-stu-id="10c32-244">The threads of a high-priority class process preempts the threads of normal-priority or idle-priority class processes.</span></span> <span data-ttu-id="10c32-245">其中一個範例就是工作清單，當使用者呼叫時，無論系統的負載為何，都必須快速回應。</span><span class="sxs-lookup"><span data-stu-id="10c32-245">An example is the Task List, which must respond quickly when called by the user regardless of the load on the system.</span></span> <span data-ttu-id="10c32-246">使用高優先順序類別時請特別小心，因為具有高優先順序類別的 CPU 系結應用程式可使用幾乎所有可用的迴圈。</span><span class="sxs-lookup"><span data-stu-id="10c32-246">Use extreme care when using the high-priority class, because a CPU-bound application with a high-priority class can use nearly all available cycles.</span></span>

</dd> <dt>

<span data-ttu-id="10c32-247">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="10c32-247">256 (0x100)</span></span>
</dt> <dd>

<span data-ttu-id="10c32-248">表示具有最高可能優先順序的進程。</span><span class="sxs-lookup"><span data-stu-id="10c32-248">Indicates a process that has the highest possible priority.</span></span> <span data-ttu-id="10c32-249">即時優先權類別進程的執行緒會優先處理所有其他進程的執行緒，包括執行重要工作的作業系統進程。</span><span class="sxs-lookup"><span data-stu-id="10c32-249">The threads of a real-time priority class process preempt the threads of all other processes, including operating system processes that perform important tasks.</span></span> <span data-ttu-id="10c32-250">例如，執行超過短暫間隔的即時程式可能會導致磁碟快取無法排清，或導致滑鼠沒有回應。</span><span class="sxs-lookup"><span data-stu-id="10c32-250">For example, a real-time process that executes for more than a brief interval can cause disk caches not to flush, or cause the mouse to be unresponsive.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="10c32-251">**RunInteractively**</span><span class="sxs-lookup"><span data-stu-id="10c32-251">**RunInteractively**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10c32-252">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="10c32-252">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="10c32-253">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10c32-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10c32-254">若 **為 True**，則會在互動式 WinStation 中啟動進程。</span><span class="sxs-lookup"><span data-stu-id="10c32-254">If **True**, the process is launched in the interactive WinStation.</span></span> <span data-ttu-id="10c32-255">如果 **為 False**，則會在預設服務 WinStation 中啟動進程。</span><span class="sxs-lookup"><span data-stu-id="10c32-255">If **False**, the process is launched in the default service WinStation.</span></span> <span data-ttu-id="10c32-256">這個屬性會覆寫 **DesktopName** 屬性。</span><span class="sxs-lookup"><span data-stu-id="10c32-256">This property overrides the **DesktopName** property.</span></span> <span data-ttu-id="10c32-257">這個屬性只會在本機使用，而且只有在互動式使用者是設定取用者的相同使用者時才會使用。</span><span class="sxs-lookup"><span data-stu-id="10c32-257">This property is only used locally, and only if the interactive user is the same user who set up the consumer.</span></span>

<span data-ttu-id="10c32-258">從 Windows Vista 開始，執行 **CommandLineEventConsumer** 實例的進程會在 **LocalSystem** 帳戶下啟動，而且會在會話0中。</span><span class="sxs-lookup"><span data-stu-id="10c32-258">Starting with Windows Vista, the process running the **CommandLineEventConsumer** instance is started under the **LocalSystem** account and is in session 0.</span></span> <span data-ttu-id="10c32-259">在會話0中執行的服務無法與使用者會話互動。</span><span class="sxs-lookup"><span data-stu-id="10c32-259">Services which run in session 0 cannot interact with user sessions.</span></span>

</dd> <dt>

<span data-ttu-id="10c32-260">**ShowWindowCommand**</span><span class="sxs-lookup"><span data-stu-id="10c32-260">**ShowWindowCommand**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10c32-261">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="10c32-261">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10c32-262">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10c32-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10c32-263">視窗顯示狀態。</span><span class="sxs-lookup"><span data-stu-id="10c32-263">Window show state.</span></span> <span data-ttu-id="10c32-264">它可以是任何可在 [ShowWindow](/windows/desktop/api/winuser/nf-winuser-showwindow)函數的 *nCmdShow* 參數中指定的值。</span><span class="sxs-lookup"><span data-stu-id="10c32-264">It can be any of the values that can be specified in the *nCmdShow* parameter for the [ShowWindow](/windows/desktop/api/winuser/nf-winuser-showwindow) function.</span></span>

</dd> <dt>

<span data-ttu-id="10c32-265">**UseDefaultErrorMode**</span><span class="sxs-lookup"><span data-stu-id="10c32-265">**UseDefaultErrorMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10c32-266">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="10c32-266">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="10c32-267">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10c32-267">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10c32-268">若 **為 True**，則會使用預設的錯誤模式。</span><span class="sxs-lookup"><span data-stu-id="10c32-268">If **True**, the default error mode is used.</span></span>

</dd> <dt>

<span data-ttu-id="10c32-269">**System.windows.controls.page.windowtitle**</span><span class="sxs-lookup"><span data-stu-id="10c32-269">**WindowTitle**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10c32-270">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="10c32-270">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10c32-271">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10c32-271">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10c32-272">出現在進程標題列上的標題。</span><span class="sxs-lookup"><span data-stu-id="10c32-272">Title that appears on the title bar of the process.</span></span> <span data-ttu-id="10c32-273">GUI 應用程式會忽略這個屬性。</span><span class="sxs-lookup"><span data-stu-id="10c32-273">This property is ignored for GUI applications.</span></span>

</dd> <dt>

<span data-ttu-id="10c32-274">**WorkingDirectory**</span><span class="sxs-lookup"><span data-stu-id="10c32-274">**WorkingDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10c32-275">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="10c32-275">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10c32-276">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10c32-276">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10c32-277">此進程的工作目錄。</span><span class="sxs-lookup"><span data-stu-id="10c32-277">Working directory for this process.</span></span>

</dd> <dt>

<span data-ttu-id="10c32-278">**XCoordinate**</span><span class="sxs-lookup"><span data-stu-id="10c32-278">**XCoordinate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10c32-279">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="10c32-279">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10c32-280">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10c32-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10c32-281">從畫面的左邊緣到視窗左邊緣的 X 位移（以圖元為單位），如果已建立新視窗。</span><span class="sxs-lookup"><span data-stu-id="10c32-281">X-offset, in pixels, from the left edge of the screen to the left edge of the window, if a new window is created.</span></span>

</dd> <dt>

<span data-ttu-id="10c32-282">**XNumCharacters**</span><span class="sxs-lookup"><span data-stu-id="10c32-282">**XNumCharacters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10c32-283">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="10c32-283">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10c32-284">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10c32-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10c32-285">如果已建立新的主控台視窗，則為字元資料行中的螢幕緩衝區寬度。</span><span class="sxs-lookup"><span data-stu-id="10c32-285">Screen buffer width, in character columns, if a new console window is created.</span></span> <span data-ttu-id="10c32-286">GUI 進程會忽略這個屬性。</span><span class="sxs-lookup"><span data-stu-id="10c32-286">This property is ignored in a GUI process.</span></span>

</dd> <dt>

<span data-ttu-id="10c32-287">**XSize**</span><span class="sxs-lookup"><span data-stu-id="10c32-287">**XSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10c32-288">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="10c32-288">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10c32-289">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10c32-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10c32-290">新視窗的寬度（以圖元為單位），如果已建立新視窗。</span><span class="sxs-lookup"><span data-stu-id="10c32-290">Width, in pixels, of a new window, if a new window is created.</span></span>

</dd> <dt>

<span data-ttu-id="10c32-291">**YCoordinate**</span><span class="sxs-lookup"><span data-stu-id="10c32-291">**YCoordinate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10c32-292">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="10c32-292">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10c32-293">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10c32-293">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10c32-294">以圖元為單位的 Y 位移（以圖元為單位），表示已建立新視窗。</span><span class="sxs-lookup"><span data-stu-id="10c32-294">Y-offset, in pixels, from the top edge of the screen to the top edge of the window, if a new window is created.</span></span>

</dd> <dt>

<span data-ttu-id="10c32-295">**YNumCharacters**</span><span class="sxs-lookup"><span data-stu-id="10c32-295">**YNumCharacters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10c32-296">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="10c32-296">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10c32-297">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10c32-297">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10c32-298">螢幕緩衝區高度，在字元資料列中，如果已建立新的主控台視窗。</span><span class="sxs-lookup"><span data-stu-id="10c32-298">Screen buffer height, in character rows, if a new console window is created.</span></span> <span data-ttu-id="10c32-299">GUI 進程會忽略這個屬性。</span><span class="sxs-lookup"><span data-stu-id="10c32-299">This property is ignored in a GUI process.</span></span>

</dd> <dt>

<span data-ttu-id="10c32-300">**YSize**</span><span class="sxs-lookup"><span data-stu-id="10c32-300">**YSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10c32-301">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="10c32-301">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10c32-302">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10c32-302">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10c32-303">新視窗的高度（以圖元為單位），如果已建立新視窗。</span><span class="sxs-lookup"><span data-stu-id="10c32-303">Height, in pixels, of the new window, if a new window is created.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="10c32-304">備註</span><span class="sxs-lookup"><span data-stu-id="10c32-304">Remarks</span></span>

<span data-ttu-id="10c32-305">**CommandLineEventConsumer** 類別衍生自 [**\_ \_ EventConsumer**](--eventconsumer.md)抽象類別。</span><span class="sxs-lookup"><span data-stu-id="10c32-305">The **CommandLineEventConsumer** class is derived from the [**\_\_EventConsumer**](--eventconsumer.md) abstract class.</span></span>

<span data-ttu-id="10c32-306">**CreateSeparateWowVdm** 屬性指出新的進程是否會在 (VDM) 的私人虛擬 DOS 電腦中執行。</span><span class="sxs-lookup"><span data-stu-id="10c32-306">The **CreateSeparateWowVdm** property indicates whether or not the new process runs in a private Virtual DOS Machine (VDM).</span></span> <span data-ttu-id="10c32-307">另外執行的優點是損毀只會終止單一的 VDM。</span><span class="sxs-lookup"><span data-stu-id="10c32-307">The advantage of running separately is that a crash only terminates the single VDM.</span></span> <span data-ttu-id="10c32-308">在相異 VDMs 中執行的程式會繼續正常運作，而在不同 VDMs 中執行的16位 Windows 應用程式會有不同的輸入佇列。</span><span class="sxs-lookup"><span data-stu-id="10c32-308">Programs running in distinct VDMs continue to function normally, and the 16-bit Windows-based applications running in separate VDMs have separate input queues.</span></span> <span data-ttu-id="10c32-309">這表示，如果某個應用程式停止回應，則個別 VDMs 中的應用程式會繼續接收輸入。</span><span class="sxs-lookup"><span data-stu-id="10c32-309">This means that if one application stops responding momentarily, the applications in separate VDMs continue to receive input.</span></span> <span data-ttu-id="10c32-310">另外執行的缺點是，它需要更多的記憶體才能執行這項作業。</span><span class="sxs-lookup"><span data-stu-id="10c32-310">The disadvantage of running separately is that it takes significantly more memory to do so.</span></span> <span data-ttu-id="10c32-311">只有當使用者要求以16位 Windows 為基礎的應用程式在自己的 VDM 中執行時，才應該將此屬性設定為 **True** 。</span><span class="sxs-lookup"><span data-stu-id="10c32-311">You should set this property to **True** only if the user requests that 16-bit Windows-based applications run in their own VDM.</span></span>

> [!Note]  
> <span data-ttu-id="10c32-312">**CommandLineEventConsumer** 會在內部使用 [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa)方法，並將 **ExecutablePath** 和 **CommandLineTemplate** 屬性作為 *lpApplicationName* 和 *lpCommandLine* 參數傳遞。</span><span class="sxs-lookup"><span data-stu-id="10c32-312">The **CommandLineEventConsumer** uses the [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) method internally, and passes the **ExecutablePath** and **CommandLineTemplate** properties as the *lpApplicationName* and *lpCommandLine* parameters.</span></span> <span data-ttu-id="10c32-313">下列受控物件格式 (MOF) 程式碼範例不會正確地使用 **CommandLineEventConsumer** 。</span><span class="sxs-lookup"><span data-stu-id="10c32-313">The following Managed Object Format (MOF) code example does not use **CommandLineEventConsumer** correctly.</span></span>

 


```mof
instance of CommandLineEventConsumer
{
  ExecutablePath = "C:\\windows\\system32\\cscript.exe";
  CommandLineTemplate = "C:\\scripts\\MyScript.js param1 param2";
};
```



<span data-ttu-id="10c32-314">[**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa)方法會將 *lpCommandLine* 傳遞為 `argv[0]` 、 `argv[1]` 等等。</span><span class="sxs-lookup"><span data-stu-id="10c32-314">The [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) method passes *lpCommandLine* as `argv[0]`, `argv[1]`, and so on.</span></span> <span data-ttu-id="10c32-315">因為 `argv[0]` 針對用來保留可執行檔名稱的16位應用程式，所以先前的 MOF 程式碼會導致建立程式，如同在命令提示字元中輸入下列命令： **c： \\ windows \\ system32 \\cscript.exe param1 param2**。</span><span class="sxs-lookup"><span data-stu-id="10c32-315">Because `argv[0]` for 16-bit applications used to be reserved for the executable file name, the previous MOF code results in the process being created as though the following command is entered at the command prompt: **c:\\windows\\system32\\cscript.exe param1 param2**.</span></span>

<span data-ttu-id="10c32-316">先前的命令不會成功，因為 Cscript.exe 不會查看 `argv[0]` ，所以無法辨識它不包含自己的名稱，而是其他 ( "c： \\ \\ scripts \\ \\MyScript.js" ) 。</span><span class="sxs-lookup"><span data-stu-id="10c32-316">The previous command does not succeed because Cscript.exe does not look at `argv[0]`, and so it does not recognize that it does not contain its own name, but something else ("c:\\\\scripts\\\\MyScript.js").</span></span> <span data-ttu-id="10c32-317">下列範例會識別 **CommandLineEventConsumer** 的建議用法。</span><span class="sxs-lookup"><span data-stu-id="10c32-317">The following example identifies the recommended use of **CommandLineEventConsumer**.</span></span>


```mof
instance of CommandLineEventConsumer
{
  ExecutablePath = "C:\\windows\\system32\\cscript.exe";
  CommandLineTemplate = "C:\\windows\\system32\\cscript.exe"
    "C:\\scripts\\MyScript.js param1 param2";
};
```



<span data-ttu-id="10c32-318">先前使用的 **CommandLineEventConsumer** 結果是在命令提示字元中輸入下列命令時所建立的進程： **c： \\ windows \\ system32 \\cscript.exe c： \\ scripts \\MyScript.js param1 param2**</span><span class="sxs-lookup"><span data-stu-id="10c32-318">The previous use of **CommandLineEventConsumer** results in the process created as though the following command was entered at the command prompt: **c:\\windows\\system32\\cscript.exe c:\\scripts\\MyScript.js param1 param2**</span></span>

<span data-ttu-id="10c32-319">因為「c： \\ \\ 腳本 \\ \\MyScript.js」現在已 `argv[1]` Cscript.exe，所以命令會成功。</span><span class="sxs-lookup"><span data-stu-id="10c32-319">Because "c:\\\\scripts\\\\MyScript.js" is now `argv[1]`, it is seen by Cscript.exe and the command succeeds.</span></span>

<span data-ttu-id="10c32-320">如需詳細資訊，請參閱 [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) 函數。</span><span class="sxs-lookup"><span data-stu-id="10c32-320">For more information, see the [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) function.</span></span>

## <a name="examples"></a><span data-ttu-id="10c32-321">範例</span><span class="sxs-lookup"><span data-stu-id="10c32-321">Examples</span></span>

<span data-ttu-id="10c32-322">如需使用 **CommandLineEventConsumer** 來建立取用者的範例，請參閱 [根據事件從命令列執行程式](running-a-program-from-the-command-line-based-on-an-event.md)。</span><span class="sxs-lookup"><span data-stu-id="10c32-322">For an example of using **CommandLineEventConsumer** to create a consumer, see [Running a Program from the Command Line Based on an Event](running-a-program-from-the-command-line-based-on-an-event.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="10c32-323">規格需求</span><span class="sxs-lookup"><span data-stu-id="10c32-323">Requirements</span></span>



| <span data-ttu-id="10c32-324">需求</span><span class="sxs-lookup"><span data-stu-id="10c32-324">Requirement</span></span> | <span data-ttu-id="10c32-325">值</span><span class="sxs-lookup"><span data-stu-id="10c32-325">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="10c32-326">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="10c32-326">Minimum supported client</span></span><br/> | <span data-ttu-id="10c32-327">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="10c32-327">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="10c32-328">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="10c32-328">Minimum supported server</span></span><br/> | <span data-ttu-id="10c32-329">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="10c32-329">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="10c32-330">命名空間</span><span class="sxs-lookup"><span data-stu-id="10c32-330">Namespace</span></span><br/>                | <span data-ttu-id="10c32-331">根 \\ 訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="10c32-331">Root\\subscription</span></span><br/>                                                           |
| <span data-ttu-id="10c32-332">MOF</span><span class="sxs-lookup"><span data-stu-id="10c32-332">MOF</span></span><br/>                      | <dl> <span data-ttu-id="10c32-333"><dt>Wbemcons mof</dt></span><span class="sxs-lookup"><span data-stu-id="10c32-333"><dt>Wbemcons.mof</dt></span></span> </dl> |
| <span data-ttu-id="10c32-334">DLL</span><span class="sxs-lookup"><span data-stu-id="10c32-334">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10c32-335"><dt>Wbemcons.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10c32-335"><dt>Wbemcons.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10c32-336">另請參閱</span><span class="sxs-lookup"><span data-stu-id="10c32-336">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10c32-337">標準取用者類別</span><span class="sxs-lookup"><span data-stu-id="10c32-337">Standard Consumer Classes</span></span>](standard-consumer-classes.md)
</dt> <dt>

[<span data-ttu-id="10c32-338">使用標準取用者監視及回應事件</span><span class="sxs-lookup"><span data-stu-id="10c32-338">Monitoring and Responding to Events with Standard Consumers</span></span>](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> <dt>

[<span data-ttu-id="10c32-339">建立邏輯取用者</span><span class="sxs-lookup"><span data-stu-id="10c32-339">Creating a Logical Consumer</span></span>](creating-a-logical-consumer.md)
</dt> <dt>

[<span data-ttu-id="10c32-340">隨時接收事件</span><span class="sxs-lookup"><span data-stu-id="10c32-340">Receiving Events At All Times</span></span>](receiving-events-at-all-times.md)
</dt> <dt>

[<span data-ttu-id="10c32-341">**\_\_EventConsumer**</span><span class="sxs-lookup"><span data-stu-id="10c32-341">**\_\_EventConsumer**</span></span>](--eventconsumer.md)
</dt> </dl>

 

