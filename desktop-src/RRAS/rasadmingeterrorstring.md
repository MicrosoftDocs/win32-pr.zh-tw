---
title: 'RasAdminGetErrorString 函式 (Rassapi) '
description: RasAdminGetErrorString 函式會抓取訊息字串，該字串會對應至其中一個 RAS 伺服器管理 (RasAdmin) 函式所傳回的 RAS 錯誤碼。
ms.assetid: b51bc1f9-fed7-43b6-9a07-f19ea4c0cd01
keywords:
- RasAdminGetErrorString 函式 RAS
topic_type:
- apiref
api_name:
- RasAdminGetErrorString
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dc239c5f26061b5234631079ba21ce0d24ad570
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001568"
---
# <a name="rasadmingeterrorstring-function"></a><span data-ttu-id="7f58f-104">RasAdminGetErrorString 函式</span><span class="sxs-lookup"><span data-stu-id="7f58f-104">RasAdminGetErrorString function</span></span>

<span data-ttu-id="7f58f-105">\[這項功能僅提供給 Windows NT Server 4.0 的回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="7f58f-105">\[This function is provided only for backward compatibility with Windows NT Server 4.0.</span></span> <span data-ttu-id="7f58f-106">它會傳回 \_ \_ 未 \_ 在 Windows Server 2003 上執行的錯誤呼叫。</span><span class="sxs-lookup"><span data-stu-id="7f58f-106">It returns ERROR\_CALL\_NOT\_IMPLEMENTED on Windows Server 2003.</span></span> <span data-ttu-id="7f58f-107">應用程式應該使用 [**MprAdminGetErrorString**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingeterrorstring) 函式。\]</span><span class="sxs-lookup"><span data-stu-id="7f58f-107">Applications should use the [**MprAdminGetErrorString**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingeterrorstring) function.\]</span></span>

<span data-ttu-id="7f58f-108">**RasAdminGetErrorString** 函式會抓取訊息字串，該字串會對應至其中一個 ras 伺服器管理 (RasAdmin) 函式所傳回的 ras 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="7f58f-108">The **RasAdminGetErrorString** function retrieves a message string that corresponds to a RAS error code returned by one of the RAS server administration (RasAdmin) functions.</span></span> <span data-ttu-id="7f58f-109">系統會從安裝為 RAS 一部分的 Rasmsg.dll 取出這些訊息字串。</span><span class="sxs-lookup"><span data-stu-id="7f58f-109">These message strings are retrieved from the Rasmsg.dll that is installed as part of RAS.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f58f-110">語法</span><span class="sxs-lookup"><span data-stu-id="7f58f-110">Syntax</span></span>


```C++
DWORD RasAdminGetErrorString(
  _In_  UINT  ResourceId,
  _Out_ WCHAR *lpszString,
  _In_  DWORD InBufSize
);
```



## <a name="parameters"></a><span data-ttu-id="7f58f-111">參數</span><span class="sxs-lookup"><span data-stu-id="7f58f-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f58f-112">*ResourceId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7f58f-112">*ResourceId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f58f-113">指定其中一個 RasAdmin 函數所傳回的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="7f58f-113">Specifies an error code returned by one of the RasAdmin functions.</span></span> <span data-ttu-id="7f58f-114">此值必須在從 RASBASE 到 RASBASEEND 的錯誤碼範圍內。</span><span class="sxs-lookup"><span data-stu-id="7f58f-114">This value must be in the range of error codes from RASBASE to RASBASEEND.</span></span> <span data-ttu-id="7f58f-115">這些是在 Raserror 中定義。</span><span class="sxs-lookup"><span data-stu-id="7f58f-115">These are defined in Raserror.h.</span></span>

</dd> <dt>

<span data-ttu-id="7f58f-116">*lpszString* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="7f58f-116">*lpszString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7f58f-117">接收對應到指定錯誤碼之錯誤訊息的緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="7f58f-117">Pointer to a buffer that receives the error message that corresponds to the specified error code.</span></span>

</dd> <dt>

<span data-ttu-id="7f58f-118">*InBufSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7f58f-118">*InBufSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f58f-119">指定 *lpszString* 緩衝區的大小（以字元為單位）。</span><span class="sxs-lookup"><span data-stu-id="7f58f-119">Specifies the size, in characters, of the *lpszString* buffer.</span></span> <span data-ttu-id="7f58f-120">錯誤訊息通常是80個字元或更少：緩衝區大小為512個字元，一律為足夠的值。</span><span class="sxs-lookup"><span data-stu-id="7f58f-120">Error messages are typically 80 characters or less; a buffer size of 512 characters is always adequate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f58f-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="7f58f-121">Return value</span></span>

<span data-ttu-id="7f58f-122">如果函式成功，則傳回值為「錯誤 \_ 成功」。</span><span class="sxs-lookup"><span data-stu-id="7f58f-122">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="7f58f-123">如果函式失敗，則傳回值是錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="7f58f-123">If the function fails, the return value is an error code.</span></span> <span data-ttu-id="7f58f-124">這個值可以是 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)、 [**GlobalAlloc**](/windows/win32/api/winbase/nf-winbase-globalalloc)或 [**loadstring 時**](/windows/win32/api/winuser/nf-winuser-loadstringa) 函數所設定的最後一個錯誤值;或者，它可以是下列其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="7f58f-124">This value can be a last error value set by the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya), [**GlobalAlloc**](/windows/win32/api/winbase/nf-winbase-globalalloc), or [**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa) functions; or it can be one of the following error codes.</span></span>



