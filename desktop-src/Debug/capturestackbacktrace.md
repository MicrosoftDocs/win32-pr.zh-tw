---
UID: ''
title: CaptureStackBackTrace 函式
description: 藉由向上查看堆疊來捕捉堆疊回溯追蹤。
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: RtlCaptureStackBackTrace
ms.topic: reference
req.header: WinBase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: Kernel32.lib
req.dll: API-MS-Win-Core-rtlsupport-l1-1-0.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location:
- API-MS-Win-Core-rtlsupport-l1-1-0.dll
api_name:
- CaptureStackBackTrace
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: 3c9edc9184000d513b82ad4131e3ac05c2ed22d6
ms.sourcegitcommit: 1f6a1bfc1c4bb2641bc3ba44beb1f2727c94681b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2020
ms.locfileid: "106969502"
---
# <a name="capturestackbacktrace-function"></a><span data-ttu-id="26b78-103">CaptureStackBackTrace 函式</span><span class="sxs-lookup"><span data-stu-id="26b78-103">CaptureStackBackTrace function</span></span>

## <a name="description"></a><span data-ttu-id="26b78-104">Description</span><span class="sxs-lookup"><span data-stu-id="26b78-104">Description</span></span>

<span data-ttu-id="26b78-105">藉由向上查看堆疊並記錄每個畫面格的資訊，來捕獲堆疊回溯追蹤。</span><span class="sxs-lookup"><span data-stu-id="26b78-105">Captures a stack back trace by walking up the stack and recording the information for each frame.</span></span>

```cpp
USHORT WINAPI CaptureStackBackTrace(
  _In_      ULONG  FramesToSkip,
  _In_      ULONG  FramesToCapture,
  _Out_     PVOID  *BackTrace,
  _Out_opt_ PULONG BackTraceHash
);
```

## <a name="parameters"></a><span data-ttu-id="26b78-106">參數</span><span class="sxs-lookup"><span data-stu-id="26b78-106">Parameters</span></span>

### <a name="framestoskip-in"></a><span data-ttu-id="26b78-107">FramesToSkip [in]</span><span class="sxs-lookup"><span data-stu-id="26b78-107">FramesToSkip [in]</span></span>

<span data-ttu-id="26b78-108">從回溯追蹤的開頭跳過的框架數。</span><span class="sxs-lookup"><span data-stu-id="26b78-108">The number of frames to skip from the start of the back trace.</span></span>

### <a name="framestocapture-in"></a><span data-ttu-id="26b78-109">FramesToCapture [in]</span><span class="sxs-lookup"><span data-stu-id="26b78-109">FramesToCapture [in]</span></span>

<span data-ttu-id="26b78-110">要捕捉的框架數目。</span><span class="sxs-lookup"><span data-stu-id="26b78-110">The number of frames to be captured.</span></span>
<span data-ttu-id="26b78-111">您可以捕獲最多 **MAXUSHORT** 的畫面格。</span><span class="sxs-lookup"><span data-stu-id="26b78-111">You can capture up to **MAXUSHORT** frames.</span></span>

<span data-ttu-id="26b78-112">**Windows Server 2003 和 WINDOWS XP：** *FramesToSkip* 和 *FramesToCapture* 參數的總和必須小於63。</span><span class="sxs-lookup"><span data-stu-id="26b78-112">**Windows Server 2003 and Windows XP:**  The sum of the *FramesToSkip* and *FramesToCapture* parameters must be less than 63.</span></span>

### <a name="backtrace-out"></a><span data-ttu-id="26b78-113">BackTrace [out]</span><span class="sxs-lookup"><span data-stu-id="26b78-113">BackTrace [out]</span></span>

<span data-ttu-id="26b78-114">從目前堆疊追蹤所捕捉的指標陣列。</span><span class="sxs-lookup"><span data-stu-id="26b78-114">An array of pointers captured from the current stack trace.</span></span>

### <a name="backtracehash-out-optional"></a><span data-ttu-id="26b78-115">BackTraceHash [out，optional]</span><span class="sxs-lookup"><span data-stu-id="26b78-115">BackTraceHash [out, optional]</span></span>

<span data-ttu-id="26b78-116">可以用來組織雜湊資料表的值。</span><span class="sxs-lookup"><span data-stu-id="26b78-116">A value that can be used to organize hash tables.</span></span>
<span data-ttu-id="26b78-117">如果此參數為 **Null**，則不會計算任何雜湊值。</span><span class="sxs-lookup"><span data-stu-id="26b78-117">If this parameter is **NULL**, then no hash value is computed.</span></span>

<span data-ttu-id="26b78-118">此值的計算方式是根據 BackTrace 陣列中傳回的指標值。</span><span class="sxs-lookup"><span data-stu-id="26b78-118">This value is calculated based on the values of the pointers returned in the BackTrace array.</span></span>
<span data-ttu-id="26b78-119">兩個相同的堆疊追蹤將會產生相同的雜湊值。</span><span class="sxs-lookup"><span data-stu-id="26b78-119">Two identical stack traces will generate identical hash values.</span></span>

## <a name="returns"></a><span data-ttu-id="26b78-120">傳回</span><span class="sxs-lookup"><span data-stu-id="26b78-120">Returns</span></span>

<span data-ttu-id="26b78-121">已捕獲的框架數目。</span><span class="sxs-lookup"><span data-stu-id="26b78-121">The number of captured frames.</span></span>

## <a name="remarks"></a><span data-ttu-id="26b78-122">備註</span><span class="sxs-lookup"><span data-stu-id="26b78-122">Remarks</span></span>

<span data-ttu-id="26b78-123">**CaptureStackBackTrace** 函式會定義為 **RtlCaptureStackBackTrace** 函式 (定義會包含在 Windows SDK 從 Windows Vista) 開始。</span><span class="sxs-lookup"><span data-stu-id="26b78-123">The **CaptureStackBackTrace** function is defined as the **RtlCaptureStackBackTrace** function (the definition is included in the Windows SDK beginning with Windows Vista).</span></span>
<span data-ttu-id="26b78-124">如需詳細資訊，請參閱 WinBase .h 和 WinNT. h。</span><span class="sxs-lookup"><span data-stu-id="26b78-124">For more information, see WinBase.h and WinNT.h.</span></span>

## <a name="see-also"></a><span data-ttu-id="26b78-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="26b78-125">See also</span></span>
