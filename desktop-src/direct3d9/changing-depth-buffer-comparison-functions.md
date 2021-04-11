---
description: 根據預設，當深度測試是在呈現介面上執行時，如果對應的深度值 (z 或 w) 的每個點小於深度緩衝區中的值，則 Direct3D 系統會更新呈現目標介面。
ms.assetid: e9243c05-e943-4a42-ab73-e684900fc81d
title: '變更深度緩衝區比較函數 (D3D9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7589ea0035376c6e73bcb70a73fcca3b913c9ecc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689208"
---
# <a name="changing-depth-buffer-comparison-functions-d3d9"></a><span data-ttu-id="8e858-103">變更深度緩衝區比較函數 (D3D9) </span><span class="sxs-lookup"><span data-stu-id="8e858-103">Changing Depth Buffer Comparison Functions (D3D9)</span></span>

<span data-ttu-id="8e858-104">根據預設，當深度測試是在呈現介面上執行時，如果對應的深度值 (z 或 w) 的每個點小於深度緩衝區中的值，則 Direct3D 系統會更新呈現目標介面。</span><span class="sxs-lookup"><span data-stu-id="8e858-104">By default, when depth-testing is performed on a rendering surface, the Direct3D system updates the render-target surface if the corresponding depth value (z or w) for each point is less than the value in the depth buffer.</span></span> <span data-ttu-id="8e858-105">在 c + + 應用程式中，您可以藉由呼叫 [**IDirect3DDevice9：： graphicsdevice**](/windows/desktop/api) 方法，並將 *State* 參數設定為 D3DRS ZFUNC，來變更系統對深度值執行比較的方式 \_ 。</span><span class="sxs-lookup"><span data-stu-id="8e858-105">In a C++ application, you change how the system performs comparisons on depth values by calling the [**IDirect3DDevice9::SetRenderState**](/windows/desktop/api) method with the *State* parameter set to D3DRS\_ZFUNC.</span></span> <span data-ttu-id="8e858-106">*Value* 參數應設定為 [**D3DCMPFUNC**](./d3dcmpfunc.md)列舉型別中的值。</span><span class="sxs-lookup"><span data-stu-id="8e858-106">The *Value* parameter should be set to a value in the [**D3DCMPFUNC**](./d3dcmpfunc.md) enumerated type.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8e858-107">相關主題</span><span class="sxs-lookup"><span data-stu-id="8e858-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e858-108">深度緩衝區</span><span class="sxs-lookup"><span data-stu-id="8e858-108">Depth Buffers</span></span>](depth-buffers.md)
</dt> </dl>

 

 
