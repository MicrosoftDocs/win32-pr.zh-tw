---
description: 一組次要的轉譯介面支援直接從使用者記憶體指標傳遞頂點和索引資料。 這些介面僅支援頂點資料的單一資料流程。 如需詳細資訊，請參閱下列參考主題。
ms.assetid: 6f64cc17-cffc-4d18-acf2-73e400fa26f9
title: '從使用者記憶體指標轉譯 (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4b5499032e6fb92ea0f363bba2bd5fd961e53c7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104187508"
---
# <a name="rendering-from-user-memory-pointers-direct3d-9"></a><span data-ttu-id="658f0-105">從使用者記憶體指標轉譯 (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="658f0-105">Rendering from User Memory Pointers (Direct3D 9)</span></span>

<span data-ttu-id="658f0-106">一組次要的轉譯介面支援直接從使用者記憶體指標傳遞頂點和索引資料。</span><span class="sxs-lookup"><span data-stu-id="658f0-106">A secondary set of rendering interfaces supports passing vertex and index data directly from user memory pointers.</span></span> <span data-ttu-id="658f0-107">這些介面僅支援頂點資料的單一資料流程。</span><span class="sxs-lookup"><span data-stu-id="658f0-107">These interfaces support a single stream of vertex data only.</span></span> <span data-ttu-id="658f0-108">如需詳細資訊，請參閱下列參考主題。</span><span class="sxs-lookup"><span data-stu-id="658f0-108">For more information, see the following reference topics.</span></span>

-   [<span data-ttu-id="658f0-109">**IDirect3DDevice9::DrawPrimitiveUP**</span><span class="sxs-lookup"><span data-stu-id="658f0-109">**IDirect3DDevice9::DrawPrimitiveUP**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitiveup)
-   [<span data-ttu-id="658f0-110">**IDirect3DDevice9::DrawIndexedPrimitiveUP**</span><span class="sxs-lookup"><span data-stu-id="658f0-110">**IDirect3DDevice9::DrawIndexedPrimitiveUP**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitiveup)

<span data-ttu-id="658f0-111">這些方法會使用使用者記憶體指標所指定的資料來呈現，而不是使用頂點和索引緩衝區。</span><span class="sxs-lookup"><span data-stu-id="658f0-111">These methods render with data specified by user memory pointers, instead of vertex and index buffers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="658f0-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="658f0-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="658f0-113">呈現基本專案</span><span class="sxs-lookup"><span data-stu-id="658f0-113">Rendering Primitives</span></span>](rendering-primitives.md)
</dt> </dl>

 

 
