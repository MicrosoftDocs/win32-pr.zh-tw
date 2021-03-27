---
description: 檔案類型驗證程式是一種工具，可讓獨立軟體廠商 (Isv) 驗證其唯一的檔案類型是否正確執行。
ms.assetid: 1BD7452B-2DF5-44e9-9B09-C29ABFFA5F93
title: 檔案類型驗證器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8e4a588e4889241762a9d8e0567d4a4542c0255
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849206"
---
# <a name="file-type-verifier"></a><span data-ttu-id="5c62b-103">檔案類型驗證器</span><span class="sxs-lookup"><span data-stu-id="5c62b-103">File Type Verifier</span></span>

<span data-ttu-id="5c62b-104">檔案類型驗證程式是一種工具，可讓獨立軟體廠商 (Isv) 驗證其唯一的檔案類型是否正確執行。</span><span class="sxs-lookup"><span data-stu-id="5c62b-104">The File Type Verifier is a tool that enables independent software vendors (ISVs) to verify that their unique file types are implemented correctly.</span></span> <span data-ttu-id="5c62b-105">檔案類型處理常式的高品質實作為良好使用者體驗的關鍵，因為使用者會在 Windows 檔案總管中以許多方式與您的檔案格式互動。</span><span class="sxs-lookup"><span data-stu-id="5c62b-105">High quality implementations of your file type handlers are crucial for a good user experience because users interact with your file format in many ways in Windows Explorer.</span></span> <span data-ttu-id="5c62b-106">使用者可以進行全文檢索搜尋、依自訂中繼資料排序，或查看檔案格式的豐富縮圖和預覽。</span><span class="sxs-lookup"><span data-stu-id="5c62b-106">Users can do full-text searches, sort by custom metadata, or view rich thumbnails and previews of your file format.</span></span>

<span data-ttu-id="5c62b-107">如需使用檔案類型驗證器的指示，請參閱 [如何使用檔案類型驗證](how-to-use-the-file-type-verifier.md)器。</span><span class="sxs-lookup"><span data-stu-id="5c62b-107">For instructions on using the File Type Verifier, see [How To Use the File Type Verifier](how-to-use-the-file-type-verifier.md).</span></span>

## <a name="about-the-file-type-verifier-tool"></a><span data-ttu-id="5c62b-108">關於檔案類型驗證器工具</span><span class="sxs-lookup"><span data-stu-id="5c62b-108">About the File Type Verifier Tool</span></span>

