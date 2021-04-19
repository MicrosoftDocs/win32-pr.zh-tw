---
description: 從 BLOB 抓取已命名的布林值。
ms.assetid: 26acfd2a-5b17-47ad-8f7b-7793174a13c3
title: 'GetBoolFromBlob 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetBoolFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: e09a35f71181343cd401b3288c2b2c74a46f677b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986301"
---
# <a name="getboolfromblob-function"></a><span data-ttu-id="16715-103">GetBoolFromBlob 函式</span><span class="sxs-lookup"><span data-stu-id="16715-103">GetBoolFromBlob function</span></span>

<span data-ttu-id="16715-104">**GetBoolFromBlob** 函式會從 BLOB 抓取已命名的布林值。</span><span class="sxs-lookup"><span data-stu-id="16715-104">The **GetBoolFromBlob** function retrieves a named Boolean value from a BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="16715-105">語法</span><span class="sxs-lookup"><span data-stu-id="16715-105">Syntax</span></span>


```C++
DWORD GetBoolFromBlob(
  _In_        HBLOB hBlob,
  _In_  const char  *pOwnerName,
  _In_  const char  *pCategoryName,
  _In_  const char  *pTagName,
  _Out_       BOOL  *pBool
);
```



## <a name="parameters"></a><span data-ttu-id="16715-106">參數</span><span class="sxs-lookup"><span data-stu-id="16715-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16715-107">*hBlob* \[在\]</span><span class="sxs-lookup"><span data-stu-id="16715-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16715-108">BLOB 的控制碼。</span><span class="sxs-lookup"><span data-stu-id="16715-108">A handle to a BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="16715-109">*pOwnerName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="16715-109">*pOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16715-110">BLOB 擁有者名稱的指標。</span><span class="sxs-lookup"><span data-stu-id="16715-110">A pointer to the BLOB owner name.</span></span>

</dd> <dt>

<span data-ttu-id="16715-111">*pCategoryName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="16715-111">*pCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16715-112">BLOB 類別目錄名稱的指標。</span><span class="sxs-lookup"><span data-stu-id="16715-112">A pointer to the BLOB category name.</span></span>

</dd> <dt>

<span data-ttu-id="16715-113">*pTagName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="16715-113">*pTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16715-114">BLOB 標記名稱的指標。</span><span class="sxs-lookup"><span data-stu-id="16715-114">A pointer to the BLOB tag name.</span></span>

</dd> <dt>

<span data-ttu-id="16715-115">*pBool* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="16715-115">*pBool* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="16715-116">BLOB 布林值的指標。</span><span class="sxs-lookup"><span data-stu-id="16715-116">Pointer to the Boolean value of the BLOB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16715-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="16715-117">Return value</span></span>

<span data-ttu-id="16715-118">如果函式成功，則傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="16715-118">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="16715-119">如果函式不成功，則傳回值為描述錯誤的 NMERR 值。</span><span class="sxs-lookup"><span data-stu-id="16715-119">If the function is unsuccessful, the return value is a NMERR value that describes the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="16715-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="16715-120">Requirements</span></span>



| <span data-ttu-id="16715-121">需求</span><span class="sxs-lookup"><span data-stu-id="16715-121">Requirement</span></span> | <span data-ttu-id="16715-122">值</span><span class="sxs-lookup"><span data-stu-id="16715-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="16715-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="16715-123">Minimum supported client</span></span><br/> | <span data-ttu-id="16715-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="16715-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="16715-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="16715-125">Minimum supported server</span></span><br/> | <span data-ttu-id="16715-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="16715-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="16715-127">標頭</span><span class="sxs-lookup"><span data-stu-id="16715-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="16715-128"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="16715-128"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="16715-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="16715-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="16715-130"><dt>Npptools .lib</dt></span><span class="sxs-lookup"><span data-stu-id="16715-130"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="16715-131">DLL</span><span class="sxs-lookup"><span data-stu-id="16715-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="16715-132"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="16715-132"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16715-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="16715-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16715-134">SetBoolInBlob</span><span class="sxs-lookup"><span data-stu-id="16715-134">SetBoolInBlob</span></span>](setboolinblob.md)
</dt> <dt>

[<span data-ttu-id="16715-135">GetClassIDFromBlob</span><span class="sxs-lookup"><span data-stu-id="16715-135">GetClassIDFromBlob</span></span>](getclassidfromblob.md)
</dt> <dt>

[<span data-ttu-id="16715-136">GetDwordFromBlob</span><span class="sxs-lookup"><span data-stu-id="16715-136">GetDwordFromBlob</span></span>](getdwordfromblob.md)
</dt> <dt>

[<span data-ttu-id="16715-137">GetMacAddressFromBlob</span><span class="sxs-lookup"><span data-stu-id="16715-137">GetMacAddressFromBlob</span></span>](getmacaddressfromblob.md)
</dt> <dt>

[<span data-ttu-id="16715-138">GetNetworkInfoFromBlob</span><span class="sxs-lookup"><span data-stu-id="16715-138">GetNetworkInfoFromBlob</span></span>](getnetworkinfofromblob.md)
</dt> <dt>

[<span data-ttu-id="16715-139">GetNPPAddressFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="16715-139">GetNPPAddressFilterFromBlob</span></span>](getnppaddressfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="16715-140">GetNPPPatternFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="16715-140">GetNPPPatternFilterFromBlob</span></span>](getnpppatternfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="16715-141">GetNPPTriggerFromBlob</span><span class="sxs-lookup"><span data-stu-id="16715-141">GetNPPTriggerFromBlob</span></span>](getnpptriggerfromblob.md)
</dt> <dt>

[<span data-ttu-id="16715-142">GetStringFromBlob</span><span class="sxs-lookup"><span data-stu-id="16715-142">GetStringFromBlob</span></span>](getstringfromblob.md)
</dt> <dt>

[<span data-ttu-id="16715-143">GetStringsFromBlob</span><span class="sxs-lookup"><span data-stu-id="16715-143">GetStringsFromBlob</span></span>](getstringsfromblob.md)
</dt> </dl>

 

 




