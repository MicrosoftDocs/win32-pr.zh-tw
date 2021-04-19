---
description: 在指定的檔案上執行操作。
ms.assetid: ce652565-40b6-4f69-bd2a-9e05e3f360ac
title: WOWShellExecute 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WOWShellExecute
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: ae50ad570211303cdfb7aa8e86908593ab48537d
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/02/2021
ms.locfileid: "106984496"
---
# <a name="wowshellexecute-function"></a><span data-ttu-id="a6ad1-103">WOWShellExecute 函式</span><span class="sxs-lookup"><span data-stu-id="a6ad1-103">WOWShellExecute function</span></span>

<span data-ttu-id="a6ad1-104">\[您可以透過 Windows XP Service Pack 2 (SP2) 和 Windows Server 2003 來取得此函式。</span><span class="sxs-lookup"><span data-stu-id="a6ad1-104">\[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="a6ad1-105">它可能會在後續版本的 Windows 中改變或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="a6ad1-105">It might be altered or unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="a6ad1-106">在指定的檔案上執行操作。</span><span class="sxs-lookup"><span data-stu-id="a6ad1-106">Performs an operation on a specified file.</span></span> <span data-ttu-id="a6ad1-107">**WOWShellExecute** 僅適用于 Microsoft WINDOWS NT 虛擬 DOS 機器 (Ntvdm.exe) ，可讓磁片作業系統 (DOS) 和16位軟體在 Windows 系統上執行，而且不應該由其他人使用。</span><span class="sxs-lookup"><span data-stu-id="a6ad1-107">**WOWShellExecute** exists only for use with the Microsoft Windows NT Virtual DOS Machine (Ntvdm.exe), which allows disk operating system (DOS) and 16-bit software to run on a Windows system, and should not be used by anyone else.</span></span> <span data-ttu-id="a6ad1-108">請改用 [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) 。</span><span class="sxs-lookup"><span data-stu-id="a6ad1-108">Use [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6ad1-109">語法</span><span class="sxs-lookup"><span data-stu-id="a6ad1-109">Syntax</span></span>


```C++
HINSTANCE WOWShellExecute(
  _In_ HWND    hwnd,
  _In_ LPCTSTR lpOperation,
  _In_ LPCTSTR lpFile,
  _In_ LPCTSTR lpParameters,
  _In_ LPCTSTR lpDirectory,
  _In_ INT     nShowCmd,
       void    *lpfnCBWinExec
);
```



## <a name="parameters"></a><span data-ttu-id="a6ad1-110">參數</span><span class="sxs-lookup"><span data-stu-id="a6ad1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6ad1-111">*hwnd* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a6ad1-111">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6ad1-112">類型： **HWND**</span><span class="sxs-lookup"><span data-stu-id="a6ad1-112">Type: **HWND**</span></span>

<span data-ttu-id="a6ad1-113">主控視窗的控制碼，用來顯示 UI 或錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="a6ad1-113">A handle to the owner window used for displaying a UI or error messages.</span></span> <span data-ttu-id="a6ad1-114">如果作業未與視窗相關聯，此值可以是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="a6ad1-114">This value can be **NULL** if the operation is not associated with a window.</span></span>

</dd> <dt>

<span data-ttu-id="a6ad1-115">*lpOperation* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a6ad1-115">*lpOperation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6ad1-116">類型： **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="a6ad1-116">Type: **LPCTSTR**</span></span>

<span data-ttu-id="a6ad1-117">以 **null** 結束的字串指標，在此案例中稱為 *動詞*，可指定要執行的動作。</span><span class="sxs-lookup"><span data-stu-id="a6ad1-117">A pointer to a **null**-terminated string, referred to in this case as a *verb*, that specifies the action to be performed.</span></span> <span data-ttu-id="a6ad1-118">可用的動詞集合取決於特定的檔案或資料夾。</span><span class="sxs-lookup"><span data-stu-id="a6ad1-118">The set of available verbs depends on the particular file or folder.</span></span> <span data-ttu-id="a6ad1-119">一般而言，可從物件的快捷方式功能表取得的動作是可用的動詞命令。</span><span class="sxs-lookup"><span data-stu-id="a6ad1-119">Generally, the actions available from an object's shortcut menu are available verbs.</span></span> <span data-ttu-id="a6ad1-120">如需動詞和其可用性的詳細資訊，請參閱 [啟動應用程式](launch.md)的 *物件動詞* 一節。</span><span class="sxs-lookup"><span data-stu-id="a6ad1-120">For more information about verbs and their availability, see the *Object Verbs* section of [Launching Applications](launch.md).</span></span> <span data-ttu-id="a6ad1-121">如需快捷方式功能表的進一步討論，請參閱 [擴充快捷方式功能表](context.md) 。</span><span class="sxs-lookup"><span data-stu-id="a6ad1-121">See [Extending Shortcut Menus](context.md) for further discussion of shortcut menus.</span></span> <span data-ttu-id="a6ad1-122">通常會使用下列動詞。</span><span class="sxs-lookup"><span data-stu-id="a6ad1-122">The following verbs are commonly used.</span></span>

<dt>

<span id="edit"></span><span id="EDIT"></span>

<span data-ttu-id="a6ad1-123"><span id="edit"></span><span id="EDIT"></span>**編輯**</span><span class="sxs-lookup"><span data-stu-id="a6ad1-123"><span id="edit"></span><span id="EDIT"></span>**edit**</span></span>


</dt> <dd>

<span data-ttu-id="a6ad1-124">啟動編輯器並開啟要編輯的檔。</span><span class="sxs-lookup"><span data-stu-id="a6ad1-124">Launches an editor and opens the document for editing.</span></span> <span data-ttu-id="a6ad1-125">如果 *lpFile* 不是檔檔，則函式會失敗。</span><span class="sxs-lookup"><span data-stu-id="a6ad1-125">If *lpFile* is not a document file, the function will fail.</span></span>

</dd> <dt>

<span id="explore"></span><span id="EXPLORE"></span>

<span data-ttu-id="a6ad1-126"><span id="explore"></span><span id="EXPLORE"></span>**探討**</span><span class="sxs-lookup"><span data-stu-id="a6ad1-126"><span id="explore"></span><span id="EXPLORE"></span>**explore**</span></span>


</dt> <dd>

<span data-ttu-id="a6ad1-127">探索 *lpFile* 所指定的資料夾。</span><span class="sxs-lookup"><span data-stu-id="a6ad1-127">Explores the folder specified by *lpFile*.</span></span>

</dd> <dt>

<span id="find"></span><span id="FIND"></span>

<span data-ttu-id="a6ad1-128"><span id="find"></span><span id="FIND"></span>**找到**</span><span class="sxs-lookup"><span data-stu-id="a6ad1-128"><span id="find"></span><span id="FIND"></span>**find**</span></span>


</dt> <dd>

<span data-ttu-id="a6ad1-129">從指定的目錄起始搜尋。</span><span class="sxs-lookup"><span data-stu-id="a6ad1-129">Initiates a search starting from the specified directory.</span></span>

</dd> <dt>

<span id="open"></span><span id="OPEN"></span>

<span data-ttu-id="a6ad1-130"><span id="open"></span><span id="OPEN"></span>**打開**</span><span class="sxs-lookup"><span data-stu-id="a6ad1-130"><span id="open"></span><span id="OPEN"></span>**open**</span></span>


</dt> <dd>

<span data-ttu-id="a6ad1-131">開啟 *lpFile* 參數所指定的檔案。</span><span class="sxs-lookup"><span data-stu-id="a6ad1-131">Opens the file specified by the *lpFile* parameter.</span></span> <span data-ttu-id="a6ad1-132">檔案可以是可執行檔、檔檔案或資料夾。</span><span class="sxs-lookup"><span data-stu-id="a6ad1-132">The file can be an executable file, a document file, or a folder.</span></span>

</dd> <dt>

<span id="print"></span><span id="PRINT"></span>

<span data-ttu-id="a6ad1-133"><span id="print"></span><span id="PRINT"></span>**列印**</span><span class="sxs-lookup"><span data-stu-id="a6ad1-133"><span id="print"></span><span id="PRINT"></span>**print**</span></span>


</dt> <dd>

<span data-ttu-id="a6ad1-134">列印 *lpFile* 所指定的檔檔案。</span><span class="sxs-lookup"><span data-stu-id="a6ad1-134">Prints the document file specified by *lpFile*.</span></span> <span data-ttu-id="a6ad1-135">如果 *lpFile* 不是檔檔，則函式會失敗。</span><span class="sxs-lookup"><span data-stu-id="a6ad1-135">If *lpFile* is not a document file, the function will fail.</span></span>

</dd> <dt>

<span id="NULL"></span><span id="null"></span>

<span data-ttu-id="a6ad1-136"><span id="NULL"></span><span id="null"></span>**空**</span><span class="sxs-lookup"><span data-stu-id="a6ad1-136"><span id="NULL"></span><span id="null"></span>**NULL**</span></span>


</dt> <dd>

<span data-ttu-id="a6ad1-137">若為 Windows 2000 之前的系統，則會使用預設動詞（如果它是有效且可在登錄中使用）。</span><span class="sxs-lookup"><span data-stu-id="a6ad1-137">For systems prior to Windows 2000, the default verb is used if it is valid and available in the registry.</span></span> <span data-ttu-id="a6ad1-138">如果沒有，則會使用 "open" 動詞。</span><span class="sxs-lookup"><span data-stu-id="a6ad1-138">If not, the "open" verb is used.</span></span>

<span data-ttu-id="a6ad1-139">若為 Windows 2000 和更新版本的系統，則會使用預設動詞（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="a6ad1-139">For Windows 2000 and later systems, the default verb is used if available.</span></span> <span data-ttu-id="a6ad1-140">如果沒有，則會使用 "open" 動詞。</span><span class="sxs-lookup"><span data-stu-id="a6ad1-140">If not, the "open" verb is used.</span></span> <span data-ttu-id="a6ad1-141">如果沒有可用的動詞命令，系統會使用登錄中列出的第一個動詞。</span><span class="sxs-lookup"><span data-stu-id="a6ad1-141">If neither verb is available, the system uses the first verb listed in the registry.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="a6ad1-142">*lpFile* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a6ad1-142">*lpFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6ad1-143">類型： **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="a6ad1-143">Type: **LPCTSTR**</span></span>

<span data-ttu-id="a6ad1-144">以 **null** 結束的字串指標，指定要在其上執行指定動詞命令的檔案或物件。</span><span class="sxs-lookup"><span data-stu-id="a6ad1-144">A pointer to a **null**-terminated string that specifies the file or object on which to execute the specified verb.</span></span> <span data-ttu-id="a6ad1-145">若要指定 Shell 命名空間物件，請傳遞完整的剖析名稱。</span><span class="sxs-lookup"><span data-stu-id="a6ad1-145">To specify a Shell namespace object, pass the fully qualified parse name.</span></span> <span data-ttu-id="a6ad1-146">請注意，並非所有的動詞都支援所有物件。</span><span class="sxs-lookup"><span data-stu-id="a6ad1-146">Note that not all verbs are supported on all objects.</span></span> <span data-ttu-id="a6ad1-147">例如，並非所有檔案類型都支援 "print" 動詞。</span><span class="sxs-lookup"><span data-stu-id="a6ad1-147">For example, not all document types support the "print" verb.</span></span>

</dd> <dt>

<span data-ttu-id="a6ad1-148">*lpParameters* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a6ad1-148">*lpParameters* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6ad1-149">類型： **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="a6ad1-149">Type: **LPCTSTR**</span></span>

<span data-ttu-id="a6ad1-150">如果 *lpFile* 參數指定可執行檔，則 *lpParameters* 是以 **null** 結束的字串指標，可指定要傳遞至應用程式的參數。</span><span class="sxs-lookup"><span data-stu-id="a6ad1-150">If the *lpFile* parameter specifies an executable file, *lpParameters* is a pointer to a **null**-terminated string that specifies the parameters to be passed to the application.</span></span> <span data-ttu-id="a6ad1-151">這個字串的格式取決於要叫用的動詞。</span><span class="sxs-lookup"><span data-stu-id="a6ad1-151">The format of this string is determined by the verb that is to be invoked.</span></span> <span data-ttu-id="a6ad1-152">如果 *lpFile* 指定檔檔， *LpParameters* 應該是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="a6ad1-152">If *lpFile* specifies a document file, *lpParameters* should be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a6ad1-153">*lpDirectory* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a6ad1-153">*lpDirectory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6ad1-154">類型： **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="a6ad1-154">Type: **LPCTSTR**</span></span>

<span data-ttu-id="a6ad1-155">指定預設目錄之以 **null** 結束的字串指標。</span><span class="sxs-lookup"><span data-stu-id="a6ad1-155">A pointer to a **null**-terminated string that specifies the default directory.</span></span>

</dd> <dt>

<span data-ttu-id="a6ad1-156">*nShowCmd* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a6ad1-156">*nShowCmd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6ad1-157">類型： **INT**</span><span class="sxs-lookup"><span data-stu-id="a6ad1-157">Type: **INT**</span></span>

<span data-ttu-id="a6ad1-158">旗標，指定應用程式在開啟時的顯示方式。</span><span class="sxs-lookup"><span data-stu-id="a6ad1-158">The flags that specify how an application is to be displayed when it is opened.</span></span> <span data-ttu-id="a6ad1-159">如果 *lpFile* 指定檔檔，旗標就會直接傳遞至相關聯的應用程式。</span><span class="sxs-lookup"><span data-stu-id="a6ad1-159">If *lpFile* specifies a document file, the flag is simply passed to the associated application.</span></span> <span data-ttu-id="a6ad1-160">應用程式會決定如何處理它。</span><span class="sxs-lookup"><span data-stu-id="a6ad1-160">It is up to the application to decide how to handle it.</span></span> <span data-ttu-id="a6ad1-161">它可以是任何可在 [ShowWindow](/windows/desktop/api/winuser/nf-winuser-showwindow)函數的 *nCmdShow* 參數中指定的值。</span><span class="sxs-lookup"><span data-stu-id="a6ad1-161">It can be any of the values that can be specified in the *nCmdShow* parameter for the [ShowWindow](/windows/desktop/api/winuser/nf-winuser-showwindow) function.</span></span>

</dd> <dt>

<span data-ttu-id="a6ad1-162">*lpfnCBWinExec*</span><span class="sxs-lookup"><span data-stu-id="a6ad1-162">*lpfnCBWinExec*</span></span> 
</dt> <dd>

<span data-ttu-id="a6ad1-163">類型： **void \***</span><span class="sxs-lookup"><span data-stu-id="a6ad1-163">Type: **void\***</span></span>

<span data-ttu-id="a6ad1-164">用來在16位核心中呼叫 [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) 的回呼函數。</span><span class="sxs-lookup"><span data-stu-id="a6ad1-164">Callback function used to call [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) in the 16-bit kernel.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6ad1-165">傳回值</span><span class="sxs-lookup"><span data-stu-id="a6ad1-165">Return value</span></span>

<span data-ttu-id="a6ad1-166">類型： **HINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="a6ad1-166">Type: **HINSTANCE**</span></span>

<span data-ttu-id="a6ad1-167">如果成功，則傳回大於32的值，否則傳回小於或等於32的錯誤值。</span><span class="sxs-lookup"><span data-stu-id="a6ad1-167">Returns a value greater than 32 if successful, or an error value that is less than or equal to 32 otherwise.</span></span> <span data-ttu-id="a6ad1-168">下表列出錯誤值。</span><span class="sxs-lookup"><span data-stu-id="a6ad1-168">The following table lists the error values.</span></span> <span data-ttu-id="a6ad1-169">傳回值會轉換成 HINSTANCE，以提供與16位 Windows 應用程式的回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="a6ad1-169">The return value is cast as an HINSTANCE for backward compatibility with 16-bit Windows applications.</span></span> <span data-ttu-id="a6ad1-170">不過，這不是真正的 HINSTANCE。</span><span class="sxs-lookup"><span data-stu-id="a6ad1-170">It is not a true HINSTANCE, however.</span></span> <span data-ttu-id="a6ad1-171">使用傳回的 HINSTANCE 唯一可以完成的工作，就是將它轉換 **成整數，並將** 其與值32或下列其中一個錯誤碼進行比較。</span><span class="sxs-lookup"><span data-stu-id="a6ad1-171">The only thing that can be done with the returned HINSTANCE is to cast it to an **int** and compare it with the value 32 or one of the error codes below.</span></span>



| <span data-ttu-id="a6ad1-172">傳回碼</span><span class="sxs-lookup"><span data-stu-id="a6ad1-172">Return code</span></span>                                                                                             | <span data-ttu-id="a6ad1-173">Description</span><span class="sxs-lookup"><span data-stu-id="a6ad1-173">Description</span></span>                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a6ad1-174"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="a6ad1-174"><dt>**0**</dt></span></span> </dl>                        | <span data-ttu-id="a6ad1-175">作業系統已用盡記憶體或資源。</span><span class="sxs-lookup"><span data-stu-id="a6ad1-175">The operating system is out of memory or resources.</span></span><br/>                                                                                                           |
| <dl> <span data-ttu-id="a6ad1-176"><dt>**\_ \_ \_ 找不到錯誤檔案**</dt></span><span class="sxs-lookup"><span data-stu-id="a6ad1-176"><dt>**ERROR\_FILE\_NOT\_FOUND**</dt></span></span> </dl>  | <span data-ttu-id="a6ad1-177">找不到指定的檔案。</span><span class="sxs-lookup"><span data-stu-id="a6ad1-177">The specified file was not found.</span></span><br/>                                                                                                                             |
| <dl> <span data-ttu-id="a6ad1-178"><dt>**\_ \_ 找不到錯誤路徑 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a6ad1-178"><dt>**ERROR\_PATH\_NOT\_FOUND**</dt></span></span> </dl>  | <span data-ttu-id="a6ad1-179">找不到指定的路徑。</span><span class="sxs-lookup"><span data-stu-id="a6ad1-179">The specified path was not found.</span></span><br/>                                                                                                                             |
| <dl> <span data-ttu-id="a6ad1-180"><dt>**錯誤 \_ \_ 格式錯誤**</dt></span><span class="sxs-lookup"><span data-stu-id="a6ad1-180"><dt>**ERROR\_BAD\_FORMAT**</dt></span></span> </dl>       | <span data-ttu-id="a6ad1-181">.Exe 檔 (非 Win32 .exe 或 .exe 映射) 中的錯誤無效。</span><span class="sxs-lookup"><span data-stu-id="a6ad1-181">The .exe file is invalid (non-Win32 .exe or error in .exe image).</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="a6ad1-182"><dt>**SE \_ ERR \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="a6ad1-182"><dt>**SE\_ERR\_ACCESSDENIED**</dt></span></span> </dl>    | <span data-ttu-id="a6ad1-183">作業系統拒絕存取指定的檔案。</span><span class="sxs-lookup"><span data-stu-id="a6ad1-183">The operating system denied access to the specified file.</span></span><br/>                                                                                                     |
| <dl> <span data-ttu-id="a6ad1-184"><dt>**SE \_ ERR \_ ASSOCINCOMPLETE**</dt></span><span class="sxs-lookup"><span data-stu-id="a6ad1-184"><dt>**SE\_ERR\_ASSOCINCOMPLETE**</dt></span></span> </dl> | <span data-ttu-id="a6ad1-185">檔案名關聯未完成或無效。</span><span class="sxs-lookup"><span data-stu-id="a6ad1-185">The file name association is incomplete or invalid.</span></span><br/>                                                                                                           |
| <dl> <span data-ttu-id="a6ad1-186"><dt>**SE \_ ERR \_ DDEBUSY**</dt></span><span class="sxs-lookup"><span data-stu-id="a6ad1-186"><dt>**SE\_ERR\_DDEBUSY**</dt></span></span> </dl>         | <span data-ttu-id="a6ad1-187">無法完成 DDE 交易，因為正在處理其他 DDE 交易。</span><span class="sxs-lookup"><span data-stu-id="a6ad1-187">The DDE transaction could not be completed because other DDE transactions were being processed.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="a6ad1-188"><dt>**SE \_ ERR \_ DDEFAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="a6ad1-188"><dt>**SE\_ERR\_DDEFAIL**</dt></span></span> </dl>         | <span data-ttu-id="a6ad1-189">DDE 交易失敗。</span><span class="sxs-lookup"><span data-stu-id="a6ad1-189">The DDE transaction failed.</span></span><br/>                                                                                                                                   |
| <dl> <span data-ttu-id="a6ad1-190"><dt>**SE \_ ERR \_ DDETIMEOUT**</dt></span><span class="sxs-lookup"><span data-stu-id="a6ad1-190"><dt>**SE\_ERR\_DDETIMEOUT**</dt></span></span> </dl>      | <span data-ttu-id="a6ad1-191">因為要求超時，所以無法完成 DDE 交易。</span><span class="sxs-lookup"><span data-stu-id="a6ad1-191">The DDE transaction could not be completed because the request timed out.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="a6ad1-192"><dt>**SE \_ ERR \_ DLLNOTFOUND**</dt></span><span class="sxs-lookup"><span data-stu-id="a6ad1-192"><dt>**SE\_ERR\_DLLNOTFOUND**</dt></span></span> </dl>     | <span data-ttu-id="a6ad1-193">找不到指定的 DLL。</span><span class="sxs-lookup"><span data-stu-id="a6ad1-193">The specified DLL was not found.</span></span><br/>                                                                                                                              |
| <dl> <span data-ttu-id="a6ad1-194"><dt>**SE \_ ERR \_ FNF**</dt></span><span class="sxs-lookup"><span data-stu-id="a6ad1-194"><dt>**SE\_ERR\_FNF**</dt></span></span> </dl>             | <span data-ttu-id="a6ad1-195">找不到指定的檔案。</span><span class="sxs-lookup"><span data-stu-id="a6ad1-195">The specified file was not found.</span></span><br/>                                                                                                                             |
| <dl> <span data-ttu-id="a6ad1-196"><dt>**SE \_ ERR \_ NOASSOC**</dt></span><span class="sxs-lookup"><span data-stu-id="a6ad1-196"><dt>**SE\_ERR\_NOASSOC**</dt></span></span> </dl>         | <span data-ttu-id="a6ad1-197">沒有與指定副檔名相關聯的應用程式。</span><span class="sxs-lookup"><span data-stu-id="a6ad1-197">There is no application associated with the given file name extension.</span></span> <span data-ttu-id="a6ad1-198">如果您嘗試列印無法列印的檔案，也會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="a6ad1-198">This error will also be returned if you attempt to print a file that is not printable.</span></span><br/> |
| <dl> <span data-ttu-id="a6ad1-199"><dt>**SE \_ ERR \_ OOM**</dt></span><span class="sxs-lookup"><span data-stu-id="a6ad1-199"><dt>**SE\_ERR\_OOM**</dt></span></span> </dl>             | <span data-ttu-id="a6ad1-200">沒有足夠的記憶體可完成此作業。</span><span class="sxs-lookup"><span data-stu-id="a6ad1-200">There was not enough memory to complete the operation.</span></span><br/>                                                                                                        |
| <dl> <span data-ttu-id="a6ad1-201"><dt>**SE \_ ERR \_ PNF**</dt></span><span class="sxs-lookup"><span data-stu-id="a6ad1-201"><dt>**SE\_ERR\_PNF**</dt></span></span> </dl>             | <span data-ttu-id="a6ad1-202">找不到指定的路徑。</span><span class="sxs-lookup"><span data-stu-id="a6ad1-202">The specified path was not found.</span></span><br/>                                                                                                                             |
| <dl> <span data-ttu-id="a6ad1-203"><dt>**SE \_ ERR \_ 共用**</dt></span><span class="sxs-lookup"><span data-stu-id="a6ad1-203"><dt>**SE\_ERR\_SHARE**</dt></span></span> </dl>           | <span data-ttu-id="a6ad1-204">發生共用違規。</span><span class="sxs-lookup"><span data-stu-id="a6ad1-204">A sharing violation occurred.</span></span><br/>                                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="a6ad1-205">備註</span><span class="sxs-lookup"><span data-stu-id="a6ad1-205">Remarks</span></span>

<span data-ttu-id="a6ad1-206">**WOWShellExecute** 不包含在標頭或 .lib 檔案中。</span><span class="sxs-lookup"><span data-stu-id="a6ad1-206">**WOWShellExecute** is not included in a header or .lib file.</span></span> <span data-ttu-id="a6ad1-207">它會依名稱從 Shell32.dll 匯出。</span><span class="sxs-lookup"><span data-stu-id="a6ad1-207">It is exported from Shell32.dll by name.</span></span>

<span data-ttu-id="a6ad1-208">這個方法可讓您在資料夾的快捷方式功能表中執行任何命令，或儲存在登錄中。</span><span class="sxs-lookup"><span data-stu-id="a6ad1-208">This method allows you to execute any commands in a folder's shortcut menu or stored in the registry.</span></span>

<span data-ttu-id="a6ad1-209">如果 *lpOperation* 為 **Null**，則函式會開啟 *lpFile* 所指定的檔案。</span><span class="sxs-lookup"><span data-stu-id="a6ad1-209">If *lpOperation* is **NULL**, the function opens the file specified by *lpFile*.</span></span> <span data-ttu-id="a6ad1-210">如果 *lpOperation* 為「開啟」或「探索」，則函式會嘗試開啟或流覽資料夾。</span><span class="sxs-lookup"><span data-stu-id="a6ad1-210">If *lpOperation* is "open" or "explore", the function attempts to open or explore the folder.</span></span>

<span data-ttu-id="a6ad1-211">若要取得由於呼叫 **WOWShellExecute** 而啟動之應用程式的相關資訊，請使用 [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa)。</span><span class="sxs-lookup"><span data-stu-id="a6ad1-211">To obtain information about the application that is launched as a result of calling **WOWShellExecute**, use [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span></span>

> [!Note]  
> <span data-ttu-id="a6ad1-212">[資料夾選項] 中個別進程設定的 [ **開機檔案夾] 視窗** 會影響 **WOWShellExecute**。</span><span class="sxs-lookup"><span data-stu-id="a6ad1-212">The **Launch folder windows in a separate process** setting in Folder Options affects **WOWShellExecute**.</span></span> <span data-ttu-id="a6ad1-213">如果停用該選項 (預設設定) ， **WOWShellExecute** 會使用開啟的瀏覽器視窗，而不是啟動新的視窗。</span><span class="sxs-lookup"><span data-stu-id="a6ad1-213">If that option is disabled (the default setting), **WOWShellExecute** uses an open Explorer window rather than launch a new one.</span></span> <span data-ttu-id="a6ad1-214">如果未開啟任何 Explorer 視窗， **WOWShellExecute** 會啟動一個新視窗。</span><span class="sxs-lookup"><span data-stu-id="a6ad1-214">If no Explorer window is open, **WOWShellExecute** launches a new one.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a6ad1-215">規格需求</span><span class="sxs-lookup"><span data-stu-id="a6ad1-215">Requirements</span></span>



| <span data-ttu-id="a6ad1-216">需求</span><span class="sxs-lookup"><span data-stu-id="a6ad1-216">Requirement</span></span> | <span data-ttu-id="a6ad1-217">值</span><span class="sxs-lookup"><span data-stu-id="a6ad1-217">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a6ad1-218">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a6ad1-218">Minimum supported client</span></span><br/> | <span data-ttu-id="a6ad1-219">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a6ad1-219">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a6ad1-220">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a6ad1-220">Minimum supported server</span></span><br/> | <span data-ttu-id="a6ad1-221">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a6ad1-221">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a6ad1-222">DLL</span><span class="sxs-lookup"><span data-stu-id="a6ad1-222">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a6ad1-223"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a6ad1-223"><dt>Shell32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6ad1-224">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a6ad1-224">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6ad1-225">**ShellExecute**</span><span class="sxs-lookup"><span data-stu-id="a6ad1-225">**ShellExecute**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea)
</dt> </dl>

 

 
