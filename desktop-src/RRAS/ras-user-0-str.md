---
title: 'RAS_USER_0 結構 (Rassapi .h) '
description: '\_ \_ RasAdminUserSetInfo 和 RasAdminUserGetInfo 函數中會使用 RAS 使用者0結構來指定使用者的相關資訊。'
ms.assetid: a2d4a935-f46d-4bc2-ada8-beaa3ac74834
keywords:
- RAS_USER_0 結構 RAS
- PRAS_USER_0 結構指標 RAS
topic_type:
- apiref
api_name:
- RAS_USER_0
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c79a6b946ed9d10cd2bfc989f8cde27fad2ffa92
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508535"
---
# <a name="ras_user_0-structure"></a><span data-ttu-id="610e3-105">RAS \_ 使用者 \_ 0 結構</span><span class="sxs-lookup"><span data-stu-id="610e3-105">RAS\_USER\_0 structure</span></span>

<span data-ttu-id="610e3-106">\[Windows Vista 不支援這個版本的 **RAS \_ 使用者 \_ 0** 結構。</span><span class="sxs-lookup"><span data-stu-id="610e3-106">\[This version of the **RAS\_USER\_0** structure is not supported as of Windows Vista.</span></span> <span data-ttu-id="610e3-107">請改用 mprapi 中定義的較新 [**RAS \_ 使用者 \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_user_0) 。\]</span><span class="sxs-lookup"><span data-stu-id="610e3-107">Use the newer [**RAS\_USER\_0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_user_0) defined in mprapi.h instead.\]</span></span>

<span data-ttu-id="610e3-108">[**RasAdminUserSetInfo**](rasadminusersetinfo.md)和 [**RasAdminUserGetInfo**](rasadminusergetinfo.md)函數中會使用 **RAS \_ 使用者 \_ 0** 結構來指定使用者的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="610e3-108">The **RAS\_USER\_0** structure is used in the [**RasAdminUserSetInfo**](rasadminusersetinfo.md) and [**RasAdminUserGetInfo**](rasadminusergetinfo.md) functions to specify information about a user.</span></span>

## <a name="syntax"></a><span data-ttu-id="610e3-109">語法</span><span class="sxs-lookup"><span data-stu-id="610e3-109">Syntax</span></span>


```C++
typedef struct _RAS_USER_0 {
  BYTE  bfPrivilege;
  WCHAR szPhoneNumber[RASSAPI_MAX_PHONENUMBER_SIZE + 1];
} RAS_USER_0, *PRAS_USER_0;
```



## <a name="members"></a><span data-ttu-id="610e3-110">成員</span><span class="sxs-lookup"><span data-stu-id="610e3-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="610e3-111">**bfPrivilege**</span><span class="sxs-lookup"><span data-stu-id="610e3-111">**bfPrivilege**</span></span>
</dt> <dd>

<span data-ttu-id="610e3-112">一組位旗標，指定使用者的 RAS 許可權。</span><span class="sxs-lookup"><span data-stu-id="610e3-112">A set of bit flags that specify the RAS privileges of the user.</span></span> <span data-ttu-id="610e3-113">這個成員可以是 RASPRIV \_ DialinPrivilege 旗標和其中一個回撥旗標的組合。</span><span class="sxs-lookup"><span data-stu-id="610e3-113">This member can be a combination of the RASPRIV\_DialinPrivilege flag and one of the call-back flags.</span></span> <span data-ttu-id="610e3-114">使用 RASPRIV \_ CallbackType mask 來識別提供給使用者的回撥許可權類型。</span><span class="sxs-lookup"><span data-stu-id="610e3-114">Use the RASPRIV\_CallbackType mask to identify the type of call-back privilege provided to the user.</span></span> <span data-ttu-id="610e3-115">已定義下列旗標。</span><span class="sxs-lookup"><span data-stu-id="610e3-115">The following flags are defined.</span></span>



