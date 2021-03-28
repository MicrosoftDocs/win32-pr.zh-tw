---
description: 不支援 ChangePassword，未來可能會變更或無法使用。 相反地，請使用使用者帳戶搭配快速切換使用者與遠端桌面。
ms.assetid: bc8813a0-9b40-481f-9ab3-cf6a9a0796d2
title: 'IUserIdentity2：： ChangePassword 方法 (Msident .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity2.ChangePassword
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: dd4b858924e4b042b3d7a0636d90eb582e9506df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972317"
---
# <a name="iuseridentity2changepassword-method"></a><span data-ttu-id="9b908-104">IUserIdentity2：： ChangePassword 方法</span><span class="sxs-lookup"><span data-stu-id="9b908-104">IUserIdentity2::ChangePassword method</span></span>

<span data-ttu-id="9b908-105">\[不支援 **ChangePassword** ，未來可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="9b908-105">\[**ChangePassword** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="9b908-106">相反地，請使用 [使用者帳戶搭配快速切換使用者與遠端桌面](fastuserswitching.md)。\]</span><span class="sxs-lookup"><span data-stu-id="9b908-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="9b908-107">為身分識別設定新的密碼。</span><span class="sxs-lookup"><span data-stu-id="9b908-107">Sets a new password for the identity.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b908-108">語法</span><span class="sxs-lookup"><span data-stu-id="9b908-108">Syntax</span></span>


```C++
HRESULT ChangePassword(
  [in] WCHAR *szOldPass,
  [in] WCHAR *szNewPass
);
```



## <a name="parameters"></a><span data-ttu-id="9b908-109">參數</span><span class="sxs-lookup"><span data-stu-id="9b908-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b908-110">*szOldPass* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9b908-110">*szOldPass* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b908-111">類型： \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="9b908-111">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="9b908-112">寬字元字串，其中包含目前與身分識別相關聯的密碼。</span><span class="sxs-lookup"><span data-stu-id="9b908-112">The wide-character string that contains the password currently associated with the identity.</span></span>

</dd> <dt>

<span data-ttu-id="9b908-113">_szNewPass \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9b908-113">_szNewPass\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b908-114">類型： \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="9b908-114">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="9b908-115">包含要與身分識別相關聯之新密碼的寬字元字串。</span><span class="sxs-lookup"><span data-stu-id="9b908-115">The wide-character string that contains the new password to be associated with the identity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b908-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="9b908-116">Return value</span></span>

<span data-ttu-id="9b908-117">類型： _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="9b908-117">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="9b908-118">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="9b908-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9b908-119">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="9b908-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b908-120">備註</span><span class="sxs-lookup"><span data-stu-id="9b908-120">Remarks</span></span>

<span data-ttu-id="9b908-121">*SzOldPass* 的值必須符合身分識別的目前密碼，才能套用 *szNewPass* 。</span><span class="sxs-lookup"><span data-stu-id="9b908-121">The value of *szOldPass* must match the current password of the identity for *szNewPass* to be applied.</span></span> <span data-ttu-id="9b908-122">*SzOldPass* 的值不正確會導致 E 的傳回值 \_ 失敗。</span><span class="sxs-lookup"><span data-stu-id="9b908-122">An incorrect value of *szOldPass* will result in a return value of E\_FAIL.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b908-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="9b908-123">Requirements</span></span>



| <span data-ttu-id="9b908-124">需求</span><span class="sxs-lookup"><span data-stu-id="9b908-124">Requirement</span></span> | <span data-ttu-id="9b908-125">值</span><span class="sxs-lookup"><span data-stu-id="9b908-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9b908-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9b908-126">Minimum supported client</span></span><br/> | <span data-ttu-id="9b908-127">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9b908-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="9b908-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9b908-128">Minimum supported server</span></span><br/> | <span data-ttu-id="9b908-129">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9b908-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="9b908-130">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="9b908-130">End of client support</span></span><br/>    | <span data-ttu-id="9b908-131">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="9b908-131">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="9b908-132">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="9b908-132">End of server support</span></span><br/>    | <span data-ttu-id="9b908-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9b908-133">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="9b908-134">標頭</span><span class="sxs-lookup"><span data-stu-id="9b908-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b908-135"><dt>Msident。h</dt></span><span class="sxs-lookup"><span data-stu-id="9b908-135"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="9b908-136">Idl</span><span class="sxs-lookup"><span data-stu-id="9b908-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9b908-137"><dt>Msident .idl</dt></span><span class="sxs-lookup"><span data-stu-id="9b908-137"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="9b908-138">DLL</span><span class="sxs-lookup"><span data-stu-id="9b908-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b908-139"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b908-139"><dt>Msident.dll</dt></span></span> </dl> |



 

 




