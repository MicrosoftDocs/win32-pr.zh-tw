---
title: 材質類型
description: 使用下列語法來宣告材質變數。
ms.assetid: 54db5432-dab8-4a4d-a4de-93c6fa640535
keywords:
- 材質類型 HLSL
topic_type:
- apiref
api_name:
- Texture type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 89568dc5cf24af38f916375795eea052c8b39200
ms.sourcegitcommit: 6f905c836d3fd04934fb3e5f1a56b4a421f7596f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/07/2020
ms.locfileid: "103681528"
---
# <a name="texture-type"></a><span data-ttu-id="5293f-104">材質類型</span><span class="sxs-lookup"><span data-stu-id="5293f-104">Texture type</span></span>

<span data-ttu-id="5293f-105">使用下列語法來宣告材質變數。</span><span class="sxs-lookup"><span data-stu-id="5293f-105">Use the following syntax to declare a texture variable.</span></span>

|                |
|----------------|
| <span data-ttu-id="5293f-106">**類型名稱;**</span><span class="sxs-lookup"><span data-stu-id="5293f-106">**Type Name;**</span></span> |

## <a name="parameters"></a><span data-ttu-id="5293f-107">參數</span><span class="sxs-lookup"><span data-stu-id="5293f-107">Parameters</span></span>
| <span data-ttu-id="5293f-108">項目</span><span class="sxs-lookup"><span data-stu-id="5293f-108">Item</span></span>                                                                                     | <span data-ttu-id="5293f-109">描述</span><span class="sxs-lookup"><span data-stu-id="5293f-109">Description</span></span>                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5293f-110"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>**類型**</span><span class="sxs-lookup"><span data-stu-id="5293f-110"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>**Type**</span></span><br/> | <span data-ttu-id="5293f-111">下列其中一種類型：材質 (不具類型，適用于回溯相容性) 、Texture1D、Texture1DArray、Texture2D、Texture2DArray、Texture3D、TextureCube。</span><span class="sxs-lookup"><span data-stu-id="5293f-111">One of the following types: texture (untyped, for backwards compatibility), Texture1D, Texture1DArray, Texture2D, Texture2DArray, Texture3D, TextureCube.</span></span> <span data-ttu-id="5293f-112">元素大小必須符合 4 32 位數量。</span><span class="sxs-lookup"><span data-stu-id="5293f-112">The element size must fit into 4 32-bit quantities.</span></span><br/> |
| <span data-ttu-id="5293f-113"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**名字**</span><span class="sxs-lookup"><span data-stu-id="5293f-113"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**</span></span><br/> | <span data-ttu-id="5293f-114">可唯一識別變數名稱的 ASCII 字串。</span><span class="sxs-lookup"><span data-stu-id="5293f-114">An ASCII string that uniquely identifies the variable name.</span></span><br/>                                                                                                                                                   |
## <a name="remarks"></a><span data-ttu-id="5293f-115">備註</span><span class="sxs-lookup"><span data-stu-id="5293f-115">Remarks</span></span>

<span data-ttu-id="5293f-116">使用材質有三個部分。</span><span class="sxs-lookup"><span data-stu-id="5293f-116">There are three parts to using a texture.</span></span>

1.  <span data-ttu-id="5293f-117">宣告材質變數。</span><span class="sxs-lookup"><span data-stu-id="5293f-117">Declaring a texture variable.</span></span> <span data-ttu-id="5293f-118">這是使用上述語法完成的。</span><span class="sxs-lookup"><span data-stu-id="5293f-118">This is done with the syntax shown above.</span></span> <span data-ttu-id="5293f-119">例如，這些都是有效的宣告。</span><span class="sxs-lookup"><span data-stu-id="5293f-119">For example, these are valid declarations.</span></span>

    ```
    texture g_MeshTexture;
    ```

    <span data-ttu-id="5293f-120">\- 或 -</span><span class="sxs-lookup"><span data-stu-id="5293f-120">\- or -</span></span>

    ```
    Texture2D g_MeshTexture;
    ```

2.  <span data-ttu-id="5293f-121">宣告和初始化取樣器物件。</span><span class="sxs-lookup"><span data-stu-id="5293f-121">Declaring and initializing a sampler object.</span></span> <span data-ttu-id="5293f-122">這是在 Direct3D 9 和 Direct3D 10 中略有不同的語法來完成。</span><span class="sxs-lookup"><span data-stu-id="5293f-122">This is done with slightly different syntax in Direct3D 9 and Direct3D 10.</span></span> <span data-ttu-id="5293f-123">如需有關取樣器物件語法的詳細資訊，請參閱 [ (DIRECTX HLSL) 的取樣器類型 ](dx-graphics-hlsl-sampler.md)。</span><span class="sxs-lookup"><span data-stu-id="5293f-123">For details about sampler object syntax, see [Sampler Type (DirectX HLSL)](dx-graphics-hlsl-sampler.md).</span></span>
3.  <span data-ttu-id="5293f-124">在著色器中叫用材質函數。</span><span class="sxs-lookup"><span data-stu-id="5293f-124">Invoking a texture function in a shader.</span></span>

<span data-ttu-id="5293f-125">Direct3D 9 與 Direct3D 10 之間的差異：</span><span class="sxs-lookup"><span data-stu-id="5293f-125">Differences between Direct3D 9 and Direct3D 10:</span></span>

<span data-ttu-id="5293f-126">Direct3D 9 使用 [內部紋理](dx-graphics-hlsl-intrinsic-functions.md) 函式來執行材質作業。</span><span class="sxs-lookup"><span data-stu-id="5293f-126">Direct3D 9 uses [intrinsic texture functions](dx-graphics-hlsl-intrinsic-functions.md) to perform texture operations.</span></span> <span data-ttu-id="5293f-127">此範例來自 [BasicHLSL 範例](/previous-versions/windows/desktop/bb153287(v%3Dvs.85)) ，並使用 [tex2D (s，t)  (DirectX HLSL) ](dx-graphics-hlsl-tex2d.md) 來執行材質取樣。</span><span class="sxs-lookup"><span data-stu-id="5293f-127">This example is from the [BasicHLSL Sample](/previous-versions/windows/desktop/bb153287(v%3Dvs.85)) and uses [tex2D(s, t) (DirectX HLSL)](dx-graphics-hlsl-tex2d.md) to perform texture sampling.</span></span>

<code>Output.RGBColor = tex2D(MeshTextureSampler, In.TextureUV) * In.Diffuse;</code>

<span data-ttu-id="5293f-128">Direct3D 10 會改為使用樣板 [化紋理物件](dx-graphics-hlsl-to-type.md) 。</span><span class="sxs-lookup"><span data-stu-id="5293f-128">Direct3D 10 uses [templated texture objects](dx-graphics-hlsl-to-type.md) instead.</span></span> <span data-ttu-id="5293f-129">以下是對等的材質運算範例。</span><span class="sxs-lookup"><span data-stu-id="5293f-129">Here is an example of the equivalent texture operation.</span></span>

<code>Output.RGBColor = g_MeshTexture.Sample(MeshTextureSampler, In.TextureUV) * In.Diffuse;</code>

## <a name="see-also"></a><span data-ttu-id="5293f-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5293f-130">See also</span></span>

[<span data-ttu-id="5293f-131"> (DirectX HLSL) 的資料類型 </span><span class="sxs-lookup"><span data-stu-id="5293f-131">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)
