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
# <a name="maximum-path-length-limitation"></a>最大路徑長度限制

在 Windows API (中，) 下列段落中所討論的一些例外狀況，路徑的最大長度為 **最大 \_ 路徑**，定義為260個字元。 本機路徑的結構如下：磁碟機號、冒號、反斜線、以反斜線分隔的名稱元件，以及終止的 null 字元。 例如，磁片磁碟機 D 上的最大路徑為 "D： \\ *某些 256-字元路徑字串* &lt; NUL &gt; "，其中 " &lt; NUL &gt; " 代表目前系統字碼頁的不可見結束 null 字元。  (使用 < > 的字元作為視覺效果，且不能是有效路徑字串的一部分。 ) 

例如，如果您要將副檔名很長的 git 存放庫複製到本身具有完整名稱的資料夾中，則可能會達到此限制。


> [!Note]  
> Windows API 中的檔案 i/o 函式會將 "/" 轉換成 " \\ "，做為將名稱轉換成 NT 樣式名稱的一部分，除非使用 " \\ \\ ？ \\ " 前置詞，如下列各節所述。

Windows API 有許多函數，也有 Unicode 版本可允許長度上限為32767個字元的最大路徑長度的擴充長度路徑。 這種類型的路徑是由以反斜線分隔的元件所組成，每個都是在 [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa)函數的 *lpMaximumComponentLength* 參數中所傳回的值 (此值通常是255個字元) 。 若要指定延長長度的路徑，請使用 " \\ \\ ？ \\ " 前置詞。 例如，「 \\ \\ ？ \\D： \\ *非常長的路徑*」。

> [!Note]  
> 32767個字元的最大路徑為近似值，因為在 \\ \\ \\ 執行時間，"？" 前置詞可能會擴充為較長的字串，而這項擴充會套用至總長度。

" \\ \\ ？ \\ " 前置詞也可以搭配根據通用命名慣例 (UNC) 所建立的路徑使用。 若要使用 UNC 指定這類路徑，請使用 " \\ \\ ？ \\UNC \\ "前置詞。 例如，「 \\ \\ ？ \\UNC \\ 伺服器 \\ 共用 "，其中" server "是電腦的名稱，而" share "是共用資料夾的名稱。 這些前置詞不會當做路徑本身的一部分使用。 它們表示路徑應以最少量的修改傳遞給系統，這表示您不能使用正斜線來代表路徑分隔符號，也不能使用句點來代表目前的目錄，或以雙點表示父目錄。 因為您無法在 \\ \\ \\ 相對路徑中使用 "？" 前置詞，所以相對路徑一律會限制為 **最大 \_ 路徑** 字元總數。

因為檔案系統會將路徑和檔案名視為不透明的 **WCHAR** 序列，所以不需要在路徑和檔案名字串上執行任何 Unicode 正規化以供 Windows 檔案 i/o API 函數使用。 您的應用程式所需的任何正規化都應該以這種方式執行，也就是對相關 Windows 檔案 i/o API 功能的任何呼叫。

使用 API 建立目錄時，指定的路徑不能超過您的長度，因為您無法附加8.3 檔案名 (也就是說，目錄名稱不能超過 **最大 \_ 路徑** 減 12) 。

Shell 和檔案系統有不同的需求。 您可以使用 Windows API 建立路徑，讓 shell 使用者介面無法正確解讀。

## <a name="enable-long-paths-in-windows-10-version-1607-and-later"></a>在 Windows 10、1607版和更新版本中啟用長路徑

從 Windows 10 開始，版本1607，已從一般 Win32 檔案和目錄函式移除 **最大 \_ 路徑** 限制。 不過，您必須加入新的行為。

若要啟用新的完整路徑行為，必須符合下列兩個條件：

* 登錄機碼 `Computer\HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\FileSystem\LongPathsEnabled (Type: REG_DWORD)` 必須存在，且必須設定為1。 系統會在第一次呼叫受影響的 Win32 檔案或目錄函式之後，) 每個進程的系統 (快取索引鍵的值 (請參閱下文以取得) 的函式清單。 登錄機碼不會在進程的存留期間重載。 為了讓系統上的所有應用程式都能辨識金鑰的值，可能需要重新開機，因為某些進程可能會在設定金鑰之前啟動。

您也可以將此程式碼複製到 `.reg` 可為您設定的檔案，或從終端機視窗使用具有較高許可權的 PowerShell 命令：
# <a name="cmd"></a>[cmd](#tab/cmd)

```cmd
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\FileSystem]
"LongPathsEnabled"=dword:00000001

```

# <a name="powershell"></a>[PowerShell](#tab/powershell)

```powershell
New-ItemProperty -Path "HKLM:\SYSTEM\CurrentControlSet\Control\FileSystem" `
-Name "LongPathsEnabled" -Value 1 -PropertyType DWORD -Force

```

---

> [!NOTE]  
> 此登錄機碼也可以透過群組原則來控制 `Computer Configuration > Administrative Templates > System > Filesystem > Enable Win32 long paths` 。

* [應用程式資訊清單](../sbscs/application-manifests.md)也必須包含 `longPathAware` 元素。

    ```XML
    <application xmlns="urn:schemas-microsoft-com:asm.v3">
        <windowsSettings xmlns:ws2="http://schemas.microsoft.com/SMI/2016/WindowsSettings">
            <ws2:longPathAware>true</ws2:longPathAware>
        </windowsSettings>
    </application>
    ```

如果您選擇使用長路徑行為，則這些目錄管理函式不會再有 **最大 \_ 路徑** 限制： CreateDirectoryW、CreateDirectoryExW GetCurrentDirectoryW RemoveDirectoryW SetCurrentDirectoryW。

如果您選擇使用長路徑行為，則這些檔案管理函式不再具有 **最大 \_ 路徑** 限制： CopyFileW、CopyFile2、CopyFileExW、CreateFileW、CreateFile2、CreateHardLinkW、CreateSymbolicLinkW、DeleteFileW、FindFirstFileW、FindFirstFileExW、FindNextFileW、GetFileAttributesW、GetFileAttributesExW、SetFileAttributesW、GetFullPathNameW、GetLongPathNameW、MoveFileW、MoveFileExW、MoveFileWithProgressW、ReplaceFileW、SearchPathW、FindFirstFileNameW、FindNextFileNameW、FindFirstStreamW、FindNextStreamW、GetCompressedFileSizeW、GetFinalPathNameByHandleW。
