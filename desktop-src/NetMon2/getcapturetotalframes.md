---
description: GetCaptureTotalFrames 函式會傳回捕捉中的總畫面數。
ms.assetid: a2b7902c-b80f-4a0a-b12a-2a139df30fca
title: 'GetCaptureTotalFrames 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCaptureTotalFrames
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: aa7c81e690e9f7eab258c832ae374f18f9b7afc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847739"
---
# <a name="getcapturetotalframes-function"></a><span data-ttu-id="1ff6a-103">GetCaptureTotalFrames 函式</span><span class="sxs-lookup"><span data-stu-id="1ff6a-103">GetCaptureTotalFrames function</span></span>

<span data-ttu-id="1ff6a-104">**GetCaptureTotalFrames** 函式會傳回捕捉中的總畫面數。</span><span class="sxs-lookup"><span data-stu-id="1ff6a-104">The **GetCaptureTotalFrames** function returns the total number of frames in the capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ff6a-105">語法</span><span class="sxs-lookup"><span data-stu-id="1ff6a-105">Syntax</span></span>


```C++
DWORD WINAPI GetCaptureTotalFrames(
  _In_ HCAPTURE hCapture
);
```



## <a name="parameters"></a><span data-ttu-id="1ff6a-106">參數</span><span class="sxs-lookup"><span data-stu-id="1ff6a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ff6a-107">*hCapture* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1ff6a-107">*hCapture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ff6a-108">捕捉的控制碼。</span><span class="sxs-lookup"><span data-stu-id="1ff6a-108">Handle to the capture.</span></span> <span data-ttu-id="1ff6a-109">如需取得 capture 控制碼的詳細資訊，請參閱本 **GetCaptureTotalFrames** 主題的「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="1ff6a-109">For information about obtaining the capture handle, see the Remarks section of this **GetCaptureTotalFrames** topic.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ff6a-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="1ff6a-110">Return value</span></span>

<span data-ttu-id="1ff6a-111">如果函式成功，則傳回值是捕捉中的框架總數。</span><span class="sxs-lookup"><span data-stu-id="1ff6a-111">If the function is successful, the return value is the total number of frames in the capture.</span></span>

<span data-ttu-id="1ff6a-112">如果函式不成功，則傳回值為0。</span><span class="sxs-lookup"><span data-stu-id="1ff6a-112">If the function is unsuccessful, the return value is 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ff6a-113">備註</span><span class="sxs-lookup"><span data-stu-id="1ff6a-113">Remarks</span></span>

<span data-ttu-id="1ff6a-114">[*專家*](e.md) 和 [*剖析*](p.md) 器可以呼叫 **GetCaptureTotalFrames** 函數。</span><span class="sxs-lookup"><span data-stu-id="1ff6a-114">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetCaptureTotalFrames** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ff6a-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="1ff6a-115">Requirements</span></span>



| <span data-ttu-id="1ff6a-116">需求</span><span class="sxs-lookup"><span data-stu-id="1ff6a-116">Requirement</span></span> | <span data-ttu-id="1ff6a-117">值</span><span class="sxs-lookup"><span data-stu-id="1ff6a-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1ff6a-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1ff6a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1ff6a-119">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1ff6a-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="1ff6a-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1ff6a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1ff6a-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1ff6a-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="1ff6a-122">標頭</span><span class="sxs-lookup"><span data-stu-id="1ff6a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ff6a-123"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="1ff6a-123"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="1ff6a-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="1ff6a-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="1ff6a-125"><dt>Nmapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="1ff6a-125"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="1ff6a-126">DLL</span><span class="sxs-lookup"><span data-stu-id="1ff6a-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1ff6a-127"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1ff6a-127"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




