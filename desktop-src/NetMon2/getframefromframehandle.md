---
description: GetFrameFromFrameHandle 函式會從框架控制碼傳回框架的指標。
ms.assetid: 790fe5fe-a857-4947-a471-d0538c0f0d61
title: 'GetFrameFromFrameHandle 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameFromFrameHandle
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: ce8151b2f4c81c61dea5969ff52e9ddf2d6615a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973219"
---
# <a name="getframefromframehandle-function"></a><span data-ttu-id="ede7c-103">GetFrameFromFrameHandle 函式</span><span class="sxs-lookup"><span data-stu-id="ede7c-103">GetFrameFromFrameHandle function</span></span>

<span data-ttu-id="ede7c-104">**GetFrameFromFrameHandle** 函式會從框架控制碼傳回框架的指標。</span><span class="sxs-lookup"><span data-stu-id="ede7c-104">The **GetFrameFromFrameHandle** function returns a pointer to a frame from a frame handle.</span></span>

## <a name="syntax"></a><span data-ttu-id="ede7c-105">語法</span><span class="sxs-lookup"><span data-stu-id="ede7c-105">Syntax</span></span>


```C++
ULPFRAME WINAPI GetFrameFromFrameHandle(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a><span data-ttu-id="ede7c-106">參數</span><span class="sxs-lookup"><span data-stu-id="ede7c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ede7c-107">*hFrame* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ede7c-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ede7c-108">框架的控制碼。</span><span class="sxs-lookup"><span data-stu-id="ede7c-108">Handle to the frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ede7c-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="ede7c-109">Return value</span></span>

<span data-ttu-id="ede7c-110">如果函式成功，則傳回值為框架的指標。</span><span class="sxs-lookup"><span data-stu-id="ede7c-110">If the function is successful, the return value is a pointer to the frame.</span></span>

<span data-ttu-id="ede7c-111">如果函式不成功，則傳回值為0。</span><span class="sxs-lookup"><span data-stu-id="ede7c-111">If the function is unsuccessful, the return value is 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="ede7c-112">備註</span><span class="sxs-lookup"><span data-stu-id="ede7c-112">Remarks</span></span>

<span data-ttu-id="ede7c-113">**GetFrameFromFrameHandle** 函式會抓取網路監視器提供的其他 helper 函數無法取出的資料。</span><span class="sxs-lookup"><span data-stu-id="ede7c-113">The **GetFrameFromFrameHandle** function retrieves data that cannot be retrieved by the other helper functions that Network Monitor provides.</span></span> <span data-ttu-id="ede7c-114">盡可能使用下列功能。</span><span class="sxs-lookup"><span data-stu-id="ede7c-114">Use the following functions whenever possible.</span></span>

<dl>

[<span data-ttu-id="ede7c-115">**GetFrameDstAddressOffset**</span><span class="sxs-lookup"><span data-stu-id="ede7c-115">**GetFrameDstAddressOffset**</span></span>](getframedstaddressoffset.md)  
[<span data-ttu-id="ede7c-116">**GetFrameSrcAddressOffset**</span><span class="sxs-lookup"><span data-stu-id="ede7c-116">**GetFrameSrcAddressOffset**</span></span>](getframesrcaddressoffset.md)  
[<span data-ttu-id="ede7c-117">**GetFrameCaptureHandle**</span><span class="sxs-lookup"><span data-stu-id="ede7c-117">**GetFrameCaptureHandle**</span></span>](getframecapturehandle.md)  
[<span data-ttu-id="ede7c-118">**GetFrameDestAddress**</span><span class="sxs-lookup"><span data-stu-id="ede7c-118">**GetFrameDestAddress**</span></span>](getframedestaddress.md)  
[<span data-ttu-id="ede7c-119">**GetFrameSourceAddress**</span><span class="sxs-lookup"><span data-stu-id="ede7c-119">**GetFrameSourceAddress**</span></span>](getframesourceaddress.md)  
[<span data-ttu-id="ede7c-120">**GetFrameMacHeaderLength**</span><span class="sxs-lookup"><span data-stu-id="ede7c-120">**GetFrameMacHeaderLength**</span></span>](getframemacheaderlength.md)  
[<span data-ttu-id="ede7c-121">**GetFrameLength**</span><span class="sxs-lookup"><span data-stu-id="ede7c-121">**GetFrameLength**</span></span>](getframelength.md)  
[<span data-ttu-id="ede7c-122">**GetFrameStoredLength**</span><span class="sxs-lookup"><span data-stu-id="ede7c-122">**GetFrameStoredLength**</span></span>](getframestoredlength.md)  
[<span data-ttu-id="ede7c-123">**GetFrameMacType**</span><span class="sxs-lookup"><span data-stu-id="ede7c-123">**GetFrameMacType**</span></span>](getframemactype.md)  
[<span data-ttu-id="ede7c-124">**GetFrameNumber**</span><span class="sxs-lookup"><span data-stu-id="ede7c-124">**GetFrameNumber**</span></span>](getframenumber.md)  
[<span data-ttu-id="ede7c-125">**GetFrameTimeStamp**</span><span class="sxs-lookup"><span data-stu-id="ede7c-125">**GetFrameTimeStamp**</span></span>](getframetimestamp.md)  
</dl>

<span data-ttu-id="ede7c-126">[*專家*](e.md) 和 [*剖析*](p.md) 器可以呼叫 **GetFrameFromFrameHandle** 函數。</span><span class="sxs-lookup"><span data-stu-id="ede7c-126">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetFrameFromFrameHandle** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="ede7c-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="ede7c-127">Requirements</span></span>



| <span data-ttu-id="ede7c-128">需求</span><span class="sxs-lookup"><span data-stu-id="ede7c-128">Requirement</span></span> | <span data-ttu-id="ede7c-129">值</span><span class="sxs-lookup"><span data-stu-id="ede7c-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ede7c-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ede7c-130">Minimum supported client</span></span><br/> | <span data-ttu-id="ede7c-131">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ede7c-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="ede7c-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ede7c-132">Minimum supported server</span></span><br/> | <span data-ttu-id="ede7c-133">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ede7c-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ede7c-134">標頭</span><span class="sxs-lookup"><span data-stu-id="ede7c-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="ede7c-135"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="ede7c-135"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="ede7c-136">程式庫</span><span class="sxs-lookup"><span data-stu-id="ede7c-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="ede7c-137"><dt>Nmapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="ede7c-137"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="ede7c-138">DLL</span><span class="sxs-lookup"><span data-stu-id="ede7c-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ede7c-139"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ede7c-139"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




