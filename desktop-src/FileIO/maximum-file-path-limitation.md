---
description: 最大路徑長度限制。
title: 最大路徑長度限制
ms.topic: article
ms.custom: contperf-fy21q1
ms.date: 09/15/2020
ms.openlocfilehash: 4bf5050f24827a2033c1e56fd9413c04f4e59500
ms.sourcegitcommit: ece80b9b7082415b2f894b0696b6b3f0c8544d72
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107899737"
---
# <a name="maximum-path-length-limitation"></a><span data-ttu-id="229db-103">最大路徑長度限制</span><span class="sxs-lookup"><span data-stu-id="229db-103">Maximum Path Length Limitation</span></span>

<span data-ttu-id="229db-104">在 Windows API (中，) 下列段落中所討論的一些例外狀況，路徑的最大長度為 **最大 \_ 路徑**，定義為260個字元。</span><span class="sxs-lookup"><span data-stu-id="229db-104">In the Windows API (with some exceptions discussed in the following paragraphs), the maximum length for a path is **MAX\_PATH**, which is defined as 260 characters.</span></span> <span data-ttu-id="229db-105">本機路徑的結構如下：磁碟機號、冒號、反斜線、以反斜線分隔的名稱元件，以及終止的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="229db-105">A local path is structured in the following order: drive letter, colon, backslash, name components separated by backslashes, and a terminating null character.</span></span> <span data-ttu-id="229db-106">例如，磁片磁碟機 D 上的最大路徑為 "D： \\ *某些 256-字元路徑字串* &lt; NUL &gt; "，其中 " &lt; NUL &gt; " 代表目前系統字碼頁的不可見結束 null 字元。</span><span class="sxs-lookup"><span data-stu-id="229db-106">For example, the maximum path on drive D is "D:\\*some 256-character path string*&lt;NUL&gt;" where "&lt;NUL&gt;" represents the invisible terminating null character for the current system codepage.</span></span> <span data-ttu-id="229db-107"> (使用 < > 的字元作為視覺效果，且不能是有效路徑字串的一部分。 ) </span><span class="sxs-lookup"><span data-stu-id="229db-107">(The characters < > are used here for visual clarity and cannot be part of a valid path string.)</span></span>

<span data-ttu-id="229db-108">例如，如果您要將副檔名很長的 git 存放庫複製到本身具有完整名稱的資料夾中，則可能會達到此限制。</span><span class="sxs-lookup"><span data-stu-id="229db-108">For example, you may hit this limitation if you are cloning a git repo that has long file names into a folder that itself has a long name.</span></span>


> [!Note]  
> <span data-ttu-id="229db-109">Windows API 中的檔案 i/o 函式會將 "/" 轉換成 " \\ "，做為將名稱轉換成 NT 樣式名稱的一部分，除非使用 " \\ \\ ？ \\ " 前置詞，如下列各節所述。</span><span class="sxs-lookup"><span data-stu-id="229db-109">File I/O functions in the Windows API convert "/" to "\\" as part of converting the name to an NT-style name, except when using the "\\\\?\\" prefix as detailed in the following sections.</span></span>

<span data-ttu-id="229db-110">Windows API 有許多函數，也有 Unicode 版本可允許長度上限為32767個字元的最大路徑長度的擴充長度路徑。</span><span class="sxs-lookup"><span data-stu-id="229db-110">The Windows API has many functions that also have Unicode versions to permit an extended-length path for a maximum total path length of 32,767 characters.</span></span> <span data-ttu-id="229db-111">這種類型的路徑是由以反斜線分隔的元件所組成，每個都是在 [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa)函數的 *lpMaximumComponentLength* 參數中所傳回的值 (此值通常是255個字元) 。</span><span class="sxs-lookup"><span data-stu-id="229db-111">This type of path is composed of components separated by backslashes, each up to the value returned in the *lpMaximumComponentLength* parameter of the [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) function (this value is commonly 255 characters).</span></span> <span data-ttu-id="229db-112">若要指定延長長度的路徑，請使用 " \\ \\ ？ \\ " 前置詞。</span><span class="sxs-lookup"><span data-stu-id="229db-112">To specify an extended-length path, use the "\\\\?\\" prefix.</span></span> <span data-ttu-id="229db-113">例如，「 \\ \\ ？ \\D： \\ *非常長的路徑*」。</span><span class="sxs-lookup"><span data-stu-id="229db-113">For example, "\\\\?\\D:\\*very long path*".</span></span>

