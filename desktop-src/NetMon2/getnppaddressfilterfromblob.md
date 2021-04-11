---
description: GetNPPAddressFilterFromBlob 函式會使用儲存在 BLOB 中的資訊來填滿指定的位址篩選準則。
ms.assetid: b34e0e52-1b2a-4d61-b60c-f1b19ff8ff38
title: 'GetNPPAddressFilterFromBlob 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPAddressFilterFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 944821620123d63f654e286a77018232c79981e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945133"
---
# <a name="getnppaddressfilterfromblob-function"></a><span data-ttu-id="74c0a-103">GetNPPAddressFilterFromBlob 函式</span><span class="sxs-lookup"><span data-stu-id="74c0a-103">GetNPPAddressFilterFromBlob function</span></span>

<span data-ttu-id="74c0a-104">**GetNPPAddressFilterFromBlob** 函式會使用儲存在 BLOB 中的資訊來填滿指定的位址篩選準則。</span><span class="sxs-lookup"><span data-stu-id="74c0a-104">The **GetNPPAddressFilterFromBlob** function fills in the given address filter with information stored in the BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="74c0a-105">語法</span><span class="sxs-lookup"><span data-stu-id="74c0a-105">Syntax</span></span>


```C++
DWORD GetNPPAddressFilterFromBlob(
  _In_    HBLOB          hBlob,
  _Inout_ LPADDRESSTABLE pAddressTable,
  _Out_   HBLOB          hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="74c0a-106">參數</span><span class="sxs-lookup"><span data-stu-id="74c0a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74c0a-107">*hBlob* \[在\]</span><span class="sxs-lookup"><span data-stu-id="74c0a-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74c0a-108">BLOB 的控制碼。</span><span class="sxs-lookup"><span data-stu-id="74c0a-108">Handle to a BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="74c0a-109">*pAddressTable* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="74c0a-109">*pAddressTable* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="74c0a-110">使用者配置的位址資料表指標。</span><span class="sxs-lookup"><span data-stu-id="74c0a-110">Pointer to the user-allocated address table.</span></span>

</dd> <dt>

<span data-ttu-id="74c0a-111">*hErrorBlob* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="74c0a-111">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="74c0a-112">錯誤 BLOB 的控制碼，指定發生任何) 時，在原始 BLOB 中的錯誤 (。</span><span class="sxs-lookup"><span data-stu-id="74c0a-112">Handle to an error BLOB that specifies where in the original BLOB the error (if any) occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74c0a-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="74c0a-113">Return value</span></span>

<span data-ttu-id="74c0a-114">如果函式成功，則傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="74c0a-114">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="74c0a-115">如果函式不成功，則傳回值為描述錯誤的 NMERR 值。</span><span class="sxs-lookup"><span data-stu-id="74c0a-115">If the function is unsuccessful, the return value is a NMERR value that describes the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="74c0a-116">備註</span><span class="sxs-lookup"><span data-stu-id="74c0a-116">Remarks</span></span>

<span data-ttu-id="74c0a-117">位址資訊會儲存在 [BLOB NPP **擁有** 者] 類別的 [ **Config** ] 區段中。</span><span class="sxs-lookup"><span data-stu-id="74c0a-117">The address information is stored in the **Config** section of the BLOB NPP **Owner** category.</span></span>

## <a name="requirements"></a><span data-ttu-id="74c0a-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="74c0a-118">Requirements</span></span>



| <span data-ttu-id="74c0a-119">需求</span><span class="sxs-lookup"><span data-stu-id="74c0a-119">Requirement</span></span> | <span data-ttu-id="74c0a-120">值</span><span class="sxs-lookup"><span data-stu-id="74c0a-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="74c0a-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="74c0a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="74c0a-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="74c0a-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="74c0a-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="74c0a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="74c0a-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="74c0a-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="74c0a-125">標頭</span><span class="sxs-lookup"><span data-stu-id="74c0a-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="74c0a-126"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="74c0a-126"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="74c0a-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="74c0a-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="74c0a-128"><dt>Npptools .lib</dt></span><span class="sxs-lookup"><span data-stu-id="74c0a-128"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="74c0a-129">DLL</span><span class="sxs-lookup"><span data-stu-id="74c0a-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74c0a-130"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="74c0a-130"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74c0a-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="74c0a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74c0a-132">SetNPPAddressFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="74c0a-132">SetNPPAddressFilterInBlob</span></span>](setnppaddressfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="74c0a-133">GetBoolFromBlob</span><span class="sxs-lookup"><span data-stu-id="74c0a-133">GetBoolFromBlob</span></span>](getboolfromblob.md)
</dt> <dt>

[<span data-ttu-id="74c0a-134">GetClassIDFromBlob</span><span class="sxs-lookup"><span data-stu-id="74c0a-134">GetClassIDFromBlob</span></span>](getclassidfromblob.md)
</dt> <dt>

[<span data-ttu-id="74c0a-135">GetDwordFromBlob</span><span class="sxs-lookup"><span data-stu-id="74c0a-135">GetDwordFromBlob</span></span>](getdwordfromblob.md)
</dt> <dt>

[<span data-ttu-id="74c0a-136">GetMacAddressFromBlob</span><span class="sxs-lookup"><span data-stu-id="74c0a-136">GetMacAddressFromBlob</span></span>](getmacaddressfromblob.md)
</dt> <dt>

[<span data-ttu-id="74c0a-137">GetNetworkInfoFromBlob</span><span class="sxs-lookup"><span data-stu-id="74c0a-137">GetNetworkInfoFromBlob</span></span>](getnetworkinfofromblob.md)
</dt> <dt>

[<span data-ttu-id="74c0a-138">GetNPPPatternFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="74c0a-138">GetNPPPatternFilterFromBlob</span></span>](getnpppatternfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="74c0a-139">GetNPPTriggerFromBlob</span><span class="sxs-lookup"><span data-stu-id="74c0a-139">GetNPPTriggerFromBlob</span></span>](getnpptriggerfromblob.md)
</dt> <dt>

[<span data-ttu-id="74c0a-140">GetStringFromBlob</span><span class="sxs-lookup"><span data-stu-id="74c0a-140">GetStringFromBlob</span></span>](getstringfromblob.md)
</dt> <dt>

[<span data-ttu-id="74c0a-141">GetStringsFromBlob</span><span class="sxs-lookup"><span data-stu-id="74c0a-141">GetStringsFromBlob</span></span>](getstringsfromblob.md)
</dt> </dl>

 

 




