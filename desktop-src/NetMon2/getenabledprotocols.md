---
description: GetEnabledProtocols 函式會傳回所有標示為已啟用之通訊協定的資料表。
ms.assetid: 11feac64-c770-47b2-a740-fc372e97b8ed
title: 'GetEnabledProtocols 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetEnabledProtocols
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 284d6c87bf5a3b26d6c3f379a710966be21006d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106967086"
---
# <a name="getenabledprotocols-function"></a><span data-ttu-id="c113b-103">GetEnabledProtocols 函式</span><span class="sxs-lookup"><span data-stu-id="c113b-103">GetEnabledProtocols function</span></span>

<span data-ttu-id="c113b-104">**GetEnabledProtocols** 函式會傳回所有標示為已啟用之通訊協定的資料表。</span><span class="sxs-lookup"><span data-stu-id="c113b-104">The **GetEnabledProtocols** function returns a table of all protocols that are marked Enabled.</span></span>

## <a name="syntax"></a><span data-ttu-id="c113b-105">語法</span><span class="sxs-lookup"><span data-stu-id="c113b-105">Syntax</span></span>


```C++
LPPROTOCOLTABLE WINAPI GetEnabledProtocols(
  _In_ HCAPTURE hCapture
);
```



## <a name="parameters"></a><span data-ttu-id="c113b-106">參數</span><span class="sxs-lookup"><span data-stu-id="c113b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c113b-107">*hCapture* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c113b-107">*hCapture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c113b-108">捕捉的控制碼。</span><span class="sxs-lookup"><span data-stu-id="c113b-108">Handle to the capture.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c113b-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="c113b-109">Return value</span></span>

<span data-ttu-id="c113b-110">如果函式成功，則傳回值是 [PROTOCOLTABLE](protocoltable.md) 結構的指標，此結構會列出捕捉中所有已啟用的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="c113b-110">If the function is successful, the return value is a pointer to a [PROTOCOLTABLE](protocoltable.md) structure that lists all the enabled protocols in the capture.</span></span>

<span data-ttu-id="c113b-111">如果函式不成功，則傳回值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="c113b-111">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c113b-112">備註</span><span class="sxs-lookup"><span data-stu-id="c113b-112">Remarks</span></span>

<span data-ttu-id="c113b-113">[*專家*](e.md) 和 [*剖析*](p.md) 器可以呼叫 **GetEnabledProtocols** 函數。</span><span class="sxs-lookup"><span data-stu-id="c113b-113">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetEnabledProtocols** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="c113b-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="c113b-114">Requirements</span></span>



| <span data-ttu-id="c113b-115">需求</span><span class="sxs-lookup"><span data-stu-id="c113b-115">Requirement</span></span> | <span data-ttu-id="c113b-116">值</span><span class="sxs-lookup"><span data-stu-id="c113b-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c113b-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c113b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c113b-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c113b-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="c113b-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c113b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c113b-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c113b-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="c113b-121">標頭</span><span class="sxs-lookup"><span data-stu-id="c113b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c113b-122"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="c113b-122"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="c113b-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="c113b-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="c113b-124"><dt>Nmapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c113b-124"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="c113b-125">DLL</span><span class="sxs-lookup"><span data-stu-id="c113b-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c113b-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c113b-126"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c113b-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c113b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c113b-128">PROTOCOLTABLE</span><span class="sxs-lookup"><span data-stu-id="c113b-128">PROTOCOLTABLE</span></span>](protocoltable.md)
</dt> </dl>

 

 




