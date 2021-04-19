---
title: XPS OM 畫布和視覺化介面
description: 本主題說明如何在 XPS OM 中使用 XPS 檔 API 的畫布相關介面。
ms.assetid: 368b8c47-9803-42ee-a3a8-681bf55315ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93a3acc8fbc85298e21d039898d4ae7d38fbb272
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314751"
---
# <a name="working-with-xps-om-canvas-and-visual-interfaces"></a><span data-ttu-id="c1ae0-103">使用 XPS OM 畫布和視覺化介面</span><span class="sxs-lookup"><span data-stu-id="c1ae0-103">Working with XPS OM Canvas and Visual Interfaces</span></span>

<span data-ttu-id="c1ae0-104">本主題說明如何在 XPS OM 中使用 XPS 檔 API 的畫布相關介面。</span><span class="sxs-lookup"><span data-stu-id="c1ae0-104">This topic describes how to use the canvas-related interfaces of the XPS Document API in an XPS OM.</span></span>

| <span data-ttu-id="c1ae0-105">介面名稱</span><span class="sxs-lookup"><span data-stu-id="c1ae0-105">Interface name</span></span>                                  | <span data-ttu-id="c1ae0-106">邏輯子介面</span><span class="sxs-lookup"><span data-stu-id="c1ae0-106">Logical child interfaces</span></span>                                                                                                                    | <span data-ttu-id="c1ae0-107">描述</span><span class="sxs-lookup"><span data-stu-id="c1ae0-107">Description</span></span>                                                                                                                                                                                                             |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c1ae0-108">**IXpsOMVisual**</span><span class="sxs-lookup"><span data-stu-id="c1ae0-108">**IXpsOMVisual**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual)<br/> | [<span data-ttu-id="c1ae0-109">**IXpsOMCanvas**</span><span class="sxs-lookup"><span data-stu-id="c1ae0-109">**IXpsOMCanvas**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)<br/> [<span data-ttu-id="c1ae0-110">**IXpsOMGlyphs**</span><span class="sxs-lookup"><span data-stu-id="c1ae0-110">**IXpsOMGlyphs**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs)<br/> [<span data-ttu-id="c1ae0-111">**IXpsOMPath**</span><span class="sxs-lookup"><span data-stu-id="c1ae0-111">**IXpsOMPath**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)<br/> | <span data-ttu-id="c1ae0-112">定義視覺物件之介面的基類，例如文字和圖形。</span><span class="sxs-lookup"><span data-stu-id="c1ae0-112">The base class of the interfaces that define visual objects, such as text and graphics.</span></span><br/> <span data-ttu-id="c1ae0-113">您可以在 [**IXpsOMVisualCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection) 介面中收集視覺物件。</span><span class="sxs-lookup"><span data-stu-id="c1ae0-113">Visual objects can be collected in an [**IXpsOMVisualCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection) interface.</span></span><br/> |
| [<span data-ttu-id="c1ae0-114">**IXpsOMCanvas**</span><span class="sxs-lookup"><span data-stu-id="c1ae0-114">**IXpsOMCanvas**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)<br/> | [<span data-ttu-id="c1ae0-115">**IXpsOMCanvas**</span><span class="sxs-lookup"><span data-stu-id="c1ae0-115">**IXpsOMCanvas**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)<br/> [<span data-ttu-id="c1ae0-116">**IXpsOMGlyphs**</span><span class="sxs-lookup"><span data-stu-id="c1ae0-116">**IXpsOMGlyphs**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs)<br/> [<span data-ttu-id="c1ae0-117">**IXpsOMPath**</span><span class="sxs-lookup"><span data-stu-id="c1ae0-117">**IXpsOMPath**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)<br/> | <span data-ttu-id="c1ae0-118">可視為單一視覺物件的視覺物件集合。</span><span class="sxs-lookup"><span data-stu-id="c1ae0-118">A collection of visual objects that can be treated as a single visual object.</span></span><br/>                                                                                                                                |