<span data-ttu-id="5c62b-109">檔案類型驗證程式是 [Windows 7 SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx)中提供的一種程式。</span><span class="sxs-lookup"><span data-stu-id="5c62b-109">File Type Verifier is a program that is available as part of the [Windows 7 SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="5c62b-110">它的設計目的是協助開發人員建立自訂的 Windows [檔案類型](fa-file-types.md) ，以偵測其檔案類型的潛在問題。</span><span class="sxs-lookup"><span data-stu-id="5c62b-110">It is designed to help developers who create custom Windows [File Types](fa-file-types.md) to detect potential issues with their file types.</span></span> <span data-ttu-id="5c62b-111">雖然檔案類型驗證器只會在 Windows 7 和更新版本上執行，但是檔案類型驗證器所強制執行的規則會套用至其所檢查之功能可用的所有 Windows 版本。</span><span class="sxs-lookup"><span data-stu-id="5c62b-111">Although the File Type Verifier runs only on Windows 7 and later, the rules that the File Type Verifier enforces apply to all versions of Windows where the features it checks are available.</span></span>

<span data-ttu-id="5c62b-112">檔案類型驗證程式會對檔案類型執行數個測試，以確認它已正確註冊，而且會提供適當的 [檔案類型處理常式](fa-file-extensions.md) ，以便在 Windows 檔案總管適當地顯示檔案類型，並在適當的情況下支援為檔案內容編制索引。</span><span class="sxs-lookup"><span data-stu-id="5c62b-112">The File Type Verifier runs several tests on the file type to verify that it is properly registered, and that it provides the appropriate [File Type Handlers](fa-file-extensions.md) to display the file type properly in Windows Explorer, and when appropriate, that it supports indexing the file content.</span></span>

<span data-ttu-id="5c62b-113">檔案類型驗證器會測試下列專案：</span><span class="sxs-lookup"><span data-stu-id="5c62b-113">The File Type Verifier tests the following things:</span></span>

-   [<span data-ttu-id="5c62b-114">預覽處理常式</span><span class="sxs-lookup"><span data-stu-id="5c62b-114">Preview Handlers</span></span>](building-preview-handlers.md)
-   [<span data-ttu-id="5c62b-115">縮圖處理常式</span><span class="sxs-lookup"><span data-stu-id="5c62b-115">Thumbnail Handlers</span></span>](building-thumbnail-providers.md)
-   [<span data-ttu-id="5c62b-116">屬性處理常式</span><span class="sxs-lookup"><span data-stu-id="5c62b-116">Property Handlers</span></span>](../search/-search-3x-wds-extidx-propertyhandlers.md)
-   [<span data-ttu-id="5c62b-117">動詞處理常式</span><span class="sxs-lookup"><span data-stu-id="5c62b-117">Verb Handlers</span></span>](fa-verbs.md)
-   [<span data-ttu-id="5c62b-118">篩選 (IFilter) </span><span class="sxs-lookup"><span data-stu-id="5c62b-118">Filters (IFilter)</span></span>](../search/-search-3x-wds-extidx-filters.md)
-   [<span data-ttu-id="5c62b-119">種類關聯</span><span class="sxs-lookup"><span data-stu-id="5c62b-119">Kind Associations</span></span>](../properties/building-property-handlers-user-friendly-kind-names.md)
-   [<span data-ttu-id="5c62b-120">認知類型</span><span class="sxs-lookup"><span data-stu-id="5c62b-120">Perceived Types</span></span>](fa-perceivedtypes.md)
-   [<span data-ttu-id="5c62b-121">重要屬性</span><span class="sxs-lookup"><span data-stu-id="5c62b-121">Important Properties</span></span>](../search/-shell-systemdefinedpropertiesforfileformats.md)

## <a name="related-topics"></a><span data-ttu-id="5c62b-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="5c62b-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c62b-123">如何使用檔案類型驗證器</span><span class="sxs-lookup"><span data-stu-id="5c62b-123">How To Use the File Type Verifier</span></span>](how-to-use-the-file-type-verifier.md)
</dt> <dt>

[<span data-ttu-id="5c62b-124">應用程式註冊</span><span class="sxs-lookup"><span data-stu-id="5c62b-124">Application Registration</span></span>](app-registration.md)
</dt> <dt>

[<span data-ttu-id="5c62b-125">檔案類型</span><span class="sxs-lookup"><span data-stu-id="5c62b-125">File Types</span></span>](fa-file-types.md)
</dt> <dt>

[<span data-ttu-id="5c62b-126">檔案關聯的運作方式</span><span class="sxs-lookup"><span data-stu-id="5c62b-126">How File Associations Work</span></span>](fa-how-work.md)
</dt> <dt>

[<span data-ttu-id="5c62b-127">依檔案類型或種類的內容視圖</span><span class="sxs-lookup"><span data-stu-id="5c62b-127">Content View By File Type or Kind</span></span>](prophand-content-view.md)
</dt> <dt>

[<span data-ttu-id="5c62b-128">檔案類型處理常式</span><span class="sxs-lookup"><span data-stu-id="5c62b-128">File Type Handlers</span></span>](fa-file-extensions.md)
</dt> <dt>

[<span data-ttu-id="5c62b-129">程式設計識別碼</span><span class="sxs-lookup"><span data-stu-id="5c62b-129">Programmatic Identifiers</span></span>](fa-progids.md)
</dt> <dt>

[<span data-ttu-id="5c62b-130">認知類型</span><span class="sxs-lookup"><span data-stu-id="5c62b-130">Perceived Types</span></span>](fa-perceivedtypes.md)
</dt> <dt>

[<span data-ttu-id="5c62b-131">關聯陣列</span><span class="sxs-lookup"><span data-stu-id="5c62b-131">Association Arrays</span></span>](fa-associationarray.md)
</dt> </dl>

 

 
