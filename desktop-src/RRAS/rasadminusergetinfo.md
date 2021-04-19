---
title: 'RasAdminUserGetInfo 函式 (Rassapi) '
description: RasAdminUserGetInfo 函式會取得指定使用者的 RAS 許可權和回呼電話號碼資訊。
ms.assetid: 178ff775-9cd2-43f0-9a9a-dbae337c5fe8
keywords:
- RasAdminUserGetInfo 函式 RAS
topic_type:
- apiref
api_name:
- RasAdminUserGetInfo
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89fe08a918a958ffb5a656ce2c76cecec31cbb61
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994282"
---
# <a name="rasadminusergetinfo-function"></a><span data-ttu-id="86afc-104">RasAdminUserGetInfo 函式</span><span class="sxs-lookup"><span data-stu-id="86afc-104">RasAdminUserGetInfo function</span></span>

<span data-ttu-id="86afc-105">\[這項功能僅提供給 Windows NT Server 4.0 的回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="86afc-105">\[This function is provided only for backward compatibility with Windows NT Server 4.0.</span></span> <span data-ttu-id="86afc-106">它會傳回 \_ \_ 未 \_ 在 Windows Server 2003 上執行的錯誤呼叫。</span><span class="sxs-lookup"><span data-stu-id="86afc-106">It returns ERROR\_CALL\_NOT\_IMPLEMENTED on Windows Server 2003.</span></span> <span data-ttu-id="86afc-107">應用程式應該使用 [**MprAdminUserGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusergetinfo) 函式。\]</span><span class="sxs-lookup"><span data-stu-id="86afc-107">Applications should use the [**MprAdminUserGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusergetinfo) function.\]</span></span>

<span data-ttu-id="86afc-108">**RasAdminUserGetInfo** 函式會取得指定使用者的 RAS 許可權和回呼電話號碼資訊。</span><span class="sxs-lookup"><span data-stu-id="86afc-108">The **RasAdminUserGetInfo** function gets the RAS permissions and callback phone number information for a specified user.</span></span>

## <a name="syntax"></a><span data-ttu-id="86afc-109">語法</span><span class="sxs-lookup"><span data-stu-id="86afc-109">Syntax</span></span>


```C++
DWORD RasAdminUserGetInfo(
  _In_ const WCHAR       *lpszUserAccountServer,
  _In_ const WCHAR       *lpszUser,
             PRAS_USER_0 pRasUser0
);
```



## <a name="parameters"></a><span data-ttu-id="86afc-110">參數</span><span class="sxs-lookup"><span data-stu-id="86afc-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86afc-111">*lpszUserAccountServer* \[在\]</span><span class="sxs-lookup"><span data-stu-id="86afc-111">*lpszUserAccountServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86afc-112">以 null 結束的 Unicode 字串指標，指定具有使用者帳戶資料庫之主要或備份網域控制站的名稱。</span><span class="sxs-lookup"><span data-stu-id="86afc-112">Pointer to a null-terminated Unicode string that specifies the name of the primary or backup domain controller that has the user account database.</span></span> <span data-ttu-id="86afc-113">使用 [**RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md) 函數來取得此伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="86afc-113">Use the [**RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md) function to get this server name.</span></span>

</dd> <dt>

<span data-ttu-id="86afc-114">*lpszUser* \[在\]</span><span class="sxs-lookup"><span data-stu-id="86afc-114">*lpszUser* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86afc-115">以 null 結束的 Unicode 字串指標，指定要取得其 RAS 資訊的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="86afc-115">Pointer to a null-terminated Unicode string that specifies the name of the user for whom to get RAS information.</span></span>

</dd> <dt>

<span data-ttu-id="86afc-116">*pRasUser0*</span><span class="sxs-lookup"><span data-stu-id="86afc-116">*pRasUser0*</span></span> 
</dt> <dd>

