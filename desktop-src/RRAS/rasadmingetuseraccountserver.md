---
title: 'RasAdminGetUserAccountServer 函式 (Rassapi) '
description: RasAdminGetUserAccountServer 函式會抓取具有使用者帳戶資料庫的伺服器名稱。 在 RasAdminUserGetInfo 和 RasAdminUserSetInfo 函數中使用傳回的伺服器名稱，以取得或設定指定使用者的相關資訊。
ms.assetid: db91aa48-32af-49ac-87ed-8c484926ca15
keywords:
- RasAdminGetUserAccountServer 函式 RAS
topic_type:
- apiref
api_name:
- RasAdminGetUserAccountServer
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c506287d94c5ec64445c74d8364a04db98100751
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998811"
---
# <a name="rasadmingetuseraccountserver-function"></a><span data-ttu-id="434ab-105">RasAdminGetUserAccountServer 函式</span><span class="sxs-lookup"><span data-stu-id="434ab-105">RasAdminGetUserAccountServer function</span></span>

<span data-ttu-id="434ab-106">\[這項功能僅提供給 Windows NT Server 4.0 的回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="434ab-106">\[This function is provided only for backward compatibility with Windows NT Server 4.0.</span></span> <span data-ttu-id="434ab-107">它會傳回 \_ \_ 未 \_ 在 Windows Server 2003 上執行的錯誤呼叫。</span><span class="sxs-lookup"><span data-stu-id="434ab-107">It returns ERROR\_CALL\_NOT\_IMPLEMENTED on Windows Server 2003.</span></span> <span data-ttu-id="434ab-108">應用程式應該使用 [**MprAdminGetPDCServer**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetpdcserver) 函式。\]</span><span class="sxs-lookup"><span data-stu-id="434ab-108">Applications should use the [**MprAdminGetPDCServer**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetpdcserver) function.\]</span></span>

<span data-ttu-id="434ab-109">**RasAdminGetUserAccountServer** 函式會抓取具有使用者帳戶資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="434ab-109">The **RasAdminGetUserAccountServer** function retrieves the name of the server that has the user account database.</span></span> <span data-ttu-id="434ab-110">在 [**RasAdminUserGetInfo**](rasadminusergetinfo.md) 和 [**RasAdminUserSetInfo**](rasadminusersetinfo.md) 函數中使用傳回的伺服器名稱，以取得或設定指定使用者的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="434ab-110">Use the returned server name in the [**RasAdminUserGetInfo**](rasadminusergetinfo.md) and [**RasAdminUserSetInfo**](rasadminusersetinfo.md) functions to get or set information about a specified user.</span></span>

## <a name="syntax"></a><span data-ttu-id="434ab-111">語法</span><span class="sxs-lookup"><span data-stu-id="434ab-111">Syntax</span></span>


```C++
DWORD RasAdminGetUserAccountServer(
  _In_  const WCHAR  *lpszDomain,
  _In_  const WCHAR  *lpszServer,
  _Out_       LPWSTR lpszUserAccountServer
);
```



