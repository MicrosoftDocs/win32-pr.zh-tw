---
description: IUserIdentity：： GetName 不受支援，而且可能會在未來變更或無法使用。 相反地，請使用使用者帳戶搭配快速切換使用者與遠端桌面。
ms.assetid: 4db24dd2-d2b8-4a58-9c16-0e721bc195da
title: 'IUserIdentity：： GetName 方法 (Msident .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity.GetName
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 88c0a3d08ff917c2cc9fd59f15e4c23fc22fc79d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973116"
---
# <a name="iuseridentitygetname-method"></a><span data-ttu-id="d1cd2-104">IUserIdentity：： GetName 方法</span><span class="sxs-lookup"><span data-stu-id="d1cd2-104">IUserIdentity::GetName method</span></span>

<span data-ttu-id="d1cd2-105">\[**IUserIdentity：： GetName** 不受支援，而且可能會在未來變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="d1cd2-105">\[**IUserIdentity::GetName** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="d1cd2-106">相反地，請使用 [使用者帳戶搭配快速切換使用者與遠端桌面](fastuserswitching.md)。\]</span><span class="sxs-lookup"><span data-stu-id="d1cd2-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="d1cd2-107">取得與此使用者識別相關聯的名稱。</span><span class="sxs-lookup"><span data-stu-id="d1cd2-107">Gets the name associated with this user identity.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1cd2-108">語法</span><span class="sxs-lookup"><span data-stu-id="d1cd2-108">Syntax</span></span>


```C++
HRESULT GetName(
  [in] WCHAR *pszName,
  [in] ULONG ulBuffSize
);
```



## <a name="parameters"></a><span data-ttu-id="d1cd2-109">參數</span><span class="sxs-lookup"><span data-stu-id="d1cd2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1cd2-110">*pszName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d1cd2-110">*pszName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1cd2-111">類型： \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="d1cd2-111">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="d1cd2-112">寬字元字串的指標，此字串會接收此使用者識別的名稱。</span><span class="sxs-lookup"><span data-stu-id="d1cd2-112">A pointer to a wide-character string that receives the name of this user identity.</span></span>

</dd> <dt>

<span data-ttu-id="d1cd2-113">_ulBuffSize \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d1cd2-113">_ulBuffSize\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1cd2-114">類型： **ULONG**</span><span class="sxs-lookup"><span data-stu-id="d1cd2-114">Type: **ULONG**</span></span>

<span data-ttu-id="d1cd2-115">值，指定 *pszName* 的大小。</span><span class="sxs-lookup"><span data-stu-id="d1cd2-115">A value that specifies the size of *pszName*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1cd2-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="d1cd2-116">Return value</span></span>

<span data-ttu-id="d1cd2-117">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="d1cd2-117">Type: **HRESULT**</span></span>

<span data-ttu-id="d1cd2-118">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="d1cd2-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d1cd2-119">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d1cd2-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1cd2-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="d1cd2-120">Requirements</span></span>



| <span data-ttu-id="d1cd2-121">需求</span><span class="sxs-lookup"><span data-stu-id="d1cd2-121">Requirement</span></span> | <span data-ttu-id="d1cd2-122">值</span><span class="sxs-lookup"><span data-stu-id="d1cd2-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d1cd2-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d1cd2-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d1cd2-124">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d1cd2-124">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="d1cd2-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d1cd2-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d1cd2-126">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d1cd2-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d1cd2-127">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="d1cd2-127">End of client support</span></span><br/>    | <span data-ttu-id="d1cd2-128">Windows XP</span><span class="sxs-lookup"><span data-stu-id="d1cd2-128">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="d1cd2-129">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="d1cd2-129">End of server support</span></span><br/>    | <span data-ttu-id="d1cd2-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d1cd2-130">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="d1cd2-131">標頭</span><span class="sxs-lookup"><span data-stu-id="d1cd2-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1cd2-132"><dt>Msident。h</dt></span><span class="sxs-lookup"><span data-stu-id="d1cd2-132"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="d1cd2-133">Idl</span><span class="sxs-lookup"><span data-stu-id="d1cd2-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d1cd2-134"><dt>Msident .idl</dt></span><span class="sxs-lookup"><span data-stu-id="d1cd2-134"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="d1cd2-135">DLL</span><span class="sxs-lookup"><span data-stu-id="d1cd2-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1cd2-136"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1cd2-136"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1cd2-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d1cd2-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1cd2-138">**IUserIdentity**</span><span class="sxs-lookup"><span data-stu-id="d1cd2-138">**IUserIdentity**</span></span>](iuseridentity.md)
</dt> <dt>

[<span data-ttu-id="d1cd2-139">**SetName**</span><span class="sxs-lookup"><span data-stu-id="d1cd2-139">**SetName**</span></span>](iuseridentity2-setname.md)
</dt> </dl>

 

 




