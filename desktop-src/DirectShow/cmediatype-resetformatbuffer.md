---
description: ResetFormatBuffer 方法會刪除格式區塊。 方法會將 AM 媒體類型結構的 cbFormat 和 pbFormat 成員設定 \_ \_ 為 Null。
ms.assetid: 5eb6dfc8-cfba-41dd-b422-8fe93ca904c1
title: 'CMediaType. ResetFormatBuffer 方法 (Mtype .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.ResetFormatBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 25047060b956e2374964c1620c010dbdf458307c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987017"
---
# <a name="cmediatyperesetformatbuffer-method"></a><span data-ttu-id="2f638-104">CMediaType. ResetFormatBuffer 方法</span><span class="sxs-lookup"><span data-stu-id="2f638-104">CMediaType.ResetFormatBuffer method</span></span>

<span data-ttu-id="2f638-105">`ResetFormatBuffer`方法會刪除格式區塊。</span><span class="sxs-lookup"><span data-stu-id="2f638-105">The `ResetFormatBuffer` method deletes the format block.</span></span> <span data-ttu-id="2f638-106">方法會將 **AM \_ 媒體 \_ 類型** 結構的 **cbFormat** 和 **pbFormat** 成員設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="2f638-106">The method sets the **cbFormat** and **pbFormat** members of the **AM\_MEDIA\_TYPE** structure to **NULL**.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f638-107">語法</span><span class="sxs-lookup"><span data-stu-id="2f638-107">Syntax</span></span>


```C++
void ResetFormatBuffer();
```



## <a name="parameters"></a><span data-ttu-id="2f638-108">參數</span><span class="sxs-lookup"><span data-stu-id="2f638-108">Parameters</span></span>

<span data-ttu-id="2f638-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="2f638-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2f638-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="2f638-110">Return value</span></span>

<span data-ttu-id="2f638-111">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="2f638-111">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f638-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="2f638-112">Requirements</span></span>



| <span data-ttu-id="2f638-113">需求</span><span class="sxs-lookup"><span data-stu-id="2f638-113">Requirement</span></span> | <span data-ttu-id="2f638-114">值</span><span class="sxs-lookup"><span data-stu-id="2f638-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f638-115">標頭</span><span class="sxs-lookup"><span data-stu-id="2f638-115">Header</span></span><br/>  | <dl> <span data-ttu-id="2f638-116"><dt>Mtype (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="2f638-116"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="2f638-117">程式庫</span><span class="sxs-lookup"><span data-stu-id="2f638-117">Library</span></span><br/> | <dl> <span data-ttu-id="2f638-118"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="2f638-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f638-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2f638-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f638-120">**CMediaType 類別**</span><span class="sxs-lookup"><span data-stu-id="2f638-120">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




