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
# <a name="how-to-display-a-rooted-view-of-a-file"></a><span data-ttu-id="48726-104">如何顯示檔案的根目錄檢視</span><span class="sxs-lookup"><span data-stu-id="48726-104">How to Display a Rooted View of a File</span></span>

<span data-ttu-id="48726-105">您可以使用命名空間延伸模組，讓使用者流覽檔案的內容，而不是以資料夾的形式呈現。</span><span class="sxs-lookup"><span data-stu-id="48726-105">You can use a namespace extension to allow users to browse the contents of a file rather than have it presented as a folder.</span></span> <span data-ttu-id="48726-106">這種排序的延伸通常用來顯示 [檔案類型](fa-file-types.md)的成員內容。</span><span class="sxs-lookup"><span data-stu-id="48726-106">Extensions of this sort are typically used to display the contents of the members of a [file type](fa-file-types.md).</span></span> <span data-ttu-id="48726-107">例如，檔案類型的成員可能包含多個壓縮檔案或在階層中組織的影像。</span><span class="sxs-lookup"><span data-stu-id="48726-107">For instance, the members of a file type might contain multiple compressed files or images, organized in a hierarchy.</span></span> <span data-ttu-id="48726-108">您可以改為撰寫命名空間延伸，並讓 Windows 檔案總管處理顯示，而不是撰寫可讓使用者查看這類檔案內容的應用程式。</span><span class="sxs-lookup"><span data-stu-id="48726-108">Rather than write an application to allow the user to view the contents of such a file, you can instead write a namespace extension and let Windows Explorer handle the display.</span></span>

<span data-ttu-id="48726-109">您必須使用根視圖才能讓擴充功能顯示檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="48726-109">You must use a rooted view in order to have an extension display the contents of a file.</span></span> <span data-ttu-id="48726-110">若要提供檔案類型成員的根目錄檢視，最常見的方法是定義可啟動 Explorer.exe 實例的 [快捷方式功能表動詞](context.md) 。</span><span class="sxs-lookup"><span data-stu-id="48726-110">The most common way to provide a rooted view of the members of a file type is to define a [shortcut menu verb](context.md) that launches an instance of Explorer.exe.</span></span> <span data-ttu-id="48726-111">藉由將此動詞設為預設動詞，按兩下也會開啟該檔案的根目錄檢視。</span><span class="sxs-lookup"><span data-stu-id="48726-111">By making this verb the default verb, a double-click will also open a rooted view of the file.</span></span> <span data-ttu-id="48726-112">您可以藉由 [修改](context.md)登錄來定義檔案類型之所有成員的動詞，或是藉由執行 [快捷方式功能表處理常式](context-menu-handlers.md)，以每個檔案為基礎動態定義動詞。</span><span class="sxs-lookup"><span data-stu-id="48726-112">You can either define a verb for all members of the file type by [modifying the registry](context.md), or dynamically define verbs on a file-by-file basis by implementing a [shortcut menu handler](context-menu-handlers.md).</span></span>

## <a name="instructions"></a><span data-ttu-id="48726-113">指示</span><span class="sxs-lookup"><span data-stu-id="48726-113">Instructions</span></span>


<span data-ttu-id="48726-114">下列範例說明如何使用登錄，藉由修改登錄來提供檔案類型成員的根視圖。</span><span class="sxs-lookup"><span data-stu-id="48726-114">The following example illustrates how to use the registry to provide a rooted view of the members of a file type by modifying the registry.</span></span> <span data-ttu-id="48726-115">範例登錄專案會修改 [擴充快速鍵功能表](context.md)中的其中一個範例。</span><span class="sxs-lookup"><span data-stu-id="48726-115">The sample registry entry is a modification of one of the examples in [Extending Shortcut Menus](context.md).</span></span> <span data-ttu-id="48726-116">登錄專案會將副檔名為 myp 的檔案定義為檔案類型，並使用 **流覽** 動詞命令來啟動該類型成員的根目錄檢視。</span><span class="sxs-lookup"><span data-stu-id="48726-116">The registry entries define files with an .myp file name extension as a file type, and use the **browse** verb to launch a rooted view of members of that type.</span></span>

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

<span data-ttu-id="48726-117">您可以藉由呼叫 [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) 函式，使用相同的動詞程式以程式設計方式開機檔案類型成員的根視圖。</span><span class="sxs-lookup"><span data-stu-id="48726-117">You can use the same verb to programmatically launch a rooted view of a member of the file type by calling the [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="48726-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="48726-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48726-119">指定命名空間延伸模組的位置</span><span class="sxs-lookup"><span data-stu-id="48726-119">Specifying a Namespace Extension's Location</span></span>](nse-junction.md)
</dt> <dt>

[<span data-ttu-id="48726-120">如何透過登錄開啟連接點的根目錄檢視</span><span class="sxs-lookup"><span data-stu-id="48726-120">How to Open a Rooted View of a Junction Point Through the Registry</span></span>](how-to-use-a-junction-point-to-open-a-rooted-view.md)
</dt> <dt>

[<span data-ttu-id="48726-121">如何透過快捷方式檔案開啟連接點的根目錄檢視</span><span class="sxs-lookup"><span data-stu-id="48726-121">How to Open a Rooted View of a Junction Point Through a Shortcut File</span></span>](how-to-use-a-shortcut-file-to-open-a-rooted-view.md)
</dt> <dt>

[<span data-ttu-id="48726-122">**ShellExecute**</span><span class="sxs-lookup"><span data-stu-id="48726-122">**ShellExecute**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea)
</dt> </dl>

 

 



