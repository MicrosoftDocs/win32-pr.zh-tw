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
# <a name="debugging-with-the-shell"></a>使用 Shell 進行偵錯工具

本主題說明如何 debug Shell 和命名空間延伸 Dll。

-   [在偵錯工具下執行 Shell](#running-the-shell-under-a-debugger)
-   [執行和測試 Shell 擴充功能](#running-and-testing-shell-extensions)
-   [卸載 DLL](#unloading-the-dll)

## <a name="running-the-shell-under-a-debugger"></a>在偵錯工具下執行 Shell

若要對您的延伸模組進行偵錯工具，您需要從偵錯工具執行 Shell。 請遵循下列步驟：

1.  將延伸模組的專案載入偵錯工具，但不要執行。
2.  關閉 Shell。

    -   針對 Windows Vista 和更新版本：
        1.  顯示 [ **開始** ] 功能表。
        2.  按 CTRL + SHIFT 鍵，然後以滑鼠右鍵按一下 [ **開始** ] 功能表右邊一半的背景。
        3.  從出現的功能表中選擇 [ **Exit Explorer**]。
    -   若為 Windows XP：
        1.  在 [ **開始** ] 功能表中，選擇 [ **關機**]。
        2.  按 CTRL + ALT + SHIFT 鍵，然後按一下 [**關機 Windows** ] 對話方塊中的 [**否**]。

    Shell 現在已關閉，但其他所有應用程式仍在執行，包括偵錯工具。

3.  將偵錯工具設定為使用 **Windows** 目錄中的 Explorer.exe 來執行擴充 DLL。
4.  從偵錯工具執行專案。 Shell 會如往常般啟動，但偵錯工具會附加至 Shell 的進程。

## <a name="running-and-testing-shell-extensions"></a>執行和測試 Shell 擴充功能

您可以在個別的 Windows 檔案總管流程中執行和測試擴充功能，以避免停止和重新開機桌面和工作列。 當您執行和測試擴充功能時，仍然可以使用您的桌面和工作列。

若要啟用這項功能，請將下列 REG \_ DWORD 專案新增至登錄。

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  DesktopProcess = 1
```

您必須登出再重新登入，此專案才會生效。 這項設定會使桌面和工作列視窗在一個 Explorer.exe 進程中建立，而其他所有的 Explorer 和資料夾視窗則會在不同的 Explorer.exe 進程中開啟。

除了讓擴充功能的執行和測試更方便，此設定也會讓桌面更健全，因為它與 Shell 擴充功能有關。 許多這類的擴充功能 (快捷方式功能表延伸模組，例如) 將載入 nondesktop Explorer.exe 進程中。 如果此進程終止，則桌面和工作列不會受到影響，而且下一個 [Explorer] 或 [資料夾] 視窗將會重新建立終止的進程。

## <a name="unloading-the-dll"></a>卸載 DLL

Shell 會在其使用計數為零時自動卸載任何 DLL，但只有在 DLL 未使用一段時間之後。 這種非使用中的期間可能會很長，尤其是在調試 Shell 擴充 DLL 時。 您可以藉由將下列資訊新增到登錄中，縮短非使用期間。

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AlwaysUnloadDll
```

 

 



