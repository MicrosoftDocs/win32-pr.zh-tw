---
description: 目錄的位置類型
ms.assetid: cc2fbadc-43f7-470c-873b-de2dc9d84e5d
title: 目錄的位置類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e1b6782a3722a6ce5a36117694f35442f8e4d43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106993070"
---
# <a name="the-position-type-of-a-table-of-contents"></a><span data-ttu-id="77182-103">目錄的位置類型</span><span class="sxs-lookup"><span data-stu-id="77182-103">The Position Type of a Table of Contents</span></span>

<span data-ttu-id="77182-104">[**ITocParser**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser)介面的某些方法有一個名為 *enumTocPosType* 的參數，其類型為 [**enum TOC \_ POS \_ 型**](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-toc_pos_type)別。</span><span class="sxs-lookup"><span data-stu-id="77182-104">Some methods of the [**ITocParser**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) interface have a parameter named *enumTocPosType* that has a type of [**enum TOC\_POS\_TYPE**](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-toc_pos_type).</span></span> <span data-ttu-id="77182-105">此參數會指定媒體檔案中儲存目錄的位置。</span><span class="sxs-lookup"><span data-stu-id="77182-105">This parameter specifies the position in a media file where a table of contents is stored.</span></span> <span data-ttu-id="77182-106">其目的是要將目錄儲存在檔案標頭中，或儲存在檔案的主體中，做為最上層物件。</span><span class="sxs-lookup"><span data-stu-id="77182-106">The intent was that the table of contents could be stored either in the file header or in the body of the file as a top level object.</span></span> <span data-ttu-id="77182-107">這種功能尚未實行。</span><span class="sxs-lookup"><span data-stu-id="77182-107">This functionality has not, as yet, been implemented.</span></span>

<span data-ttu-id="77182-108">目前，目錄只能儲存為最上層的物件，因此您必須一律將 *enumTocPosType* 參數設定為 **TOC \_ POS \_ TOPLEVELOBJECT**。</span><span class="sxs-lookup"><span data-stu-id="77182-108">Currently, tables of contents can only be stored as top level objects, so you must always set the *enumTocPosType* parameter to **TOC\_POS\_TOPLEVELOBJECT**.</span></span> <span data-ttu-id="77182-109">如果您將 *enumTocPosType* 設定為 **TOC \_ POS \_ INHEADER**，此方法將會傳回 **E \_ >notimpl**。</span><span class="sxs-lookup"><span data-stu-id="77182-109">If you set *enumTocPosType* to **TOC\_POS\_INHEADER**, the method will return **E\_NOTIMPL**.</span></span>

<span data-ttu-id="77182-110">下列方法具有 *enumTocPosType* 參數。</span><span class="sxs-lookup"><span data-stu-id="77182-110">The following methods have an *enumTocPosType* parameter.</span></span>

-   [<span data-ttu-id="77182-111">**GetTocCount**</span><span class="sxs-lookup"><span data-stu-id="77182-111">**GetTocCount**</span></span>](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-gettoccount)
-   [<span data-ttu-id="77182-112">**GetTocByIndex**</span><span class="sxs-lookup"><span data-stu-id="77182-112">**GetTocByIndex**</span></span>](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-gettocbyindex)
-   [<span data-ttu-id="77182-113">**GetTocByType**</span><span class="sxs-lookup"><span data-stu-id="77182-113">**GetTocByType**</span></span>](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-gettocbytype)
-   [<span data-ttu-id="77182-114">**AddToc**</span><span class="sxs-lookup"><span data-stu-id="77182-114">**AddToc**</span></span>](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-addtoc)
-   [<span data-ttu-id="77182-115">**RemoveTocByIndex**</span><span class="sxs-lookup"><span data-stu-id="77182-115">**RemoveTocByIndex**</span></span>](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-removetocbyindex)
-   [<span data-ttu-id="77182-116">**RemoveTocByType**</span><span class="sxs-lookup"><span data-stu-id="77182-116">**RemoveTocByType**</span></span>](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-removetocbytype)

## <a name="related-topics"></a><span data-ttu-id="77182-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="77182-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77182-118">目錄剖析器程式設計指南</span><span class="sxs-lookup"><span data-stu-id="77182-118">Table of Contents Parser Programming Guide</span></span>](toc-parser-programming-guide.md)
</dt> </dl>

 

 



