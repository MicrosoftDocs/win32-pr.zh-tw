---
description: 本章節包含 Direct3D 10 圖形中 D3DX 公用程式程式庫所提供之元件物件模型 (COM) 介面的參考資訊。
ms.assetid: c57d9c39-3f30-4205-9b0a-665fe53f2b14
title: " (Direct3D 10 圖形) 的 D3DX 介面"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c064edce5d5841875eb3148bf74b18f50f93081
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408011"
---
# <a name="d3dx-interfaces-direct3d-10-graphics"></a><span data-ttu-id="217ce-103"> (Direct3D 10 圖形) 的 D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="217ce-103">D3DX Interfaces (Direct3D 10 Graphics)</span></span>

<span data-ttu-id="217ce-104">本章節包含 D3DX 公用程式程式庫所提供之元件物件模型 (COM) 介面的參考資訊。</span><span class="sxs-lookup"><span data-stu-id="217ce-104">This section contains reference information for the component object model (COM) interfaces provided by the D3DX utility library.</span></span> <span data-ttu-id="217ce-105">下列介面適用于 D3DX 公用程式程式庫。</span><span class="sxs-lookup"><span data-stu-id="217ce-105">The following interfaces are used with the D3DX utility library.</span></span>



| <span data-ttu-id="217ce-106">介面</span><span class="sxs-lookup"><span data-stu-id="217ce-106">Interfaces</span></span>                                                     | <span data-ttu-id="217ce-107">描述</span><span class="sxs-lookup"><span data-stu-id="217ce-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="217ce-108">**ID3DX10DataLoader 介面**</span><span class="sxs-lookup"><span data-stu-id="217ce-108">**ID3DX10DataLoader Interface**</span></span>](id3dx10dataloader.md)       | <span data-ttu-id="217ce-109">[**ID3DX10ThreadPump 介面**](id3dx10threadpump.md)用來以非同步方式載入資料的資料載入物件。</span><span class="sxs-lookup"><span data-stu-id="217ce-109">Data loading object used by [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md) for loading data asynchronously.</span></span><br/>                                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="217ce-110">**ID3DX10DataProcessor 介面**</span><span class="sxs-lookup"><span data-stu-id="217ce-110">**ID3DX10DataProcessor Interface**</span></span>](id3dx10dataprocessor.md) | <span data-ttu-id="217ce-111">[**ID3DX10ThreadPump 介面**](id3dx10threadpump.md)使用的資料處理物件，以非同步方式處理載入的資料。</span><span class="sxs-lookup"><span data-stu-id="217ce-111">Data processing object used by [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md) for processing loaded data asynchronously.</span></span><br/>                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="217ce-112">**ID3DX10Font 介面**</span><span class="sxs-lookup"><span data-stu-id="217ce-112">**ID3DX10Font Interface**</span></span>](id3dx10font.md)                   | <span data-ttu-id="217ce-113">ID3DX10Font 介面會封裝在特定裝置上呈現特定字型所需的材質和資源。</span><span class="sxs-lookup"><span data-stu-id="217ce-113">The ID3DX10Font interface encapsulates the textures and resources needed to render a specific font on a specific device.</span></span><br/>                                                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="217ce-114">**ID3DX10Mesh 介面**</span><span class="sxs-lookup"><span data-stu-id="217ce-114">**ID3DX10Mesh Interface**</span></span>](id3dx10mesh.md)                   | <span data-ttu-id="217ce-115">應用程式會使用 ID3DX10Mesh 介面的方法來操作網格物件。</span><span class="sxs-lookup"><span data-stu-id="217ce-115">Applications use the methods of the ID3DX10Mesh interface to manipulate mesh objects.</span></span><br/>                                                                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="217ce-116">**ID3DX10MeshBuffer 介面**</span><span class="sxs-lookup"><span data-stu-id="217ce-116">**ID3DX10MeshBuffer Interface**</span></span>](id3dx10meshbuffer.md)       |                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="217ce-117">**ID3DX10SkinInfo 介面**</span><span class="sxs-lookup"><span data-stu-id="217ce-117">**ID3DX10SkinInfo Interface**</span></span>](id3dx10skininfo.md)           | <span data-ttu-id="217ce-118">ID3DX10SkinInfo 可讓您優化、處理及手動設定網格中的骨骼與頂點之間的關聯性 (請參閱 [維琪百科) 上的框架動畫](https://en.wikipedia.org/wiki/Skeletal_animation) 。</span><span class="sxs-lookup"><span data-stu-id="217ce-118">ID3DX10SkinInfo allows you to optimize, process, and manually set the relationship between bones and vertices in your meshes (see [Skeletal Animation on Wikipedia](https://en.wikipedia.org/wiki/Skeletal_animation)).</span></span> <span data-ttu-id="217ce-119">它最適合用來製作 DCC Apps 所匯出的. x 檔案 (例如 3DS Max 和 Maya) 更容易使用硬體，以及改善 skinned 網格在軟體轉譯模式中的呈現速度。</span><span class="sxs-lookup"><span data-stu-id="217ce-119">It is most useful for making .x files exported by DCC Apps (such as 3DS Max and Maya) more hardware-friendly, and for improving the render speed of your skinned meshes in software render mode.</span></span><br/> |
| [<span data-ttu-id="217ce-120">**ID3DX10Sprite 介面**</span><span class="sxs-lookup"><span data-stu-id="217ce-120">**ID3DX10Sprite Interface**</span></span>](id3dx10sprite.md)               | <span data-ttu-id="217ce-121">ID3DX10Sprite 介面提供一組方法，可使用 Microsoft Direct3D 簡化繪製 sprite 的程式。</span><span class="sxs-lookup"><span data-stu-id="217ce-121">The ID3DX10Sprite interface provides a set of methods that simplify the process of drawing sprites using Microsoft Direct3D.</span></span><br/>                                                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="217ce-122">**ID3DX10ThreadPump 介面**</span><span class="sxs-lookup"><span data-stu-id="217ce-122">**ID3DX10ThreadPump Interface**</span></span>](id3dx10threadpump.md)       | <span data-ttu-id="217ce-123">用來以非同步方式執行工作。</span><span class="sxs-lookup"><span data-stu-id="217ce-123">Used to execute tasks asynchronously.</span></span> <span data-ttu-id="217ce-124">此物件佔用大量資源，因此通常每個應用程式只能建立一個資源。</span><span class="sxs-lookup"><span data-stu-id="217ce-124">This object takes up a substantial amount of resources, so generally only one should be created per application.</span></span><br/>                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="217ce-125">**ID3DXMatrixStack 介面**</span><span class="sxs-lookup"><span data-stu-id="217ce-125">**ID3DXMatrixStack Interface**</span></span>](d3d10-id3dxmatrixstack.md)   | <span data-ttu-id="217ce-126">應用程式會使用 ID3DXMATRIXStack 介面的方法來操作矩陣堆疊。</span><span class="sxs-lookup"><span data-stu-id="217ce-126">Applications use the methods of the ID3DXMATRIXStack interface to manipulate a matrix stack.</span></span><br/>                                                                                                                                                                                                                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="217ce-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="217ce-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="217ce-128">D3DX 參考</span><span class="sxs-lookup"><span data-stu-id="217ce-128">D3DX Reference</span></span>](d3d10-graphics-reference-d3dx10.md)
</dt> </dl>

 

 




