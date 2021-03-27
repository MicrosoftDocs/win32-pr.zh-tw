---
description: GetIdentityFolder 不受支援，未來可能會變更或無法使用。 相反地，請使用使用者帳戶搭配快速切換使用者與遠端桌面。
ms.assetid: cd3370a2-b393-4cb9-ad9c-a46086987aaa
title: 'IUserIdentity：： GetIdentityFolder 方法 (Msident .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity.GetIdentityFolder
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 9f2644570bb7ccc2ae5bee8a37d4471ffb65861a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972324"
---
# <a name="iuseridentitygetidentityfolder-method"></a><span data-ttu-id="5b97e-104">IUserIdentity：： GetIdentityFolder 方法</span><span class="sxs-lookup"><span data-stu-id="5b97e-104">IUserIdentity::GetIdentityFolder method</span></span>

<span data-ttu-id="5b97e-105">\[**GetIdentityFolder** 不受支援，未來可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="5b97e-105">\[**GetIdentityFolder** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="5b97e-106">相反地，請使用 [使用者帳戶搭配快速切換使用者與遠端桌面](fastuserswitching.md)。\]</span><span class="sxs-lookup"><span data-stu-id="5b97e-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="5b97e-107">取得與此身分識別相關聯的檔案資料夾。</span><span class="sxs-lookup"><span data-stu-id="5b97e-107">Gets the file folder associated with this identity.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b97e-108">語法</span><span class="sxs-lookup"><span data-stu-id="5b97e-108">Syntax</span></span>


```C++
HRESULT GetIdentityFolder(
  [in] DWORD dwFlags,
  [in] WCHAR *pszPath,
  [in] ULONG ulBuffSize
);
```



## <a name="parameters"></a><span data-ttu-id="5b97e-109">參數</span><span class="sxs-lookup"><span data-stu-id="5b97e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b97e-110">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5b97e-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b97e-111">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="5b97e-111">Type: **DWORD**</span></span>

<span data-ttu-id="5b97e-112">必要。</span><span class="sxs-lookup"><span data-stu-id="5b97e-112">Required.</span></span> <span data-ttu-id="5b97e-113">值，這個值會指定與此身分識別相關聯的資料夾是否為漫遊。</span><span class="sxs-lookup"><span data-stu-id="5b97e-113">A value that specifies whether the folder associated with this identity is roaming.</span></span> <span data-ttu-id="5b97e-114">必須是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="5b97e-114">Must be one of the following values.</span></span>

<dt>



 <span data-ttu-id="5b97e-115"> (GIF \_ 漫遊 \_ 資料夾) </span><span class="sxs-lookup"><span data-stu-id="5b97e-115">(GIF\_ROAMING\_FOLDER)</span></span>


</dt> <dd>

<span data-ttu-id="5b97e-116">此資料夾為漫遊。</span><span class="sxs-lookup"><span data-stu-id="5b97e-116">The folder is roaming.</span></span>

</dd> <dt>



 <span data-ttu-id="5b97e-117"> (GIF \_ 非 \_ 漫遊 \_ 資料夾) </span><span class="sxs-lookup"><span data-stu-id="5b97e-117">(GIF\_NON\_ROAMING\_FOLDER)</span></span>


</dt> <dd>

<span data-ttu-id="5b97e-118">資料夾是本機資料夾。</span><span class="sxs-lookup"><span data-stu-id="5b97e-118">The folder is local.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="5b97e-119">*pszPath* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5b97e-119">*pszPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b97e-120">類型： \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="5b97e-120">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="5b97e-121">接收資料夾路徑的寬字元字串指標。</span><span class="sxs-lookup"><span data-stu-id="5b97e-121">A pointer to a wide-character string that receives the folder path.</span></span>

</dd> <dt>

<span data-ttu-id="5b97e-122">_ulBuffSize \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5b97e-122">_ulBuffSize\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b97e-123">類型： **ULONG**</span><span class="sxs-lookup"><span data-stu-id="5b97e-123">Type: **ULONG**</span></span>

<span data-ttu-id="5b97e-124">值，指定 *pszPath* 的大小。</span><span class="sxs-lookup"><span data-stu-id="5b97e-124">A value that specifies the size of *pszPath*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b97e-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="5b97e-125">Return value</span></span>

<span data-ttu-id="5b97e-126">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="5b97e-126">Type: **HRESULT**</span></span>

<span data-ttu-id="5b97e-127">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="5b97e-127">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5b97e-128">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="5b97e-128">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b97e-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="5b97e-129">Requirements</span></span>



| <span data-ttu-id="5b97e-130">需求</span><span class="sxs-lookup"><span data-stu-id="5b97e-130">Requirement</span></span> | <span data-ttu-id="5b97e-131">值</span><span class="sxs-lookup"><span data-stu-id="5b97e-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5b97e-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5b97e-132">Minimum supported client</span></span><br/> | <span data-ttu-id="5b97e-133">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5b97e-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="5b97e-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5b97e-134">Minimum supported server</span></span><br/> | <span data-ttu-id="5b97e-135">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5b97e-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="5b97e-136">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="5b97e-136">End of client support</span></span><br/>    | <span data-ttu-id="5b97e-137">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="5b97e-137">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="5b97e-138">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="5b97e-138">End of server support</span></span><br/>    | <span data-ttu-id="5b97e-139">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5b97e-139">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="5b97e-140">標頭</span><span class="sxs-lookup"><span data-stu-id="5b97e-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b97e-141"><dt>Msident。h</dt></span><span class="sxs-lookup"><span data-stu-id="5b97e-141"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="5b97e-142">Idl</span><span class="sxs-lookup"><span data-stu-id="5b97e-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5b97e-143"><dt>Msident .idl</dt></span><span class="sxs-lookup"><span data-stu-id="5b97e-143"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="5b97e-144">DLL</span><span class="sxs-lookup"><span data-stu-id="5b97e-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5b97e-145"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b97e-145"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b97e-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5b97e-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b97e-147">**IUserIdentity**</span><span class="sxs-lookup"><span data-stu-id="5b97e-147">**IUserIdentity**</span></span>](iuseridentity.md)
</dt> <dt>

[<span data-ttu-id="5b97e-148">**IUserIdentity::OpenIdentityRegKey**</span><span class="sxs-lookup"><span data-stu-id="5b97e-148">**IUserIdentity::OpenIdentityRegKey**</span></span>](iuseridentity-openidentityregkey.md)
</dt> </dl>

 

 




