---
title: 中繼資料
description: 基於這個 SDK 的目的，中繼資料是描述 ASF 檔案或檔案內容的資訊。
ms.assetid: 4ccca0c3-52c5-4291-bdab-354705db9b10
keywords:
- Windows Media Format SDK，中繼資料總覽
- Advanced Systems Format (ASF) ，中繼資料總覽
- ASF (Advanced Systems Format) ，中繼資料總覽
- 中繼資料，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 552e968ab4a5908ec1a2a80012ecba3a5b959c6c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311252"
---
# <a name="metadata"></a><span data-ttu-id="ef38c-107">中繼資料</span><span class="sxs-lookup"><span data-stu-id="ef38c-107">Metadata</span></span>

<span data-ttu-id="ef38c-108">基於這個 SDK 的目的，中繼資料是描述 ASF 檔案或檔案內容的資訊。</span><span class="sxs-lookup"><span data-stu-id="ef38c-108">Metadata, for the purposes of this SDK, is information that describes an ASF file or the contents of the file.</span></span> <span data-ttu-id="ef38c-109">ASF 檔案的標頭區段包含與該檔案相關聯的所有中繼資料。</span><span class="sxs-lookup"><span data-stu-id="ef38c-109">The header section of an ASF file contains all of the metadata associated with that file.</span></span> <span data-ttu-id="ef38c-110">ASF 檔案中中繼資料的個別專案稱為屬性。</span><span class="sxs-lookup"><span data-stu-id="ef38c-110">Individual items of metadata in an ASF file are called attributes.</span></span> <span data-ttu-id="ef38c-111">每個屬性都有名稱和值。</span><span class="sxs-lookup"><span data-stu-id="ef38c-111">Each attribute has a name and a value.</span></span> <span data-ttu-id="ef38c-112">在本檔中，全域常數用來識別屬性。</span><span class="sxs-lookup"><span data-stu-id="ef38c-112">Throughout this documentation, global constants are used to identify attributes.</span></span> <span data-ttu-id="ef38c-113">例如，ASF 檔案的標題會儲存在 **g \_ wszWMTitle** 屬性中。</span><span class="sxs-lookup"><span data-stu-id="ef38c-113">For example, the title of an ASF file is stored in the **g\_wszWMTitle** attribute.</span></span>

<span data-ttu-id="ef38c-114">Windows Media Format SDK 中定義了數個屬性，可處理最常見的中繼資料需求。</span><span class="sxs-lookup"><span data-stu-id="ef38c-114">A number of attributes are defined in the Windows Media Format SDK to handle the most common metadata needs.</span></span> <span data-ttu-id="ef38c-115">此外，您還可以建立自己的屬性。</span><span class="sxs-lookup"><span data-stu-id="ef38c-115">In addition, you can create your own attributes.</span></span> <span data-ttu-id="ef38c-116">不過，您應該在命名自訂屬性時小心，因為其他應用程式開發人員可以使用相同的名稱，而且可能會發生衝突。</span><span class="sxs-lookup"><span data-stu-id="ef38c-116">You should take care when naming custom attributes, however, because other application developers can use the same names, and conflicts can occur.</span></span>

<span data-ttu-id="ef38c-117">有些屬性是由 SDK 設定，無法手動變更。</span><span class="sxs-lookup"><span data-stu-id="ef38c-117">Some attributes are set by the SDK and cannot be changed manually.</span></span> <span data-ttu-id="ef38c-118">例如，當您為 ASF 檔案編制索引時，SDK 會設定 **g \_ wszWMSeekable** 屬性，以顯示現在可以從任何指定的點讀取該檔案。</span><span class="sxs-lookup"><span data-stu-id="ef38c-118">For example, when you index an ASF file, the SDK sets the **g\_wszWMSeekable** attribute to show that the file can now be read from any specified point.</span></span>

<span data-ttu-id="ef38c-119">其他屬性則是單純的資訊，必須手動設定。</span><span class="sxs-lookup"><span data-stu-id="ef38c-119">Other attributes are purely informational and must be set manually.</span></span> <span data-ttu-id="ef38c-120">例如，如果您想要追蹤檔案的作者，您應該設定 **g \_ wszWMAuthor**。</span><span class="sxs-lookup"><span data-stu-id="ef38c-120">For example, if you want to keep track of the author of a file, you should set **g\_wszWMAuthor**.</span></span>

<span data-ttu-id="ef38c-121">Windows Media Format SDK 提供適用于整個檔案的屬性，以及適用于個別資料流程的屬性支援。</span><span class="sxs-lookup"><span data-stu-id="ef38c-121">The Windows Media Format SDK provides support for attributes that apply to the entire file, and attributes that apply to individual streams.</span></span>

<span data-ttu-id="ef38c-122">您可以使用 Windows Media Format SDK 來編輯 MP3 檔案中的中繼資料，不過，您應該一律在 MP3 檔中使用 ID3 相容的屬性，以維持與其他 MP3 操作程式的相容性。</span><span class="sxs-lookup"><span data-stu-id="ef38c-122">You can use the Windows Media Format SDK to edit the metadata in MP3 files, though you should always use ID3-compliant attributes in MP3 files to maintain compatibility with other MP3 manipulation programs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ef38c-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="ef38c-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef38c-124">**概念**</span><span class="sxs-lookup"><span data-stu-id="ef38c-124">**Concepts**</span></span>](concepts.md)
</dt> <dt>

[<span data-ttu-id="ef38c-125">**中繼資料編輯器物件**</span><span class="sxs-lookup"><span data-stu-id="ef38c-125">**Metadata Editor Object**</span></span>](metadata-editor-object.md)
</dt> <dt>

[<span data-ttu-id="ef38c-126">**中繼資料功能**</span><span class="sxs-lookup"><span data-stu-id="ef38c-126">**Metadata Features**</span></span>](metadata-features.md)
</dt> <dt>

[<span data-ttu-id="ef38c-127">**使用中繼資料**</span><span class="sxs-lookup"><span data-stu-id="ef38c-127">**Working with Metadata**</span></span>](working-with-metadata.md)
</dt> </dl>

 

 




