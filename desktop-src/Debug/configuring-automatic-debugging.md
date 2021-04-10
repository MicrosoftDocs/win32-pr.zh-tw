---
description: 使用者可以設定自動偵測，以協助他們判斷其系統或應用程式停止回應的原因。
ms.assetid: c3c7aa98-c298-452c-b8d0-10a08b4d82a3
title: 設定自動調試
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2630784d678e08b67a93d00ec52d9bc67c949bc7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110000"
---
# <a name="configuring-automatic-debugging"></a><span data-ttu-id="45dfe-103">設定自動調試</span><span class="sxs-lookup"><span data-stu-id="45dfe-103">Configuring Automatic Debugging</span></span>

<span data-ttu-id="45dfe-104">使用者可以設定自動偵測，以協助他們判斷其系統或應用程式停止回應的原因。</span><span class="sxs-lookup"><span data-stu-id="45dfe-104">Users can configure automatic debugging to help them determine why their system or an application has stopped responding.</span></span>

## <a name="configuring-automatic-debugging-for-system-crashes"></a><span data-ttu-id="45dfe-105">設定系統損毀的自動偵測</span><span class="sxs-lookup"><span data-stu-id="45dfe-105">Configuring Automatic Debugging for System Crashes</span></span>

<span data-ttu-id="45dfe-106">若要設定目的電腦在系統停止回應時產生損毀傾印檔案，請使用主控台中的 **系統** 應用程式。</span><span class="sxs-lookup"><span data-stu-id="45dfe-106">To configure the target computer to generate a crash dump file when the system stops responding, use the **System** application in Control Panel.</span></span> <span data-ttu-id="45dfe-107">按一下 [ **Advanced system settings**]，這會顯示 [ **系統** 內容] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="45dfe-107">Click **Advanced system settings**, which displays the **System Properties** dialog box.</span></span> <span data-ttu-id="45dfe-108">在該方塊的 [ **Advanced** ] 索引標籤上，按一下 [**啟動和** 復原] 下的 [**設定**]，然後使用適當的修復選項。</span><span class="sxs-lookup"><span data-stu-id="45dfe-108">On the **Advanced** tab of that box, click **Settings** under **Startup and Recovery**, and then use the appropriate recovery options.</span></span> <span data-ttu-id="45dfe-109">或者，您可以使用下列登錄機碼來設定損毀傾印選項：</span><span class="sxs-lookup"><span data-stu-id="45dfe-109">Alternatively, you can configure crash dump options using the following registry key:</span></span>

<span data-ttu-id="45dfe-110">**HKEY \_本機 \_ 電腦** \\ **系統** \\ **CurrentControlSet** \\ **控制項** \\ **CrashControl**</span><span class="sxs-lookup"><span data-stu-id="45dfe-110">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Control**\\**CrashControl**</span></span>

<span data-ttu-id="45dfe-111">您可以指定的檔案是損毀傾印檔案。</span><span class="sxs-lookup"><span data-stu-id="45dfe-111">The file you can specify is the crash dump file.</span></span> <span data-ttu-id="45dfe-112">其預設名稱為 Memory。</span><span class="sxs-lookup"><span data-stu-id="45dfe-112">Its default name is Memory.dmp.</span></span> <span data-ttu-id="45dfe-113">您可以使用核心模式的偵錯工具（例如 WinDbg 或 KD）來進行損毀傾印的偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="45dfe-113">You can debug a crash dump with a kernel-mode debugger, such as WinDbg or KD.</span></span> <span data-ttu-id="45dfe-114">如需詳細資訊，請參閱偵錯工具隨附的檔。</span><span class="sxs-lookup"><span data-stu-id="45dfe-114">For more information, see the documentation included with the debugger.</span></span>

## <a name="configuring-automatic-debugging-for-application-crashes"></a><span data-ttu-id="45dfe-115">設定應用程式損毀的自動偵測</span><span class="sxs-lookup"><span data-stu-id="45dfe-115">Configuring Automatic Debugging for Application Crashes</span></span>

