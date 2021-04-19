---
description: 效果是藉由將它載入效果架構來建立。
ms.assetid: b0a12620-4f8f-44d9-bc73-2c3ab30f80af
title: " (Direct3D 10 建立效果) "
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b630bae35b8e1390a4be77e5cb5e4aaa3f41d9c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106984149"
---
# <a name="create-an-effect-direct3d-10"></a><span data-ttu-id="3564b-103"> (Direct3D 10 建立效果) </span><span class="sxs-lookup"><span data-stu-id="3564b-103">Create an Effect (Direct3D 10)</span></span>

<span data-ttu-id="3564b-104">效果是藉由將它載入效果架構來建立。</span><span class="sxs-lookup"><span data-stu-id="3564b-104">An effect is created by loading it into the effects framework.</span></span> <span data-ttu-id="3564b-105">如果從未編譯過此效果，則會在建立時進行編譯。</span><span class="sxs-lookup"><span data-stu-id="3564b-105">If the effect has never been compiled, it will be compiled when it is created.</span></span> <span data-ttu-id="3564b-106">您可以藉由呼叫 [**D3DX10CreateEffectFromMemory**](d3dx10createeffectfrommemory.md)來建立已載入記憶體的效果。</span><span class="sxs-lookup"><span data-stu-id="3564b-106">Effects that are already loaded into memory can be created by calling [**D3DX10CreateEffectFromMemory**](d3dx10createeffectfrommemory.md).</span></span> <span data-ttu-id="3564b-107">下列程式碼範例會使用 [**D3DX10CreateEffectFromFile**](d3dx10createeffectfromfile.md) 來建立檔案的效果。</span><span class="sxs-lookup"><span data-stu-id="3564b-107">The following code example uses [**D3DX10CreateEffectFromFile**](d3dx10createeffectfromfile.md) to create an effect from a file.</span></span>


```
ID3D10Effect* g_pEffect10 = NULL; 

// Read the effect file 
D3DX10CreateEffectFromFile( "BasicHLSL10.fx", NULL, NULL,
  D3D10_SHADER_ENABLE_STRICTNESS, 0, pd3dDevice, NULL, NULL, 
  &g_pEffect10, NULL );
```



<span data-ttu-id="3564b-108">讀取效果需要與編譯效果相同的參數，以及裝置和集區。</span><span class="sxs-lookup"><span data-stu-id="3564b-108">Reading an effect requires the same parameters as compiling an effect, plus a device and a pool.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3564b-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="3564b-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3564b-110">轉譯 (Direct3D 10) 的效果 </span><span class="sxs-lookup"><span data-stu-id="3564b-110">Rendering an Effect (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 



