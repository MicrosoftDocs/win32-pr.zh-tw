---
description: GetOrdinal 不受支援，未來可能會變更或無法使用。 相反地，請使用使用者帳戶搭配快速切換使用者與遠端桌面。
ms.assetid: 20b1c1d0-b09f-43a8-9026-9cdbac28c108
title: 'IUserIdentity2：： GetOrdinal 方法 (Msident .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity2.GetOrdinal
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: f5a7e875e92342363722858b3ac714171cb547b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973396"
---
# <a name="iuseridentity2getordinal-method"></a><span data-ttu-id="41d54-104">IUserIdentity2：： GetOrdinal 方法</span><span class="sxs-lookup"><span data-stu-id="41d54-104">IUserIdentity2::GetOrdinal method</span></span>

<span data-ttu-id="41d54-105">\[**GetOrdinal** 不受支援，未來可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="41d54-105">\[**GetOrdinal** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="41d54-106">相反地，請使用 [使用者帳戶搭配快速切換使用者與遠端桌面](fastuserswitching.md)。\]</span><span class="sxs-lookup"><span data-stu-id="41d54-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="41d54-107">取得此身分識別的序號。</span><span class="sxs-lookup"><span data-stu-id="41d54-107">Gets the ordinal number for this identity.</span></span>

## <a name="syntax"></a><span data-ttu-id="41d54-108">語法</span><span class="sxs-lookup"><span data-stu-id="41d54-108">Syntax</span></span>


```C++
HRESULT GetOrdinal(
  [out] DWORD *dwOrdinal
);
```



## <a name="parameters"></a><span data-ttu-id="41d54-109">參數</span><span class="sxs-lookup"><span data-stu-id="41d54-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41d54-110">*dwOrdinal* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="41d54-110">*dwOrdinal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="41d54-111">類型： \**DWORD \** _</span><span class="sxs-lookup"><span data-stu-id="41d54-111">Type: \**DWORD\** _</span></span>

<span data-ttu-id="41d54-112">_ *DWORD*\* 值的指標，此值會接收此身分識別的序數。</span><span class="sxs-lookup"><span data-stu-id="41d54-112">A pointer to a _ *DWORD*\* value that receives the ordinal number for this identity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41d54-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="41d54-113">Return value</span></span>

<span data-ttu-id="41d54-114">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="41d54-114">Type: **HRESULT**</span></span>

<span data-ttu-id="41d54-115">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="41d54-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="41d54-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="41d54-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="41d54-117">備註</span><span class="sxs-lookup"><span data-stu-id="41d54-117">Remarks</span></span>

<span data-ttu-id="41d54-118">序數會決定身分識別清單中的身分識別順序，但可能不會在身分識別的整個作業中保存。</span><span class="sxs-lookup"><span data-stu-id="41d54-118">The ordinal determines the order of the identities in the identity list, but may not persist throughout operations on the identities.</span></span> <span data-ttu-id="41d54-119">若要取得身分識別的唯一值，請呼叫 [**system.windows.application.getcookie**](iuseridentity-getcookie.md)。</span><span class="sxs-lookup"><span data-stu-id="41d54-119">To get a unique value for an identity, call [**GetCookie**](iuseridentity-getcookie.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="41d54-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="41d54-120">Requirements</span></span>



| <span data-ttu-id="41d54-121">需求</span><span class="sxs-lookup"><span data-stu-id="41d54-121">Requirement</span></span> | <span data-ttu-id="41d54-122">值</span><span class="sxs-lookup"><span data-stu-id="41d54-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="41d54-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="41d54-123">Minimum supported client</span></span><br/> | <span data-ttu-id="41d54-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="41d54-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="41d54-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="41d54-125">Minimum supported server</span></span><br/> | <span data-ttu-id="41d54-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="41d54-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="41d54-127">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="41d54-127">End of client support</span></span><br/>    | <span data-ttu-id="41d54-128">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="41d54-128">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="41d54-129">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="41d54-129">End of server support</span></span><br/>    | <span data-ttu-id="41d54-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="41d54-130">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="41d54-131">標頭</span><span class="sxs-lookup"><span data-stu-id="41d54-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="41d54-132"><dt>Msident。h</dt></span><span class="sxs-lookup"><span data-stu-id="41d54-132"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="41d54-133">Idl</span><span class="sxs-lookup"><span data-stu-id="41d54-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="41d54-134"><dt>Msident .idl</dt></span><span class="sxs-lookup"><span data-stu-id="41d54-134"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="41d54-135">DLL</span><span class="sxs-lookup"><span data-stu-id="41d54-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41d54-136"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41d54-136"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41d54-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="41d54-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41d54-138">**IUserIdentity2**</span><span class="sxs-lookup"><span data-stu-id="41d54-138">**IUserIdentity2**</span></span>](iuseridentity2.md)
</dt> <dt>

[<span data-ttu-id="41d54-139">**System.windows.application.getcookie**</span><span class="sxs-lookup"><span data-stu-id="41d54-139">**GetCookie**</span></span>](iuseridentity-getcookie.md)
</dt> </dl>

 

 