> [!Note]  
> <span data-ttu-id="229db-114">32767個字元的最大路徑為近似值，因為在 \\ \\ \\ 執行時間，"？" 前置詞可能會擴充為較長的字串，而這項擴充會套用至總長度。</span><span class="sxs-lookup"><span data-stu-id="229db-114">The maximum path of 32,767 characters is approximate, because the "\\\\?\\" prefix may be expanded to a longer string by the system at run time, and this expansion applies to the total length.</span></span>

<span data-ttu-id="229db-115">" \\ \\ ？ \\ " 前置詞也可以搭配根據通用命名慣例 (UNC) 所建立的路徑使用。</span><span class="sxs-lookup"><span data-stu-id="229db-115">The "\\\\?\\" prefix can also be used with paths constructed according to the universal naming convention (UNC).</span></span> <span data-ttu-id="229db-116">若要使用 UNC 指定這類路徑，請使用 " \\ \\ ？ \\UNC \\ "前置詞。</span><span class="sxs-lookup"><span data-stu-id="229db-116">To specify such a path using UNC, use the "\\\\?\\UNC\\" prefix.</span></span> <span data-ttu-id="229db-117">例如，「 \\ \\ ？ \\UNC \\ 伺服器 \\ 共用 "，其中" server "是電腦的名稱，而" share "是共用資料夾的名稱。</span><span class="sxs-lookup"><span data-stu-id="229db-117">For example, "\\\\?\\UNC\\server\\share", where "server" is the name of the computer and "share" is the name of the shared folder.</span></span> <span data-ttu-id="229db-118">這些前置詞不會當做路徑本身的一部分使用。</span><span class="sxs-lookup"><span data-stu-id="229db-118">These prefixes are not used as part of the path itself.</span></span> <span data-ttu-id="229db-119">它們表示路徑應以最少量的修改傳遞給系統，這表示您不能使用正斜線來代表路徑分隔符號，也不能使用句點來代表目前的目錄，或以雙點表示父目錄。</span><span class="sxs-lookup"><span data-stu-id="229db-119">They indicate that the path should be passed to the system with minimal modification, which means that you cannot use forward slashes to represent path separators, or a period to represent the current directory, or double dots to represent the parent directory.</span></span> <span data-ttu-id="229db-120">因為您無法在 \\ \\ \\ 相對路徑中使用 "？" 前置詞，所以相對路徑一律會限制為 **最大 \_ 路徑** 字元總數。</span><span class="sxs-lookup"><span data-stu-id="229db-120">Because you cannot use the "\\\\?\\" prefix with a relative path, relative paths are always limited to a total of **MAX\_PATH** characters.</span></span>

<span data-ttu-id="229db-121">因為檔案系統會將路徑和檔案名視為不透明的 **WCHAR** 序列，所以不需要在路徑和檔案名字串上執行任何 Unicode 正規化以供 Windows 檔案 i/o API 函數使用。</span><span class="sxs-lookup"><span data-stu-id="229db-121">There is no need to perform any Unicode normalization on path and file name strings for use by the Windows file I/O API functions because the file system treats path and file names as an opaque sequence of **WCHAR** s.</span></span> <span data-ttu-id="229db-122">您的應用程式所需的任何正規化都應該以這種方式執行，也就是對相關 Windows 檔案 i/o API 功能的任何呼叫。</span><span class="sxs-lookup"><span data-stu-id="229db-122">Any normalization that your application requires should be performed with this in mind, external of any calls to related Windows file I/O API functions.</span></span>