<span data-ttu-id="45dfe-116">當應用程式停止回應時 (例如，在存取違規) 之後，系統會自動叫用登錄中指定的偵錯工具進行事後的偵錯工具，如果已正確設定命令列，則會將處理序識別碼和事件控制碼傳遞至偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="45dfe-116">When an application stops responding (for example, after an access violation), the system automatically invokes a debugger that is specified in the registry for postmortem debugging, The process ID and event handle are passed to the debugger if the command line is properly configured.</span></span> <span data-ttu-id="45dfe-117">下列程式描述如何在登錄中指定偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="45dfe-117">The following procedure describes how to specify a debugger in the registry.</span></span>

<span data-ttu-id="45dfe-118">**將偵錯工具設定為事後偵錯工具**</span><span class="sxs-lookup"><span data-stu-id="45dfe-118">**To set a debugger as the postmortem debugger**</span></span>

1.  <span data-ttu-id="45dfe-119">移至下列登錄機碼：</span><span class="sxs-lookup"><span data-stu-id="45dfe-119">Go to the following registry key:</span></span>

    <span data-ttu-id="45dfe-120">**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **AeDebug**</span><span class="sxs-lookup"><span data-stu-id="45dfe-120">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Windows NT**\\**CurrentVersion**\\**AeDebug**</span></span>

2.  <span data-ttu-id="45dfe-121">使用指定偵錯工具命令列的 REG SZ 字串，來新增或編輯 **偵錯工具** 值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="45dfe-121">Add or edit the **Debugger** value, using a REG\_SZ string that specifies the command line for the debugger.</span></span>

    <span data-ttu-id="45dfe-122">字串應包含偵錯工具可執行檔的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="45dfe-122">The string should include the fully qualified path to the debugger executable.</span></span> <span data-ttu-id="45dfe-123">以 "% ld" 參數表示偵錯工具命令列的處理序識別碼和事件控制碼。</span><span class="sxs-lookup"><span data-stu-id="45dfe-123">Indicate the process ID and event handle with "%ld" parameters to the debugger command line.</span></span> <span data-ttu-id="45dfe-124">不同的偵錯工具可能會有自己的參數語法來指出這些值。</span><span class="sxs-lookup"><span data-stu-id="45dfe-124">Different debuggers may have their own parameter syntaxes for indicating these values.</span></span> <span data-ttu-id="45dfe-125">叫用偵錯工具時，會以處理序識別碼取代第一個 "% ld"，然後將第二個 "% ld" 取代成事件控制碼。</span><span class="sxs-lookup"><span data-stu-id="45dfe-125">When the debugger is invoked, the first "%ld" is replaced with the process ID and the second "%ld" is replaced with the event handle.</span></span>

    <span data-ttu-id="45dfe-126">下列文字是如何將 WinDbg 設定為偵錯工具的範例。</span><span class="sxs-lookup"><span data-stu-id="45dfe-126">The following text is an example of how to setup up WinDbg as the debugger.</span></span>

    ``` syntax
    "C:\debuggers\windbg.exe" -p %ld -e %ld -g
    ```

3.  <span data-ttu-id="45dfe-127">如果您想要在沒有使用者互動的情況下叫用偵錯工具， 請在叫用 \_ 偵錯工具之前，使用指定系統是否應該對使用者顯示對話方塊的 REG SZ 字串，來新增或編輯自動值。</span><span class="sxs-lookup"><span data-stu-id="45dfe-127">If you want the debugger to be invoked without user interaction, add or edit the **Auto** value, using a REG\_SZ string that specifies whether the system should display a dialog box to the user before the debugger is invoked.</span></span> <span data-ttu-id="45dfe-128">字串 "1" 停用此對話方塊;字串 "0" 會啟用對話方塊。</span><span class="sxs-lookup"><span data-stu-id="45dfe-128">The string "1" disables the dialog box; the string "0" enables the dialog box.</span></span>

