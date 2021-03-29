---
description: 察覺的型別是一種檔案類型類別，可讓您將檔案類型識別為 Windows (，而應用程式) 為映射、音訊、檔或其他類型。
title: " (Windows Shell 的認知類型) "
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 56d4c495-a886-4723-88ca-5b7753398062
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e6136389c717fd4e27621a4d7f9f4cf2895c4116
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "104991862"
---
# <a name="perceived-types-the-windows-shell"></a><span data-ttu-id="8a544-103"> (Windows Shell 的認知類型) </span><span class="sxs-lookup"><span data-stu-id="8a544-103">Perceived Types (The Windows Shell)</span></span>

<span data-ttu-id="8a544-104">察覺的型別是一種檔案類型類別，可讓您將檔案類型識別為 Windows (，而應用程式) 為映射、音訊、檔或其他類型。</span><span class="sxs-lookup"><span data-stu-id="8a544-104">A perceived type is a category of file types that lets you identify your file type to Windows (and applications) as being an image, audio, document, or other type.</span></span> <span data-ttu-id="8a544-105">察覺的型別用於多種用途，包括決定資料夾類型，然後用來設定預設的視圖設定。</span><span class="sxs-lookup"><span data-stu-id="8a544-105">Perceived types are used for several purposes, including the determination of the folder type, which is then used to set the default view settings.</span></span> <span data-ttu-id="8a544-106">例如，已將已感知類型映射之檔案的資料夾，指派為縮圖的預設視圖模式。</span><span class="sxs-lookup"><span data-stu-id="8a544-106">For example, a folder full of files that are of the perceived type image is assigned a default view mode of thumbnails.</span></span>

