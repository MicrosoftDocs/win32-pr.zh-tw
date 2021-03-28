---
description: 本主題列出 Region 類別的函式。 如需完整的類別清單，請參閱 Region 類別。
ms.assetid: 94f4971c-defa-43e0-a0c0-4000557b0a5c
title: Region 函數
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name: ''
api_type:
- NA
api_location: ''
ms.openlocfilehash: 98663587fab3722d689c9d34578d60daad922a2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115249"
---
# <a name="regionregion-constructors"></a><span data-ttu-id="132f2-104">Region 函數</span><span class="sxs-lookup"><span data-stu-id="132f2-104">Region.Region constructors</span></span>

<span data-ttu-id="132f2-105">本主題列出 [**Region**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-region) 類別的函式。</span><span class="sxs-lookup"><span data-stu-id="132f2-105">This topic lists the constructors of the [**Region**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-region) class.</span></span> <span data-ttu-id="132f2-106">如需完整的類別清單，請參閱 **Region 類別**。</span><span class="sxs-lookup"><span data-stu-id="132f2-106">For a complete class listing, see **Region Class**.</span></span>

### <a name="overload-list"></a><span data-ttu-id="132f2-107">多載清單</span><span class="sxs-lookup"><span data-stu-id="132f2-107">Overload list</span></span>



| <span data-ttu-id="132f2-108">建構函式</span><span class="sxs-lookup"><span data-stu-id="132f2-108">Constructor</span></span>                                                                 | <span data-ttu-id="132f2-109">描述</span><span class="sxs-lookup"><span data-stu-id="132f2-109">Description</span></span>                                                                                                                                                                                      |
|:----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="132f2-110">[**區域 (HRGN)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inhrgn))</span><span class="sxs-lookup"><span data-stu-id="132f2-110">[**Region(HRGN)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inhrgn))</span></span>                  | <span data-ttu-id="132f2-111">建立區域，該區域與 GDI 區域的控制碼所指定的區域相同。</span><span class="sxs-lookup"><span data-stu-id="132f2-111">Creates a region that is identical to the region that is specified by a handle to a GDI region.</span></span><br/>                                                                                       |
| <span data-ttu-id="132f2-112">[**區域 (Rect&)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inconstrect_))</span><span class="sxs-lookup"><span data-stu-id="132f2-112">[**Region(Rect&)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inconstrect_))</span></span>            | <span data-ttu-id="132f2-113">建立由矩形定義的區域。</span><span class="sxs-lookup"><span data-stu-id="132f2-113">Creates a region that is defined by a rectangle.</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="132f2-114">[**區域 (RectF&)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inconstrectf_))</span><span class="sxs-lookup"><span data-stu-id="132f2-114">[**Region(RectF&)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inconstrectf_))</span></span>          | <span data-ttu-id="132f2-115">建立由矩形定義的區域。</span><span class="sxs-lookup"><span data-stu-id="132f2-115">Creates a region that is defined by a rectangle.</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="132f2-116">[**區域 (位元組 \* 、INT)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inconstbyte_inint))</span><span class="sxs-lookup"><span data-stu-id="132f2-116">[**Region(BYTE\*,INT)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inconstbyte_inint))</span></span> | <span data-ttu-id="132f2-117">建立區域，該區域是由其他區域所取得的資料所定義。</span><span class="sxs-lookup"><span data-stu-id="132f2-117">Creates a region that is defined by data obtained from another region.</span></span> <br/>                                                                                                               |
| <span data-ttu-id="132f2-118">[**區域 (GraphicsPath \*)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inconstgraphicspath))</span><span class="sxs-lookup"><span data-stu-id="132f2-118">[**Region(GraphicsPath\*)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inconstgraphicspath))</span></span>        | <span data-ttu-id="132f2-119">建立一個區域，該區域是由 [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath)) 物件 (路徑所定義，且具有 **GraphicsPath** 物件中所含的填滿模式。</span><span class="sxs-lookup"><span data-stu-id="132f2-119">Creates a region that is defined by a path (a [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) object) and has a fill mode that is contained in the **GraphicsPath** object.</span></span><br/> |
| <span data-ttu-id="132f2-120">[**區域 ()**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(constregion_))</span><span class="sxs-lookup"><span data-stu-id="132f2-120">[**Region()**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(constregion_))</span></span>                           | <span data-ttu-id="132f2-121">建立無限的區域。</span><span class="sxs-lookup"><span data-stu-id="132f2-121">Creates a region that is infinite.</span></span> <span data-ttu-id="132f2-122">這是預設建構函式。</span><span class="sxs-lookup"><span data-stu-id="132f2-122">This is the default constructor.</span></span> <br/>                                                                                                                  |



 

 
