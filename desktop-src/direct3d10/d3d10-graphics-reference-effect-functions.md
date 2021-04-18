---
description: 本節包含下列效果函數的相關資訊：
ms.assetid: b76643f0-387f-49c6-80e5-4d7b406b4db7
title: " (Direct3D 10) 的效果函數"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 111fdcb34bbf1d9a86a295e62f734938991dda99
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510624"
---
# <a name="effect-functions-direct3d-10"></a><span data-ttu-id="3a450-103"> (Direct3D 10) 的效果函數</span><span class="sxs-lookup"><span data-stu-id="3a450-103">Effect Functions (Direct3D 10)</span></span>

<span data-ttu-id="3a450-104">本節包含下列效果函數的相關資訊：</span><span class="sxs-lookup"><span data-stu-id="3a450-104">This section contains information about the following effect functions:</span></span>



| <span data-ttu-id="3a450-105">函式</span><span class="sxs-lookup"><span data-stu-id="3a450-105">Functions</span></span>                                                                      | <span data-ttu-id="3a450-106">Description</span><span class="sxs-lookup"><span data-stu-id="3a450-106">Description</span></span>                                                         |
|--------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [<span data-ttu-id="3a450-107">**D3D10CompileEffectFromMemory**</span><span class="sxs-lookup"><span data-stu-id="3a450-107">**D3D10CompileEffectFromMemory**</span></span>](/windows/desktop/api/D3D10Effect/nf-d3d10effect-d3d10compileeffectfrommemory)           | <span data-ttu-id="3a450-108">編譯效果。</span><span class="sxs-lookup"><span data-stu-id="3a450-108">Compile an effect.</span></span>                                                  |
| [<span data-ttu-id="3a450-109">**D3D10CreateEffectFromMemory**</span><span class="sxs-lookup"><span data-stu-id="3a450-109">**D3D10CreateEffectFromMemory**</span></span>](/windows/desktop/api/D3D10Effect/nf-d3d10effect-d3d10createeffectfrommemory)             | <span data-ttu-id="3a450-110">建立效果。</span><span class="sxs-lookup"><span data-stu-id="3a450-110">Create an effect.</span></span>                                                   |
| [<span data-ttu-id="3a450-111">**D3D10CreateEffectPoolFromMemory**</span><span class="sxs-lookup"><span data-stu-id="3a450-111">**D3D10CreateEffectPoolFromMemory**</span></span>](/windows/desktop/api/D3D10Effect/nf-d3d10effect-d3d10createeffectpoolfrommemory)     | <span data-ttu-id="3a450-112">建立效果集區。</span><span class="sxs-lookup"><span data-stu-id="3a450-112">Create an effect pool.</span></span>                                              |
| [<span data-ttu-id="3a450-113">**D3D10CreateStateBlock**</span><span class="sxs-lookup"><span data-stu-id="3a450-113">**D3D10CreateStateBlock**</span></span>](/windows/desktop/api/D3D10Effect/nf-d3d10effect-d3d10createstateblock)                         | <span data-ttu-id="3a450-114">建立狀態欄塊。</span><span class="sxs-lookup"><span data-stu-id="3a450-114">Create a state block.</span></span>                                               |
| [<span data-ttu-id="3a450-115">**D3D10DisassembleEffect**</span><span class="sxs-lookup"><span data-stu-id="3a450-115">**D3D10DisassembleEffect**</span></span>](/windows/desktop/api/D3D10Effect/nf-d3d10effect-d3d10disassembleeffect)                       | <span data-ttu-id="3a450-116">將已編譯的效果分解為著色器元件指示。</span><span class="sxs-lookup"><span data-stu-id="3a450-116">Disassemble a compiled effect into shader assembly instructions.</span></span>    |
| [<span data-ttu-id="3a450-117">**D3D10StateBlockMaskDifference**</span><span class="sxs-lookup"><span data-stu-id="3a450-117">**D3D10StateBlockMaskDifference**</span></span>](/windows/desktop/api/D3D10Effect/nf-d3d10effect-d3d10stateblockmaskdifference)         | <span data-ttu-id="3a450-118">將兩個狀態欄塊遮罩與位 XOR 合併。</span><span class="sxs-lookup"><span data-stu-id="3a450-118">Combine two state-block masks with a bitwise XOR.</span></span>                   |
| [<span data-ttu-id="3a450-119">**D3D10StateBlockMaskDisableAll**</span><span class="sxs-lookup"><span data-stu-id="3a450-119">**D3D10StateBlockMaskDisableAll**</span></span>](/windows/desktop/api/D3D10Effect/nf-d3d10effect-d3d10stateblockmaskdisableall)         | <span data-ttu-id="3a450-120">停用狀態捕捉。</span><span class="sxs-lookup"><span data-stu-id="3a450-120">Disable state capturing.</span></span>                                            |
| [<span data-ttu-id="3a450-121">**D3D10StateBlockMaskDisableCapture**</span><span class="sxs-lookup"><span data-stu-id="3a450-121">**D3D10StateBlockMaskDisableCapture**</span></span>](/windows/desktop/api/D3D10Effect/nf-d3d10effect-d3d10stateblockmaskdisablecapture) | <span data-ttu-id="3a450-122">使用狀態欄塊遮罩來停用狀態捕捉。</span><span class="sxs-lookup"><span data-stu-id="3a450-122">Disable state capturing with a state-block mask.</span></span>                    |
| [<span data-ttu-id="3a450-123">**D3D10StateBlockMaskEnableAll**</span><span class="sxs-lookup"><span data-stu-id="3a450-123">**D3D10StateBlockMaskEnableAll**</span></span>](/windows/desktop/api/D3D10Effect/nf-d3d10effect-d3d10stateblockmaskenableall)           | <span data-ttu-id="3a450-124">啟用狀態欄塊遮罩來捕捉和套用所有狀態變數。</span><span class="sxs-lookup"><span data-stu-id="3a450-124">Enable a state-block mask to capture and apply all state variables.</span></span> |
| [<span data-ttu-id="3a450-125">**D3D10StateBlockMaskEnableCapture**</span><span class="sxs-lookup"><span data-stu-id="3a450-125">**D3D10StateBlockMaskEnableCapture**</span></span>](/windows/desktop/api/D3D10Effect/nf-d3d10effect-d3d10stateblockmaskenablecapture)   | <span data-ttu-id="3a450-126">啟用狀態欄塊遮罩中的狀態值範圍。</span><span class="sxs-lookup"><span data-stu-id="3a450-126">Enable a range of state values in a state block mask.</span></span>               |
| [<span data-ttu-id="3a450-127">**D3D10StateBlockMaskGetSetting**</span><span class="sxs-lookup"><span data-stu-id="3a450-127">**D3D10StateBlockMaskGetSetting**</span></span>](/windows/desktop/api/D3D10Effect/nf-d3d10effect-d3d10stateblockmaskgetsetting)         | <span data-ttu-id="3a450-128">取得狀態欄塊遮罩中的元素。</span><span class="sxs-lookup"><span data-stu-id="3a450-128">Get an element in a state-block mask.</span></span>                               |
| [<span data-ttu-id="3a450-129">**D3D10StateBlockMaskIntersect**</span><span class="sxs-lookup"><span data-stu-id="3a450-129">**D3D10StateBlockMaskIntersect**</span></span>](/windows/desktop/api/D3D10Effect/nf-d3d10effect-d3d10stateblockmaskintersect)           | <span data-ttu-id="3a450-130">結合兩個狀態欄塊遮罩與位 AND。</span><span class="sxs-lookup"><span data-stu-id="3a450-130">Combine two state-block masks with a bitwise AND.</span></span>                   |
| [<span data-ttu-id="3a450-131">**D3D10StateBlockMaskUnion**</span><span class="sxs-lookup"><span data-stu-id="3a450-131">**D3D10StateBlockMaskUnion**</span></span>](/windows/desktop/api/D3D10Effect/nf-d3d10effect-d3d10stateblockmaskunion)                   | <span data-ttu-id="3a450-132">結合兩個狀態欄塊遮罩與位 OR。</span><span class="sxs-lookup"><span data-stu-id="3a450-132">Combine two state-block masks with a bitwise OR.</span></span>                    |



 

## <a name="related-topics"></a><span data-ttu-id="3a450-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="3a450-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a450-134">效果參考</span><span class="sxs-lookup"><span data-stu-id="3a450-134">Effect Reference</span></span>](d3d10-graphics-reference-effect.md)
</dt> </dl>

 

 



