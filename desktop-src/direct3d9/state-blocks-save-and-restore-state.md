---
description: 狀態欄塊是裝置狀態的群組。
ms.assetid: 6b1917a8-8685-40c3-983d-6bd2fed95642
title: '狀態欄塊儲存和還原狀態 (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c8f19d6409e0dc9c40f1d4c7711440a0dc09fe2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103935618"
---
# <a name="state-blocks-save-and-restore-state-direct3d-9"></a><span data-ttu-id="9f234-103">狀態欄塊儲存和還原狀態 (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="9f234-103">State Blocks Save and Restore State (Direct3D 9)</span></span>

<span data-ttu-id="9f234-104">狀態欄塊是裝置狀態的群組。</span><span class="sxs-lookup"><span data-stu-id="9f234-104">A state block is a group of device states.</span></span> <span data-ttu-id="9f234-105">裝置狀態是由呈現狀態、頂點狀態、圖元狀態或上述所有內容所組成。</span><span class="sxs-lookup"><span data-stu-id="9f234-105">Device state is made up of render state, vertex state, pixel state, or all of the above.</span></span> <span data-ttu-id="9f234-106">狀態欄塊包含裝置目前狀態的快照，您也可以建立狀態欄塊來記錄應用程式所進行的每個狀態變更。</span><span class="sxs-lookup"><span data-stu-id="9f234-106">A state block contains a snapshot of a device's current state, or you can create a state block that records each state change that your application makes.</span></span>

## <a name="capture-a-block-of-state"></a><span data-ttu-id="9f234-107">捕捉狀態的區塊</span><span class="sxs-lookup"><span data-stu-id="9f234-107">Capture a Block of State</span></span>

<span data-ttu-id="9f234-108">選擇您想要捕捉的狀態類型，並建立如下的狀態欄塊：</span><span class="sxs-lookup"><span data-stu-id="9f234-108">Choose the type of state that you want to capture, and create a state block like this:</span></span>


```
IDirect3DStateBlock9* pStateBlock = NULL;
pd3dDevice->CreateStateBlock( D3DSBT_ALL, &pStateBlock );
```



<span data-ttu-id="9f234-109">[**IDirect3DDevice9：： CreateStateBlock**](/windows/desktop/api) 會建立狀態欄塊，並自動捕獲裝置狀態。</span><span class="sxs-lookup"><span data-stu-id="9f234-109">[**IDirect3DDevice9::CreateStateBlock**](/windows/desktop/api) creates a state block, and automatically captures the device state.</span></span> <span data-ttu-id="9f234-110">裝置狀態是由第一個引數中的狀態欄塊類型所指定。</span><span class="sxs-lookup"><span data-stu-id="9f234-110">The device state is specified by the state block type in the first argument.</span></span> <span data-ttu-id="9f234-111">此狀態可以是下列其中一項：所有裝置狀態 (參閱將 [所有裝置狀態儲存為 StateBlock (direct3d 9) ](saving-all-device-states-with-a-stateblock.md)) 、所有圖元狀態 (請參閱 [將圖元狀態儲存為 StateBlock (direct3d 9) ](saving-pixel-states-with-a-stateblock.md)) 或所有頂點狀態 (請參閱 [使用 StateBlock (Direct3d 9) ) 儲存頂點 ](saving-vertex-states-with-a-stateblock.md) 狀態。</span><span class="sxs-lookup"><span data-stu-id="9f234-111">This state can be one of the following: all device state (see [Saving All Device States with a StateBlock (Direct3D 9)](saving-all-device-states-with-a-stateblock.md)), all pixel state (see [Saving Pixel State With a StateBlock (Direct3D 9)](saving-pixel-states-with-a-stateblock.md)), or all vertex state (see [Saving Vertex States With a StateBlock (Direct3D 9)](saving-vertex-states-with-a-stateblock.md)).</span></span>

