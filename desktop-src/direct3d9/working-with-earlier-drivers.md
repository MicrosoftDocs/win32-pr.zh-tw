---
description: 本節列出在針對 Direct3D 9 之前的 Direct3D 版本所撰寫的驅動程式上使用 Direct3D 9 時，可能會遇到的問題。
ms.assetid: 891198e8-6c45-4f03-99bb-e24a4082b0d8
title: '使用舊版驅動程式 (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76567bc4778924835e20a476b03dc94ea77739fd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385601"
---
# <a name="working-with-earlier-drivers-direct3d-9"></a><span data-ttu-id="db08d-103">使用舊版驅動程式 (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="db08d-103">Working with Earlier Drivers (Direct3D 9)</span></span>

<span data-ttu-id="db08d-104">本節列出在針對 Direct3D 9 之前的 Direct3D 版本所撰寫的驅動程式上使用 Direct3D 9 時，可能會遇到的問題。</span><span class="sxs-lookup"><span data-stu-id="db08d-104">This section lists issues that can be encountered when working with Direct3D 9 on drivers written for versions of Direct3D earlier than Direct3D 9.</span></span>

-   <span data-ttu-id="db08d-105">使用 T&L HAL 裝置時，會計算霧化濃度，但不會將絕對值運算套用到此值。</span><span class="sxs-lookup"><span data-stu-id="db08d-105">When working with a T&L HAL device, the fog intensity is computed but the absolute value operation is not applied to this value.</span></span> <span data-ttu-id="db08d-106">相反地，如果是計算的值，則值會保持為負數。</span><span class="sxs-lookup"><span data-stu-id="db08d-106">Rather, the value is left negative if that is what is computed.</span></span> <span data-ttu-id="db08d-107">避免這種情況的最佳方式是適當地設定轉換。</span><span class="sxs-lookup"><span data-stu-id="db08d-107">The best way to avoid this situation is to set up transforms appropriately.</span></span> <span data-ttu-id="db08d-108">較不慣用的方法是讓霧開始和霧化值變成負數以符合。</span><span class="sxs-lookup"><span data-stu-id="db08d-108">A less-preferred method is to make the fog-start and fog-end values negative to match.</span></span>

<span data-ttu-id="db08d-109">若要檢查 Direct3D 9 驅動程式，請 \_ 在 [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)的 DevCaps2 成員中尋找非零值的 D3DDEVCAPS2 STREAMOFFSET。</span><span class="sxs-lookup"><span data-stu-id="db08d-109">To check for a Direct3D 9 driver, look for a nonzero value for D3DDEVCAPS2\_STREAMOFFSET in the DevCaps2 member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="related-topics"></a><span data-ttu-id="db08d-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="db08d-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db08d-111">程式設計秘訣</span><span class="sxs-lookup"><span data-stu-id="db08d-111">Programming Tips</span></span>](programming-tips.md)
</dt> </dl>

 

 