<span data-ttu-id="c1ae0-119">[**IXpsOMVisual**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual) 是基底介面;頁面的可見物件繼承自它。</span><span class="sxs-lookup"><span data-stu-id="c1ae0-119">[**IXpsOMVisual**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual) is the base interface; the visible objects of a page inherit from it.</span></span> <span data-ttu-id="c1ae0-120">[**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) 繼承自 [**IXpsOMVisual**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual) ，可讓許多其他視覺元素以單一視覺元素來分組和處理。</span><span class="sxs-lookup"><span data-stu-id="c1ae0-120">[**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) inherits from [**IXpsOMVisual**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual) and enables many other visual elements to be grouped and acted upon as a single visual element.</span></span> <span data-ttu-id="c1ae0-121">例如，您可以使用 [**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) 介面來建立包含文字和圖形元素集合的網頁橫幅。</span><span class="sxs-lookup"><span data-stu-id="c1ae0-121">For example, you could use an [**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) interface to create a page banner that contains a collection of text and graphical elements.</span></span> <span data-ttu-id="c1ae0-122">這類橫幅可能包含標誌、公司口號和公司位址。</span><span class="sxs-lookup"><span data-stu-id="c1ae0-122">Such a banner might contain a logo, the company slogan, and the company address.</span></span> <span data-ttu-id="c1ae0-123">您可以將所有這些元素放入 [**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)介面的 [**IXpsOMVisualCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection)中，然後將單一轉換套用至 [**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)物件，以將其調整為特定頁面。</span><span class="sxs-lookup"><span data-stu-id="c1ae0-123">You could place all these elements into the [**IXpsOMVisualCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection) of an [**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) interface, and then apply a single transform to the [**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) object to resize it to a particular page.</span></span> <span data-ttu-id="c1ae0-124">這比計算更簡單，而且會將轉換套用至橫幅中的每個個別視覺元件。</span><span class="sxs-lookup"><span data-stu-id="c1ae0-124">This is much simpler than computing and applying a transform to each individual visual component in the banner.</span></span>

<span data-ttu-id="c1ae0-125">您也可以使用畫布來調整頁面內容大小，以符合目前的頁面大小。</span><span class="sxs-lookup"><span data-stu-id="c1ae0-125">You can also use a canvas to resize the page contents to fit the current page size.</span></span> <span data-ttu-id="c1ae0-126">若要完成此動作，請將網頁的所有內容放在單一畫布中，然後套用適當的轉換，以將畫布調整為目前的頁面大小。</span><span class="sxs-lookup"><span data-stu-id="c1ae0-126">To accomplish this, place all contents of the page into a single canvas, then apply the appropriate transform to fit the canvas to the current page size.</span></span> <span data-ttu-id="c1ae0-127">這也比嘗試調整頁面視覺效果集合中的每個視覺元素更簡單。</span><span class="sxs-lookup"><span data-stu-id="c1ae0-127">This is also much simpler than trying to resize each visual element in the collection of visuals in the page.</span></span>

## <a name="move-page-contents-to-a-canvas"></a><span data-ttu-id="c1ae0-128">將頁面內容移至畫布</span><span class="sxs-lookup"><span data-stu-id="c1ae0-128">Move page contents to a canvas</span></span>

<span data-ttu-id="c1ae0-129">下列程式碼範例會將頁面的內容移至畫布。</span><span class="sxs-lookup"><span data-stu-id="c1ae0-129">The following code example moves the contents of a page to a canvas.</span></span>

```C++
    HRESULT                   hr = S_OK;

    IXpsOMVisualCollection    *pageVisuals;
    IXpsOMVisualCollection    *canvasVisuals;
    IXpsOMVisual              *oneVisual;
    IXpsOMCanvas              *newPageCanvas;

    UINT32 numVisuals = 0;
    UINT32 thisVisual;

    // get the page's visual collection
    // and how many objects it contains
    hr = page->GetVisuals( &pageVisuals );
    hr = pageVisuals->GetCount ( &numVisuals );

    // create the new canvas object and
    // its (empty) visual collection
    hr = xpsFactory->CreateCanvas ( &newPageCanvas );
    hr = newPageCanvas->GetVisuals ( &canvasVisuals );

    // go through the page's list of visual objects,
    //  move each one from the page's list to the canvas' list
    //  release the local pointer
    //  remove it from the page's collection
    thisVisual = 0;
    while (thisVisual < numVisuals) {
        hr = pageVisuals->GetAt (0, &oneVisual);
        hr = canvasVisuals->Append (oneVisual);
        hr = pageVisuals->RemoveAt (0);
        thisVisual++;
    }
    // the page's visual collection should be empty
    hr = pageVisuals->GetCount (&numVisuals);
    _ASSERT (0 == numVisuals);

    // add the new canvas to the page's visual collection
    pageVisuals->Append ( newPageCanvas );

```

## <a name="related-topics"></a><span data-ttu-id="c1ae0-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="c1ae0-130">Related topics</span></span>

<dl> 
  <span data-ttu-id="c1ae0-131"><dt>[**IXpsOMCanvas 介面**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)</dt>
  <dt>[**IXpsOMVisual 介面**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual)</dt>
  <dt>[**IXpsOMVisualCollection 介面**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection)</dt>
</span><span class="sxs-lookup"><span data-stu-id="c1ae0-131"><dt>[**IXpsOMCanvas Interface**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)</dt>
  <dt>[**IXpsOMVisual Interface**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual)</dt>
  <dt>[**IXpsOMVisualCollection Interface**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection)</dt>
</span></span></dl>
