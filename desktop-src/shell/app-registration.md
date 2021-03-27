---
description: 本主題討論應用程式如何公開啟用特定案例所需的相關資訊。
ms.assetid: F88AA3E6-6F7B-442d-935A-7D2CB4958E6B
title: 應用程式註冊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 857e96893d2fe717f1a4939d06c77af043ead318
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943273"
---
# <a name="application-registration"></a><span data-ttu-id="79410-103">應用程式註冊</span><span class="sxs-lookup"><span data-stu-id="79410-103">Application Registration</span></span>

<span data-ttu-id="79410-104">本主題討論應用程式如何公開啟用特定案例所需的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="79410-104">This topic discusses how applications can expose information about themselves necessary to enable certain scenarios.</span></span> <span data-ttu-id="79410-105">這包括找出應用程式所需的資訊、應用程式支援的動詞，以及應用程式可以處理的檔案類型。</span><span class="sxs-lookup"><span data-stu-id="79410-105">This includes information needed to locate the application, the verbs that the application supports and the types of files that an application can handle.</span></span>

<span data-ttu-id="79410-106">本主題的組織方式如下：</span><span class="sxs-lookup"><span data-stu-id="79410-106">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="79410-107">尋找應用程式可執行檔</span><span class="sxs-lookup"><span data-stu-id="79410-107">Finding an Application Executable</span></span>](#finding-an-application-executable)
-   [<span data-ttu-id="79410-108">註冊應用程式</span><span class="sxs-lookup"><span data-stu-id="79410-108">Registering Applications</span></span>](#registering-applications)
    -   [<span data-ttu-id="79410-109">使用應用程式路徑子機碼</span><span class="sxs-lookup"><span data-stu-id="79410-109">Using the App Paths Subkey</span></span>](#using-the-app-paths-subkey)
    -   [<span data-ttu-id="79410-110">使用應用程式子機碼</span><span class="sxs-lookup"><span data-stu-id="79410-110">Using the Applications Subkey</span></span>](#using-the-applications-subkey)
-   [<span data-ttu-id="79410-111">註冊動詞和其他檔案關聯資訊</span><span class="sxs-lookup"><span data-stu-id="79410-111">Registering Verbs and Other File Association Information</span></span>](#registering-verbs-and-other-file-association-information)
-   [<span data-ttu-id="79410-112">註冊認知型別</span><span class="sxs-lookup"><span data-stu-id="79410-112">Registering a Perceived Type</span></span>](#registering-a-perceived-type)
-   [<span data-ttu-id="79410-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="79410-113">Related topics</span></span>](#related-topics)

> [!Note]  
> <span data-ttu-id="79410-114">您也可以在 [設定程式存取和電腦預設值] (SPAD) 中註冊應用程式，並將您的預設程式 (SYDP) 控制台應用程式。</span><span class="sxs-lookup"><span data-stu-id="79410-114">Applications can also be registered in the Set Program Access and Computer Defaults (SPAD) and Set Your Default Programs (SYDP) control panel applications.</span></span> <span data-ttu-id="79410-115">如需 SPAD 和 SYDP 應用程式註冊的相關資訊，請參閱檔案 [關聯和預設程式的指導方針](appguide-fa-defpro.md)，以及 [設定程式存取和電腦預設值 (SPAD) ](cpl-setprogramaccess.md)。</span><span class="sxs-lookup"><span data-stu-id="79410-115">For information about SPAD and SYDP application registration, see [Guidelines for File Associations and Default Programs](appguide-fa-defpro.md), and [Set Program Access and Computer Defaults (SPAD)](cpl-setprogramaccess.md).</span></span>

 

## <a name="finding-an-application-executable"></a><span data-ttu-id="79410-116">尋找應用程式可執行檔</span><span class="sxs-lookup"><span data-stu-id="79410-116">Finding an Application Executable</span></span>

<span data-ttu-id="79410-117">使用 *lpFile* 參數中的可執行檔名稱呼叫 [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa)函式時，函式會尋找檔案的數個位置。</span><span class="sxs-lookup"><span data-stu-id="79410-117">When the [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) function is called with the name of an executable file in its *lpFile* parameter, there are several places where the function looks for the file.</span></span> <span data-ttu-id="79410-118">建議您在 **應用程式路徑** 登錄子機碼中註冊您的應用程式。</span><span class="sxs-lookup"><span data-stu-id="79410-118">We recommend registering your application in the **App Paths** registry subkey.</span></span> <span data-ttu-id="79410-119">這麼做可避免應用程式需要修改系統 PATH 環境變數。</span><span class="sxs-lookup"><span data-stu-id="79410-119">Doing so avoids the need for applications to modify the system PATH environment variable.</span></span>

<span data-ttu-id="79410-120">檔案會在下列位置中尋找：</span><span class="sxs-lookup"><span data-stu-id="79410-120">The file is sought in the following locations:</span></span>

-   <span data-ttu-id="79410-121">目前的工作目錄。</span><span class="sxs-lookup"><span data-stu-id="79410-121">The current working directory.</span></span>
-   <span data-ttu-id="79410-122">只有 (不會) 搜尋任何子目錄的 **Windows** 目錄。</span><span class="sxs-lookup"><span data-stu-id="79410-122">The **Windows** directory only (no subdirectories are searched).</span></span>
-   <span data-ttu-id="79410-123">**Windows \\ System32** 目錄。</span><span class="sxs-lookup"><span data-stu-id="79410-123">The **Windows\\System32** directory.</span></span>
-   <span data-ttu-id="79410-124">PATH 環境變數中所列的目錄。</span><span class="sxs-lookup"><span data-stu-id="79410-124">Directories listed in the PATH environment variable.</span></span>
-   <span data-ttu-id="79410-125">建議： **HKEY \_ 本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **應用程式路徑**</span><span class="sxs-lookup"><span data-stu-id="79410-125">Recommended: **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**App Paths**</span></span>

## <a name="registering-applications"></a><span data-ttu-id="79410-126">註冊應用程式</span><span class="sxs-lookup"><span data-stu-id="79410-126">Registering Applications</span></span>

<span data-ttu-id="79410-127">應用程式 **路徑** 和 **應用程式** 登錄子機碼都是用來代表應用程式註冊和控制系統的行為。</span><span class="sxs-lookup"><span data-stu-id="79410-127">Both the **App Paths** and **Applications** registry subkeys are used to register and control the behavior of the system on behalf of applications.</span></span> <span data-ttu-id="79410-128">[ **應用程式路徑** ] 子機碼是慣用的位置。</span><span class="sxs-lookup"><span data-stu-id="79410-128">The **App Paths** subkey is the preferred location.</span></span>

### <a name="using-the-app-paths-subkey"></a><span data-ttu-id="79410-129">使用應用程式路徑子機碼</span><span class="sxs-lookup"><span data-stu-id="79410-129">Using the App Paths Subkey</span></span>

<span data-ttu-id="79410-130">在 Windows 7 和更新版本中，強烈建議您安裝每位使用者的應用程式，而不是每部電腦的應用程式。</span><span class="sxs-lookup"><span data-stu-id="79410-130">In Windows 7 and later, we strongly recommend you install applications per user rather than per machine.</span></span> <span data-ttu-id="79410-131">針對每位使用者安裝的應用程式，可以在 **HKEY \_ CURRENT \_ user** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **應用程式路徑** 下註冊。</span><span class="sxs-lookup"><span data-stu-id="79410-131">An application that is installed for per user can be registered under **HKEY\_CURRENT\_USER**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**App Paths**.</span></span> <span data-ttu-id="79410-132">針對電腦的所有使用者所安裝的應用程式，都可以在 **HKEY \_ 本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **應用程式路徑** 上註冊。</span><span class="sxs-lookup"><span data-stu-id="79410-132">An application that is installed for all users of the computer can be registered under **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**App Paths**.</span></span>

<span data-ttu-id="79410-133">在 **應用程式路徑** 下找到的專案主要用於下列用途：</span><span class="sxs-lookup"><span data-stu-id="79410-133">The entries found under **App Paths** are used primarily for the following purposes:</span></span>

-   <span data-ttu-id="79410-134">將應用程式的可執行檔名稱對應至該檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="79410-134">To map an application's executable file name to that file's fully qualified path.</span></span>
-   <span data-ttu-id="79410-135">在每個應用程式上，以每個進程為基礎，將資訊預先暫止至 PATH 環境變數。</span><span class="sxs-lookup"><span data-stu-id="79410-135">To pre-pend information to the PATH environment variable on a per-application, per-process basis.</span></span>

<span data-ttu-id="79410-136">如果 **應用程式路徑** 的子機碼名稱與檔案名相符，則 Shell 會執行兩個動作：</span><span class="sxs-lookup"><span data-stu-id="79410-136">If the name of a subkey of **App Paths** matches the file name, the Shell performs two actions:</span></span>

-   <span data-ttu-id="79410-137"> (預設) 專案會用來做為檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="79410-137">The (Default) entry is used as the file's fully qualified path.</span></span>
-   <span data-ttu-id="79410-138">該子機碼的路徑專案會預先暫止至該進程的 PATH 環境變數。</span><span class="sxs-lookup"><span data-stu-id="79410-138">The Path entry for that subkey is pre-pended to the PATH environment variable of that process.</span></span> <span data-ttu-id="79410-139">如果這不是必要的，則可以省略路徑值。</span><span class="sxs-lookup"><span data-stu-id="79410-139">If this is not required, the Path value can be omitted.</span></span>

<span data-ttu-id="79410-140">可能要注意的問題包括：</span><span class="sxs-lookup"><span data-stu-id="79410-140">Potential issues to be aware of include:</span></span>

-   <span data-ttu-id="79410-141">Shell 會將命令列的長度限制為最大 \_ 路徑 \* 2 個字元。</span><span class="sxs-lookup"><span data-stu-id="79410-141">The Shell limits the length of a command line to MAX\_PATH \* 2 characters.</span></span> <span data-ttu-id="79410-142">如果有許多檔案列為登錄專案或其路徑很長，則清單稍後的檔案名可能會在截斷命令列時遺失。</span><span class="sxs-lookup"><span data-stu-id="79410-142">If there are many files listed as registry entries or their paths are long, file names later in the list could be lost as the command line is truncated.</span></span>
-   <span data-ttu-id="79410-143">有些應用程式不接受命令列中的多個檔案名。</span><span class="sxs-lookup"><span data-stu-id="79410-143">Some applications do not accept multiple file names in a command line.</span></span>
-   <span data-ttu-id="79410-144">某些接受多個檔案名的應用程式無法辨識 Shell 提供這些名稱的格式。</span><span class="sxs-lookup"><span data-stu-id="79410-144">Some applications that accept multiple file names do not recognize the format in which the Shell provides them.</span></span> <span data-ttu-id="79410-145">Shell 將參數清單提供為加上引號的字串，但有些應用程式可能需要不含引號的字串。</span><span class="sxs-lookup"><span data-stu-id="79410-145">The Shell provides the parameter list as a quoted string, but some applications might require strings without quotes.</span></span>
-   <span data-ttu-id="79410-146">並非所有可拖曳的專案都是檔案系統的一部分;例如，印表機。</span><span class="sxs-lookup"><span data-stu-id="79410-146">Not all items that can be dragged are part of the file system; for example, printers.</span></span> <span data-ttu-id="79410-147">這些專案沒有標準的 Win32 路徑，所以沒有任何方法可提供有意義的 *lpParameters* 值給 [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa)。</span><span class="sxs-lookup"><span data-stu-id="79410-147">These items do not have a standard Win32 path, so there is no way to provide a meaningful *lpParameters* value to [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span></span>

<span data-ttu-id="79410-148">使用 DropTarget 專案可避免這些潛在問題，方法是提供所有剪貼簿格式的存取權，包括長檔案清單的 [CFSTR \_ SHELLIDLIST](clipboard.md) (，以及) 非檔案系統物件) 和 [CFSTR \_ FILECONTENTS](clipboard.md) (。</span><span class="sxs-lookup"><span data-stu-id="79410-148">Using the DropTarget entry avoids these potential issues by providing access to all of the clipboard formats, including [CFSTR\_SHELLIDLIST](clipboard.md) (for long file lists) and [CFSTR\_FILECONTENTS](clipboard.md) (for non-file-system objects).</span></span>

<span data-ttu-id="79410-149">**使用應用程式路徑子機碼註冊及控制應用程式的行為**：</span><span class="sxs-lookup"><span data-stu-id="79410-149">**To register and control the behavior of your applications with the App Paths subkey**:</span></span>

1.  <span data-ttu-id="79410-150">將名稱與可執行檔相同的子機碼新增至 [ **應用程式路徑** ] 子機碼，如下列登錄專案所示。</span><span class="sxs-lookup"><span data-stu-id="79410-150">Add a subkey with the same name as your executable file to the **App Paths** subkey, as shown in the following registry entry.</span></span>

    ```
    HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER
       SOFTWARE
          Microsoft
             Windows
                CurrentVersion
                   App Paths
                      file.exe
                         (Default)
                         DontUseDesktopChangeRouter
                         DropTarget
                         Path
                         UseUrl
    ```

2.  <span data-ttu-id="79410-151">請參閱下表，以取得 **應用程式路徑** 子機碼專案的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="79410-151">See the following table for details of the **App Paths** subkey entries.</span></span> 

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="79410-152">登錄項目</span><span class="sxs-lookup"><span data-stu-id="79410-152">Registry entry</span></span></th>
    <th><span data-ttu-id="79410-153">詳細資料</span><span class="sxs-lookup"><span data-stu-id="79410-153">Details</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="79410-154">(預設值)</span><span class="sxs-lookup"><span data-stu-id="79410-154">(Default)</span></span></td>
    <td><span data-ttu-id="79410-155">是應用程式的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="79410-155">Is the fully qualified path to the application.</span></span> <span data-ttu-id="79410-156">在 (預設) 專案中提供的應用程式名稱可以使用或不含 .exe 副檔名來陳述。</span><span class="sxs-lookup"><span data-stu-id="79410-156">The application name provided in the (Default) entry can be stated with or without its .exe extension.</span></span> <span data-ttu-id="79410-157">如有必要， <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a> 函式會在搜尋 <strong>應用程式路徑</strong> 子機碼時新增擴充功能。</span><span class="sxs-lookup"><span data-stu-id="79410-157">If necessary, the <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a> function adds the extension when searching <strong>App Paths</strong> subkey.</span></span> <span data-ttu-id="79410-158">專案屬於 <strong>REG_SZ</strong> 類型。</span><span class="sxs-lookup"><span data-stu-id="79410-158">The entry is of the <strong>REG_SZ</strong> type.</span></span></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="79410-159">DontUseDesktopChangeRouter</span><span class="sxs-lookup"><span data-stu-id="79410-159">DontUseDesktopChangeRouter</span></span></td>
    <td><span data-ttu-id="79410-160">偵錯工具應用程式必須有這項功能，以避免在處理 Windows 檔案總管進程時發生檔案對話方塊鎖死。</span><span class="sxs-lookup"><span data-stu-id="79410-160">Is mandatory for debugger applications to avoid file dialog deadlocks when debugging the Windows Explorer process.</span></span> <span data-ttu-id="79410-161">但是，設定 DontUseDesktopChangeRouter 專案會產生稍微不有效率的變更通知處理。</span><span class="sxs-lookup"><span data-stu-id="79410-161">Setting the DontUseDesktopChangeRouter entry produces a slightly less efficient handling of the change notifications, however.</span></span> <span data-ttu-id="79410-162">專案屬於 <strong>REG_DWORD</strong> 類型，而值為0x1。</span><span class="sxs-lookup"><span data-stu-id="79410-162">The entry is of the <strong>REG_DWORD</strong> type and the value is 0x1.</span></span></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="79410-163">DropTarget</span><span class="sxs-lookup"><span data-stu-id="79410-163">DropTarget</span></span></td>
    <td><span data-ttu-id="79410-164">是)  (CLSID 的類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="79410-164">Is a class identifier (CLSID).</span></span> <span data-ttu-id="79410-165">DropTarget 專案包含物件的 CLSID (通常是本機伺服器，而不是執行 <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"><strong>IDropTarget</strong></a>的同進程伺服器) 。</span><span class="sxs-lookup"><span data-stu-id="79410-165">The DropTarget entry contains the CLSID of an object (usually a local server rather than an in-process server) that implements <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"><strong>IDropTarget</strong></a>.</span></span> <span data-ttu-id="79410-166">根據預設，當放置目標是可執行檔，且未提供任何 DropTarget 值時，Shell 會將已卸載的檔案清單轉換成命令列參數，並透過<em>lpParameters</em>將其傳遞至<a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="79410-166">By default, when the drop target is an executable file, and no DropTarget value is provided, the Shell converts the list of dropped files into a command-line parameter and passes it to <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a> through <em>lpParameters</em>.</span></span></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="79410-167">路徑</span><span class="sxs-lookup"><span data-stu-id="79410-167">Path</span></span></td>
    <td><span data-ttu-id="79410-168">藉由呼叫 <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a>來啟動應用程式時，以分號分隔的目錄清單格式提供字串 (，) 附加至 PATH 環境變數。</span><span class="sxs-lookup"><span data-stu-id="79410-168">Supplies a string (in the form of a semicolon-separated list of directories) to append to the PATH environment variable when an application is launched by calling <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a>.</span></span> <span data-ttu-id="79410-169">它是 .exe 的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="79410-169">It is the fully qualified path to the .exe.</span></span> <span data-ttu-id="79410-170">這是 <strong>REG_SZ</strong>。</span><span class="sxs-lookup"><span data-stu-id="79410-170">It is of <strong>REG_SZ</strong>.</span></span> <span data-ttu-id="79410-171">在 <strong>Windows 7 和更新版本</strong>中，可以 <strong>REG_EXPAND_SZ</strong>類型，而且通常 <strong>REG_EXPAND_SZ</strong> % ProgramFiles%。</span><span class="sxs-lookup"><span data-stu-id="79410-171">In <strong>Windows 7 and later</strong>, the type can be <strong>REG_EXPAND_SZ</strong>, and is commonly <strong>REG_EXPAND_SZ</strong> %ProgramFiles%.</span></span>
    <blockquote>
    [!Note]<br />
<span data-ttu-id="79410-172">除了 Shell 辨識的 (預設) 、路徑和 DropTarget 專案之外，應用程式也可以將自訂值新增至其可執行檔的 <strong>應用程式路徑</strong> 子機碼。</span><span class="sxs-lookup"><span data-stu-id="79410-172">In addition to the (Default), Path, and DropTarget entries recognized by the Shell, an application can also add custom values to its executable file's <strong>App Paths</strong> subkey.</span></span> <span data-ttu-id="79410-173">我們鼓勵應用程式開發人員使用應用程式 <strong>路徑</strong> 子機碼，以提供應用程式特定路徑，而不是將新增至全域系統路徑。</span><span class="sxs-lookup"><span data-stu-id="79410-173">We encourage application developers to use the <strong>App Paths</strong> subkey to provide an application-specific path instead of making additions to the global system path.</span></span>
    </blockquote>
    <br/></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="79410-174">SupportedProtocols</span><span class="sxs-lookup"><span data-stu-id="79410-174">SupportedProtocols</span></span></td>
    <td><span data-ttu-id="79410-175">建立字串，其中包含指定之索引鍵的 URL 通訊協定配置。</span><span class="sxs-lookup"><span data-stu-id="79410-175">Creates a string that contains the URL protocol schemes for a given key.</span></span> <span data-ttu-id="79410-176">這可包含多個登錄值，以指出支援的配置。</span><span class="sxs-lookup"><span data-stu-id="79410-176">This can contain multiple registry values to indicate which schemes are supported.</span></span> <span data-ttu-id="79410-177">此字串的格式如下 <strong>scheme1： scheme2</strong>。</span><span class="sxs-lookup"><span data-stu-id="79410-177">This string follows the format of <strong>scheme1:scheme2</strong>.</span></span> <span data-ttu-id="79410-178">如果這份清單不是空的，則會將 <strong>file：</strong> 新增至字串。</span><span class="sxs-lookup"><span data-stu-id="79410-178">If this list is not empty, <strong>file:</strong> will be added to the string.</span></span> <span data-ttu-id="79410-179">定義 <em>SupportedProtocols</em> 時，會隱含地支援此通訊協定。</span><span class="sxs-lookup"><span data-stu-id="79410-179">This protocol is implicitly supported when <em>SupportedProtocols</em> is defined.</span></span> <br/></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="79410-180">UseUrl</span><span class="sxs-lookup"><span data-stu-id="79410-180">UseUrl</span></span></td>
    <td><span data-ttu-id="79410-181">指出您的應用程式可以接受 URL (而不是在命令列上) 的檔案名。</span><span class="sxs-lookup"><span data-stu-id="79410-181">Indicates that your application can accept a URL (instead of a file name) on the command line.</span></span> <span data-ttu-id="79410-182">可以直接從網際網路開啟檔的應用程式（例如網頁瀏覽器和媒體播放機）應該設定此專案。</span><span class="sxs-lookup"><span data-stu-id="79410-182">Applications that can open documents directly from the internet, like web browsers and media players, should set this entry.</span></span> <br/> <span data-ttu-id="79410-183">當 <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a> 函式啟動應用程式，且未設定 UseUrl = 1 值時， <strong>ShellExecuteEx</strong> 會將檔下載至本機檔案，並在本機複本上叫用處理程式。</span><span class="sxs-lookup"><span data-stu-id="79410-183">When the <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a> function starts an application and the UseUrl=1 value is not set, <strong>ShellExecuteEx</strong> downloads the document to a local file and invokes the handler on the local copy.</span></span><br/> <span data-ttu-id="79410-184">例如，如果應用程式具有這個專案集，且使用者以滑鼠右鍵按一下儲存在 web 伺服器上的檔案，則會提供開啟的動詞。</span><span class="sxs-lookup"><span data-stu-id="79410-184">For example, if the application has this entry set and a user right-clicks on a file stored on a web server, the Open verb will be made available.</span></span> <span data-ttu-id="79410-185">如果沒有，使用者將必須下載檔案並開啟本機複本。</span><span class="sxs-lookup"><span data-stu-id="79410-185">If not, the user will have to download the file and open the local copy.</span></span> <br/> <span data-ttu-id="79410-186">UseUrl 專案屬於 <strong>REG_DWORD</strong> 類型，而值為0x1。</span><span class="sxs-lookup"><span data-stu-id="79410-186">The UseUrl entry is of <strong>REG_DWORD</strong> type, and the value is 0x1.</span></span><br/> <span data-ttu-id="79410-187">在 Windows Vista （含）以前版本中，此專案指出當透過 ShellExecuteEx 呼叫時，應將 URL 傳遞至應用程式以及本機檔案名。</span><span class="sxs-lookup"><span data-stu-id="79410-187">In Windows Vista and earlier, this entry indicated that the URL should be passed to the application along with a local file name, when called via ShellExecuteEx.</span></span> <span data-ttu-id="79410-188">在 Windows 7 中，它表示應用程式可以瞭解任何傳遞給它的 HTTP 或 HTTPs url，也不需要提供快取檔案名稱。</span><span class="sxs-lookup"><span data-stu-id="79410-188">In Windows 7, it indicates that the application can understand any http or https url that is passed to it, without having to supply the cache file name as well.</span></span> <span data-ttu-id="79410-189">此登錄機碼與 <em>SupportedProtocols</em> 索引鍵相關聯。</span><span class="sxs-lookup"><span data-stu-id="79410-189">This registry key is associated with the <em>SupportedProtocols</em> key.</span></span><br/></td>
    </tr>
    </tbody>
    </table>

    

     

### <a name="using-the-applications-subkey"></a><span data-ttu-id="79410-190">使用應用程式子機碼</span><span class="sxs-lookup"><span data-stu-id="79410-190">Using the Applications Subkey</span></span>

<span data-ttu-id="79410-191">透過在 **HKEY \_ 類別的 \_ 根** 應用程式下包含登錄專案ApplicationName.exe子機碼 \\  \\  ，應用程式可以提供下表所示的應用程式特定資訊。</span><span class="sxs-lookup"><span data-stu-id="79410-191">Through the inclusion of registry entries under the **HKEY\_CLASSES\_ROOT**\\**Applications**\\*ApplicationName.exe* subkey, applications can provide the application-specific information shown in the following table.</span></span>



| <span data-ttu-id="79410-192">登錄項目</span><span class="sxs-lookup"><span data-stu-id="79410-192">Registry entry</span></span>                   | <span data-ttu-id="79410-193">Description</span><span class="sxs-lookup"><span data-stu-id="79410-193">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79410-194">shell \\ 動詞</span><span class="sxs-lookup"><span data-stu-id="79410-194">shell\\verb</span></span>                      | <span data-ttu-id="79410-195">提供從 OpenWith 呼叫應用程式的動詞方法。</span><span class="sxs-lookup"><span data-stu-id="79410-195">Provides the verb method for calling the application from OpenWith.</span></span> <span data-ttu-id="79410-196">如果沒有在這裡指定動詞定義，系統會假設應用程式支援 [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa)，並在命令列上傳遞檔案名。</span><span class="sxs-lookup"><span data-stu-id="79410-196">Without a verb definition specified here, the system assumes that the application supports [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa), and passes the file name on the command line.</span></span> <span data-ttu-id="79410-197">此功能適用于所有動詞方法，包括 DropTarget、ExecuteCommand 和動態資料交換 (DDE) 。</span><span class="sxs-lookup"><span data-stu-id="79410-197">This functionality applies to all the verb methods, including DropTarget, ExecuteCommand, and Dynamic Data Exchange (DDE).</span></span>                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="79410-198">DefaultIcon</span><span class="sxs-lookup"><span data-stu-id="79410-198">DefaultIcon</span></span>                      | <span data-ttu-id="79410-199">讓應用程式提供特定圖示來代表應用程式，而不是儲存在 .exe 檔案中的第一個圖示。</span><span class="sxs-lookup"><span data-stu-id="79410-199">Enables an application to provide a specific icon to represent the application instead of the first icon stored in the .exe file.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="79410-200">FriendlyAppName</span><span class="sxs-lookup"><span data-stu-id="79410-200">FriendlyAppName</span></span>                  | <span data-ttu-id="79410-201">提供一種方式，讓您取得可當地語系化的應用程式名稱，而不只是顯示的版本資訊，可能無法當地語系化。</span><span class="sxs-lookup"><span data-stu-id="79410-201">Provides a way to get a localizable name to display for an application instead of just the version information appearing, which may not be localizable.</span></span> <span data-ttu-id="79410-202">關聯查詢 [**ASSOCSTR**](/windows/desktop/api/Shlwapi/ne-shlwapi-assocstr) 會讀取這個登錄專案值，並切換回使用版本資訊中的 FileDescription 名稱。</span><span class="sxs-lookup"><span data-stu-id="79410-202">The association query [**ASSOCSTR**](/windows/desktop/api/Shlwapi/ne-shlwapi-assocstr) reads this registry entry value and falls back to use the FileDescription name in the version information.</span></span> <span data-ttu-id="79410-203">如果遺漏該名稱，關聯查詢會預設為檔案的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="79410-203">If that name is missing, the association query defaults to the display name of the file.</span></span> <span data-ttu-id="79410-204">應用程式應該使用 **ASSOCSTR \_ FRIENDLYAPPNAME** 來取得此資訊，以取得正確的行為。</span><span class="sxs-lookup"><span data-stu-id="79410-204">Applications should use **ASSOCSTR\_FRIENDLYAPPNAME** to retrieve this information to obtain the proper behavior.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="79410-205">SupportedTypes</span><span class="sxs-lookup"><span data-stu-id="79410-205">SupportedTypes</span></span>                   | <span data-ttu-id="79410-206">列出應用程式所支援的檔案類型。</span><span class="sxs-lookup"><span data-stu-id="79410-206">Lists the file types that the application supports.</span></span> <span data-ttu-id="79410-207">這樣做可讓應用程式列在 [ **開啟檔案** ] 對話方塊的 [cascade] 功能表中。</span><span class="sxs-lookup"><span data-stu-id="79410-207">Doing so enables the application to be listed in the cascade menu of the **Open with** dialog box.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="79410-208">NoOpenWith</span><span class="sxs-lookup"><span data-stu-id="79410-208">NoOpenWith</span></span>                       | <span data-ttu-id="79410-209">指出未指定任何應用程式來開啟此檔案類型。</span><span class="sxs-lookup"><span data-stu-id="79410-209">Indicates that no application is specified for opening this file type.</span></span> <span data-ttu-id="79410-210">請注意，如果已依檔案類型設定應用程式的 OpenWithProgIDs 子機碼，而且 ProgID 子機碼本身也沒有 NoOpenWith 專案，則該應用程式將會出現在建議或可用的應用程式清單中，即使已指定 NoOpenWith 專案也一樣。</span><span class="sxs-lookup"><span data-stu-id="79410-210">Be aware that if an OpenWithProgIDs subkey has been set for an application by file type, and the ProgID subkey itself does not also have a NoOpenWith entry, that application will appear in the list of recommended or available applications even if it has specified the NoOpenWith entry.</span></span> <span data-ttu-id="79410-211">如需詳細資訊，請參閱如何 [在 [開啟方式] 對話方塊中加入應用程式](how-to-include-an-application-on-the-open-with-dialog-box.md) ，以及 [如何從 [開啟檔案] 對話方塊中排除應用程式](how-to-exclude-an-application-from-the-open-with-dialog-box-for-unassociated-file-types.md)。</span><span class="sxs-lookup"><span data-stu-id="79410-211">For more information, see [How to How to Include an Application in the Open With Dialog Box](how-to-include-an-application-on-the-open-with-dialog-box.md) and [How to exclude an Application from the Open with Dialog Box](how-to-exclude-an-application-from-the-open-with-dialog-box-for-unassociated-file-types.md).</span></span><br/> |
| <span data-ttu-id="79410-212">IsHostApp</span><span class="sxs-lookup"><span data-stu-id="79410-212">IsHostApp</span></span>                        | <span data-ttu-id="79410-213">指出程式是一種主機進程，例如 Rundll32.exe 或 Dllhost.exe，而且不應該被視為 [ **開始** ] 功能表釘選，或包含在最常使用的 (MFU) 清單中。</span><span class="sxs-lookup"><span data-stu-id="79410-213">Indicates that the process is a host process, such as Rundll32.exe or Dllhost.exe, and should not be considered for **Start** menu pinning or inclusion in the Most Frequently Used (MFU) list.</span></span> <span data-ttu-id="79410-214">當使用包含非 null 引數清單的快捷方式啟動，或 [ (AppUserModelIDs) 的明確應用程式使用者模型識別碼 ](appids.md)啟動時，可以將該程式釘選 () 的快捷方式。</span><span class="sxs-lookup"><span data-stu-id="79410-214">When launched with a shortcut that contains a non-null argument list or an explicit [Application User Model IDs (AppUserModelIDs)](appids.md), the process can be pinned (as that shortcut).</span></span> <span data-ttu-id="79410-215">這類快速鍵是要包含在 最常使用清單中的候選項目。</span><span class="sxs-lookup"><span data-stu-id="79410-215">Such shortcuts are candidates for inclusion in the MFU list.</span></span>                                                                                                                                                                                                                                                  |
| <span data-ttu-id="79410-216">NoStartPage</span><span class="sxs-lookup"><span data-stu-id="79410-216">NoStartPage</span></span>                      | <span data-ttu-id="79410-217">指出應該從 [ **開始** ] 功能表排除應用程式可執行檔和快捷方式，並將其釘選或包含在 最常使用清單中。</span><span class="sxs-lookup"><span data-stu-id="79410-217">Indicates that the application executable and shortcuts should be excluded from the **Start** menu and from pinning or inclusion in the MFU list.</span></span> <span data-ttu-id="79410-218">此專案通常用來排除系統工具、安裝程式和 uninstallers，以及讀我檔案。</span><span class="sxs-lookup"><span data-stu-id="79410-218">This entry is typically used to exclude system tools, installers and uninstallers, and readme files.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="79410-219">UseExecutableForTaskbarGroupIcon</span><span class="sxs-lookup"><span data-stu-id="79410-219">UseExecutableForTaskbarGroupIcon</span></span> | <span data-ttu-id="79410-220">如果沒有此應用程式的可釘選快捷方式，而不是第一次遇到的視窗圖示，則會讓工作列使用這個可執行檔的預設圖示。</span><span class="sxs-lookup"><span data-stu-id="79410-220">Causes the taskbar to use the default icon of this executable if there is no pinnable shortcut for this application, and instead of the icon of the window that was first encountered.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="79410-221">TaskbarGroupIcon</span><span class="sxs-lookup"><span data-stu-id="79410-221">TaskbarGroupIcon</span></span>                 | <span data-ttu-id="79410-222">指定用來覆寫工作列圖示的圖示。</span><span class="sxs-lookup"><span data-stu-id="79410-222">Specifies the icon used to override the taskbar icon.</span></span> <span data-ttu-id="79410-223">視窗圖示通常用於工作列。</span><span class="sxs-lookup"><span data-stu-id="79410-223">The window icon is normally used for the taskbar.</span></span> <span data-ttu-id="79410-224">設定 TaskbarGroupIcon 專案會導致系統改為使用來自應用程式 .exe 的圖示。</span><span class="sxs-lookup"><span data-stu-id="79410-224">Setting the TaskbarGroupIcon entry causes the system to use the icon from the .exe for the application instead.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

### <a name="examples"></a><span data-ttu-id="79410-225">範例</span><span class="sxs-lookup"><span data-stu-id="79410-225">Examples</span></span>

<span data-ttu-id="79410-226">透過 **HKEY \_ 類別 \_ 根** \\ **應用程式** \\ *ApplicationName.exe* 子機碼的一些應用程式註冊範例如下所示。</span><span class="sxs-lookup"><span data-stu-id="79410-226">Some examples of application registrations through the **HKEY\_CLASSES\_ROOT**\\**Applications**\\*ApplicationName.exe* subkey are as follows.</span></span> <span data-ttu-id="79410-227">所有登錄專案值都是 **reg \_ sz** 型別，但 **DefaultIcon** 是 **reg \_ EXPAND \_ sz** 型別。</span><span class="sxs-lookup"><span data-stu-id="79410-227">All registry entry values are of **REG\_SZ** type, with the exception of **DefaultIcon** which is of **REG\_EXPAND\_SZ** type.</span></span>

```
HKEY_CLASSES_ROOT
   Applications
      wordpad.exe
         FriendlyAppName = @%SystemRoot%\System32\shell32.dll,-22069
```

```
HKEY_CLASSES_ROOT
   Applications
      wmplayer.exe
         SupportedTypes
            .3gp2
```

```
HKEY_CLASSES_ROOT
   Applications
      wmplayer.exe
         DefaultIcon
            (Default) = %SystemRoot%\system32\wmploc.dll,-730
```

```
HKEY_CLASSES_ROOT
   Applications
      WScript.exe
         NoOpenWith
```

```
HKEY_CLASSES_ROOT
   Applications
      photoviewer.dll
         shell
            open
               DropTarget
                  Clsid = {FFE2A43C-56B9-4bf5-9A79-CC6D4285608A}
```

```
HKEY_CLASSES_ROOT
   Applications
      mspaint.exe
         SupportedTypes
            .bmp
            .dib
            .rle
            .jpg
            .jpeg
            .jpe
            .jfif
            .gif
            .emf
            .wmf
            .tif
            .tiff
            .png
            .ico
```

## <a name="registering-verbs-and-other-file-association-information"></a><span data-ttu-id="79410-228">註冊動詞和其他檔案關聯資訊</span><span class="sxs-lookup"><span data-stu-id="79410-228">Registering Verbs and Other File Association Information</span></span>

<span data-ttu-id="79410-229">在 **HKEY \_ 類別 \_ 根** SystemFileAssociations 下註冊的子機碼， \\ 可讓 Shell 定義檔案類型之屬性的預設行為，並啟用共用檔案關聯。</span><span class="sxs-lookup"><span data-stu-id="79410-229">Subkeys registered under **HKEY\_CLASSES\_ROOT**\\**SystemFileAssociations** enable the Shell to define the default behavior of attributes for file types and enable shared file associations.</span></span> <span data-ttu-id="79410-230">當使用者變更檔案類型的預設應用程式時，新的預設應用程式的 ProgID 具有提供動詞和其他關聯資訊的優先順序。</span><span class="sxs-lookup"><span data-stu-id="79410-230">When users change the default application for a file type, the ProgID of the new default application has priority in providing verbs and other association information.</span></span> <span data-ttu-id="79410-231">此優先順序是因為它是關聯陣列中的第一個專案。</span><span class="sxs-lookup"><span data-stu-id="79410-231">This priority is due to it being the first entry in the association array.</span></span> <span data-ttu-id="79410-232">如果預設程式已變更，則無法再使用先前 ProgID 下的資訊。</span><span class="sxs-lookup"><span data-stu-id="79410-232">If the default program is changed, the information under the previous ProgID is no longer available.</span></span>

<span data-ttu-id="79410-233">若要主動處理變更為預設程式的結果，您可以使用 **HKEY \_ 類別 \_ 根** \\ **SystemFileAssociations** 來註冊動詞和其他關聯資訊。</span><span class="sxs-lookup"><span data-stu-id="79410-233">To deal proactively with the consequences of a change to default programs, you can use **HKEY\_CLASSES\_ROOT**\\**SystemFileAssociations** to register verbs and other association information.</span></span> <span data-ttu-id="79410-234">因為它們在關聯陣列中的 ProgID 之後的位置，所以這些註冊的優先順序較低。</span><span class="sxs-lookup"><span data-stu-id="79410-234">Due to their location after the ProgID in the association array, these registrations are lower priority.</span></span> <span data-ttu-id="79410-235">即使使用者變更預設程式，並提供位置來註冊將永遠可供特定檔案類型使用的次要動詞命令，這些 SystemFileAssociationsregistrations 仍是穩定的。</span><span class="sxs-lookup"><span data-stu-id="79410-235">These SystemFileAssociationsregistrations are stable even when users change the default programs, and provide a location to register secondary verbs that will always be available for a particular file type.</span></span> <span data-ttu-id="79410-236">如需登錄範例，請參閱本主題稍後的 [註冊認知型](#registering-a-perceived-type) 別。</span><span class="sxs-lookup"><span data-stu-id="79410-236">For a registry example, see [Registering a Perceived Type](#registering-a-perceived-type) later in this topic.</span></span>

<span data-ttu-id="79410-237">下列登錄範例顯示當使用者在主控台中執行 **預設程式** 專案時所發生的情況，以將 mp3 檔的預設值變更為 App2ProgID。</span><span class="sxs-lookup"><span data-stu-id="79410-237">The following registry example shows what happens when the user runs the **Default Programs** item in Control Panel to change the default for .mp3 files to App2ProgID.</span></span> <span data-ttu-id="79410-238">變更預設值之後，Verb1 就無法再使用，Verb2 會成為預設值。</span><span class="sxs-lookup"><span data-stu-id="79410-238">After changing the default, Verb1 is no longer available, and Verb2 becomes the default.</span></span>

```
HKEY_CLASSES_ROOT
   .mp3
      (Default) = App1ProgID
```

```
HKEY_CLASSES_ROOT
   App1ProgID
      shell
         Verb1
```

```
HKEY_CLASSES_ROOT
   App2ProgID
      shell
         Verb2
```

## <a name="registering-a-perceived-type"></a><span data-ttu-id="79410-239">註冊認知型別</span><span class="sxs-lookup"><span data-stu-id="79410-239">Registering a Perceived Type</span></span>

<span data-ttu-id="79410-240">已知類型的登錄值會定義為 **HKEY \_ 類別 \_ 根** SystemFileAssociations 登錄子機碼的子機碼 \\  。</span><span class="sxs-lookup"><span data-stu-id="79410-240">Registry values for perceived types are defined as subkeys of the **HKEY\_CLASSES\_ROOT**\\**SystemFileAssociations** registry subkey.</span></span> <span data-ttu-id="79410-241">例如，認知的型別 **文字** 會註冊如下：</span><span class="sxs-lookup"><span data-stu-id="79410-241">For example, the perceived type **text** is registered as follows:</span></span>

```
HKEY_CLASSES_ROOT
   SystemFileAssociations
      text
         shell
            edit
               command
                  (Default) = "%SystemRoot%\system32\NOTEPAD.EXE" "%1"
            open
               command
                  (Default) = "%SystemRoot%\system32\NOTEPAD.EXE" "%1"
```

<span data-ttu-id="79410-242">在檔案類型的子機碼中包含 PerceivedType 值，即表示檔案類型的可感知類型。</span><span class="sxs-lookup"><span data-stu-id="79410-242">A file type's perceived type is indicated by including a PerceivedType value in the file type's subkey.</span></span> <span data-ttu-id="79410-243">PerceivedType 值會設定為在 **HKEY \_ 類別 \_ 根** SystemFileAssociations 登錄子機碼下註冊的認知型別名稱 \\  ，如先前的登錄範例所示。</span><span class="sxs-lookup"><span data-stu-id="79410-243">The PerceivedType value is set to the name of the perceived type registered under **HKEY\_CLASSES\_ROOT**\\**SystemFileAssociations** registry subkey, as shown in the previous registry example.</span></span> <span data-ttu-id="79410-244">例如，若要將 .cpp 檔案宣告為「文字」類型，請新增下列登錄專案：</span><span class="sxs-lookup"><span data-stu-id="79410-244">To declare .cpp files as being of perceived type "text", for example, add the following registry entry:</span></span>

```
HKEY_CLASSES_ROOT
   .cpp
      PerceivedType = text
```

## <a name="related-topics"></a><span data-ttu-id="79410-245">相關主題</span><span class="sxs-lookup"><span data-stu-id="79410-245">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79410-246">檔案類型</span><span class="sxs-lookup"><span data-stu-id="79410-246">File Types</span></span>](fa-file-types.md)
</dt> <dt>

[<span data-ttu-id="79410-247">檔案關聯的運作方式</span><span class="sxs-lookup"><span data-stu-id="79410-247">How File Associations Work</span></span>](fa-how-work.md)
</dt> <dt>

[<span data-ttu-id="79410-248">依檔案類型或種類的內容視圖</span><span class="sxs-lookup"><span data-stu-id="79410-248">Content View By File Type or Kind</span></span>](prophand-content-view.md)
</dt> <dt>

[<span data-ttu-id="79410-249">檔案類型驗證器</span><span class="sxs-lookup"><span data-stu-id="79410-249">File Type Verifier</span></span>](file-type-verifier.md)
</dt> <dt>

[<span data-ttu-id="79410-250">檔案類型處理常式</span><span class="sxs-lookup"><span data-stu-id="79410-250">File Type Handlers</span></span>](fa-file-extensions.md)
</dt> <dt>

[<span data-ttu-id="79410-251">程式設計識別碼</span><span class="sxs-lookup"><span data-stu-id="79410-251">Programmatic Identifiers</span></span>](fa-progids.md)
</dt> <dt>

[<span data-ttu-id="79410-252">認知類型</span><span class="sxs-lookup"><span data-stu-id="79410-252">Perceived Types</span></span>](fa-perceivedtypes.md)
</dt> <dt>

[<span data-ttu-id="79410-253">關聯陣列</span><span class="sxs-lookup"><span data-stu-id="79410-253">Association Arrays</span></span>](fa-associationarray.md)
</dt> </dl>

