---
title: '迴圈計數器 Register (HLSL 與參考) '
description: 此銀行中唯一的註冊是) 註冊 (aL 的目前迴圈計數器。
ms.assetid: b32fabf8-38d3-446c-bb80-c647d5aa028d
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b12f57ba3fcfcb41aaff3827be39dbd1b6b07df1
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/23/2019
ms.locfileid: "104373962"
---
# <a name="loop-counter-register-hlsl-vs-reference"></a><span data-ttu-id="b9912-103">迴圈計數器 Register (HLSL 與參考) </span><span class="sxs-lookup"><span data-stu-id="b9912-103">Loop Counter Register (HLSL VS reference)</span></span>

<span data-ttu-id="b9912-104">此銀行中唯一的註冊是) 註冊 (aL 的目前迴圈計數器。</span><span class="sxs-lookup"><span data-stu-id="b9912-104">The only register in this bank is the current loop counter (aL) register.</span></span> <span data-ttu-id="b9912-105">每次執行迴圈時，它會自動遞增 [（與](loop---vs.md).。。[endloop-vs](endloop---vs.md) block。</span><span class="sxs-lookup"><span data-stu-id="b9912-105">It automatically gets incremented in each execution of the [loop - vs](loop---vs.md)...[endloop - vs](endloop---vs.md) block.</span></span> <span data-ttu-id="b9912-106">因此，它可以在區塊中用於相對定址（如有需要），而且在迴圈外使用它是不正確。</span><span class="sxs-lookup"><span data-stu-id="b9912-106">So it can be used in the block for relative addressing if needed and is invalid to use it outside the loop.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b9912-107">相關主題</span><span class="sxs-lookup"><span data-stu-id="b9912-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b9912-108">頂點著色器暫存器</span><span class="sxs-lookup"><span data-stu-id="b9912-108">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




