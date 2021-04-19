---
description: 本主題說明如何使用頁面層級介面，提供 XPS OM 中頁面內容的存取權。
ms.assetid: 7127ee28-eca9-4e0e-a27a-9051eb105b27
title: 使用 XPS OM 頁面介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8350409f2f436cc4ec2293e735c3f020b49bea68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975758"
---
# <a name="working-with-xps-om-page-interfaces"></a><span data-ttu-id="efaf2-103">使用 XPS OM 頁面介面</span><span class="sxs-lookup"><span data-stu-id="efaf2-103">Working with XPS OM Page Interfaces</span></span>

<span data-ttu-id="efaf2-104">本主題說明如何使用頁面層級介面，提供 XPS OM 中頁面內容的存取權。</span><span class="sxs-lookup"><span data-stu-id="efaf2-104">This topic describes how to use the page-level interfaces that provide access to the contents of a page in an XPS OM.</span></span>



| <span data-ttu-id="efaf2-105">介面名稱</span><span class="sxs-lookup"><span data-stu-id="efaf2-105">Interface name</span></span>                                                                                                                                                                              | <span data-ttu-id="efaf2-106">邏輯子介面</span><span class="sxs-lookup"><span data-stu-id="efaf2-106">Logical child interfaces</span></span>                                                                                                                                                                                            | <span data-ttu-id="efaf2-107">Description</span><span class="sxs-lookup"><span data-stu-id="efaf2-107">Description</span></span>                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="efaf2-108">**IXpsOMPage**</span><span class="sxs-lookup"><span data-stu-id="efaf2-108">**IXpsOMPage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)<br/>                                                                                                                                                 | [<span data-ttu-id="efaf2-109">**IXpsOMCanvas**</span><span class="sxs-lookup"><span data-stu-id="efaf2-109">**IXpsOMCanvas**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)<br/> [<span data-ttu-id="efaf2-110">**IXpsOMGlyphs**</span><span class="sxs-lookup"><span data-stu-id="efaf2-110">**IXpsOMGlyphs**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs)<br/> [<span data-ttu-id="efaf2-111">**IXpsOMPath**</span><span class="sxs-lookup"><span data-stu-id="efaf2-111">**IXpsOMPath**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)<br/>                                                                         | <span data-ttu-id="efaf2-112">頁面內容的根物件。</span><span class="sxs-lookup"><span data-stu-id="efaf2-112">The root object of the page contents.</span></span><br/> <span data-ttu-id="efaf2-113">此物件代表檔元件。</span><span class="sxs-lookup"><span data-stu-id="efaf2-113">This object represents a document part.</span></span><br/>                                                |
| [<span data-ttu-id="efaf2-114">**IXpsOMShareable**</span><span class="sxs-lookup"><span data-stu-id="efaf2-114">**IXpsOMShareable**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomshareable)<br/>                                                                                                                                       | [<span data-ttu-id="efaf2-115">**IXpsOMVisual**</span><span class="sxs-lookup"><span data-stu-id="efaf2-115">**IXpsOMVisual**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual)<br/> [<span data-ttu-id="efaf2-116">**IXpsOMMatrixTransform**</span><span class="sxs-lookup"><span data-stu-id="efaf2-116">**IXpsOMMatrixTransform**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsommatrixtransform)<br/> [<span data-ttu-id="efaf2-117">**IXpsOMGeometry**</span><span class="sxs-lookup"><span data-stu-id="efaf2-117">**IXpsOMGeometry**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry)<br/> [<span data-ttu-id="efaf2-118">**IXpsOMBrush**</span><span class="sxs-lookup"><span data-stu-id="efaf2-118">**IXpsOMBrush**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush)<br/> | <span data-ttu-id="efaf2-119">衍生自 [**IXpsOMShareable**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomshareable) 介面的介面可以儲存在資源字典中並共用。</span><span class="sxs-lookup"><span data-stu-id="efaf2-119">Interfaces that derive from the [**IXpsOMShareable**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomshareable) interface can be stored in a resource dictionary and shared.</span></span><br/> |
| [<span data-ttu-id="efaf2-120">**IXpsOMRemoteDictionaryResource**</span><span class="sxs-lookup"><span data-stu-id="efaf2-120">**IXpsOMRemoteDictionaryResource**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresource)<br/> [<span data-ttu-id="efaf2-121">**IXpsOMRemoteDictionaryResourceCollection**</span><span class="sxs-lookup"><span data-stu-id="efaf2-121">**IXpsOMRemoteDictionaryResourceCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresourcecollection)<br/> | [<span data-ttu-id="efaf2-122">**IXpsOMDictionary**</span><span class="sxs-lookup"><span data-stu-id="efaf2-122">**IXpsOMDictionary**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdictionary)<br/>                                                                                                                                                             | <span data-ttu-id="efaf2-123">包含資源字典。</span><span class="sxs-lookup"><span data-stu-id="efaf2-123">Contains a resource dictionary.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="efaf2-124">**IXpsOMDictionary**</span><span class="sxs-lookup"><span data-stu-id="efaf2-124">**IXpsOMDictionary**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdictionary)<br/>                                                                                                                                     | <span data-ttu-id="efaf2-125">無</span><span class="sxs-lookup"><span data-stu-id="efaf2-125">None</span></span><br/>                                                                                                                                                                                                     | <span data-ttu-id="efaf2-126">參考其他物件所共用的資源。</span><span class="sxs-lookup"><span data-stu-id="efaf2-126">References the resources that are shared by other objects.</span></span><br/>                                                                              |
| [<span data-ttu-id="efaf2-127">**IXpsOMStoryFragmentsResource**</span><span class="sxs-lookup"><span data-stu-id="efaf2-127">**IXpsOMStoryFragmentsResource**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomstoryfragmentsresource)<br/>                                                                                                             | <span data-ttu-id="efaf2-128">無</span><span class="sxs-lookup"><span data-stu-id="efaf2-128">None</span></span><br/>                                                                                                                                                                                                     | <span data-ttu-id="efaf2-129">提供檔 StoryFragments 部分之資源串流內容的存取權。</span><span class="sxs-lookup"><span data-stu-id="efaf2-129">Provides access to the content of the resource stream of the StoryFragments part of the document.</span></span><br/>                                       |



 

