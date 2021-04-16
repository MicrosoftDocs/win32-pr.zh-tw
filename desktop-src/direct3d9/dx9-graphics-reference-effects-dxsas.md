---
description: 標準注釋和語義 (DXSAS) 提供以標準方式使用著色器的方法，可讓著色器用於工具、應用程式和遊戲引擎。
ms.assetid: b3206b30-56b4-4d56-a778-af3a6b3b8d9c
title: DirectX 標準注釋和語義參考
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c989f4aed7c01c62d6133e01fe035223b74c8d3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467685"
---
# <a name="directx-standard-annotations-and-semantics-reference"></a><span data-ttu-id="2f900-103">DirectX 標準注釋和語義參考</span><span class="sxs-lookup"><span data-stu-id="2f900-103">DirectX Standard Annotations and Semantics Reference</span></span>

<span data-ttu-id="2f900-104">標準注釋和語義 (DXSAS) 提供以標準方式使用著色器的方法，可讓著色器用於工具、應用程式和遊戲引擎。</span><span class="sxs-lookup"><span data-stu-id="2f900-104">Standard annotations and semantics (DXSAS) provide a method of using shaders in a standard way that enables shaders to be used with tools, applications, and game engines.</span></span> <span data-ttu-id="2f900-105">DXSAS 會針對共用效果，定義一組附加至主應用程式值和效果參數的一組語義和批註。</span><span class="sxs-lookup"><span data-stu-id="2f900-105">DXSAS defines a set of semantics and annotations that are attached to host application values and effect parameters for the purpose of sharing effects.</span></span> <span data-ttu-id="2f900-106">為了讓這些批註和語義都能發揮效用，必須同時在主應用程式和效果檔案中執行它們。</span><span class="sxs-lookup"><span data-stu-id="2f900-106">In order for these annotations and semantics to be useful, they must be implemented in both the host application and the effect file.</span></span> <span data-ttu-id="2f900-107">本檔說明利用 DirectX 效果架構強大功能的 DXSAS 標準，可讓主應用程式和工具以程式設計的方式)  ( fx 檔案共用 DirectX 效果，以及設計與 UI 的互動。</span><span class="sxs-lookup"><span data-stu-id="2f900-107">This document describes the DXSAS standard which leverages the power of the DirectX Effect Framework to enable host applications and tools to share DirectX effects (.fx files) programmatically, as well as to design interaction with UI.</span></span>

## <a name="background-information"></a><span data-ttu-id="2f900-108">背景資訊</span><span class="sxs-lookup"><span data-stu-id="2f900-108">Background Information</span></span>

<span data-ttu-id="2f900-109">標準注釋和語義是設計用來系結效果和 X 檔案參數，以裝載應用程式值。</span><span class="sxs-lookup"><span data-stu-id="2f900-109">Standard annotations and semantics are designed to bind effect and X-file parameters to host application values.</span></span> <span data-ttu-id="2f900-110">D3DX 效果架構 (或效果) 封裝呈現狀態。</span><span class="sxs-lookup"><span data-stu-id="2f900-110">The D3DX Effect Framework (or effects) encapsulates rendering state.</span></span> <span data-ttu-id="2f900-111">藉由封裝轉譯狀態 (（包括頂點、材質和圖元處理狀態）) 效果中，您可以建立效果的程式庫，其中涵蓋各式各樣的呈現選項。</span><span class="sxs-lookup"><span data-stu-id="2f900-111">By encapsulating rendering state (including vertex, texture, and pixel processing state) in an effect, you can create a library of effects covering a wide range of rendering options.</span></span> <span data-ttu-id="2f900-112">這可能包括在不同硬體類型上轉譯的選項，或使用單一或多重行程混合進行轉譯的選項。</span><span class="sxs-lookup"><span data-stu-id="2f900-112">This might include options such as rendering on different types of hardware, or rendering with single or multi-pass blending.</span></span> <span data-ttu-id="2f900-113">如需效果架構的詳細資訊，請參閱 [效果參考](dx9-graphics-reference-effects.md)。</span><span class="sxs-lookup"><span data-stu-id="2f900-113">For more information on the effect framework, you should refer to [Effect Reference](dx9-graphics-reference-effects.md).</span></span> <span data-ttu-id="2f900-114">DXSAS 建置於這個架構之上，讓開發人員能獲得更一致的體驗。</span><span class="sxs-lookup"><span data-stu-id="2f900-114">DXSAS builds on top of this framework allowing for a more consistent experience for developers.</span></span> <span data-ttu-id="2f900-115">當轉譯設定封裝成效果之後，DXSAS 標準可讓效果開發人員透過注釋公開效果參數的意圖。</span><span class="sxs-lookup"><span data-stu-id="2f900-115">Once the rendering setup is encapsulated in an effect, the DXSAS standard allows the effect developer to expose the intent of the effect parameters through annotations.</span></span> <span data-ttu-id="2f900-116">然後，任何主機應用程式或工具都可以讀取這些注釋 (而不只是設計用來使用符合標準之效果) 的注釋，也可以瞭解如何以設計方式使用效果。</span><span class="sxs-lookup"><span data-stu-id="2f900-116">These annotations can then be read by any host application or tool (not just the one that was designed to use the effect) that is compliant with the standard will understand how to use the effect in the manner that was designed.</span></span>

<span data-ttu-id="2f900-117">將裝載應用程式所支援的效果語義和注釋標準化，可讓效果作者建立可在多個專案中使用的效果，進而提升更廣大的效果使用者組合。</span><span class="sxs-lookup"><span data-stu-id="2f900-117">Standardizing the set of effect semantics and annotations that host applications support allow effect authors to create effects that can be used in multiple projects and thus promote a wider community of effect users.</span></span> <span data-ttu-id="2f900-118">DXSAS standard 讓開發人員可以讀取檔案，在工具之間交換，並讓開發人員利用協力廠商工具來撰寫管線的效果。</span><span class="sxs-lookup"><span data-stu-id="2f900-118">The DXSAS standard makes files readable by developers, exchangeable between tools, and enables developers to leverage 3rd party tools for authoring effects for their pipeline.</span></span>

<span data-ttu-id="2f900-119">本檔說明使用注釋表達效果參數意圖的 DXSAS 標準，以及定義主應用程式同意可讓其生效的主應用程式值集合。</span><span class="sxs-lookup"><span data-stu-id="2f900-119">This document describes the DXSAS standard which uses annotations to express the intent of effect parameters, as well as defining a collection of host application values that host applications agree to make available to an effect.</span></span>

## <a name="authoring-effects-with-standard-annotations-and-semantics"></a><span data-ttu-id="2f900-120">使用標準注釋和語義撰寫效果</span><span class="sxs-lookup"><span data-stu-id="2f900-120">Authoring Effects with Standard Annotations and Semantics</span></span>

<span data-ttu-id="2f900-121">如下圖所示，DXSAS 標準需要效果檔案中的批註，以及遵循此處所述指導方針的主應用程式來處理檔案。</span><span class="sxs-lookup"><span data-stu-id="2f900-121">As you can see from the following diagram, the DXSAS standard requires annotations in an effect file, as well as a host application that follows the guidelines described here to work with the file.</span></span>

![主機應用程式和效果檔案的 dxsas 標準圖表](images/sas-2.png)

<span data-ttu-id="2f900-123">主應用程式必須執行使用者介面邏輯和主機環境。</span><span class="sxs-lookup"><span data-stu-id="2f900-123">The host application must implement the user interface logic and the host environment.</span></span> <span data-ttu-id="2f900-124">若要執行 DXSAS 相容效果，請閱讀下列主題：</span><span class="sxs-lookup"><span data-stu-id="2f900-124">To implement DXSAS-compliant effects, read the following topics:</span></span>

-   <span data-ttu-id="2f900-125">[全域參數](global-parameter.md)會定義效果的相關資訊，例如版本或效果作者。</span><span class="sxs-lookup"><span data-stu-id="2f900-125">The [Global Parameter](global-parameter.md) defines information pertinent to the effect, such as the version, or the effect author.</span></span>
-   <span data-ttu-id="2f900-126">[資料](data-binding.md) 系結會定義參數的集合 (以及其型別和結構) ，可由可由主應用程式所設定的效果所使用的效果來設定。</span><span class="sxs-lookup"><span data-stu-id="2f900-126">[Data Binding](data-binding.md) defines the collection of parameters (as well as their type and structure) that can be used by an effect that can be set by the host application exposed to effects.</span></span>
-   <span data-ttu-id="2f900-127">若要將使用者介面控制項與效果參數產生關聯，請使用 [UI 注釋](ui-annotation.md)。</span><span class="sxs-lookup"><span data-stu-id="2f900-127">To associate a user-interface control with an effect parameter, use a [UI Annotation](ui-annotation.md).</span></span> <span data-ttu-id="2f900-128">這些批註包括： [SasUiMax](ui-annotation.md)、 [SasUiMin](ui-annotation.md)、 [SasUiSteps](ui-annotation.md)、 [SasUiStepsPower](ui-annotation.md)和 [SasUiStride](ui-annotation.md)。</span><span class="sxs-lookup"><span data-stu-id="2f900-128">These annotations include: [SasUiMax](ui-annotation.md), [SasUiMin](ui-annotation.md), [SasUiSteps](ui-annotation.md), [SasUiStepsPower](ui-annotation.md), and [SasUiStride](ui-annotation.md).</span></span>
-   <span data-ttu-id="2f900-129">若要使用外部檔案中包含的資料來初始化效果參數，請使用 [參數初始化注釋](parameter-initialization-annotation.md)。</span><span class="sxs-lookup"><span data-stu-id="2f900-129">To initialize an effect parameter with data contained in an external file, use a [Parameter Initialization Annotation](parameter-initialization-annotation.md).</span></span>
-   <span data-ttu-id="2f900-130">當主應用程式和效果之間的資料傳輸 (或反之亦然) ，當類型不完全相符時，就會發生 [轉換和轉換](casting-and-conversion.md) 。</span><span class="sxs-lookup"><span data-stu-id="2f900-130">When data is transferred between the host application and an effect (or vice versa), [Casting and Conversion](casting-and-conversion.md) will occur when the types do not exactly match.</span></span> <span data-ttu-id="2f900-131">此區段指定當來源和目標型別不同時，如何寫入資料。</span><span class="sxs-lookup"><span data-stu-id="2f900-131">This section specifies how data is written when the source and target types differ.</span></span> <span data-ttu-id="2f900-132">此外，您也可以使用 [ParameterValueModifiers](casting-and-conversion.md) 來修改主機應用程式應該如何解讀從效果參數讀取的資料。</span><span class="sxs-lookup"><span data-stu-id="2f900-132">In addition, use [ParameterValueModifiers](casting-and-conversion.md) to modify how the host application should interpret data read from the effect parameter.</span></span> <span data-ttu-id="2f900-133">這些批註包括： [SasNormalize](casting-and-conversion.md) 和 [SasUnits](casting-and-conversion.md)。</span><span class="sxs-lookup"><span data-stu-id="2f900-133">These annotations include: [SasNormalize](casting-and-conversion.md) and [SasUnits](casting-and-conversion.md).</span></span>

## <a name="case-sensitivity"></a><span data-ttu-id="2f900-134">區分大小寫</span><span class="sxs-lookup"><span data-stu-id="2f900-134">Case Sensitivity</span></span>

<span data-ttu-id="2f900-135">所有識別碼、語義和批註值都不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="2f900-135">All identifiers, semantics, and annotation values are case insensitive.</span></span> <span data-ttu-id="2f900-136">批註名稱 (不) 值會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="2f900-136">Annotation names (not values) are case sensitive.</span></span> <span data-ttu-id="2f900-137">批註名稱可由 D3DX 效果系統辨識，因此 SAS 批註名稱也是如此。</span><span class="sxs-lookup"><span data-stu-id="2f900-137">Annotation names are recognized by the D3DX effects system and therefore SAS annotation names are as well.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2f900-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="2f900-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f900-139">效果參考</span><span class="sxs-lookup"><span data-stu-id="2f900-139">Effect Reference</span></span>](dx9-graphics-reference-effects.md)
</dt> </dl>

 

 



