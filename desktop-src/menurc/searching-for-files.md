---
title: 搜尋檔案
description: 根據預設，RC 會搜尋標頭檔和資源檔 (例如，圖示和游標檔案) 先在目前的目錄中，然後在 INCLUDE 環境變數所指定的目錄中。
ms.assetid: 6c8c905d-b0f6-4665-9a93-62617ff30137
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 078a04a4cf2f3461d03c7026e0f1d73d8fd38665
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106995555"
---
# <a name="searching-for-files"></a><span data-ttu-id="e0572-103">搜尋檔案</span><span class="sxs-lookup"><span data-stu-id="e0572-103">Searching for Files</span></span>

<span data-ttu-id="e0572-104">根據預設，RC 會搜尋標頭檔和資源檔 (例如，圖示和游標檔案) 先在目前的目錄中，然後在 INCLUDE 環境變數所指定的目錄中。</span><span class="sxs-lookup"><span data-stu-id="e0572-104">By default, RC searches for header files and resource files (such as icon and cursor files) first in the current directory and then in the directories specified by the INCLUDE environment variable.</span></span> <span data-ttu-id="e0572-105"> (PATH 環境變數不會影響哪些目錄 RC 搜尋。 ) </span><span class="sxs-lookup"><span data-stu-id="e0572-105">(The PATH environment variable has no effect on which directories RC searches.)</span></span>

## <a name="adding-a-directory-to-search"></a><span data-ttu-id="e0572-106">新增要搜尋的目錄</span><span class="sxs-lookup"><span data-stu-id="e0572-106">Adding a Directory to Search</span></span>

<span data-ttu-id="e0572-107">您可以使用 **/i** 選項，將目錄新增至目錄 RC 搜尋清單。</span><span class="sxs-lookup"><span data-stu-id="e0572-107">You can use the **/i** option to add a directory to the list of directories RC searches.</span></span> <span data-ttu-id="e0572-108">然後編譯器會依下列順序搜尋目錄：</span><span class="sxs-lookup"><span data-stu-id="e0572-108">The compiler then searches the directories in the following order:</span></span>

1.  <span data-ttu-id="e0572-109">目前的目錄</span><span class="sxs-lookup"><span data-stu-id="e0572-109">The current directory</span></span>
2.  <span data-ttu-id="e0572-110">使用 **/i** 選項指定的目錄或目錄（依它們出現在 RC 命令列上的順序）</span><span class="sxs-lookup"><span data-stu-id="e0572-110">The directory or directories you specify by using the **/i** option, in the order in which they appear on the RC command line</span></span>
3.  <span data-ttu-id="e0572-111">包含環境變數所指定的目錄清單（依變數列出的順序），除非您指定 **/x** 選項</span><span class="sxs-lookup"><span data-stu-id="e0572-111">The list of directories specified by the INCLUDE environment variable, in the order in which the variable lists them, unless you specify the **/x** option</span></span>

<span data-ttu-id="e0572-112">下列範例會編譯資源定義檔案 MyApp .rc：</span><span class="sxs-lookup"><span data-stu-id="e0572-112">The following example compiles the resource-definition file MyApp.rc:</span></span>

<span data-ttu-id="e0572-113">**rc/i c： \\ 來源 \\ 內容/i d： \\ 資源 myapp. rc**</span><span class="sxs-lookup"><span data-stu-id="e0572-113">**rc /i c:\\source\\stuff /i d:\\resources myapp.rc**</span></span>

<span data-ttu-id="e0572-114">在編譯 MyApp 的腳本時，RC 會先在目前的目錄中搜尋標頭檔和資源檔，然後在 C： \\ 來源 \\ 內容和 D： \\ 資源，然後在 INCLUDE 環境變數所指定的目錄中搜尋標頭檔和資源檔。</span><span class="sxs-lookup"><span data-stu-id="e0572-114">When compiling the script MyApp.rc, RC searches for header files and resource files first in the current directory, then in C:\\Source\\Stuff and D:\\Resources, and then in the directories specified by the INCLUDE environment variable.</span></span>

## <a name="ignoring-the-include-environment-variable"></a><span data-ttu-id="e0572-115">忽略 INCLUDE 環境變數</span><span class="sxs-lookup"><span data-stu-id="e0572-115">Ignoring the INCLUDE Environment Variable</span></span>

<span data-ttu-id="e0572-116">您可以在決定要搜尋的目錄時，防止 RC 使用 INCLUDE 環境變數。</span><span class="sxs-lookup"><span data-stu-id="e0572-116">You can prevent RC from using the INCLUDE environment variable when determining the directories to search.</span></span> <span data-ttu-id="e0572-117">若要這樣做，請使用 **/x** 選項。</span><span class="sxs-lookup"><span data-stu-id="e0572-117">To do so, use the **/x** option.</span></span> <span data-ttu-id="e0572-118">然後編譯器只會搜尋目前目錄中的檔案，以及使用 **/i** 選項指定的任何目錄中的檔案。</span><span class="sxs-lookup"><span data-stu-id="e0572-118">The compiler then searches for files only in the current directory and in any directories you specify by using the **/i** option.</span></span>

<span data-ttu-id="e0572-119">下列命令會編譯腳本檔案 MyApp .rc：</span><span class="sxs-lookup"><span data-stu-id="e0572-119">The following command compiles the script file MyApp.rc:</span></span>

<span data-ttu-id="e0572-120">**rc/x/i c： \\ 來源專案 \\ myapp. rc**</span><span class="sxs-lookup"><span data-stu-id="e0572-120">**rc /x /i c:\\source\\stuff myapp.rc**</span></span>

<span data-ttu-id="e0572-121">在編譯 MyApp 的腳本時，RC 會先搜尋目前目錄中的標頭檔和資源檔，然後再搜尋 C： \\ 來源 \\ 內容。</span><span class="sxs-lookup"><span data-stu-id="e0572-121">When compiling the script MyApp.rc, RC searches for header files and resource files first in the current directory and then in C:\\Source\\Stuff.</span></span> <span data-ttu-id="e0572-122">它不會搜尋 INCLUDE 環境變數所指定的目錄。</span><span class="sxs-lookup"><span data-stu-id="e0572-122">It does not search the directories specified by the INCLUDE environment variable.</span></span>

 

 




