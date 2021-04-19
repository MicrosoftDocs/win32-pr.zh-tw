---
description: SetDwordInBlob 函式會設定 BLOB 的已命名 DWORD 值。
ms.assetid: 9174cd5c-4442-4fbe-8dc7-f8a74e1cc85d
title: 'SetDwordInBlob 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetDwordInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 9bca0efe61824c6fb8dd41b0b241791b6303799d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106985636"
---
# <a name="setdwordinblob-function"></a><span data-ttu-id="9b125-103">SetDwordInBlob 函式</span><span class="sxs-lookup"><span data-stu-id="9b125-103">SetDwordInBlob function</span></span>

<span data-ttu-id="9b125-104">**SetDwordInBlob** 函式會設定 BLOB 的已命名 **DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="9b125-104">The **SetDwordInBlob** function sets the named **DWORD** value of a BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b125-105">語法</span><span class="sxs-lookup"><span data-stu-id="9b125-105">Syntax</span></span>


```C++
DWORD SetDwordInBlob(
  _In_       HBLOB hBlob,
  _In_ const char  *pOwnerName,
  _In_ const char  *pCategoryName,
  _In_ const char  *pTagName,
  _In_       DWORD Dword
);
```



## <a name="parameters"></a><span data-ttu-id="9b125-106">參數</span><span class="sxs-lookup"><span data-stu-id="9b125-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b125-107">*hBlob* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9b125-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b125-108">要設定之 BLOB 的控制碼。</span><span class="sxs-lookup"><span data-stu-id="9b125-108">Handle to a BLOB being set.</span></span>

</dd> <dt>

<span data-ttu-id="9b125-109">*pOwnerName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9b125-109">*pOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b125-110">要設定之 BLOB **擁有** 者名稱的指標。</span><span class="sxs-lookup"><span data-stu-id="9b125-110">Pointer to the BLOB **Owner** name being set.</span></span>

</dd> <dt>

<span data-ttu-id="9b125-111">*pCategoryName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9b125-111">*pCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b125-112">要設定之 BLOB **類別目錄** 名稱的指標。</span><span class="sxs-lookup"><span data-stu-id="9b125-112">Pointer to the BLOB **Category** name being set.</span></span>

</dd> <dt>

<span data-ttu-id="9b125-113">*pTagName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9b125-113">*pTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b125-114">要設定之 BLOB **標記** 名稱的指標。</span><span class="sxs-lookup"><span data-stu-id="9b125-114">Pointer to the BLOB **Tag** name being set.</span></span>

</dd> <dt>

<span data-ttu-id="9b125-115">*Dword* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9b125-115">*Dword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b125-116">要設定之 BLOB 的 **DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="9b125-116">**DWORD** value of the BLOB being set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b125-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="9b125-117">Return value</span></span>

<span data-ttu-id="9b125-118">如果函式成功，則傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="9b125-118">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="9b125-119">如果函式不成功，則傳回值會是指出錯誤的 NMERR 值。</span><span class="sxs-lookup"><span data-stu-id="9b125-119">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b125-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="9b125-120">Requirements</span></span>



| <span data-ttu-id="9b125-121">需求</span><span class="sxs-lookup"><span data-stu-id="9b125-121">Requirement</span></span> | <span data-ttu-id="9b125-122">值</span><span class="sxs-lookup"><span data-stu-id="9b125-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9b125-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9b125-123">Minimum supported client</span></span><br/> | <span data-ttu-id="9b125-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9b125-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="9b125-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9b125-125">Minimum supported server</span></span><br/> | <span data-ttu-id="9b125-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9b125-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9b125-127">標頭</span><span class="sxs-lookup"><span data-stu-id="9b125-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b125-128"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="9b125-128"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="9b125-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="9b125-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="9b125-130"><dt>Npptools .lib</dt></span><span class="sxs-lookup"><span data-stu-id="9b125-130"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="9b125-131">DLL</span><span class="sxs-lookup"><span data-stu-id="9b125-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b125-132"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b125-132"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b125-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9b125-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b125-134">GetDwordFromBlob</span><span class="sxs-lookup"><span data-stu-id="9b125-134">GetDwordFromBlob</span></span>](getdwordfromblob.md)
</dt> <dt>

[<span data-ttu-id="9b125-135">SetBoolInBlob</span><span class="sxs-lookup"><span data-stu-id="9b125-135">SetBoolInBlob</span></span>](setboolinblob.md)
</dt> <dt>

[<span data-ttu-id="9b125-136">SetClassIDInBlob</span><span class="sxs-lookup"><span data-stu-id="9b125-136">SetClassIDInBlob</span></span>](setclassidinblob.md)
</dt> <dt>

[<span data-ttu-id="9b125-137">SetMacAddressInBlob</span><span class="sxs-lookup"><span data-stu-id="9b125-137">SetMacAddressInBlob</span></span>](setmacaddressinblob.md)
</dt> <dt>

[<span data-ttu-id="9b125-138">SetNetworkInfoInBlob</span><span class="sxs-lookup"><span data-stu-id="9b125-138">SetNetworkInfoInBlob</span></span>](setnetworkinfoinblob.md)
</dt> <dt>

[<span data-ttu-id="9b125-139">SetNPPAddressFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="9b125-139">SetNPPAddressFilterInBlob</span></span>](setnppaddressfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="9b125-140">SetNPPPatternFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="9b125-140">SetNPPPatternFilterInBlob</span></span>](setnpppatternfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="9b125-141">SetNPPTriggerInBlob</span><span class="sxs-lookup"><span data-stu-id="9b125-141">SetNPPTriggerInBlob</span></span>](setnpptriggerinblob.md)
</dt> <dt>

[<span data-ttu-id="9b125-142">SetStringInBlob</span><span class="sxs-lookup"><span data-stu-id="9b125-142">SetStringInBlob</span></span>](setstringinblob.md)
</dt> </dl>

 

 




