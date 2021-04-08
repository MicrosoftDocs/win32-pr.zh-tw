---
title: DirectComposition 概念
description: 本節提供 DirectComposition 的概念總覽。
ms.assetid: 7839C264-C15F-4E89-82B6-2963A5C61CEC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bea823d2edd27b2c725cefdd73cd053e94124d7f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104022254"
---
# <a name="directcomposition-concepts"></a><span data-ttu-id="415e9-103">DirectComposition 概念</span><span class="sxs-lookup"><span data-stu-id="415e9-103">DirectComposition concepts</span></span>

> [!NOTE]
> <span data-ttu-id="415e9-104">針對 Windows 10 上的應用程式，我們建議使用 DirectComposition，而不是使用。</span><span class="sxs-lookup"><span data-stu-id="415e9-104">For apps on Windows 10, we recommend using Windows.UI.Composition APIs instead of DirectComposition.</span></span> <span data-ttu-id="415e9-105">如需詳細資訊，請參閱 [使用視覺分層將您的桌面應用程式現代化](/windows/uwp/composition/visual-layer-in-desktop-apps)。</span><span class="sxs-lookup"><span data-stu-id="415e9-105">For more info, see [Modernize your desktop app using the Visual layer](/windows/uwp/composition/visual-layer-in-desktop-apps).</span></span>

<span data-ttu-id="415e9-106">本節提供 DirectComposition 的概念總覽。</span><span class="sxs-lookup"><span data-stu-id="415e9-106">This section provides a conceptual overview of DirectComposition.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="415e9-107">本節內容</span><span class="sxs-lookup"><span data-stu-id="415e9-107">In this section</span></span>



| <span data-ttu-id="415e9-108">主題</span><span class="sxs-lookup"><span data-stu-id="415e9-108">Topic</span></span>                                                                     | <span data-ttu-id="415e9-109">描述</span><span class="sxs-lookup"><span data-stu-id="415e9-109">Description</span></span>                                                                                                                                                                            |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="415e9-110">基本概念</span><span class="sxs-lookup"><span data-stu-id="415e9-110">Basic concepts</span></span>](basic-concepts.md)<br/>                           | <span data-ttu-id="415e9-111">本主題概要說明 Microsoft DirectComposition 的基本概念。</span><span class="sxs-lookup"><span data-stu-id="415e9-111">This topic provides an overview of the basic concepts of Microsoft DirectComposition.</span></span><br/>                                                                                       |
| [<span data-ttu-id="415e9-112">點陣圖物件</span><span class="sxs-lookup"><span data-stu-id="415e9-112">Bitmap objects</span></span>](bitmap-surfaces.md)<br/>                          | <span data-ttu-id="415e9-113">本主題說明 DirectComposition 支援的點陣圖內容類型。</span><span class="sxs-lookup"><span data-stu-id="415e9-113">This topic describes the types of bitmap content that DirectComposition supports.</span></span><br/>                                                                                           |
| [<span data-ttu-id="415e9-114">組合介面</span><span class="sxs-lookup"><span data-stu-id="415e9-114">Composition surface</span></span>](composition-surface.md)<br/>                 | <span data-ttu-id="415e9-115">本主題說明 DirectComposition 支援之介面類別型的類型。</span><span class="sxs-lookup"><span data-stu-id="415e9-115">This topic describes the types of types of surfaces that DirectComposition supports.</span></span><br/>                                                                                        |
| [<span data-ttu-id="415e9-116">轉換</span><span class="sxs-lookup"><span data-stu-id="415e9-116">Transforms</span></span>](transforms.md)<br/>                                   | <span data-ttu-id="415e9-117">本主題討論二維 (2D) 仿射 (線性) 轉換的 DirectComposition 支援，並說明 DirectComposition 支援的轉換類型。</span><span class="sxs-lookup"><span data-stu-id="415e9-117">This topic discusses DirectComposition support for two-dimensional (2D) affine (linear) transforms, and describes the types of transforms that DirectComposition supports.</span></span> <br/> |
| [<span data-ttu-id="415e9-118">影響</span><span class="sxs-lookup"><span data-stu-id="415e9-118">Effects</span></span>](effects.md)<br/>                                         | <span data-ttu-id="415e9-119">本主題討論 DirectComposition 效果的基本概念，並說明 DirectComposition 支援的效果類型。</span><span class="sxs-lookup"><span data-stu-id="415e9-119">This topic discusses the basics of DirectComposition effects, and describes the types of effects that DirectComposition supports.</span></span> <br/>                                          |
| [<span data-ttu-id="415e9-120">動畫</span><span class="sxs-lookup"><span data-stu-id="415e9-120">Animation</span></span>](animation.md)<br/>                                     | <span data-ttu-id="415e9-121">本主題討論 DirectComposition 動畫的基本概念。</span><span class="sxs-lookup"><span data-stu-id="415e9-121">This topic discusses the basics of DirectComposition animation.</span></span> <br/>                                                                                                            |
| [<span data-ttu-id="415e9-122">裁剪</span><span class="sxs-lookup"><span data-stu-id="415e9-122">Clipping</span></span>](clipping.md)<br/>                                       | <span data-ttu-id="415e9-123">本主題說明裁剪視覺效果的 DirectComposition 支援。</span><span class="sxs-lookup"><span data-stu-id="415e9-123">This topic describes DirectComposition support for clipping visuals.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="415e9-124">架構與元件</span><span class="sxs-lookup"><span data-stu-id="415e9-124">Architecture and components</span></span>](architecture-and-components.md)<br/> | <span data-ttu-id="415e9-125">本主題說明組成 DirectComposition 的元件。</span><span class="sxs-lookup"><span data-stu-id="415e9-125">This topic describes the components that make up DirectComposition.</span></span><br/>                                                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="415e9-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="415e9-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="415e9-127">DirectComposition</span><span class="sxs-lookup"><span data-stu-id="415e9-127">DirectComposition</span></span>](directcomposition-portal.md)
</dt> </dl>

 

 





