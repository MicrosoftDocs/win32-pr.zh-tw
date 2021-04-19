---
title: 'RasAdminServerGetInfo 函式 (Rassapi) '
description: RasAdminServerGetInfo 函數會取得 RAS 伺服器的伺服器設定。
ms.assetid: a1c371fd-462c-443c-8016-592efb2f0b1a
keywords:
- RasAdminServerGetInfo 函式 RAS
topic_type:
- apiref
api_name:
- RasAdminServerGetInfo
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 115a2421db5efbafb72d73952684ff7758c6995b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993577"
---
# <a name="rasadminservergetinfo-function"></a><span data-ttu-id="f83d7-104">RasAdminServerGetInfo 函式</span><span class="sxs-lookup"><span data-stu-id="f83d7-104">RasAdminServerGetInfo function</span></span>

<span data-ttu-id="f83d7-105">\[這項功能僅提供給 Windows NT Server 4.0 的回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="f83d7-105">\[This function is provided only for backward compatibility with Windows NT Server 4.0.</span></span> <span data-ttu-id="f83d7-106">它會傳回 \_ \_ 未 \_ 在 Windows Server 2003 上執行的錯誤呼叫。</span><span class="sxs-lookup"><span data-stu-id="f83d7-106">It returns ERROR\_CALL\_NOT\_IMPLEMENTED on Windows Server 2003.</span></span> <span data-ttu-id="f83d7-107">應用程式應該使用 [**MprAdminServerGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminservergetinfo) 函式。\]</span><span class="sxs-lookup"><span data-stu-id="f83d7-107">Applications should use the [**MprAdminServerGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminservergetinfo) function.\]</span></span>

<span data-ttu-id="f83d7-108">**RasAdminServerGetInfo** 函數會取得 RAS 伺服器的伺服器設定。</span><span class="sxs-lookup"><span data-stu-id="f83d7-108">The **RasAdminServerGetInfo** function gets the server configuration of a RAS server.</span></span>

## <a name="syntax"></a><span data-ttu-id="f83d7-109">語法</span><span class="sxs-lookup"><span data-stu-id="f83d7-109">Syntax</span></span>


```C++
DWORD RasAdminServerGetInfo(
  _In_  const WCHAR         *lpszServer,
  _Out_       PRAS_SERVER_0 pRasServer0
);
```



## <a name="parameters"></a><span data-ttu-id="f83d7-110">參數</span><span class="sxs-lookup"><span data-stu-id="f83d7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f83d7-111">*lpszServer* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f83d7-111">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f83d7-112">以 **null** 結束的 Unicode 字串指標，指定 Windows NT/WINDOWS 2000 RAS 伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="f83d7-112">Pointer to a **null**-terminated Unicode string that specifies the name of the Windows NT/Windows 2000 RAS server.</span></span> <span data-ttu-id="f83d7-113">如果此參數為 **Null**，則函式會傳回本機電腦的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f83d7-113">If this parameter is **NULL**, the function returns information about the local computer.</span></span> <span data-ttu-id="f83d7-114">\\ \\ 請以下列格式指定開頭為 "" 字元的名稱： \\ \\ *servername*。</span><span class="sxs-lookup"><span data-stu-id="f83d7-114">Specify the name with leading "\\\\" characters, in the form: \\\\*servername*.</span></span>

</dd> <dt>

<span data-ttu-id="f83d7-115">*pRasServer0* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f83d7-115">*pRasServer0* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f83d7-116">[**RAS \_ 伺服器 \_ 0**](ras-server-0-str.md)結構的指標，此結構會接收伺服器上設定的埠數目、目前使用中的埠數目，以及伺服器版本號碼。</span><span class="sxs-lookup"><span data-stu-id="f83d7-116">Pointer to the [**RAS\_SERVER\_0**](ras-server-0-str.md) structure that receives the number of ports configured on the server, the number of ports currently in use, and the server version number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f83d7-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="f83d7-117">Return value</span></span>

