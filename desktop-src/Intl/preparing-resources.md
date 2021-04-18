---
description: MUI 應用程式的資源準備支援 Win32 PE 和非 Win32 PE 模型。
ms.assetid: e528dac7-c157-42d7-808d-709a4ae84f1e
title: 準備資源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4ca7655535318fa7a385993e6a55f9e7b6110ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978113"
---
# <a name="preparing-resources"></a><span data-ttu-id="ac20c-103">準備資源</span><span class="sxs-lookup"><span data-stu-id="ac20c-103">Preparing Resources</span></span>

<span data-ttu-id="ac20c-104">MUI 應用程式的資源準備支援 Win32 PE 和非 Win32 PE 模型。</span><span class="sxs-lookup"><span data-stu-id="ac20c-104">Resource preparation for a MUI application supports both Win32 PE and non-Win32 PE models.</span></span> <span data-ttu-id="ac20c-105">Win32 PE 資源是在以 PE 為基礎的檔案中提供，例如 .dll、.exe 或 sys 檔。</span><span class="sxs-lookup"><span data-stu-id="ac20c-105">Win32 PE resources are provided in PE-based files, such as .dll, .exe, or .sys files.</span></span> <span data-ttu-id="ac20c-106">非 Win32 PE 資源是由您選擇的自訂模組所提供。</span><span class="sxs-lookup"><span data-stu-id="ac20c-106">Non-Win32 PE resources are furnished in a customized module of your choosing.</span></span>

> [!Note]  
> <span data-ttu-id="ac20c-107">強烈建議您對 Win32 MUI 應用程式使用 Win32 PE 資源，因為這些資源完全受到 MUI 資源技術的支援。</span><span class="sxs-lookup"><span data-stu-id="ac20c-107">It is highly recommended for you to use Win32 PE resources for Win32 MUI applications, as these resources are completely supported by the MUI resource technology.</span></span> <span data-ttu-id="ac20c-108">您可以藉由呼叫 [**GetFileMUIPath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath) 函式（如 [尋找非 win32 pe 資源](locating-non-win32-pe-resources.md)中所述）來找出非 win32 pe 資源檔，但應用程式必須提供自己的功能來尋找和載入所需的資源。</span><span class="sxs-lookup"><span data-stu-id="ac20c-108">Non-Win32 PE resource files can be located by calling the [**GetFileMUIPath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath) function as described in [Locating Non-Win32 PE Resources](locating-non-win32-pe-resources.md), but the application must provide its own functionality to find and load the required resources.</span></span>

 

<span data-ttu-id="ac20c-109">本節包含下列主題：</span><span class="sxs-lookup"><span data-stu-id="ac20c-109">This section contains the following topics:</span></span>

-   [<span data-ttu-id="ac20c-110">建立基礎語言資源檔</span><span class="sxs-lookup"><span data-stu-id="ac20c-110">Creating the Base Language Resource File</span></span>](creating-the-base-language-resource-file.md)
-   [<span data-ttu-id="ac20c-111">使用登錄字串重新導向</span><span class="sxs-lookup"><span data-stu-id="ac20c-111">Using Registry String Redirection</span></span>](using-registry-string-redirection.md)
-   [<span data-ttu-id="ac20c-112">準備資源設定檔</span><span class="sxs-lookup"><span data-stu-id="ac20c-112">Preparing a Resource Configuration File</span></span>](preparing-a-resource-configuration-file.md)

 

 



