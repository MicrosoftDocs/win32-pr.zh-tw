---
title: texm3x2pad-ps
description: 執行兩個數據列矩陣相乘的第一個資料列乘法。 此指令必須與 texm3x2tex-ps 或 texm3x2depth （ps）結合。 如需使用 texmpad 的詳細資訊，請參閱下列其中一項指示。
ms.assetid: 26eb3237-6e48-4880-b40d-37de8d65daa6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 91d161d0b3cc7a90bbbfcee17774b1a587e4c04f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "103841672"
---
# <a name="texm3x2pad---ps"></a><span data-ttu-id="c7c9b-105">texm3x2pad-ps</span><span class="sxs-lookup"><span data-stu-id="c7c9b-105">texm3x2pad - ps</span></span>

<span data-ttu-id="c7c9b-106">執行兩個數據列矩陣相乘的第一個資料列乘法。</span><span class="sxs-lookup"><span data-stu-id="c7c9b-106">Performs the first row multiplication of a two-row matrix multiply.</span></span> <span data-ttu-id="c7c9b-107">此指令必須與 [texm3x2tex-ps](texm3x2tex---ps.md) 或 [texm3x2depth （ps](texm3x2depth---ps.md)）結合。</span><span class="sxs-lookup"><span data-stu-id="c7c9b-107">This instruction must be combined with either [texm3x2tex - ps](texm3x2tex---ps.md) or [texm3x2depth - ps](texm3x2depth---ps.md).</span></span> <span data-ttu-id="c7c9b-108">如需使用 texmpad 的詳細資訊，請參閱下列其中一項指示。</span><span class="sxs-lookup"><span data-stu-id="c7c9b-108">Refer to either of these instructions for details on using texmpad.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7c9b-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="c7c9b-109">Syntax</span></span>



| <span data-ttu-id="c7c9b-110">tex3x2pad dst、src</span><span class="sxs-lookup"><span data-stu-id="c7c9b-110">tex3x2pad dst, src</span></span> |
|--------------------|



 

<span data-ttu-id="c7c9b-111">其中</span><span class="sxs-lookup"><span data-stu-id="c7c9b-111">where</span></span>

-   <span data-ttu-id="c7c9b-112">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="c7c9b-112">dst is the destination register.</span></span>
-   <span data-ttu-id="c7c9b-113">src 是來源暫存器。</span><span class="sxs-lookup"><span data-stu-id="c7c9b-113">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7c9b-114">備註</span><span class="sxs-lookup"><span data-stu-id="c7c9b-114">Remarks</span></span>



| <span data-ttu-id="c7c9b-115">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="c7c9b-115">Pixel shader versions</span></span> | <span data-ttu-id="c7c9b-116">1\_1</span><span class="sxs-lookup"><span data-stu-id="c7c9b-116">1\_1</span></span> | <span data-ttu-id="c7c9b-117">1\_2</span><span class="sxs-lookup"><span data-stu-id="c7c9b-117">1\_2</span></span> | <span data-ttu-id="c7c9b-118">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="c7c9b-118">1\_3</span></span> | <span data-ttu-id="c7c9b-119">1\_4</span><span class="sxs-lookup"><span data-stu-id="c7c9b-119">1\_4</span></span> | <span data-ttu-id="c7c9b-120">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c7c9b-120">2\_0</span></span> | <span data-ttu-id="c7c9b-121">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="c7c9b-121">2\_x</span></span> | <span data-ttu-id="c7c9b-122">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="c7c9b-122">2\_sw</span></span> | <span data-ttu-id="c7c9b-123">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c7c9b-123">3\_0</span></span> | <span data-ttu-id="c7c9b-124">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="c7c9b-124">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="c7c9b-125">texm3x2pad</span><span class="sxs-lookup"><span data-stu-id="c7c9b-125">texm3x2pad</span></span>            | <span data-ttu-id="c7c9b-126">x</span><span class="sxs-lookup"><span data-stu-id="c7c9b-126">x</span></span>    | <span data-ttu-id="c7c9b-127">x</span><span class="sxs-lookup"><span data-stu-id="c7c9b-127">x</span></span>    | <span data-ttu-id="c7c9b-128">x</span><span class="sxs-lookup"><span data-stu-id="c7c9b-128">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="c7c9b-129">此指令本身不能使用。</span><span class="sxs-lookup"><span data-stu-id="c7c9b-129">This instruction cannot be used by itself.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c7c9b-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="c7c9b-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7c9b-131">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="c7c9b-131">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




