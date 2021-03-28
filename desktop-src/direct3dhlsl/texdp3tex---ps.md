---
title: texdp3tex-ps
description: 執行三個元件的點乘積，並使用結果來執行1D 紋理查閱。
ms.assetid: vs|directx_sdk|~\texdp3tex___ps.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dfe74dd0a73bc47cd2855d35b239e80a1b5153c1
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990711"
---
# <a name="texdp3tex---ps"></a><span data-ttu-id="248db-103">texdp3tex-ps</span><span class="sxs-lookup"><span data-stu-id="248db-103">texdp3tex - ps</span></span>

<span data-ttu-id="248db-104">執行三個元件的點乘積，並使用結果來執行1D 紋理查閱。</span><span class="sxs-lookup"><span data-stu-id="248db-104">Performs a three-component dot product and uses the result to do a 1D texture lookup.</span></span>

## <a name="syntax"></a><span data-ttu-id="248db-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="248db-105">Syntax</span></span>



| <span data-ttu-id="248db-106">texdp3tex dst、src</span><span class="sxs-lookup"><span data-stu-id="248db-106">texdp3tex dst, src</span></span> |
|--------------------|



 

<span data-ttu-id="248db-107">其中</span><span class="sxs-lookup"><span data-stu-id="248db-107">where</span></span>

-   <span data-ttu-id="248db-108">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="248db-108">dst is the destination register.</span></span>
-   <span data-ttu-id="248db-109">src 是來源暫存器。</span><span class="sxs-lookup"><span data-stu-id="248db-109">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="248db-110">備註</span><span class="sxs-lookup"><span data-stu-id="248db-110">Remarks</span></span>



| <span data-ttu-id="248db-111">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="248db-111">Pixel shader versions</span></span> | <span data-ttu-id="248db-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="248db-112">1\_1</span></span> | <span data-ttu-id="248db-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="248db-113">1\_2</span></span> | <span data-ttu-id="248db-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="248db-114">1\_3</span></span> | <span data-ttu-id="248db-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="248db-115">1\_4</span></span> | <span data-ttu-id="248db-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="248db-116">2\_0</span></span> | <span data-ttu-id="248db-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="248db-117">2\_x</span></span> | <span data-ttu-id="248db-118">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="248db-118">2\_sw</span></span> | <span data-ttu-id="248db-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="248db-119">3\_0</span></span> | <span data-ttu-id="248db-120">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="248db-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="248db-121">texdp3tex</span><span class="sxs-lookup"><span data-stu-id="248db-121">texdp3tex</span></span>             |      | <span data-ttu-id="248db-122">x</span><span class="sxs-lookup"><span data-stu-id="248db-122">x</span></span>    | <span data-ttu-id="248db-123">x</span><span class="sxs-lookup"><span data-stu-id="248db-123">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="248db-124">材質暫存器必須使用下列順序。</span><span class="sxs-lookup"><span data-stu-id="248db-124">Texture registers must use the following sequence.</span></span>


```
 
tex       t(n)        // Define tn as a standard 3-vector (tn must be 
                      // defined in some way before texdp3tex uses it)
texdp3tex t(m), t(n)  // where m > n                 
                      // Perform a three-component dot product between t(n) and 
                      // the texture coordinate set m. Use the scalar result to
                      // do a 1D texture lookup at texturestage m and place
                      // the result in t(m)
```



<span data-ttu-id="248db-125">以下是如何完成點乘積和紋理查閱的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="248db-125">Here is more detail about how the dot product and texture lookup are done.</span></span>

<span data-ttu-id="248db-126">Texdp3tex 指令會執行三個元件的點乘積。</span><span class="sxs-lookup"><span data-stu-id="248db-126">The texdp3tex instruction performs a three-component dot product.</span></span>

<span data-ttu-id="248db-127">u ' = TextureCoordinates (階段 m) <sub>UVW</sub> \* t (n) <sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="248db-127">u' = TextureCoordinates(stage m)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="248db-128">結果是用來執行1D 查閱，以在材質階段 m 進行紋理取樣。</span><span class="sxs-lookup"><span data-stu-id="248db-128">The result is used to sample the texture at texture stage m by performing a 1D lookup.</span></span>

<span data-ttu-id="248db-129">t (m) <sub>rgba</sub> = TextureSample (階段 m) <sub>RGBA</sub> 使用 (u '，0，0) 作為座標</span><span class="sxs-lookup"><span data-stu-id="248db-129">t(m)<sub>RGBA</sub> = TextureSample(stage m)<sub>RGBA</sub> using (u',0,0) as coordinates</span></span>

## <a name="related-topics"></a><span data-ttu-id="248db-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="248db-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="248db-131">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="248db-131">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




