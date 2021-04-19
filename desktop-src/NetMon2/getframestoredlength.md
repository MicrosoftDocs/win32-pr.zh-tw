---
description: GetFrameStoredLength 函式會傳回框架的長度。
ms.assetid: 7ac0e528-a45a-4c36-a99d-647347bdd143
title: 'GetFrameStoredLength 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameStoredLength
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: e48f1d357645a9f50a85da4aba79d72baba4e4bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985261"
---
# <a name="getframestoredlength-function"></a><span data-ttu-id="7a8d7-103">GetFrameStoredLength 函式</span><span class="sxs-lookup"><span data-stu-id="7a8d7-103">GetFrameStoredLength function</span></span>

<span data-ttu-id="7a8d7-104">**GetFrameStoredLength** 函式會傳回框架的長度。</span><span class="sxs-lookup"><span data-stu-id="7a8d7-104">The **GetFrameStoredLength** function returns the length of the frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a8d7-105">語法</span><span class="sxs-lookup"><span data-stu-id="7a8d7-105">Syntax</span></span>


```C++
DWORD WINAPI GetFrameStoredLength(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a><span data-ttu-id="7a8d7-106">參數</span><span class="sxs-lookup"><span data-stu-id="7a8d7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a8d7-107">*hFrame* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7a8d7-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a8d7-108">框架的控制碼。</span><span class="sxs-lookup"><span data-stu-id="7a8d7-108">Handle to the frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a8d7-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="7a8d7-109">Return value</span></span>

<span data-ttu-id="7a8d7-110">如果函式成功，則傳回值會是所儲存之框架的長度。</span><span class="sxs-lookup"><span data-stu-id="7a8d7-110">If the function is successful, the return value is the length of the frame as stored.</span></span>

<span data-ttu-id="7a8d7-111">如果函式不成功，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="7a8d7-111">If the function is unsuccessful, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a8d7-112">備註</span><span class="sxs-lookup"><span data-stu-id="7a8d7-112">Remarks</span></span>

<span data-ttu-id="7a8d7-113">[*專家*](e.md) 和 [*剖析*](p.md) 器可以呼叫 **GetFrameStoredLength** 函數。</span><span class="sxs-lookup"><span data-stu-id="7a8d7-113">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetFrameStoredLength** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a8d7-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="7a8d7-114">Requirements</span></span>



| <span data-ttu-id="7a8d7-115">需求</span><span class="sxs-lookup"><span data-stu-id="7a8d7-115">Requirement</span></span> | <span data-ttu-id="7a8d7-116">值</span><span class="sxs-lookup"><span data-stu-id="7a8d7-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7a8d7-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7a8d7-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7a8d7-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7a8d7-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="7a8d7-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7a8d7-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7a8d7-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7a8d7-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="7a8d7-121">標頭</span><span class="sxs-lookup"><span data-stu-id="7a8d7-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a8d7-122"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="7a8d7-122"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="7a8d7-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="7a8d7-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="7a8d7-124"><dt>Nmapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="7a8d7-124"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="7a8d7-125">DLL</span><span class="sxs-lookup"><span data-stu-id="7a8d7-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a8d7-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a8d7-126"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a8d7-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7a8d7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a8d7-128">GetFrameLength</span><span class="sxs-lookup"><span data-stu-id="7a8d7-128">GetFrameLength</span></span>](getframelength.md)
</dt> </dl>

 

 