## <a name="related-topics"></a><span data-ttu-id="efaf2-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="efaf2-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="efaf2-131">**IXpsOMDictionary 介面**</span><span class="sxs-lookup"><span data-stu-id="efaf2-131">**IXpsOMDictionary Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdictionary)
</dt> <dt>

[<span data-ttu-id="efaf2-132">**IXpsOMDocumentStructureResource**</span><span class="sxs-lookup"><span data-stu-id="efaf2-132">**IXpsOMDocumentStructureResource**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentstructureresource)
</dt> <dt>

[<span data-ttu-id="efaf2-133">**IXpsOMPage 介面**</span><span class="sxs-lookup"><span data-stu-id="efaf2-133">**IXpsOMPage Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)
</dt> <dt>

[<span data-ttu-id="efaf2-134">**IXpsOMRemoteDictionaryResource 介面**</span><span class="sxs-lookup"><span data-stu-id="efaf2-134">**IXpsOMRemoteDictionaryResource Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresource)
</dt> <dt>

[<span data-ttu-id="efaf2-135">**IXpsOMRemoteDictionaryResourceCollection 介面**</span><span class="sxs-lookup"><span data-stu-id="efaf2-135">**IXpsOMRemoteDictionaryResourceCollection Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresourcecollection)
</dt> <dt>

[<span data-ttu-id="efaf2-136">**IXpsOMStoryFragmentsResource 介面**</span><span class="sxs-lookup"><span data-stu-id="efaf2-136">**IXpsOMStoryFragmentsResource Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomstoryfragmentsresource)
</dt> </dl>

 

 




