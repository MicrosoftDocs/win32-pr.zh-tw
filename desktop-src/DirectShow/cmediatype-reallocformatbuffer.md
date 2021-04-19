---
description: ReallocFormatBuffer 方法會將格式區塊重新配置為新的大小。
ms.assetid: 49bec677-09cc-4e1a-994a-13e873e61713
title: 'CMediaType. ReallocFormatBuffer 方法 (Mtype .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.ReallocFormatBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 22e861c61f01a7594d720833e2b3a4b923a1e183
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990115"
---
# <a name="cmediatypereallocformatbuffer-method"></a><span data-ttu-id="62941-103">CMediaType. ReallocFormatBuffer 方法</span><span class="sxs-lookup"><span data-stu-id="62941-103">CMediaType.ReallocFormatBuffer method</span></span>

<span data-ttu-id="62941-104">方法會將 `ReallocFormatBuffer` 格式區塊重新配置為新的大小。</span><span class="sxs-lookup"><span data-stu-id="62941-104">The `ReallocFormatBuffer` method reallocates the format block to a new size.</span></span>

## <a name="syntax"></a><span data-ttu-id="62941-105">語法</span><span class="sxs-lookup"><span data-stu-id="62941-105">Syntax</span></span>


```C++
BYTE* ReallocFormatBuffer(
   ULONG length
);
```



## <a name="parameters"></a><span data-ttu-id="62941-106">參數</span><span class="sxs-lookup"><span data-stu-id="62941-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62941-107">*length* (長度)</span><span class="sxs-lookup"><span data-stu-id="62941-107">*length*</span></span> 
</dt> <dd>

<span data-ttu-id="62941-108">格式區塊所需的新大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="62941-108">New size required for the format block, in bytes.</span></span> <span data-ttu-id="62941-109">必須大於零。</span><span class="sxs-lookup"><span data-stu-id="62941-109">Must be greater than zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62941-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="62941-110">Return value</span></span>

<span data-ttu-id="62941-111">如果成功，則傳回新區塊的指標。</span><span class="sxs-lookup"><span data-stu-id="62941-111">Returns a pointer to the new block if successful.</span></span> <span data-ttu-id="62941-112">否則，會傳回舊格式區塊的指標，或傳回 **Null**。</span><span class="sxs-lookup"><span data-stu-id="62941-112">Otherwise, returns either a pointer to the old format block, or **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="62941-113">備註</span><span class="sxs-lookup"><span data-stu-id="62941-113">Remarks</span></span>

<span data-ttu-id="62941-114">這個方法會配置新的格式區塊。</span><span class="sxs-lookup"><span data-stu-id="62941-114">This method allocates a new format block.</span></span> <span data-ttu-id="62941-115">它會將現有的格式區塊盡可能複製到新的格式區塊。</span><span class="sxs-lookup"><span data-stu-id="62941-115">It copies as much of the existing format block as possible into the new format block.</span></span> <span data-ttu-id="62941-116">如果新區塊小於現有區塊，則會截斷現有的格式區塊。</span><span class="sxs-lookup"><span data-stu-id="62941-116">If the new block is smaller than the existing block, the existing format block is truncated.</span></span> <span data-ttu-id="62941-117">如果新的區塊更大，則不會定義其他空間的內容。</span><span class="sxs-lookup"><span data-stu-id="62941-117">If the new block is larger, the contents of the additional space are undefined.</span></span> <span data-ttu-id="62941-118">它們不會明確設定為零。</span><span class="sxs-lookup"><span data-stu-id="62941-118">They are not explicitly set to zero.</span></span>

<span data-ttu-id="62941-119">方法會更新 **AM \_ 媒體 \_ 類型** 結構的 **cbFormat** 和 **pbFormat** 成員。</span><span class="sxs-lookup"><span data-stu-id="62941-119">The method updates the **cbFormat** and **pbFormat** members of the **AM\_MEDIA\_TYPE** structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="62941-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="62941-120">Requirements</span></span>



| <span data-ttu-id="62941-121">需求</span><span class="sxs-lookup"><span data-stu-id="62941-121">Requirement</span></span> | <span data-ttu-id="62941-122">值</span><span class="sxs-lookup"><span data-stu-id="62941-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62941-123">標頭</span><span class="sxs-lookup"><span data-stu-id="62941-123">Header</span></span><br/>  | <dl> <span data-ttu-id="62941-124"><dt>Mtype (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="62941-124"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="62941-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="62941-125">Library</span></span><br/> | <dl> <span data-ttu-id="62941-126"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="62941-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62941-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="62941-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62941-128">**CMediaType 類別**</span><span class="sxs-lookup"><span data-stu-id="62941-128">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