## <a name="excluding-an-application-from-automatic-debugging"></a><span data-ttu-id="45dfe-129">從自動偵測排除應用程式</span><span class="sxs-lookup"><span data-stu-id="45dfe-129">Excluding an Application from Automatic Debugging</span></span>

<span data-ttu-id="45dfe-130">下列程式描述如何在 **AeDebug** 索引鍵的 **自動** 值設定為1之後，從自動偵測排除應用程式。</span><span class="sxs-lookup"><span data-stu-id="45dfe-130">The following procedure describes how to exclude an application from automatic debugging after the **Auto** value under the **AeDebug** key has been set to 1.</span></span>

<span data-ttu-id="45dfe-131">**若要將應用程式從自動偵錯工具中排除**</span><span class="sxs-lookup"><span data-stu-id="45dfe-131">**To exclude an application from automatic debugging**</span></span>

1.  <span data-ttu-id="45dfe-132">移至下列登錄機碼：</span><span class="sxs-lookup"><span data-stu-id="45dfe-132">Go to the following registry key:</span></span>

    <span data-ttu-id="45dfe-133">**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **AeDebug**</span><span class="sxs-lookup"><span data-stu-id="45dfe-133">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Windows NT**\\**CurrentVersion**\\**AeDebug**</span></span>

2.  <span data-ttu-id="45dfe-134">將 REG \_ DWORD 值新增至 **AutoExclusionList** 子機碼，其中名稱是可執行檔的名稱，而值為1。</span><span class="sxs-lookup"><span data-stu-id="45dfe-134">Add a REG\_DWORD value to the **AutoExclusionList** subkey, where the name is the name of the executable file and the value is 1.</span></span> <span data-ttu-id="45dfe-135">根據預設，桌面視窗管理員 (Dwm.exe) 會從自動偵錯工具中排除，否則如果 Dwm.exe 停止回應，則會發生系統鎖死 (使用者無法看到偵錯工具所顯示的介面，因為 Dwm.exe 沒有回應，而且 Dwm.exe 因為偵錯工具) 而無法終止。</span><span class="sxs-lookup"><span data-stu-id="45dfe-135">By default, the Desktop Window Manager (Dwm.exe) is excluded from automatic debugging because otherwise a system deadlock can occur if Dwm.exe stops responding (the user cannot see the interface displayed by the debugger because Dwm.exe isn't responding, and Dwm.exe cannot terminate because it is held by the debugger).</span></span>

    <span data-ttu-id="45dfe-136">**Windows Server 2003 和 WINDOWS XP：\*\*\*\*AutoExclusionList** 子機碼無法使用;因此，您無法從自動偵測中排除任何應用程式（包括 Dwm.exe）。</span><span class="sxs-lookup"><span data-stu-id="45dfe-136">**Windows Server 2003 and Windows XP:** The **AutoExclusionList** subkey is not available; thus you cannot exclude any application, including Dwm.exe, from automatic debugging.</span></span>

<span data-ttu-id="45dfe-137">預設的 **AeDebug** 登錄專案可以如下所示：</span><span class="sxs-lookup"><span data-stu-id="45dfe-137">The default **AeDebug** registry entries can be represented as follows:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows NT
            CurrentVersion
               AeDebug
                  Auto = 1
                  AutoExclusionList
                     DWM.exe = 1
```

## <a name="related-topics"></a><span data-ttu-id="45dfe-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="45dfe-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45dfe-139">使用 WinDbg 啟用事後的調試</span><span class="sxs-lookup"><span data-stu-id="45dfe-139">Enabling Postmortem Debugging with WinDbg</span></span>](/windows-hardware/drivers/debugger/enabling-postmortem-debugging)
</dt> </dl>

 

 
