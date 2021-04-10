---
title: 課程模組
description: 包含指定進程之模組清單的快照集包含指定進程所使用的每個模組、可執行檔或動態連結程式庫 (DLL) 的相關資訊。
ms.assetid: 1b539e2f-1326-42aa-af58-ffd7e2833b9b
keywords:
- 動態連結程式庫
- 動態連結程式庫，列舉 Dll
- 列舉
- 列舉，Dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb6a844b536d12a15202f47ad9712f3f7ef55df0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092788"
---
# <a name="module-walking"></a><span data-ttu-id="04718-107">課程模組</span><span class="sxs-lookup"><span data-stu-id="04718-107">Module Walking</span></span>

<span data-ttu-id="04718-108">包含指定進程之模組清單的快照集包含指定進程所使用的每個模組、可執行檔或動態連結程式庫 (DLL) 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="04718-108">A snapshot that includes the module list for a specified process contains information about each module, executable file, or dynamic-link library (DLL), used by the specified process.</span></span> <span data-ttu-id="04718-109">您可以使用 [**Module32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32first) 函式來取得清單中第一個模組的資訊。</span><span class="sxs-lookup"><span data-stu-id="04718-109">You can retrieve information for the first module in the list by using the [**Module32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32first) function.</span></span> <span data-ttu-id="04718-110">在取得清單中的第一個模組之後，您可以使用 [**Module32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32next) 函式，在清單中抓取後續模組的資訊。</span><span class="sxs-lookup"><span data-stu-id="04718-110">After retrieving the first module in the list, you can retrieve information for subsequent modules in the list by using the [**Module32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32next) function.</span></span> <span data-ttu-id="04718-111">**Module32First** 和 **Module32Next** 會以模組的相關資訊填入 [**MODULEENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-moduleentry32) 結構。</span><span class="sxs-lookup"><span data-stu-id="04718-111">**Module32First** and **Module32Next** fill a [**MODULEENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-moduleentry32) structure with information about the module.</span></span>

<span data-ttu-id="04718-112">您可以使用 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)函式來取得 [**Module32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32first)和 [**Module32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32next)的擴充錯誤狀態碼。</span><span class="sxs-lookup"><span data-stu-id="04718-112">You can retrieve an extended error status code for [**Module32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32first) and [**Module32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32next) by using the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span>

> [!Note]  
> <span data-ttu-id="04718-113">在 [**MODULEENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-moduleentry32)的 **th32ModuleID** 成員中指定的模組識別碼，只有在16位的視窗中才有意義。</span><span class="sxs-lookup"><span data-stu-id="04718-113">The module identifier, which is specified in the **th32ModuleID** member of [**MODULEENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-moduleentry32), only has meaning in 16-bit Windows.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="04718-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="04718-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04718-115">遍歷模組清單</span><span class="sxs-lookup"><span data-stu-id="04718-115">Traversing the Module List</span></span>](traversing-the-module-list.md)
</dt> </dl>

 

 