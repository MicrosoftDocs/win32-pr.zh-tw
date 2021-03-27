---
description: 本主題說明如何 debug Shell 和命名空間延伸 Dll。
title: 使用 Shell 進行偵錯工具
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2fcaf633-9a6d-4fda-a690-28445b10a6d6
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 3ca6e30809565408454976e1b07ff37dcc8f8f8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511055"
---
# <a name="debugging-with-the-shell"></a><span data-ttu-id="9d5db-103">使用 Shell 進行偵錯工具</span><span class="sxs-lookup"><span data-stu-id="9d5db-103">Debugging with the Shell</span></span>

<span data-ttu-id="9d5db-104">本主題說明如何 debug Shell 和命名空間延伸 Dll。</span><span class="sxs-lookup"><span data-stu-id="9d5db-104">This topic explains how to debug Shell and namespace extension DLLs.</span></span>

-   [<span data-ttu-id="9d5db-105">在偵錯工具下執行 Shell</span><span class="sxs-lookup"><span data-stu-id="9d5db-105">Running the Shell Under a Debugger</span></span>](#running-the-shell-under-a-debugger)
-   [<span data-ttu-id="9d5db-106">執行和測試 Shell 擴充功能</span><span class="sxs-lookup"><span data-stu-id="9d5db-106">Running and Testing Shell Extensions</span></span>](#running-and-testing-shell-extensions)
-   [<span data-ttu-id="9d5db-107">卸載 DLL</span><span class="sxs-lookup"><span data-stu-id="9d5db-107">Unloading the DLL</span></span>](#unloading-the-dll)

## <a name="running-the-shell-under-a-debugger"></a><span data-ttu-id="9d5db-108">在偵錯工具下執行 Shell</span><span class="sxs-lookup"><span data-stu-id="9d5db-108">Running the Shell Under a Debugger</span></span>

<span data-ttu-id="9d5db-109">若要對您的延伸模組進行偵錯工具，您需要從偵錯工具執行 Shell。</span><span class="sxs-lookup"><span data-stu-id="9d5db-109">To debug your extension, you need to run the Shell from the debugger.</span></span> <span data-ttu-id="9d5db-110">請遵循下列步驟：</span><span class="sxs-lookup"><span data-stu-id="9d5db-110">Follow these steps:</span></span>

1.  <span data-ttu-id="9d5db-111">將延伸模組的專案載入偵錯工具，但不要執行。</span><span class="sxs-lookup"><span data-stu-id="9d5db-111">Load the extension's project into the debugger, but do not run it.</span></span>
2.  <span data-ttu-id="9d5db-112">關閉 Shell。</span><span class="sxs-lookup"><span data-stu-id="9d5db-112">Shut down the Shell.</span></span>

    -   <span data-ttu-id="9d5db-113">針對 Windows Vista 和更新版本：</span><span class="sxs-lookup"><span data-stu-id="9d5db-113">For Windows Vista and later:</span></span>
        1.  <span data-ttu-id="9d5db-114">顯示 [ **開始** ] 功能表。</span><span class="sxs-lookup"><span data-stu-id="9d5db-114">Display the **Start** menu.</span></span>
        2.  <span data-ttu-id="9d5db-115">按 CTRL + SHIFT 鍵，然後以滑鼠右鍵按一下 [ **開始** ] 功能表右邊一半的背景。</span><span class="sxs-lookup"><span data-stu-id="9d5db-115">Press CTRL+SHIFT and right-click on the background of the right half of the **Start** menu.</span></span>
        3.  <span data-ttu-id="9d5db-116">從出現的功能表中選擇 [ **Exit Explorer**]。</span><span class="sxs-lookup"><span data-stu-id="9d5db-116">From the menu that appears, choose **Exit Explorer**.</span></span>
    -   <span data-ttu-id="9d5db-117">若為 Windows XP：</span><span class="sxs-lookup"><span data-stu-id="9d5db-117">For Windows XP:</span></span>
        1.  <span data-ttu-id="9d5db-118">在 [ **開始** ] 功能表中，選擇 [ **關機**]。</span><span class="sxs-lookup"><span data-stu-id="9d5db-118">From the **Start** menu, choose **Shut down**.</span></span>
        2.  <span data-ttu-id="9d5db-119">按 CTRL + ALT + SHIFT 鍵，然後按一下 [**關機 Windows** ] 對話方塊中的 [**否**]。</span><span class="sxs-lookup"><span data-stu-id="9d5db-119">Press CTRL+ALT+SHIFT, and click **No** in the **Shut Down Windows** dialog box.</span></span>

    <span data-ttu-id="9d5db-120">Shell 現在已關閉，但其他所有應用程式仍在執行，包括偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="9d5db-120">The Shell is now shut down, but all other applications are still running, including the debugger.</span></span>

3.  <span data-ttu-id="9d5db-121">將偵錯工具設定為使用 **Windows** 目錄中的 Explorer.exe 來執行擴充 DLL。</span><span class="sxs-lookup"><span data-stu-id="9d5db-121">Set the debugger to run the extension DLL with Explorer.exe from the **Windows** directory.</span></span>
4.  <span data-ttu-id="9d5db-122">從偵錯工具執行專案。</span><span class="sxs-lookup"><span data-stu-id="9d5db-122">Run the project from the debugger.</span></span> <span data-ttu-id="9d5db-123">Shell 會如往常般啟動，但偵錯工具會附加至 Shell 的進程。</span><span class="sxs-lookup"><span data-stu-id="9d5db-123">The Shell will launch as usual, but the debugger will be attached to the Shell's process.</span></span>

## <a name="running-and-testing-shell-extensions"></a><span data-ttu-id="9d5db-124">執行和測試 Shell 擴充功能</span><span class="sxs-lookup"><span data-stu-id="9d5db-124">Running and Testing Shell Extensions</span></span>

<span data-ttu-id="9d5db-125">您可以在個別的 Windows 檔案總管流程中執行和測試擴充功能，以避免停止和重新開機桌面和工作列。</span><span class="sxs-lookup"><span data-stu-id="9d5db-125">You can run and test your extensions in a separate Windows Explorer process to avoid stopping and restarting the desktop and taskbar.</span></span> <span data-ttu-id="9d5db-126">當您執行和測試擴充功能時，仍然可以使用您的桌面和工作列。</span><span class="sxs-lookup"><span data-stu-id="9d5db-126">Your desktop and taskbar can still be used while you run and test the extensions.</span></span>

<span data-ttu-id="9d5db-127">若要啟用這項功能，請將下列 REG \_ DWORD 專案新增至登錄。</span><span class="sxs-lookup"><span data-stu-id="9d5db-127">To enable this feature, add the following REG\_DWORD entry to the registry.</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  DesktopProcess = 1
```

<span data-ttu-id="9d5db-128">您必須登出再重新登入，此專案才會生效。</span><span class="sxs-lookup"><span data-stu-id="9d5db-128">For this entry to take effect, you must log off and log on again.</span></span> <span data-ttu-id="9d5db-129">這項設定會使桌面和工作列視窗在一個 Explorer.exe 進程中建立，而其他所有的 Explorer 和資料夾視窗則會在不同的 Explorer.exe 進程中開啟。</span><span class="sxs-lookup"><span data-stu-id="9d5db-129">This setting causes the desktop and taskbar windows to be created in one Explorer.exe process and all other Explorer and folder windows to be opened in a different Explorer.exe process.</span></span>

<span data-ttu-id="9d5db-130">除了讓擴充功能的執行和測試更方便，此設定也會讓桌面更健全，因為它與 Shell 擴充功能有關。</span><span class="sxs-lookup"><span data-stu-id="9d5db-130">In addition to making the running and testing of your extensions more convenient, this setting also makes the desktop more robust as it relates to Shell extensions.</span></span> <span data-ttu-id="9d5db-131">許多這類的擴充功能 (快捷方式功能表延伸模組，例如) 將載入 nondesktop Explorer.exe 進程中。</span><span class="sxs-lookup"><span data-stu-id="9d5db-131">Many such extensions (shortcut menu extensions, for example) will be loaded into the nondesktop Explorer.exe process.</span></span> <span data-ttu-id="9d5db-132">如果此進程終止，則桌面和工作列不會受到影響，而且下一個 [Explorer] 或 [資料夾] 視窗將會重新建立終止的進程。</span><span class="sxs-lookup"><span data-stu-id="9d5db-132">If this process terminates, the desktop and taskbar will be unaffected, and the next Explorer or folder window will re-create the terminated process.</span></span>

## <a name="unloading-the-dll"></a><span data-ttu-id="9d5db-133">卸載 DLL</span><span class="sxs-lookup"><span data-stu-id="9d5db-133">Unloading the DLL</span></span>

<span data-ttu-id="9d5db-134">Shell 會在其使用計數為零時自動卸載任何 DLL，但只有在 DLL 未使用一段時間之後。</span><span class="sxs-lookup"><span data-stu-id="9d5db-134">The Shell automatically unloads any DLL when its usage count is zero, but only after the DLL has not been used for a period of time.</span></span> <span data-ttu-id="9d5db-135">這種非使用中的期間可能會很長，尤其是在調試 Shell 擴充 DLL 時。</span><span class="sxs-lookup"><span data-stu-id="9d5db-135">This inactive period might be unacceptably long at times, especially when a Shell extension DLL is being debugged.</span></span> <span data-ttu-id="9d5db-136">您可以藉由將下列資訊新增到登錄中，縮短非使用期間。</span><span class="sxs-lookup"><span data-stu-id="9d5db-136">You can shorten the inactive period by adding the following information to the registry.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AlwaysUnloadDll
```

 

 



