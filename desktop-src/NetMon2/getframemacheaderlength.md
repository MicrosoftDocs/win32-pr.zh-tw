---
description: GetFrameMacHeaderLength 函式會傳回框架的 MAC 標頭長度（以位元組為單位）。
ms.assetid: 4a0f6a8c-04e0-47cb-abd1-b4011cd2d062
title: 'GetFrameMacHeaderLength 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameMacHeaderLength
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 4d11a0efac2086884e984edae986720ef704cf81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972374"
---
# <a name="getframemacheaderlength-function"></a><span data-ttu-id="a8342-103">GetFrameMacHeaderLength 函式</span><span class="sxs-lookup"><span data-stu-id="a8342-103">GetFrameMacHeaderLength function</span></span>

<span data-ttu-id="a8342-104">**GetFrameMacHeaderLength** 函式會傳回框架的 MAC 標頭長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="a8342-104">The **GetFrameMacHeaderLength** function returns the length, in bytes, of the MAC header of the frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8342-105">語法</span><span class="sxs-lookup"><span data-stu-id="a8342-105">Syntax</span></span>


```C++
DWORD WINAPI GetFrameMacHeaderLength(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a><span data-ttu-id="a8342-106">參數</span><span class="sxs-lookup"><span data-stu-id="a8342-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8342-107">*hFrame* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a8342-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8342-108">框架的控制碼。</span><span class="sxs-lookup"><span data-stu-id="a8342-108">Handle to the frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8342-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="a8342-109">Return value</span></span>

<span data-ttu-id="a8342-110">如果函式成功，則傳回值是 MAC 標頭的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="a8342-110">If the function is successful, the return value is the length   in bytes   of the MAC header.</span></span>

<span data-ttu-id="a8342-111">如果函式不成功，或遇到未知的 MAC 型別，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="a8342-111">If the function is not successful, or an unknown MAC type is encountered, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8342-112">備註</span><span class="sxs-lookup"><span data-stu-id="a8342-112">Remarks</span></span>

<span data-ttu-id="a8342-113">[*專家*](e.md) 和 [*剖析*](p.md) 器可以呼叫 **GetFrameMacHeaderLength** 函數。</span><span class="sxs-lookup"><span data-stu-id="a8342-113">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetFrameMacHeaderLength** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8342-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="a8342-114">Requirements</span></span>



| <span data-ttu-id="a8342-115">需求</span><span class="sxs-lookup"><span data-stu-id="a8342-115">Requirement</span></span> | <span data-ttu-id="a8342-116">值</span><span class="sxs-lookup"><span data-stu-id="a8342-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a8342-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a8342-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a8342-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a8342-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="a8342-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a8342-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a8342-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a8342-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="a8342-121">標頭</span><span class="sxs-lookup"><span data-stu-id="a8342-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8342-122"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="a8342-122"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="a8342-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="a8342-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="a8342-124"><dt>Nmapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a8342-124"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="a8342-125">DLL</span><span class="sxs-lookup"><span data-stu-id="a8342-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8342-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8342-126"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




