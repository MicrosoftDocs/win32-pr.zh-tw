---
description: SetNPPAddressFilterInBlob 函式會在 BLOB 中設定指定的位址篩選準則。
ms.assetid: bdd1482d-8be0-4999-9a7a-16b0400412fb
title: 'SetNPPAddressFilterInBlob 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetNPPAddressFilterInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 39e8a85599fa63b1320d707f648731a195dbb48e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984743"
---
# <a name="setnppaddressfilterinblob-function"></a><span data-ttu-id="14e06-103">SetNPPAddressFilterInBlob 函式</span><span class="sxs-lookup"><span data-stu-id="14e06-103">SetNPPAddressFilterInBlob function</span></span>

<span data-ttu-id="14e06-104">**SetNPPAddressFilterInBlob** 函式會在 BLOB 中設定指定的位址篩選準則。</span><span class="sxs-lookup"><span data-stu-id="14e06-104">The **SetNPPAddressFilterInBlob** function sets the given address filter in the BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="14e06-105">語法</span><span class="sxs-lookup"><span data-stu-id="14e06-105">Syntax</span></span>


```C++
DWORD SetNPPAddressFilterInBlob(
  _In_ HBLOB          hBlob,
  _In_ LPADDRESSTABLE pAddressTable
);
```



## <a name="parameters"></a><span data-ttu-id="14e06-106">參數</span><span class="sxs-lookup"><span data-stu-id="14e06-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14e06-107">*hBlob* \[在\]</span><span class="sxs-lookup"><span data-stu-id="14e06-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14e06-108">BLOB 的控制碼。</span><span class="sxs-lookup"><span data-stu-id="14e06-108">Handle to a BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="14e06-109">*pAddressTable* \[在\]</span><span class="sxs-lookup"><span data-stu-id="14e06-109">*pAddressTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14e06-110">[**ADDRESSTABLE**](addresstable.md)結構的指標，該結構定義使用者配置的位址資料表。</span><span class="sxs-lookup"><span data-stu-id="14e06-110">Pointer to an [**ADDRESSTABLE**](addresstable.md) structure that defines the user-allocated address table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14e06-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="14e06-111">Return value</span></span>

<span data-ttu-id="14e06-112">如果函式成功，則傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="14e06-112">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="14e06-113">如果函式不成功，則傳回值會是指出錯誤的 NMERR 值。</span><span class="sxs-lookup"><span data-stu-id="14e06-113">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="14e06-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="14e06-114">Requirements</span></span>



| <span data-ttu-id="14e06-115">需求</span><span class="sxs-lookup"><span data-stu-id="14e06-115">Requirement</span></span> | <span data-ttu-id="14e06-116">值</span><span class="sxs-lookup"><span data-stu-id="14e06-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="14e06-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="14e06-117">Minimum supported client</span></span><br/> | <span data-ttu-id="14e06-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="14e06-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="14e06-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="14e06-119">Minimum supported server</span></span><br/> | <span data-ttu-id="14e06-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="14e06-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="14e06-121">標頭</span><span class="sxs-lookup"><span data-stu-id="14e06-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="14e06-122"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="14e06-122"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="14e06-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="14e06-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="14e06-124"><dt>Npptools .lib</dt></span><span class="sxs-lookup"><span data-stu-id="14e06-124"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="14e06-125">DLL</span><span class="sxs-lookup"><span data-stu-id="14e06-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="14e06-126"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14e06-126"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14e06-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="14e06-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14e06-128">GetNPPAddressFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="14e06-128">GetNPPAddressFilterFromBlob</span></span>](getnppaddressfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="14e06-129">SetBoolInBlob</span><span class="sxs-lookup"><span data-stu-id="14e06-129">SetBoolInBlob</span></span>](setboolinblob.md)
</dt> <dt>

[<span data-ttu-id="14e06-130">SetClassIDInBlob</span><span class="sxs-lookup"><span data-stu-id="14e06-130">SetClassIDInBlob</span></span>](setclassidinblob.md)
</dt> <dt>

[<span data-ttu-id="14e06-131">SetDwordInBlob</span><span class="sxs-lookup"><span data-stu-id="14e06-131">SetDwordInBlob</span></span>](setdwordinblob.md)
</dt> <dt>

[<span data-ttu-id="14e06-132">SetMacAddressInBlob</span><span class="sxs-lookup"><span data-stu-id="14e06-132">SetMacAddressInBlob</span></span>](setmacaddressinblob.md)
</dt> <dt>

[<span data-ttu-id="14e06-133">SetNetworkInfoInBlob</span><span class="sxs-lookup"><span data-stu-id="14e06-133">SetNetworkInfoInBlob</span></span>](setnetworkinfoinblob.md)
</dt> <dt>

[<span data-ttu-id="14e06-134">SetNPPPatternFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="14e06-134">SetNPPPatternFilterInBlob</span></span>](setnpppatternfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="14e06-135">SetNPPTriggerInBlob</span><span class="sxs-lookup"><span data-stu-id="14e06-135">SetNPPTriggerInBlob</span></span>](setnpptriggerinblob.md)
</dt> <dt>

[<span data-ttu-id="14e06-136">SetStringInBlob</span><span class="sxs-lookup"><span data-stu-id="14e06-136">SetStringInBlob</span></span>](setstringinblob.md)
</dt> </dl>

 

 




