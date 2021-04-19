---
description: NotifyMediaType 方法會通知目前媒體類型的 CDrawImage 物件。
ms.assetid: 419d516f-4b96-47aa-80cc-ac785e65af8b
title: 'CDrawImage. NotifyMediaType 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.NotifyMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3e3af4d926bd0ca8db5ef11839dd0ca84523c374
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991180"
---
# <a name="cdrawimagenotifymediatype-method"></a><span data-ttu-id="9ee6b-103">CDrawImage. NotifyMediaType 方法</span><span class="sxs-lookup"><span data-stu-id="9ee6b-103">CDrawImage.NotifyMediaType method</span></span>

<span data-ttu-id="9ee6b-104">`NotifyMediaType`方法會通知目前媒體類型的 **CDrawImage** 物件。</span><span class="sxs-lookup"><span data-stu-id="9ee6b-104">The `NotifyMediaType` method notifies the **CDrawImage** object of the current media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ee6b-105">語法</span><span class="sxs-lookup"><span data-stu-id="9ee6b-105">Syntax</span></span>


```C++
void NotifyMediaType(
   CMediaType *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="9ee6b-106">參數</span><span class="sxs-lookup"><span data-stu-id="9ee6b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ee6b-107">*pMediaType*</span><span class="sxs-lookup"><span data-stu-id="9ee6b-107">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="9ee6b-108">[**CMediaType**](cmediatype.md)物件的指標，或為 **Null** 以清除媒體類型。</span><span class="sxs-lookup"><span data-stu-id="9ee6b-108">Pointer to a [**CMediaType**](cmediatype.md) object, or **NULL** to clear the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ee6b-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="9ee6b-109">Return value</span></span>

<span data-ttu-id="9ee6b-110">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="9ee6b-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ee6b-111">備註</span><span class="sxs-lookup"><span data-stu-id="9ee6b-111">Remarks</span></span>

<span data-ttu-id="9ee6b-112">當媒體類型變更時，擁有篩選應呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="9ee6b-112">The owning filter should call this method whenever the media type changes.</span></span> <span data-ttu-id="9ee6b-113">一般來說，當 pin 首次連接，以及動態格式變更之後，就會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="9ee6b-113">Typically this occurs when the pin first connects, and after a dynamic format change.</span></span>

<span data-ttu-id="9ee6b-114">**CDrawImage** 物件會將 *pMediaType* 指標儲存在 **m \_ pMediaType** 成員變數中。</span><span class="sxs-lookup"><span data-stu-id="9ee6b-114">The **CDrawImage** object stores the *pMediaType* pointer in the **m\_pMediaType** member variable.</span></span> <span data-ttu-id="9ee6b-115">因此，如果呼叫端需要釋放 **CMediaType** 物件，則應該再次呼叫這個方法來更新 **CDrawImage** 物件，其方式是使用新的指標或 **Null** 值。</span><span class="sxs-lookup"><span data-stu-id="9ee6b-115">Therefore, if the caller needs to release the **CMediaType** object, it should update the **CDrawImage** object by calling this method again, either with a new pointer or with a **NULL** value.</span></span> <span data-ttu-id="9ee6b-116">否則，當 **CDrawImage** 物件嘗試參考舊指標時，就會發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="9ee6b-116">Otherwise, an error can occur when the **CDrawImage** object attempts to reference the old pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ee6b-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="9ee6b-117">Requirements</span></span>



| <span data-ttu-id="9ee6b-118">需求</span><span class="sxs-lookup"><span data-stu-id="9ee6b-118">Requirement</span></span> | <span data-ttu-id="9ee6b-119">值</span><span class="sxs-lookup"><span data-stu-id="9ee6b-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ee6b-120">標頭</span><span class="sxs-lookup"><span data-stu-id="9ee6b-120">Header</span></span><br/>  | <dl> <span data-ttu-id="9ee6b-121"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="9ee6b-121"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9ee6b-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="9ee6b-122">Library</span></span><br/> | <dl> <span data-ttu-id="9ee6b-123"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="9ee6b-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ee6b-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9ee6b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ee6b-125">**CDrawImage 類別**</span><span class="sxs-lookup"><span data-stu-id="9ee6b-125">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




