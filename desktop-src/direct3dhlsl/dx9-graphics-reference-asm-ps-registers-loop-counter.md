---
title: '迴圈計數器 register (HLSL PS 參考) '
description: 瞭解圖元著色器的迴圈計數器暫存器。 此銀行中唯一的註冊是) 註冊 (aL 的目前迴圈計數器。
ms.assetid: 36999873-a251-4939-aac0-faa7f910bc33
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b2a2f7f42c83308fa72ceae2875c35c600dfd7db
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405511"
---
# <a name="loop-counter-register-hlsl-ps-reference"></a><span data-ttu-id="1ed83-104">迴圈計數器 register (HLSL PS 參考) </span><span class="sxs-lookup"><span data-stu-id="1ed83-104">Loop counter register (HLSL PS reference)</span></span>

<span data-ttu-id="1ed83-105">此銀行中唯一的註冊是) 註冊 (aL 的目前迴圈計數器。</span><span class="sxs-lookup"><span data-stu-id="1ed83-105">The only register in this bank is the current loop counter (aL) register.</span></span> <span data-ttu-id="1ed83-106">它會在每次執行[迴圈 ps](loop---ps.md) / [endloop-ps](endloop---ps.md)區塊時自動遞增。</span><span class="sxs-lookup"><span data-stu-id="1ed83-106">It automatically gets incremented in each execution of the [loop - ps](loop---ps.md)/[endloop - ps](endloop---ps.md) block.</span></span> <span data-ttu-id="1ed83-107">因此，它可以在區塊中用於相對定址（如有需要），而且在迴圈外使用它是不正確。</span><span class="sxs-lookup"><span data-stu-id="1ed83-107">So it can be used in the block for relative addressing if needed and is invalid to use it outside the loop.</span></span>



| <span data-ttu-id="1ed83-108">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="1ed83-108">Pixel shader versions</span></span> | <span data-ttu-id="1ed83-109">1\_1</span><span class="sxs-lookup"><span data-stu-id="1ed83-109">1\_1</span></span> | <span data-ttu-id="1ed83-110">1\_2</span><span class="sxs-lookup"><span data-stu-id="1ed83-110">1\_2</span></span> | <span data-ttu-id="1ed83-111">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="1ed83-111">1\_3</span></span> | <span data-ttu-id="1ed83-112">1\_4</span><span class="sxs-lookup"><span data-stu-id="1ed83-112">1\_4</span></span> | <span data-ttu-id="1ed83-113">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="1ed83-113">2\_0</span></span> | <span data-ttu-id="1ed83-114">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="1ed83-114">2\_sw</span></span> | <span data-ttu-id="1ed83-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="1ed83-115">2\_x</span></span> | <span data-ttu-id="1ed83-116">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="1ed83-116">3\_0</span></span> | <span data-ttu-id="1ed83-117">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="1ed83-117">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|-------|------|------|-------|
| <span data-ttu-id="1ed83-118">迴圈計數器暫存器</span><span class="sxs-lookup"><span data-stu-id="1ed83-118">Loop Counter Register</span></span> |      |      |      |      |      |       |      | <span data-ttu-id="1ed83-119">x</span><span class="sxs-lookup"><span data-stu-id="1ed83-119">x</span></span>    | <span data-ttu-id="1ed83-120">x</span><span class="sxs-lookup"><span data-stu-id="1ed83-120">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="1ed83-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="1ed83-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ed83-122">寄存 器</span><span class="sxs-lookup"><span data-stu-id="1ed83-122">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




