---
description: 設定 BLOB 模式符合篩選。
ms.assetid: 44e7c67a-f430-4d68-bc7f-f6bbd5b9e5a9
title: 'SetNPPPatternFilterInBlob 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetNPPPatternFilterInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: b2e8989264a042368b37926bbb502f48ab2fb04b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511828"
---
# <a name="setnpppatternfilterinblob-function"></a><span data-ttu-id="46923-103">SetNPPPatternFilterInBlob 函式</span><span class="sxs-lookup"><span data-stu-id="46923-103">SetNPPPatternFilterInBlob function</span></span>

<span data-ttu-id="46923-104">**SetNPPPatternFilterInBlob** 函數會設定 BLOB 模式比對篩選。</span><span class="sxs-lookup"><span data-stu-id="46923-104">The **SetNPPPatternFilterInBlob** function sets the BLOB pattern match filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="46923-105">語法</span><span class="sxs-lookup"><span data-stu-id="46923-105">Syntax</span></span>


```C++
DWORD SetNPPPatternFilterInBlob(
  _In_  HBLOB        hBlob,
  _In_  LPEXPRESSION pExpression,
  _Out_ HBLOB        hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="46923-106">參數</span><span class="sxs-lookup"><span data-stu-id="46923-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46923-107">*hBlob* \[在\]</span><span class="sxs-lookup"><span data-stu-id="46923-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46923-108">BLOB 的控制碼。</span><span class="sxs-lookup"><span data-stu-id="46923-108">The handle to the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="46923-109">*pExpression* \[在\]</span><span class="sxs-lookup"><span data-stu-id="46923-109">*pExpression* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46923-110">[運算式](expression.md)結構的指標，此結構會定義要設定的篩選運算式。</span><span class="sxs-lookup"><span data-stu-id="46923-110">A pointer to an [EXPRESSION](expression.md) structure that defines the filter expression being set.</span></span>

</dd> <dt>

<span data-ttu-id="46923-111">*hErrorBlob* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="46923-111">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="46923-112">錯誤 BLOB 的控制碼，指定當發生任何) 時，原始 BLOB 中的錯誤 (。</span><span class="sxs-lookup"><span data-stu-id="46923-112">The handle to an error BLOB that specifies where in the original BLOB the error (if any) occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46923-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="46923-113">Return value</span></span>

<span data-ttu-id="46923-114">如果 **SetNPPPatternFilterInBlob** 函式成功，則傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="46923-114">If the **SetNPPPatternFilterInBlob** function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="46923-115">如果函式不成功，則傳回值會是指出錯誤的 NMERR 值。</span><span class="sxs-lookup"><span data-stu-id="46923-115">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="46923-116">備註</span><span class="sxs-lookup"><span data-stu-id="46923-116">Remarks</span></span>

<span data-ttu-id="46923-117">模式會比對儲存在 BLOB 之 **Config** 分類中的篩選資料。</span><span class="sxs-lookup"><span data-stu-id="46923-117">The pattern match filter data stored in the **Config** category of the BLOB.</span></span>

## <a name="requirements"></a><span data-ttu-id="46923-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="46923-118">Requirements</span></span>



| <span data-ttu-id="46923-119">需求</span><span class="sxs-lookup"><span data-stu-id="46923-119">Requirement</span></span> | <span data-ttu-id="46923-120">值</span><span class="sxs-lookup"><span data-stu-id="46923-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="46923-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="46923-121">Minimum supported client</span></span><br/> | <span data-ttu-id="46923-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="46923-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="46923-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="46923-123">Minimum supported server</span></span><br/> | <span data-ttu-id="46923-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="46923-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="46923-125">標頭</span><span class="sxs-lookup"><span data-stu-id="46923-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="46923-126"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="46923-126"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="46923-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="46923-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="46923-128"><dt>Npptools .lib</dt></span><span class="sxs-lookup"><span data-stu-id="46923-128"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="46923-129">DLL</span><span class="sxs-lookup"><span data-stu-id="46923-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46923-130"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="46923-130"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46923-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="46923-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46923-132">GetNPPAddressFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="46923-132">GetNPPAddressFilterFromBlob</span></span>](getnppaddressfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="46923-133">SetBoolInBlob</span><span class="sxs-lookup"><span data-stu-id="46923-133">SetBoolInBlob</span></span>](setboolinblob.md)
</dt> <dt>

[<span data-ttu-id="46923-134">SetClassIDInBlob</span><span class="sxs-lookup"><span data-stu-id="46923-134">SetClassIDInBlob</span></span>](setclassidinblob.md)
</dt> <dt>

[<span data-ttu-id="46923-135">SetDwordInBlob</span><span class="sxs-lookup"><span data-stu-id="46923-135">SetDwordInBlob</span></span>](setdwordinblob.md)
</dt> <dt>

[<span data-ttu-id="46923-136">SetMacAddressInBlob</span><span class="sxs-lookup"><span data-stu-id="46923-136">SetMacAddressInBlob</span></span>](setmacaddressinblob.md)
</dt> <dt>

[<span data-ttu-id="46923-137">SetNetworkInfoInBlob</span><span class="sxs-lookup"><span data-stu-id="46923-137">SetNetworkInfoInBlob</span></span>](setnetworkinfoinblob.md)
</dt> <dt>

[<span data-ttu-id="46923-138">SetNPPAddressFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="46923-138">SetNPPAddressFilterInBlob</span></span>](setnppaddressfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="46923-139">SetNPPTriggerInBlob</span><span class="sxs-lookup"><span data-stu-id="46923-139">SetNPPTriggerInBlob</span></span>](setnpptriggerinblob.md)
</dt> <dt>

[<span data-ttu-id="46923-140">SetStringInBlob</span><span class="sxs-lookup"><span data-stu-id="46923-140">SetStringInBlob</span></span>](setstringinblob.md)
</dt> </dl>

 

 




