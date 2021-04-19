---
title: 'RasAdminUserSetInfo 函式 (Rassapi) '
description: RasAdminUserSetInfo 函式會設定指定使用者的 RAS 許可權和回撥電話號碼。
ms.assetid: 5b049dfd-ecc8-47e4-82cc-71a875752714
keywords:
- RasAdminUserSetInfo 函式 RAS
topic_type:
- apiref
api_name:
- RasAdminUserSetInfo
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16d35f62713a3f4669db191891d2fb6b1694cabe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001571"
---
# <a name="rasadminusersetinfo-function"></a><span data-ttu-id="dff7c-104">RasAdminUserSetInfo 函式</span><span class="sxs-lookup"><span data-stu-id="dff7c-104">RasAdminUserSetInfo function</span></span>

<span data-ttu-id="dff7c-105">\[這項功能僅提供給 Windows NT Server 4.0 的回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="dff7c-105">\[This function is provided only for backward compatibility with Windows NT Server 4.0.</span></span> <span data-ttu-id="dff7c-106">它會傳回 \_ \_ 未 \_ 在 Windows Server 2003 上執行的錯誤呼叫。</span><span class="sxs-lookup"><span data-stu-id="dff7c-106">It returns ERROR\_CALL\_NOT\_IMPLEMENTED on Windows Server 2003.</span></span> <span data-ttu-id="dff7c-107">應用程式應該使用 [**MprAdminUserSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusersetinfo) 函式。\]</span><span class="sxs-lookup"><span data-stu-id="dff7c-107">Applications should use the [**MprAdminUserSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusersetinfo) function.\]</span></span>

<span data-ttu-id="dff7c-108">**RasAdminUserSetInfo** 函式會設定指定使用者的 RAS 許可權和回撥電話號碼。</span><span class="sxs-lookup"><span data-stu-id="dff7c-108">The **RasAdminUserSetInfo** function sets the RAS permissions and call-back phone number for a specified user.</span></span>

## <a name="syntax"></a><span data-ttu-id="dff7c-109">語法</span><span class="sxs-lookup"><span data-stu-id="dff7c-109">Syntax</span></span>


```C++
DWORD RasAdminUserSetInfo(
  _In_ const WCHAR       *lpszUserAccountServer,
  _In_ const WCHAR       *lpszUser,
  _In_ const PRAS_USER_0 pRasUser0
);
```



## <a name="parameters"></a><span data-ttu-id="dff7c-110">參數</span><span class="sxs-lookup"><span data-stu-id="dff7c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dff7c-111">*lpszUserAccountServer* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dff7c-111">*lpszUserAccountServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dff7c-112">以 null 結束的 Unicode 字串指標，指定具有使用者帳戶資料庫之主要或備份網域控制站的名稱。</span><span class="sxs-lookup"><span data-stu-id="dff7c-112">Pointer to a null-terminated Unicode string that specifies the name of the primary or backup domain controller that has the user account database.</span></span> <span data-ttu-id="dff7c-113">使用 [**RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md) 函數來取得此伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="dff7c-113">Use the [**RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md) function to get this server name.</span></span>

</dd> <dt>

<span data-ttu-id="dff7c-114">*lpszUser* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dff7c-114">*lpszUser* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dff7c-115">以 null 結束的 Unicode 字串指標，指定要設定 RAS 資訊之使用者的名稱。</span><span class="sxs-lookup"><span data-stu-id="dff7c-115">Pointer to a null-terminated Unicode string that specifies the name of the user for whom RAS information is to be set.</span></span>

</dd> <dt>

<span data-ttu-id="dff7c-116">*pRasUser0* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dff7c-116">*pRasUser0* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dff7c-117">[**RAS \_ 使用者 \_ 0**](ras-user-0-str.md)結構的指標，指定指定使用者的新 RAS 資料。</span><span class="sxs-lookup"><span data-stu-id="dff7c-117">Pointer to the [**RAS\_USER\_0**](ras-user-0-str.md) structure that specifies the new RAS data for the specified user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dff7c-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="dff7c-118">Return value</span></span>

<span data-ttu-id="dff7c-119">如果函式成功，則傳回值為「錯誤 \_ 成功」。</span><span class="sxs-lookup"><span data-stu-id="dff7c-119">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="dff7c-120">如果函式失敗，則傳回值可以是下列其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="dff7c-120">If the function fails, the return value can be one of the following error codes.</span></span>



