---
description: CreateDIB 方法會在 DIB)  (建立與 GDI 裝置無關的點陣圖。 DIB 是在共用的 mempory 區塊中配置，可在擁有篩選器 blits 影像時排除複製作業。
ms.assetid: 8a9ab1cf-4104-48e9-ba6c-28d0f1a1d226
title: 'CImageAllocator. CreateDIB 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.CreateDIB
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 316b7aeadfa442a8df4e80075380464758f3c6bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989674"
---
# <a name="cimageallocatorcreatedib-method"></a><span data-ttu-id="4bcfe-104">CImageAllocator. CreateDIB 方法</span><span class="sxs-lookup"><span data-stu-id="4bcfe-104">CImageAllocator.CreateDIB method</span></span>

<span data-ttu-id="4bcfe-105">`CreateDIB`方法會建立與 GDI 裝置無關的點陣圖 (DIB) 。</span><span class="sxs-lookup"><span data-stu-id="4bcfe-105">The `CreateDIB` method creates a GDI device-independent bitmap (DIB).</span></span> <span data-ttu-id="4bcfe-106">DIB 是在共用的 mempory 區塊中配置，可在擁有篩選器 blits 影像時排除複製作業。</span><span class="sxs-lookup"><span data-stu-id="4bcfe-106">The DIB is allocated in a shared mempory block, which eliminates a copy operation when the owning filter blits the image.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bcfe-107">語法</span><span class="sxs-lookup"><span data-stu-id="4bcfe-107">Syntax</span></span>


```C++
HRESULT CreateDIB(
        LONG    InSize,
  [ref] DIBDATA &DibData
);
```



## <a name="parameters"></a><span data-ttu-id="4bcfe-108">參數</span><span class="sxs-lookup"><span data-stu-id="4bcfe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4bcfe-109">*InSize*</span><span class="sxs-lookup"><span data-stu-id="4bcfe-109">*InSize*</span></span> 
</dt> <dd>

<span data-ttu-id="4bcfe-110">點陣圖的大小。</span><span class="sxs-lookup"><span data-stu-id="4bcfe-110">Size of the bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="4bcfe-111">*DibData* \[裁判\]</span><span class="sxs-lookup"><span data-stu-id="4bcfe-111">*DibData* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="4bcfe-112">[**DIBDATA**](dibdata.md)結構的參考。</span><span class="sxs-lookup"><span data-stu-id="4bcfe-112">Reference to a [**DIBDATA**](dibdata.md) structure.</span></span> <span data-ttu-id="4bcfe-113">方法會在此結構中填入 DIB 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="4bcfe-113">The method fills in this structure with information about the DIB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4bcfe-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="4bcfe-114">Return value</span></span>

<span data-ttu-id="4bcfe-115">\_如果成功，則傳回，否則傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="4bcfe-115">Returns S\_OK if successful, or an error code otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="4bcfe-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="4bcfe-116">Requirements</span></span>



| <span data-ttu-id="4bcfe-117">需求</span><span class="sxs-lookup"><span data-stu-id="4bcfe-117">Requirement</span></span> | <span data-ttu-id="4bcfe-118">值</span><span class="sxs-lookup"><span data-stu-id="4bcfe-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4bcfe-119">標頭</span><span class="sxs-lookup"><span data-stu-id="4bcfe-119">Header</span></span><br/>  | <dl> <span data-ttu-id="4bcfe-120"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="4bcfe-120"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4bcfe-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="4bcfe-121">Library</span></span><br/> | <dl> <span data-ttu-id="4bcfe-122"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="4bcfe-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4bcfe-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4bcfe-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bcfe-124">**CImageAllocator 類別**</span><span class="sxs-lookup"><span data-stu-id="4bcfe-124">**CImageAllocator Class**</span></span>](cimageallocator.md)
</dt> <dt>

[<span data-ttu-id="4bcfe-125">**CImageAllocator：：配置**</span><span class="sxs-lookup"><span data-stu-id="4bcfe-125">**CImageAllocator::Alloc**</span></span>](cimageallocator-alloc.md)
</dt> </dl>

 

 




