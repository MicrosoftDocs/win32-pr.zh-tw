---
title: 位址註冊
description: A0 註冊是位址暫存器。
ms.assetid: ad86013c-3358-4770-a01c-544c868691f4
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e58f42848034d12063611e14b82cb2f2d132cb43
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840467"
---
# <a name="address-register"></a><span data-ttu-id="6faf6-103">位址註冊</span><span class="sxs-lookup"><span data-stu-id="6faf6-103">Address Register</span></span>

<span data-ttu-id="6faf6-104">A0 註冊是位址暫存器。</span><span class="sxs-lookup"><span data-stu-id="6faf6-104">The a0 register is an address register.</span></span> <span data-ttu-id="6faf6-105">版本與 1 1 之間有提供單一 \_ 登錄 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6faf6-105">A single register is available in version vs\_1\_1.</span></span> <span data-ttu-id="6faf6-106">在 vs 1 1 中指定為 a0. x 的位址暫存器， \_ \_ 可用來做為相對定址的帶正負號整數位移，以取得常數暫存器檔案的相對定址。</span><span class="sxs-lookup"><span data-stu-id="6faf6-106">The address register, designated as a0.x in vs\_1\_1, can be used as a signed integer offset for relative addressing into the constant register file.</span></span> <span data-ttu-id="6faf6-107">針對版本與 \_ 2 \_ 0 （含）以上版本，所有四個元件 (. x、. y、. z、w) 都可用於相對定址。</span><span class="sxs-lookup"><span data-stu-id="6faf6-107">For versions vs\_2\_0 and above, all four components (.x, .y, .z, .w) are available for relative addressing.</span></span>


```
c[a0.x + n]
```



<span data-ttu-id="6faf6-108">端點著色器無法讀取位址暫存器，它只能用於常數暫存器的相對定址。</span><span class="sxs-lookup"><span data-stu-id="6faf6-108">The address register cannot be read by a vertex shader, it can only be used for relative addressing of a constant register.</span></span> <span data-ttu-id="6faf6-109">若讀取合法範圍以外的值，將會傳回 (0.0、0.0、0.0、0.0) 。</span><span class="sxs-lookup"><span data-stu-id="6faf6-109">Reading values outside of the legal range will return (0.0, 0.0, 0.0, 0.0).</span></span> <span data-ttu-id="6faf6-110">位址暫存器只能是 [mov-vs](mov---vs.md) 指令的目的地。</span><span class="sxs-lookup"><span data-stu-id="6faf6-110">The address register can only be a destination for the [mov - vs](mov---vs.md) instruction.</span></span> <span data-ttu-id="6faf6-111">如果將浮點數移至整數暫存器中，就會發生四捨五入到最接近的轉換。</span><span class="sxs-lookup"><span data-stu-id="6faf6-111">If a floating-point number is moved into an integer register, a round-to-nearest conversion happens.</span></span>

<span data-ttu-id="6faf6-112">所有著色器都必須先初始化位址暫存器，才能使用它。</span><span class="sxs-lookup"><span data-stu-id="6faf6-112">All shaders must initialize the address register before using it.</span></span> <span data-ttu-id="6faf6-113">針對版本 vs \_ 2 \_ 0 和更新版本， [mova vs](mova---vs.md) 指令可以將浮點值移至位址暫存器。</span><span class="sxs-lookup"><span data-stu-id="6faf6-113">For version vs\_2\_0 and above, the [mova - vs](mova---vs.md) instruction can move a floating-point value to an address register.</span></span>



| <span data-ttu-id="6faf6-114">頂點著色器版本</span><span class="sxs-lookup"><span data-stu-id="6faf6-114">Vertex shader versions</span></span> | <span data-ttu-id="6faf6-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="6faf6-115">1\_1</span></span> | <span data-ttu-id="6faf6-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6faf6-116">2\_0</span></span> | <span data-ttu-id="6faf6-117">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="6faf6-117">2\_sw</span></span> | <span data-ttu-id="6faf6-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="6faf6-118">2\_x</span></span> | <span data-ttu-id="6faf6-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6faf6-119">3\_0</span></span> | <span data-ttu-id="6faf6-120">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="6faf6-120">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="6faf6-121">位址註冊</span><span class="sxs-lookup"><span data-stu-id="6faf6-121">Address Register</span></span>       | <span data-ttu-id="6faf6-122">x</span><span class="sxs-lookup"><span data-stu-id="6faf6-122">x</span></span>    | <span data-ttu-id="6faf6-123">x</span><span class="sxs-lookup"><span data-stu-id="6faf6-123">x</span></span>    | <span data-ttu-id="6faf6-124">x</span><span class="sxs-lookup"><span data-stu-id="6faf6-124">x</span></span>     | <span data-ttu-id="6faf6-125">x</span><span class="sxs-lookup"><span data-stu-id="6faf6-125">x</span></span>    | <span data-ttu-id="6faf6-126">x</span><span class="sxs-lookup"><span data-stu-id="6faf6-126">x</span></span>    | <span data-ttu-id="6faf6-127">x</span><span class="sxs-lookup"><span data-stu-id="6faf6-127">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="6faf6-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="6faf6-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6faf6-129">頂點著色器暫存器</span><span class="sxs-lookup"><span data-stu-id="6faf6-129">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




