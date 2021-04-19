---
title: 預留位置檔案
description: 預留位置檔案
ms.assetid: E14655DA-CEA0-4106-B882-C9E9116FC234
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93c15037b0daec7a6521a299b6c4587c956e0be3
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/10/2020
ms.locfileid: "106966895"
---
# <a name="placeholder-files"></a><span data-ttu-id="4c99c-103">預留位置檔案</span><span class="sxs-lookup"><span data-stu-id="4c99c-103">Placeholder files</span></span>

## <a name="platform"></a><span data-ttu-id="4c99c-104">平台</span><span class="sxs-lookup"><span data-stu-id="4c99c-104">Platform</span></span>

<span data-ttu-id="4c99c-105">**用戶端-** Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="4c99c-105">**Clients -** Windows 8.1</span></span>  
<span data-ttu-id="4c99c-106">**伺服器-** Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="4c99c-106">**Servers -** Windows Server 2012 R2</span></span>  

## <a name="description"></a><span data-ttu-id="4c99c-107">Description</span><span class="sxs-lookup"><span data-stu-id="4c99c-107">Description</span></span>

<span data-ttu-id="4c99c-108">預留位置檔案可讓使用者不論連線能力，都能看到及管理 Microsoft OneDrive 檔案。</span><span class="sxs-lookup"><span data-stu-id="4c99c-108">Placeholder files enable users to view and manage Microsoft OneDrive files regardless of connectivity.</span></span> <span data-ttu-id="4c99c-109">預留位置檔案代表 OneDrive 命名空間，即使檔案不是在本機快取。</span><span class="sxs-lookup"><span data-stu-id="4c99c-109">Placeholder files represent the OneDrive namespace, even when files are not cached locally.</span></span> <span data-ttu-id="4c99c-110">它們包含相片的檔案中繼資料和縮圖影像。</span><span class="sxs-lookup"><span data-stu-id="4c99c-110">They contain file metadata and thumbnail images of photos.</span></span>

## <a name="manifestation"></a><span data-ttu-id="4c99c-111">表現</span><span class="sxs-lookup"><span data-stu-id="4c99c-111">Manifestation</span></span>

<span data-ttu-id="4c99c-112">對於使用者和開發人員而言，預留位置檔案的外觀和行為幾乎與本機檔案相同。</span><span class="sxs-lookup"><span data-stu-id="4c99c-112">To end users and developers, placeholder files look and behave almost the same as the local files.</span></span>

<span data-ttu-id="4c99c-113">如果您的應用程式使用 [一般檔案] 對話方塊來列舉檔案系統，則您的應用程式不會受到影響。</span><span class="sxs-lookup"><span data-stu-id="4c99c-113">If your app uses the Common File Dialog to enumerate the file system, your app will not be impacted.</span></span> <span data-ttu-id="4c99c-114">當使用者嘗試從 [一般/file] 對話方塊開啟檔案時，將會下載檔案內容，並將其傳遞至您的應用程式。</span><span class="sxs-lookup"><span data-stu-id="4c99c-114">When the user tries to open the file from the common /file Dialog, the file content will be downloaded and will be passed to your app.</span></span>

<span data-ttu-id="4c99c-115">如果您的應用程式直接存取檔案系統，則您的應用程式可以使用下列指導方針來利用預留位置檔案。</span><span class="sxs-lookup"><span data-stu-id="4c99c-115">If your app accesses the file system directly, then your app may take advantage of the placeholder files by using the guidelines below.</span></span>

## <a name="solution"></a><span data-ttu-id="4c99c-116">解決方法</span><span class="sxs-lookup"><span data-stu-id="4c99c-116">Solution</span></span>

-   <span data-ttu-id="4c99c-117">根據屬性，根據慣例隱藏預留位置</span><span class="sxs-lookup"><span data-stu-id="4c99c-117">Placeholders are hidden by convention based on attributes</span></span>
-   <span data-ttu-id="4c99c-118">使用重新分析標記識別項 IO 重新 \_ 分析 \_ 標記 \_ 檔案 \_ 預留位置來識別預留位置</span><span class="sxs-lookup"><span data-stu-id="4c99c-118">Identify placeholders using reparse tag ID IO\_REPARSE\_TAG\_FILE\_PLACEHOLDER</span></span>

<span data-ttu-id="4c99c-119">使用 shell 資料模型來取得無縫行為：</span><span class="sxs-lookup"><span data-stu-id="4c99c-119">Use the shell data model for seamless behavior:</span></span>

-   <span data-ttu-id="4c99c-120">使用 SHCreateItemFromParsingName () 建立 shell 專案</span><span class="sxs-lookup"><span data-stu-id="4c99c-120">Use SHCreateItemFromParsingName() to create a shell item</span></span>
-   <span data-ttu-id="4c99c-121">使用 IShellItem：： BindToHandler (BHID stream 來系結至資料流程 \_) </span><span class="sxs-lookup"><span data-stu-id="4c99c-121">Bind to the stream using IShellItem::BindToHandler(BHID\_Stream)</span></span>
-   <span data-ttu-id="4c99c-122">屬性存取 (IShellItem2：： GetPropertyHandler) 的使用者屬性處理常式</span><span class="sxs-lookup"><span data-stu-id="4c99c-122">User property handler for property access (IShellItem2::GetPropertyHandler)</span></span>
-   <span data-ttu-id="4c99c-123">使用者介面 thumbnailhandler 取得預留位置的縮圖影像</span><span class="sxs-lookup"><span data-stu-id="4c99c-123">User shell thumbnailhandler to get thumbnail images for placeholders</span></span>
-   <span data-ttu-id="4c99c-124">\*如果動詞透過 BindToHandler 系結至資料流程，請在您的動詞執行上指定 SupportedProtocols =</span><span class="sxs-lookup"><span data-stu-id="4c99c-124">Specify SupportedProtocols=\* on your verb implementation if the verb binds to the stream via BindToHandler</span></span>


```
#include <winnth> //for IO_REPARSE_TAG_FILE_PLACEHOLDER
//  Helper that indicates this is a 
bool IsFilePlaceholder(WIN32_FIND_DATA const &findData)
{
  return (findData.dwFileAttributes & FILE_ATTRIBUTE_REPARSE_POINT) &&
    (findData.dwReserved0 == IO_REPARSE_TAG_FILE_PLACEHOLDER);
}
bool IsFilePlaceholder(_In_PCWSTR filePath)
{
  bool isPlaceholder = false;
  WIN32_FIND_DATA findData;
  HANDLE hFind = FindFirstFile(filePath, &findData);
  if (hFind ! = INVALID_HANDLE_VALUE)
  {
    isPlaceholder = (findData.dwFileAttributes &    FILE_ATTRIBUTE_REPARSE_POINT) &&
    (findData.dwReserved0 == IO_REPARSE_TAG_FILE_PLACEHOLDER);
    FindClose(hFind);
  }
  Return isPlaceholder;
}
```



 

 




