---
title: texm3x3pad-ps
description: 執行三個數據列矩陣相乘的第一個或第二個數據列相乘。 此指令必須與 texm3x3-ps、texm3x3spec-ps、texm3x3vspec-ps 或 texm3x3tex-ps 組合使用。
ms.assetid: 375526ee-cd58-4179-9b21-c63f17282f6b
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0013c4d2baf9a404406982b5a8e984698a964f33
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104373782"
---
# <a name="texm3x3pad---ps"></a><span data-ttu-id="c1c86-104">texm3x3pad-ps</span><span class="sxs-lookup"><span data-stu-id="c1c86-104">texm3x3pad - ps</span></span>

<span data-ttu-id="c1c86-105">執行三個數據列矩陣相乘的第一個或第二個數據列相乘。</span><span class="sxs-lookup"><span data-stu-id="c1c86-105">Performs the first or second row multiply of a three-row matrix multiply.</span></span> <span data-ttu-id="c1c86-106">此指令必須與 [texm3x3-ps](texm3x3---ps.md)、 [texm3x3spec-ps](texm3x3spec---ps.md)、 [texm3x3vspec-ps](texm3x3vspec---ps.md)或 [texm3x3tex-ps](texm3x3tex---ps.md)組合使用。</span><span class="sxs-lookup"><span data-stu-id="c1c86-106">This instruction must be used in combination with [texm3x3 - ps](texm3x3---ps.md), [texm3x3spec - ps](texm3x3spec---ps.md), [texm3x3vspec - ps](texm3x3vspec---ps.md), or [texm3x3tex - ps](texm3x3tex---ps.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c1c86-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c1c86-107">Syntax</span></span>



| <span data-ttu-id="c1c86-108">texm3x3pad dst、src</span><span class="sxs-lookup"><span data-stu-id="c1c86-108">texm3x3pad dst, src</span></span> |
|---------------------|



 

<span data-ttu-id="c1c86-109">其中</span><span class="sxs-lookup"><span data-stu-id="c1c86-109">where</span></span>

-   <span data-ttu-id="c1c86-110">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="c1c86-110">dst is the destination register.</span></span>
-   <span data-ttu-id="c1c86-111">src 是來源暫存器。</span><span class="sxs-lookup"><span data-stu-id="c1c86-111">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1c86-112">備註</span><span class="sxs-lookup"><span data-stu-id="c1c86-112">Remarks</span></span>



| <span data-ttu-id="c1c86-113">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="c1c86-113">Pixel shader versions</span></span> | <span data-ttu-id="c1c86-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="c1c86-114">1\_1</span></span> | <span data-ttu-id="c1c86-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="c1c86-115">1\_2</span></span> | <span data-ttu-id="c1c86-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="c1c86-116">1\_3</span></span> | <span data-ttu-id="c1c86-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="c1c86-117">1\_4</span></span> | <span data-ttu-id="c1c86-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c1c86-118">2\_0</span></span> | <span data-ttu-id="c1c86-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="c1c86-119">2\_x</span></span> | <span data-ttu-id="c1c86-120">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="c1c86-120">2\_sw</span></span> | <span data-ttu-id="c1c86-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c1c86-121">3\_0</span></span> | <span data-ttu-id="c1c86-122">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="c1c86-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="c1c86-123">texm3x3pad</span><span class="sxs-lookup"><span data-stu-id="c1c86-123">texm3x3pad</span></span>            | <span data-ttu-id="c1c86-124">x</span><span class="sxs-lookup"><span data-stu-id="c1c86-124">x</span></span>    | <span data-ttu-id="c1c86-125">x</span><span class="sxs-lookup"><span data-stu-id="c1c86-125">x</span></span>    | <span data-ttu-id="c1c86-126">x</span><span class="sxs-lookup"><span data-stu-id="c1c86-126">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="c1c86-127">此指令本身不能使用。</span><span class="sxs-lookup"><span data-stu-id="c1c86-127">This instruction cannot be used by itself.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c1c86-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="c1c86-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1c86-129">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="c1c86-129">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




