---
description: CRendererPosPassThru 類別會處理轉譯器篩選的搜尋命令，方法是將它們傳遞給下一個篩選器。
ms.assetid: 7b532177-939c-4cb7-a6fa-c0133f65c768
title: 'CRendererPosPassThru 類別 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7154dde8adefdb3292107e9c33d7b6a2b54f6af0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994043"
---
# <a name="crendererpospassthru-class"></a><span data-ttu-id="f6154-103">CRendererPosPassThru 類別</span><span class="sxs-lookup"><span data-stu-id="f6154-103">CRendererPosPassThru class</span></span>

![crendererpospassthru 類別階層](images/cutil14.png)

<span data-ttu-id="f6154-105">`CRendererPosPassThru`類別會處理轉譯器篩選的搜尋命令，方法是將它們傳遞給下一個篩選器。</span><span class="sxs-lookup"><span data-stu-id="f6154-105">The `CRendererPosPassThru` class handles seek commands for renderer filters, by passing them upstream to the next filter.</span></span>

<span data-ttu-id="f6154-106">這個類別衍生自 [**CPosPassThru**](cpospassthru.md) 類別。</span><span class="sxs-lookup"><span data-stu-id="f6154-106">This class derives from the [**CPosPassThru**](cpospassthru.md) class.</span></span> <span data-ttu-id="f6154-107">它新增了在範例抵達時快取時間戳記的支援。</span><span class="sxs-lookup"><span data-stu-id="f6154-107">It adds support for caching the time stamps from samples as they arrive.</span></span> <span data-ttu-id="f6154-108">使用與 **CPosPassThru** 類別相同的方式來使用這個類別。</span><span class="sxs-lookup"><span data-stu-id="f6154-108">Use this class in the same way as the **CPosPassThru** class.</span></span> <span data-ttu-id="f6154-109">如需詳細資訊，請參閱 **CPosPassThru** 檔。</span><span class="sxs-lookup"><span data-stu-id="f6154-109">Refer to the **CPosPassThru** documentation for details.</span></span>

<span data-ttu-id="f6154-110">轉譯器篩選準則必須更新 `CRendererPosPassThru` 物件的快取時間戳記，如下所示：</span><span class="sxs-lookup"><span data-stu-id="f6154-110">The renderer filter must update the `CRendererPosPassThru` object's cached time stamps, as follows:</span></span>

-   <span data-ttu-id="f6154-111">針對篩選器收到的每個範例，呼叫 [**CRendererPosPassThru：： RegisterMediaTime**](crendererpospassthru-registermediatime.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="f6154-111">For each sample the filter receives, call the [**CRendererPosPassThru::RegisterMediaTime**](crendererpospassthru-registermediatime.md) method.</span></span>
-   <span data-ttu-id="f6154-112">當篩選準則停止或接收 **EndFlush** 呼叫時，請呼叫 [**CRendererPosPassThru：： ResetMediaTime**](crendererpospassthru-resetmediatime.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="f6154-112">When the filter is stopped or receives an **EndFlush** call, call the [**CRendererPosPassThru::ResetMediaTime**](crendererpospassthru-resetmediatime.md) method.</span></span>
-   <span data-ttu-id="f6154-113">當篩選接收到資料流程結束通知時，請呼叫 [**CRendererPosPassThru：： EOS**](crendererpospassthru-eos.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="f6154-113">When the filter receives an end-of-stream notification, call the [**CRendererPosPassThru::EOS**](crendererpospassthru-eos.md) method.</span></span>

<span data-ttu-id="f6154-114">如需如何使用這個類別的範例，請參閱 [**CBaseRenderer**](cbaserenderer.md) 原始程式碼。</span><span class="sxs-lookup"><span data-stu-id="f6154-114">For an example of how to use this class, refer to the [**CBaseRenderer**](cbaserenderer.md) source code.</span></span>



| <span data-ttu-id="f6154-115">公用方法</span><span class="sxs-lookup"><span data-stu-id="f6154-115">Public Methods</span></span>                                                            | <span data-ttu-id="f6154-116">Description</span><span class="sxs-lookup"><span data-stu-id="f6154-116">Description</span></span>                                                         |
|---------------------------------------------------------------------------|---------------------------------------------------------------------|
| [<span data-ttu-id="f6154-117">**CRendererPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="f6154-117">**CRendererPosPassThru**</span></span>](crendererpospassthru-crendererpospassthru.md) | <span data-ttu-id="f6154-118">函式方法。</span><span class="sxs-lookup"><span data-stu-id="f6154-118">Constructor method.</span></span>                                                 |
| [<span data-ttu-id="f6154-119">**GetMediaTime**</span><span class="sxs-lookup"><span data-stu-id="f6154-119">**GetMediaTime**</span></span>](crendererpospassthru-getmediatime.md)                 | <span data-ttu-id="f6154-120">抓取目前樣本上的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="f6154-120">Retrieves the time stamps on the current sample.</span></span>                    |
| [<span data-ttu-id="f6154-121">**RegisterMediaTime**</span><span class="sxs-lookup"><span data-stu-id="f6154-121">**RegisterMediaTime**</span></span>](crendererpospassthru-registermediatime.md)       | <span data-ttu-id="f6154-122">快取目前範例中的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="f6154-122">Caches the time stamps from the current sample.</span></span>                     |
| [<span data-ttu-id="f6154-123">**ResetMediaTime**</span><span class="sxs-lookup"><span data-stu-id="f6154-123">**ResetMediaTime**</span></span>](crendererpospassthru-resetmediatime.md)             | <span data-ttu-id="f6154-124">將快取的時間戳記重設為零。</span><span class="sxs-lookup"><span data-stu-id="f6154-124">Resets the cached time stamps to zero.</span></span>                              |
| [<span data-ttu-id="f6154-125">**Eos**</span><span class="sxs-lookup"><span data-stu-id="f6154-125">**EOS**</span></span>](crendererpospassthru-eos.md)                                   | <span data-ttu-id="f6154-126">在結束資料流程通知之後，更新快取的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="f6154-126">Updates the cached time stamps after an end-of-stream notification.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="f6154-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="f6154-127">Requirements</span></span>



| <span data-ttu-id="f6154-128">需求</span><span class="sxs-lookup"><span data-stu-id="f6154-128">Requirement</span></span> | <span data-ttu-id="f6154-129">值</span><span class="sxs-lookup"><span data-stu-id="f6154-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6154-130">標頭</span><span class="sxs-lookup"><span data-stu-id="f6154-130">Header</span></span><br/>  | <dl> <span data-ttu-id="f6154-131"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="f6154-131"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f6154-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="f6154-132">Library</span></span><br/> | <dl> <span data-ttu-id="f6154-133"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="f6154-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




