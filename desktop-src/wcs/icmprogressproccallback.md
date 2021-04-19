---
title: ICMProgressProcCallback 回呼函式
description: ICMProgressProcCallback 函式是由應用程式提供的回呼函式，它會報告進度，並允許應用程式取消色彩處理。
ms.assetid: 4e0bfa4c-f0eb-4776-98d6-90d9adf71bee
keywords:
- ICMProgressProcCallback 回呼函式 Windows 色彩系統
topic_type:
- apiref
api_name:
- ICMProgressProcCallback
api_location:
- Icm.h
api_type:
- UserDefined
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8acf790a135a41e4eabb4a67c2498f1ed914c4c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106988646"
---
# <a name="icmprogressproccallback-callback-function"></a><span data-ttu-id="9745d-104">ICMProgressProcCallback 回呼函式</span><span class="sxs-lookup"><span data-stu-id="9745d-104">ICMProgressProcCallback callback function</span></span>

<span data-ttu-id="9745d-105">**ICMProgressProcCallback** 函式是由應用程式提供的回呼函式，它會報告進度，並允許應用程式取消色彩處理。</span><span class="sxs-lookup"><span data-stu-id="9745d-105">The **ICMProgressProcCallback** function is an application-supplied callback function that reports progress and permits the application to cancel color processing.</span></span>

## <a name="syntax"></a><span data-ttu-id="9745d-106">語法</span><span class="sxs-lookup"><span data-stu-id="9745d-106">Syntax</span></span>


```C++
BOOL WINAPI ICMProgressProcCallback(
   ULONG  ulMax,
   ULONG  ulCurrent,
   LPARAM ulCallbackData
);
```



## <a name="parameters"></a><span data-ttu-id="9745d-107">參數</span><span class="sxs-lookup"><span data-stu-id="9745d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9745d-108">*ulMax*</span><span class="sxs-lookup"><span data-stu-id="9745d-108">*ulMax*</span></span> 
</dt> <dd>

<span data-ttu-id="9745d-109">指定進度計數器的最大值 (用來預估點陣圖處理) 的完成。</span><span class="sxs-lookup"><span data-stu-id="9745d-109">Specifies the maximum value of the progress counter (used to estimate completion of the bitmap processing).</span></span>

</dd> <dt>

<span data-ttu-id="9745d-110">*ulCurrent*</span><span class="sxs-lookup"><span data-stu-id="9745d-110">*ulCurrent*</span></span> 
</dt> <dd>

<span data-ttu-id="9745d-111">指定進度計數器的目前值除以最大值時 (，提供完成) 百分比的粗略估計。</span><span class="sxs-lookup"><span data-stu-id="9745d-111">Specifies the current value of the progress counter (when divided by the maximum value, provides a rough estimate of percentage of completion).</span></span>

</dd> <dt>

<span data-ttu-id="9745d-112">*ulCallbackData*</span><span class="sxs-lookup"><span data-stu-id="9745d-112">*ulCallbackData*</span></span> 
</dt> <dd>

<span data-ttu-id="9745d-113">指定應用程式傳遞至 ICM2 函式的資料，然後將其傳遞至回呼函數。</span><span class="sxs-lookup"><span data-stu-id="9745d-113">Specifies the data which is passed by the application to an ICM2 function, which then passes it on to the callback function.</span></span> <span data-ttu-id="9745d-114">例如，您可以使用這類資料來識別要報告進度的點陣圖和處理常式。</span><span class="sxs-lookup"><span data-stu-id="9745d-114">Such data can be used, for example, to identify the bitmap and process about which progress is being reported.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9745d-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="9745d-115">Return value</span></span>

<span data-ttu-id="9745d-116">此函數會傳回 **TRUE** 以繼續點陣圖處理。</span><span class="sxs-lookup"><span data-stu-id="9745d-116">This function returns **TRUE** to continue bitmap processing.</span></span> <span data-ttu-id="9745d-117">傳回值為 **FALSE** ，表示取消處理。</span><span class="sxs-lookup"><span data-stu-id="9745d-117">The return value is **FALSE** to cancel processing.</span></span> <span data-ttu-id="9745d-118">如果取消處理，呼叫的函式會傳回零以表示失敗，雖然可能會部分填滿其輸出緩衝區。</span><span class="sxs-lookup"><span data-stu-id="9745d-118">If processing is canceled, the calling function returns zero to indicate failure, although its output buffer may be partially filled.</span></span>

## <a name="remarks"></a><span data-ttu-id="9745d-119">備註</span><span class="sxs-lookup"><span data-stu-id="9745d-119">Remarks</span></span>

<span data-ttu-id="9745d-120">這個回呼函式的名稱是由應用程式所提供。</span><span class="sxs-lookup"><span data-stu-id="9745d-120">The name of this callback function is supplied by the application.</span></span> <span data-ttu-id="9745d-121">許多 WCS 函式（包括 [**TranslateBitmapBits**](/windows/win32/api/icm/nf-icm-translatebitmapbits) 和 [**CheckBitmapBits**](/windows/win32/api/icm/nf-icm-checkbitmapbits)）會定期呼叫此函數。</span><span class="sxs-lookup"><span data-stu-id="9745d-121">A number of WCS functions, including [**TranslateBitmapBits**](/windows/win32/api/icm/nf-icm-translatebitmapbits) and [**CheckBitmapBits**](/windows/win32/api/icm/nf-icm-checkbitmapbits), call this function periodically.</span></span>

## <a name="requirements"></a><span data-ttu-id="9745d-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="9745d-122">Requirements</span></span>



| <span data-ttu-id="9745d-123">需求</span><span class="sxs-lookup"><span data-stu-id="9745d-123">Requirement</span></span> | <span data-ttu-id="9745d-124">值</span><span class="sxs-lookup"><span data-stu-id="9745d-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="9745d-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9745d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="9745d-126">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9745d-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="9745d-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9745d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="9745d-128">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9745d-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="9745d-129">標頭</span><span class="sxs-lookup"><span data-stu-id="9745d-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="9745d-130"><dt>Icm。h</dt></span><span class="sxs-lookup"><span data-stu-id="9745d-130"><dt>Icm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9745d-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9745d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9745d-132">基本色彩管理概念</span><span class="sxs-lookup"><span data-stu-id="9745d-132">Basic color management concepts</span></span>](basic-color-management-concepts.md)
</dt> <dt>

[<span data-ttu-id="9745d-133">函數</span><span class="sxs-lookup"><span data-stu-id="9745d-133">Functions</span></span>](functions.md)
</dt> <dt>

[<span data-ttu-id="9745d-134">**TranslateBitmapBits**</span><span class="sxs-lookup"><span data-stu-id="9745d-134">**TranslateBitmapBits**</span></span>](/windows/win32/api/icm/nf-icm-translatebitmapbits)
</dt> <dt>

[<span data-ttu-id="9745d-135">**CheckBitmapBits**</span><span class="sxs-lookup"><span data-stu-id="9745d-135">**CheckBitmapBits**</span></span>](/windows/win32/api/icm/nf-icm-checkbitmapbits)
</dt> </dl>
