---
title: else-vs
description: 其他區塊的開頭。 |else-vs
ms.assetid: c3bd99c2-35a1-4ffd-9781-4bac9f6bb0ef
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 97481d7cb651719fdf0843fd1b985c6586e54b3b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974329"
---
# <a name="else---vs"></a><span data-ttu-id="849e8-104">else-vs</span><span class="sxs-lookup"><span data-stu-id="849e8-104">else - vs</span></span>

<span data-ttu-id="849e8-105">其他區塊的開頭。</span><span class="sxs-lookup"><span data-stu-id="849e8-105">Start of an else block.</span></span>

## <a name="syntax"></a><span data-ttu-id="849e8-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="849e8-106">Syntax</span></span>



| <span data-ttu-id="849e8-107">else</span><span class="sxs-lookup"><span data-stu-id="849e8-107">else</span></span> |
|------|



 

## <a name="remarks"></a><span data-ttu-id="849e8-108">備註</span><span class="sxs-lookup"><span data-stu-id="849e8-108">Remarks</span></span>



| <span data-ttu-id="849e8-109">頂點著色器版本</span><span class="sxs-lookup"><span data-stu-id="849e8-109">Vertex shader versions</span></span> | <span data-ttu-id="849e8-110">1\_1</span><span class="sxs-lookup"><span data-stu-id="849e8-110">1\_1</span></span> | <span data-ttu-id="849e8-111">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="849e8-111">2\_0</span></span> | <span data-ttu-id="849e8-112">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="849e8-112">2\_x</span></span> | <span data-ttu-id="849e8-113">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="849e8-113">2\_sw</span></span> | <span data-ttu-id="849e8-114">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="849e8-114">3\_0</span></span> | <span data-ttu-id="849e8-115">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="849e8-115">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="849e8-116">else</span><span class="sxs-lookup"><span data-stu-id="849e8-116">else</span></span>                   |      | <span data-ttu-id="849e8-117">x</span><span class="sxs-lookup"><span data-stu-id="849e8-117">x</span></span>    | <span data-ttu-id="849e8-118">x</span><span class="sxs-lookup"><span data-stu-id="849e8-118">x</span></span>    | <span data-ttu-id="849e8-119">x</span><span class="sxs-lookup"><span data-stu-id="849e8-119">x</span></span>     | <span data-ttu-id="849e8-120">x</span><span class="sxs-lookup"><span data-stu-id="849e8-120">x</span></span>    | <span data-ttu-id="849e8-121">x</span><span class="sxs-lookup"><span data-stu-id="849e8-121">x</span></span>     |



 

<span data-ttu-id="849e8-122">如果對應的 [if bool-vs](if-bool---vs.md) 語句中的條件為 true，則會執行 if bool-vs 語句和相符的 [endif](endif---vs.md) 所括住的程式碼。</span><span class="sxs-lookup"><span data-stu-id="849e8-122">If the condition in the corresponding [if bool - vs](if-bool---vs.md) statement is true, the code enclosed by the if bool - vs statement and the matching [endif](endif---vs.md) is run.</span></span> <span data-ttu-id="849e8-123">否則，程式碼會以其他 .。。執行 endif 語句。</span><span class="sxs-lookup"><span data-stu-id="849e8-123">Otherwise, the code enclosed by the else...endif statements is run.</span></span>

## <a name="related-topics"></a><span data-ttu-id="849e8-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="849e8-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="849e8-125">頂點著色器指示</span><span class="sxs-lookup"><span data-stu-id="849e8-125">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> <dt>

[<span data-ttu-id="849e8-126">if bool-vs</span><span class="sxs-lookup"><span data-stu-id="849e8-126">if bool - vs</span></span>](if-bool---vs.md)
</dt> <dt>

[<span data-ttu-id="849e8-127">endif-vs</span><span class="sxs-lookup"><span data-stu-id="849e8-127">endif - vs</span></span>](endif---vs.md)
</dt> </dl>

 

 




