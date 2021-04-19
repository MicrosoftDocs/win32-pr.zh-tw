---
description: 用法類似于參數的範圍，因為它會定義參數有效的範圍。
ms.assetid: 9ba10dba-626f-4cb8-8dc2-1419329b199e
title: " (Direct3D 9) 的使用方式和常值"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5ca6f010d2c1e05055fd4427b8b5f7d4ab445ae
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106971945"
---
# <a name="usages-and-literals-direct3d-9"></a><span data-ttu-id="b179e-103"> (Direct3D 9) 的使用方式和常值</span><span class="sxs-lookup"><span data-stu-id="b179e-103">Usages and Literals (Direct3D 9)</span></span>

<span data-ttu-id="b179e-104">用法類似于參數的範圍，因為它會定義參數有效的範圍。</span><span class="sxs-lookup"><span data-stu-id="b179e-104">Usage is similar to a parameter's scope, because it defines the scope in which the parameter is valid.</span></span>



|        |                                                                                                                                                                                                                                                                                     |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b179e-105">值</span><span class="sxs-lookup"><span data-stu-id="b179e-105">Value</span></span>  | <span data-ttu-id="b179e-106">描述</span><span class="sxs-lookup"><span data-stu-id="b179e-106">Description</span></span>                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="b179e-107">const</span><span class="sxs-lookup"><span data-stu-id="b179e-107">const</span></span>  | <span data-ttu-id="b179e-108">參數在所有函式的範圍內都是常數。</span><span class="sxs-lookup"><span data-stu-id="b179e-108">The parameter will be constant within the scope of all functions.</span></span> <span data-ttu-id="b179e-109"> (請注意，這類參數仍然可以使用 [**ID3DXEffect**](id3dxeffect.md) 或 [**ID3DXEffectCompiler**](id3dxeffectcompiler.md)寫入，因為這會發生在所有函數的範圍之外。 ) </span><span class="sxs-lookup"><span data-stu-id="b179e-109">(Note that such parameters can still be written to with either [**ID3DXEffect**](id3dxeffect.md) or [**ID3DXEffectCompiler**](id3dxeffectcompiler.md), because this occurs outside the scope of all functions.)</span></span> |
| <span data-ttu-id="b179e-110">共用</span><span class="sxs-lookup"><span data-stu-id="b179e-110">shared</span></span> | <span data-ttu-id="b179e-111">此參數將會在效果集區中共用。</span><span class="sxs-lookup"><span data-stu-id="b179e-111">The parameter will be shared in the effect pool.</span></span>                                                                                                                                                                                                                                    |
| <span data-ttu-id="b179e-112">static</span><span class="sxs-lookup"><span data-stu-id="b179e-112">static</span></span> | <span data-ttu-id="b179e-113">應用程式不會看到參數，也就是您無法從 [**ID3DXEffect**](id3dxeffect.md) 或 [**ID3DXEffectCompiler**](id3dxeffectcompiler.md)存取。</span><span class="sxs-lookup"><span data-stu-id="b179e-113">The parameter will be invisible to the application, that is, you cannot access them from [**ID3DXEffect**](id3dxeffect.md) or [**ID3DXEffectCompiler**](id3dxeffectcompiler.md).</span></span>                                                                                                  |



 

<span data-ttu-id="b179e-114">將參數標記為常值表示它的值永遠不會變更。</span><span class="sxs-lookup"><span data-stu-id="b179e-114">Marking a parameter as literal indicates that its value will never change.</span></span> <span data-ttu-id="b179e-115">這可讓效果編譯器進行額外的優化。</span><span class="sxs-lookup"><span data-stu-id="b179e-115">This enables the effect compiler to do extra optimization.</span></span>

<span data-ttu-id="b179e-116">只有非共用的最上層參數可以標記為常值。</span><span class="sxs-lookup"><span data-stu-id="b179e-116">Only non-shared top-level parameters can be marked as literal.</span></span> <span data-ttu-id="b179e-117">參數只能使用 [**ID3DXEffectCompiler**](id3dxeffectcompiler.md)標示為常值。</span><span class="sxs-lookup"><span data-stu-id="b179e-117">Parameters can only be marked as literal with [**ID3DXEffectCompiler**](id3dxeffectcompiler.md).</span></span> <span data-ttu-id="b179e-118">無法使用 [**ID3DXEffect**](id3dxeffect.md)來設定常值。</span><span class="sxs-lookup"><span data-stu-id="b179e-118">Literal values cannot be set with [**ID3DXEffect**](id3dxeffect.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b179e-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="b179e-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b179e-120">效果格式</span><span class="sxs-lookup"><span data-stu-id="b179e-120">Effect Format</span></span>](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



