---
description: GetFrameMacType 函式會傳回框架的 MAC 型別。
ms.assetid: 8d3da770-1392-4638-a267-32c2dae289b0
title: 'GetFrameMacType 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameMacType
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: b85accc64a6e29424e3f65d070bafcf29bb3ec0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936625"
---
# <a name="getframemactype-function"></a><span data-ttu-id="18666-103">GetFrameMacType 函式</span><span class="sxs-lookup"><span data-stu-id="18666-103">GetFrameMacType function</span></span>

<span data-ttu-id="18666-104">**GetFrameMacType** 函式會傳回框架的 MAC 型別。</span><span class="sxs-lookup"><span data-stu-id="18666-104">The **GetFrameMacType** function returns the MAC type of the frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="18666-105">語法</span><span class="sxs-lookup"><span data-stu-id="18666-105">Syntax</span></span>


```C++
DWORD WINAPI GetFrameMacType(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a><span data-ttu-id="18666-106">參數</span><span class="sxs-lookup"><span data-stu-id="18666-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18666-107">*hFrame* \[在\]</span><span class="sxs-lookup"><span data-stu-id="18666-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18666-108">框架的控制碼。</span><span class="sxs-lookup"><span data-stu-id="18666-108">Handle to the frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18666-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="18666-109">Return value</span></span>

<span data-ttu-id="18666-110">函數會傳回框架的 MAC 型別，它可以有下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="18666-110">The function returns the MAC type of the frame, which can have one of the following values.</span></span>

-   <span data-ttu-id="18666-111">MAC \_ 類型 \_ 不明</span><span class="sxs-lookup"><span data-stu-id="18666-111">MAC\_TYPE\_UNKNOWN</span></span>
-   <span data-ttu-id="18666-112">MAC \_ 類型 \_ ETHERNET</span><span class="sxs-lookup"><span data-stu-id="18666-112">MAC\_TYPE\_ETHERNET</span></span>
-   <span data-ttu-id="18666-113">MAC \_ 類型 \_ TOKENRING</span><span class="sxs-lookup"><span data-stu-id="18666-113">MAC\_TYPE\_TOKENRING</span></span>
-   <span data-ttu-id="18666-114">MAC \_ 類型的 \_ FDDI</span><span class="sxs-lookup"><span data-stu-id="18666-114">MAC\_TYPE\_FDDI</span></span>

## <a name="remarks"></a><span data-ttu-id="18666-115">備註</span><span class="sxs-lookup"><span data-stu-id="18666-115">Remarks</span></span>

<span data-ttu-id="18666-116">[*專家*](e.md) 和 [*剖析*](p.md) 器可以呼叫 **GetFrameMacType** 函數。</span><span class="sxs-lookup"><span data-stu-id="18666-116">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetFrameMacType** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="18666-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="18666-117">Requirements</span></span>



| <span data-ttu-id="18666-118">需求</span><span class="sxs-lookup"><span data-stu-id="18666-118">Requirement</span></span> | <span data-ttu-id="18666-119">值</span><span class="sxs-lookup"><span data-stu-id="18666-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="18666-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="18666-120">Minimum supported client</span></span><br/> | <span data-ttu-id="18666-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="18666-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="18666-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="18666-122">Minimum supported server</span></span><br/> | <span data-ttu-id="18666-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="18666-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="18666-124">標頭</span><span class="sxs-lookup"><span data-stu-id="18666-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="18666-125"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="18666-125"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="18666-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="18666-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="18666-127"><dt>Nmapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="18666-127"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="18666-128">DLL</span><span class="sxs-lookup"><span data-stu-id="18666-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18666-129"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18666-129"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




