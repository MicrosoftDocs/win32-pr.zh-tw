---
description: Array.blit 一詞是 &\# 0034; bit block transfer 的速記，&\# 0034; 這是將資料區塊從記憶體中的一個位置傳送到另一個位置的進程。
ms.assetid: 5f2aed2e-66d2-40e6-be35-92c3f92d17bd
title: " (Direct3D 9) 複製表面"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50000e3b620c4d2fd217695551d898e5892430ba
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970112"
---
# <a name="copying-surfaces-direct3d-9"></a><span data-ttu-id="d5f61-103"> (Direct3D 9) 複製表面</span><span class="sxs-lookup"><span data-stu-id="d5f61-103">Copying Surfaces (Direct3D 9)</span></span>

<span data-ttu-id="d5f61-104">詞彙 array.blit 是「位區塊傳輸」的縮寫，這是將資料區塊從記憶體中的一個位置傳送到另一個位置的程式。</span><span class="sxs-lookup"><span data-stu-id="d5f61-104">The term blit is shorthand for "bit block transfer," which is the process of transferring blocks of data from one place in memory to another.</span></span> <span data-ttu-id="d5f61-105">Blitting 設備磁碟機介面 (DDI) 繼續在 Direct3D 9 中用來做為每個框架移動大型矩形的主要機制，也就是複製導向 IDirect3DDevice9 背後的機制 [**：:P 重發**](/windows/desktop/api) 的方法。</span><span class="sxs-lookup"><span data-stu-id="d5f61-105">The blitting device driver interface (DDI) continues to be used in Direct3D 9 as the primary mechanism for moving large rectangles of pixels on a per-frame basis, the mechanism behind the copy-oriented [**IDirect3DDevice9::Present**](/windows/desktop/api) method.</span></span> <span data-ttu-id="d5f61-106">Array.blit 作業中的圖稿傳輸是由 [**IDirect3DDevice9：： UpdateTexture**](/windows/desktop/api) 方法所執行。</span><span class="sxs-lookup"><span data-stu-id="d5f61-106">The transportation of artwork in the blit operation is performed by the [**IDirect3DDevice9::UpdateTexture**](/windows/desktop/api) method.</span></span> <span data-ttu-id="d5f61-107">您也可以使用 [**IDirect3DDevice9：： UpdateSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface) 方法（複製圖元的矩形子集），在 Direct3D 9 中複製作品。</span><span class="sxs-lookup"><span data-stu-id="d5f61-107">Artwork can also be copied in Direct3D 9 by using the [**IDirect3DDevice9::UpdateSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface) method, which copies a rectangular subset of pixels.</span></span>

> [!Note]  
> <span data-ttu-id="d5f61-108">Direct3D 9 提供 D3DX 函式，可讓您從檔案載入圖片、套用色彩轉換，以及調整圖形大小。</span><span class="sxs-lookup"><span data-stu-id="d5f61-108">Direct3D 9 provides D3DX functions that enable you to load artwork from files, apply color conversion, and resize artwork.</span></span> <span data-ttu-id="d5f61-109">如需可用函式的詳細資訊，請參閱 [D3DX 9 中的材質函數](dx9-graphics-reference-d3dx-functions-texture.md)。</span><span class="sxs-lookup"><span data-stu-id="d5f61-109">For more information about the available functions see [Texture Functions in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="d5f61-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="d5f61-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5f61-111">Direct3D 表面</span><span class="sxs-lookup"><span data-stu-id="d5f61-111">Direct3D Surfaces</span></span>](direct3d-surfaces.md)
</dt> <dt>

[<span data-ttu-id="d5f61-112">**IDirect3DDevice9::StretchRect**</span><span class="sxs-lookup"><span data-stu-id="d5f61-112">**IDirect3DDevice9::StretchRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect)
</dt> <dt>

<span data-ttu-id="d5f61-113">**IDirect3DDevice9::StretchRect**</span><span class="sxs-lookup"><span data-stu-id="d5f61-113">**IDirect3DDevice9::StretchRect**</span></span>
</dt> </dl>

 

 
