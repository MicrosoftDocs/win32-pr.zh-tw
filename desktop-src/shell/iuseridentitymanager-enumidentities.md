---
description: IUserIdentityManager：： EnumIdentities 不受支援，而且可能會在未來變更或無法使用。 相反地，請使用使用者帳戶搭配快速切換使用者與遠端桌面。
ms.assetid: 8111fbcd-dc4d-45cb-83e0-3c2cd7c4df27
title: 'IUserIdentityManager：： EnumIdentities 方法 (Msident .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentityManager.EnumIdentities
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 3109867651b69e311639d8b2e70e5f02e33a3dc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111717"
---
# <a name="iuseridentitymanagerenumidentities-method"></a><span data-ttu-id="a9c4b-104">IUserIdentityManager：： EnumIdentities 方法</span><span class="sxs-lookup"><span data-stu-id="a9c4b-104">IUserIdentityManager::EnumIdentities method</span></span>

<span data-ttu-id="a9c4b-105">\[**IUserIdentityManager：： EnumIdentities** 不受支援，而且可能會在未來變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="a9c4b-105">\[**IUserIdentityManager::EnumIdentities** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="a9c4b-106">相反地，請使用 [使用者帳戶搭配快速切換使用者與遠端桌面](fastuserswitching.md)。\]</span><span class="sxs-lookup"><span data-stu-id="a9c4b-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="a9c4b-107">取得 [**IEnumUserIdentity**](ienumuseridentity.md) 物件，可用來列舉系統上存在的使用者身分識別。</span><span class="sxs-lookup"><span data-stu-id="a9c4b-107">Gets an [**IEnumUserIdentity**](ienumuseridentity.md) object, which can be used to enumerate through the user identities present on the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9c4b-108">語法</span><span class="sxs-lookup"><span data-stu-id="a9c4b-108">Syntax</span></span>


```C++
HRESULT EnumIdentities(
  [out] IEnumUserIdentity **ppEnumUser
);
```



## <a name="parameters"></a><span data-ttu-id="a9c4b-109">參數</span><span class="sxs-lookup"><span data-stu-id="a9c4b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9c4b-110">*ppEnumUser* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a9c4b-110">*ppEnumUser* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a9c4b-111">類型： **[ **IEnumUserIdentity**](ienumuseridentity.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="a9c4b-111">Type: **[**IEnumUserIdentity**](ienumuseridentity.md)\*\***</span></span>

<span data-ttu-id="a9c4b-112">新身分識別列舉物件之指標的位址。</span><span class="sxs-lookup"><span data-stu-id="a9c4b-112">The address of the pointer to the new identity enumeration object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9c4b-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="a9c4b-113">Return value</span></span>

<span data-ttu-id="a9c4b-114">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="a9c4b-114">Type: **HRESULT**</span></span>

<span data-ttu-id="a9c4b-115">抓取作業的結果。</span><span class="sxs-lookup"><span data-stu-id="a9c4b-115">The result of the retrieval operation.</span></span> <span data-ttu-id="a9c4b-116">如果成功，則會傳回 \_ [確定]。</span><span class="sxs-lookup"><span data-stu-id="a9c4b-116">If successful, it returns S\_OK.</span></span> <span data-ttu-id="a9c4b-117">如果無法建立列舉物件，它會傳回 E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="a9c4b-117">If the enumeration object could not be created, it returns E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9c4b-118">備註</span><span class="sxs-lookup"><span data-stu-id="a9c4b-118">Remarks</span></span>

<span data-ttu-id="a9c4b-119">這個方法適用于反覆運算系統上的身分識別清單。</span><span class="sxs-lookup"><span data-stu-id="a9c4b-119">This method is useful for iteration over the list of identities on the system.</span></span> <span data-ttu-id="a9c4b-120">若要在不存取清單的情況下，透過 cookie 取得單一身分識別，請呼叫 [**IUserIdentityManager：： GetIdentityByCookie**](iuseridentitymanager-getidentitybycookie.md)。</span><span class="sxs-lookup"><span data-stu-id="a9c4b-120">To retrieve a single identity by its cookie without accessing the list, call [**IUserIdentityManager::GetIdentityByCookie**](iuseridentitymanager-getidentitybycookie.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a9c4b-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="a9c4b-121">Requirements</span></span>



| <span data-ttu-id="a9c4b-122">需求</span><span class="sxs-lookup"><span data-stu-id="a9c4b-122">Requirement</span></span> | <span data-ttu-id="a9c4b-123">值</span><span class="sxs-lookup"><span data-stu-id="a9c4b-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a9c4b-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a9c4b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a9c4b-125">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a9c4b-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a9c4b-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a9c4b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a9c4b-127">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a9c4b-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a9c4b-128">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="a9c4b-128">End of client support</span></span><br/>    | <span data-ttu-id="a9c4b-129">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="a9c4b-129">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="a9c4b-130">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="a9c4b-130">End of server support</span></span><br/>    | <span data-ttu-id="a9c4b-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a9c4b-131">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="a9c4b-132">標頭</span><span class="sxs-lookup"><span data-stu-id="a9c4b-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9c4b-133"><dt>Msident。h</dt></span><span class="sxs-lookup"><span data-stu-id="a9c4b-133"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="a9c4b-134">Idl</span><span class="sxs-lookup"><span data-stu-id="a9c4b-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a9c4b-135"><dt>Msident .idl</dt></span><span class="sxs-lookup"><span data-stu-id="a9c4b-135"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="a9c4b-136">DLL</span><span class="sxs-lookup"><span data-stu-id="a9c4b-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a9c4b-137"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a9c4b-137"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9c4b-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a9c4b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9c4b-139">**IUserIdentityManager**</span><span class="sxs-lookup"><span data-stu-id="a9c4b-139">**IUserIdentityManager**</span></span>](iuseridentitymanager.md)
</dt> <dt>

[<span data-ttu-id="a9c4b-140">**IEnumUserIdentity**</span><span class="sxs-lookup"><span data-stu-id="a9c4b-140">**IEnumUserIdentity**</span></span>](ienumuseridentity.md)
</dt> <dt>

[<span data-ttu-id="a9c4b-141">**IUserIdentityManager::GetIdentityByCookie**</span><span class="sxs-lookup"><span data-stu-id="a9c4b-141">**IUserIdentityManager::GetIdentityByCookie**</span></span>](iuseridentitymanager-getidentitybycookie.md)
</dt> </dl>

 

 




