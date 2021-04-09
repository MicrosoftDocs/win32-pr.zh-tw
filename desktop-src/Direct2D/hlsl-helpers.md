---
title: HLSL 協助程式
description: 為了協助效果作者撰寫可連結圖元著色器，d2d1effecthelpers. hlsli 會以 helper 方法和宏的形式來定義一組 HLSL 語言延伸模組。
ms.assetid: 5D0BB99E-7C77-4D45-82E6-F038E4B752A4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec8f43447c16d93ef9e1839ac319c761b975222a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103931980"
---
# <a name="hlsl-helpers"></a><span data-ttu-id="96931-103">HLSL 協助程式</span><span class="sxs-lookup"><span data-stu-id="96931-103">HLSL Helpers</span></span>

<span data-ttu-id="96931-104">為了協助效果作者撰寫可連結圖元著色器，d2d1effecthelpers. hlsli 會以 helper 方法和宏的形式來定義一組 HLSL 語言延伸模組。</span><span class="sxs-lookup"><span data-stu-id="96931-104">To assist effect authors in writing linkable pixel shaders, d2d1effecthelpers.hlsli defines a set of HLSL language extensions in the form of helper methods and macros.</span></span>

<span data-ttu-id="96931-105">若要將 d2d1effecthelpers hlsli 加入至您的專案，請 \# 在 HLSL 檔案中加入 include 語句。</span><span class="sxs-lookup"><span data-stu-id="96931-105">To add d2d1effecthelpers.hlsli to your project, add an \#include statement in the HLSL file.</span></span> <span data-ttu-id="96931-106">d2d1effecthelpers 與其他 Direct2D 標頭位於相同的位置，例如 d2d1 .h;您可以從 HLSL 檔的屬性頁中參考它，方法是將宏 $ (WindowsSDK \_ IncludePath) 新增至其他 Include 目錄屬性。</span><span class="sxs-lookup"><span data-stu-id="96931-106">d2d1effecthelpers.hlsli is located in the same location as other Direct2D headers such as d2d1.h; it can be referenced from the HLSL file's property page by adding the macro $(WindowsSDK\_IncludePath) to the Additional Include Directories property.</span></span> <span data-ttu-id="96931-107">請注意， \# include 語句必須在任何預處理器指示詞之後，也就是已定義的 D2D \_ 輸入 \_ 計數。</span><span class="sxs-lookup"><span data-stu-id="96931-107">Note that the \#include statement must come after any preprocessor directives such D2D\_INPUT\_COUNT have been defined.</span></span>

``` syntax
#include <d2d1effecthelpers.hlsli>
```

<span data-ttu-id="96931-108">Direct2D 不支援連結計算或頂點著色器。</span><span class="sxs-lookup"><span data-stu-id="96931-108">Direct2D does not support linking compute or vertex shaders.</span></span> <span data-ttu-id="96931-109">但是，如果您的效果同時使用了頂點著色器和圖元著色器，則圖元著色器的輸出仍可連結。</span><span class="sxs-lookup"><span data-stu-id="96931-109">However, if your effect uses both a vertex shader and pixel shader, the output of the pixel shader can still be linked.</span></span>

## <a name="preprocessor-directives"></a><span data-ttu-id="96931-110">前置處理器指示詞</span><span class="sxs-lookup"><span data-stu-id="96931-110">Preprocessor Directives</span></span>

<span data-ttu-id="96931-111">需要預處理器指示詞才能傳達效果的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="96931-111">Preprocessor directives are required to communicate information about the effect.</span></span> <span data-ttu-id="96931-112">這包括每個輸入的輸入數目和取樣類型。</span><span class="sxs-lookup"><span data-stu-id="96931-112">This includes the number of inputs and sampling type of each input.</span></span> <span data-ttu-id="96931-113">下列值應該在相關著色器進入點上方的效果著色器程式碼中定義（如果適用）。</span><span class="sxs-lookup"><span data-stu-id="96931-113">The following values should be defined in the effect shader code above the relevant shader entry point when applicable.</span></span>

