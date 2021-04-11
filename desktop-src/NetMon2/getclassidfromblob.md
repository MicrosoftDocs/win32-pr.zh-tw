---
description: GetClassIDFromBlob 函式會從 BLOB 抓取命名類別識別碼值。
ms.assetid: fef29a42-ccd3-4655-958c-d150e5bcd0d7
title: 'GetClassIDFromBlob 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetClassIDFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 70122422c47a986058322ca8d17082093e02a4b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112228"
---
# <a name="getclassidfromblob-function"></a><span data-ttu-id="3b453-103">GetClassIDFromBlob 函式</span><span class="sxs-lookup"><span data-stu-id="3b453-103">GetClassIDFromBlob function</span></span>

<span data-ttu-id="3b453-104">**GetClassIDFromBlob** 函式會從 BLOB 抓取命名類別識別碼值。</span><span class="sxs-lookup"><span data-stu-id="3b453-104">The **GetClassIDFromBlob** function retrieves a named class identifier value from a BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b453-105">語法</span><span class="sxs-lookup"><span data-stu-id="3b453-105">Syntax</span></span>


```C++
DWORD GetClassIDFromBlob(
  _In_        HBLOB hBlob,
  _In_  const char  *pOwnerName,
  _In_  const char  *pCategoryName,
  _In_  const char  *pTagName,
  _Out_       CLSID *pClsID
);
```



## <a name="parameters"></a><span data-ttu-id="3b453-106">參數</span><span class="sxs-lookup"><span data-stu-id="3b453-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b453-107">*hBlob* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3b453-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b453-108">BLOB 的控制碼。</span><span class="sxs-lookup"><span data-stu-id="3b453-108">Handle to a BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="3b453-109">*pOwnerName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3b453-109">*pOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b453-110">BLOB 擁有者名稱的指標。</span><span class="sxs-lookup"><span data-stu-id="3b453-110">Pointer to the BLOB owner name.</span></span>

</dd> <dt>

<span data-ttu-id="3b453-111">*pCategoryName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3b453-111">*pCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b453-112">BLOB 類別目錄名稱的指標。</span><span class="sxs-lookup"><span data-stu-id="3b453-112">Pointer to the BLOB category name.</span></span>

</dd> <dt>

<span data-ttu-id="3b453-113">*pTagName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3b453-113">*pTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b453-114">BLOB 標記名稱的指標。</span><span class="sxs-lookup"><span data-stu-id="3b453-114">Pointer to the BLOB tag name.</span></span>

</dd> <dt>

<span data-ttu-id="3b453-115">*pClsID* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="3b453-115">*pClsID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3b453-116">BLOB 類別識別碼的指標。</span><span class="sxs-lookup"><span data-stu-id="3b453-116">Pointer to the BLOB class identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b453-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="3b453-117">Return value</span></span>

<span data-ttu-id="3b453-118">如果函式成功，則傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="3b453-118">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="3b453-119">如果函式不成功，則傳回值為描述錯誤的 NMERR 值。</span><span class="sxs-lookup"><span data-stu-id="3b453-119">If the function is unsuccessful, the return value is a NMERR value that describes the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b453-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="3b453-120">Requirements</span></span>



| <span data-ttu-id="3b453-121">需求</span><span class="sxs-lookup"><span data-stu-id="3b453-121">Requirement</span></span> | <span data-ttu-id="3b453-122">值</span><span class="sxs-lookup"><span data-stu-id="3b453-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b453-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3b453-123">Minimum supported client</span></span><br/> | <span data-ttu-id="3b453-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3b453-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="3b453-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3b453-125">Minimum supported server</span></span><br/> | <span data-ttu-id="3b453-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3b453-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3b453-127">標頭</span><span class="sxs-lookup"><span data-stu-id="3b453-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b453-128"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="3b453-128"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="3b453-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="3b453-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="3b453-130"><dt>Npptools .lib</dt></span><span class="sxs-lookup"><span data-stu-id="3b453-130"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="3b453-131">DLL</span><span class="sxs-lookup"><span data-stu-id="3b453-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b453-132"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b453-132"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b453-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3b453-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b453-134">SetClassIDInBlob</span><span class="sxs-lookup"><span data-stu-id="3b453-134">SetClassIDInBlob</span></span>](setclassidinblob.md)
</dt> <dt>

[<span data-ttu-id="3b453-135">GetBoolFromBlob</span><span class="sxs-lookup"><span data-stu-id="3b453-135">GetBoolFromBlob</span></span>](getboolfromblob.md)
</dt> <dt>

[<span data-ttu-id="3b453-136">GetDwordFromBlob</span><span class="sxs-lookup"><span data-stu-id="3b453-136">GetDwordFromBlob</span></span>](getdwordfromblob.md)
</dt> <dt>

[<span data-ttu-id="3b453-137">GetMacAddressFromBlob</span><span class="sxs-lookup"><span data-stu-id="3b453-137">GetMacAddressFromBlob</span></span>](getmacaddressfromblob.md)
</dt> <dt>

[<span data-ttu-id="3b453-138">GetNetworkInfoFromBlob</span><span class="sxs-lookup"><span data-stu-id="3b453-138">GetNetworkInfoFromBlob</span></span>](getnetworkinfofromblob.md)
</dt> <dt>

[<span data-ttu-id="3b453-139">GetNPPAddressFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="3b453-139">GetNPPAddressFilterFromBlob</span></span>](getnppaddressfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="3b453-140">GetNPPPatternFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="3b453-140">GetNPPPatternFilterFromBlob</span></span>](getnpppatternfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="3b453-141">GetNPPTriggerFromBlob</span><span class="sxs-lookup"><span data-stu-id="3b453-141">GetNPPTriggerFromBlob</span></span>](getnpptriggerfromblob.md)
</dt> <dt>

[<span data-ttu-id="3b453-142">GetStringFromBlob</span><span class="sxs-lookup"><span data-stu-id="3b453-142">GetStringFromBlob</span></span>](getstringfromblob.md)
</dt> <dt>

[<span data-ttu-id="3b453-143">GetStringsFromBlob</span><span class="sxs-lookup"><span data-stu-id="3b453-143">GetStringsFromBlob</span></span>](getstringsfromblob.md)
</dt> </dl>

 

 




