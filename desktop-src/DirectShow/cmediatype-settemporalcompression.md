---
description: SetTemporalCompression 方法會指定是否使用時態 (幀) 壓縮來壓縮範例。
ms.assetid: cdd181ee-d1e9-48b0-96f6-e76db9f3f933
title: 'CMediaType. SetTemporalCompression 方法 (Mtype .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetTemporalCompression
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a0aba07375c5b5c760c432de704562efb2bea148
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997698"
---
# <a name="cmediatypesettemporalcompression-method"></a><span data-ttu-id="a1e6b-103">CMediaType. SetTemporalCompression 方法</span><span class="sxs-lookup"><span data-stu-id="a1e6b-103">CMediaType.SetTemporalCompression method</span></span>

<span data-ttu-id="a1e6b-104">`SetTemporalCompression`方法會指定是否使用時態性 (幀) 壓縮來壓縮範例。</span><span class="sxs-lookup"><span data-stu-id="a1e6b-104">The `SetTemporalCompression` method specifies whether samples are compressed using temporal (interframe) compression.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1e6b-105">語法</span><span class="sxs-lookup"><span data-stu-id="a1e6b-105">Syntax</span></span>


```C++
void SetTemporalCompression(
   BOOL bCompressed
);
```



## <a name="parameters"></a><span data-ttu-id="a1e6b-106">參數</span><span class="sxs-lookup"><span data-stu-id="a1e6b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1e6b-107">*bCompressed*</span><span class="sxs-lookup"><span data-stu-id="a1e6b-107">*bCompressed*</span></span> 
</dt> <dd>

<span data-ttu-id="a1e6b-108">指定資料流程是否使用時態性壓縮的布林值。</span><span class="sxs-lookup"><span data-stu-id="a1e6b-108">Boolean value that specifies whether the stream uses temporal compression.</span></span> <span data-ttu-id="a1e6b-109">如果資料流程使用時態性壓縮，請將值設定為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="a1e6b-109">If the stream uses temporal compression, set the value to **TRUE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1e6b-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="a1e6b-110">Return value</span></span>

<span data-ttu-id="a1e6b-111">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="a1e6b-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1e6b-112">備註</span><span class="sxs-lookup"><span data-stu-id="a1e6b-112">Remarks</span></span>

<span data-ttu-id="a1e6b-113">這個方法會設定 **bTemporalCompression** 成員。</span><span class="sxs-lookup"><span data-stu-id="a1e6b-113">This method sets the **bTemporalCompression** member.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1e6b-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="a1e6b-114">Requirements</span></span>



| <span data-ttu-id="a1e6b-115">需求</span><span class="sxs-lookup"><span data-stu-id="a1e6b-115">Requirement</span></span> | <span data-ttu-id="a1e6b-116">值</span><span class="sxs-lookup"><span data-stu-id="a1e6b-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1e6b-117">標頭</span><span class="sxs-lookup"><span data-stu-id="a1e6b-117">Header</span></span><br/>  | <dl> <span data-ttu-id="a1e6b-118"><dt>Mtype (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="a1e6b-118"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="a1e6b-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="a1e6b-119">Library</span></span><br/> | <dl> <span data-ttu-id="a1e6b-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="a1e6b-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1e6b-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a1e6b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1e6b-122">**CMediaType 類別**</span><span class="sxs-lookup"><span data-stu-id="a1e6b-122">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