## <a name="parameters"></a><span data-ttu-id="434ab-112">參數</span><span class="sxs-lookup"><span data-stu-id="434ab-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="434ab-113">*lpszDomain* \[在\]</span><span class="sxs-lookup"><span data-stu-id="434ab-113">*lpszDomain* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="434ab-114">以 **null** 結束的 Unicode 字串指標，指定 RAS 伺服器所屬之網域的名稱。</span><span class="sxs-lookup"><span data-stu-id="434ab-114">Pointer to a **null**-terminated Unicode string that specifies the name of the domain to which the RAS server belongs.</span></span> <span data-ttu-id="434ab-115">對於在非網域成員的工作站或伺服器上執行的 RAS 管理應用程式而言，這個參數是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="434ab-115">This parameter is **NULL** for the RAS administration applications running on workstations or servers that are not members of a domain.</span></span> <span data-ttu-id="434ab-116">如果此參數為 **null**，則 *lpszServer* 參數必須為非 **null**。</span><span class="sxs-lookup"><span data-stu-id="434ab-116">If this parameter is **NULL**, the *lpszServer* parameter must be non-**NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="434ab-117">*lpszServer* \[在\]</span><span class="sxs-lookup"><span data-stu-id="434ab-117">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="434ab-118">以 **null** 結束的 Unicode 字串指標，指定 RAS 伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="434ab-118">Pointer to a **null**-terminated Unicode string that specifies the name of the RAS server.</span></span> <span data-ttu-id="434ab-119">\\ \\ 請以下列格式指定開頭為 "" 字元的名稱： \\ \\ *servername*。</span><span class="sxs-lookup"><span data-stu-id="434ab-119">Specify the name with leading "\\\\" characters, in the form: \\\\*servername*.</span></span> <span data-ttu-id="434ab-120">如果 *lpszDomain* 參數不是 **null**，這個參數可以是 **null** 。</span><span class="sxs-lookup"><span data-stu-id="434ab-120">This parameter can be **NULL** if the *lpszDomain* parameter is not **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="434ab-121">*lpszUserAccountServer* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="434ab-121">*lpszUserAccountServer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="434ab-122">緩衝區的指標，此緩衝區會接收以 **null** 終止的 Unicode 字串，這個字串會指定擁有使用者帳戶資料庫之網域控制站的名稱。</span><span class="sxs-lookup"><span data-stu-id="434ab-122">Pointer to a buffer that receives a **null**-terminated Unicode string that specifies the name of a domain controller that has the user account database.</span></span> <span data-ttu-id="434ab-123">緩衝區必須夠大，才能保存伺服器名稱 (UNCLEN + 1) 。</span><span class="sxs-lookup"><span data-stu-id="434ab-123">The buffer should be big enough to hold the server name (UNCLEN +1).</span></span> <span data-ttu-id="434ab-124">函數會在傳回的伺服器名稱前面加 \\ \\ 上 "" 字元，格式為： \\ \\ *servername*。</span><span class="sxs-lookup"><span data-stu-id="434ab-124">The function prefixes the returned server name with leading "\\\\" characters, in the form: \\\\*servername*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="434ab-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="434ab-125">Return value</span></span>

<span data-ttu-id="434ab-126">如果函式成功，則傳回值為「錯誤 \_ 成功」。</span><span class="sxs-lookup"><span data-stu-id="434ab-126">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="434ab-127">如果函式失敗，則傳回值可能是下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="434ab-127">If the function fails, the return value can be the following error code.</span></span>



| <span data-ttu-id="434ab-128">值</span><span class="sxs-lookup"><span data-stu-id="434ab-128">Value</span></span>                                                                                                    | <span data-ttu-id="434ab-129">意義</span><span class="sxs-lookup"><span data-stu-id="434ab-129">Meaning</span></span>                                                     |
|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="434ab-130"><dt>**錯誤 \_ 不正確 \_ 參數**</dt></span><span class="sxs-lookup"><span data-stu-id="434ab-130"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl> | <span data-ttu-id="434ab-131">*LpszDomain* 和 *LpszServer* 都是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="434ab-131">Both *lpszDomain* and *lpszServer* are **NULL**.</span></span><br/> |



 

<span data-ttu-id="434ab-132">此函數沒有任何延伸的錯誤資訊;請勿呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)。</span><span class="sxs-lookup"><span data-stu-id="434ab-132">There is no extended error information for this function; do not call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="434ab-133">備註</span><span class="sxs-lookup"><span data-stu-id="434ab-133">Remarks</span></span>

<span data-ttu-id="434ab-134">**RasAdminGetUserAccountServer** 函數會取得具有使用者帳戶資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="434ab-134">The **RasAdminGetUserAccountServer** function obtains the name of the server with the user accounts database.</span></span> <span data-ttu-id="434ab-135">此函數需要 RAS 伺服器的名稱，或 RAS 伺服器所在網域的名稱。</span><span class="sxs-lookup"><span data-stu-id="434ab-135">This function requires the name of the RAS server or the name of the domain in which the RAS server resides.</span></span>

<span data-ttu-id="434ab-136">*LpszDomain* 參數應指定有效的功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="434ab-136">The *lpszDomain* parameter should specify a valid domain name.</span></span> <span data-ttu-id="434ab-137">對於在非網域成員的伺服器上執行的 RAS 系統管理應用程式而言，這個參數是 **Null** (例如，伺服器位於自己的工作組) 中。</span><span class="sxs-lookup"><span data-stu-id="434ab-137">This parameter is **NULL** for RAS administration applications running on servers that are not members of a domain (for example, the server is in its own workgroup).</span></span> <span data-ttu-id="434ab-138">在此情況下， *lpszServer* 參數必須指定伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="434ab-138">In this case, the *lpszServer* parameter must specify the server name.</span></span> <span data-ttu-id="434ab-139">若要取得伺服器名稱，請呼叫 [**GetComputerName**](/windows/win32/api/winbase/nf-winbase-getcomputernamea) 函數。</span><span class="sxs-lookup"><span data-stu-id="434ab-139">To get the server name, call the [**GetComputerName**](/windows/win32/api/winbase/nf-winbase-getcomputernamea) function.</span></span> <span data-ttu-id="434ab-140">請務必在伺服器名稱前面加上 " \\ \\ " 字元。</span><span class="sxs-lookup"><span data-stu-id="434ab-140">Be sure to prefix the server name with the "\\\\" characters.</span></span>

