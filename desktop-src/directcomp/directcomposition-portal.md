---
title: DirectComposition
description: 本主題說明 Microsoft DirectComposition 的用途、識別其執行時間需求，並說明有效使用 Microsoft DirectComposition 所需的程式設計背景。
ms.assetid: 40e2d02b-77e8-425f-ac5e-3dcddef08173
keywords:
- DirectComposition
- DirectComposition API
- Microsoft DirectComposition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb34a4bb3bb7c0ffe370777888e20704fd0165d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300468"
---
# <a name="directcomposition"></a><span data-ttu-id="d3f30-106">DirectComposition</span><span class="sxs-lookup"><span data-stu-id="d3f30-106">DirectComposition</span></span>

> [!NOTE]
> <span data-ttu-id="d3f30-107">針對 Windows 10 上的應用程式，我們建議使用 DirectComposition，而不是使用。</span><span class="sxs-lookup"><span data-stu-id="d3f30-107">For apps on Windows 10, we recommend using Windows.UI.Composition APIs instead of DirectComposition.</span></span> <span data-ttu-id="d3f30-108">如需詳細資訊，請參閱 [使用視覺分層將您的桌面應用程式現代化](/windows/uwp/composition/visual-layer-in-desktop-apps)。</span><span class="sxs-lookup"><span data-stu-id="d3f30-108">For more info, see [Modernize your desktop app using the Visual layer](/windows/uwp/composition/visual-layer-in-desktop-apps).</span></span>

## <a name="purpose"></a><span data-ttu-id="d3f30-109">目的</span><span class="sxs-lookup"><span data-stu-id="d3f30-109">Purpose</span></span>

<span data-ttu-id="d3f30-110">Microsoft DirectComposition 是一種 Windows 元件，可透過轉換、效果和動畫來提供高效能點陣圖組合。</span><span class="sxs-lookup"><span data-stu-id="d3f30-110">Microsoft DirectComposition is a Windows component that enables high-performance bitmap composition with transforms, effects, and animations.</span></span> <span data-ttu-id="d3f30-111">應用程式開發人員可以使用 DirectComposition API 來建立視覺上吸引人的使用者介面，以提供豐富和流暢的動畫轉換 (從一種視覺效果轉換成另一種視覺效果)。</span><span class="sxs-lookup"><span data-stu-id="d3f30-111">Application developers can use the DirectComposition API to create visually engaging user interfaces that feature rich and fluid animated transitions from one visual to another.</span></span>

<span data-ttu-id="d3f30-112">DirectComposition 可讓您藉由使用圖形硬體，以及獨立于 UI 執行緒之外運作的方式，來達到豐富且流暢的轉換。</span><span class="sxs-lookup"><span data-stu-id="d3f30-112">DirectComposition enables rich and fluid transitions by achieving a high framerate, using graphics hardware, and operating independently of the UI thread.</span></span> <span data-ttu-id="d3f30-113">DirectComposition 可以接受由不同轉譯程式庫（包括 Microsoft DirectX 點陣圖）所繪製的點陣圖內容，以及轉譯成視窗 (HWND 點陣圖) 的點陣圖。</span><span class="sxs-lookup"><span data-stu-id="d3f30-113">DirectComposition can accept bitmap content drawn by different rendering libraries, including Microsoft DirectX bitmaps, and bitmaps rendered to a window (HWND bitmaps).</span></span> <span data-ttu-id="d3f30-114">此外，DirectComposition 還支援各種不同的轉換，例如2D 仿射轉換和3D 透視圖的轉換，以及像是裁剪和不透明度的基本效果。</span><span class="sxs-lookup"><span data-stu-id="d3f30-114">Also, DirectComposition supports a variety of transformations, such as 2D affine transforms and 3D perspective transforms, as well as basic effects such as clipping and opacity.</span></span>

<span data-ttu-id="d3f30-115">DirectComposition 的設計目的是要簡化撰寫 [*視覺效果*](directcomposition-glossary.md) 和建立動畫轉換的流程。</span><span class="sxs-lookup"><span data-stu-id="d3f30-115">DirectComposition is designed to simplify the process of composing [*visuals*](directcomposition-glossary.md) and creating animated transitions.</span></span> <span data-ttu-id="d3f30-116">如果您的應用程式已經包含轉譯程式碼，或已經使用建議的 DirectX API，您只需要執行最少量的工作，就能有效地使用 DirectComposition。</span><span class="sxs-lookup"><span data-stu-id="d3f30-116">If your application already contains rendering code or already uses the recommended DirectX API, you only need to do a minimal amount of work to use DirectComposition effectively.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="d3f30-117">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="d3f30-117">Developer audience</span></span>

