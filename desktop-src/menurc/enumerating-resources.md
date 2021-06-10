---
title: 列舉資源
description: 本主題討論用來取得資源清單的函式。
ms.assetid: 388deaa1-3b04-43fa-aad2-8b52376d570c
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: b978636303f3fc5bcae8c1d854289dde42ae0247
ms.sourcegitcommit: 78ce1d1e3f12ee3e08390868e5b93c034f437657
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/10/2021
ms.locfileid: "111910271"
---
# <a name="enumerating-resources"></a><span data-ttu-id="326d4-103">列舉資源</span><span class="sxs-lookup"><span data-stu-id="326d4-103">Enumerating resources</span></span>

<span data-ttu-id="326d4-104">在某些情況下，您可能會想要探索 (PE) 模組的未知可攜式可執行檔的資源內容。</span><span class="sxs-lookup"><span data-stu-id="326d4-104">In certain situations, you might want to discover the resource contents of an unknown portable executable (PE) module.</span></span> <span data-ttu-id="326d4-105">Windows SDK 提供資源列舉函式，可讓您的應用程式取得指定模組中的資源類型、名稱和語言清單。</span><span class="sxs-lookup"><span data-stu-id="326d4-105">The Windows SDK provides resource enumeration functions that enable your application to obtain lists of resource types, names, and languages in a specified module.</span></span>

* <span data-ttu-id="326d4-106">[**EnumResourceTypeW**](/windows/win32/api/Winbase/nf-winbase-enumresourcetypesw)和 [**EnumResourceTypesExW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcetypesexw)函式會提供在模組中找到的資源類型清單。</span><span class="sxs-lookup"><span data-stu-id="326d4-106">The [**EnumResourceTypeW**](/windows/win32/api/Winbase/nf-winbase-enumresourcetypesw) and [**EnumResourceTypesExW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcetypesexw) functions provide a list of resource types found in the module.</span></span>
* <span data-ttu-id="326d4-107">[**EnumResourceNamesW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcenamesw)和 [**EnumResourceNamesExW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcenamesexw)函式會提供指定類型內每個資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="326d4-107">The [**EnumResourceNamesW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcenamesw) and [**EnumResourceNamesExW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcenamesexw) functions provide the name of each resource within a given type.</span></span>
* <span data-ttu-id="326d4-108">[**EnumResourceLanguagesW**](/windows/win32/api/Winbase/nf-winbase-enumresourcelanguagesw)和 [**EnumResourceLanguagesExW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcelanguagesexw)函式會提供指定名稱和類型之每個資源的語言。</span><span class="sxs-lookup"><span data-stu-id="326d4-108">The [**EnumResourceLanguagesW**](/windows/win32/api/Winbase/nf-winbase-enumresourcelanguagesw) and [**EnumResourceLanguagesExW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcelanguagesexw) functions provide the language of each resource of a given name and type.</span></span> 

<span data-ttu-id="326d4-109">這些函式和其相關聯的回呼函式可讓您的應用程式建立模組中所有資源的清單。</span><span class="sxs-lookup"><span data-stu-id="326d4-109">These functions and their associated callback functions enable your application to create a list of all resources in a module.</span></span> <span data-ttu-id="326d4-110">這項程式會在 [建立資源清單](using-resources.md)中加以說明。</span><span class="sxs-lookup"><span data-stu-id="326d4-110">This process is described in [Creating a resource list](using-resources.md).</span></span>

## <a name="-see-also"></a><span data-ttu-id="326d4-111">-另請參閱</span><span class="sxs-lookup"><span data-stu-id="326d4-111">-see-also</span></span>

[<span data-ttu-id="326d4-112">Msistuff.exe 範例應用程式</span><span class="sxs-lookup"><span data-stu-id="326d4-112">Msistuff.exe sample app</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/sysmgmt/msi/msistuff)