<span data-ttu-id="229db-123">使用 API 建立目錄時，指定的路徑不能超過您的長度，因為您無法附加8.3 檔案名 (也就是說，目錄名稱不能超過 **最大 \_ 路徑** 減 12) 。</span><span class="sxs-lookup"><span data-stu-id="229db-123">When using an API to create a directory, the specified path cannot be so long that you cannot append an 8.3 file name (that is, the directory name cannot exceed **MAX\_PATH** minus 12).</span></span>

<span data-ttu-id="229db-124">Shell 和檔案系統有不同的需求。</span><span class="sxs-lookup"><span data-stu-id="229db-124">The shell and the file system have different requirements.</span></span> <span data-ttu-id="229db-125">您可以使用 Windows API 建立路徑，讓 shell 使用者介面無法正確解讀。</span><span class="sxs-lookup"><span data-stu-id="229db-125">It is possible to create a path with the Windows API that the shell user interface is not able to interpret properly.</span></span>

## <a name="enable-long-paths-in-windows-10-version-1607-and-later"></a><span data-ttu-id="229db-126">在 Windows 10、1607版和更新版本中啟用長路徑</span><span class="sxs-lookup"><span data-stu-id="229db-126">Enable Long Paths in Windows 10, Version 1607, and Later</span></span>

<span data-ttu-id="229db-127">從 Windows 10 開始，版本1607，已從一般 Win32 檔案和目錄函式移除 **最大 \_ 路徑** 限制。</span><span class="sxs-lookup"><span data-stu-id="229db-127">Starting in Windows 10, version 1607, **MAX\_PATH** limitations have been removed from common Win32 file and directory functions.</span></span> <span data-ttu-id="229db-128">不過，您必須加入新的行為。</span><span class="sxs-lookup"><span data-stu-id="229db-128">However, you must opt-in to the new behavior.</span></span>

<span data-ttu-id="229db-129">若要啟用新的完整路徑行為，必須符合下列兩個條件：</span><span class="sxs-lookup"><span data-stu-id="229db-129">To enable the new long path behavior, both of the following conditions must be met:</span></span>

