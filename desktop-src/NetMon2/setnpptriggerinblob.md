---
description: 設定 BLOB 觸發程式。
ms.assetid: 88bfd5cd-f563-4d0c-81a3-54a846805b87
title: 'SetNPPTriggerInBlob 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetNPPTriggerInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 05b8bb3f7f95dc3246ef10f3945b9ab0868550cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191487"
---
# <a name="setnpptriggerinblob-function"></a><span data-ttu-id="fdbe5-103">SetNPPTriggerInBlob 函式</span><span class="sxs-lookup"><span data-stu-id="fdbe5-103">SetNPPTriggerInBlob function</span></span>

<span data-ttu-id="fdbe5-104">**SetNPPTriggerInBlob** 函式會設定 BLOB 觸發程式。</span><span class="sxs-lookup"><span data-stu-id="fdbe5-104">The **SetNPPTriggerInBlob** function sets the BLOB trigger.</span></span>

## <a name="syntax"></a><span data-ttu-id="fdbe5-105">語法</span><span class="sxs-lookup"><span data-stu-id="fdbe5-105">Syntax</span></span>


```C++
DWORD SetNPPTriggerInBlob(
  _In_  HBLOB     hBlob,
  _In_  LPTRIGGER pTrigger,
  _Out_ HBLOB     hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="fdbe5-106">參數</span><span class="sxs-lookup"><span data-stu-id="fdbe5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fdbe5-107">*hBlob* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fdbe5-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fdbe5-108">BLOB 的控制碼。</span><span class="sxs-lookup"><span data-stu-id="fdbe5-108">The handle to the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="fdbe5-109">*pTrigger* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fdbe5-109">*pTrigger* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fdbe5-110">觸發程式值的指標。</span><span class="sxs-lookup"><span data-stu-id="fdbe5-110">A pointer to the trigger value.</span></span>

</dd> <dt>

<span data-ttu-id="fdbe5-111">*hErrorBlob* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="fdbe5-111">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fdbe5-112">錯誤 BLOB 的控制碼，指定當發生任何) 時，原始 BLOB 中的錯誤 (。</span><span class="sxs-lookup"><span data-stu-id="fdbe5-112">The handle to an error BLOB that specifies where in the original BLOB the error (if any) occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fdbe5-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="fdbe5-113">Return value</span></span>

<span data-ttu-id="fdbe5-114">如果函式成功，則傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="fdbe5-114">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="fdbe5-115">如果函式不成功，則傳回值會是指出錯誤的 NMERR 值。</span><span class="sxs-lookup"><span data-stu-id="fdbe5-115">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="fdbe5-116">備註</span><span class="sxs-lookup"><span data-stu-id="fdbe5-116">Remarks</span></span>

<span data-ttu-id="fdbe5-117">此觸發程式資料會儲存在 BLOB 的 **觸發** 程式類別中。</span><span class="sxs-lookup"><span data-stu-id="fdbe5-117">This trigger data is stored in the **Trigger** category of the BLOB.</span></span>

## <a name="requirements"></a><span data-ttu-id="fdbe5-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="fdbe5-118">Requirements</span></span>



| <span data-ttu-id="fdbe5-119">需求</span><span class="sxs-lookup"><span data-stu-id="fdbe5-119">Requirement</span></span> | <span data-ttu-id="fdbe5-120">值</span><span class="sxs-lookup"><span data-stu-id="fdbe5-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fdbe5-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fdbe5-121">Minimum supported client</span></span><br/> | <span data-ttu-id="fdbe5-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fdbe5-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="fdbe5-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fdbe5-123">Minimum supported server</span></span><br/> | <span data-ttu-id="fdbe5-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fdbe5-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fdbe5-125">標頭</span><span class="sxs-lookup"><span data-stu-id="fdbe5-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="fdbe5-126"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="fdbe5-126"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="fdbe5-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="fdbe5-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="fdbe5-128"><dt>Npptools .lib</dt></span><span class="sxs-lookup"><span data-stu-id="fdbe5-128"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="fdbe5-129">DLL</span><span class="sxs-lookup"><span data-stu-id="fdbe5-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fdbe5-130"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fdbe5-130"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fdbe5-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fdbe5-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdbe5-132">GetNPPTriggerFromBlob</span><span class="sxs-lookup"><span data-stu-id="fdbe5-132">GetNPPTriggerFromBlob</span></span>](getnpptriggerfromblob.md)
</dt> <dt>

[<span data-ttu-id="fdbe5-133">SetBoolInBlob</span><span class="sxs-lookup"><span data-stu-id="fdbe5-133">SetBoolInBlob</span></span>](setboolinblob.md)
</dt> <dt>

[<span data-ttu-id="fdbe5-134">SetClassIDInBlob</span><span class="sxs-lookup"><span data-stu-id="fdbe5-134">SetClassIDInBlob</span></span>](setclassidinblob.md)
</dt> <dt>

[<span data-ttu-id="fdbe5-135">SetDwordInBlob</span><span class="sxs-lookup"><span data-stu-id="fdbe5-135">SetDwordInBlob</span></span>](setdwordinblob.md)
</dt> <dt>

[<span data-ttu-id="fdbe5-136">SetMacAddressInBlob</span><span class="sxs-lookup"><span data-stu-id="fdbe5-136">SetMacAddressInBlob</span></span>](setmacaddressinblob.md)
</dt> <dt>

[<span data-ttu-id="fdbe5-137">SetNetworkInfoInBlob</span><span class="sxs-lookup"><span data-stu-id="fdbe5-137">SetNetworkInfoInBlob</span></span>](setnetworkinfoinblob.md)
</dt> <dt>

[<span data-ttu-id="fdbe5-138">SetNPPAddressFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="fdbe5-138">SetNPPAddressFilterInBlob</span></span>](setnppaddressfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="fdbe5-139">SetNPPPatternFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="fdbe5-139">SetNPPPatternFilterInBlob</span></span>](setnpppatternfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="fdbe5-140">SetStringInBlob</span><span class="sxs-lookup"><span data-stu-id="fdbe5-140">SetStringInBlob</span></span>](setstringinblob.md)
</dt> </dl>

 

 




