---
title: texdp3-ps
description: 在材質暫存器編號中的資料和對應至目的地暫存器編號的材質座標集合之間，執行三個元件的點乘積。
ms.assetid: 82e02f3f-4b88-4007-b4be-0c66223d9c66
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 64cc14ee66123ea3e25941579b9838977a753174
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313617"
---
# <a name="texdp3---ps"></a><span data-ttu-id="e2222-103">texdp3-ps</span><span class="sxs-lookup"><span data-stu-id="e2222-103">texdp3 - ps</span></span>

<span data-ttu-id="e2222-104">在材質暫存器編號中的資料和對應至目的地暫存器編號的材質座標集合之間，執行三個元件的點乘積。</span><span class="sxs-lookup"><span data-stu-id="e2222-104">Performs a three-component dot product between data in the texture register number and the texture coordinate set corresponding to the destination register number.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2222-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e2222-105">Syntax</span></span>



| <span data-ttu-id="e2222-106">texdp3 dst、src</span><span class="sxs-lookup"><span data-stu-id="e2222-106">texdp3 dst, src</span></span> |
|-----------------|



 

<span data-ttu-id="e2222-107">其中</span><span class="sxs-lookup"><span data-stu-id="e2222-107">where</span></span>

-   <span data-ttu-id="e2222-108">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="e2222-108">dst is the destination register.</span></span>
-   <span data-ttu-id="e2222-109">src 是來源暫存器。</span><span class="sxs-lookup"><span data-stu-id="e2222-109">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2222-110">備註</span><span class="sxs-lookup"><span data-stu-id="e2222-110">Remarks</span></span>



| <span data-ttu-id="e2222-111">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="e2222-111">Pixel shader versions</span></span> | <span data-ttu-id="e2222-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="e2222-112">1\_1</span></span> | <span data-ttu-id="e2222-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="e2222-113">1\_2</span></span> | <span data-ttu-id="e2222-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="e2222-114">1\_3</span></span> | <span data-ttu-id="e2222-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="e2222-115">1\_4</span></span> | <span data-ttu-id="e2222-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e2222-116">2\_0</span></span> | <span data-ttu-id="e2222-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="e2222-117">2\_x</span></span> | <span data-ttu-id="e2222-118">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="e2222-118">2\_sw</span></span> | <span data-ttu-id="e2222-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e2222-119">3\_0</span></span> | <span data-ttu-id="e2222-120">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="e2222-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="e2222-121">texdp3</span><span class="sxs-lookup"><span data-stu-id="e2222-121">texdp3</span></span>                |      | <span data-ttu-id="e2222-122">x</span><span class="sxs-lookup"><span data-stu-id="e2222-122">x</span></span>    | <span data-ttu-id="e2222-123">x</span><span class="sxs-lookup"><span data-stu-id="e2222-123">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="e2222-124">材質暫存器必須使用下列順序。</span><span class="sxs-lookup"><span data-stu-id="e2222-124">Texture registers must use the following sequence.</span></span>


```
 
tex    t(n)        // Define tn as a standard 3-vector (tn must be 
                   //   defined in some way before texdp3 uses it)
texdp3 t(m), t(n)  // where m > n
                   // Perform a three-component dot product between tn and 
                   //   the texture coordinate set m. The scalar result is
                   //   replicated to all components of t(m)
```



<span data-ttu-id="e2222-125">以下是如何完成點乘積的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="e2222-125">Here is more detail about how the dot product is accomplished.</span></span>

<span data-ttu-id="e2222-126">Texdp3 指令會執行三個元件的點乘積，並將其複製到所有四個色頻。</span><span class="sxs-lookup"><span data-stu-id="e2222-126">The texdp3 instruction performs a three-component dot product and replicates it to all four color channels.</span></span>

<span data-ttu-id="e2222-127">t (m) <sub>RGBA</sub> = TextureCoordinates (階段 m) <sub>UVW</sub> \* t (x) <sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="e2222-127">t(m)<sub>RGBA</sub> = TextureCoordinates(stage m)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

## <a name="related-topics"></a><span data-ttu-id="e2222-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="e2222-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2222-129">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="e2222-129">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