<span data-ttu-id="434ab-141">如果 *lpszServer* 所指定的伺服器名稱是獨立伺服器 (也就是伺服器或工作站不是網域) 的成員，則伺服器名稱本身會在 *lpszUserAccountServer* 緩衝區中傳回。</span><span class="sxs-lookup"><span data-stu-id="434ab-141">If the server name specified by *lpszServer* is a stand-alone server (that is, the server or workstation is not a member of a domain), then the server name itself is returned in the *lpszUserAccountServer* buffer.</span></span>

<span data-ttu-id="434ab-142">然後，在 [**NetQueryDisplayInformation**](/windows/win32/api/lmaccess/nf-lmaccess-netquerydisplayinformation) 函式的呼叫中使用使用者帳戶伺服器的名稱，以列舉使用者帳戶資料庫中的使用者。</span><span class="sxs-lookup"><span data-stu-id="434ab-142">Then use the name of the user account server in a call to the [**NetQueryDisplayInformation**](/windows/win32/api/lmaccess/nf-lmaccess-netquerydisplayinformation) function to enumerate the users in the user account database.</span></span>

## <a name="requirements"></a><span data-ttu-id="434ab-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="434ab-143">Requirements</span></span>



| <span data-ttu-id="434ab-144">需求</span><span class="sxs-lookup"><span data-stu-id="434ab-144">Requirement</span></span> | <span data-ttu-id="434ab-145">值</span><span class="sxs-lookup"><span data-stu-id="434ab-145">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="434ab-146">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="434ab-146">End of client support</span></span><br/> | <span data-ttu-id="434ab-147">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="434ab-147">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="434ab-148">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="434ab-148">End of server support</span></span><br/> | <span data-ttu-id="434ab-149">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="434ab-149">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="434ab-150">標頭</span><span class="sxs-lookup"><span data-stu-id="434ab-150">Header</span></span><br/>                | <dl> <span data-ttu-id="434ab-151"><dt>Rassapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="434ab-151"><dt>Rassapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="434ab-152">程式庫</span><span class="sxs-lookup"><span data-stu-id="434ab-152">Library</span></span><br/>               | <dl> <span data-ttu-id="434ab-153"><dt>Rassapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="434ab-153"><dt>Rassapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="434ab-154">DLL</span><span class="sxs-lookup"><span data-stu-id="434ab-154">DLL</span></span><br/>                   | <dl> <span data-ttu-id="434ab-155"><dt>Rassapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="434ab-155"><dt>Rassapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="434ab-156">另請參閱</span><span class="sxs-lookup"><span data-stu-id="434ab-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="434ab-157">遠端存取服務 (RAS) 總覽</span><span class="sxs-lookup"><span data-stu-id="434ab-157">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="434ab-158">RAS 伺服器管理功能</span><span class="sxs-lookup"><span data-stu-id="434ab-158">RAS Server Administration Functions</span></span>](ras-server-administration-functions.md)
</dt> <dt>

[<span data-ttu-id="434ab-159">**GetComputerName**</span><span class="sxs-lookup"><span data-stu-id="434ab-159">**GetComputerName**</span></span>](/windows/win32/api/winbase/nf-winbase-getcomputernamea)
</dt> <dt>

[<span data-ttu-id="434ab-160">**RasAdminUserGetInfo**</span><span class="sxs-lookup"><span data-stu-id="434ab-160">**RasAdminUserGetInfo**</span></span>](rasadminusergetinfo.md)
</dt> <dt>

[<span data-ttu-id="434ab-161">**RasAdminUserSetInfo**</span><span class="sxs-lookup"><span data-stu-id="434ab-161">**RasAdminUserSetInfo**</span></span>](rasadminusersetinfo.md)
</dt> </dl>

 

