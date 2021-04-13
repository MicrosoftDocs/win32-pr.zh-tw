---
description: Direct3D 會維持最多8個目前材質的清單。 它會將這些材質混合到其呈現的所有基本型別。 只有建立為材質介面指標的紋理，才能在目前的材質集中使用。
ms.assetid: 5a58c915-7b67-45a7-9493-6657c75aaa10
title: '將目前的材質指派 (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e7ae6d603d9547841628f9395889095533cf3e2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468577"
---
# <a name="assigning-the-current-textures-direct3d-9"></a><span data-ttu-id="6471c-105">將目前的材質指派 (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="6471c-105">Assigning the Current Textures (Direct3D 9)</span></span>

<span data-ttu-id="6471c-106">Direct3D 會維持最多8個目前材質的清單。</span><span class="sxs-lookup"><span data-stu-id="6471c-106">Direct3D maintains a list of up to eight current textures.</span></span> <span data-ttu-id="6471c-107">它會將這些材質混合到其呈現的所有基本型別。</span><span class="sxs-lookup"><span data-stu-id="6471c-107">It blends these textures onto all the primitive it renders.</span></span> <span data-ttu-id="6471c-108">只有建立為材質介面指標的紋理，才能在目前的材質集中使用。</span><span class="sxs-lookup"><span data-stu-id="6471c-108">Only textures created as texture interface pointers can be used in the set of current textures.</span></span>

<span data-ttu-id="6471c-109">應用程式會呼叫 [**IDirect3DDevice9：： SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) 方法，將材質指派給目前材質的集合。</span><span class="sxs-lookup"><span data-stu-id="6471c-109">Applications call the [**IDirect3DDevice9::SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) method to assign textures into the set of current textures.</span></span> <span data-ttu-id="6471c-110">第一個參數必須是0-7 （含）範圍內的數位。</span><span class="sxs-lookup"><span data-stu-id="6471c-110">The first parameter must be a number in the range of 0-7, inclusive.</span></span> <span data-ttu-id="6471c-111">傳遞紋理介面指標做為第二個參數。</span><span class="sxs-lookup"><span data-stu-id="6471c-111">Pass the texture interface pointer as the second parameter.</span></span>

<span data-ttu-id="6471c-112">下列 c + + 程式碼範例會示範如何將材質指派給目前的材質集。</span><span class="sxs-lookup"><span data-stu-id="6471c-112">The following C++ code example demonstrates how a texture can be assigned to the set of current textures.</span></span>


```
// This code example assumes that the variable lpd3dDev is a
// valid pointer to an IDirect3DDevice9 interface and pTexture
// is a valid pointer to an IDirect3DBaseTexture9 interface.

// Set the third texture.
d3dDevice->SetTexture(2, pTexture);
```



> [!Note]  
> <span data-ttu-id="6471c-113">軟體裝置不支援一次將材質指派給一個以上的材質階段。</span><span class="sxs-lookup"><span data-stu-id="6471c-113">Software devices do not support assigning a texture to more than one texture stage at a time.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="6471c-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="6471c-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6471c-115">材質混色</span><span class="sxs-lookup"><span data-stu-id="6471c-115">Texture Blending</span></span>](texture-blending.md)
</dt> </dl>

 

 
