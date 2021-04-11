---
description: GetFrameSrcAddressOffset 函式會傳回框架來源位址的位移。
ms.assetid: 1c5408d7-cf66-4887-93ee-134c0b8c5eff
title: 'GetFrameSrcAddressOffset 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameSrcAddressOffset
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: f7310c0ac2c6f402c37537100cc8060fef9eedd1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193917"
---
# <a name="getframesrcaddressoffset-function"></a><span data-ttu-id="c40f3-103">GetFrameSrcAddressOffset 函式</span><span class="sxs-lookup"><span data-stu-id="c40f3-103">GetFrameSrcAddressOffset function</span></span>

<span data-ttu-id="c40f3-104">**GetFrameSrcAddressOffset** 函式會傳回框架來源位址的位移。</span><span class="sxs-lookup"><span data-stu-id="c40f3-104">The **GetFrameSrcAddressOffset** function returns the offset of the frame's source address.</span></span>

## <a name="syntax"></a><span data-ttu-id="c40f3-105">語法</span><span class="sxs-lookup"><span data-stu-id="c40f3-105">Syntax</span></span>


```C++
DWORD WINAPI GetFrameSrcAddressOffset(
   HFRAME  hFrame,
   DWORD   AddressType,
   LPDWORD AddressLength
);
```



## <a name="parameters"></a><span data-ttu-id="c40f3-106">參數</span><span class="sxs-lookup"><span data-stu-id="c40f3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c40f3-107">*hFrame*</span><span class="sxs-lookup"><span data-stu-id="c40f3-107">*hFrame*</span></span> 
</dt> <dd>

<span data-ttu-id="c40f3-108">框架的控制碼。</span><span class="sxs-lookup"><span data-stu-id="c40f3-108">Handle to the frame.</span></span>

</dd> <dt>

<span data-ttu-id="c40f3-109">*AddressType*</span><span class="sxs-lookup"><span data-stu-id="c40f3-109">*AddressType*</span></span> 
</dt> <dd>

<span data-ttu-id="c40f3-110">來源網址類別型。</span><span class="sxs-lookup"><span data-stu-id="c40f3-110">Source address type.</span></span> <span data-ttu-id="c40f3-111">參數值可以是下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="c40f3-111">The parameter value can be one of the following:</span></span>

-   <span data-ttu-id="c40f3-112">位址 \_ 類型 \_ ETHERNET</span><span class="sxs-lookup"><span data-stu-id="c40f3-112">ADDRESS\_TYPE\_ETHERNET</span></span>
-   <span data-ttu-id="c40f3-113">位址 \_ 類型 \_ IP</span><span class="sxs-lookup"><span data-stu-id="c40f3-113">ADDRESS\_TYPE\_IP</span></span>
-   <span data-ttu-id="c40f3-114">位址 \_ 類型的 \_ IPX</span><span class="sxs-lookup"><span data-stu-id="c40f3-114">ADDRESS\_TYPE\_IPX</span></span>
-   <span data-ttu-id="c40f3-115">位址 \_ 類型 \_ TOKENRING</span><span class="sxs-lookup"><span data-stu-id="c40f3-115">ADDRESS\_TYPE\_TOKENRING</span></span>
-   <span data-ttu-id="c40f3-116">位址 \_ 類型的 \_ FDDI</span><span class="sxs-lookup"><span data-stu-id="c40f3-116">ADDRESS\_TYPE\_FDDI</span></span>
-   <span data-ttu-id="c40f3-117">位址 \_ 類型 \_ XNS</span><span class="sxs-lookup"><span data-stu-id="c40f3-117">ADDRESS\_TYPE\_XNS</span></span>
-   <span data-ttu-id="c40f3-118">位址 \_ 類型 \_ VINES \_ IP</span><span class="sxs-lookup"><span data-stu-id="c40f3-118">ADDRESS\_TYPE\_VINES\_IP</span></span>
-   <span data-ttu-id="c40f3-119">位址 \_ 類型的 \_ ATM</span><span class="sxs-lookup"><span data-stu-id="c40f3-119">ADDRESS\_TYPE\_ATM</span></span>

</dd> <dt>

<span data-ttu-id="c40f3-120">*AddressLength*</span><span class="sxs-lookup"><span data-stu-id="c40f3-120">*AddressLength*</span></span> 
</dt> <dd>

<span data-ttu-id="c40f3-121">**DWORD** 的指標，它會在傳回時包含位址的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="c40f3-121">Pointer to a **DWORD**, which on return, contains the length of the address, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c40f3-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="c40f3-122">Return value</span></span>

<span data-ttu-id="c40f3-123">如果函式成功，則傳回值為來源位址的位移。</span><span class="sxs-lookup"><span data-stu-id="c40f3-123">If the function is successful, the return value is the offset to the source address.</span></span>

<span data-ttu-id="c40f3-124">如果函式不成功，則傳回值為減去 1 (-1) 。</span><span class="sxs-lookup"><span data-stu-id="c40f3-124">If the function is unsuccessful, the return value is minus one (-1).</span></span>

## <a name="requirements"></a><span data-ttu-id="c40f3-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="c40f3-125">Requirements</span></span>



| <span data-ttu-id="c40f3-126">需求</span><span class="sxs-lookup"><span data-stu-id="c40f3-126">Requirement</span></span> | <span data-ttu-id="c40f3-127">值</span><span class="sxs-lookup"><span data-stu-id="c40f3-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c40f3-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c40f3-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c40f3-129">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c40f3-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="c40f3-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c40f3-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c40f3-131">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c40f3-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="c40f3-132">標頭</span><span class="sxs-lookup"><span data-stu-id="c40f3-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="c40f3-133"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="c40f3-133"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="c40f3-134">程式庫</span><span class="sxs-lookup"><span data-stu-id="c40f3-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="c40f3-135"><dt>Nmapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c40f3-135"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="c40f3-136">DLL</span><span class="sxs-lookup"><span data-stu-id="c40f3-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c40f3-137"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c40f3-137"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




