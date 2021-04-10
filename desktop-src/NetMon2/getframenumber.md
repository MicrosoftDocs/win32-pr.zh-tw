---
description: GetFrameNumber 函式會傳回框架的數目。
ms.assetid: 97d343a3-2a1e-47d7-bfc2-b63f8d84b29d
title: 'GetFrameNumber 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameNumber
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: de04fa513fab98b1a82d036f6f40a6c67cdda3ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936624"
---
# <a name="getframenumber-function"></a><span data-ttu-id="35305-103">GetFrameNumber 函式</span><span class="sxs-lookup"><span data-stu-id="35305-103">GetFrameNumber function</span></span>

<span data-ttu-id="35305-104">**GetFrameNumber** 函式會傳回框架的數目。</span><span class="sxs-lookup"><span data-stu-id="35305-104">The **GetFrameNumber** function returns the number of a frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="35305-105">語法</span><span class="sxs-lookup"><span data-stu-id="35305-105">Syntax</span></span>


```C++
DWORD WINAPI GetFrameNumber(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a><span data-ttu-id="35305-106">參數</span><span class="sxs-lookup"><span data-stu-id="35305-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35305-107">*hFrame* \[在\]</span><span class="sxs-lookup"><span data-stu-id="35305-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35305-108">框架的控制碼。</span><span class="sxs-lookup"><span data-stu-id="35305-108">Handle to the frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35305-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="35305-109">Return value</span></span>

<span data-ttu-id="35305-110">如果函式成功，則傳回值是以零為基底的框架編號。</span><span class="sxs-lookup"><span data-stu-id="35305-110">If the function is successful, the return value is a zero-based frame number.</span></span>

<span data-ttu-id="35305-111">如果函式不成功，則傳回值為減去 1 (-1) 。</span><span class="sxs-lookup"><span data-stu-id="35305-111">If the function is not successful, the return value is minus one (-1).</span></span>

## <a name="remarks"></a><span data-ttu-id="35305-112">備註</span><span class="sxs-lookup"><span data-stu-id="35305-112">Remarks</span></span>

<span data-ttu-id="35305-113">[*專家*](e.md) 和 [*剖析*](p.md) 器可以呼叫 **GetFrameNumber** 函數。</span><span class="sxs-lookup"><span data-stu-id="35305-113">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetFrameNumber** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="35305-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="35305-114">Requirements</span></span>



| <span data-ttu-id="35305-115">需求</span><span class="sxs-lookup"><span data-stu-id="35305-115">Requirement</span></span> | <span data-ttu-id="35305-116">值</span><span class="sxs-lookup"><span data-stu-id="35305-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="35305-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="35305-117">Minimum supported client</span></span><br/> | <span data-ttu-id="35305-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="35305-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="35305-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="35305-119">Minimum supported server</span></span><br/> | <span data-ttu-id="35305-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="35305-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="35305-121">標頭</span><span class="sxs-lookup"><span data-stu-id="35305-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="35305-122"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="35305-122"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="35305-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="35305-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="35305-124"><dt>Nmapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="35305-124"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="35305-125">DLL</span><span class="sxs-lookup"><span data-stu-id="35305-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35305-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35305-126"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