* <span data-ttu-id="229db-130">登錄機碼 `Computer\HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\FileSystem\LongPathsEnabled (Type: REG_DWORD)` 必須存在，且必須設定為1。</span><span class="sxs-lookup"><span data-stu-id="229db-130">The registry key `Computer\HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\FileSystem\LongPathsEnabled (Type: REG_DWORD)` must exist and be set to 1.</span></span> <span data-ttu-id="229db-131">系統會在第一次呼叫受影響的 Win32 檔案或目錄函式之後，) 每個進程的系統 (快取索引鍵的值 (請參閱下文以取得) 的函式清單。</span><span class="sxs-lookup"><span data-stu-id="229db-131">The key's value will be cached by the system (per process) after the first call to an affected Win32 file or directory function (see below for the list of functions).</span></span> <span data-ttu-id="229db-132">登錄機碼不會在進程的存留期間重載。</span><span class="sxs-lookup"><span data-stu-id="229db-132">The registry key will not be reloaded during the lifetime of the process.</span></span> <span data-ttu-id="229db-133">為了讓系統上的所有應用程式都能辨識金鑰的值，可能需要重新開機，因為某些進程可能會在設定金鑰之前啟動。</span><span class="sxs-lookup"><span data-stu-id="229db-133">In order for all apps on the system to recognize the value of the key, a reboot might be required because some processes may have started before the key was set.</span></span>

<span data-ttu-id="229db-134">您也可以將此程式碼複製到 `.reg` 可為您設定的檔案，或從終端機視窗使用具有較高許可權的 PowerShell 命令：</span><span class="sxs-lookup"><span data-stu-id="229db-134">You can also copy this code to a `.reg` file which can set this for you, or use the PowerShell command from a terminal window with elevated privileges:</span></span>
# <a name="cmd"></a>[<span data-ttu-id="229db-135">cmd</span><span class="sxs-lookup"><span data-stu-id="229db-135">cmd</span></span>](#tab/cmd)

```cmd
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\FileSystem]
"LongPathsEnabled"=dword:00000001

```

# <a name="powershell"></a>[<span data-ttu-id="229db-136">PowerShell</span><span class="sxs-lookup"><span data-stu-id="229db-136">PowerShell</span></span>](#tab/powershell)

```powershell
New-ItemProperty -Path "HKLM:\SYSTEM\CurrentControlSet\Control\FileSystem" `
-Name "LongPathsEnabled" -Value 1 -PropertyType DWORD -Force

```

---

> [!NOTE]  
> <span data-ttu-id="229db-137">此登錄機碼也可以透過群組原則來控制 `Computer Configuration > Administrative Templates > System > Filesystem > Enable Win32 long paths` 。</span><span class="sxs-lookup"><span data-stu-id="229db-137">This registry key can also be controlled via Group Policy at `Computer Configuration > Administrative Templates > System > Filesystem > Enable Win32 long paths`.</span></span>

* <span data-ttu-id="229db-138">[應用程式資訊清單](../sbscs/application-manifests.md)也必須包含 `longPathAware` 元素。</span><span class="sxs-lookup"><span data-stu-id="229db-138">The [application manifest](../sbscs/application-manifests.md) must also include the `longPathAware` element.</span></span>

    ```XML
    <application xmlns="urn:schemas-microsoft-com:asm.v3">
        <windowsSettings xmlns:ws2="http://schemas.microsoft.com/SMI/2016/WindowsSettings">
            <ws2:longPathAware>true</ws2:longPathAware>
        </windowsSettings>
    </application>
    ```

<span data-ttu-id="229db-139">如果您選擇使用長路徑行為，則這些目錄管理函式不會再有 **最大 \_ 路徑** 限制： CreateDirectoryW、CreateDirectoryExW GetCurrentDirectoryW RemoveDirectoryW SetCurrentDirectoryW。</span><span class="sxs-lookup"><span data-stu-id="229db-139">These are the directory management functions that no longer have **MAX\_PATH** restrictions if you opt-in to long path behavior: CreateDirectoryW, CreateDirectoryExW GetCurrentDirectoryW RemoveDirectoryW SetCurrentDirectoryW.</span></span>

<span data-ttu-id="229db-140">如果您選擇使用長路徑行為，則這些檔案管理函式不再具有 **最大 \_ 路徑** 限制： CopyFileW、CopyFile2、CopyFileExW、CreateFileW、CreateFile2、CreateHardLinkW、CreateSymbolicLinkW、DeleteFileW、FindFirstFileW、FindFirstFileExW、FindNextFileW、GetFileAttributesW、GetFileAttributesExW、SetFileAttributesW、GetFullPathNameW、GetLongPathNameW、MoveFileW、MoveFileExW、MoveFileWithProgressW、ReplaceFileW、SearchPathW、FindFirstFileNameW、FindNextFileNameW、FindFirstStreamW、FindNextStreamW、GetCompressedFileSizeW、GetFinalPathNameByHandleW。</span><span class="sxs-lookup"><span data-stu-id="229db-140">These are the file management functions that no longer have **MAX\_PATH** restrictions if you opt-in to long path behavior: CopyFileW, CopyFile2, CopyFileExW, CreateFileW, CreateFile2, CreateHardLinkW, CreateSymbolicLinkW, DeleteFileW, FindFirstFileW, FindFirstFileExW, FindNextFileW, GetFileAttributesW, GetFileAttributesExW, SetFileAttributesW, GetFullPathNameW, GetLongPathNameW, MoveFileW, MoveFileExW, MoveFileWithProgressW, ReplaceFileW, SearchPathW, FindFirstFileNameW, FindNextFileNameW, FindFirstStreamW, FindNextStreamW, GetCompressedFileSizeW, GetFinalPathNameByHandleW.</span></span>
