---
description: GetPointer 方法會擷取緩衝區的讀取/寫入指標。 這個方法會實 IMediaSample：： GetPointer 方法。
ms.assetid: dd797ad5-6066-4366-a56f-621132f2e6ea
title: 'CMediaSample. GetPointer 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetPointer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fe8d8785bd52fbe601d9980f8fc146a2c6f41e40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992566"
---
# <a name="cmediasamplegetpointer-method"></a><span data-ttu-id="e257f-104">CMediaSample. GetPointer 方法</span><span class="sxs-lookup"><span data-stu-id="e257f-104">CMediaSample.GetPointer method</span></span>

<span data-ttu-id="e257f-105">`GetPointer`方法會擷取緩衝區的讀取/寫入指標。</span><span class="sxs-lookup"><span data-stu-id="e257f-105">The `GetPointer` method retrieves a read/write pointer to the buffer.</span></span> <span data-ttu-id="e257f-106">這個方法會實 [**IMediaSample：： GetPointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) 方法。</span><span class="sxs-lookup"><span data-stu-id="e257f-106">This method implements the [**IMediaSample::GetPointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e257f-107">語法</span><span class="sxs-lookup"><span data-stu-id="e257f-107">Syntax</span></span>


```C++
HRESULT GetPointer(
   BYTE **ppBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="e257f-108">參數</span><span class="sxs-lookup"><span data-stu-id="e257f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e257f-109">*ppBuffer*</span><span class="sxs-lookup"><span data-stu-id="e257f-109">*ppBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="e257f-110">接收緩衝區指標之變數的位址。</span><span class="sxs-lookup"><span data-stu-id="e257f-110">Address of a variable that receives a pointer to the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e257f-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="e257f-111">Return value</span></span>

<span data-ttu-id="e257f-112">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="e257f-112">Returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="e257f-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="e257f-113">Requirements</span></span>



| <span data-ttu-id="e257f-114">需求</span><span class="sxs-lookup"><span data-stu-id="e257f-114">Requirement</span></span> | <span data-ttu-id="e257f-115">值</span><span class="sxs-lookup"><span data-stu-id="e257f-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e257f-116">標頭</span><span class="sxs-lookup"><span data-stu-id="e257f-116">Header</span></span><br/>  | <dl> <span data-ttu-id="e257f-117"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="e257f-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e257f-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="e257f-118">Library</span></span><br/> | <dl> <span data-ttu-id="e257f-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="e257f-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e257f-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e257f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e257f-121">**CMediaSample 類別**</span><span class="sxs-lookup"><span data-stu-id="e257f-121">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




