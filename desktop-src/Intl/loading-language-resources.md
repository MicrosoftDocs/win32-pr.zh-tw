---
description: 正在載入語言資源
ms.assetid: 2655b2a3-2926-43f6-aef4-8b756c02a162
title: 正在載入語言資源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af6917f03e773a470288fb4c9577812e0b38868b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104321099"
---
# <a name="loading-language-resources"></a><span data-ttu-id="1f38a-103">正在載入語言資源</span><span class="sxs-lookup"><span data-stu-id="1f38a-103">Loading Language Resources</span></span>

<span data-ttu-id="1f38a-104">您的應用程式會使用標準資源載入函式的呼叫（例如， [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage)、 [**loadstring 時**](/windows/win32/api/winuser/nf-winuser-loadstringa)和 [**LoadImage**](/windows/win32/api/winuser/nf-winuser-loadimagea)）載入所有使用者介面語言資源，而非特定重新導向的登錄字串。</span><span class="sxs-lookup"><span data-stu-id="1f38a-104">Your application loads all user interface language resources, other than certain redirected registry strings, using calls to standard resource loading functions, for example, [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage), [**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa), and [**LoadImage**](/windows/win32/api/winuser/nf-winuser-loadimagea).</span></span> <span data-ttu-id="1f38a-105">許多資源載入函式已經過修改，可自動從特定語言的資源檔載入資源，將資源視為包含在 LN 檔案中。</span><span class="sxs-lookup"><span data-stu-id="1f38a-105">Many resource loading functions have been modified to load resources from language-specific resource files automatically, treating resources as if they are contained in the LN file.</span></span> <span data-ttu-id="1f38a-106">下列範例說明如何使用 **loadstring 時** ，為遵循系統語言設定的應用程式載入語言字串。</span><span class="sxs-lookup"><span data-stu-id="1f38a-106">The following example illustrates the use of **LoadString** to load language strings for an application that follows system language settings.</span></span>


```C++
HMODULE hResModule = LoadLibraryEx(TEXT("Mymodule.dll"), 0,
                                   LOAD_LIBRARY_AS_DATAFILE | LOAD_LIBRARY_AS_IMAGE_RESOURCE);
// ...
LoadString(hResModule, myID, lpBuffer, cbBufferSize);
// ...
FreeLibrary(hResModule);
```



## <a name="related-topics"></a><span data-ttu-id="1f38a-107">相關主題</span><span class="sxs-lookup"><span data-stu-id="1f38a-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f38a-108">尋找 Win32 PE 資源</span><span class="sxs-lookup"><span data-stu-id="1f38a-108">Locating Win32 PE Resources</span></span>](locating-win32-pe-resources.md)
</dt> </dl>

 

 
