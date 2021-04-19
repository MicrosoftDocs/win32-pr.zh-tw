---
description: GetMacAddressFromBlob 函式會從 BLOB 取出命名的 MAC 位址。
ms.assetid: 1769c92c-0946-447c-885a-fcf175fa1bf3
title: 'GetMacAddressFromBlob 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetMacAddressFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 022d4f618c09652c368f6664b194b4ebafc81717
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107001431"
---
# <a name="getmacaddressfromblob-function"></a><span data-ttu-id="2b03c-103">GetMacAddressFromBlob 函式</span><span class="sxs-lookup"><span data-stu-id="2b03c-103">GetMacAddressFromBlob function</span></span>

<span data-ttu-id="2b03c-104">**GetMacAddressFromBlob** 函式會從 BLOB 取出命名的 MAC 位址。</span><span class="sxs-lookup"><span data-stu-id="2b03c-104">The **GetMacAddressFromBlob** function retrieves the named MAC address from a BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b03c-105">語法</span><span class="sxs-lookup"><span data-stu-id="2b03c-105">Syntax</span></span>


```C++
DWORD GetMacAddressFromBlob(
  _In_        HBLOB hBlob,
  _In_  const char  *pOwnerName,
  _In_  const char  *pCategoryName,
  _In_  const char  *pTagName,
  _Out_       BYTE  *pMacAddress
);
```



## <a name="parameters"></a><span data-ttu-id="2b03c-106">參數</span><span class="sxs-lookup"><span data-stu-id="2b03c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b03c-107">*hBlob* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2b03c-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b03c-108">BLOB 的控制碼。</span><span class="sxs-lookup"><span data-stu-id="2b03c-108">Handle to a BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="2b03c-109">*pOwnerName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2b03c-109">*pOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b03c-110">BLOB 擁有者名稱的指標。</span><span class="sxs-lookup"><span data-stu-id="2b03c-110">Pointer to the BLOB owner name.</span></span>

</dd> <dt>

<span data-ttu-id="2b03c-111">*pCategoryName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2b03c-111">*pCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b03c-112">BLOB 類別目錄名稱的指標。</span><span class="sxs-lookup"><span data-stu-id="2b03c-112">Pointer to the BLOB category name.</span></span>

</dd> <dt>

<span data-ttu-id="2b03c-113">*pTagName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2b03c-113">*pTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b03c-114">BLOB 標記名稱的指標。</span><span class="sxs-lookup"><span data-stu-id="2b03c-114">Pointer to the BLOB tag name.</span></span>

</dd> <dt>

<span data-ttu-id="2b03c-115">*pMacAddress* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="2b03c-115">*pMacAddress* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2b03c-116">BLOB 的 MAC 位址指標。</span><span class="sxs-lookup"><span data-stu-id="2b03c-116">Pointer to the MAC address of the BLOB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b03c-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="2b03c-117">Return value</span></span>

<span data-ttu-id="2b03c-118">如果函式成功，則傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="2b03c-118">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="2b03c-119">如果函式不成功，則傳回值為描述錯誤的 NMERR 值。</span><span class="sxs-lookup"><span data-stu-id="2b03c-119">If the function is unsuccessful, the return value is a NMERR value that describes the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b03c-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="2b03c-120">Requirements</span></span>



| <span data-ttu-id="2b03c-121">需求</span><span class="sxs-lookup"><span data-stu-id="2b03c-121">Requirement</span></span> | <span data-ttu-id="2b03c-122">值</span><span class="sxs-lookup"><span data-stu-id="2b03c-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2b03c-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2b03c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="2b03c-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2b03c-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="2b03c-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2b03c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="2b03c-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2b03c-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2b03c-127">標頭</span><span class="sxs-lookup"><span data-stu-id="2b03c-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b03c-128"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="2b03c-128"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="2b03c-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="2b03c-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="2b03c-130"><dt>Npptools .lib</dt></span><span class="sxs-lookup"><span data-stu-id="2b03c-130"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="2b03c-131">DLL</span><span class="sxs-lookup"><span data-stu-id="2b03c-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b03c-132"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b03c-132"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b03c-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2b03c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b03c-134">SetMacAddressInBlob</span><span class="sxs-lookup"><span data-stu-id="2b03c-134">SetMacAddressInBlob</span></span>](setmacaddressinblob.md)
</dt> <dt>

[<span data-ttu-id="2b03c-135">GetBoolFromBlob</span><span class="sxs-lookup"><span data-stu-id="2b03c-135">GetBoolFromBlob</span></span>](getboolfromblob.md)
</dt> <dt>

[<span data-ttu-id="2b03c-136">GetClassIDFromBlob</span><span class="sxs-lookup"><span data-stu-id="2b03c-136">GetClassIDFromBlob</span></span>](getclassidfromblob.md)
</dt> <dt>

[<span data-ttu-id="2b03c-137">GetDwordFromBlob</span><span class="sxs-lookup"><span data-stu-id="2b03c-137">GetDwordFromBlob</span></span>](getdwordfromblob.md)
</dt> <dt>

[<span data-ttu-id="2b03c-138">GetNetworkInfoFromBlob</span><span class="sxs-lookup"><span data-stu-id="2b03c-138">GetNetworkInfoFromBlob</span></span>](getnetworkinfofromblob.md)
</dt> <dt>

[<span data-ttu-id="2b03c-139">GetNPPAddressFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="2b03c-139">GetNPPAddressFilterFromBlob</span></span>](getnppaddressfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="2b03c-140">GetNPPPatternFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="2b03c-140">GetNPPPatternFilterFromBlob</span></span>](getnpppatternfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="2b03c-141">GetNPPTriggerFromBlob</span><span class="sxs-lookup"><span data-stu-id="2b03c-141">GetNPPTriggerFromBlob</span></span>](getnpptriggerfromblob.md)
</dt> <dt>

[<span data-ttu-id="2b03c-142">GetStringFromBlob</span><span class="sxs-lookup"><span data-stu-id="2b03c-142">GetStringFromBlob</span></span>](getstringfromblob.md)
</dt> <dt>

[<span data-ttu-id="2b03c-143">GetStringsFromBlob</span><span class="sxs-lookup"><span data-stu-id="2b03c-143">GetStringsFromBlob</span></span>](getstringsfromblob.md)
</dt> </dl>

 

 




