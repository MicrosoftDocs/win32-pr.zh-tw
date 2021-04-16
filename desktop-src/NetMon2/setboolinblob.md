---
description: SetBoolInBlob 函式會在 BLOB 中的指定位置設定布林值。
ms.assetid: 354d22be-b8c4-4068-8356-19b30ac188d0
title: 'SetBoolInBlob 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetBoolInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 5cfbb9a3410d511ab143f1d77584a0144435c230
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104513088"
---
# <a name="setboolinblob-function"></a><span data-ttu-id="806d5-103">SetBoolInBlob 函式</span><span class="sxs-lookup"><span data-stu-id="806d5-103">SetBoolInBlob function</span></span>

<span data-ttu-id="806d5-104">**SetBoolInBlob** 函式會在 BLOB 中的指定位置設定布林值。</span><span class="sxs-lookup"><span data-stu-id="806d5-104">The **SetBoolInBlob** function sets a Boolean value at a given location within a BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="806d5-105">語法</span><span class="sxs-lookup"><span data-stu-id="806d5-105">Syntax</span></span>


```C++
DWORD SetBoolInBlob(
  _In_       HBLOB hBlob,
  _In_ const char  *pOwnerName,
  _In_ const char  *pCategoryName,
  _In_ const char  *pTagName,
  _In_       BOOL  Bool
);
```



## <a name="parameters"></a><span data-ttu-id="806d5-106">參數</span><span class="sxs-lookup"><span data-stu-id="806d5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="806d5-107">*hBlob* \[在\]</span><span class="sxs-lookup"><span data-stu-id="806d5-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="806d5-108">BLOB 的控制碼。</span><span class="sxs-lookup"><span data-stu-id="806d5-108">Handle to a BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="806d5-109">*pOwnerName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="806d5-109">*pOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="806d5-110">BLOB **擁有** 者名稱的指標。</span><span class="sxs-lookup"><span data-stu-id="806d5-110">Pointer to the BLOB **Owner** name.</span></span>

</dd> <dt>

<span data-ttu-id="806d5-111">*pCategoryName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="806d5-111">*pCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="806d5-112">BLOB **類別目錄** 名稱的指標。</span><span class="sxs-lookup"><span data-stu-id="806d5-112">Pointer to the BLOB **Category** name.</span></span>

</dd> <dt>

<span data-ttu-id="806d5-113">*pTagName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="806d5-113">*pTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="806d5-114">BLOB **標記** 名稱的指標。</span><span class="sxs-lookup"><span data-stu-id="806d5-114">Pointer to the BLOB **Tag** name.</span></span>

</dd> <dt>

<span data-ttu-id="806d5-115">*Bool* \[在\]</span><span class="sxs-lookup"><span data-stu-id="806d5-115">*Bool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="806d5-116">在指定位置設定的布林值。</span><span class="sxs-lookup"><span data-stu-id="806d5-116">Boolean value that is set at the given location.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="806d5-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="806d5-117">Return value</span></span>

<span data-ttu-id="806d5-118">如果函式成功，則傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="806d5-118">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="806d5-119">如果函式不成功，則傳回值會是指出錯誤的 NMERR 值。</span><span class="sxs-lookup"><span data-stu-id="806d5-119">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="806d5-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="806d5-120">Requirements</span></span>



| <span data-ttu-id="806d5-121">需求</span><span class="sxs-lookup"><span data-stu-id="806d5-121">Requirement</span></span> | <span data-ttu-id="806d5-122">值</span><span class="sxs-lookup"><span data-stu-id="806d5-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="806d5-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="806d5-123">Minimum supported client</span></span><br/> | <span data-ttu-id="806d5-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="806d5-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="806d5-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="806d5-125">Minimum supported server</span></span><br/> | <span data-ttu-id="806d5-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="806d5-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="806d5-127">標頭</span><span class="sxs-lookup"><span data-stu-id="806d5-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="806d5-128"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="806d5-128"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="806d5-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="806d5-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="806d5-130"><dt>Npptools .lib</dt></span><span class="sxs-lookup"><span data-stu-id="806d5-130"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="806d5-131">DLL</span><span class="sxs-lookup"><span data-stu-id="806d5-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="806d5-132"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="806d5-132"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="806d5-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="806d5-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="806d5-134">GetBoolFromBlob</span><span class="sxs-lookup"><span data-stu-id="806d5-134">GetBoolFromBlob</span></span>](getboolfromblob.md)
</dt> <dt>

[<span data-ttu-id="806d5-135">SetClassIDInBlob</span><span class="sxs-lookup"><span data-stu-id="806d5-135">SetClassIDInBlob</span></span>](setclassidinblob.md)
</dt> <dt>

[<span data-ttu-id="806d5-136">SetDwordInBlob</span><span class="sxs-lookup"><span data-stu-id="806d5-136">SetDwordInBlob</span></span>](setdwordinblob.md)
</dt> <dt>

[<span data-ttu-id="806d5-137">SetMacAddressInBlob</span><span class="sxs-lookup"><span data-stu-id="806d5-137">SetMacAddressInBlob</span></span>](setmacaddressinblob.md)
</dt> <dt>

[<span data-ttu-id="806d5-138">SetNetworkInfoInBlob</span><span class="sxs-lookup"><span data-stu-id="806d5-138">SetNetworkInfoInBlob</span></span>](setnetworkinfoinblob.md)
</dt> <dt>

[<span data-ttu-id="806d5-139">SetNPPAddressFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="806d5-139">SetNPPAddressFilterInBlob</span></span>](setnppaddressfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="806d5-140">SetNPPPatternFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="806d5-140">SetNPPPatternFilterInBlob</span></span>](setnpppatternfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="806d5-141">SetNPPTriggerInBlob</span><span class="sxs-lookup"><span data-stu-id="806d5-141">SetNPPTriggerInBlob</span></span>](setnpptriggerinblob.md)
</dt> <dt>

[<span data-ttu-id="806d5-142">SetStringInBlob</span><span class="sxs-lookup"><span data-stu-id="806d5-142">SetStringInBlob</span></span>](setstringinblob.md)
</dt> </dl>

 

 




