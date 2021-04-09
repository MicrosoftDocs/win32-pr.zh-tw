---
title: 樣板測試
description: 樣板測試會根據樣板緩衝區中的值與參考值之間的比較結果，有條件地捨棄片段。
ms.assetid: 967be1e5-a9a2-45cc-aae7-c33cc257ade1
keywords:
- OpenGL 處理管線，樣板測試
- 樣板測試 OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e285c3dfb1591c5ed3d95969024d2350a7517a79
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675487"
---
# <a name="stencil-test"></a><span data-ttu-id="be64e-105">樣板測試</span><span class="sxs-lookup"><span data-stu-id="be64e-105">Stencil Test</span></span>

<span data-ttu-id="be64e-106">樣板測試會根據樣板緩衝區中的值與參考值之間的比較結果，有條件地捨棄片段。</span><span class="sxs-lookup"><span data-stu-id="be64e-106">The stencil test conditionally discards a fragment based on the outcome of a comparison between the value in the stencil buffer and a reference value.</span></span> <span data-ttu-id="be64e-107">[**GlStencilFunc**](glstencilfunc.md)函數會指定比較函數和參考值。</span><span class="sxs-lookup"><span data-stu-id="be64e-107">The [**glStencilFunc**](glstencilfunc.md) function specifies the comparison function and the reference value.</span></span> <span data-ttu-id="be64e-108">如果片段通過或失敗樣板測試，則會根據以 [**glStencilOp**](glstencilop.md)指定的指示修改樣板緩衝區中的值。</span><span class="sxs-lookup"><span data-stu-id="be64e-108">Whether the fragment passes or fails the stencil test, the value in the stencil buffer is modified according to the instructions specified with [**glStencilOp**](glstencilop.md).</span></span>

 

 




