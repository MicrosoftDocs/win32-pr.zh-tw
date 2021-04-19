---
description: 函式方法。
ms.assetid: d7550c38-d728-41b2-80a6-20728abf6012
title: 'CImageSample. CImageSample (Winutil. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageSample.CImageSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 805be59cfc899b6461fa8c761eebb5821118640f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998379"
---
# <a name="cimagesamplecimagesample-constructor"></a><span data-ttu-id="df44c-103">CImageSample. CImageSample 函數</span><span class="sxs-lookup"><span data-stu-id="df44c-103">CImageSample.CImageSample constructor</span></span>

<span data-ttu-id="df44c-104">函式方法。</span><span class="sxs-lookup"><span data-stu-id="df44c-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="df44c-105">語法</span><span class="sxs-lookup"><span data-stu-id="df44c-105">Syntax</span></span>


```C++
CImageSample(
   CBaseAllocator *pAllocator,
   TCHAR          *pName,
   HRESULT        *phr,
   LPBYTE         pBuffer,
   LONG           length
);
```



## <a name="parameters"></a><span data-ttu-id="df44c-106">參數</span><span class="sxs-lookup"><span data-stu-id="df44c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df44c-107">*pAllocator*</span><span class="sxs-lookup"><span data-stu-id="df44c-107">*pAllocator*</span></span> 
</dt> <dd>

<span data-ttu-id="df44c-108">建立此範例的配置器指標。</span><span class="sxs-lookup"><span data-stu-id="df44c-108">Pointer to the allocator that created this sample.</span></span>

</dd> <dt>

<span data-ttu-id="df44c-109">*pName*</span><span class="sxs-lookup"><span data-stu-id="df44c-109">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="df44c-110">忽略。</span><span class="sxs-lookup"><span data-stu-id="df44c-110">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="df44c-111">*phr*</span><span class="sxs-lookup"><span data-stu-id="df44c-111">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="df44c-112">忽略。</span><span class="sxs-lookup"><span data-stu-id="df44c-112">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="df44c-113">*pBuffer*</span><span class="sxs-lookup"><span data-stu-id="df44c-113">*pBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="df44c-114">由呼叫端配置的記憶體緩衝區指標，大小 *長度*。</span><span class="sxs-lookup"><span data-stu-id="df44c-114">Pointer to a memory buffer allocated by the caller, of size *length*.</span></span> <span data-ttu-id="df44c-115">緩衝區應該包含與 GDI 裝置無關的點陣圖 (DIB) 。</span><span class="sxs-lookup"><span data-stu-id="df44c-115">The buffer should contain a GDI device-independent bitmap (DIB).</span></span>

</dd> <dt>

<span data-ttu-id="df44c-116">*length* (長度)</span><span class="sxs-lookup"><span data-stu-id="df44c-116">*length*</span></span> 
</dt> <dd>

<span data-ttu-id="df44c-117">緩衝區的長度。</span><span class="sxs-lookup"><span data-stu-id="df44c-117">Length of the buffer.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="df44c-118">備註</span><span class="sxs-lookup"><span data-stu-id="df44c-118">Remarks</span></span>

<span data-ttu-id="df44c-119">[**CImageAllocator**](cimageallocator.md)類別會使用作業系統分頁檔所支援的檔案對應物件來建立 DIB。</span><span class="sxs-lookup"><span data-stu-id="df44c-119">The [**CImageAllocator**](cimageallocator.md) class creates a DIB using a file-mapping object that is backed by the operating-system paging file.</span></span> <span data-ttu-id="df44c-120">檔案對應物件的控制碼會儲存在 **m \_ DibData** 結構的 **hMapping** 成員中。</span><span class="sxs-lookup"><span data-stu-id="df44c-120">The handle to the file-mapping object is stored in the **hMapping** member of the **m\_DibData** structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="df44c-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="df44c-121">Requirements</span></span>



| <span data-ttu-id="df44c-122">需求</span><span class="sxs-lookup"><span data-stu-id="df44c-122">Requirement</span></span> | <span data-ttu-id="df44c-123">值</span><span class="sxs-lookup"><span data-stu-id="df44c-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df44c-124">標頭</span><span class="sxs-lookup"><span data-stu-id="df44c-124">Header</span></span><br/>  | <dl> <span data-ttu-id="df44c-125"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="df44c-125"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="df44c-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="df44c-126">Library</span></span><br/> | <dl> <span data-ttu-id="df44c-127"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="df44c-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df44c-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="df44c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df44c-129">**CImageSample 類別**</span><span class="sxs-lookup"><span data-stu-id="df44c-129">**CImageSample Class**</span></span>](cimagesample.md)
</dt> </dl>

 

 