<span data-ttu-id="86afc-117">[**Ras \_ 使用者 \_ 0**](ras-user-0-str.md)結構的指標，此結構會接收指定使用者的 ras 資料。</span><span class="sxs-lookup"><span data-stu-id="86afc-117">Pointer to the [**RAS\_USER\_0**](ras-user-0-str.md) structure that receives the RAS data for the specified user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86afc-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="86afc-118">Return value</span></span>

<span data-ttu-id="86afc-119">如果函式成功，則傳回值為「錯誤 \_ 成功」。</span><span class="sxs-lookup"><span data-stu-id="86afc-119">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="86afc-120">如果函式失敗，則傳回值可能是下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="86afc-120">If the function fails, the return value can be the following error code.</span></span>



| <span data-ttu-id="86afc-121">值</span><span class="sxs-lookup"><span data-stu-id="86afc-121">Value</span></span>                                                                                            | <span data-ttu-id="86afc-122">意義</span><span class="sxs-lookup"><span data-stu-id="86afc-122">Meaning</span></span>                                                  |
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="86afc-123"><dt>**NERR \_ BufTooSmall**</dt></span><span class="sxs-lookup"><span data-stu-id="86afc-123"><dt>**NERR\_BufTooSmall**</dt></span></span> </dl> | <span data-ttu-id="86afc-124">記憶體不足，無法執行此功能。</span><span class="sxs-lookup"><span data-stu-id="86afc-124">Insufficient memory to perform this function.</span></span><br/> |



 

<span data-ttu-id="86afc-125">此函數沒有任何延伸的錯誤資訊;請勿呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)。</span><span class="sxs-lookup"><span data-stu-id="86afc-125">There is no extended error information for this function; do not call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="requirements"></a><span data-ttu-id="86afc-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="86afc-126">Requirements</span></span>



| <span data-ttu-id="86afc-127">需求</span><span class="sxs-lookup"><span data-stu-id="86afc-127">Requirement</span></span> | <span data-ttu-id="86afc-128">值</span><span class="sxs-lookup"><span data-stu-id="86afc-128">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="86afc-129">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="86afc-129">End of client support</span></span><br/> | <span data-ttu-id="86afc-130">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="86afc-130">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="86afc-131">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="86afc-131">End of server support</span></span><br/> | <span data-ttu-id="86afc-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="86afc-132">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="86afc-133">標頭</span><span class="sxs-lookup"><span data-stu-id="86afc-133">Header</span></span><br/>                | <dl> <span data-ttu-id="86afc-134"><dt>Rassapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="86afc-134"><dt>Rassapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="86afc-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="86afc-135">Library</span></span><br/>               | <dl> <span data-ttu-id="86afc-136"><dt>Rassapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="86afc-136"><dt>Rassapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="86afc-137">DLL</span><span class="sxs-lookup"><span data-stu-id="86afc-137">DLL</span></span><br/>                   | <dl> <span data-ttu-id="86afc-138"><dt>Rassapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86afc-138"><dt>Rassapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86afc-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="86afc-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86afc-140">遠端存取服務 (RAS) 總覽</span><span class="sxs-lookup"><span data-stu-id="86afc-140">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="86afc-141">RAS 伺服器管理功能</span><span class="sxs-lookup"><span data-stu-id="86afc-141">RAS Server Administration Functions</span></span>](ras-server-administration-functions.md)
</dt> <dt>

[<span data-ttu-id="86afc-142">**RAS \_ 使用者 \_ 0**</span><span class="sxs-lookup"><span data-stu-id="86afc-142">**RAS\_USER\_0**</span></span>](ras-user-0-str.md)
</dt> <dt>

[<span data-ttu-id="86afc-143">**RasAdminGetUserAccountServer**</span><span class="sxs-lookup"><span data-stu-id="86afc-143">**RasAdminGetUserAccountServer**</span></span>](rasadmingetuseraccountserver.md)
</dt> <dt>

[<span data-ttu-id="86afc-144">**RasAdminUserSetInfo**</span><span class="sxs-lookup"><span data-stu-id="86afc-144">**RasAdminUserSetInfo**</span></span>](rasadminusersetinfo.md)
</dt> </dl>

 

