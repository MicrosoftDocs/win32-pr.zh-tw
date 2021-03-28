---
title: RWBuffer
description: 讀取/寫入緩衝區。
ms.assetid: e9b60e63-5b2b-4f45-834b-269e692ba84c
keywords:
- RWBuffer HLSL
topic_type:
- apiref
api_name:
- RWBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 765634da85fb74f2d3a3591bfe4767ccee1a80c8
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312560"
---
# <a name="rwbuffer"></a><span data-ttu-id="0a1df-104">RWBuffer</span><span class="sxs-lookup"><span data-stu-id="0a1df-104">RWBuffer</span></span>

<span data-ttu-id="0a1df-105">讀取/寫入緩衝區。</span><span class="sxs-lookup"><span data-stu-id="0a1df-105">A read/write buffer.</span></span>



| <span data-ttu-id="0a1df-106">方法</span><span class="sxs-lookup"><span data-stu-id="0a1df-106">Method</span></span>                                                     | <span data-ttu-id="0a1df-107">描述</span><span class="sxs-lookup"><span data-stu-id="0a1df-107">Description</span></span>                            |
|------------------------------------------------------------|----------------------------------------|
| [<span data-ttu-id="0a1df-108">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="0a1df-108">**GetDimensions**</span></span>](sm5-object-rwbuffer-getdimensions.md) | <span data-ttu-id="0a1df-109">取得資源維度。</span><span class="sxs-lookup"><span data-stu-id="0a1df-109">Gets the resource dimensions.</span></span>          |
| [<span data-ttu-id="0a1df-110">**載入**</span><span class="sxs-lookup"><span data-stu-id="0a1df-110">**Load**</span></span>](rwbuffer-load.md)                              | <span data-ttu-id="0a1df-111">取得讀寫緩衝區中的一個值。</span><span class="sxs-lookup"><span data-stu-id="0a1df-111">Gets one value in a read-write buffer.</span></span> |
| <span data-ttu-id="0a1df-112">[**運算子\[\]**](sm5-object-rwbuffer-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="0a1df-112">[**Operator\[\]**](sm5-object-rwbuffer-operatorindex.md)</span></span>  | <span data-ttu-id="0a1df-113">傳回資源變數。</span><span class="sxs-lookup"><span data-stu-id="0a1df-113">Returns a resource variable.</span></span>           |



 

<span data-ttu-id="0a1df-114">資源變數也可以傳遞至任何未排序或連鎖的作業。</span><span class="sxs-lookup"><span data-stu-id="0a1df-114">A resource variable can also be passed into any unordered or interlocked operation.</span></span>

<span data-ttu-id="0a1df-115">**RWBuffer** 物件的前面可以加上儲存類別 **globallycoherent**。</span><span class="sxs-lookup"><span data-stu-id="0a1df-115">**RWBuffer** objects can be prefixed with the storage class **globallycoherent**.</span></span> <span data-ttu-id="0a1df-116">此儲存類別會造成記憶體阻礙和同步處理，以排清整個 GPU 上的資料，讓其他群組可以看到寫入。</span><span class="sxs-lookup"><span data-stu-id="0a1df-116">This storage class causes memory barriers and syncs to flush data across the entire GPU such that other groups can see writes.</span></span> <span data-ttu-id="0a1df-117">如果沒有這個規範，記憶體屏障或同步將只會在目前群組內排清 UAV。</span><span class="sxs-lookup"><span data-stu-id="0a1df-117">Without this specifier, a memory barrier or sync will flush a UAV only within the current group.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="0a1df-118">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="0a1df-118">Minimum Shader Model</span></span>

<span data-ttu-id="0a1df-119">下列著色器模型支援此物件。</span><span class="sxs-lookup"><span data-stu-id="0a1df-119">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="0a1df-120">著色器模型</span><span class="sxs-lookup"><span data-stu-id="0a1df-120">Shader Model</span></span>                                                                | <span data-ttu-id="0a1df-121">支援</span><span class="sxs-lookup"><span data-stu-id="0a1df-121">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="0a1df-122">[著色器模型 5](d3d11-graphics-reference-sm5.md) 和更新版本的著色器模型</span><span class="sxs-lookup"><span data-stu-id="0a1df-122">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="0a1df-123">是</span><span class="sxs-lookup"><span data-stu-id="0a1df-123">yes</span></span>       |



 

<span data-ttu-id="0a1df-124">下列著色器類型支援此物件：</span><span class="sxs-lookup"><span data-stu-id="0a1df-124">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="0a1df-125">頂點</span><span class="sxs-lookup"><span data-stu-id="0a1df-125">Vertex</span></span> | <span data-ttu-id="0a1df-126">船體</span><span class="sxs-lookup"><span data-stu-id="0a1df-126">Hull</span></span> | <span data-ttu-id="0a1df-127">網域</span><span class="sxs-lookup"><span data-stu-id="0a1df-127">Domain</span></span> | <span data-ttu-id="0a1df-128">幾何</span><span class="sxs-lookup"><span data-stu-id="0a1df-128">Geometry</span></span> | <span data-ttu-id="0a1df-129">像素</span><span class="sxs-lookup"><span data-stu-id="0a1df-129">Pixel</span></span> | <span data-ttu-id="0a1df-130">計算</span><span class="sxs-lookup"><span data-stu-id="0a1df-130">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="0a1df-131">x</span><span class="sxs-lookup"><span data-stu-id="0a1df-131">x</span></span>     | <span data-ttu-id="0a1df-132">x</span><span class="sxs-lookup"><span data-stu-id="0a1df-132">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="0a1df-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0a1df-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a1df-134">著色器模型5物件</span><span class="sxs-lookup"><span data-stu-id="0a1df-134">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