<span data-ttu-id="d3f30-118">DirectComposition API 適用于熟悉 C/c + + 的經驗豐富且具備高度能力的圖形開發人員，對於元件物件模型 (的 COM) 有充分的瞭解，而且熟悉 Windows 程式設計概念。</span><span class="sxs-lookup"><span data-stu-id="d3f30-118">The DirectComposition API is intended for experienced and highly-capable graphics developers who know C/C++, have a solid understanding of the Component Object Model (COM), and are familiar with Windows programming concepts.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="d3f30-119">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="d3f30-119">Run-time requirements</span></span>

<span data-ttu-id="d3f30-120">DirectComposition 是在 Windows 8 引進。</span><span class="sxs-lookup"><span data-stu-id="d3f30-120">DirectComposition was introduced in Windows 8.</span></span> <span data-ttu-id="d3f30-121">它包含在32位、64位和 ARM 平臺中。</span><span class="sxs-lookup"><span data-stu-id="d3f30-121">It is included in 32-bit, 64-bit, and ARM platforms.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="d3f30-122">本節內容</span><span class="sxs-lookup"><span data-stu-id="d3f30-122">In this section</span></span>



| <span data-ttu-id="d3f30-123">主題</span><span class="sxs-lookup"><span data-stu-id="d3f30-123">Topic</span></span>                                                                       | <span data-ttu-id="d3f30-124">描述</span><span class="sxs-lookup"><span data-stu-id="d3f30-124">Description</span></span>                                                                                                                                                    |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d3f30-125">為何要使用 DirectComposition？</span><span class="sxs-lookup"><span data-stu-id="d3f30-125">Why use DirectComposition?</span></span>](why-use-directcomposition-.md)<br/>     | <span data-ttu-id="d3f30-126">本主題說明 DirectComposition 的功能和優點。</span><span class="sxs-lookup"><span data-stu-id="d3f30-126">This topic describes the capabilities and benefits of DirectComposition.</span></span> <br/>                                                                           |
| [<span data-ttu-id="d3f30-127">如何使用 DirectComposition</span><span class="sxs-lookup"><span data-stu-id="d3f30-127">How to Use DirectComposition</span></span>](how-to-use-directcomposition.md)<br/> | <span data-ttu-id="d3f30-128">本節說明使用 DirectComposition API 的最佳作法，並示範如何使用 API 來完成數個常見的工作。</span><span class="sxs-lookup"><span data-stu-id="d3f30-128">This section describes best practices for using the DirectComposition API, and demonstrates how to use the API to accomplish several common tasks.</span></span> <br/> |
| [<span data-ttu-id="d3f30-129">DirectComposition 概念</span><span class="sxs-lookup"><span data-stu-id="d3f30-129">DirectComposition concepts</span></span>](directcomposition-concepts.md)<br/>     | <span data-ttu-id="d3f30-130">本節提供 DirectComposition 的概念總覽。</span><span class="sxs-lookup"><span data-stu-id="d3f30-130">This section provides a conceptual overview of DirectComposition.</span></span><br/>                                                                                   |
| [<span data-ttu-id="d3f30-131">DirectComposition 參考</span><span class="sxs-lookup"><span data-stu-id="d3f30-131">DirectComposition reference</span></span>](reference.md)<br/>                     | <span data-ttu-id="d3f30-132">本節提供組成 DirectComposition API 之元素的詳細參考資訊。</span><span class="sxs-lookup"><span data-stu-id="d3f30-132">This section provides detailed reference information for the elements that make up the DirectComposition API.</span></span><br/>                                       |
| [<span data-ttu-id="d3f30-133">DirectComposition 範例</span><span class="sxs-lookup"><span data-stu-id="d3f30-133">DirectComposition samples</span></span>](directcomposition-code-samples.md)<br/>  | <span data-ttu-id="d3f30-134">下列範例應用程式會示範如何使用 DirectComposition API，並示範其功能。</span><span class="sxs-lookup"><span data-stu-id="d3f30-134">The following sample applications show how to use the DirectComposition API and demonstrate its capabilities.</span></span> <br/>                                      |
| [<span data-ttu-id="d3f30-135">DirectComposition 詞彙</span><span class="sxs-lookup"><span data-stu-id="d3f30-135">DirectComposition glossary</span></span>](directcomposition-glossary.md)<br/>     | <span data-ttu-id="d3f30-136">本主題定義 DirectComposition 條款。</span><span class="sxs-lookup"><span data-stu-id="d3f30-136">This topic defines DirectComposition terms.</span></span> <br/>                                                                                                        |



 

 

 





