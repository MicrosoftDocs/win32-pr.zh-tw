---
description: 協力廠商可以建立應用程式，以程式設計方式查詢資料的索引，並可延伸 Windows Search 從自訂檔案格式和資料存放區索引資料。
ms.assetid: 70046df0-ce48-472d-b24b-8231ea3a43c0
title: Windows Search 開發人員指南
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61593f47e081059966936a99a7d2baea114df92a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468808"
---
# <a name="windows-search-developers-guide"></a><span data-ttu-id="85f3b-103">Windows Search 開發人員指南</span><span class="sxs-lookup"><span data-stu-id="85f3b-103">Windows Search Developer's Guide</span></span>

<span data-ttu-id="85f3b-104">協力廠商可以建立應用程式，以程式設計方式查詢資料的索引，並可延伸 Windows Search 從自訂檔案格式和資料存放區索引資料。</span><span class="sxs-lookup"><span data-stu-id="85f3b-104">Third parties can create applications that query the index for data programmatically and can extend Windows Search to index data from custom file formats and data stores.</span></span> <span data-ttu-id="85f3b-105">若要建立 Windows Search 的應用程式，協力廠商開發人員必須先將 Shell 資料存放區實作為，才能達到合理的使用者體驗。</span><span class="sxs-lookup"><span data-stu-id="85f3b-105">To create Windows Search applications, third-party developers must first implement a Shell data store to a achieve a reasonable user experience.</span></span> <span data-ttu-id="85f3b-106">如需詳細資訊，請參閱 [執行基本資料夾物件介面](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="85f3b-106">For more information, see [Implementing the Basic Folder Object Interfaces](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).</span></span>

<span data-ttu-id="85f3b-107">您也必須下載 Windows Search 程式庫的 [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="85f3b-107">You must also download the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) for the Windows Search libraries.</span></span> <span data-ttu-id="85f3b-108">[WINDOWS SEARCH SDK 範例](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8)包含實用的程式碼範例，以及使用 managed 程式碼進行開發的 interopability 元件。</span><span class="sxs-lookup"><span data-stu-id="85f3b-108">The [Windows Search SDK Samples](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8) contains useful code samples and an interopability assembly for developing with managed code.</span></span> <span data-ttu-id="85f3b-109">如需使用程式碼範例的詳細資訊，請參閱 [Windows Search 程式碼範例](-search-3x-wds-sampleentry.md)。</span><span class="sxs-lookup"><span data-stu-id="85f3b-109">For more information on using the code samples, see [Windows Search Code Samples](-search-3x-wds-sampleentry.md).</span></span>

<span data-ttu-id="85f3b-110">本節的組織方式如下：</span><span class="sxs-lookup"><span data-stu-id="85f3b-110">This section is organized as follows:</span></span>

- [<span data-ttu-id="85f3b-111">管理索引</span><span class="sxs-lookup"><span data-stu-id="85f3b-111">Managing the Index</span></span>](-search-3x-wds-mngidx-overview.md)
- [<span data-ttu-id="85f3b-112">以程式設計方式查詢索引</span><span class="sxs-lookup"><span data-stu-id="85f3b-112">Querying the Index Programmatically</span></span>](-search-3x-wds-qryidx-overview.md)
- [<span data-ttu-id="85f3b-113">擴充索引</span><span class="sxs-lookup"><span data-stu-id="85f3b-113">Extending the Index</span></span>](-search-3x-wds-extidx-overview.md)
- [<span data-ttu-id="85f3b-114">擴充語言資源</span><span class="sxs-lookup"><span data-stu-id="85f3b-114">Extending Language Resources</span></span>](extending-language-resources-in-windows-search.md)

## <a name="additional-resources"></a><span data-ttu-id="85f3b-115">其他資源</span><span class="sxs-lookup"><span data-stu-id="85f3b-115">Additional Resources</span></span>

- <span data-ttu-id="85f3b-116">如需有關搜尋技術的社區支援問題和討論訊息板，請參閱 [MSDN 論壇： Windows 桌面搜尋開發](https://social.msdn.microsoft.com/Forums/windowsdesktopsearchdevelopment/threads)。</span><span class="sxs-lookup"><span data-stu-id="85f3b-116">For community-supported question and discussion message boards on Search technologies, see [MSDN Forum: Windows Desktop Search Development](https://social.msdn.microsoft.com/Forums/windowsdesktopsearchdevelopment/threads).</span></span>
- <span data-ttu-id="85f3b-117">若要下載搜尋程式碼範例：</span><span class="sxs-lookup"><span data-stu-id="85f3b-117">To download the Search Code Samples:</span></span>
  - [<span data-ttu-id="85f3b-118">Windows Search 範例</span><span class="sxs-lookup"><span data-stu-id="85f3b-118">Windows Search Samples</span></span>](-search-samples-ovw.md)
- <span data-ttu-id="85f3b-119">若要下載 Windows SDK：</span><span class="sxs-lookup"><span data-stu-id="85f3b-119">To download the Windows SDK:</span></span>
  - <span data-ttu-id="85f3b-120">針對 Windows 10： [WINDOWS 10 SDK](https://developer.microsoft.com/windows/downloads/windows-10-sdk)</span><span class="sxs-lookup"><span data-stu-id="85f3b-120">For Windows 10: [Windows 10 SDK](https://developer.microsoft.com/windows/downloads/windows-10-sdk)</span></span>
  - <span data-ttu-id="85f3b-121">適用于 windows 7： [適用于 windows 7 和 .NET Framework 的 Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx)</span><span class="sxs-lookup"><span data-stu-id="85f3b-121">For Windows 7: [Windows SDK for Windows 7 and .NET Framework](https://msdn.microsoft.com/windowsvista/bb980924.aspx)</span></span>

## <a name="related-topics"></a><span data-ttu-id="85f3b-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="85f3b-122">Related topics</span></span>

[<span data-ttu-id="85f3b-123">Windows Search 概觀</span><span class="sxs-lookup"><span data-stu-id="85f3b-123">Windows Search Overview</span></span>](-search-3x-wds-overview.md)

[<span data-ttu-id="85f3b-124">Windows Search 參考</span><span class="sxs-lookup"><span data-stu-id="85f3b-124">Windows Search Reference</span></span>](-search-reference-entry-page.md)

[<span data-ttu-id="85f3b-125">Windows Search 程式碼範例</span><span class="sxs-lookup"><span data-stu-id="85f3b-125">Windows Search Code Samples</span></span>](-search-samples-ovw.md)

[<span data-ttu-id="85f3b-126">Windows 中的同盟搜尋</span><span class="sxs-lookup"><span data-stu-id="85f3b-126">Federated Search in Windows</span></span>](-search-federated-search-overview.md)

[<span data-ttu-id="85f3b-127">相關搜尋技術</span><span class="sxs-lookup"><span data-stu-id="85f3b-127">Related Search Technologies</span></span>](-search-3x-wds-sampleentry.md)

[<span data-ttu-id="85f3b-128">Windows Search 詞彙</span><span class="sxs-lookup"><span data-stu-id="85f3b-128">Windows Search Glossary</span></span>](search-glossary.md)
