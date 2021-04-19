---
description: 本主題說明應用程式如何在 Windows Vista 和更新版本或舊版作業系統上載入 Win32 PE 資源模組。 包含用於釋放資源模組的呼叫。
ms.assetid: c9f126a7-315a-4856-80b3-aec02402a80e
title: 載入 Win32 PE 資源模組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3c4c1906a4fc09dc39b805e8ad5a875d96fae27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997266"
---
# <a name="loading-a-win32-pe-resource-module"></a><span data-ttu-id="8bd4f-104">載入 Win32 PE 資源模組</span><span class="sxs-lookup"><span data-stu-id="8bd4f-104">Loading a Win32 PE Resource Module</span></span>

<span data-ttu-id="8bd4f-105">本主題說明應用程式如何在 Windows Vista 和更新版本或舊版作業系統上載入 Win32 PE 資源模組。</span><span class="sxs-lookup"><span data-stu-id="8bd4f-105">This topic describes how the application loads a Win32 PE resource module on either Windows Vista and later or on an earlier operating system.</span></span> <span data-ttu-id="8bd4f-106">包含用於釋放資源模組的呼叫。</span><span class="sxs-lookup"><span data-stu-id="8bd4f-106">Calls are included for releasing the resource module.</span></span>

## <a name="load-the-resource-module-on-windows-vista-and-later"></a><span data-ttu-id="8bd4f-107">在 Windows Vista 和更新版本上載入資源模組</span><span class="sxs-lookup"><span data-stu-id="8bd4f-107">Load the Resource Module on Windows Vista and Later</span></span>

<span data-ttu-id="8bd4f-108">在 Windows Vista 和更新版本中，應用程式會使用對 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 或 [**LoadLibraryEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa)的呼叫來載入資源模組。</span><span class="sxs-lookup"><span data-stu-id="8bd4f-108">On Windows Vista and later, the application loads the resource module using a call to [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) or [**LoadLibraryEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa).</span></span> <span data-ttu-id="8bd4f-109">建議的作業是呼叫此函式，並指定兩個旗標。</span><span class="sxs-lookup"><span data-stu-id="8bd4f-109">The recommended operation is to call this function with both flags specified.</span></span> <span data-ttu-id="8bd4f-110">以下是根據系統語言設定載入模組的應用程式程式碼範例。</span><span class="sxs-lookup"><span data-stu-id="8bd4f-110">The following is an example of application code that loads a module based on system language settings.</span></span>


```C++
HMODULE hResModule = LoadLibraryEx(TEXT("Mymodule.dll"), 0,
                                   LOAD_LIBRARY_AS_DATAFILE | LOAD_LIBRARY_AS_IMAGE_RESOURCE);
// ... insert code here to call resource loading functions ...
FreeLibrary(hResModule);
```



## <a name="load-the-resource-module-on-pre-windows-vista-operating-systems"></a><span data-ttu-id="8bd4f-111">在 Windows Vista 之前的作業系統上載入資源模組</span><span class="sxs-lookup"><span data-stu-id="8bd4f-111">Load the Resource Module on Pre-Windows Vista Operating Systems</span></span>

<span data-ttu-id="8bd4f-112">在 Windows Vista 之前版本的作業系統上，應用程式會根據與目標作業系統相容的語言設定，以及 Windows Vista 和更新版本來載入資源模組。</span><span class="sxs-lookup"><span data-stu-id="8bd4f-112">On pre-Windows Vista operating systems, the application loads a resource module based on a language setting that is compatible with the target operating system, as well as Windows Vista and later.</span></span> <span data-ttu-id="8bd4f-113">針對此類型的模組載入，應用程式必須呼叫 MUI 函式 [**LoadMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-loadmuilibrarya) 和 [**FreeMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-freemuilibrary)。</span><span class="sxs-lookup"><span data-stu-id="8bd4f-113">For this type of module loading, the application must call the MUI functions [**LoadMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-loadmuilibrarya) and [**FreeMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-freemuilibrary).</span></span>


```C++
#include "MuiLoad.h"
HMODULE hResModule = LoadMUILibrary(TEXT("Mymodule.dll"), MUI_LANGUAGE_NAME, 0);
// ... insert code here to call resource loading functions ...
FreeMUILibrary(hResModule);
```



## <a name="related-topics"></a><span data-ttu-id="8bd4f-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="8bd4f-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8bd4f-115">尋找 Win32 PE 資源</span><span class="sxs-lookup"><span data-stu-id="8bd4f-115">Locating Win32 PE Resources</span></span>](locating-win32-pe-resources.md)
</dt> <dt>

[<span data-ttu-id="8bd4f-116">MUI： (Windows Vista) 的 Application-Specific 設定範例 </span><span class="sxs-lookup"><span data-stu-id="8bd4f-116">MUI: Application-Specific Settings Sample (Windows Vista)</span></span>](mui-application-specific-settings-sample-vista.md)
</dt> <dt>

[<span data-ttu-id="8bd4f-117">MUI： (Windows Vista 之前的 Application-Specific 設定範例) </span><span class="sxs-lookup"><span data-stu-id="8bd4f-117">MUI: Application-Specific Settings Sample (Pre-Windows Vista)</span></span>](mui-application-specific-settings-sample-pre-vista.md)
</dt> </dl>

 

 
