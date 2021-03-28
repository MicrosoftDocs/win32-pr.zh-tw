---
description: 有數種影像檔案格式可讓您儲存中繼資料和影像。
ms.assetid: 1eba4b91-bbf4-4f82-b2d7-65f331a84859
title: 影像屬性標記常數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dea9a6c3b8ea7ad9f0693032d3bc779bc414d9b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972916"
---
# <a name="image-property-tag-constants"></a><span data-ttu-id="58364-103">影像屬性標記常數</span><span class="sxs-lookup"><span data-stu-id="58364-103">Image Property Tag Constants</span></span>

<span data-ttu-id="58364-104">有數種影像檔案格式可讓您儲存中繼資料和影像。</span><span class="sxs-lookup"><span data-stu-id="58364-104">Several image file formats enable you to store metadata along with an image.</span></span> <span data-ttu-id="58364-105">中繼資料是關於影像的資訊，例如標題、寬度、相機型號和演出者。</span><span class="sxs-lookup"><span data-stu-id="58364-105">Metadata is information about an image, for example, title, width, camera model, and artist.</span></span> <span data-ttu-id="58364-106">Windows GDI + 提供統一的方式，可讓您以標記的影像檔案格式儲存和取出影像檔案的中繼資料， (TIFF) 、JPEG、便攜網狀圖形 (PNG) 和交換影像檔案 (EXIF) 格式。</span><span class="sxs-lookup"><span data-stu-id="58364-106">Windows GDI+ provides a uniform way of storing and retrieving metadata from image files in the Tagged Image File Format (TIFF), JPEG, Portable Network Graphics (PNG), and Exchangeable Image File (EXIF) formats.</span></span>

<span data-ttu-id="58364-107">在 GDI + 中，中繼資料的部分稱為 *屬性專案*，而個別屬性專案則是由稱為 *屬性標記* 的數值常數來識別。</span><span class="sxs-lookup"><span data-stu-id="58364-107">In GDI+, a piece of metadata is called a *property item*, and an individual property item is identified by a numerical constant called a *property tag*.</span></span> <span data-ttu-id="58364-108">您可以藉由呼叫 [**image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image)類別的 [**Image：： SetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-setpropertyitem)和 [**image：： GetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertyitem)方法來儲存和取出中繼資料，而不需要擔心特定檔案格式儲存該中繼資料的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="58364-108">You can store and retrieve metadata by calling the [**Image::SetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-setpropertyitem) and [**Image::GetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertyitem) methods of the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class, and you don't have to be concerned with the details of how a particular file format stores that metadata.</span></span>

<span data-ttu-id="58364-109">下列主題將列出並描述 GDI + 所支援的屬性專案。</span><span class="sxs-lookup"><span data-stu-id="58364-109">The following topics list and describe the property items supported by GDI+.</span></span> <span data-ttu-id="58364-110">描述很簡單且一般，因此適用于各種不同的檔案格式。</span><span class="sxs-lookup"><span data-stu-id="58364-110">The descriptions are brief and general so that they apply to a variety of file formats.</span></span> <span data-ttu-id="58364-111">如需有關如何在特定檔案格式中使用屬性專案的詳細說明，請參閱該檔案格式的規格。</span><span class="sxs-lookup"><span data-stu-id="58364-111">For a detailed description of how a property item is used in a particular file format, see the specification for that file format.</span></span> <span data-ttu-id="58364-112">如需多個檔案格式規格的連結，請參閱 [影像檔案格式規格](-gdiplus-constant-image-file-format-specifications.md)。</span><span class="sxs-lookup"><span data-stu-id="58364-112">For links to several file format specifications, see [Image File Format Specifications](-gdiplus-constant-image-file-format-specifications.md).</span></span> <span data-ttu-id="58364-113">如需中繼資料的詳細資訊，請參閱 [讀取和寫入中繼資料](-gdiplus-reading-and-writing-metadata-use.md) 和 [**影像屬性標記類型常數**](-gdiplus-constant-image-property-tag-type-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="58364-113">For more information about metadata, see [Reading and Writing Metadata](-gdiplus-reading-and-writing-metadata-use.md) and [**Image Property Tag Type Constants**](-gdiplus-constant-image-property-tag-type-constants.md).</span></span>

-   [<span data-ttu-id="58364-114">以數位順序排序的屬性標記</span><span class="sxs-lookup"><span data-stu-id="58364-114">Property Tags in Numerical Order</span></span>](-gdiplus-constant-property-tags-in-numerical-order.md)
-   [<span data-ttu-id="58364-115">依字母順序排列的屬性標記</span><span class="sxs-lookup"><span data-stu-id="58364-115">Property Tags in Alphabetical Order</span></span>](-gdiplus-constant-property-tags-in-alphabetical-order.md)
-   [<span data-ttu-id="58364-116">屬性專案描述</span><span class="sxs-lookup"><span data-stu-id="58364-116">Property Item Descriptions</span></span>](-gdiplus-constant-property-item-descriptions.md)

 

 



