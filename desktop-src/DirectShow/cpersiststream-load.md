---
description: 從指定的資料流程載入篩選的資料。
ms.assetid: c2bfd379-2916-4698-bc41-653161723706
title: CPersistStream) Load 方法 (Pstream
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.Load
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 83b16c3fe7bf905d1ade6b7f38cf27c61b44e4d6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993372"
---
# <a name="cpersiststreamload-method"></a><span data-ttu-id="70316-103">CPersistStream Load 方法</span><span class="sxs-lookup"><span data-stu-id="70316-103">CPersistStream.Load method</span></span>

<span data-ttu-id="70316-104">從指定的資料流程載入篩選的資料。</span><span class="sxs-lookup"><span data-stu-id="70316-104">Loads the filter's data from a given stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="70316-105">語法</span><span class="sxs-lookup"><span data-stu-id="70316-105">Syntax</span></span>


```C++
HRESULT Load(
   LPSTREAM pStm
);
```



## <a name="parameters"></a><span data-ttu-id="70316-106">參數</span><span class="sxs-lookup"><span data-stu-id="70316-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70316-107">*pStm*</span><span class="sxs-lookup"><span data-stu-id="70316-107">*pStm*</span></span> 
</dt> <dd>

<span data-ttu-id="70316-108">要載入之資料流程的指標。</span><span class="sxs-lookup"><span data-stu-id="70316-108">Pointer to the stream from which to be loaded.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70316-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="70316-109">Return value</span></span>

<span data-ttu-id="70316-110">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="70316-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="70316-111">備註</span><span class="sxs-lookup"><span data-stu-id="70316-111">Remarks</span></span>

<span data-ttu-id="70316-112">此成員函式會實行 **IPersistStream：： Load** 方法。</span><span class="sxs-lookup"><span data-stu-id="70316-112">This member function implements the **IPersistStream::Load** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="70316-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="70316-113">Requirements</span></span>



| <span data-ttu-id="70316-114">需求</span><span class="sxs-lookup"><span data-stu-id="70316-114">Requirement</span></span> | <span data-ttu-id="70316-115">值</span><span class="sxs-lookup"><span data-stu-id="70316-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70316-116">標頭</span><span class="sxs-lookup"><span data-stu-id="70316-116">Header</span></span><br/>  | <dl> <span data-ttu-id="70316-117"><dt>Pstream (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="70316-117"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="70316-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="70316-118">Library</span></span><br/> | <dl> <span data-ttu-id="70316-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="70316-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70316-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="70316-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70316-121">**CPersistStream 類別**</span><span class="sxs-lookup"><span data-stu-id="70316-121">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




