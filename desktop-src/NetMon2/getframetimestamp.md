---
description: GetFrameTimeStamp 函式會傳回指定框架的時間戳記。
ms.assetid: 4ac50400-6674-40fa-9a69-9c0ccb55b92c
title: 'GetFrameTimeStamp 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameTimeStamp
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 37a75f946a5fc0ddb2b32d99334368a272fdf2e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106982456"
---
# <a name="getframetimestamp-function"></a><span data-ttu-id="38337-103">GetFrameTimeStamp 函式</span><span class="sxs-lookup"><span data-stu-id="38337-103">GetFrameTimeStamp function</span></span>

<span data-ttu-id="38337-104">**GetFrameTimeStamp** 函式會傳回指定框架的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="38337-104">The **GetFrameTimeStamp** function returns the time stamp of a given frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="38337-105">語法</span><span class="sxs-lookup"><span data-stu-id="38337-105">Syntax</span></span>


```C++
__int64 WINAPI GetFrameTimeStamp(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a><span data-ttu-id="38337-106">參數</span><span class="sxs-lookup"><span data-stu-id="38337-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38337-107">*hFrame* \[在\]</span><span class="sxs-lookup"><span data-stu-id="38337-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38337-108">框架的控制碼。</span><span class="sxs-lookup"><span data-stu-id="38337-108">Handle to the frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38337-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="38337-109">Return value</span></span>

<span data-ttu-id="38337-110">如果函式成功，則傳回值為框架的時間戳記（以微秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="38337-110">If the function is successful, the return value is the time stamp of the frame   in microseconds.</span></span>

<span data-ttu-id="38337-111">如果函式不成功，則傳回值為減去 1 (-1) 。</span><span class="sxs-lookup"><span data-stu-id="38337-111">If the function is unsuccessful, the return value is minus one (-1).</span></span>

## <a name="remarks"></a><span data-ttu-id="38337-112">備註</span><span class="sxs-lookup"><span data-stu-id="38337-112">Remarks</span></span>

<span data-ttu-id="38337-113">**GetFrameTimeStamp** 函式會傳回時間戳記，以顯示捕捉程式開始與框架錄製之間經過的時間。</span><span class="sxs-lookup"><span data-stu-id="38337-113">The **GetFrameTimeStamp** function returns a time stamp that shows the elapsed time between the start of the capture process, and the recording of the frame.</span></span>

<span data-ttu-id="38337-114">[*專家*](e.md) 和 [*剖析*](p.md) 器可以呼叫 **GetFrameTimeStamp** 函數。</span><span class="sxs-lookup"><span data-stu-id="38337-114">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetFrameTimeStamp** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="38337-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="38337-115">Requirements</span></span>



| <span data-ttu-id="38337-116">需求</span><span class="sxs-lookup"><span data-stu-id="38337-116">Requirement</span></span> | <span data-ttu-id="38337-117">值</span><span class="sxs-lookup"><span data-stu-id="38337-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="38337-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="38337-118">Minimum supported client</span></span><br/> | <span data-ttu-id="38337-119">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="38337-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="38337-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="38337-120">Minimum supported server</span></span><br/> | <span data-ttu-id="38337-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="38337-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="38337-122">標頭</span><span class="sxs-lookup"><span data-stu-id="38337-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="38337-123"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="38337-123"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="38337-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="38337-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="38337-125"><dt>Nmapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="38337-125"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="38337-126">DLL</span><span class="sxs-lookup"><span data-stu-id="38337-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="38337-127"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="38337-127"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




