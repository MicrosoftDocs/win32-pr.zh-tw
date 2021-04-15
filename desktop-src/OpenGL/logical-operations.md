---
title: 邏輯作業
description: 邏輯運算可以在片段和儲存在畫面格緩衝區中對應位置的值之間套用。結果會取代目前的畫面格緩衝區值。
ms.assetid: 0d1ea309-e86b-4aff-87ac-9d9d5909c2ce
keywords:
- OpenGL 處理管線，邏輯運算
- 邏輯運算 OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3736f9a06892e652825a7232aa087eb8b4832f20
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507168"
---
# <a name="logical-operations"></a><span data-ttu-id="00711-105">邏輯作業</span><span class="sxs-lookup"><span data-stu-id="00711-105">Logical Operations</span></span>

<span data-ttu-id="00711-106">邏輯運算可以在片段和儲存在畫面格緩衝區中對應位置的值之間套用。結果會取代目前的畫面格緩衝區值。</span><span class="sxs-lookup"><span data-stu-id="00711-106">A logical operation can be applied between the fragment and the value stored at the corresponding location in the framebuffer; the result replaces the current framebuffer value.</span></span> <span data-ttu-id="00711-107">您可以使用 [**glLogicOp**](gllogicop.md)選擇所需的邏輯作業。</span><span class="sxs-lookup"><span data-stu-id="00711-107">You choose the desired logical operation with [**glLogicOp**](gllogicop.md).</span></span> <span data-ttu-id="00711-108">邏輯作業只會在色彩索引上執行，而不會在 RGBA 值上執行。</span><span class="sxs-lookup"><span data-stu-id="00711-108">Logical operations are performed only on color indexes, never on RGBA values.</span></span>

 

 




