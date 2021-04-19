---
description: 抓取目前資料流程所需的最大位元組大小，不包含版本號碼。
ms.assetid: ca1a68e2-02b4-4eea-916a-e0418ae811ae
title: 'CPersistStream. SizeMax 方法 (Pstream .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.SizeMax
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: afa29e2c81cc454a9e85b9038486221f6f44aaf5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977748"
---
# <a name="cpersiststreamsizemax-method"></a><span data-ttu-id="9092c-103">CPersistStream. SizeMax 方法</span><span class="sxs-lookup"><span data-stu-id="9092c-103">CPersistStream.SizeMax method</span></span>

<span data-ttu-id="9092c-104">抓取目前資料流程所需的最大位元組大小，不包含版本號碼。</span><span class="sxs-lookup"><span data-stu-id="9092c-104">Retrieves the maximum byte size needed for the current stream, not including the version number.</span></span>

## <a name="syntax"></a><span data-ttu-id="9092c-105">語法</span><span class="sxs-lookup"><span data-stu-id="9092c-105">Syntax</span></span>


```C++
virtual int SizeMax();
```



## <a name="parameters"></a><span data-ttu-id="9092c-106">參數</span><span class="sxs-lookup"><span data-stu-id="9092c-106">Parameters</span></span>

<span data-ttu-id="9092c-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="9092c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9092c-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="9092c-108">Return value</span></span>

<span data-ttu-id="9092c-109">傳回資料所需的位元組數目，不包括版本號碼。</span><span class="sxs-lookup"><span data-stu-id="9092c-109">Returns the number of bytes needed for data, not including the version number.</span></span>

## <a name="remarks"></a><span data-ttu-id="9092c-110">備註</span><span class="sxs-lookup"><span data-stu-id="9092c-110">Remarks</span></span>

<span data-ttu-id="9092c-111">預設版本傳回零;應該覆寫它，以提供一些其他適當的值。</span><span class="sxs-lookup"><span data-stu-id="9092c-111">The default version returns zero; it should be overridden to provide some other appropriate value.</span></span>

## <a name="requirements"></a><span data-ttu-id="9092c-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="9092c-112">Requirements</span></span>



| <span data-ttu-id="9092c-113">需求</span><span class="sxs-lookup"><span data-stu-id="9092c-113">Requirement</span></span> | <span data-ttu-id="9092c-114">值</span><span class="sxs-lookup"><span data-stu-id="9092c-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9092c-115">標頭</span><span class="sxs-lookup"><span data-stu-id="9092c-115">Header</span></span><br/>  | <dl> <span data-ttu-id="9092c-116"><dt>Pstream (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="9092c-116"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9092c-117">程式庫</span><span class="sxs-lookup"><span data-stu-id="9092c-117">Library</span></span><br/> | <dl> <span data-ttu-id="9092c-118"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="9092c-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9092c-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9092c-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9092c-120">**CPersistStream 類別**</span><span class="sxs-lookup"><span data-stu-id="9092c-120">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




