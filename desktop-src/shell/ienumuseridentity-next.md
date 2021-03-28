---
description: IEnumUserIdentity：： Next 不受支援，而且可能會在未來變更或無法使用。 相反地，請使用使用者帳戶搭配快速切換使用者與遠端桌面。
ms.assetid: 2c8dfe36-c1bb-49f8-8847-f355cfab2984
title: 'IEnumUserIdentity：： Next 方法 (Msident .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumUserIdentity.Next
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 763b2b4a612596c5f02a9826ad2e9c09ab8e4b0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991527"
---
# <a name="ienumuseridentitynext-method"></a><span data-ttu-id="500ec-104">IEnumUserIdentity：： Next 方法</span><span class="sxs-lookup"><span data-stu-id="500ec-104">IEnumUserIdentity::Next method</span></span>

<span data-ttu-id="500ec-105">\[**IEnumUserIdentity：： Next** 不受支援，而且可能會在未來變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="500ec-105">\[**IEnumUserIdentity::Next** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="500ec-106">相反地，請使用 [使用者帳戶搭配快速切換使用者與遠端桌面](fastuserswitching.md)。\]</span><span class="sxs-lookup"><span data-stu-id="500ec-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="500ec-107">已取代。</span><span class="sxs-lookup"><span data-stu-id="500ec-107">Deprecated.</span></span> <span data-ttu-id="500ec-108">從列舉中抓取使用者識別介面的陣列。</span><span class="sxs-lookup"><span data-stu-id="500ec-108">Retrieves an array of user identity interfaces from the enumeration.</span></span>

## <a name="syntax"></a><span data-ttu-id="500ec-109">語法</span><span class="sxs-lookup"><span data-stu-id="500ec-109">Syntax</span></span>


```C++
HRESULT Next(
  [in]  ULONG    celt,
  [out] IUnknown **rgelt,
  [out] ULONG    *pceltFetched
);
```



## <a name="parameters"></a><span data-ttu-id="500ec-110">參數</span><span class="sxs-lookup"><span data-stu-id="500ec-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="500ec-111">*celt* \[在\]</span><span class="sxs-lookup"><span data-stu-id="500ec-111">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="500ec-112">類型： **ULONG**</span><span class="sxs-lookup"><span data-stu-id="500ec-112">Type: **ULONG**</span></span>

<span data-ttu-id="500ec-113">**ULONG** 值，表示要取出的介面數目。</span><span class="sxs-lookup"><span data-stu-id="500ec-113">A **ULONG** value that represents the number of interfaces to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="500ec-114">*rgelt* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="500ec-114">*rgelt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="500ec-115">類型： **[ **IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\*\***</span><span class="sxs-lookup"><span data-stu-id="500ec-115">Type: **[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\*\***</span></span>

<span data-ttu-id="500ec-116">接收介面之指標的位址。</span><span class="sxs-lookup"><span data-stu-id="500ec-116">The address of a pointer that receives the interfaces.</span></span>

</dd> <dt>

<span data-ttu-id="500ec-117">*pceltFetched* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="500ec-117">*pceltFetched* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="500ec-118">類型： \**ULONG \** _</span><span class="sxs-lookup"><span data-stu-id="500ec-118">Type: \**ULONG\** _</span></span>

<span data-ttu-id="500ec-119">接收成功抓取之介面數目的指標位址。</span><span class="sxs-lookup"><span data-stu-id="500ec-119">The address of a pointer that receives the number of interfaces successfully retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="500ec-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="500ec-120">Return value</span></span>

<span data-ttu-id="500ec-121">類型： _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="500ec-121">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="500ec-122">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="500ec-122">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="500ec-123">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="500ec-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="500ec-124">備註</span><span class="sxs-lookup"><span data-stu-id="500ec-124">Remarks</span></span>

<span data-ttu-id="500ec-125">[**IEnumUserIdentity**](ienumuseridentity.md) 會保留內部計數，以指定要取出的介面。</span><span class="sxs-lookup"><span data-stu-id="500ec-125">[**IEnumUserIdentity**](ienumuseridentity.md) keeps an internal count that specifies which interface is next to be retrieved.</span></span> <span data-ttu-id="500ec-126">這個方法的多個呼叫不會重設這個計數。</span><span class="sxs-lookup"><span data-stu-id="500ec-126">Multiple calls to this method will not reset this count.</span></span> <span data-ttu-id="500ec-127">若要重設計數，請呼叫 [**IEnumUserIdentity：： reset**](ienumuseridentity-reset.md)。</span><span class="sxs-lookup"><span data-stu-id="500ec-127">To reset the count, call [**IEnumUserIdentity::Reset**](ienumuseridentity-reset.md).</span></span> <span data-ttu-id="500ec-128">若要遞增計數而不需要取出介面，請呼叫 [**IEnumUserIdentity：： Skip**](ienumuseridentity-skip.md)。</span><span class="sxs-lookup"><span data-stu-id="500ec-128">To increment the count without retrieving interfaces, call [**IEnumUserIdentity::Skip**](ienumuseridentity-skip.md).</span></span>

<span data-ttu-id="500ec-129">*Celt* 的值不應超過 [**IEnumUserIdentity：： GetCount**](ienumuseridentity-getcount.md)傳回的值。</span><span class="sxs-lookup"><span data-stu-id="500ec-129">The value of *celt* should not exceed the value returned by [**IEnumUserIdentity::GetCount**](ienumuseridentity-getcount.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="500ec-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="500ec-130">Requirements</span></span>



| <span data-ttu-id="500ec-131">需求</span><span class="sxs-lookup"><span data-stu-id="500ec-131">Requirement</span></span> | <span data-ttu-id="500ec-132">值</span><span class="sxs-lookup"><span data-stu-id="500ec-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="500ec-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="500ec-133">Minimum supported client</span></span><br/> | <span data-ttu-id="500ec-134">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="500ec-134">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="500ec-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="500ec-135">Minimum supported server</span></span><br/> | <span data-ttu-id="500ec-136">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="500ec-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="500ec-137">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="500ec-137">End of client support</span></span><br/>    | <span data-ttu-id="500ec-138">Windows XP</span><span class="sxs-lookup"><span data-stu-id="500ec-138">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="500ec-139">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="500ec-139">End of server support</span></span><br/>    | <span data-ttu-id="500ec-140">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="500ec-140">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="500ec-141">標頭</span><span class="sxs-lookup"><span data-stu-id="500ec-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="500ec-142"><dt>Msident。h</dt></span><span class="sxs-lookup"><span data-stu-id="500ec-142"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="500ec-143">Idl</span><span class="sxs-lookup"><span data-stu-id="500ec-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="500ec-144"><dt>Msident .idl</dt></span><span class="sxs-lookup"><span data-stu-id="500ec-144"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="500ec-145">DLL</span><span class="sxs-lookup"><span data-stu-id="500ec-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="500ec-146"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="500ec-146"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="500ec-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="500ec-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="500ec-148">**IEnumUserIdentity**</span><span class="sxs-lookup"><span data-stu-id="500ec-148">**IEnumUserIdentity**</span></span>](ienumuseridentity.md)
</dt> <dt>

[<span data-ttu-id="500ec-149">**IEnumUserIdentity：： Skip**</span><span class="sxs-lookup"><span data-stu-id="500ec-149">**IEnumUserIdentity::Skip**</span></span>](ienumuseridentity-skip.md)
</dt> <dt>

[<span data-ttu-id="500ec-150">**IEnumUserIdentity：： Reset**</span><span class="sxs-lookup"><span data-stu-id="500ec-150">**IEnumUserIdentity::Reset**</span></span>](ienumuseridentity-reset.md)
</dt> <dt>

[<span data-ttu-id="500ec-151">**IEnumUserIdentity：： GetCount**</span><span class="sxs-lookup"><span data-stu-id="500ec-151">**IEnumUserIdentity::GetCount**</span></span>](ienumuseridentity-getcount.md)
</dt> </dl>

 

 
