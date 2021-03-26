---
description: IUserIdentity2：： SetName 不受支援，而且可能會在未來變更或無法使用。 相反地，請使用使用者帳戶搭配快速切換使用者與遠端桌面。
ms.assetid: 1c9c3beb-fa1c-4b4d-9cfd-656b97949036
title: 'IUserIdentity2：： SetName 方法 (Msident .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity2.SetName
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 0b0fd06ef4b582987e41c2343f2d4596db6b8528
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973392"
---
# <a name="iuseridentity2setname-method"></a><span data-ttu-id="2c712-104">IUserIdentity2：： SetName 方法</span><span class="sxs-lookup"><span data-stu-id="2c712-104">IUserIdentity2::SetName method</span></span>

<span data-ttu-id="2c712-105">\[**IUserIdentity2：： SetName** 不受支援，而且可能會在未來變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="2c712-105">\[**IUserIdentity2::SetName** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="2c712-106">相反地，請使用 [使用者帳戶搭配快速切換使用者與遠端桌面](fastuserswitching.md)。\]</span><span class="sxs-lookup"><span data-stu-id="2c712-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="2c712-107">設定身分識別的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="2c712-107">Sets the display name of the identity.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c712-108">語法</span><span class="sxs-lookup"><span data-stu-id="2c712-108">Syntax</span></span>


```C++
HRESULT SetName(
  [in] WCHAR *pszName
);
```



## <a name="parameters"></a><span data-ttu-id="2c712-109">參數</span><span class="sxs-lookup"><span data-stu-id="2c712-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c712-110">*pszName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2c712-110">*pszName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c712-111">類型： \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="2c712-111">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="2c712-112">寬字元字串，其中包含身分識別的新名稱。</span><span class="sxs-lookup"><span data-stu-id="2c712-112">The wide-character string that contains the new name of the identity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c712-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="2c712-113">Return value</span></span>

<span data-ttu-id="2c712-114">類型： _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="2c712-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="2c712-115">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="2c712-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2c712-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="2c712-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c712-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="2c712-117">Requirements</span></span>



| <span data-ttu-id="2c712-118">需求</span><span class="sxs-lookup"><span data-stu-id="2c712-118">Requirement</span></span> | <span data-ttu-id="2c712-119">值</span><span class="sxs-lookup"><span data-stu-id="2c712-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2c712-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2c712-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2c712-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2c712-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="2c712-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2c712-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2c712-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2c712-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="2c712-124">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="2c712-124">End of client support</span></span><br/>    | <span data-ttu-id="2c712-125">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="2c712-125">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="2c712-126">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="2c712-126">End of server support</span></span><br/>    | <span data-ttu-id="2c712-127">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2c712-127">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="2c712-128">標頭</span><span class="sxs-lookup"><span data-stu-id="2c712-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c712-129"><dt>Msident。h</dt></span><span class="sxs-lookup"><span data-stu-id="2c712-129"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="2c712-130">Idl</span><span class="sxs-lookup"><span data-stu-id="2c712-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2c712-131"><dt>Msident .idl</dt></span><span class="sxs-lookup"><span data-stu-id="2c712-131"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="2c712-132">DLL</span><span class="sxs-lookup"><span data-stu-id="2c712-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c712-133"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c712-133"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c712-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2c712-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c712-135">**IUserIdentity2**</span><span class="sxs-lookup"><span data-stu-id="2c712-135">**IUserIdentity2**</span></span>](iuseridentity2.md)
</dt> <dt>

[<span data-ttu-id="2c712-136">**GetName**</span><span class="sxs-lookup"><span data-stu-id="2c712-136">**GetName**</span></span>](iuseridentity-getname.md)
</dt> </dl>

 

 




