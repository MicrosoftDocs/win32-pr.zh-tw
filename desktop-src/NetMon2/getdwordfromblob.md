---
description: GetDwordFromBlob 函式會從 BLOB 抓取指名的 DWORD 值。
ms.assetid: edad74a7-b726-46d9-b49f-9984272d0a29
title: 'GetDwordFromBlob 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetDwordFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 064985f0f3b9a235dc1c00d683fe4b11371df87d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112224"
---
# <a name="getdwordfromblob-function"></a><span data-ttu-id="2b4ec-103">GetDwordFromBlob 函式</span><span class="sxs-lookup"><span data-stu-id="2b4ec-103">GetDwordFromBlob function</span></span>

<span data-ttu-id="2b4ec-104">**GetDwordFromBlob** 函式會從 BLOB 抓取指名的 **DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="2b4ec-104">The **GetDwordFromBlob** function retrieves the named **DWORD** value from a BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b4ec-105">語法</span><span class="sxs-lookup"><span data-stu-id="2b4ec-105">Syntax</span></span>


```C++
DWORD GetDwordFromBlob(
  _In_        HBLOB hBlob,
  _In_  const char  *pOwnerName,
  _In_  const char  *pCategoryName,
  _In_  const char  *pTagName,
  _Out_       DWORD *pDword
);
```



## <a name="parameters"></a><span data-ttu-id="2b4ec-106">參數</span><span class="sxs-lookup"><span data-stu-id="2b4ec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b4ec-107">*hBlob* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2b4ec-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b4ec-108">BLOB 的控制碼。</span><span class="sxs-lookup"><span data-stu-id="2b4ec-108">Handle to a BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="2b4ec-109">*pOwnerName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2b4ec-109">*pOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b4ec-110">BLOB 擁有者名稱的指標。</span><span class="sxs-lookup"><span data-stu-id="2b4ec-110">Pointer to the BLOB owner name.</span></span>

</dd> <dt>

<span data-ttu-id="2b4ec-111">*pCategoryName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2b4ec-111">*pCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b4ec-112">BLOB 類別目錄名稱的指標。</span><span class="sxs-lookup"><span data-stu-id="2b4ec-112">Pointer to the BLOB category name.</span></span>

</dd> <dt>

<span data-ttu-id="2b4ec-113">*pTagName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2b4ec-113">*pTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b4ec-114">BLOB 標記名稱的指標。</span><span class="sxs-lookup"><span data-stu-id="2b4ec-114">Pointer to the BLOB tag name.</span></span>

</dd> <dt>

<span data-ttu-id="2b4ec-115">*pDword* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="2b4ec-115">*pDword* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2b4ec-116">BLOB **DWORD** 值的指標。</span><span class="sxs-lookup"><span data-stu-id="2b4ec-116">Pointer to the **DWORD** value of the BLOB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b4ec-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="2b4ec-117">Return value</span></span>

<span data-ttu-id="2b4ec-118">如果函式成功，則傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="2b4ec-118">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="2b4ec-119">如果函式不成功，則傳回值為描述錯誤的 NMERR 值。</span><span class="sxs-lookup"><span data-stu-id="2b4ec-119">If the function is unsuccessful, the return value is a NMERR value that describes the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b4ec-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="2b4ec-120">Requirements</span></span>



| <span data-ttu-id="2b4ec-121">需求</span><span class="sxs-lookup"><span data-stu-id="2b4ec-121">Requirement</span></span> | <span data-ttu-id="2b4ec-122">值</span><span class="sxs-lookup"><span data-stu-id="2b4ec-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2b4ec-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2b4ec-123">Minimum supported client</span></span><br/> | <span data-ttu-id="2b4ec-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2b4ec-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="2b4ec-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2b4ec-125">Minimum supported server</span></span><br/> | <span data-ttu-id="2b4ec-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2b4ec-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2b4ec-127">標頭</span><span class="sxs-lookup"><span data-stu-id="2b4ec-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b4ec-128"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="2b4ec-128"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="2b4ec-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="2b4ec-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="2b4ec-130"><dt>Npptools .lib</dt></span><span class="sxs-lookup"><span data-stu-id="2b4ec-130"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="2b4ec-131">DLL</span><span class="sxs-lookup"><span data-stu-id="2b4ec-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b4ec-132"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b4ec-132"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b4ec-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2b4ec-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b4ec-134">SetDwordInBlob</span><span class="sxs-lookup"><span data-stu-id="2b4ec-134">SetDwordInBlob</span></span>](setdwordinblob.md)
</dt> <dt>

[<span data-ttu-id="2b4ec-135">GetBoolFromBlob</span><span class="sxs-lookup"><span data-stu-id="2b4ec-135">GetBoolFromBlob</span></span>](getboolfromblob.md)
</dt> <dt>

[<span data-ttu-id="2b4ec-136">GetClassIDFromBlob</span><span class="sxs-lookup"><span data-stu-id="2b4ec-136">GetClassIDFromBlob</span></span>](getclassidfromblob.md)
</dt> <dt>

[<span data-ttu-id="2b4ec-137">GetMacAddressFromBlob</span><span class="sxs-lookup"><span data-stu-id="2b4ec-137">GetMacAddressFromBlob</span></span>](getmacaddressfromblob.md)
</dt> <dt>

[<span data-ttu-id="2b4ec-138">GetNetworkInfoFromBlob</span><span class="sxs-lookup"><span data-stu-id="2b4ec-138">GetNetworkInfoFromBlob</span></span>](getnetworkinfofromblob.md)
</dt> <dt>

[<span data-ttu-id="2b4ec-139">GetNPPAddressFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="2b4ec-139">GetNPPAddressFilterFromBlob</span></span>](getnppaddressfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="2b4ec-140">GetNPPPatternFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="2b4ec-140">GetNPPPatternFilterFromBlob</span></span>](getnpppatternfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="2b4ec-141">GetNPPTriggerFromBlob</span><span class="sxs-lookup"><span data-stu-id="2b4ec-141">GetNPPTriggerFromBlob</span></span>](getnpptriggerfromblob.md)
</dt> <dt>

[<span data-ttu-id="2b4ec-142">GetStringFromBlob</span><span class="sxs-lookup"><span data-stu-id="2b4ec-142">GetStringFromBlob</span></span>](getstringfromblob.md)
</dt> <dt>

[<span data-ttu-id="2b4ec-143">GetStringsFromBlob</span><span class="sxs-lookup"><span data-stu-id="2b4ec-143">GetStringsFromBlob</span></span>](getstringsfromblob.md)
</dt> </dl>

 

 




