---
title: 如何使用 DirectComposition
description: 本節說明使用 Microsoft DirectComposition \ 32 的最佳作法;API，並示範如何使用 API 來完成數個常見的工作。
ms.assetid: 49F6E356-90C7-423A-A31A-AEE41F882D3B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0658a9693567dfd88e9a986893048fa1d0fa1e5
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "106991093"
---
# <a name="how-to-use-directcomposition"></a><span data-ttu-id="4ef7f-103">如何使用 DirectComposition</span><span class="sxs-lookup"><span data-stu-id="4ef7f-103">How to use DirectComposition</span></span>

> [!NOTE]
> <span data-ttu-id="4ef7f-104">針對 Windows 10 上的應用程式，我們建議使用 DirectComposition，而不是使用。</span><span class="sxs-lookup"><span data-stu-id="4ef7f-104">For apps on Windows 10, we recommend using Windows.UI.Composition APIs instead of DirectComposition.</span></span> <span data-ttu-id="4ef7f-105">如需詳細資訊，請參閱 [使用視覺分層將您的桌面應用程式現代化](/windows/uwp/composition/visual-layer-in-desktop-apps)。</span><span class="sxs-lookup"><span data-stu-id="4ef7f-105">For more info, see [Modernize your desktop app using the Visual layer](/windows/uwp/composition/visual-layer-in-desktop-apps).</span></span>

<span data-ttu-id="4ef7f-106">本節說明使用 Microsoft DirectComposition API 的最佳作法，並示範如何使用 API 來完成數個常見的工作。</span><span class="sxs-lookup"><span data-stu-id="4ef7f-106">This section describes best practices for using the Microsoft DirectComposition API, and demonstrates how to use the API to accomplish several common tasks.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="4ef7f-107">本節內容</span><span class="sxs-lookup"><span data-stu-id="4ef7f-107">In this section</span></span>



| <span data-ttu-id="4ef7f-108">主題</span><span class="sxs-lookup"><span data-stu-id="4ef7f-108">Topic</span></span>                                                                                                                      | <span data-ttu-id="4ef7f-109">描述</span><span class="sxs-lookup"><span data-stu-id="4ef7f-109">Description</span></span>                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4ef7f-110">DirectComposition 的最佳作法</span><span class="sxs-lookup"><span data-stu-id="4ef7f-110">Best practices for DirectComposition</span></span>](best-practices-for-directcomposition.md)<br/>                                | <span data-ttu-id="4ef7f-111">本主題說明使用 DirectComposition 的最佳作法。</span><span class="sxs-lookup"><span data-stu-id="4ef7f-111">This topic describes best practices for using DirectComposition.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="4ef7f-112">如何初始化 DirectComposition</span><span class="sxs-lookup"><span data-stu-id="4ef7f-112">How to initialize DirectComposition</span></span>](initialize-directcomposition.md)<br/>                                         | <span data-ttu-id="4ef7f-113">本主題將示範如何建立和初始化建立簡單撰寫所需的最小一組 DirectComposition 物件。</span><span class="sxs-lookup"><span data-stu-id="4ef7f-113">This topic demonstrates how to create and initialize the minimum set of DirectComposition objects needed to create a simple composition.</span></span><br/>                                                          |
| [<span data-ttu-id="4ef7f-114">如何建立簡單的視覺化樹狀結構</span><span class="sxs-lookup"><span data-stu-id="4ef7f-114">How to build a simple visual tree</span></span>](how-to--build-a-visual-tree.md)<br/>                                            | <span data-ttu-id="4ef7f-115">本主題將示範如何建立簡單的 DirectComposition 視覺化樹狀結構。</span><span class="sxs-lookup"><span data-stu-id="4ef7f-115">This topic demonstrates how to build a simple DirectComposition visual tree.</span></span> <span data-ttu-id="4ef7f-116">本主題中的範例會建立並撰寫由根視覺效果和三個子視覺效果組成的視覺化樹狀結構。</span><span class="sxs-lookup"><span data-stu-id="4ef7f-116">The example in this topic builds and composes a visual tree that consists of a root visual and three child visuals.</span></span> <br/> |
| [<span data-ttu-id="4ef7f-117">如何使用矩形剪輯物件裁剪</span><span class="sxs-lookup"><span data-stu-id="4ef7f-117">How to clip with a rectangle clip object</span></span>](how-to--set-the-clip-rectangle-for-a-visual.md)<br/>                     | <span data-ttu-id="4ef7f-118">本主題將示範如何使用矩形剪輯物件來裁剪視覺效果或視覺化樹狀結構。</span><span class="sxs-lookup"><span data-stu-id="4ef7f-118">This topic demonstrates how to use a rectangle clip object to clip a visual or visual tree.</span></span> <br/>                                                                                                      |
| [<span data-ttu-id="4ef7f-119">如何套用2D 轉換</span><span class="sxs-lookup"><span data-stu-id="4ef7f-119">How to apply 2D transforms</span></span>](apply-2d-transforms.md)<br/>                                                           | <span data-ttu-id="4ef7f-120">本主題示範如何使用 DirectComposition 將2D 轉換套用至視覺效果。</span><span class="sxs-lookup"><span data-stu-id="4ef7f-120">This topic demonstrates how to apply 2D transforms to a visual by using DirectComposition.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="4ef7f-121">如何套用效果</span><span class="sxs-lookup"><span data-stu-id="4ef7f-121">How to apply effects</span></span>](how-to--apply-transforms-and-effects-to-a-visual.md)<br/>                                    | <span data-ttu-id="4ef7f-122">本主題將示範如何使用 DirectComposition 將效果和3D 轉換套用至視覺效果。</span><span class="sxs-lookup"><span data-stu-id="4ef7f-122">This topic demonstrates how to use DirectComposition to apply effects and 3D transformations to a visual.</span></span><br/>                                                                                         |
| [<span data-ttu-id="4ef7f-123">如何套用動畫</span><span class="sxs-lookup"><span data-stu-id="4ef7f-123">How to apply animations</span></span>](how-to--animate-a-visual.md)<br/>                                                         | <span data-ttu-id="4ef7f-124">本主題示範如何使用 DirectComposition 以動畫顯示視覺效果的屬性。</span><span class="sxs-lookup"><span data-stu-id="4ef7f-124">This topic demonstrates how to animate the properties of a visual by using DirectComposition.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="4ef7f-125">如何建立分層子視窗點陣圖的動畫</span><span class="sxs-lookup"><span data-stu-id="4ef7f-125">How to animate the bitmap of a layered child window</span></span>](how-to--animate-the-bitmap-of-a-layered-child-window.md)<br/> | <span data-ttu-id="4ef7f-126">本主題說明如何建立視覺效果，並為其建立動畫，其使用分層子視窗的點陣圖作為視覺效果的內容。</span><span class="sxs-lookup"><span data-stu-id="4ef7f-126">This topic describes how to create and animate a visual that uses the bitmap of a layered child window as the visual's content.</span></span> <br/>                                                                  |



 

## <a name="related-topics"></a><span data-ttu-id="4ef7f-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="4ef7f-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ef7f-128">DirectComposition</span><span class="sxs-lookup"><span data-stu-id="4ef7f-128">DirectComposition</span></span>](directcomposition-portal.md)
</dt> </dl>

 

 





