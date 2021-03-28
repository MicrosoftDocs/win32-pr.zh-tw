---
description: GetCount 不受支援，未來可能會變更或無法使用。 相反地，請使用使用者帳戶搭配快速切換使用者與遠端桌面。
ms.assetid: 1fe39f2d-f95e-4436-a780-40fe8bd41b74
title: 'IEnumUserIdentity：： GetCount 方法 (Msident .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumUserIdentity.GetCount
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 43355a9585fc4099c8649f7df506ff3495a53944
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319131"
---
# <a name="ienumuseridentitygetcount-method"></a><span data-ttu-id="94069-104">IEnumUserIdentity：： GetCount 方法</span><span class="sxs-lookup"><span data-stu-id="94069-104">IEnumUserIdentity::GetCount method</span></span>

<span data-ttu-id="94069-105">\[**GetCount** 不受支援，未來可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="94069-105">\[**GetCount** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="94069-106">相反地，請使用 [使用者帳戶搭配快速切換使用者與遠端桌面](fastuserswitching.md)。\]</span><span class="sxs-lookup"><span data-stu-id="94069-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="94069-107">取得目前在系統上的使用者身分識別計數。</span><span class="sxs-lookup"><span data-stu-id="94069-107">Gets the count of user identities currently on the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="94069-108">語法</span><span class="sxs-lookup"><span data-stu-id="94069-108">Syntax</span></span>


```C++
HRESULT GetCount(
  [out] ULONG *pnCount
);
```



## <a name="parameters"></a><span data-ttu-id="94069-109">參數</span><span class="sxs-lookup"><span data-stu-id="94069-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94069-110">*pnCount* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="94069-110">*pnCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="94069-111">類型： \**ULONG \** _</span><span class="sxs-lookup"><span data-stu-id="94069-111">Type: \**ULONG\** _</span></span>

<span data-ttu-id="94069-112">接收計數的 _ *ULONG*\* 指標。</span><span class="sxs-lookup"><span data-stu-id="94069-112">Pointer to a _ *ULONG*\* that receives the count.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94069-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="94069-113">Return value</span></span>

<span data-ttu-id="94069-114">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="94069-114">Type: **HRESULT**</span></span>

<span data-ttu-id="94069-115">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="94069-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="94069-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="94069-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="94069-117">備註</span><span class="sxs-lookup"><span data-stu-id="94069-117">Remarks</span></span>

<span data-ttu-id="94069-118">如果停用多個使用者身分識別的支援， *pnCount* 將會收到值1。</span><span class="sxs-lookup"><span data-stu-id="94069-118">If support for multiple user identities is disabled, *pnCount* will receive a value of 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="94069-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="94069-119">Requirements</span></span>



| <span data-ttu-id="94069-120">需求</span><span class="sxs-lookup"><span data-stu-id="94069-120">Requirement</span></span> | <span data-ttu-id="94069-121">值</span><span class="sxs-lookup"><span data-stu-id="94069-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="94069-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="94069-122">Minimum supported client</span></span><br/> | <span data-ttu-id="94069-123">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="94069-123">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="94069-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="94069-124">Minimum supported server</span></span><br/> | <span data-ttu-id="94069-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="94069-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="94069-126">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="94069-126">End of client support</span></span><br/>    | <span data-ttu-id="94069-127">Windows XP</span><span class="sxs-lookup"><span data-stu-id="94069-127">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="94069-128">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="94069-128">End of server support</span></span><br/>    | <span data-ttu-id="94069-129">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="94069-129">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="94069-130">標頭</span><span class="sxs-lookup"><span data-stu-id="94069-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="94069-131"><dt>Msident。h</dt></span><span class="sxs-lookup"><span data-stu-id="94069-131"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="94069-132">Idl</span><span class="sxs-lookup"><span data-stu-id="94069-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="94069-133"><dt>Msident .idl</dt></span><span class="sxs-lookup"><span data-stu-id="94069-133"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="94069-134">DLL</span><span class="sxs-lookup"><span data-stu-id="94069-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94069-135"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94069-135"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94069-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="94069-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94069-137">**IEnumUserIdentity**</span><span class="sxs-lookup"><span data-stu-id="94069-137">**IEnumUserIdentity**</span></span>](ienumuseridentity.md)
</dt> <dt>

[<span data-ttu-id="94069-138">**IEnumUserIdentity：： Skip**</span><span class="sxs-lookup"><span data-stu-id="94069-138">**IEnumUserIdentity::Skip**</span></span>](ienumuseridentity-skip.md)
</dt> <dt>

[<span data-ttu-id="94069-139">**IEnumUserIdentity：： Reset**</span><span class="sxs-lookup"><span data-stu-id="94069-139">**IEnumUserIdentity::Reset**</span></span>](ienumuseridentity-reset.md)
</dt> <dt>

[<span data-ttu-id="94069-140">**IEnumUserIdentity：： Next**</span><span class="sxs-lookup"><span data-stu-id="94069-140">**IEnumUserIdentity::Next**</span></span>](ienumuseridentity-next.md)
</dt> </dl>

 

 




