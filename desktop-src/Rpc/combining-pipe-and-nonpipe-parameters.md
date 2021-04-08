---
title: 結合管道和 Nonpipe 參數
description: 將遠端程序呼叫中的管道和 nonpipe 參數結合 (RPC) 。
ms.assetid: 52109ba9-4e10-4426-8dfc-e3052d403e9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0776f995dacb4d477724b0ee1e5c2fa969723199
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842587"
---
# <a name="combining-pipe-and-nonpipe-parameters"></a><span data-ttu-id="4a198-103">結合管道和 Nonpipe 參數</span><span class="sxs-lookup"><span data-stu-id="4a198-103">Combining Pipe and Nonpipe Parameters</span></span>

<span data-ttu-id="4a198-104">當您在遠端程序呼叫中結合管道類型和其他類型時，會根據參數的方向來傳輸資料：</span><span class="sxs-lookup"><span data-stu-id="4a198-104">When you combine pipe types and other types in a remote procedure call, the data is transmitted according to the direction of the parameter:</span></span>

-   <span data-ttu-id="4a198-105">在 [ **\[ \] 方向]** 中，會先傳送所有 nonpipe 引數的資料，然後再傳送管線資料。</span><span class="sxs-lookup"><span data-stu-id="4a198-105">In the **\[in\]** direction, the data for all nonpipe arguments is transmitted first, followed by pipe data.</span></span>
-   <span data-ttu-id="4a198-106">在 **\[ 輸出 \]** 方向中，伺服器會先傳送管線資料。</span><span class="sxs-lookup"><span data-stu-id="4a198-106">In the **\[out\]** direction, the server sends the pipe data first.</span></span> <span data-ttu-id="4a198-107">在管理員常式傳回之後，伺服器會傳送 nonpipe 的資料。</span><span class="sxs-lookup"><span data-stu-id="4a198-107">After the manager routine returns, the server transmits the nonpipe data.</span></span>
-   <span data-ttu-id="4a198-108">當 **\[ in、out \]** 管道引數與 **\[ in、out \]** 非管道引數合併時，會先將輸入資料完整傳輸（如先前所述）。</span><span class="sxs-lookup"><span data-stu-id="4a198-108">When there are **\[in,out\]** pipe arguments combined with **\[in,out\]** non-pipe arguments, first the input data is transmitted in its entirety, as previously described.</span></span> <span data-ttu-id="4a198-109">然後，輸出資料會如先前所述傳輸。</span><span class="sxs-lookup"><span data-stu-id="4a198-109">Then, the output data is transmitted as previously described.</span></span>

<span data-ttu-id="4a198-110">下列限制適用于此 (MIDL 3.0) 實作為管道：當您在單一遠端程序呼叫中結合管道類型和其他類型時，nonpipe 參數必須有妥善定義的大小，才能讓 MIDL 編譯器計算所需的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="4a198-110">The following restriction applies to this (MIDL 3.0) implementation of pipes: When you combine pipe types and other types in a single remote procedure call, the nonpipe parameters must have a well-defined size in order to allow the MIDL compiler to calculate the buffer size needed.</span></span> <span data-ttu-id="4a198-111">例如，您無法將管道參數與 \[ [唯一](/windows/desktop/Midl/unique) \] 指標或符合標準的結構結合，因為它們的大小無法在編譯時期決定。</span><span class="sxs-lookup"><span data-stu-id="4a198-111">For example, you cannot combine pipe parameters with a \[ [unique](/windows/desktop/Midl/unique)\] pointer or a conformant structure, since their sizes cannot be determined at compile time.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4a198-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="4a198-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a198-113">管道</span><span class="sxs-lookup"><span data-stu-id="4a198-113">pipe</span></span>](/windows/desktop/Midl/pipe)
</dt> <dt>

[<span data-ttu-id="4a198-114">/Oi</span><span class="sxs-lookup"><span data-stu-id="4a198-114">/Oi</span></span>](/windows/desktop/Midl/-oi)
</dt> </dl>

 

 