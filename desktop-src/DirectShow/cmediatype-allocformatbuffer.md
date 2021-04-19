---
description: AllocFormatBuffer 方法會為格式區塊配置記憶體。
ms.assetid: 5ff716c7-f9cf-4b1c-9d3a-62ab955c1392
title: 'CMediaType. AllocFormatBuffer 方法 (Mtype .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.AllocFormatBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d6a9314fd06734adcc367b7be34dc8d6d1b9d996
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999071"
---
# <a name="cmediatypeallocformatbuffer-method"></a><span data-ttu-id="99f80-103">CMediaType. AllocFormatBuffer 方法</span><span class="sxs-lookup"><span data-stu-id="99f80-103">CMediaType.AllocFormatBuffer method</span></span>

<span data-ttu-id="99f80-104">方法會配置 `AllocFormatBuffer` 格式區塊的記憶體。</span><span class="sxs-lookup"><span data-stu-id="99f80-104">The `AllocFormatBuffer` method allocates memory for the format block.</span></span>

## <a name="syntax"></a><span data-ttu-id="99f80-105">語法</span><span class="sxs-lookup"><span data-stu-id="99f80-105">Syntax</span></span>


```C++
BYTE* AllocFormatBuffer(
   ULONG length
);
```



## <a name="parameters"></a><span data-ttu-id="99f80-106">參數</span><span class="sxs-lookup"><span data-stu-id="99f80-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99f80-107">*length* (長度)</span><span class="sxs-lookup"><span data-stu-id="99f80-107">*length*</span></span> 
</dt> <dd>

<span data-ttu-id="99f80-108">格式區塊所需的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="99f80-108">Size required for the format block, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99f80-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="99f80-109">Return value</span></span>

<span data-ttu-id="99f80-110">如果成功，則傳回新區塊的指標。</span><span class="sxs-lookup"><span data-stu-id="99f80-110">Returns a pointer to the new block if successful.</span></span> <span data-ttu-id="99f80-111">否則，會傳回 **Null**。</span><span class="sxs-lookup"><span data-stu-id="99f80-111">Otherwise, returns **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="99f80-112">備註</span><span class="sxs-lookup"><span data-stu-id="99f80-112">Remarks</span></span>

<span data-ttu-id="99f80-113">如果方法成功配置新的格式區塊，就會釋出現有的格式區塊。</span><span class="sxs-lookup"><span data-stu-id="99f80-113">If the method successfully allocates a new format block, it frees the existing format block.</span></span> <span data-ttu-id="99f80-114">如果配置失敗，方法會保留現有的格式區塊。</span><span class="sxs-lookup"><span data-stu-id="99f80-114">If the allocation fails, the method leaves the existing format block.</span></span>

<span data-ttu-id="99f80-115">方法會更新 **AM \_ 媒體 \_ 類型** 結構的 **cbFormat** 和 **pbFormat** 成員。</span><span class="sxs-lookup"><span data-stu-id="99f80-115">The method updates the **cbFormat** and **pbFormat** members of the **AM\_MEDIA\_TYPE** structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="99f80-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="99f80-116">Requirements</span></span>



| <span data-ttu-id="99f80-117">需求</span><span class="sxs-lookup"><span data-stu-id="99f80-117">Requirement</span></span> | <span data-ttu-id="99f80-118">值</span><span class="sxs-lookup"><span data-stu-id="99f80-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99f80-119">標頭</span><span class="sxs-lookup"><span data-stu-id="99f80-119">Header</span></span><br/>  | <dl> <span data-ttu-id="99f80-120"><dt>Mtype (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="99f80-120"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="99f80-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="99f80-121">Library</span></span><br/> | <dl> <span data-ttu-id="99f80-122"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="99f80-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99f80-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="99f80-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99f80-124">**CMediaType 類別**</span><span class="sxs-lookup"><span data-stu-id="99f80-124">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