<span data-ttu-id="8a544-107">本主題的組織方式如下：</span><span class="sxs-lookup"><span data-stu-id="8a544-107">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="8a544-108">關於認知類型</span><span class="sxs-lookup"><span data-stu-id="8a544-108">About Perceived Types</span></span>](#about-perceived-types)
-   [<span data-ttu-id="8a544-109">其他資源</span><span class="sxs-lookup"><span data-stu-id="8a544-109">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="8a544-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="8a544-110">Related topics</span></span>](#related-topics)

## <a name="about-perceived-types"></a><span data-ttu-id="8a544-111">關於認知類型</span><span class="sxs-lookup"><span data-stu-id="8a544-111">About Perceived Types</span></span>

<span data-ttu-id="8a544-112">定義為 PerceivedType 值的認知類型與檔案類型類似，不同之處在于它們是指檔案格式類型的廣泛分類，而不是特定檔案類型。</span><span class="sxs-lookup"><span data-stu-id="8a544-112">Perceived types, defined as PerceivedType values, are similar to file types except that they refer to broad categories of file format types rather than specific file types.</span></span> <span data-ttu-id="8a544-113">例如，影像、文字、音訊和壓縮都是可察覺的類型。</span><span class="sxs-lookup"><span data-stu-id="8a544-113">For example, image, text, audio, and compressed are perceived types.</span></span> <span data-ttu-id="8a544-114">檔案類型 (一般公用檔案類型) 可以被指派一個感知的型別，而且只要有適當的類型，一律會指派一個。</span><span class="sxs-lookup"><span data-stu-id="8a544-114">File types (generally public file types) can be assigned a perceived type, and should always be assigned one whenever there is one that is appropriate.</span></span> <span data-ttu-id="8a544-115">例如，圖像檔案類型 .bmp、.png、.jpg 和 .gif 也是察覺的類型影像。</span><span class="sxs-lookup"><span data-stu-id="8a544-115">For example, the image file types .bmp, .png, .jpg, and .gif are also of perceived type image.</span></span>

<span data-ttu-id="8a544-116">預設的已知類型如下：</span><span class="sxs-lookup"><span data-stu-id="8a544-116">The default perceived types are as follows:</span></span>

-   <span data-ttu-id="8a544-117">資料夾</span><span class="sxs-lookup"><span data-stu-id="8a544-117">Folder</span></span>
-   <span data-ttu-id="8a544-118">Text</span><span class="sxs-lookup"><span data-stu-id="8a544-118">Text</span></span>
-   <span data-ttu-id="8a544-119">Image</span><span class="sxs-lookup"><span data-stu-id="8a544-119">Image</span></span>
-   <span data-ttu-id="8a544-120">音訊</span><span class="sxs-lookup"><span data-stu-id="8a544-120">Audio</span></span>
-   <span data-ttu-id="8a544-121">影片</span><span class="sxs-lookup"><span data-stu-id="8a544-121">Video</span></span>
-   <span data-ttu-id="8a544-122">Compressed</span><span class="sxs-lookup"><span data-stu-id="8a544-122">Compressed</span></span>
-   <span data-ttu-id="8a544-123">文件</span><span class="sxs-lookup"><span data-stu-id="8a544-123">Document</span></span>
-   <span data-ttu-id="8a544-124">系統</span><span class="sxs-lookup"><span data-stu-id="8a544-124">System</span></span>
-   <span data-ttu-id="8a544-125">Application</span><span class="sxs-lookup"><span data-stu-id="8a544-125">Application</span></span>
-   <span data-ttu-id="8a544-126">Gamemedia</span><span class="sxs-lookup"><span data-stu-id="8a544-126">Gamemedia</span></span>
-   <span data-ttu-id="8a544-127">連絡人</span><span class="sxs-lookup"><span data-stu-id="8a544-127">Contacts</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8a544-128">其他資源</span><span class="sxs-lookup"><span data-stu-id="8a544-128">Additional Resources</span></span>

-   <span data-ttu-id="8a544-129">如需如何註冊認知類型的詳細資訊，請參閱 [應用程式註冊](app-registration.md)。</span><span class="sxs-lookup"><span data-stu-id="8a544-129">For information about how to register perceived types, see [Application Registration](app-registration.md).</span></span>
-   <span data-ttu-id="8a544-130">如需預設感知類型的清單，請參閱 [**認知**](/windows/win32/api/shtypes/ne-shtypes-perceived) 的列舉。</span><span class="sxs-lookup"><span data-stu-id="8a544-130">For a list of default perceived types, see the [**PERCEIVED**](/windows/win32/api/shtypes/ne-shtypes-perceived) enumeration.</span></span>
-   <span data-ttu-id="8a544-131">若要根據檔案的副檔名抓取檔案的認知型別，請參閱 [**AssocGetPerceivedType**](/windows/desktop/api/Shlwapi/nf-shlwapi-assocgetperceivedtype) 函數。</span><span class="sxs-lookup"><span data-stu-id="8a544-131">To retrieves a file's perceived type based on its file name extension, see the [**AssocGetPerceivedType**](/windows/desktop/api/Shlwapi/nf-shlwapi-assocgetperceivedtype) function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8a544-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="8a544-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a544-133">應用程式註冊</span><span class="sxs-lookup"><span data-stu-id="8a544-133">Application Registration</span></span>](app-registration.md)
</dt> <dt>

[<span data-ttu-id="8a544-134">檔案類型</span><span class="sxs-lookup"><span data-stu-id="8a544-134">File Types</span></span>](fa-file-types.md)
</dt> <dt>

[<span data-ttu-id="8a544-135">檔案關聯的運作方式</span><span class="sxs-lookup"><span data-stu-id="8a544-135">How File Associations Work</span></span>](fa-how-work.md)
</dt> <dt>

[<span data-ttu-id="8a544-136">依檔案類型或種類的內容視圖</span><span class="sxs-lookup"><span data-stu-id="8a544-136">Content View By File Type or Kind</span></span>](prophand-content-view.md)
</dt> <dt>

[<span data-ttu-id="8a544-137">檔案類型驗證器</span><span class="sxs-lookup"><span data-stu-id="8a544-137">File Type Verifier</span></span>](file-type-verifier.md)
</dt> <dt>

[<span data-ttu-id="8a544-138">檔案類型處理常式</span><span class="sxs-lookup"><span data-stu-id="8a544-138">File Type Handlers</span></span>](fa-file-extensions.md)
</dt> <dt>

[<span data-ttu-id="8a544-139">程式設計識別碼</span><span class="sxs-lookup"><span data-stu-id="8a544-139">Programmatic Identifiers</span></span>](fa-progids.md)
</dt> <dt>

[<span data-ttu-id="8a544-140">關聯陣列</span><span class="sxs-lookup"><span data-stu-id="8a544-140">Association Arrays</span></span>](fa-associationarray.md)
</dt> </dl>

 

 



