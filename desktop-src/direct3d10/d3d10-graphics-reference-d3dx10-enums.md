---
description: 本節包含下列與 D3DX 搭配使用之列舉類型和旗標的相關資訊：
ms.assetid: 8836f350-9edd-4521-b7a3-3aa827394c57
title: D3DX (Direct3D 10 圖形) 的列舉
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59a34ae9c1b275376343ecab321ab9e7762c59fe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104187785"
---
# <a name="d3dx-enumerations-direct3d-10-graphics"></a><span data-ttu-id="7425b-103">D3DX (Direct3D 10 圖形) 的列舉</span><span class="sxs-lookup"><span data-stu-id="7425b-103">D3DX Enumerations (Direct3D 10 Graphics)</span></span>

<span data-ttu-id="7425b-104">本節包含下列與 D3DX 搭配使用之列舉類型和旗標的相關資訊：</span><span class="sxs-lookup"><span data-stu-id="7425b-104">This section contains information about the following enumerated types and flags used with D3DX.:</span></span>



| <span data-ttu-id="7425b-105">列舉型別</span><span class="sxs-lookup"><span data-stu-id="7425b-105">Enumeration</span></span>                                                       | <span data-ttu-id="7425b-106">描述</span><span class="sxs-lookup"><span data-stu-id="7425b-106">Description</span></span>                                                                                                                                                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7425b-107">**D3DX10 \_ 通道 \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="7425b-107">**D3DX10\_CHANNEL\_FLAG**</span></span>](d3dx10-channel-flag.md)              | <span data-ttu-id="7425b-108">這些旗標會由函式使用，這些函式會在材質中的一或多個通道上運作。</span><span class="sxs-lookup"><span data-stu-id="7425b-108">These flags are used by functions which operate on one or more channels in a texture.</span></span>                                                                                                  |
| [<span data-ttu-id="7425b-109">**D3DX \_ CPU \_ 優化**</span><span class="sxs-lookup"><span data-stu-id="7425b-109">**D3DX\_CPU\_OPTIMIZATION**</span></span>](d3dx-cpu-optimization.md)          | <span data-ttu-id="7425b-110">指定目前針對 D3DX 優化的指令集。</span><span class="sxs-lookup"><span data-stu-id="7425b-110">Specifies the instruction set D3DX is currently optimized for.</span></span>                                                                                                                         |
| [<span data-ttu-id="7425b-111">**D3DX10 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="7425b-111">**D3DX10\_ERR**</span></span>](d3dx10-err.md)                                 | <span data-ttu-id="7425b-112">錯誤會以負數值表示，而且無法合併。</span><span class="sxs-lookup"><span data-stu-id="7425b-112">Errors are represented by negative values and cannot be combined.</span></span>                                                                                                                      |
| [<span data-ttu-id="7425b-113">**D3DX10 \_ 篩選 \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="7425b-113">**D3DX10\_FILTER\_FLAG**</span></span>](d3dx10-filter-flag.md)                | <span data-ttu-id="7425b-114">材質篩選旗標。</span><span class="sxs-lookup"><span data-stu-id="7425b-114">Texture filtering flags.</span></span>                                                                                                                                                               |
| [<span data-ttu-id="7425b-115">**D3DX10 \_ 圖像 \_ 檔案 \_ 格式**</span><span class="sxs-lookup"><span data-stu-id="7425b-115">**D3DX10\_IMAGE\_FILE\_FORMAT**</span></span>](d3dx10-image-file-format.md)   | <span data-ttu-id="7425b-116">描述支援的影像檔案格式。</span><span class="sxs-lookup"><span data-stu-id="7425b-116">Describes the supported image file formats.</span></span>                                                                                                                                            |
| [<span data-ttu-id="7425b-117">**D3DX10 \_ 網格**</span><span class="sxs-lookup"><span data-stu-id="7425b-117">**D3DX10\_MESH**</span></span>](d3dx10-mesh.md)                               | <span data-ttu-id="7425b-118">用來指定網格之建立選項的旗標。</span><span class="sxs-lookup"><span data-stu-id="7425b-118">Flags used to specify creation options for a mesh.</span></span>                                                                                                                                     |
| [<span data-ttu-id="7425b-119">**D3DX10 \_ 網格 \_ 捨棄 \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="7425b-119">**D3DX10\_MESH\_DISCARD\_FLAGS**</span></span>](d3dx10-mesh-discard-flags.md) | <span data-ttu-id="7425b-120">指定要從裝置捨棄哪些網格資料片段。</span><span class="sxs-lookup"><span data-stu-id="7425b-120">Specifies which pieces of mesh data to discard from the device.</span></span> <span data-ttu-id="7425b-121">搭配 [**ID3DX10Mesh 使用：:D iscard**](id3dx10mesh-discard.md)。</span><span class="sxs-lookup"><span data-stu-id="7425b-121">Used with [**ID3DX10Mesh::Discard**](id3dx10mesh-discard.md).</span></span>                                                         |
| [<span data-ttu-id="7425b-122">**D3DX10 \_ MESHOPT**</span><span class="sxs-lookup"><span data-stu-id="7425b-122">**D3DX10\_MESHOPT**</span></span>](d3dx10-meshopt.md)                         | <span data-ttu-id="7425b-123">指定要執行的網格優化類型。</span><span class="sxs-lookup"><span data-stu-id="7425b-123">Specifies the type of mesh optimization to be performed.</span></span>                                                                                                                               |
| [<span data-ttu-id="7425b-124">**D3DX10 \_ NORMALMAP \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="7425b-124">**D3DX10\_NORMALMAP\_FLAG**</span></span>](d3dx10-normalmap-flag.md)          | <span data-ttu-id="7425b-125">這些旗標是用來控制 [**D3DX10ComputeNormalMap**](d3dx10computenormalmap.md) 產生一般對應的方式。</span><span class="sxs-lookup"><span data-stu-id="7425b-125">These flags are used to control how [**D3DX10ComputeNormalMap**](d3dx10computenormalmap.md) generates normal maps.</span></span> <span data-ttu-id="7425b-126">這些旗標的任意數目可能會以任何組合方式組合。</span><span class="sxs-lookup"><span data-stu-id="7425b-126">Any number of these flags may be OR'd together in any combination.</span></span> |
| [<span data-ttu-id="7425b-127">**D3DX10 \_ 儲存 \_ 材質 \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="7425b-127">**D3DX10\_SAVE\_TEXTURE\_FLAG**</span></span>](d3dx10-save-texture-flag.md)   | <span data-ttu-id="7425b-128">材質儲存選項。</span><span class="sxs-lookup"><span data-stu-id="7425b-128">Texture save options.</span></span>                                                                                                                                                                  |



 

## <a name="related-topics"></a><span data-ttu-id="7425b-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="7425b-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7425b-130">D3DX 參考</span><span class="sxs-lookup"><span data-stu-id="7425b-130">D3DX Reference</span></span>](d3d10-graphics-reference-d3dx10.md)
</dt> </dl>

 

 



