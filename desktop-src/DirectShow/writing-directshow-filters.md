---
description: 撰寫 DirectShow 篩選器
ms.assetid: ffbc92b2-4f45-439b-b140-49a66fc4d914
title: 撰寫 DirectShow 篩選器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e2b266f3bbb9781dddcd2d0fb065b63d895a732
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977198"
---
# <a name="writing-directshow-filters"></a><span data-ttu-id="3678b-103">撰寫 DirectShow 篩選器</span><span class="sxs-lookup"><span data-stu-id="3678b-103">Writing DirectShow Filters</span></span>

<span data-ttu-id="3678b-104">如果您正在開發用於 Microsoft DirectShow 篩選圖形的篩選器，請閱讀本節中的文章。</span><span class="sxs-lookup"><span data-stu-id="3678b-104">If you are developing a filter for use in a Microsoft DirectShow filter graph, read the articles in this section.</span></span> <span data-ttu-id="3678b-105">一般而言，如果您要撰寫 DirectShow 應用程式，則不需要閱讀此區段。</span><span class="sxs-lookup"><span data-stu-id="3678b-105">In general, you do not have to read this section if you are writing a DirectShow application.</span></span> <span data-ttu-id="3678b-106">大部分的應用程式都不會存取此區段所討論層級的篩選或篩選圖表。</span><span class="sxs-lookup"><span data-stu-id="3678b-106">Most applications do not access filters or the filter graph at the level discussed in this section.</span></span>

-   [<span data-ttu-id="3678b-107">DirectShow 篩選器開發簡介</span><span class="sxs-lookup"><span data-stu-id="3678b-107">Introduction to DirectShow Filter Development</span></span>](introduction-to-directshow-filter-development.md)
-   [<span data-ttu-id="3678b-108">建立 DirectShow 篩選器</span><span class="sxs-lookup"><span data-stu-id="3678b-108">Building DirectShow Filters</span></span>](building-directshow-filters.md)
-   [<span data-ttu-id="3678b-109">篩選準則的連接方式</span><span class="sxs-lookup"><span data-stu-id="3678b-109">How Filters Connect</span></span>](how-filters-connect.md)
-   [<span data-ttu-id="3678b-110">篩選開發人員的資料流程</span><span class="sxs-lookup"><span data-stu-id="3678b-110">Data Flow for Filter Developers</span></span>](data-flow-for-filter-developers.md)
-   [<span data-ttu-id="3678b-111">執行緒和重要區段</span><span class="sxs-lookup"><span data-stu-id="3678b-111">Threads and Critical Sections</span></span>](threads-and-critical-sections.md)
-   [<span data-ttu-id="3678b-112">品質控制管理</span><span class="sxs-lookup"><span data-stu-id="3678b-112">Quality-Control Management</span></span>](quality-control-management.md)
-   [<span data-ttu-id="3678b-113">DirectShow 和 COM</span><span class="sxs-lookup"><span data-stu-id="3678b-113">DirectShow and COM</span></span>](directshow-and-com.md)
-   [<span data-ttu-id="3678b-114">寫入來源篩選</span><span class="sxs-lookup"><span data-stu-id="3678b-114">Writing Source Filters</span></span>](writing-source-filters.md)
-   [<span data-ttu-id="3678b-115">寫入轉換篩選</span><span class="sxs-lookup"><span data-stu-id="3678b-115">Writing Transform Filters</span></span>](writing-transform-filters.md)
-   [<span data-ttu-id="3678b-116">撰寫影片轉譯器</span><span class="sxs-lookup"><span data-stu-id="3678b-116">Writing Video Renderers</span></span>](writing-video-renderers.md)
-   [<span data-ttu-id="3678b-117">寫入捕獲篩選器</span><span class="sxs-lookup"><span data-stu-id="3678b-117">Writing Capture Filters</span></span>](writing-capture-filters.md)
-   [<span data-ttu-id="3678b-118">公開捕捉和壓縮格式</span><span class="sxs-lookup"><span data-stu-id="3678b-118">Exposing Capture and Compression Formats</span></span>](exposing-capture-and-compression-formats.md)
-   [<span data-ttu-id="3678b-119">註冊自訂檔案類型</span><span class="sxs-lookup"><span data-stu-id="3678b-119">Registering a Custom File Type</span></span>](registering-a-custom-file-type.md)
-   [<span data-ttu-id="3678b-120">建立篩選屬性頁</span><span class="sxs-lookup"><span data-stu-id="3678b-120">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)

 

 



