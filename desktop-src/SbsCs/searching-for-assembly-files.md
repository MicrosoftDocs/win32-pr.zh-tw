---
description: 搜尋元件檔
ms.assetid: 6e6c1104-5cde-4c07-9ee2-d87062675dac
title: 搜尋元件檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d7be73b162ea41fd9eeb0a042a1fc2e202b8115
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194535"
---
# <a name="searching-for-assembly-files"></a><span data-ttu-id="a21c3-103">搜尋元件檔</span><span class="sxs-lookup"><span data-stu-id="a21c3-103">Searching for Assembly Files</span></span>

<span data-ttu-id="a21c3-104">啟用內容可協助載入器尋找元件檔。</span><span class="sxs-lookup"><span data-stu-id="a21c3-104">Activation contexts can help the loader find assembly files.</span></span> <span data-ttu-id="a21c3-105">當載入器搜尋要依名稱載入的檔案時，它會先搜尋具有指定名稱的檔案，該檔案是由目前作用中啟用內容的成員所參考。</span><span class="sxs-lookup"><span data-stu-id="a21c3-105">When the loader searches for a file to load by name, it first searches for files with the specified name that are referenced by assemblies that are members of the currently active activation context.</span></span> <span data-ttu-id="a21c3-106">對 [**SearchPath**](/windows/desktop/api/processenv/nf-processenv-searchpathw) 的呼叫也會先找到這些檔案。</span><span class="sxs-lookup"><span data-stu-id="a21c3-106">A call to [**SearchPath**](/windows/desktop/api/processenv/nf-processenv-searchpathw) also locates these files first.</span></span> <span data-ttu-id="a21c3-107">具有指定名稱和目前啟用內容的檔案，會在本機目錄或 PATH 環境變數中具有名稱的檔案之前找到並載入。</span><span class="sxs-lookup"><span data-stu-id="a21c3-107">Files having the specified name and the current activation context are found and loaded before files with the name in the local directory or in the PATH environment variable.</span></span> <span data-ttu-id="a21c3-108">這表示當您建立資訊清單時，您需要列出所有您打算搭配 **SearchPath**、 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)或靜態匯入使用的檔案。</span><span class="sxs-lookup"><span data-stu-id="a21c3-108">This means that when you create manifests you need to list all files you plan to use with **SearchPath**, [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya), or static imports.</span></span>

<span data-ttu-id="a21c3-109">請注意，使用 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) 或其他未搜尋檔案的函式時，不會自動找到這些檔案。</span><span class="sxs-lookup"><span data-stu-id="a21c3-109">Note that these files are not automatically located when using [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) or other functions that do not search for files.</span></span> <span data-ttu-id="a21c3-110">若要將這些檔案與 **CreateFile** 搭配使用，請先使用 [**SearchPath**](/windows/desktop/api/processenv/nf-processenv-searchpathw) 來尋找隔離檔案的路徑，然後在傳回的路徑上使用 **CreateFile** 。</span><span class="sxs-lookup"><span data-stu-id="a21c3-110">To use these files with **CreateFile**, use [**SearchPath**](/windows/desktop/api/processenv/nf-processenv-searchpathw) first to find the path to the isolated file, and then use **CreateFile** on the returned path.</span></span>

<span data-ttu-id="a21c3-111">這種檔案搜尋方法有助於將隔離的應用程式分開，因為具有相同名稱的多個檔案，則只會與不同版本號碼的元件關聯不同。</span><span class="sxs-lookup"><span data-stu-id="a21c3-111">This method of file searching helps to keep isolated applications separate because multiple files with the same name can then differ only by their association with assemblies of different version numbers.</span></span> <span data-ttu-id="a21c3-112">作業系統可以在檔案作業期間找到正確的檔案。</span><span class="sxs-lookup"><span data-stu-id="a21c3-112">The operating system can find the correct file to use during file operations.</span></span>

<span data-ttu-id="a21c3-113">如果 DLL 使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)以這種方式載入，則會呼叫該 dll 的進入)  (點，而原始啟用內容會保持作用中，但除非 DLL 本身包含特定資源識別碼 (ISOLATIONAWARE \_ 資訊清單 \_ 資源 \_ 識別碼或 2) </span><span class="sxs-lookup"><span data-stu-id="a21c3-113">If a DLL is loaded in this manner using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya), that DLL's entry point (DllMain) is called while the original activation context is kept active, except if the DLL itself contains a manifest at a certain resource ID (ISOLATIONAWARE\_MANIFEST\_RESOURCE\_ID, or 2)</span></span>

 

 