<span data-ttu-id="9f234-112">效果系統會使用狀態欄塊來儲存狀態。</span><span class="sxs-lookup"><span data-stu-id="9f234-112">The effect system uses a state block to save state.</span></span> <span data-ttu-id="9f234-113">呼叫 [**ID3DXEffect：： Begin**](id3dxeffect--begin.md) 之後，會建立狀態欄塊並捕獲狀態。</span><span class="sxs-lookup"><span data-stu-id="9f234-113">After [**ID3DXEffect::Begin**](id3dxeffect--begin.md) is called, a state block is created and state is captured.</span></span> <span data-ttu-id="9f234-114">呼叫 [**ID3DXEffect：： End**](id3dxeffect--end.md) 時，會將狀態欄塊狀態重新套用至裝置。</span><span class="sxs-lookup"><span data-stu-id="9f234-114">When [**ID3DXEffect::End**](id3dxeffect--end.md) is called, the state block state is reapplied to the device.</span></span>

## <a name="capture-individual-states"></a><span data-ttu-id="9f234-115">捕捉個別狀態</span><span class="sxs-lookup"><span data-stu-id="9f234-115">Capture Individual States</span></span>

<span data-ttu-id="9f234-116">若要儲存自訂狀態順序，請將您要儲存的狀態包裝在 [**IDirect3DDevice9：： BeginStateBlock**](/windows/desktop/api) 和 [**IDirect3DDevice9：： EndStateBlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endstateblock) 配對中。</span><span class="sxs-lookup"><span data-stu-id="9f234-116">To save a custom state sequence, wrap the state that you want to save in a [**IDirect3DDevice9::BeginStateBlock**](/windows/desktop/api) and [**IDirect3DDevice9::EndStateBlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endstateblock) pair.</span></span> <span data-ttu-id="9f234-117">BeginStateBlock 會告知目前裝置設定狀態欄塊，並將其新增至在呼叫 EndStateBlock 之前發生的每個狀態變更。</span><span class="sxs-lookup"><span data-stu-id="9f234-117">BeginStateBlock tells the current device to set up a state block and add to it every state change that occurs until EndStateBlock is called.</span></span> <span data-ttu-id="9f234-118">以下為範例：</span><span class="sxs-lookup"><span data-stu-id="9f234-118">Here's an example:</span></span>


```
IDirect3DStateBlock9* pStateBlock = NULL;
pd3dDevice->BeginStateBlock();
pd3dDevice->SetRenderState ( D3DRS_ZENABLE, true );
pd3dDevice->EndStateBlock( &pStateBlock );
```



<span data-ttu-id="9f234-119">這會以任何順序將任何數目的狀態變更儲存至自訂 stateblock。</span><span class="sxs-lookup"><span data-stu-id="9f234-119">This will save any number of state changes in any sequence to a custom stateblock.</span></span> <span data-ttu-id="9f234-120">稍後，當您想要使用 stateblock 來重設裝置狀態時，請呼叫 [**IDirect3DStateBlock9：： Apply**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dstateblock9-apply)。</span><span class="sxs-lookup"><span data-stu-id="9f234-120">Later, when you want to use the stateblock to reset the device state, call [**IDirect3DStateBlock9::Apply**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dstateblock9-apply).</span></span> <span data-ttu-id="9f234-121">這只會覆寫狀態欄塊中已捕捉的裝置狀態。</span><span class="sxs-lookup"><span data-stu-id="9f234-121">This will overwrite only the device state that has been captured in the state block.</span></span> <span data-ttu-id="9f234-122">未使用自訂 stateblock 所捕捉的任何其他裝置狀態都不會變更。</span><span class="sxs-lookup"><span data-stu-id="9f234-122">Any other device state that was not captured with the custom stateblock will not be changed.</span></span> <span data-ttu-id="9f234-123">同樣地，由於 stateblock 物件是介面，因此您必須在完成時將它釋放。</span><span class="sxs-lookup"><span data-stu-id="9f234-123">Once again, since the stateblock object is an interface, you will need to release it when you are done with it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9f234-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="9f234-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9f234-125">狀態 (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="9f234-125">States (Direct3D 9)</span></span>](states.md)
</dt> </dl>

 

 
