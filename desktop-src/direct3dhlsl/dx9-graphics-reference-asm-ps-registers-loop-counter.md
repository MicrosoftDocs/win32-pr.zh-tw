---
title: '迴圈計數器 register (HLSL PS 參考) '
description: 此銀行中唯一的註冊是) 註冊 (aL 的目前迴圈計數器。
ms.assetid: 36999873-a251-4939-aac0-faa7f910bc33
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 47582552b7e32ede7cd83637cbc3900494dfd611
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/23/2019
ms.locfileid: "103679227"
---
# <a name="loop-counter-register-hlsl-ps-reference"></a><span data-ttu-id="55f24-103">迴圈計數器 register (HLSL PS 參考) </span><span class="sxs-lookup"><span data-stu-id="55f24-103">Loop counter register (HLSL PS reference)</span></span>

<span data-ttu-id="55f24-104">此銀行中唯一的註冊是) 註冊 (aL 的目前迴圈計數器。</span><span class="sxs-lookup"><span data-stu-id="55f24-104">The only register in this bank is the current loop counter (aL) register.</span></span> <span data-ttu-id="55f24-105">它會在每次執行[迴圈 ps](loop---ps.md) / [endloop-ps](endloop---ps.md)區塊時自動遞增。</span><span class="sxs-lookup"><span data-stu-id="55f24-105">It automatically gets incremented in each execution of the [loop - ps](loop---ps.md)/[endloop - ps](endloop---ps.md) block.</span></span> <span data-ttu-id="55f24-106">因此，它可以在區塊中用於相對定址（如有需要），而且在迴圈外使用它是不正確。</span><span class="sxs-lookup"><span data-stu-id="55f24-106">So it can be used in the block for relative addressing if needed and is invalid to use it outside the loop.</span></span>



| <span data-ttu-id="55f24-107">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="55f24-107">Pixel shader versions</span></span> | <span data-ttu-id="55f24-108">1\_1</span><span class="sxs-lookup"><span data-stu-id="55f24-108">1\_1</span></span> | <span data-ttu-id="55f24-109">1\_2</span><span class="sxs-lookup"><span data-stu-id="55f24-109">1\_2</span></span> | <span data-ttu-id="55f24-110">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="55f24-110">1\_3</span></span> | <span data-ttu-id="55f24-111">1\_4</span><span class="sxs-lookup"><span data-stu-id="55f24-111">1\_4</span></span> | <span data-ttu-id="55f24-112">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="55f24-112">2\_0</span></span> | <span data-ttu-id="55f24-113">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="55f24-113">2\_sw</span></span> | <span data-ttu-id="55f24-114">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="55f24-114">2\_x</span></span> | <span data-ttu-id="55f24-115">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="55f24-115">3\_0</span></span> | <span data-ttu-id="55f24-116">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="55f24-116">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|-------|------|------|-------|
| <span data-ttu-id="55f24-117">迴圈計數器暫存器</span><span class="sxs-lookup"><span data-stu-id="55f24-117">Loop Counter Register</span></span> |      |      |      |      |      |       |      | <span data-ttu-id="55f24-118">x</span><span class="sxs-lookup"><span data-stu-id="55f24-118">x</span></span>    | <span data-ttu-id="55f24-119">x</span><span class="sxs-lookup"><span data-stu-id="55f24-119">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="55f24-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="55f24-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55f24-121">寄存 器</span><span class="sxs-lookup"><span data-stu-id="55f24-121">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