| <span data-ttu-id="610e3-116">值</span><span class="sxs-lookup"><span data-stu-id="610e3-116">Value</span></span>                                                                                                                                                                                                                                         | <span data-ttu-id="610e3-117">意義</span><span class="sxs-lookup"><span data-stu-id="610e3-117">Meaning</span></span>                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="RASPRIV_NoCallback"></span><span id="raspriv_nocallback"></span><span id="RASPRIV_NOCALLBACK"></span><dl> <span data-ttu-id="610e3-118"><dt>**RASPRIV \_ NoCallback**</dt></span><span class="sxs-lookup"><span data-stu-id="610e3-118"><dt>**RASPRIV\_NoCallback**</dt></span></span> </dl>                             | <span data-ttu-id="610e3-119">使用者沒有任何回撥許可權。</span><span class="sxs-lookup"><span data-stu-id="610e3-119">The user has no call-back privilege.</span></span><br/>                                               |
| <span id="RASPRIV_AdminSetCallback"></span><span id="raspriv_adminsetcallback"></span><span id="RASPRIV_ADMINSETCALLBACK"></span><dl> <span data-ttu-id="610e3-120"><dt>**RASPRIV \_ AdminSetCallback**</dt></span><span class="sxs-lookup"><span data-stu-id="610e3-120"><dt>**RASPRIV\_AdminSetCallback**</dt></span></span> </dl>     | <span data-ttu-id="610e3-121">使用者帳戶已設定為讓系統管理員設定回撥號碼。</span><span class="sxs-lookup"><span data-stu-id="610e3-121">The user account is configured to have the administrator set the call-back number.</span></span><br/> |
| <span id="RASPRIV_CallerSetCallback"></span><span id="raspriv_callersetcallback"></span><span id="RASPRIV_CALLERSETCALLBACK"></span><dl> <span data-ttu-id="610e3-122"><dt>**RASPRIV \_ CallerSetCallback**</dt></span><span class="sxs-lookup"><span data-stu-id="610e3-122"><dt>**RASPRIV\_CallerSetCallback**</dt></span></span> </dl> | <span data-ttu-id="610e3-123">遠端使用者可以在撥入時指定撥回電話號碼。</span><span class="sxs-lookup"><span data-stu-id="610e3-123">The remote user can specify a call-back phone number when dialing in.</span></span><br/>              |
| <span id="RASPRIV_DialinPrivilege"></span><span id="raspriv_dialinprivilege"></span><span id="RASPRIV_DIALINPRIVILEGE"></span><dl> <span data-ttu-id="610e3-124"><dt>**RASPRIV \_ DialinPrivilege**</dt></span><span class="sxs-lookup"><span data-stu-id="610e3-124"><dt>**RASPRIV\_DialinPrivilege**</dt></span></span> </dl>         | <span data-ttu-id="610e3-125">使用者有權撥入這部伺服器。</span><span class="sxs-lookup"><span data-stu-id="610e3-125">The user has permission to dial in to this server.</span></span><br/>                                 |



 

<span data-ttu-id="610e3-126">在 [**RasAdminUserSetInfo**](rasadminusersetinfo.md) 函式的呼叫中指定其中一個回呼旗標。</span><span class="sxs-lookup"><span data-stu-id="610e3-126">Specify one of the call-back flags in the call to the [**RasAdminUserSetInfo**](rasadminusersetinfo.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="610e3-127">**szPhoneNumber**</span><span class="sxs-lookup"><span data-stu-id="610e3-127">**szPhoneNumber**</span></span>
</dt> <dd>

<span data-ttu-id="610e3-128">以 null 結束的 Unicode 字串，指定使用者的回撥電話號碼。</span><span class="sxs-lookup"><span data-stu-id="610e3-128">A null-terminated Unicode string that specifies the call-back phone number for the user.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="610e3-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="610e3-129">Requirements</span></span>



| <span data-ttu-id="610e3-130">需求</span><span class="sxs-lookup"><span data-stu-id="610e3-130">Requirement</span></span> | <span data-ttu-id="610e3-131">值</span><span class="sxs-lookup"><span data-stu-id="610e3-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="610e3-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="610e3-132">Minimum supported client</span></span><br/> | <span data-ttu-id="610e3-133">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="610e3-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="610e3-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="610e3-134">Minimum supported server</span></span><br/> | <span data-ttu-id="610e3-135">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="610e3-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="610e3-136">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="610e3-136">End of client support</span></span><br/>    | <span data-ttu-id="610e3-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="610e3-137">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="610e3-138">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="610e3-138">End of server support</span></span><br/>    | <span data-ttu-id="610e3-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="610e3-139">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="610e3-140">標頭</span><span class="sxs-lookup"><span data-stu-id="610e3-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="610e3-141"><dt>Rassapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="610e3-141"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="610e3-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="610e3-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="610e3-143">遠端存取服務 (RAS) 總覽</span><span class="sxs-lookup"><span data-stu-id="610e3-143">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="610e3-144">RAS 伺服器管理結構</span><span class="sxs-lookup"><span data-stu-id="610e3-144">RAS Server Administration Structures</span></span>](ras-server-administration-structures.md)
</dt> <dt>

[<span data-ttu-id="610e3-145">**RasAdminUserGetInfo**</span><span class="sxs-lookup"><span data-stu-id="610e3-145">**RasAdminUserGetInfo**</span></span>](rasadminusergetinfo.md)
</dt> <dt>

[<span data-ttu-id="610e3-146">**RasAdminUserSetInfo**</span><span class="sxs-lookup"><span data-stu-id="610e3-146">**RasAdminUserSetInfo**</span></span>](rasadminusersetinfo.md)
</dt> </dl>

 

 





