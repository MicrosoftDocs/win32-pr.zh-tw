---
description: 已取代。 抓取登錄中對應此使用者識別的索引鍵。
ms.assetid: eecf8b73-e86a-4274-8d9c-c601153f81db
title: 'IUserIdentity：： OpenIdentityRegKey 方法 (Msident .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity.OpenIdentityRegKey
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: f1d67918f4a9802e63682e0663994c1ea6a06200
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972320"
---
# <a name="iuseridentityopenidentityregkey-method"></a><span data-ttu-id="b23ed-104">IUserIdentity：： OpenIdentityRegKey 方法</span><span class="sxs-lookup"><span data-stu-id="b23ed-104">IUserIdentity::OpenIdentityRegKey method</span></span>

<span data-ttu-id="b23ed-105">\[**IUserIdentity：： OpenIdentityRegKey** 方法可用於 Windows 2000。</span><span class="sxs-lookup"><span data-stu-id="b23ed-105">\[The **IUserIdentity::OpenIdentityRegKey** method is available for use in Windows 2000.</span></span> <span data-ttu-id="b23ed-106">在 Windows XP 中，這項功能已由 [使用者帳戶取代為快速使用者切換和遠端桌面](fastuserswitching.md)，而且可能會在後續版本中變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="b23ed-106">In Windows XP, this functionality has been superseded by [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md), and might be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="b23ed-107">已取代。</span><span class="sxs-lookup"><span data-stu-id="b23ed-107">Deprecated.</span></span> <span data-ttu-id="b23ed-108">抓取登錄中對應此使用者識別的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="b23ed-108">Retrieves the key in the registry that corresponds to this user identity.</span></span>

## <a name="syntax"></a><span data-ttu-id="b23ed-109">語法</span><span class="sxs-lookup"><span data-stu-id="b23ed-109">Syntax</span></span>


```C++
HRESULT OpenIdentityRegKey(
  [in]  DWORD dwDesiredAccess,
  [out] HKEY  *phKey
);
```



## <a name="parameters"></a><span data-ttu-id="b23ed-110">參數</span><span class="sxs-lookup"><span data-stu-id="b23ed-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b23ed-111">*dwDesiredAccess* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b23ed-111">*dwDesiredAccess* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b23ed-112">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="b23ed-112">Type: **DWORD**</span></span>

<span data-ttu-id="b23ed-113">值，描述登錄機碼要求的存取層級。</span><span class="sxs-lookup"><span data-stu-id="b23ed-113">A value that describes the access level requested of the registry key.</span></span>

</dd> <dt>

<span data-ttu-id="b23ed-114">*phKey* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b23ed-114">*phKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b23ed-115">類型： \**HKEY \** _</span><span class="sxs-lookup"><span data-stu-id="b23ed-115">Type: \**HKEY\** _</span></span>

<span data-ttu-id="b23ed-116">接收登錄機碼的指標。</span><span class="sxs-lookup"><span data-stu-id="b23ed-116">A pointer that receives the registry key.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b23ed-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="b23ed-117">Return value</span></span>

<span data-ttu-id="b23ed-118">類型： _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="b23ed-118">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="b23ed-119">登錄要求的結果。</span><span class="sxs-lookup"><span data-stu-id="b23ed-119">The result of the registry request.</span></span> <span data-ttu-id="b23ed-120">如果成功，則會 **傳回 \_ [確定]**。</span><span class="sxs-lookup"><span data-stu-id="b23ed-120">If successful, it returns **S\_OK**.</span></span> <span data-ttu-id="b23ed-121">否則，它會傳回下列其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b23ed-121">Otherwise it will return one of the following error codes.</span></span>



| <span data-ttu-id="b23ed-122">傳回碼</span><span class="sxs-lookup"><span data-stu-id="b23ed-122">Return code</span></span>                                                                                            | <span data-ttu-id="b23ed-123">Description</span><span class="sxs-lookup"><span data-stu-id="b23ed-123">Description</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="b23ed-124"><dt>**E \_ \_ 找不 \_ 到身分識別**</dt></span><span class="sxs-lookup"><span data-stu-id="b23ed-124"><dt>**E\_IDENTITY\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="b23ed-125">此身分識別沒有相關聯的登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="b23ed-125">This identity does not have an associated registry key.</span></span><br/> |
| <dl> <span data-ttu-id="b23ed-126"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="b23ed-126"><dt>**E\_FAIL**</dt></span></span> </dl>                 | <span data-ttu-id="b23ed-127">無法存取登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="b23ed-127">The registry key was unable to be accessed.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="b23ed-128">備註</span><span class="sxs-lookup"><span data-stu-id="b23ed-128">Remarks</span></span>

<span data-ttu-id="b23ed-129">*DwDesiredAccess* 參數是標準的登錄存取安全描述項，描述您想要對登錄機碼取得的存取權。</span><span class="sxs-lookup"><span data-stu-id="b23ed-129">The *dwDesiredAccess* parameter is a standard registry access security descriptor that describes the access you want to gain to the registry key.</span></span> <span data-ttu-id="b23ed-130">如需登錄安全性的詳細資訊，包括此參數可接受的值清單，請參閱登錄機 [碼安全性和存取權限](../sysinfo/registry-key-security-and-access-rights.md)。</span><span class="sxs-lookup"><span data-stu-id="b23ed-130">For more information on registry security, including a list of acceptable values for this parameter, see [Registry Key Security and Access Rights](../sysinfo/registry-key-security-and-access-rights.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b23ed-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="b23ed-131">Requirements</span></span>



| <span data-ttu-id="b23ed-132">需求</span><span class="sxs-lookup"><span data-stu-id="b23ed-132">Requirement</span></span> | <span data-ttu-id="b23ed-133">值</span><span class="sxs-lookup"><span data-stu-id="b23ed-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b23ed-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b23ed-134">Minimum supported client</span></span><br/> | <span data-ttu-id="b23ed-135">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b23ed-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b23ed-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b23ed-136">Minimum supported server</span></span><br/> | <span data-ttu-id="b23ed-137">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b23ed-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="b23ed-138">標頭</span><span class="sxs-lookup"><span data-stu-id="b23ed-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="b23ed-139"><dt>Msident。h</dt></span><span class="sxs-lookup"><span data-stu-id="b23ed-139"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="b23ed-140">Idl</span><span class="sxs-lookup"><span data-stu-id="b23ed-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b23ed-141"><dt>Msident .idl</dt></span><span class="sxs-lookup"><span data-stu-id="b23ed-141"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="b23ed-142">DLL</span><span class="sxs-lookup"><span data-stu-id="b23ed-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b23ed-143"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b23ed-143"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b23ed-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b23ed-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b23ed-145">**IUserIdentity**</span><span class="sxs-lookup"><span data-stu-id="b23ed-145">**IUserIdentity**</span></span>](iuseridentity.md)
</dt> <dt>

[<span data-ttu-id="b23ed-146">**IUserIdentity::GetIdentityFolder**</span><span class="sxs-lookup"><span data-stu-id="b23ed-146">**IUserIdentity::GetIdentityFolder**</span></span>](iuseridentity-getidentityfolder.md)
</dt> </dl>

 

 
