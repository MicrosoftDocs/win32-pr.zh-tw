---
title: '迴圈計數器 Register (HLSL 與參考) '
description: 瞭解頂點著色器的迴圈計數器暫存器。 此銀行中唯一的註冊是) 註冊 (aL 的目前迴圈計數器。
ms.assetid: b32fabf8-38d3-446c-bb80-c647d5aa028d
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8fb728420dc48c6cb67d5973085845b0eab742a2
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405771"
---
# <a name="loop-counter-register-hlsl-vs-reference"></a><span data-ttu-id="b8828-104">迴圈計數器 Register (HLSL 與參考) </span><span class="sxs-lookup"><span data-stu-id="b8828-104">Loop Counter Register (HLSL VS reference)</span></span>

<span data-ttu-id="b8828-105">此銀行中唯一的註冊是) 註冊 (aL 的目前迴圈計數器。</span><span class="sxs-lookup"><span data-stu-id="b8828-105">The only register in this bank is the current loop counter (aL) register.</span></span> <span data-ttu-id="b8828-106">每次執行迴圈時，它會自動遞增 [（與](loop---vs.md).。。[endloop-vs](endloop---vs.md) block。</span><span class="sxs-lookup"><span data-stu-id="b8828-106">It automatically gets incremented in each execution of the [loop - vs](loop---vs.md)...[endloop - vs](endloop---vs.md) block.</span></span> <span data-ttu-id="b8828-107">因此，它可以在區塊中用於相對定址（如有需要），而且在迴圈外使用它是不正確。</span><span class="sxs-lookup"><span data-stu-id="b8828-107">So it can be used in the block for relative addressing if needed and is invalid to use it outside the loop.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b8828-108">相關主題</span><span class="sxs-lookup"><span data-stu-id="b8828-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8828-109">頂點著色器暫存器</span><span class="sxs-lookup"><span data-stu-id="b8828-109">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




