---
description: GetFrameCaptureHandle 函式會根據指定的框架，傳回捕捉的控制碼。
ms.assetid: 71b32799-194c-40f8-8438-36aebaba31c7
title: 'GetFrameCaptureHandle 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameCaptureHandle
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 3770ad0fd3db7d1c076b5d1f286c1fdbdc2707a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847737"
---
# <a name="getframecapturehandle-function"></a><span data-ttu-id="377ef-103">GetFrameCaptureHandle 函式</span><span class="sxs-lookup"><span data-stu-id="377ef-103">GetFrameCaptureHandle function</span></span>

<span data-ttu-id="377ef-104">**GetFrameCaptureHandle** 函式會根據指定的框架，傳回捕捉的控制碼。</span><span class="sxs-lookup"><span data-stu-id="377ef-104">The **GetFrameCaptureHandle** function returns a handle to the capture based on a given frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="377ef-105">語法</span><span class="sxs-lookup"><span data-stu-id="377ef-105">Syntax</span></span>


```C++
HCAPTURE WINAPI GetFrameCaptureHandle(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a><span data-ttu-id="377ef-106">參數</span><span class="sxs-lookup"><span data-stu-id="377ef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="377ef-107">*hFrame* \[在\]</span><span class="sxs-lookup"><span data-stu-id="377ef-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="377ef-108">框架的控制碼。</span><span class="sxs-lookup"><span data-stu-id="377ef-108">Handle to a frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="377ef-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="377ef-109">Return value</span></span>

<span data-ttu-id="377ef-110">如果函式成功，則傳回值會是捕捉的控制碼。</span><span class="sxs-lookup"><span data-stu-id="377ef-110">If the function is successful, the return value is a handle to the capture.</span></span>

<span data-ttu-id="377ef-111">如果函式不成功，則傳回值為0。</span><span class="sxs-lookup"><span data-stu-id="377ef-111">If the function is unsuccessful, the return value is 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="377ef-112">備註</span><span class="sxs-lookup"><span data-stu-id="377ef-112">Remarks</span></span>

<span data-ttu-id="377ef-113">[*專家*](e.md) 和 [*剖析*](p.md) 器可以呼叫 **GetFrameCaptureHandle** 函數。</span><span class="sxs-lookup"><span data-stu-id="377ef-113">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetFrameCaptureHandle** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="377ef-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="377ef-114">Requirements</span></span>



| <span data-ttu-id="377ef-115">需求</span><span class="sxs-lookup"><span data-stu-id="377ef-115">Requirement</span></span> | <span data-ttu-id="377ef-116">值</span><span class="sxs-lookup"><span data-stu-id="377ef-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="377ef-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="377ef-117">Minimum supported client</span></span><br/> | <span data-ttu-id="377ef-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="377ef-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="377ef-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="377ef-119">Minimum supported server</span></span><br/> | <span data-ttu-id="377ef-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="377ef-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="377ef-121">標頭</span><span class="sxs-lookup"><span data-stu-id="377ef-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="377ef-122"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="377ef-122"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="377ef-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="377ef-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="377ef-124"><dt>Nmapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="377ef-124"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="377ef-125">DLL</span><span class="sxs-lookup"><span data-stu-id="377ef-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="377ef-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="377ef-126"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