-   <span data-ttu-id="96931-114">`D2D_INPUT_COUNT <N>` ：宣告效果的材質輸入數目。</span><span class="sxs-lookup"><span data-stu-id="96931-114">`D2D_INPUT_COUNT <N>` : Declares the number of texture inputs to the effect.</span></span> <span data-ttu-id="96931-115">如果效果有不定數目的輸入，此值必須適當地設定為每個著色器進入點的範圍。</span><span class="sxs-lookup"><span data-stu-id="96931-115">If the effect has a variable number of inputs, this value must be scoped appropriately to each shader entry point.</span></span> <span data-ttu-id="96931-116">定義此值是必要的。</span><span class="sxs-lookup"><span data-stu-id="96931-116">Defining this value is mandatory.</span></span>
-   <span data-ttu-id="96931-117">`D2D_INPUT<N>_SIMPLE` ：宣告第 n 個輸入以使用簡單取樣。</span><span class="sxs-lookup"><span data-stu-id="96931-117">`D2D_INPUT<N>_SIMPLE` : Declares the Nth input to use simple sampling.</span></span> <span data-ttu-id="96931-118">如果未定義，則第 n 個輸入預設為 [複雜]。</span><span class="sxs-lookup"><span data-stu-id="96931-118">If not defined, the Nth input defaults to complex.</span></span> <span data-ttu-id="96931-119">定義此值是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="96931-119">Defining this value is optional.</span></span>
-   <span data-ttu-id="96931-120">`D2D_INPUT<N>_COMPLEX` ：宣告第 n 個輸入以使用複雜的取樣。</span><span class="sxs-lookup"><span data-stu-id="96931-120">`D2D_INPUT<N>_COMPLEX` : Declares the Nth input to use complex sampling.</span></span> <span data-ttu-id="96931-121">如果未定義，則第 n 個輸入預設為 [複雜]。</span><span class="sxs-lookup"><span data-stu-id="96931-121">If not defined, the Nth input defaults to complex.</span></span> <span data-ttu-id="96931-122">定義此值是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="96931-122">Defining this value is optional.</span></span>
-   <span data-ttu-id="96931-123">`D2D_REQUIRES_SCENE_POSITION` ：表示著色器函式會呼叫使用場景位置值的 helper 方法 (亦即， [D2DGetScenePosition](d2dgetsceneposition.md) helper 函數) 。</span><span class="sxs-lookup"><span data-stu-id="96931-123">`D2D_REQUIRES_SCENE_POSITION` : Indicates that the shader function calls helper methods that use the scene position value (namely, the [D2DGetScenePosition](d2dgetsceneposition.md) helper function).</span></span> <span data-ttu-id="96931-124">只有在必要時才會包含這個參數，因為每個連結的著色器只有一個函式可以使用此參數。</span><span class="sxs-lookup"><span data-stu-id="96931-124">This parameter should only be included when necessary, since only one function per linked shader can utilize this parameter.</span></span> <span data-ttu-id="96931-125">定義此值是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="96931-125">Defining this value is optional.</span></span>
-   <span data-ttu-id="96931-126">`D2D_CUSTOM_ENTRY` ：表示圖元著色器函式會使用自訂頂點著色器的輸出，因此會宣告其輸入參數。</span><span class="sxs-lookup"><span data-stu-id="96931-126">`D2D_CUSTOM_ENTRY` : Indicates that the pixel shader function consumes the output of a custom vertex shader, and thus will declare its input parameters.</span></span> <span data-ttu-id="96931-127">所有自訂頂點著色器輸入都會使用複雜的取樣，而且無法使用另一個著色器函式的輸出 (亦即，它們只是可連結後的) 。</span><span class="sxs-lookup"><span data-stu-id="96931-127">All custom vertex shader inputs use complex sampling, and cannot consume the output of another shader function (i.e. they are only post-linkable).</span></span> <span data-ttu-id="96931-128">定義此值是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="96931-128">Defining this value is optional.</span></span>

<span data-ttu-id="96931-129">例如：</span><span class="sxs-lookup"><span data-stu-id="96931-129">For example:</span></span>

``` syntax
#define D2D_INPUT_COUNT 3
#define D2D_INPUT0_SIMPLE
#define D2D_INPUT1_SIMPLE
#define D2D_INPUT2_COMPLEX
#include <d2d1effecthelpers.hlsli>
          
```

## <a name="helper-functions"></a><span data-ttu-id="96931-130">輔助函式</span><span class="sxs-lookup"><span data-stu-id="96931-130">Helper Functions</span></span>

<span data-ttu-id="96931-131">Helper 函式可用來取代某些原生 HLSL 內建函式。</span><span class="sxs-lookup"><span data-stu-id="96931-131">Helper functions are used as a replacement for some native HLSL intrinsic functions.</span></span> <span data-ttu-id="96931-132">在編譯時期，這些 helper 函式會由 Direct2D 重新定義為適當的版本，視編譯目標型別 (完整著色器或匯出函數) 而定。</span><span class="sxs-lookup"><span data-stu-id="96931-132">At compile time, these helper functions are redefined by Direct2D into the appropriate version depending on the compilation target type (full shader or export function).</span></span>

<span data-ttu-id="96931-133">Helper 函式：</span><span class="sxs-lookup"><span data-stu-id="96931-133">The helper functions:</span></span>

<dl>

[<span data-ttu-id="96931-134">D2DGetInput</span><span class="sxs-lookup"><span data-stu-id="96931-134">D2DGetInput</span></span>](d2dgetinput.md)  
[<span data-ttu-id="96931-135">D2DSampleInput</span><span class="sxs-lookup"><span data-stu-id="96931-135">D2DSampleInput</span></span>](d2dsampleinput.md)  
[<span data-ttu-id="96931-136">D2DSampleInputAtOffset</span><span class="sxs-lookup"><span data-stu-id="96931-136">D2DSampleInputAtOffset</span></span>](d2dsampleinputatoffset.md)  
[<span data-ttu-id="96931-137">D2DSampleInputAtPosition</span><span class="sxs-lookup"><span data-stu-id="96931-137">D2DSampleInputAtPosition</span></span>](d2dsampleinputatposition.md)  
[<span data-ttu-id="96931-138">D2DGetInputCoordinate</span><span class="sxs-lookup"><span data-stu-id="96931-138">D2DGetInputCoordinate</span></span>](d2dgetinputcoordinate.md)  
[<span data-ttu-id="96931-139">D2DGetScenePosition</span><span class="sxs-lookup"><span data-stu-id="96931-139">D2DGetScenePosition</span></span>](d2dgetsceneposition.md)  
[<span data-ttu-id="96931-140">D2D \_ PS \_ 專案</span><span class="sxs-lookup"><span data-stu-id="96931-140">D2D\_PS\_ENTRY</span></span>](d2d-ps-entry.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="96931-141">相關主題</span><span class="sxs-lookup"><span data-stu-id="96931-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="96931-142">效果著色器連結</span><span class="sxs-lookup"><span data-stu-id="96931-142">Effect Shader Linking</span></span>](effect-shader-linking.md)
</dt> </dl>

 

 




