---
description: IsPartiallySpecified 方法會判斷是否已部分定義媒體類型。 如果主要類型、子類型或格式類型為 GUID Null，則媒體類型為 [部分] \_ 。
ms.assetid: 26dd7a2b-b2f8-485f-a9af-31c3a9eb1def
title: 'CMediaType. IsPartiallySpecified 方法 (Mtype .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.IsPartiallySpecified
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 32c39942ab3f97d45ecf71ba841d56b7afd4be62
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983130"
---
# <a name="cmediatypeispartiallyspecified-method"></a><span data-ttu-id="0ac89-104">CMediaType. IsPartiallySpecified 方法</span><span class="sxs-lookup"><span data-stu-id="0ac89-104">CMediaType.IsPartiallySpecified method</span></span>

<span data-ttu-id="0ac89-105">`IsPartiallySpecified`方法會判斷是否已部分定義媒體類型。</span><span class="sxs-lookup"><span data-stu-id="0ac89-105">The `IsPartiallySpecified` method determines if the media type is partially defined.</span></span> <span data-ttu-id="0ac89-106">如果主要類型、子類型或格式類型為 GUID Null，則媒體類型為 [ *部分* ] \_ 。</span><span class="sxs-lookup"><span data-stu-id="0ac89-106">A media type is *partial* if the major type, subtype, or format type is GUID\_NULL.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ac89-107">語法</span><span class="sxs-lookup"><span data-stu-id="0ac89-107">Syntax</span></span>


```C++
BOOL IsPartiallySpecified() const;
```



## <a name="parameters"></a><span data-ttu-id="0ac89-108">參數</span><span class="sxs-lookup"><span data-stu-id="0ac89-108">Parameters</span></span>

<span data-ttu-id="0ac89-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="0ac89-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0ac89-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="0ac89-110">Return value</span></span>

<span data-ttu-id="0ac89-111">如果媒體類型為部分指定，則傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="0ac89-111">Returns **TRUE** if the media type is partially specified.</span></span> <span data-ttu-id="0ac89-112">否則，會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="0ac89-112">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ac89-113">備註</span><span class="sxs-lookup"><span data-stu-id="0ac89-113">Remarks</span></span>

<span data-ttu-id="0ac89-114">[**IPin：： Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect)方法可以接受部分媒體類型。</span><span class="sxs-lookup"><span data-stu-id="0ac89-114">The [**IPin::Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) method can accept partial media types.</span></span>

<span data-ttu-id="0ac89-115">其實作並不會實際測試子類型。</span><span class="sxs-lookup"><span data-stu-id="0ac89-115">The implementation does not actually test the subtype.</span></span> <span data-ttu-id="0ac89-116">如果有指定的格式類型，即使子類型為 GUID Null，也不會將媒體類型視為部分 \_ 。</span><span class="sxs-lookup"><span data-stu-id="0ac89-116">If there is a specified format type, the media type is not considered partial, even if the subtype is GUID\_NULL.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ac89-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="0ac89-117">Requirements</span></span>



| <span data-ttu-id="0ac89-118">需求</span><span class="sxs-lookup"><span data-stu-id="0ac89-118">Requirement</span></span> | <span data-ttu-id="0ac89-119">值</span><span class="sxs-lookup"><span data-stu-id="0ac89-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ac89-120">標頭</span><span class="sxs-lookup"><span data-stu-id="0ac89-120">Header</span></span><br/>  | <dl> <span data-ttu-id="0ac89-121"><dt>Mtype (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="0ac89-121"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="0ac89-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="0ac89-122">Library</span></span><br/> | <dl> <span data-ttu-id="0ac89-123"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="0ac89-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ac89-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0ac89-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ac89-125">**CMediaType 類別**</span><span class="sxs-lookup"><span data-stu-id="0ac89-125">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




