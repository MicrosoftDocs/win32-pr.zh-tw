---
description: System.windows.application.getcookie 不受支援，未來可能會變更或無法使用。 相反地，請使用使用者帳戶搭配快速切換使用者與遠端桌面。
ms.assetid: 4a743d64-9af3-43cf-9a9f-d808676ab337
title: 'IUserIdentity：： System.windows.application.getcookie 方法 (Msident .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity.GetCookie
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 96cafb13f2c90c41e4aa6dcaaa72cf052757d0ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972329"
---
# <a name="iuseridentitygetcookie-method"></a><span data-ttu-id="1344b-104">IUserIdentity：： System.windows.application.getcookie 方法</span><span class="sxs-lookup"><span data-stu-id="1344b-104">IUserIdentity::GetCookie method</span></span>

<span data-ttu-id="1344b-105">\[**System.windows.application.getcookie** 不受支援，未來可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="1344b-105">\[**GetCookie** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="1344b-106">相反地，請使用 [使用者帳戶搭配快速切換使用者與遠端桌面](fastuserswitching.md)。\]</span><span class="sxs-lookup"><span data-stu-id="1344b-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="1344b-107">取得用來唯一識別此使用者識別的 cookie。</span><span class="sxs-lookup"><span data-stu-id="1344b-107">Gets the cookie used to uniquely identify this user identity.</span></span>

## <a name="syntax"></a><span data-ttu-id="1344b-108">語法</span><span class="sxs-lookup"><span data-stu-id="1344b-108">Syntax</span></span>


```C++
HRESULT GetCookie(
  [out] GUID *puidCookie
);
```



## <a name="parameters"></a><span data-ttu-id="1344b-109">參數</span><span class="sxs-lookup"><span data-stu-id="1344b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1344b-110">*puidCookie* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="1344b-110">*puidCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1344b-111">類型： \**GUID \** _</span><span class="sxs-lookup"><span data-stu-id="1344b-111">Type: \**GUID\** _</span></span>

<span data-ttu-id="1344b-112">_ *GUID*\* 值的指標，此值會接收用來唯一識別此使用者身分識別的 cookie。</span><span class="sxs-lookup"><span data-stu-id="1344b-112">A pointer to a _ *GUID*\* value that receives the cookie used to uniquely identify this user identity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1344b-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="1344b-113">Return value</span></span>

<span data-ttu-id="1344b-114">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="1344b-114">Type: **HRESULT**</span></span>

<span data-ttu-id="1344b-115">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="1344b-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1344b-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="1344b-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="1344b-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="1344b-117">Requirements</span></span>



| <span data-ttu-id="1344b-118">需求</span><span class="sxs-lookup"><span data-stu-id="1344b-118">Requirement</span></span> | <span data-ttu-id="1344b-119">值</span><span class="sxs-lookup"><span data-stu-id="1344b-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1344b-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1344b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1344b-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1344b-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="1344b-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1344b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1344b-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1344b-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="1344b-124">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="1344b-124">End of client support</span></span><br/>    | <span data-ttu-id="1344b-125">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="1344b-125">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="1344b-126">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="1344b-126">End of server support</span></span><br/>    | <span data-ttu-id="1344b-127">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1344b-127">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="1344b-128">標頭</span><span class="sxs-lookup"><span data-stu-id="1344b-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="1344b-129"><dt>Msident。h</dt></span><span class="sxs-lookup"><span data-stu-id="1344b-129"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="1344b-130">Idl</span><span class="sxs-lookup"><span data-stu-id="1344b-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1344b-131"><dt>Msident .idl</dt></span><span class="sxs-lookup"><span data-stu-id="1344b-131"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="1344b-132">DLL</span><span class="sxs-lookup"><span data-stu-id="1344b-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1344b-133"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1344b-133"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1344b-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1344b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1344b-135">**IUserIdentity**</span><span class="sxs-lookup"><span data-stu-id="1344b-135">**IUserIdentity**</span></span>](iuseridentity.md)
</dt> <dt>

[<span data-ttu-id="1344b-136">**GetOrdinal**</span><span class="sxs-lookup"><span data-stu-id="1344b-136">**GetOrdinal**</span></span>](iuseridentity2-getordinal.md)
</dt> </dl>

 

 




