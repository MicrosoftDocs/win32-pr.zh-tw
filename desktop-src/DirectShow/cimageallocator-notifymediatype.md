---
description: NotifyMediaType 方法會通知物件目前的媒體類型。
ms.assetid: 6fb708ff-e968-4867-baca-ebe2515c9fab
title: 'CImageAllocator. NotifyMediaType 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.NotifyMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cb9261884b8940b571876502741fcc52e1c40a33
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001138"
---
# <a name="cimageallocatornotifymediatype-method"></a><span data-ttu-id="2b119-103">CImageAllocator. NotifyMediaType 方法</span><span class="sxs-lookup"><span data-stu-id="2b119-103">CImageAllocator.NotifyMediaType method</span></span>

<span data-ttu-id="2b119-104">`NotifyMediaType`方法會通知目前媒體類型的物件。</span><span class="sxs-lookup"><span data-stu-id="2b119-104">The `NotifyMediaType` method informs the object of the current media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b119-105">語法</span><span class="sxs-lookup"><span data-stu-id="2b119-105">Syntax</span></span>


```C++
void NotifyMediaType(
   CMediaType *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="2b119-106">參數</span><span class="sxs-lookup"><span data-stu-id="2b119-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b119-107">*pMediaType*</span><span class="sxs-lookup"><span data-stu-id="2b119-107">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="2b119-108">[**CMediaType**](cmediatype.md)物件的指標，或為 **Null** 以清除媒體類型。</span><span class="sxs-lookup"><span data-stu-id="2b119-108">Pointer to a [**CMediaType**](cmediatype.md) object, or **NULL** to clear the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b119-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="2b119-109">Return value</span></span>

<span data-ttu-id="2b119-110">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="2b119-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b119-111">備註</span><span class="sxs-lookup"><span data-stu-id="2b119-111">Remarks</span></span>

<span data-ttu-id="2b119-112">當媒體類型變更時，擁有篩選應呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="2b119-112">The owning filter should call this method whenever the media type changes.</span></span> <span data-ttu-id="2b119-113">一般來說，當 pin 首次連接，以及動態格式變更之後，就會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="2b119-113">Typically this occurs when the pin first connects, and after a dynamic format change.</span></span> <span data-ttu-id="2b119-114">配置器會使用媒體類型來驗證建議的配置器屬性，也會在建立媒體範例時使用。</span><span class="sxs-lookup"><span data-stu-id="2b119-114">The allocator uses the media type to validate proposed allocator properties, and also when it creates media samples.</span></span>

<span data-ttu-id="2b119-115">**CImageAllocator** 物件會將 *pMediaType* 指標儲存在 **m \_ pMediaType** 成員變數中。</span><span class="sxs-lookup"><span data-stu-id="2b119-115">The **CImageAllocator** object stores the *pMediaType* pointer in the **m\_pMediaType** member variable.</span></span> <span data-ttu-id="2b119-116">因此，如果呼叫端需要釋放 **CMediaType** 物件，則應該再次呼叫這個方法來更新配置器，方法是使用新的指標或 **Null** 值。</span><span class="sxs-lookup"><span data-stu-id="2b119-116">Therefore, if the caller needs to release the **CMediaType** object, it should update the allocator by calling this method again, either with a new pointer or with a **NULL** value.</span></span> <span data-ttu-id="2b119-117">否則，當配置器嘗試參考舊指標時，就會發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="2b119-117">Otherwise, an error can occur when the allocator attempts to reference the old pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b119-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="2b119-118">Requirements</span></span>



| <span data-ttu-id="2b119-119">需求</span><span class="sxs-lookup"><span data-stu-id="2b119-119">Requirement</span></span> | <span data-ttu-id="2b119-120">值</span><span class="sxs-lookup"><span data-stu-id="2b119-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b119-121">標頭</span><span class="sxs-lookup"><span data-stu-id="2b119-121">Header</span></span><br/>  | <dl> <span data-ttu-id="2b119-122"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="2b119-122"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2b119-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="2b119-123">Library</span></span><br/> | <dl> <span data-ttu-id="2b119-124"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="2b119-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b119-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2b119-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b119-126">**CImageAllocator 類別**</span><span class="sxs-lookup"><span data-stu-id="2b119-126">**CImageAllocator Class**</span></span>](cimageallocator.md)
</dt> </dl>

 

 