| <span data-ttu-id="7f58f-125">值</span><span class="sxs-lookup"><span data-stu-id="7f58f-125">Value</span></span>                                                                                                      | <span data-ttu-id="7f58f-126">意義</span><span class="sxs-lookup"><span data-stu-id="7f58f-126">Meaning</span></span>                                                                  |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7f58f-127"><dt>**錯誤 \_ 不正確 \_ 參數**</dt></span><span class="sxs-lookup"><span data-stu-id="7f58f-127"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>   | <span data-ttu-id="7f58f-128">*ResourceId* 或 *lpszString* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="7f58f-128">The *ResourceId* or *lpszString* parameters are invalid.</span></span><br/>      |
| <dl> <span data-ttu-id="7f58f-129"><dt>**\_緩衝區不足的錯誤 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7f58f-129"><dt>**ERROR\_INSUFFICIENT\_BUFFER**</dt></span></span> </dl> | <span data-ttu-id="7f58f-130">*InBufSize* 參數所指定的大小太小。</span><span class="sxs-lookup"><span data-stu-id="7f58f-130">The size specified by the *InBufSize* parameter is too small.</span></span><br/> |



 

<span data-ttu-id="7f58f-131">此函數沒有任何延伸的錯誤資訊;請勿呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)。</span><span class="sxs-lookup"><span data-stu-id="7f58f-131">There is no extended error information for this function; do not call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="7f58f-132">備註</span><span class="sxs-lookup"><span data-stu-id="7f58f-132">Remarks</span></span>

<span data-ttu-id="7f58f-133">RasAdmin 函數可以傳回不在 **RasAdminGetErrorString** 函數所支援範圍內的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="7f58f-133">The RasAdmin functions can return error codes that are not in the range supported by the **RasAdminGetErrorString** function.</span></span> <span data-ttu-id="7f58f-134">例如，RasAdmin 函式可能會傳回 Lmerr 中定義的錯誤碼，以及 Winerror.h. h。</span><span class="sxs-lookup"><span data-stu-id="7f58f-134">For example, the RasAdmin functions can return error codes that are defined in Lmerr.h and Winerror.h.</span></span> <span data-ttu-id="7f58f-135">在呼叫 **RasAdminGetErrorString** 之前，請確認錯誤碼位於 RASBASE 到 RASBASEEND 的範圍中，如 Raserror 中所定義。</span><span class="sxs-lookup"><span data-stu-id="7f58f-135">Before calling **RasAdminGetErrorString**, verify that the error code is in the range RASBASE to RASBASEEND, as defined in Raserror.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f58f-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="7f58f-136">Requirements</span></span>



| <span data-ttu-id="7f58f-137">需求</span><span class="sxs-lookup"><span data-stu-id="7f58f-137">Requirement</span></span> | <span data-ttu-id="7f58f-138">值</span><span class="sxs-lookup"><span data-stu-id="7f58f-138">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7f58f-139">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="7f58f-139">End of client support</span></span><br/> | <span data-ttu-id="7f58f-140">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="7f58f-140">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="7f58f-141">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="7f58f-141">End of server support</span></span><br/> | <span data-ttu-id="7f58f-142">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7f58f-142">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="7f58f-143">標頭</span><span class="sxs-lookup"><span data-stu-id="7f58f-143">Header</span></span><br/>                | <dl> <span data-ttu-id="7f58f-144"><dt>Rassapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="7f58f-144"><dt>Rassapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="7f58f-145">程式庫</span><span class="sxs-lookup"><span data-stu-id="7f58f-145">Library</span></span><br/>               | <dl> <span data-ttu-id="7f58f-146"><dt>Rassapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="7f58f-146"><dt>Rassapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="7f58f-147">DLL</span><span class="sxs-lookup"><span data-stu-id="7f58f-147">DLL</span></span><br/>                   | <dl> <span data-ttu-id="7f58f-148"><dt>Rassapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f58f-148"><dt>Rassapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f58f-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7f58f-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f58f-150">遠端存取服務 (RAS) 總覽</span><span class="sxs-lookup"><span data-stu-id="7f58f-150">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="7f58f-151">RAS 伺服器管理功能</span><span class="sxs-lookup"><span data-stu-id="7f58f-151">RAS Server Administration Functions</span></span>](ras-server-administration-functions.md)
</dt> <dt>

[<span data-ttu-id="7f58f-152">**LoadLibrary**</span><span class="sxs-lookup"><span data-stu-id="7f58f-152">**LoadLibrary**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> <dt>

[<span data-ttu-id="7f58f-153">**GlobalAlloc**</span><span class="sxs-lookup"><span data-stu-id="7f58f-153">**GlobalAlloc**</span></span>](/windows/win32/api/winbase/nf-winbase-globalalloc)
</dt> <dt>

[<span data-ttu-id="7f58f-154">**Loadstring 時**</span><span class="sxs-lookup"><span data-stu-id="7f58f-154">**LoadString**</span></span>](/windows/win32/api/winuser/nf-winuser-loadstringa)
</dt> </dl>

 

