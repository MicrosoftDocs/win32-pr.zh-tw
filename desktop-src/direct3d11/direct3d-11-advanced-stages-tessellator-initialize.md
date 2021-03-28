---
title: 如何初始化鑲嵌階段
description: 本主題說明如何初始化鑲嵌階段。
ms.assetid: 81f5461a-0938-4c46-b3e8-bef2bea125a5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50cfe00a4d59396f0dc1b0157f84e57e9cabc4a0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104990594"
---
# <a name="how-to-initialize-the-tessellator-stage"></a><span data-ttu-id="d8cc1-103">如何：初始化鑲嵌階段</span><span class="sxs-lookup"><span data-stu-id="d8cc1-103">How To: Initialize the Tessellator Stage</span></span>

<span data-ttu-id="d8cc1-104">一般而言，鑲嵌會將修補程式的精簡、使用者定義模型，以包含可程式化的詳細資料數量的幾何展開。</span><span class="sxs-lookup"><span data-stu-id="d8cc1-104">In general, tessellation expands the compact, user-defined, model of a patch into geometry that contains a programmable amount of detail.</span></span> <span data-ttu-id="d8cc1-105">幾何通常是一組表示詳細表面幾何的三角形。</span><span class="sxs-lookup"><span data-stu-id="d8cc1-105">The geometry is typically a set of triangles that represents detailed surface geometry.</span></span> <span data-ttu-id="d8cc1-106">本主題說明如何初始化鑲嵌階段。</span><span class="sxs-lookup"><span data-stu-id="d8cc1-106">This topic shows how to initialize the tessellator stage.</span></span>

<span data-ttu-id="d8cc1-107">鑲嵌階段是三個階段的第二個，可共同運作以 tessellate 或磚化介面。</span><span class="sxs-lookup"><span data-stu-id="d8cc1-107">The tessellator stage is the second of three stages that work together to tessellate or tile a surface.</span></span> <span data-ttu-id="d8cc1-108">第一個階段是輪廓著色器階段;它會針對每個修補程式進行一次，並設定 (fixed function 鑲嵌) 行為的下一個階段。</span><span class="sxs-lookup"><span data-stu-id="d8cc1-108">The first stage is the hull-shader stage; it operates once per patch and configures how the next stage (the fixed function tessellator) behaves.</span></span> <span data-ttu-id="d8cc1-109">輪廓著色器也會產生使用者定義輸出（例如輸出控制點），以及直接傳送至第三個階段（網域著色器階段）的鑲嵌的 patch 常數。</span><span class="sxs-lookup"><span data-stu-id="d8cc1-109">A hull shader also generates user-defined outputs such as output-control points and patch constants that are sent past the tessellator directly to the third stage, the domain-shader stage.</span></span> <span data-ttu-id="d8cc1-110">每個鑲嵌階段點都會叫用一次網域著色器，並評估介面位置。</span><span class="sxs-lookup"><span data-stu-id="d8cc1-110">A domain shader is invoked once per tessellator-stage point and evaluates surface positions.</span></span>

<span data-ttu-id="d8cc1-111">鑲嵌階段是固定的函式階段，沒有可產生的著色器，也沒有要設定的狀態。</span><span class="sxs-lookup"><span data-stu-id="d8cc1-111">The tessellator stage is a fixed function stage, there is no shader to generate, and no state to set.</span></span> <span data-ttu-id="d8cc1-112">它會從輪廓-著色器階段接收所有的設定狀態;一旦將輪廓著色器階段初始化之後，就會自動初始化鑲嵌階段。</span><span class="sxs-lookup"><span data-stu-id="d8cc1-112">It receives all of its setup state from the hull-shader stage; once the hull-shader stage has been initialized, the tessellator stage is automatically initialized.</span></span>

<span data-ttu-id="d8cc1-113">**若要初始化鑲嵌階段**</span><span class="sxs-lookup"><span data-stu-id="d8cc1-113">**To initialize the tessellator stage**</span></span>

-   <span data-ttu-id="d8cc1-114">使用 [**>id3d11devicecoNtext：： HSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader)，初始化輪廓著色器階段。</span><span class="sxs-lookup"><span data-stu-id="d8cc1-114">Initialize the hull-shader stage using [**ID3D11DeviceContext::HSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader).</span></span>

    ```
    void HSSetShader(
      ID3D11HullShader *pHullShader,  
      ID3D11ClassInstance *const *ppClassInstances,
      UINT NumClassInstances
    );
    ```

    

    <span data-ttu-id="d8cc1-115">*ppClassInstances* 是指向著色器介面陣列的指標，並以 [**ID3D11ClassInstance**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance) 指標和介面數目（由 *NumClassInstances* 表示）來表示。</span><span class="sxs-lookup"><span data-stu-id="d8cc1-115">*ppClassInstances* is a pointer to an array of shader interfaces, represented by [**ID3D11ClassInstance**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance) pointers and the number of interfaces, represented by *NumClassInstances*.</span></span> <span data-ttu-id="d8cc1-116">如果未使用，這些參數可以分別設定為 **Null** 和0。</span><span class="sxs-lookup"><span data-stu-id="d8cc1-116">If not used, these parameters can be set to **NULL** and 0 respectively.</span></span>

<span data-ttu-id="d8cc1-117">在將輪廓著色器階段初始化之後，您也應該初始化網域著色器階段。</span><span class="sxs-lookup"><span data-stu-id="d8cc1-117">After the hull-shader stage is initialized, you should also initialize the domain-shader stage.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d8cc1-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="d8cc1-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8cc1-119">如何使用 Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="d8cc1-119">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> <dt>

[<span data-ttu-id="d8cc1-120">鑲嵌式總覽</span><span class="sxs-lookup"><span data-stu-id="d8cc1-120">Tessellation Overview</span></span>](direct3d-11-advanced-stages-tessellation.md)
</dt> </dl>

 

 