| <span data-ttu-id="dff7c-121">值</span><span class="sxs-lookup"><span data-stu-id="dff7c-121">Value</span></span>                                                                                                           | <span data-ttu-id="dff7c-122">描述</span><span class="sxs-lookup"><span data-stu-id="dff7c-122">Description</span></span>                                                                                     |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="dff7c-123"><dt>**錯誤 \_ 不正確 \_ 資料**</dt></span><span class="sxs-lookup"><span data-stu-id="dff7c-123"><dt>**ERROR\_INVALID\_DATA**</dt></span></span> </dl>             | <span data-ttu-id="dff7c-124">*PRasUser0* 緩衝區包含不正確資料。</span><span class="sxs-lookup"><span data-stu-id="dff7c-124">The *pRasUser0* buffer contains invalid data.</span></span><br/>                                        |
| <dl> <span data-ttu-id="dff7c-125"><dt>**錯誤 \_ 不正確 \_ 回呼 \_ 號碼**</dt></span><span class="sxs-lookup"><span data-stu-id="dff7c-125"><dt>**ERROR\_INVALID\_CALLBACK\_NUMBER**</dt></span></span> </dl> | <span data-ttu-id="dff7c-126">*PRasUser0* 緩衝區中指定的回呼號碼包含不正確字元。</span><span class="sxs-lookup"><span data-stu-id="dff7c-126">The callback number specified in the *pRasUser0* buffer contains invalid characters.</span></span><br/> |
| <dl> <span data-ttu-id="dff7c-127"><dt>**NERR \_BufTooSmall**</dt></span><span class="sxs-lookup"><span data-stu-id="dff7c-127"><dt>**NERR\_BufTooSmall** </dt></span></span> </dl>               | <span data-ttu-id="dff7c-128">記憶體不足，無法執行此功能。</span><span class="sxs-lookup"><span data-stu-id="dff7c-128">Insufficient memory to perform this function.</span></span><br/>                                        |



 

<span data-ttu-id="dff7c-129">此函數沒有任何延伸的錯誤資訊;請勿呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)。</span><span class="sxs-lookup"><span data-stu-id="dff7c-129">There is no extended error information for this function; do not call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="dff7c-130">備註</span><span class="sxs-lookup"><span data-stu-id="dff7c-130">Remarks</span></span>

<span data-ttu-id="dff7c-131">設定使用者的 RAS 許可權時， [**RAS \_ 使用者 \_ 0**](ras-user-0-str.md)結構的 **bfPrivilege** 成員必須指定至少一個回撥旗標。</span><span class="sxs-lookup"><span data-stu-id="dff7c-131">When setting the RAS permissions for a user, the **bfPrivilege** member of the [**RAS\_USER\_0**](ras-user-0-str.md) structure must specify at least one of the call-back flags.</span></span> <span data-ttu-id="dff7c-132">例如，若要將使用者的許可權設定為允許撥入許可權，但沒有回呼許可權，請將 **bfPrivilege** 設定為 RASPRIV \_ DialinPrivilege \| RASPRIV \_ NoCallback。</span><span class="sxs-lookup"><span data-stu-id="dff7c-132">For example, to set a user's privileges to allow dial-in privilege but no call-back privilege, set **bfPrivilege** to RASPRIV\_DialinPrivilege \| RASPRIV\_NoCallback.</span></span>

## <a name="requirements"></a><span data-ttu-id="dff7c-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="dff7c-133">Requirements</span></span>



| <span data-ttu-id="dff7c-134">需求</span><span class="sxs-lookup"><span data-stu-id="dff7c-134">Requirement</span></span> | <span data-ttu-id="dff7c-135">值</span><span class="sxs-lookup"><span data-stu-id="dff7c-135">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dff7c-136">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="dff7c-136">End of client support</span></span><br/> | <span data-ttu-id="dff7c-137">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="dff7c-137">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="dff7c-138">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="dff7c-138">End of server support</span></span><br/> | <span data-ttu-id="dff7c-139">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="dff7c-139">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="dff7c-140">標頭</span><span class="sxs-lookup"><span data-stu-id="dff7c-140">Header</span></span><br/>                | <dl> <span data-ttu-id="dff7c-141"><dt>Rassapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="dff7c-141"><dt>Rassapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="dff7c-142">程式庫</span><span class="sxs-lookup"><span data-stu-id="dff7c-142">Library</span></span><br/>               | <dl> <span data-ttu-id="dff7c-143"><dt>Rassapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="dff7c-143"><dt>Rassapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="dff7c-144">DLL</span><span class="sxs-lookup"><span data-stu-id="dff7c-144">DLL</span></span><br/>                   | <dl> <span data-ttu-id="dff7c-145"><dt>Rassapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dff7c-145"><dt>Rassapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dff7c-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dff7c-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dff7c-147">遠端存取服務 (RAS) 總覽</span><span class="sxs-lookup"><span data-stu-id="dff7c-147">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="dff7c-148">RAS 伺服器管理功能</span><span class="sxs-lookup"><span data-stu-id="dff7c-148">RAS Server Administration Functions</span></span>](ras-server-administration-functions.md)
</dt> <dt>

[<span data-ttu-id="dff7c-149">**RAS \_ 使用者 \_ 0**</span><span class="sxs-lookup"><span data-stu-id="dff7c-149">**RAS\_USER\_0**</span></span>](ras-user-0-str.md)
</dt> <dt>

[<span data-ttu-id="dff7c-150">**RasAdminGetUserAccountServer**</span><span class="sxs-lookup"><span data-stu-id="dff7c-150">**RasAdminGetUserAccountServer**</span></span>](rasadmingetuseraccountserver.md)
</dt> <dt>

[<span data-ttu-id="dff7c-151">**RasAdminUserGetInfo**</span><span class="sxs-lookup"><span data-stu-id="dff7c-151">**RasAdminUserGetInfo**</span></span>](rasadminusergetinfo.md)
</dt> </dl>

 

