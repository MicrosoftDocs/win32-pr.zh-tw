---
description: 定義可套用至完整網格或網格個別臉部的基本材質色彩。 功率是材質的反射指數。
ms.assetid: vs|directx_sdk|~\material.htm
title: Material
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54c13d201152350a8a61950bb609f73cbdb2a3aa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467437"
---
# <a name="material"></a><span data-ttu-id="dbf44-104">Material</span><span class="sxs-lookup"><span data-stu-id="dbf44-104">Material</span></span>

<span data-ttu-id="dbf44-105">定義可套用至完整網格或網格個別臉部的基本材質色彩。</span><span class="sxs-lookup"><span data-stu-id="dbf44-105">Defines a basic material color that can be applied to either a complete mesh or a mesh's individual faces.</span></span> <span data-ttu-id="dbf44-106">功率是材質的反射指數。</span><span class="sxs-lookup"><span data-stu-id="dbf44-106">The power is the specular exponent of the material.</span></span>

``` syntax
template Material
{
    < 3D82AB4D-62DA-11CF-AB39-0020AF71E433 >
    ColorRGBA faceColor;
    FLOAT power;
    ColorRGB specularColor;
    ColorRGB emissiveColor;
    [...]
} 
```

<span data-ttu-id="dbf44-107">其中：</span><span class="sxs-lookup"><span data-stu-id="dbf44-107">Where:</span></span>

-   <span data-ttu-id="dbf44-108">faceColor-臉部色彩。</span><span class="sxs-lookup"><span data-stu-id="dbf44-108">faceColor - Face color.</span></span> <span data-ttu-id="dbf44-109">ColorRGBA 範本。</span><span class="sxs-lookup"><span data-stu-id="dbf44-109">A ColorRGBA template.</span></span> <span data-ttu-id="dbf44-110">請參閱 [**ColorRGBA**](colorrgba.md)。</span><span class="sxs-lookup"><span data-stu-id="dbf44-110">See [**ColorRGBA**](colorrgba.md).</span></span>
-   <span data-ttu-id="dbf44-111">電源材質反射色彩指數。</span><span class="sxs-lookup"><span data-stu-id="dbf44-111">power - Material specular color exponent.</span></span>
-   <span data-ttu-id="dbf44-112">specularColor-材質反射色彩。</span><span class="sxs-lookup"><span data-stu-id="dbf44-112">specularColor - Material specular color.</span></span> <span data-ttu-id="dbf44-113">ColorRGB 範本。</span><span class="sxs-lookup"><span data-stu-id="dbf44-113">A ColorRGB template.</span></span> <span data-ttu-id="dbf44-114">請參閱 [**ColorRGB**](colorrgb.md)。</span><span class="sxs-lookup"><span data-stu-id="dbf44-114">See [**ColorRGB**](colorrgb.md).</span></span>
-   <span data-ttu-id="dbf44-115">emissiveColor-材質放射色彩。</span><span class="sxs-lookup"><span data-stu-id="dbf44-115">emissiveColor - Material emissive color.</span></span> <span data-ttu-id="dbf44-116">ColorRGB 範本。</span><span class="sxs-lookup"><span data-stu-id="dbf44-116">A ColorRGB template.</span></span> <span data-ttu-id="dbf44-117">請參閱 [**ColorRGB**](colorrgb.md)。</span><span class="sxs-lookup"><span data-stu-id="dbf44-117">See [**ColorRGB**](colorrgb.md).</span></span>

> [!Note]  
> <span data-ttu-id="dbf44-118">環境色彩需要 Alpha 元件。</span><span class="sxs-lookup"><span data-stu-id="dbf44-118">The ambient color requires an alpha component.</span></span>

 

<span data-ttu-id="dbf44-119">[**TextureFilename**](texturefilename.md) 是選擇性的資料物件。</span><span class="sxs-lookup"><span data-stu-id="dbf44-119">[**TextureFilename**](texturefilename.md) is an optional data object.</span></span> <span data-ttu-id="dbf44-120">如果這個物件不存在，就會 uNtextured 臉部。</span><span class="sxs-lookup"><span data-stu-id="dbf44-120">If this object is not present, the face is untextured.</span></span>

## <a name="see-also"></a><span data-ttu-id="dbf44-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dbf44-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbf44-122">範本</span><span class="sxs-lookup"><span data-stu-id="dbf44-122">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



