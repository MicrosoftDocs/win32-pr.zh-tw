---
description: GetFrame 函式會將控制碼傳回給捕捉內的指定框架。
ms.assetid: d40bc364-0028-4006-a6c2-6ee100366ba3
title: 'GetFrame 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 3f79e7fa6fc4e79f4dea804769cc9d51b8096860
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112225"
---
# <a name="getframe-function"></a><span data-ttu-id="9eb2f-103">GetFrame 函式</span><span class="sxs-lookup"><span data-stu-id="9eb2f-103">GetFrame function</span></span>

<span data-ttu-id="9eb2f-104">**GetFrame** 函式會將控制碼傳回給捕捉內的指定框架。</span><span class="sxs-lookup"><span data-stu-id="9eb2f-104">The **GetFrame** function returns a handle to a given frame within a capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="9eb2f-105">語法</span><span class="sxs-lookup"><span data-stu-id="9eb2f-105">Syntax</span></span>


```C++
HFRAME WINAPI GetFrame(
  _In_ HCAPTURE hCapture,
  _In_ DWORD    FrameNumber
);
```



## <a name="parameters"></a><span data-ttu-id="9eb2f-106">參數</span><span class="sxs-lookup"><span data-stu-id="9eb2f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9eb2f-107">*hCapture* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9eb2f-107">*hCapture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9eb2f-108">捕捉的控制碼。</span><span class="sxs-lookup"><span data-stu-id="9eb2f-108">Handle to a capture.</span></span> <span data-ttu-id="9eb2f-109">若要取得 capture 控制碼，請呼叫 [GetFrameCaptureHandle](getframecapturehandle.md) 函數。</span><span class="sxs-lookup"><span data-stu-id="9eb2f-109">To obtain the capture handle, call the [GetFrameCaptureHandle](getframecapturehandle.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="9eb2f-110">*FrameNumber* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9eb2f-110">*FrameNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9eb2f-111">以零為基底的框架)  (數目。</span><span class="sxs-lookup"><span data-stu-id="9eb2f-111">Number (zero-based) of the frame.</span></span> <span data-ttu-id="9eb2f-112">捕捉中第一個框架的數目為零。</span><span class="sxs-lookup"><span data-stu-id="9eb2f-112">The number of the first frame in a capture is zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9eb2f-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="9eb2f-113">Return value</span></span>

<span data-ttu-id="9eb2f-114">如果函式成功，則傳回值是框架的控制碼。</span><span class="sxs-lookup"><span data-stu-id="9eb2f-114">If the function is successful, the return value is a handle to the frame.</span></span>

<span data-ttu-id="9eb2f-115">如果函式不成功 (也就是說，如果 *hCapture* 無效，或框架編號超出範圍) ，則傳回值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="9eb2f-115">If the function is unsuccessful (that is, if *hCapture* is invalid, or the frame number is out of range), the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="9eb2f-116">備註</span><span class="sxs-lookup"><span data-stu-id="9eb2f-116">Remarks</span></span>

<span data-ttu-id="9eb2f-117">您可以使用 **GetFrame** 函式來取得尋找屬性實例時所需的框架控制碼。</span><span class="sxs-lookup"><span data-stu-id="9eb2f-117">Use the **GetFrame** function to obtain the frame handle needed when locating instances of a property.</span></span> <span data-ttu-id="9eb2f-118">用來尋找屬性實例的函式是 [FindPropertyInstance](findpropertyinstance.md) ，它會找出第一個實例，而 [FindPropertyInstanceRestart](findpropertyinstancerestart.md) 則會尋找下一個實例。</span><span class="sxs-lookup"><span data-stu-id="9eb2f-118">The functions used to locate property instances are [FindPropertyInstance](findpropertyinstance.md) which locates the first instance, and [FindPropertyInstanceRestart](findpropertyinstancerestart.md) which locates the next instance.</span></span>

<span data-ttu-id="9eb2f-119">[*專家*](e.md) 和 [*剖析*](p.md) 器可以呼叫 **GetFrame** 函數。</span><span class="sxs-lookup"><span data-stu-id="9eb2f-119">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetFrame** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="9eb2f-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="9eb2f-120">Requirements</span></span>



| <span data-ttu-id="9eb2f-121">需求</span><span class="sxs-lookup"><span data-stu-id="9eb2f-121">Requirement</span></span> | <span data-ttu-id="9eb2f-122">值</span><span class="sxs-lookup"><span data-stu-id="9eb2f-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9eb2f-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9eb2f-123">Minimum supported client</span></span><br/> | <span data-ttu-id="9eb2f-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9eb2f-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="9eb2f-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9eb2f-125">Minimum supported server</span></span><br/> | <span data-ttu-id="9eb2f-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9eb2f-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9eb2f-127">標頭</span><span class="sxs-lookup"><span data-stu-id="9eb2f-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="9eb2f-128"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="9eb2f-128"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="9eb2f-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="9eb2f-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="9eb2f-130"><dt>Nmapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="9eb2f-130"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="9eb2f-131">DLL</span><span class="sxs-lookup"><span data-stu-id="9eb2f-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9eb2f-132"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9eb2f-132"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9eb2f-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9eb2f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9eb2f-134">FindPropertyInstance</span><span class="sxs-lookup"><span data-stu-id="9eb2f-134">FindPropertyInstance</span></span>](findpropertyinstance.md)
</dt> <dt>

[<span data-ttu-id="9eb2f-135">FindPropertyInstanceRestart</span><span class="sxs-lookup"><span data-stu-id="9eb2f-135">FindPropertyInstanceRestart</span></span>](findpropertyinstancerestart.md)
</dt> </dl>

 

 




