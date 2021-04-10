---
title: 'UtilLoadStringWithAlloc 函式 (Ndattributils) '
description: 從資源資料表配置和載入字串。
ms.assetid: 34bf0b93-2bec-49c3-9441-c83686c4abdb
keywords:
- UtilLoadStringWithAlloc 函式 NDF
topic_type:
- apiref
api_name:
- UtilLoadStringWithAlloc
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72e13930fe9bb11ae9c9456152c823491eabc462
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106500"
---
# <a name="utilloadstringwithalloc-function"></a><span data-ttu-id="6a39c-104">UtilLoadStringWithAlloc 函式</span><span class="sxs-lookup"><span data-stu-id="6a39c-104">UtilLoadStringWithAlloc function</span></span>

<span data-ttu-id="6a39c-105">**UtilLoadStringWithAlloc** 函式會從資源資料表配置和載入字串。</span><span class="sxs-lookup"><span data-stu-id="6a39c-105">The **UtilLoadStringWithAlloc** function allocates and loads a string out of the resource table.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a39c-106">語法</span><span class="sxs-lookup"><span data-stu-id="6a39c-106">Syntax</span></span>


```C++
HRESULT UtilLoadStringWithAlloc(
  _In_  UINT   uID,
  _Out_ LPWSTR *ppwzBuffer,
  _In_  UINT   cchBufferMax
);
```



## <a name="parameters"></a><span data-ttu-id="6a39c-107">參數</span><span class="sxs-lookup"><span data-stu-id="6a39c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a39c-108">*uID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6a39c-108">*uID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a39c-109">類型： **UINT**</span><span class="sxs-lookup"><span data-stu-id="6a39c-109">Type: **UINT**</span></span>

<span data-ttu-id="6a39c-110">要載入之字串的識別碼。</span><span class="sxs-lookup"><span data-stu-id="6a39c-110">Identifier of of the string to be loaded.</span></span>

</dd> <dt>

<span data-ttu-id="6a39c-111">*ppwzBuffer* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6a39c-111">*ppwzBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6a39c-112">類型： \**LPWSTR \** _</span><span class="sxs-lookup"><span data-stu-id="6a39c-112">Type: \**LPWSTR\** _</span></span>

<span data-ttu-id="6a39c-113">將放置新配置之字串的位置。</span><span class="sxs-lookup"><span data-stu-id="6a39c-113">The location where the newly allocated string will be placed.</span></span> <span data-ttu-id="6a39c-114">當您不再需要字串時，必須使用 [_ *CoTaskMemFree* \*](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)釋放字串。</span><span class="sxs-lookup"><span data-stu-id="6a39c-114">The string must be freed using [_ *CoTaskMemFree*\*](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) when it is no longer needed.</span></span>

</dd> <dt>

<span data-ttu-id="6a39c-115">*cchBufferMax* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6a39c-115">*cchBufferMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a39c-116">類型： **UINT**</span><span class="sxs-lookup"><span data-stu-id="6a39c-116">Type: **UINT**</span></span>

<span data-ttu-id="6a39c-117">要從資源資料表載入的最大字元數。</span><span class="sxs-lookup"><span data-stu-id="6a39c-117">The maximum number of characters to load from the resource table.</span></span> <span data-ttu-id="6a39c-118">如果資源字串的長度超過指定的字元數，則會被截斷並以 null 結束。</span><span class="sxs-lookup"><span data-stu-id="6a39c-118">If the resource string is longer than the number of characters specified, it is truncated and null-terminated.</span></span>

> [!Note]  
> <span data-ttu-id="6a39c-119">此參數不可以設定為零。</span><span class="sxs-lookup"><span data-stu-id="6a39c-119">This parameter may not be set to zero.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a39c-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="6a39c-120">Return value</span></span>

<span data-ttu-id="6a39c-121">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="6a39c-121">Type: **HRESULT**</span></span>

<span data-ttu-id="6a39c-122">可能的傳回值包括（但不限於）下列各項。</span><span class="sxs-lookup"><span data-stu-id="6a39c-122">Possible return values include, but are not limited to, the following.</span></span>



| <span data-ttu-id="6a39c-123">傳回碼</span><span class="sxs-lookup"><span data-stu-id="6a39c-123">Return code</span></span>                                                                                  | <span data-ttu-id="6a39c-124">Description</span><span class="sxs-lookup"><span data-stu-id="6a39c-124">Description</span></span>                                                        |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="6a39c-125"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="6a39c-125"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="6a39c-126">作業成功。</span><span class="sxs-lookup"><span data-stu-id="6a39c-126">The operation succeeded.</span></span><br/>                                |
| <dl> <span data-ttu-id="6a39c-127"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="6a39c-127"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="6a39c-128">未正確提供一或多個參數。</span><span class="sxs-lookup"><span data-stu-id="6a39c-128">One or more parameters has not been provided correctly.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="6a39c-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="6a39c-129">Requirements</span></span>



| <span data-ttu-id="6a39c-130">需求</span><span class="sxs-lookup"><span data-stu-id="6a39c-130">Requirement</span></span> | <span data-ttu-id="6a39c-131">值</span><span class="sxs-lookup"><span data-stu-id="6a39c-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a39c-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6a39c-132">Minimum supported client</span></span><br/> | <span data-ttu-id="6a39c-133">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6a39c-133">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="6a39c-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6a39c-134">Minimum supported server</span></span><br/> | <span data-ttu-id="6a39c-135">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6a39c-135">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="6a39c-136">標頭</span><span class="sxs-lookup"><span data-stu-id="6a39c-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a39c-137"><dt>Ndattributils。h</dt></span><span class="sxs-lookup"><span data-stu-id="6a39c-137"><dt>Ndattributils.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a39c-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6a39c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a39c-139">**UtilStringCopyWithAlloc**</span><span class="sxs-lookup"><span data-stu-id="6a39c-139">**UtilStringCopyWithAlloc**</span></span>](utilstringcopywithalloc.md)
</dt> <dt>

[<span data-ttu-id="6a39c-140">**UtilAssembleStringsWithAlloc**</span><span class="sxs-lookup"><span data-stu-id="6a39c-140">**UtilAssembleStringsWithAlloc**</span></span>](utilassemblestringswithalloc.md)
</dt> <dt>

[<span data-ttu-id="6a39c-141">**CoTaskMemFree**</span><span class="sxs-lookup"><span data-stu-id="6a39c-141">**CoTaskMemFree**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