<span data-ttu-id="f83d7-118">如果函式成功，則傳回值為「錯誤 \_ 成功」。</span><span class="sxs-lookup"><span data-stu-id="f83d7-118">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="f83d7-119">如果函式失敗，則傳回值是錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f83d7-119">If the function fails, the return value is an error code.</span></span> <span data-ttu-id="f83d7-120">可能的錯誤代碼包括由 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 針對 [**CallNamedPipe**](/windows/desktop/api/winbase/nf-winbase-callnamedpipea) 函式傳回的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f83d7-120">Possible error codes include those returned by [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) for the [**CallNamedPipe**](/windows/desktop/api/winbase/nf-winbase-callnamedpipea) function.</span></span> <span data-ttu-id="f83d7-121">此函數沒有任何延伸的錯誤資訊;請勿呼叫 **GetLastError**。</span><span class="sxs-lookup"><span data-stu-id="f83d7-121">There is no extended error information for this function; do not call **GetLastError**.</span></span>

## <a name="remarks"></a><span data-ttu-id="f83d7-122">備註</span><span class="sxs-lookup"><span data-stu-id="f83d7-122">Remarks</span></span>

<span data-ttu-id="f83d7-123">若要列舉網域中的所有 RAS 伺服器，請呼叫 [**NetServerEnum**](/windows/desktop/api/lmserver/nf-lmserver-netserverenum) 函式， \_ 並 \_ 為 *servertype* 參數指定 SV 類型撥入。</span><span class="sxs-lookup"><span data-stu-id="f83d7-123">To enumerate all RAS servers in a domain, call the [**NetServerEnum**](/windows/desktop/api/lmserver/nf-lmserver-netserverenum) function and specify SV\_TYPE\_DIALIN for the *servertype* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="f83d7-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="f83d7-124">Requirements</span></span>



| <span data-ttu-id="f83d7-125">需求</span><span class="sxs-lookup"><span data-stu-id="f83d7-125">Requirement</span></span> | <span data-ttu-id="f83d7-126">值</span><span class="sxs-lookup"><span data-stu-id="f83d7-126">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f83d7-127">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="f83d7-127">End of client support</span></span><br/> | <span data-ttu-id="f83d7-128">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f83d7-128">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="f83d7-129">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="f83d7-129">End of server support</span></span><br/> | <span data-ttu-id="f83d7-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f83d7-130">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="f83d7-131">標頭</span><span class="sxs-lookup"><span data-stu-id="f83d7-131">Header</span></span><br/>                | <dl> <span data-ttu-id="f83d7-132"><dt>Rassapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="f83d7-132"><dt>Rassapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="f83d7-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="f83d7-133">Library</span></span><br/>               | <dl> <span data-ttu-id="f83d7-134"><dt>Rassapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f83d7-134"><dt>Rassapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="f83d7-135">DLL</span><span class="sxs-lookup"><span data-stu-id="f83d7-135">DLL</span></span><br/>                   | <dl> <span data-ttu-id="f83d7-136"><dt>Rassapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f83d7-136"><dt>Rassapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f83d7-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f83d7-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f83d7-138">遠端存取服務 (RAS) 總覽</span><span class="sxs-lookup"><span data-stu-id="f83d7-138">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="f83d7-139">RAS 伺服器管理功能</span><span class="sxs-lookup"><span data-stu-id="f83d7-139">RAS Server Administration Functions</span></span>](ras-server-administration-functions.md)
</dt> <dt>

[<span data-ttu-id="f83d7-140">**NetServerEnum**</span><span class="sxs-lookup"><span data-stu-id="f83d7-140">**NetServerEnum**</span></span>](/windows/win32/api/lmserver/nf-lmserver-netserverenum)
</dt> <dt>

[<span data-ttu-id="f83d7-141">**RAS \_ 伺服器 \_ 0**</span><span class="sxs-lookup"><span data-stu-id="f83d7-141">**RAS\_SERVER\_0**</span></span>](ras-server-0-str.md)
</dt> </dl>

 

