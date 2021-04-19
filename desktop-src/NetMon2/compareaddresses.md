---
description: CompareAddresses 函式會比較兩個位址，表示其中一個位址大於、小於或等於其他位址。
ms.assetid: 76ff37d2-714f-4bac-adcc-eab78c8f25d3
title: 'CompareAddresses 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CompareAddresses
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: fd72ef0281615c0b56176e86ee9bb3659b498a0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980525"
---
# <a name="compareaddresses-function"></a><span data-ttu-id="61eff-103">CompareAddresses 函式</span><span class="sxs-lookup"><span data-stu-id="61eff-103">CompareAddresses function</span></span>

<span data-ttu-id="61eff-104">**CompareAddresses** 函式會比較兩個位址，表示其中一個位址大於、小於或等於其他位址。</span><span class="sxs-lookup"><span data-stu-id="61eff-104">The **CompareAddresses** function compares two addresses, indicating that one of the addresses is greater than, less than, or equal to the other address.</span></span>

## <a name="syntax"></a><span data-ttu-id="61eff-105">語法</span><span class="sxs-lookup"><span data-stu-id="61eff-105">Syntax</span></span>


```C++
int WINAPI CompareAddresses(
  _In_ LPADDRESS lpAddress1,
  _In_ LPADDRESS lpAddress2
);
```



## <a name="parameters"></a><span data-ttu-id="61eff-106">參數</span><span class="sxs-lookup"><span data-stu-id="61eff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61eff-107">*lpAddress1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="61eff-107">*lpAddress1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61eff-108">第一個位址的指標。</span><span class="sxs-lookup"><span data-stu-id="61eff-108">Pointer to the first address.</span></span>

</dd> <dt>

<span data-ttu-id="61eff-109">*lpAddress2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="61eff-109">*lpAddress2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61eff-110">第二個位址的指標。</span><span class="sxs-lookup"><span data-stu-id="61eff-110">Pointer to the second address.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61eff-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="61eff-111">Return value</span></span>

<span data-ttu-id="61eff-112">如果位址相同，則函數會傳回零。</span><span class="sxs-lookup"><span data-stu-id="61eff-112">If the addresses are the same, the function returns zero.</span></span>

<span data-ttu-id="61eff-113">如果 *lpAddress1* 參數指定的位址小於 *lpAddress2* 參數指定的位址，則傳回值為負數。</span><span class="sxs-lookup"><span data-stu-id="61eff-113">If the *lpAddress1* parameter specifies an address that is less than the address that the *lpAddress2* parameter specifies, the return value is a negative number.</span></span>

<span data-ttu-id="61eff-114">如果 *lpAddress1* 參數指定的位址大於 *lpAddress2* 參數指定的位址，則傳回值為正數。</span><span class="sxs-lookup"><span data-stu-id="61eff-114">If the *lpAddress1* parameter specifies an address that is greater than the address that the *lpAddress2* parameter specifies, the return value is a positive number.</span></span>

## <a name="remarks"></a><span data-ttu-id="61eff-115">備註</span><span class="sxs-lookup"><span data-stu-id="61eff-115">Remarks</span></span>

<span data-ttu-id="61eff-116">小於另一個位址的位址表示先前的畫面格。</span><span class="sxs-lookup"><span data-stu-id="61eff-116">An address that is less than another address indicates a previous frame.</span></span> <span data-ttu-id="61eff-117">大於另一個位址的位址表示較新的畫面格。</span><span class="sxs-lookup"><span data-stu-id="61eff-117">An address that is greater than another address indicates a later frame.</span></span>

<span data-ttu-id="61eff-118">網路監視器提供兩個其他函式： [CompareFrameDestAddress](compareframedestaddress.md) 和 [CompareFrameSourceAddress](compareframesourceaddress.md)，可供您用來比較位址。</span><span class="sxs-lookup"><span data-stu-id="61eff-118">Network Monitor provides two other functions, [CompareFrameDestAddress](compareframedestaddress.md) and [CompareFrameSourceAddress](compareframesourceaddress.md), which you can use to compare addresses.</span></span> <span data-ttu-id="61eff-119">**CompareFrameDestAddress** 函式會比較指定的位址與框架的目的地位址，而 **CompareFrameSourceAddress** 函式會比較指定的位址與框架的來源位址。</span><span class="sxs-lookup"><span data-stu-id="61eff-119">The **CompareFrameDestAddress** function compares a given address to the frame's destination address, and the **CompareFrameSourceAddress** function compares a given address to the frame's source address.</span></span>

## <a name="requirements"></a><span data-ttu-id="61eff-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="61eff-120">Requirements</span></span>



| <span data-ttu-id="61eff-121">需求</span><span class="sxs-lookup"><span data-stu-id="61eff-121">Requirement</span></span> | <span data-ttu-id="61eff-122">值</span><span class="sxs-lookup"><span data-stu-id="61eff-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="61eff-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="61eff-123">Minimum supported client</span></span><br/> | <span data-ttu-id="61eff-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="61eff-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="61eff-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="61eff-125">Minimum supported server</span></span><br/> | <span data-ttu-id="61eff-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="61eff-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="61eff-127">標頭</span><span class="sxs-lookup"><span data-stu-id="61eff-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="61eff-128"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="61eff-128"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="61eff-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="61eff-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="61eff-130"><dt>Nmapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="61eff-130"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="61eff-131">DLL</span><span class="sxs-lookup"><span data-stu-id="61eff-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61eff-132"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="61eff-132"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61eff-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="61eff-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61eff-134">CompareFrameDestAddress</span><span class="sxs-lookup"><span data-stu-id="61eff-134">CompareFrameDestAddress</span></span>](compareframedestaddress.md)
</dt> <dt>

[<span data-ttu-id="61eff-135">CompareFrameSourceAddress</span><span class="sxs-lookup"><span data-stu-id="61eff-135">CompareFrameSourceAddress</span></span>](compareframesourceaddress.md)
</dt> </dl>

 

 




