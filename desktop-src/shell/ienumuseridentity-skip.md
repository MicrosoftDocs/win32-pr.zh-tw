---
description: IEnumUserIdentity：： Skip 不受支援，而且可能會在未來變更或無法使用。 相反地，請使用使用者帳戶搭配快速切換使用者與遠端桌面。
ms.assetid: bb19ae50-b384-48fb-9272-15e3e3eaa9d0
title: 'IEnumUserIdentity：： Skip 方法 (Msident .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumUserIdentity.Skip
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: cedd4f3c6e9736e26cbf8d58f27f805f0f5d33a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991523"
---
# <a name="ienumuseridentityskip-method"></a><span data-ttu-id="5865c-104">IEnumUserIdentity：： Skip 方法</span><span class="sxs-lookup"><span data-stu-id="5865c-104">IEnumUserIdentity::Skip method</span></span>

<span data-ttu-id="5865c-105">\[**IEnumUserIdentity：： Skip** 不受支援，而且可能會在未來變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="5865c-105">\[**IEnumUserIdentity::Skip** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="5865c-106">相反地，請使用 [使用者帳戶搭配快速切換使用者與遠端桌面](fastuserswitching.md)。\]</span><span class="sxs-lookup"><span data-stu-id="5865c-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="5865c-107">在列舉中略過指定數目的使用者識別介面。</span><span class="sxs-lookup"><span data-stu-id="5865c-107">Skips a given number of user identity interfaces in the enumeration.</span></span> <span data-ttu-id="5865c-108">在抓取介面時使用。</span><span class="sxs-lookup"><span data-stu-id="5865c-108">Used when retrieving interfaces.</span></span>

## <a name="syntax"></a><span data-ttu-id="5865c-109">語法</span><span class="sxs-lookup"><span data-stu-id="5865c-109">Syntax</span></span>


```C++
HRESULT Skip(
  [in] ULONG celt
);
```



## <a name="parameters"></a><span data-ttu-id="5865c-110">參數</span><span class="sxs-lookup"><span data-stu-id="5865c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5865c-111">*celt* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5865c-111">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5865c-112">類型： **ULONG**</span><span class="sxs-lookup"><span data-stu-id="5865c-112">Type: **ULONG**</span></span>

<span data-ttu-id="5865c-113">要略過的介面數目。</span><span class="sxs-lookup"><span data-stu-id="5865c-113">The number of interfaces to skip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5865c-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="5865c-114">Return value</span></span>

<span data-ttu-id="5865c-115">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="5865c-115">Type: **HRESULT**</span></span>

<span data-ttu-id="5865c-116">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="5865c-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5865c-117">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="5865c-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5865c-118">備註</span><span class="sxs-lookup"><span data-stu-id="5865c-118">Remarks</span></span>

<span data-ttu-id="5865c-119">[**IEnumUserIdentity**](ienumuseridentity.md) 會保留內部計數，以指定要取出的介面。</span><span class="sxs-lookup"><span data-stu-id="5865c-119">[**IEnumUserIdentity**](ienumuseridentity.md) keeps an internal count that specifies which interface is next to be retrieved.</span></span> <span data-ttu-id="5865c-120">若要遞增此計數而不需要抓取介面，請呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="5865c-120">To increment this count without retrieving interfaces, call this method.</span></span> <span data-ttu-id="5865c-121">若要重設計數，請呼叫 [**IEnumUserIdentity：： reset**](ienumuseridentity-reset.md)。</span><span class="sxs-lookup"><span data-stu-id="5865c-121">To reset the count, call [**IEnumUserIdentity::Reset**](ienumuseridentity-reset.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5865c-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="5865c-122">Requirements</span></span>



| <span data-ttu-id="5865c-123">需求</span><span class="sxs-lookup"><span data-stu-id="5865c-123">Requirement</span></span> | <span data-ttu-id="5865c-124">值</span><span class="sxs-lookup"><span data-stu-id="5865c-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5865c-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5865c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="5865c-126">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5865c-126">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="5865c-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5865c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="5865c-128">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5865c-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="5865c-129">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="5865c-129">End of client support</span></span><br/>    | <span data-ttu-id="5865c-130">Windows XP</span><span class="sxs-lookup"><span data-stu-id="5865c-130">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="5865c-131">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="5865c-131">End of server support</span></span><br/>    | <span data-ttu-id="5865c-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5865c-132">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="5865c-133">標頭</span><span class="sxs-lookup"><span data-stu-id="5865c-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="5865c-134"><dt>Msident。h</dt></span><span class="sxs-lookup"><span data-stu-id="5865c-134"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="5865c-135">Idl</span><span class="sxs-lookup"><span data-stu-id="5865c-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5865c-136"><dt>Msident .idl</dt></span><span class="sxs-lookup"><span data-stu-id="5865c-136"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="5865c-137">DLL</span><span class="sxs-lookup"><span data-stu-id="5865c-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5865c-138"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5865c-138"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5865c-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5865c-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5865c-140">**IEnumUserIdentity**</span><span class="sxs-lookup"><span data-stu-id="5865c-140">**IEnumUserIdentity**</span></span>](ienumuseridentity.md)
</dt> <dt>

[<span data-ttu-id="5865c-141">**IEnumUserIdentity：： Reset**</span><span class="sxs-lookup"><span data-stu-id="5865c-141">**IEnumUserIdentity::Reset**</span></span>](ienumuseridentity-reset.md)
</dt> <dt>

[<span data-ttu-id="5865c-142">**IEnumUserIdentity：： Next**</span><span class="sxs-lookup"><span data-stu-id="5865c-142">**IEnumUserIdentity::Next**</span></span>](ienumuseridentity-next.md)
</dt> <dt>

[<span data-ttu-id="5865c-143">**IEnumUserIdentity：： GetCount**</span><span class="sxs-lookup"><span data-stu-id="5865c-143">**IEnumUserIdentity::GetCount**</span></span>](ienumuseridentity-getcount.md)
</dt> </dl>

 

 




