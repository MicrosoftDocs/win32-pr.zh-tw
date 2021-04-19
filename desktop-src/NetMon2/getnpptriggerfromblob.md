---
description: GetNPPTriggerFromBlob 函式會從指定的 BLOB 抓取觸發程式。
ms.assetid: 48a27cf3-57b0-4241-a925-4209e0d384e2
title: 'GetNPPTriggerFromBlob 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPTriggerFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 11622078354012de4796ddd43a698ac812951742
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106967085"
---
# <a name="getnpptriggerfromblob-function"></a><span data-ttu-id="6ef24-103">GetNPPTriggerFromBlob 函式</span><span class="sxs-lookup"><span data-stu-id="6ef24-103">GetNPPTriggerFromBlob function</span></span>

<span data-ttu-id="6ef24-104">**GetNPPTriggerFromBlob** 函式會從指定的 BLOB 抓取觸發程式。</span><span class="sxs-lookup"><span data-stu-id="6ef24-104">The **GetNPPTriggerFromBlob** function retrieves the trigger from the given BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ef24-105">語法</span><span class="sxs-lookup"><span data-stu-id="6ef24-105">Syntax</span></span>


```C++
DWORD GetNPPTriggerFromBlob(
  _In_  HBLOB     hBlob,
  _Out_ LPTRIGGER pTrigger,
  _Out_ HBLOB     hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="6ef24-106">參數</span><span class="sxs-lookup"><span data-stu-id="6ef24-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ef24-107">*hBlob* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6ef24-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ef24-108">BLOB 的控制碼。</span><span class="sxs-lookup"><span data-stu-id="6ef24-108">Handle to the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="6ef24-109">*pTrigger* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6ef24-109">*pTrigger* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6ef24-110">觸發程式值的指標。</span><span class="sxs-lookup"><span data-stu-id="6ef24-110">Pointer to the trigger value.</span></span>

</dd> <dt>

<span data-ttu-id="6ef24-111">*hErrorBlob* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6ef24-111">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6ef24-112">錯誤 BLOB 的控制碼，指定發生任何) 時，在原始 BLOB 中的錯誤 (。</span><span class="sxs-lookup"><span data-stu-id="6ef24-112">Handle to an error BLOB that specifies where in the original BLOB the error (if any) occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ef24-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="6ef24-113">Return value</span></span>

<span data-ttu-id="6ef24-114">如果函式成功，則傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="6ef24-114">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="6ef24-115">如果函式不成功，則傳回值會是指出錯誤的 NMERR 值。</span><span class="sxs-lookup"><span data-stu-id="6ef24-115">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ef24-116">備註</span><span class="sxs-lookup"><span data-stu-id="6ef24-116">Remarks</span></span>

<span data-ttu-id="6ef24-117">觸發程式資訊會儲存在 BLOB 的 **觸發** 程式類別中。</span><span class="sxs-lookup"><span data-stu-id="6ef24-117">The trigger information is stored in the **Trigger** category of the BLOB.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ef24-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="6ef24-118">Requirements</span></span>



| <span data-ttu-id="6ef24-119">需求</span><span class="sxs-lookup"><span data-stu-id="6ef24-119">Requirement</span></span> | <span data-ttu-id="6ef24-120">值</span><span class="sxs-lookup"><span data-stu-id="6ef24-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ef24-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6ef24-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6ef24-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6ef24-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="6ef24-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6ef24-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6ef24-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6ef24-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6ef24-125">標頭</span><span class="sxs-lookup"><span data-stu-id="6ef24-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ef24-126"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="6ef24-126"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="6ef24-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="6ef24-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="6ef24-128"><dt>Npptools .lib</dt></span><span class="sxs-lookup"><span data-stu-id="6ef24-128"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="6ef24-129">DLL</span><span class="sxs-lookup"><span data-stu-id="6ef24-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ef24-130"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ef24-130"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ef24-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6ef24-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ef24-132">GetBoolFromBlob</span><span class="sxs-lookup"><span data-stu-id="6ef24-132">GetBoolFromBlob</span></span>](getboolfromblob.md)
</dt> <dt>

[<span data-ttu-id="6ef24-133">GetClassIDFromBlob</span><span class="sxs-lookup"><span data-stu-id="6ef24-133">GetClassIDFromBlob</span></span>](getclassidfromblob.md)
</dt> <dt>

[<span data-ttu-id="6ef24-134">GetDwordFromBlob</span><span class="sxs-lookup"><span data-stu-id="6ef24-134">GetDwordFromBlob</span></span>](getdwordfromblob.md)
</dt> <dt>

[<span data-ttu-id="6ef24-135">GetMacAddressFromBlob</span><span class="sxs-lookup"><span data-stu-id="6ef24-135">GetMacAddressFromBlob</span></span>](getmacaddressfromblob.md)
</dt> <dt>

[<span data-ttu-id="6ef24-136">GetNetworkInfoFromBlob</span><span class="sxs-lookup"><span data-stu-id="6ef24-136">GetNetworkInfoFromBlob</span></span>](getnetworkinfofromblob.md)
</dt> <dt>

[<span data-ttu-id="6ef24-137">GetNPPAddressFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="6ef24-137">GetNPPAddressFilterFromBlob</span></span>](getnppaddressfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="6ef24-138">GetNPPPatternFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="6ef24-138">GetNPPPatternFilterFromBlob</span></span>](getnpppatternfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="6ef24-139">GetStringFromBlob</span><span class="sxs-lookup"><span data-stu-id="6ef24-139">GetStringFromBlob</span></span>](getstringfromblob.md)
</dt> <dt>

[<span data-ttu-id="6ef24-140">GetStringsFromBlob</span><span class="sxs-lookup"><span data-stu-id="6ef24-140">GetStringsFromBlob</span></span>](getstringsfromblob.md)
</dt> </dl>

 

 




