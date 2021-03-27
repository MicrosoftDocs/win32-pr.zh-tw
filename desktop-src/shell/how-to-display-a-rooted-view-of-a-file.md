---
description: 您可以使用命名空間延伸模組，讓使用者流覽檔案的內容，而不是以資料夾的形式呈現。 這種排序的延伸通常用來顯示檔案類型的成員內容。
title: 如何顯示檔案的根目錄檢視
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30ee16f3ce50cd79800dd98aa53256591d1f79d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849196"
---
# <a name="how-to-display-a-rooted-view-of-a-file"></a>如何顯示檔案的根目錄檢視

您可以使用命名空間延伸模組，讓使用者流覽檔案的內容，而不是以資料夾的形式呈現。 這種排序的延伸通常用來顯示 [檔案類型](fa-file-types.md)的成員內容。 例如，檔案類型的成員可能包含多個壓縮檔案或在階層中組織的影像。 您可以改為撰寫命名空間延伸，並讓 Windows 檔案總管處理顯示，而不是撰寫可讓使用者查看這類檔案內容的應用程式。

您必須使用根視圖才能讓擴充功能顯示檔案的內容。 若要提供檔案類型成員的根目錄檢視，最常見的方法是定義可啟動 Explorer.exe 實例的 [快捷方式功能表動詞](context.md) 。 藉由將此動詞設為預設動詞，按兩下也會開啟該檔案的根目錄檢視。 您可以藉由 [修改](context.md)登錄來定義檔案類型之所有成員的動詞，或是藉由執行 [快捷方式功能表處理常式](context-menu-handlers.md)，以每個檔案為基礎動態定義動詞。

## <a name="instructions"></a>指示


下列範例說明如何使用登錄，藉由修改登錄來提供檔案類型成員的根視圖。 範例登錄專案會修改 [擴充快速鍵功能表](context.md)中的其中一個範例。 登錄專案會將副檔名為 myp 的檔案定義為檔案類型，並使用 **流覽** 動詞命令來啟動該類型成員的根目錄檢視。

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   MyProgram.1
      (Default) = MyProgram Application
      Shell
         (Default) = browse
         browse
            command
               (Default) = %SYSTEMROOT%\explorer.exe /e,/root,{Extension CLSID}, "%1"
```

您可以藉由呼叫 [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) 函式，使用相同的動詞程式以程式設計方式開機檔案類型成員的根視圖。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[指定命名空間延伸模組的位置](nse-junction.md)
</dt> <dt>

[如何透過登錄開啟連接點的根目錄檢視](how-to-use-a-junction-point-to-open-a-rooted-view.md)
</dt> <dt>

[如何透過快捷方式檔案開啟連接點的根目錄檢視](how-to-use-a-shortcut-file-to-open-a-rooted-view.md)
</dt> <dt>

[**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea)
</dt> </dl>

 

 



