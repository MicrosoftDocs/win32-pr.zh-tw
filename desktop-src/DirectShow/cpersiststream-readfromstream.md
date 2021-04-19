---
description: 從指定的資料流程讀取篩選的資料。
ms.assetid: 009f4812-8cc6-436a-9553-3a3161d5e992
title: 'CPersistStream. ReadFromStream 方法 (Pstream .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.ReadFromStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ce6c037fbce9fbaeabf7491b1b840000f67e25d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985568"
---
# <a name="cpersiststreamreadfromstream-method"></a><span data-ttu-id="d959d-103">CPersistStream. ReadFromStream 方法</span><span class="sxs-lookup"><span data-stu-id="d959d-103">CPersistStream.ReadFromStream method</span></span>

<span data-ttu-id="d959d-104">從指定的資料流程讀取篩選的資料。</span><span class="sxs-lookup"><span data-stu-id="d959d-104">Reads the filter's data from the given stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="d959d-105">語法</span><span class="sxs-lookup"><span data-stu-id="d959d-105">Syntax</span></span>


```C++
virtual HRESULT ReadFromStream(
   IStream *pStream
);
```



## <a name="parameters"></a><span data-ttu-id="d959d-106">參數</span><span class="sxs-lookup"><span data-stu-id="d959d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d959d-107">*pStream*</span><span class="sxs-lookup"><span data-stu-id="d959d-107">*pStream*</span></span> 
</dt> <dd>

<span data-ttu-id="d959d-108">要從中讀取資料的 **IStream** 介面指標。</span><span class="sxs-lookup"><span data-stu-id="d959d-108">Pointer to an **IStream** interface from which data is to be read.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d959d-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="d959d-109">Return value</span></span>

<span data-ttu-id="d959d-110">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="d959d-110">Returns S\_OK.</span></span> <span data-ttu-id="d959d-111">衍生類別應該會傳回有效的 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="d959d-111">The derived class should return a valid **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d959d-112">備註</span><span class="sxs-lookup"><span data-stu-id="d959d-112">Remarks</span></span>

<span data-ttu-id="d959d-113">預設版本不會讀取任何內容;您可以覆寫它來讀取您類別的特定資料。</span><span class="sxs-lookup"><span data-stu-id="d959d-113">The default version reads nothing; it can be overridden to read data specific to your class.</span></span>

## <a name="requirements"></a><span data-ttu-id="d959d-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="d959d-114">Requirements</span></span>



| <span data-ttu-id="d959d-115">需求</span><span class="sxs-lookup"><span data-stu-id="d959d-115">Requirement</span></span> | <span data-ttu-id="d959d-116">值</span><span class="sxs-lookup"><span data-stu-id="d959d-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d959d-117">標頭</span><span class="sxs-lookup"><span data-stu-id="d959d-117">Header</span></span><br/>  | <dl> <span data-ttu-id="d959d-118"><dt>Pstream (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="d959d-118"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d959d-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="d959d-119">Library</span></span><br/> | <dl> <span data-ttu-id="d959d-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="d959d-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d959d-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d959d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d959d-122">**CPersistStream 類別**</span><span class="sxs-lookup"><span data-stu-id="d959d-122">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




