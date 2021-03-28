---
description: GetIdentityByCookie 不受支援，未來可能會變更或無法使用。 相反地，請使用使用者帳戶搭配快速切換使用者與遠端桌面。
ms.assetid: c2f549ac-e13d-4198-864f-7f5fbec30c72
title: 'IUserIdentityManager：： GetIdentityByCookie 方法 (Msident .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentityManager.GetIdentityByCookie
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: eb4e5ad5bda349a5b1650b090abc44a9fd1e6332
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510771"
---
# <a name="iuseridentitymanagergetidentitybycookie-method"></a><span data-ttu-id="c2521-104">IUserIdentityManager：： GetIdentityByCookie 方法</span><span class="sxs-lookup"><span data-stu-id="c2521-104">IUserIdentityManager::GetIdentityByCookie method</span></span>

<span data-ttu-id="c2521-105">\[**GetIdentityByCookie** 不受支援，未來可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="c2521-105">\[**GetIdentityByCookie** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="c2521-106">相反地，請使用 [使用者帳戶搭配快速切換使用者與遠端桌面](fastuserswitching.md)。\]</span><span class="sxs-lookup"><span data-stu-id="c2521-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="c2521-107">依據用來唯一識別它的 cookie 取得特定使用者身分識別。</span><span class="sxs-lookup"><span data-stu-id="c2521-107">Gets a specific user identity by the cookie used to uniquely identify it.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2521-108">語法</span><span class="sxs-lookup"><span data-stu-id="c2521-108">Syntax</span></span>


```C++
HRESULT GetIdentityByCookie(
  [in]  GUID          *uidCookie,
  [out] IUserIdentity **ppIdentity
);
```



## <a name="parameters"></a><span data-ttu-id="c2521-109">參數</span><span class="sxs-lookup"><span data-stu-id="c2521-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2521-110">*uidCookie* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c2521-110">*uidCookie* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2521-111">類型： \**GUID \** _</span><span class="sxs-lookup"><span data-stu-id="c2521-111">Type: \**GUID\** _</span></span>

<span data-ttu-id="c2521-112">_ *GUID*\* 值的位址，代表您要取得之身分識別的 cookie。</span><span class="sxs-lookup"><span data-stu-id="c2521-112">The address of a _ *GUID*\* value that represents the cookie for the identity you want to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="c2521-113">*ppIdentity* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c2521-113">*ppIdentity* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c2521-114">類型： **[ **IUserIdentity**](iuseridentity.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="c2521-114">Type: **[**IUserIdentity**](iuseridentity.md)\*\***</span></span>

<span data-ttu-id="c2521-115">將接收使用者識別物件之指標的位址。</span><span class="sxs-lookup"><span data-stu-id="c2521-115">The address of the pointer that will receive the user identity object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2521-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="c2521-116">Return value</span></span>

<span data-ttu-id="c2521-117">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c2521-117">Type: **HRESULT**</span></span>

<span data-ttu-id="c2521-118">抓取要求的結果。</span><span class="sxs-lookup"><span data-stu-id="c2521-118">The result of the retrieval request.</span></span> <span data-ttu-id="c2521-119">如果成功，則會傳回 \_ [確定]。</span><span class="sxs-lookup"><span data-stu-id="c2521-119">If successful, it returns S\_OK.</span></span> <span data-ttu-id="c2521-120">否則，它會傳回下列其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c2521-120">Otherwise it will return one of the following error codes.</span></span>



| <span data-ttu-id="c2521-121">傳回碼</span><span class="sxs-lookup"><span data-stu-id="c2521-121">Return code</span></span>                                                                                            | <span data-ttu-id="c2521-122">Description</span><span class="sxs-lookup"><span data-stu-id="c2521-122">Description</span></span>                                               |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <span data-ttu-id="c2521-123"><dt>**E \_ \_ 找不 \_ 到身分識別**</dt></span><span class="sxs-lookup"><span data-stu-id="c2521-123"><dt>**E\_IDENTITY\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="c2521-124">找不到要求的身分識別。</span><span class="sxs-lookup"><span data-stu-id="c2521-124">The identity requested could not be found.</span></span><br/>     |
| <dl> <span data-ttu-id="c2521-125"><dt>**E 身分識別 \_ \_ 已停用**</dt></span><span class="sxs-lookup"><span data-stu-id="c2521-125"><dt>**E\_IDENTITIES\_DISABLED**</dt></span></span> </dl> | <span data-ttu-id="c2521-126">系統上的身分識別管理已停用。</span><span class="sxs-lookup"><span data-stu-id="c2521-126">Identity management is disabled on the system.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c2521-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="c2521-127">Requirements</span></span>



| <span data-ttu-id="c2521-128">需求</span><span class="sxs-lookup"><span data-stu-id="c2521-128">Requirement</span></span> | <span data-ttu-id="c2521-129">值</span><span class="sxs-lookup"><span data-stu-id="c2521-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c2521-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c2521-130">Minimum supported client</span></span><br/> | <span data-ttu-id="c2521-131">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c2521-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c2521-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c2521-132">Minimum supported server</span></span><br/> | <span data-ttu-id="c2521-133">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c2521-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c2521-134">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="c2521-134">End of client support</span></span><br/>    | <span data-ttu-id="c2521-135">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="c2521-135">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="c2521-136">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="c2521-136">End of server support</span></span><br/>    | <span data-ttu-id="c2521-137">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c2521-137">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="c2521-138">標頭</span><span class="sxs-lookup"><span data-stu-id="c2521-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2521-139"><dt>Msident。h</dt></span><span class="sxs-lookup"><span data-stu-id="c2521-139"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="c2521-140">Idl</span><span class="sxs-lookup"><span data-stu-id="c2521-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c2521-141"><dt>Msident .idl</dt></span><span class="sxs-lookup"><span data-stu-id="c2521-141"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="c2521-142">DLL</span><span class="sxs-lookup"><span data-stu-id="c2521-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2521-143"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c2521-143"><dt>Msident.dll</dt></span></span> </dl> |



 

 




