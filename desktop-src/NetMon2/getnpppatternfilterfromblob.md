---
description: GetNPPPatternFilterFromBlob 函式會從特定的 BLOB 抓取模式比對篩選。
ms.assetid: b17cde55-8abb-4699-960f-676cbbb24326
title: 'GetNPPPatternFilterFromBlob 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPPatternFilterFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 5758c53fe21231d300058a9168e556e9f9ceaa43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689719"
---
# <a name="getnpppatternfilterfromblob-function"></a><span data-ttu-id="3c8eb-103">GetNPPPatternFilterFromBlob 函式</span><span class="sxs-lookup"><span data-stu-id="3c8eb-103">GetNPPPatternFilterFromBlob function</span></span>

<span data-ttu-id="3c8eb-104">**GetNPPPatternFilterFromBlob** 函式會從特定的 BLOB 抓取模式比對篩選。</span><span class="sxs-lookup"><span data-stu-id="3c8eb-104">The **GetNPPPatternFilterFromBlob** function retrieves the pattern match filter from a specific BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c8eb-105">語法</span><span class="sxs-lookup"><span data-stu-id="3c8eb-105">Syntax</span></span>


```C++
DWORD GetNPPPatternFilterFromBlob(
  _In_  HBLOB        hBlob,
  _In_  LPEXPRESSION pExpression,
  _Out_ HBLOB        hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="3c8eb-106">參數</span><span class="sxs-lookup"><span data-stu-id="3c8eb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c8eb-107">*hBlob* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3c8eb-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c8eb-108">BLOB 的控制碼。</span><span class="sxs-lookup"><span data-stu-id="3c8eb-108">Handle to the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="3c8eb-109">*pExpression* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3c8eb-109">*pExpression* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c8eb-110">篩選條件運算式的指標。</span><span class="sxs-lookup"><span data-stu-id="3c8eb-110">Pointer to the filter expression.</span></span>

</dd> <dt>

<span data-ttu-id="3c8eb-111">*hErrorBlob* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="3c8eb-111">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3c8eb-112">錯誤 BLOB 的控制碼，指定發生任何) 時，在原始 BLOB 中的錯誤 (。</span><span class="sxs-lookup"><span data-stu-id="3c8eb-112">Handle to an error BLOB that specifies where in the original BLOB the error (if any) occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c8eb-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="3c8eb-113">Return value</span></span>

<span data-ttu-id="3c8eb-114">如果函式成功，則傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="3c8eb-114">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="3c8eb-115">如果函式不成功，則傳回值會是指出錯誤的 NMERR。</span><span class="sxs-lookup"><span data-stu-id="3c8eb-115">If the function is unsuccessful, the return value is a NMERR that indicates the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c8eb-116">備註</span><span class="sxs-lookup"><span data-stu-id="3c8eb-116">Remarks</span></span>

<span data-ttu-id="3c8eb-117">模式比對篩選資訊會儲存在 BLOB 的 **Config** 類別中。</span><span class="sxs-lookup"><span data-stu-id="3c8eb-117">The pattern match filter information is stored in the **Config** category of the BLOB.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c8eb-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="3c8eb-118">Requirements</span></span>



| <span data-ttu-id="3c8eb-119">需求</span><span class="sxs-lookup"><span data-stu-id="3c8eb-119">Requirement</span></span> | <span data-ttu-id="3c8eb-120">值</span><span class="sxs-lookup"><span data-stu-id="3c8eb-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3c8eb-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3c8eb-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3c8eb-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3c8eb-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="3c8eb-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3c8eb-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3c8eb-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3c8eb-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3c8eb-125">標頭</span><span class="sxs-lookup"><span data-stu-id="3c8eb-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c8eb-126"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="3c8eb-126"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="3c8eb-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="3c8eb-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="3c8eb-128"><dt>Npptools .lib</dt></span><span class="sxs-lookup"><span data-stu-id="3c8eb-128"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="3c8eb-129">DLL</span><span class="sxs-lookup"><span data-stu-id="3c8eb-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c8eb-130"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c8eb-130"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c8eb-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3c8eb-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c8eb-132">SetNPPPatternFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="3c8eb-132">SetNPPPatternFilterInBlob</span></span>](setnpppatternfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="3c8eb-133">GetBoolFromBlob</span><span class="sxs-lookup"><span data-stu-id="3c8eb-133">GetBoolFromBlob</span></span>](getboolfromblob.md)
</dt> <dt>

[<span data-ttu-id="3c8eb-134">GetClassIDFromBlob</span><span class="sxs-lookup"><span data-stu-id="3c8eb-134">GetClassIDFromBlob</span></span>](getclassidfromblob.md)
</dt> <dt>

[<span data-ttu-id="3c8eb-135">GetDwordFromBlob</span><span class="sxs-lookup"><span data-stu-id="3c8eb-135">GetDwordFromBlob</span></span>](getdwordfromblob.md)
</dt> <dt>

[<span data-ttu-id="3c8eb-136">GetMacAddressFromBlob</span><span class="sxs-lookup"><span data-stu-id="3c8eb-136">GetMacAddressFromBlob</span></span>](getmacaddressfromblob.md)
</dt> <dt>

[<span data-ttu-id="3c8eb-137">GetNetworkInfoFromBlob</span><span class="sxs-lookup"><span data-stu-id="3c8eb-137">GetNetworkInfoFromBlob</span></span>](getnetworkinfofromblob.md)
</dt> <dt>

[<span data-ttu-id="3c8eb-138">GetNPPAddressFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="3c8eb-138">GetNPPAddressFilterFromBlob</span></span>](getnppaddressfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="3c8eb-139">GetNPPTriggerFromBlob</span><span class="sxs-lookup"><span data-stu-id="3c8eb-139">GetNPPTriggerFromBlob</span></span>](getnpptriggerfromblob.md)
</dt> <dt>

[<span data-ttu-id="3c8eb-140">GetStringFromBlob</span><span class="sxs-lookup"><span data-stu-id="3c8eb-140">GetStringFromBlob</span></span>](getstringfromblob.md)
</dt> <dt>

[<span data-ttu-id="3c8eb-141">GetStringsFromBlob</span><span class="sxs-lookup"><span data-stu-id="3c8eb-141">GetStringsFromBlob</span></span>](getstringsfromblob.md)
</dt> </dl>

 

 




