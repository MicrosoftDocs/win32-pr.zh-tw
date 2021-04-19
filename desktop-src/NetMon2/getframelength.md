---
description: GetFrameLength 函式會傳回框架的長度。
ms.assetid: 30be1f5c-9b13-42ad-944a-92b1aee8a6bc
title: 'GetFrameLength 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameLength
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 29a2a08ac105414a914e14a9ce8e69976725700c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986300"
---
# <a name="getframelength-function"></a><span data-ttu-id="f8f06-103">GetFrameLength 函式</span><span class="sxs-lookup"><span data-stu-id="f8f06-103">GetFrameLength function</span></span>

<span data-ttu-id="f8f06-104">**GetFrameLength** 函式會傳回框架的長度。</span><span class="sxs-lookup"><span data-stu-id="f8f06-104">The **GetFrameLength** function returns the length of the frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8f06-105">語法</span><span class="sxs-lookup"><span data-stu-id="f8f06-105">Syntax</span></span>


```C++
DWORD WINAPI GetFrameLength(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a><span data-ttu-id="f8f06-106">參數</span><span class="sxs-lookup"><span data-stu-id="f8f06-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8f06-107">*hFrame* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f8f06-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8f06-108">框架的控制碼。</span><span class="sxs-lookup"><span data-stu-id="f8f06-108">Handle to a frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8f06-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="f8f06-109">Return value</span></span>

<span data-ttu-id="f8f06-110">如果函式成功，則傳回值為框架的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="f8f06-110">If the function is successful, the return value is the length of the frame   in bytes.</span></span>

<span data-ttu-id="f8f06-111">如果函式不成功，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="f8f06-111">If the function is unsuccessful, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8f06-112">備註</span><span class="sxs-lookup"><span data-stu-id="f8f06-112">Remarks</span></span>

<span data-ttu-id="f8f06-113">[*專家*](e.md) 和 [*剖析*](p.md) 器可以呼叫 **GetFrameLength** 函數。</span><span class="sxs-lookup"><span data-stu-id="f8f06-113">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetFrameLength** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8f06-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="f8f06-114">Requirements</span></span>



| <span data-ttu-id="f8f06-115">需求</span><span class="sxs-lookup"><span data-stu-id="f8f06-115">Requirement</span></span> | <span data-ttu-id="f8f06-116">值</span><span class="sxs-lookup"><span data-stu-id="f8f06-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f8f06-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f8f06-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f8f06-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f8f06-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="f8f06-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f8f06-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f8f06-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f8f06-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f8f06-121">標頭</span><span class="sxs-lookup"><span data-stu-id="f8f06-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8f06-122"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="f8f06-122"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="f8f06-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="f8f06-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="f8f06-124"><dt>Nmapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f8f06-124"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="f8f06-125">DLL</span><span class="sxs-lookup"><span data-stu-id="f8f06-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f8f06-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f8f06-126"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




