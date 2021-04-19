---
description: 傳回捕捉批註的指標。
ms.assetid: 3ef5c5b3-5586-469f-8975-049713715403
title: 'GetCaptureComment 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCaptureComment
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: ca2d3dd3fdc91c54c49b12119a56180396df5ec5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991807"
---
# <a name="getcapturecomment-function"></a><span data-ttu-id="84dce-103">GetCaptureComment 函式</span><span class="sxs-lookup"><span data-stu-id="84dce-103">GetCaptureComment function</span></span>

<span data-ttu-id="84dce-104">**GetCaptureComment** 函式會傳回捕捉批註的指標。</span><span class="sxs-lookup"><span data-stu-id="84dce-104">The **GetCaptureComment** function returns a pointer to the comment of a capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="84dce-105">語法</span><span class="sxs-lookup"><span data-stu-id="84dce-105">Syntax</span></span>


```C++
LPSTR WINAPI GetCaptureComment(
  _In_ HCAPTURE hCapture
);
```



## <a name="parameters"></a><span data-ttu-id="84dce-106">參數</span><span class="sxs-lookup"><span data-stu-id="84dce-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84dce-107">*hCapture* \[在\]</span><span class="sxs-lookup"><span data-stu-id="84dce-107">*hCapture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84dce-108">捕捉的控制碼。</span><span class="sxs-lookup"><span data-stu-id="84dce-108">A handle to the capture.</span></span> <span data-ttu-id="84dce-109">如需取得 capture 控制碼的詳細資訊，請參閱「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="84dce-109">For more information about obtaining the capture handle, see the Remarks section.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84dce-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="84dce-110">Return value</span></span>

<span data-ttu-id="84dce-111">如果函式成功 (也就是，如果捕捉包含批註) ，則傳回值會是批註字串的指標。</span><span class="sxs-lookup"><span data-stu-id="84dce-111">If the function is successful (that is, if the capture contains a comment), the return value is a pointer to the comment string.</span></span>

<span data-ttu-id="84dce-112">如果函式不成功，則傳回值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="84dce-112">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="84dce-113">備註</span><span class="sxs-lookup"><span data-stu-id="84dce-113">Remarks</span></span>

<span data-ttu-id="84dce-114">請勿變更傳回的批註字串，這是載入的捕獲中的實際批註字串。</span><span class="sxs-lookup"><span data-stu-id="84dce-114">Do not alter the returned comment string which is the actual comment string that is in the loaded capture.</span></span> <span data-ttu-id="84dce-115">任何變更可能會損毀捕捉。</span><span class="sxs-lookup"><span data-stu-id="84dce-115">Any changes can corrupt the capture.</span></span> <span data-ttu-id="84dce-116">嘗試修改字串會導致存取違規。</span><span class="sxs-lookup"><span data-stu-id="84dce-116">Attempts to modify the string result in an access violation.</span></span>

<span data-ttu-id="84dce-117">您可以透過數種方式取得 capture 的控制碼，視呼叫是由專家或剖析器進行。</span><span class="sxs-lookup"><span data-stu-id="84dce-117">The handle of the capture can be obtained in several ways, depending if the call is made by an expert or parser.</span></span> <span data-ttu-id="84dce-118">對於專家而言，控制碼是在 [EXPERTSTARTUPINFO](expertstartupinfo.md)結構的 **hCapture** 成員中指定的。</span><span class="sxs-lookup"><span data-stu-id="84dce-118">For experts, the handle is specified in the **hCapture** member of the [EXPERTSTARTUPINFO](expertstartupinfo.md) structure.</span></span> <span data-ttu-id="84dce-119">若為剖析器，可以藉由呼叫 [GetFrameCaptureHandle](getframecapturehandle.md) 函數來取得 capture 控制碼。</span><span class="sxs-lookup"><span data-stu-id="84dce-119">For parsers, the capture handle can be obtained by calling the [GetFrameCaptureHandle](getframecapturehandle.md) function.</span></span>

<span data-ttu-id="84dce-120">若要從其 capture 檔案取出 capture 的批註，請呼叫 [GetCaptureCommentFromFilename](getcapturecommentfromfilename.md) 函數。</span><span class="sxs-lookup"><span data-stu-id="84dce-120">To retrieve the comment of a capture from its capture file, call the [GetCaptureCommentFromFilename](getcapturecommentfromfilename.md) function.</span></span>

<span data-ttu-id="84dce-121">[*專家*](e.md) 和 [*剖析*](p.md) 器可以呼叫 **GetCaptureComment** 函數。</span><span class="sxs-lookup"><span data-stu-id="84dce-121">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetCaptureComment** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="84dce-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="84dce-122">Requirements</span></span>



| <span data-ttu-id="84dce-123">需求</span><span class="sxs-lookup"><span data-stu-id="84dce-123">Requirement</span></span> | <span data-ttu-id="84dce-124">值</span><span class="sxs-lookup"><span data-stu-id="84dce-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="84dce-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="84dce-125">Minimum supported client</span></span><br/> | <span data-ttu-id="84dce-126">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="84dce-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="84dce-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="84dce-127">Minimum supported server</span></span><br/> | <span data-ttu-id="84dce-128">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="84dce-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="84dce-129">標頭</span><span class="sxs-lookup"><span data-stu-id="84dce-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="84dce-130"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="84dce-130"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="84dce-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="84dce-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="84dce-132"><dt>Nmapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="84dce-132"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="84dce-133">DLL</span><span class="sxs-lookup"><span data-stu-id="84dce-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84dce-134"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="84dce-134"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84dce-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="84dce-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84dce-136">EXPERTSTARTUPINFO</span><span class="sxs-lookup"><span data-stu-id="84dce-136">EXPERTSTARTUPINFO</span></span>](expertstartupinfo.md)
</dt> <dt>

[<span data-ttu-id="84dce-137">GetCaptureCommentFromFilename</span><span class="sxs-lookup"><span data-stu-id="84dce-137">GetCaptureCommentFromFilename</span></span>](getcapturecommentfromfilename.md)
</dt> <dt>

[<span data-ttu-id="84dce-138">GetFrameCaptureHandle</span><span class="sxs-lookup"><span data-stu-id="84dce-138">GetFrameCaptureHandle</span></span>](getframecapturehandle.md)
</dt> </dl>

 

 




