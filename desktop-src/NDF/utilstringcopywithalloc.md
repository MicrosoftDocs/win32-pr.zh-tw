---
title: 'UtilStringCopyWithAlloc 函式 (Ndattributils) '
description: 配置和複製來源字串。
ms.assetid: e1400ae1-0edd-4b59-af03-3da1b9d7073b
keywords:
- UtilStringCopyWithAlloc 函式 NDF
topic_type:
- apiref
api_name:
- UtilStringCopyWithAlloc
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b68bd1815ff09473f0431dde19a12a87603a9dec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965706"
---
# <a name="utilstringcopywithalloc-function"></a><span data-ttu-id="2c489-104">UtilStringCopyWithAlloc 函式</span><span class="sxs-lookup"><span data-stu-id="2c489-104">UtilStringCopyWithAlloc function</span></span>

<span data-ttu-id="2c489-105">**UtilStringCopyWithAlloc** 函數會配置和複製來源字串。</span><span class="sxs-lookup"><span data-stu-id="2c489-105">The **UtilStringCopyWithAlloc** function allocates and copies a source string.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c489-106">語法</span><span class="sxs-lookup"><span data-stu-id="2c489-106">Syntax</span></span>


```C++
HRESULT UtilStringCopyWithAlloc(
  _Out_ LPWSTR  *Buffer,
  _In_  UINT    BufferMax,
  _In_  LPCWSTR Source
);
```



## <a name="parameters"></a><span data-ttu-id="2c489-107">參數</span><span class="sxs-lookup"><span data-stu-id="2c489-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c489-108">*緩衝區* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="2c489-108">*Buffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2c489-109">類型： \**LPWSTR \** _</span><span class="sxs-lookup"><span data-stu-id="2c489-109">Type: \**LPWSTR\** _</span></span>

<span data-ttu-id="2c489-110">儲存配置記憶體指標的位置。</span><span class="sxs-lookup"><span data-stu-id="2c489-110">The location where the pointer to the allocated memory is stored.</span></span> <span data-ttu-id="2c489-111">當不再需要時，必須使用 [_ *CoTaskMemFree* \*](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)來發行。</span><span class="sxs-lookup"><span data-stu-id="2c489-111">When no longer needed, it must be released with [_ *CoTaskMemFree*\*](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span> <span data-ttu-id="2c489-112">這個緩衝區一律會以 null 結束。</span><span class="sxs-lookup"><span data-stu-id="2c489-112">This buffer is always null-terminated.</span></span>

</dd> <dt>

<span data-ttu-id="2c489-113">*BufferMax* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2c489-113">*BufferMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c489-114">類型： **UINT**</span><span class="sxs-lookup"><span data-stu-id="2c489-114">Type: **UINT**</span></span>

<span data-ttu-id="2c489-115">要從 *來源* 讀取的最大字元數。</span><span class="sxs-lookup"><span data-stu-id="2c489-115">The maximum number of characters to read from *Source*.</span></span>

</dd> <dt>

<span data-ttu-id="2c489-116">*來源* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2c489-116">*Source* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c489-117">類型： **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="2c489-117">Type: **LPCWSTR**</span></span>

<span data-ttu-id="2c489-118">要複製的字串。</span><span class="sxs-lookup"><span data-stu-id="2c489-118">The string to be copied.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c489-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="2c489-119">Return value</span></span>

<span data-ttu-id="2c489-120">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="2c489-120">Type: **HRESULT**</span></span>

<span data-ttu-id="2c489-121">可能的傳回值包括（但不限於）下列各項。</span><span class="sxs-lookup"><span data-stu-id="2c489-121">Possible return values include, but are not limited to, the following.</span></span>



| <span data-ttu-id="2c489-122">傳回碼</span><span class="sxs-lookup"><span data-stu-id="2c489-122">Return code</span></span>                                                                                  | <span data-ttu-id="2c489-123">Description</span><span class="sxs-lookup"><span data-stu-id="2c489-123">Description</span></span>                                                        |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="2c489-124"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="2c489-124"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="2c489-125">作業成功。</span><span class="sxs-lookup"><span data-stu-id="2c489-125">The operation succeeded.</span></span><br/>                                |
| <dl> <span data-ttu-id="2c489-126"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="2c489-126"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="2c489-127">未正確提供一或多個參數。</span><span class="sxs-lookup"><span data-stu-id="2c489-127">One or more parameters has not been provided correctly.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="2c489-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="2c489-128">Requirements</span></span>



| <span data-ttu-id="2c489-129">需求</span><span class="sxs-lookup"><span data-stu-id="2c489-129">Requirement</span></span> | <span data-ttu-id="2c489-130">值</span><span class="sxs-lookup"><span data-stu-id="2c489-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c489-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2c489-131">Minimum supported client</span></span><br/> | <span data-ttu-id="2c489-132">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2c489-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="2c489-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2c489-133">Minimum supported server</span></span><br/> | <span data-ttu-id="2c489-134">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2c489-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="2c489-135">標頭</span><span class="sxs-lookup"><span data-stu-id="2c489-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c489-136"><dt>Ndattributils。h</dt></span><span class="sxs-lookup"><span data-stu-id="2c489-136"><dt>Ndattributils.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c489-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2c489-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c489-138">**CoTaskMemFree**</span><span class="sxs-lookup"><span data-stu-id="2c489-138">**CoTaskMemFree**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> <dt>

[<span data-ttu-id="2c489-139">**UtilAssembleStringsWithAlloc**</span><span class="sxs-lookup"><span data-stu-id="2c489-139">**UtilAssembleStringsWithAlloc**</span></span>](utilassemblestringswithalloc.md)
</dt> <dt>

[<span data-ttu-id="2c489-140">**UtilLoadStringWithAlloc**</span><span class="sxs-lookup"><span data-stu-id="2c489-140">**UtilLoadStringWithAlloc**</span></span>](utilloadstringwithalloc.md)
</dt> </dl>

 

