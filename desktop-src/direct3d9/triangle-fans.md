---
description: 三角形的風扇類似于三角形的帶狀線，不同之處在于所有三角形都會共用一個頂點，如下圖所示。
ms.assetid: a1fbfd78-121f-4f79-9ba8-44f23356a432
title: " (Direct3D 9) 的三角形風扇"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2357af0d999cc759453e34cd278f61064a637cfd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104564665"
---
# <a name="triangle-fans-direct3d-9"></a><span data-ttu-id="9c30f-103"> (Direct3D 9) 的三角形風扇</span><span class="sxs-lookup"><span data-stu-id="9c30f-103">Triangle Fans (Direct3D 9)</span></span>

<span data-ttu-id="9c30f-104">三角形的風扇類似于三角形的帶狀線，不同之處在于所有三角形都會共用一個頂點，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="9c30f-104">A triangle fan is similar to a triangle strip, except that all the triangles share one vertex, as shown in the following illustration.</span></span>

![三角形風扇的圖例](images/trifan.gif)

<span data-ttu-id="9c30f-106">系統會使用頂點 v2、v3 和 v1 來繪製第一個三角形;v3、v4 和 v1 以繪製第二個三角形;v4、v5 和 v1，以繪製第三個三角形;依此類推。</span><span class="sxs-lookup"><span data-stu-id="9c30f-106">The system uses vertices v2, v3, and v1 to draw the first triangle; v3, v4, and v1 to draw the second triangle; v4, v5, and v1 to draw the third triangle; and so on.</span></span> <span data-ttu-id="9c30f-107">啟用一般陰影時，系統會以其第一個頂點的色彩為三角形加上陰影。</span><span class="sxs-lookup"><span data-stu-id="9c30f-107">When flat shading is enabled, the system shades the triangle with the color from its first vertex.</span></span>

<span data-ttu-id="9c30f-108">下圖說明呈現的三角形風扇。</span><span class="sxs-lookup"><span data-stu-id="9c30f-108">The following illustration depicts a rendered triangle fan.</span></span>

![呈現三角形風扇的圖例](images/tfan2.gif)

<span data-ttu-id="9c30f-110">下列程式碼示範如何建立此三角形風扇的頂點。</span><span class="sxs-lookup"><span data-stu-id="9c30f-110">The following code shows how to create vertices for this triangle fan.</span></span>


```
struct CUSTOMVERTEX
{
    float x,y,z;
};

CUSTOMVERTEX Vertices[] = 
{
    { 0.0, 0.0, 0.0},
    {-5.0, 5.0, 0.0},
    {-3.0,  7.0, 0.0},
    { 0.0, 10.0, 0.0},
    { 3.0,  7.0, 0.0},
    { 5.0,  5.0, 0.0},
};
```



<span data-ttu-id="9c30f-111">下列程式碼範例顯示如何使用 [**IDirect3DDevice9：:D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)，在 Direct3D 9 中轉譯此三角形風扇。</span><span class="sxs-lookup"><span data-stu-id="9c30f-111">The code example below shows how to render this triangle fan in Direct3D 9 using [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).</span></span>


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_TRIANGLEFAN, 0, 4 );
```



<span data-ttu-id="9c30f-112">Direct3D 10 或更新版本不支援三角形風扇。</span><span class="sxs-lookup"><span data-stu-id="9c30f-112">Triangle fans are not supported in Direct3D 10 or later.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9c30f-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="9c30f-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c30f-114">基本</span><span class="sxs-lookup"><span data-stu-id="9c30f-114">Primitives</span></span>](primitives.md)
</dt> </dl>

 

 
