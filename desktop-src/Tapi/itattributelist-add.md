---
description: Add 方法會在指定的索引處加入屬性。
ms.assetid: 5b74c177-bf5c-4547-bebb-034a9a10be13
title: 'ITAttributeList：： Add 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5504a216549231aca82eac3b3311ae7208eb8432
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996311"
---
# <a name="itattributelistadd-method"></a><span data-ttu-id="29ee1-103">ITAttributeList：： Add 方法</span><span class="sxs-lookup"><span data-stu-id="29ee1-103">ITAttributeList::Add method</span></span>

<span data-ttu-id="29ee1-104">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="29ee1-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="29ee1-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="29ee1-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="29ee1-106">**Add** 方法會在指定的索引處加入屬性。</span><span class="sxs-lookup"><span data-stu-id="29ee1-106">The **Add** method adds the attribute at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="29ee1-107">語法</span><span class="sxs-lookup"><span data-stu-id="29ee1-107">Syntax</span></span>


```C++
HRESULT Add(
  [in] LONG Index,
  [in] BSTR pAttribute
);
```



## <a name="parameters"></a><span data-ttu-id="29ee1-108">參數</span><span class="sxs-lookup"><span data-stu-id="29ee1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29ee1-109">*索引* \[在\]</span><span class="sxs-lookup"><span data-stu-id="29ee1-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29ee1-110">要加入之屬性的索引。</span><span class="sxs-lookup"><span data-stu-id="29ee1-110">Index of the attribute to add.</span></span>

</dd> <dt>

<span data-ttu-id="29ee1-111">*pAttribute* \[在\]</span><span class="sxs-lookup"><span data-stu-id="29ee1-111">*pAttribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29ee1-112">**BSTR** 的指標，其中包含要加入的屬性值。</span><span class="sxs-lookup"><span data-stu-id="29ee1-112">Pointer to a **BSTR** containing the value of the attribute to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29ee1-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="29ee1-113">Return value</span></span>

<span data-ttu-id="29ee1-114">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="29ee1-114">This method can return one of these values.</span></span>



| <span data-ttu-id="29ee1-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="29ee1-115">Return code</span></span>                                                                                   | <span data-ttu-id="29ee1-116">Description</span><span class="sxs-lookup"><span data-stu-id="29ee1-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="29ee1-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="29ee1-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="29ee1-118">方法成功。</span><span class="sxs-lookup"><span data-stu-id="29ee1-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="29ee1-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="29ee1-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="29ee1-120">*Index* 或 *pAttribute* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="29ee1-120">The *Index* or *pAttribute* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="29ee1-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="29ee1-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="29ee1-122">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="29ee1-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="29ee1-123"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="29ee1-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="29ee1-124">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="29ee1-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="29ee1-125"><dt>**E \_ >NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="29ee1-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="29ee1-126">尚未實作這個方法。</span><span class="sxs-lookup"><span data-stu-id="29ee1-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="29ee1-127">備註</span><span class="sxs-lookup"><span data-stu-id="29ee1-127">Remarks</span></span>

<span data-ttu-id="29ee1-128">應用程式必須使用 [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) 為 *pAttribute* 參數配置記憶體，並在不再需要該變數時，使用 [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) 來釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="29ee1-128">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pAttribute* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="29ee1-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="29ee1-129">Requirements</span></span>



| <span data-ttu-id="29ee1-130">需求</span><span class="sxs-lookup"><span data-stu-id="29ee1-130">Requirement</span></span> | <span data-ttu-id="29ee1-131">值</span><span class="sxs-lookup"><span data-stu-id="29ee1-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="29ee1-132">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="29ee1-132">TAPI version</span></span><br/> | <span data-ttu-id="29ee1-133">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="29ee1-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="29ee1-134">標頭</span><span class="sxs-lookup"><span data-stu-id="29ee1-134">Header</span></span><br/>       | <dl> <span data-ttu-id="29ee1-135"><dt>Sdpblb。h</dt></span><span class="sxs-lookup"><span data-stu-id="29ee1-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="29ee1-136">程式庫</span><span class="sxs-lookup"><span data-stu-id="29ee1-136">Library</span></span><br/>      | <dl> <span data-ttu-id="29ee1-137"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="29ee1-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="29ee1-138">DLL</span><span class="sxs-lookup"><span data-stu-id="29ee1-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="29ee1-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29ee1-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29ee1-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="29ee1-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29ee1-141">**ITAttributeList**</span><span class="sxs-lookup"><span data-stu-id="29ee1-141">**ITAttributeList**</span></span>](itattributelist.md)
</dt> </dl>

 

