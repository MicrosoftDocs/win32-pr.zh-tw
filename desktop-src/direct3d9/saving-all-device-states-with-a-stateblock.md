---
description: 狀態欄塊可以用來捕捉所有裝置狀態 (請參閱 (Direct3D 9) ) 的狀態欄塊儲存和還原狀態。
ms.assetid: e14077e4-1453-4aa3-b2de-4d3a829a819a
title: 以 StateBlock (Direct3D 9) 儲存所有裝置狀態
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bfdb4f9b3a9c1e33c2e8e7f50765f1656bd59e1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106972934"
---
# <a name="saving-all-device-states-with-a-stateblock-direct3d-9"></a><span data-ttu-id="ef12b-103">以 StateBlock (Direct3D 9) 儲存所有裝置狀態</span><span class="sxs-lookup"><span data-stu-id="ef12b-103">Saving All Device States with a StateBlock (Direct3D 9)</span></span>

<span data-ttu-id="ef12b-104">狀態欄塊可以用來捕捉所有裝置狀態 (請參閱 [ (Direct3D 9) ) 的狀態欄塊儲存和還原狀態 ](state-blocks-save-and-restore-state.md) 。</span><span class="sxs-lookup"><span data-stu-id="ef12b-104">A state block can be used to capture all device states (see [State Blocks Save and Restore State (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span></span> <span data-ttu-id="ef12b-105">裝置狀態包含下列狀態元素：</span><span class="sxs-lookup"><span data-stu-id="ef12b-105">The following state elements are included in the device state:</span></span>

-   <span data-ttu-id="ef12b-106">頂點狀態 (請參閱 [使用 StateBlock (Direct3D 9) ) 儲存頂點狀態 ](saving-vertex-states-with-a-stateblock.md) 。</span><span class="sxs-lookup"><span data-stu-id="ef12b-106">Vertex state (see [Saving Vertex States With a StateBlock (Direct3D 9)](saving-vertex-states-with-a-stateblock.md)).</span></span>
-   <span data-ttu-id="ef12b-107">圖元狀態 (請參閱 [使用 StateBlock (Direct3D 9) ) 儲存圖元狀態 ](saving-pixel-states-with-a-stateblock.md) 。</span><span class="sxs-lookup"><span data-stu-id="ef12b-107">Pixel state (see [Saving Pixel State With a StateBlock (Direct3D 9)](saving-pixel-states-with-a-stateblock.md)).</span></span>
-   <span data-ttu-id="ef12b-108">每個指派給取樣器的材質。</span><span class="sxs-lookup"><span data-stu-id="ef12b-108">Each texture assigned to a sampler.</span></span>
-   <span data-ttu-id="ef12b-109">每個頂點材質。</span><span class="sxs-lookup"><span data-stu-id="ef12b-109">Each vertex texture.</span></span>
-   <span data-ttu-id="ef12b-110">每個置換地圖材質。</span><span class="sxs-lookup"><span data-stu-id="ef12b-110">Each displacement map texture.</span></span>
-   <span data-ttu-id="ef12b-111">目前的材質調色板。</span><span class="sxs-lookup"><span data-stu-id="ef12b-111">The current texture palette.</span></span>
-   <span data-ttu-id="ef12b-112">針對每個頂點資料流程：指向頂點緩衝區的指標、來自 [**IDirect3DDevice9：： SetStreamSource**](/windows/desktop/api)的每個引數，以及從 [**IDirect3DDevice9：： SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq)取得的任何) 的分隔 (。</span><span class="sxs-lookup"><span data-stu-id="ef12b-112">For each vertex stream: a pointer to the vertex buffer, each argument from [**IDirect3DDevice9::SetStreamSource**](/windows/desktop/api), and the divider (if any) from [**IDirect3DDevice9::SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq).</span></span>
-   <span data-ttu-id="ef12b-113">索引緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="ef12b-113">A pointer to the index buffer.</span></span>
-   <span data-ttu-id="ef12b-114">視口。</span><span class="sxs-lookup"><span data-stu-id="ef12b-114">The viewport.</span></span>
-   <span data-ttu-id="ef12b-115">剪刀矩形。</span><span class="sxs-lookup"><span data-stu-id="ef12b-115">The scissors rectangle.</span></span>
-   <span data-ttu-id="ef12b-116">世界、視野和投射矩陣。</span><span class="sxs-lookup"><span data-stu-id="ef12b-116">The world, view, and projection matrices.</span></span>
-   <span data-ttu-id="ef12b-117">紋理轉換。</span><span class="sxs-lookup"><span data-stu-id="ef12b-117">The texture transforms.</span></span>
-   <span data-ttu-id="ef12b-118">如果有任何) ，裁剪平面就 (。</span><span class="sxs-lookup"><span data-stu-id="ef12b-118">The clipping planes (if any).</span></span>
-   <span data-ttu-id="ef12b-119">目前的材質。</span><span class="sxs-lookup"><span data-stu-id="ef12b-119">The current material.</span></span>

<span data-ttu-id="ef12b-120">若要使用狀態欄塊來捕捉所有裝置狀態，請 \_ 在呼叫 [**IDirect3DDevice9：： CreateStateBlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createstateblock)時指定 D3DSBT all。</span><span class="sxs-lookup"><span data-stu-id="ef12b-120">To capture all device states with a state block, specify D3DSBT\_ALL when calling [**IDirect3DDevice9::CreateStateBlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createstateblock).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ef12b-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="ef12b-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef12b-122">狀態欄塊儲存與還原狀態</span><span class="sxs-lookup"><span data-stu-id="ef12b-122">State Blocks Save and Restore State</span></span>](state-blocks-save-and-restore-state.md)
</dt> </dl>

 

 
