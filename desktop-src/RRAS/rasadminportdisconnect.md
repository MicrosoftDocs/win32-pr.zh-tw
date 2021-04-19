---
title: 'RasAdminPortDisconnect 函式 (Rassapi) '
description: RasAdminPortDisconnect 函式會中斷目前正在使用的通訊埠。
ms.assetid: 7ed3bc46-2d56-44c8-afd5-fcbdad0f7f3a
keywords:
- RasAdminPortDisconnect 函式 RAS
topic_type:
- apiref
api_name:
- RasAdminPortDisconnect
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee05e7927bd6c9adb086a09f76b9022affd74792
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000898"
---
# <a name="rasadminportdisconnect-function"></a><span data-ttu-id="af310-104">RasAdminPortDisconnect 函式</span><span class="sxs-lookup"><span data-stu-id="af310-104">RasAdminPortDisconnect function</span></span>

<span data-ttu-id="af310-105">\[這項功能僅提供給 Windows NT Server 4.0 的回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="af310-105">\[This function is provided only for backward compatibility with Windows NT Server 4.0.</span></span> <span data-ttu-id="af310-106">它會傳回 \_ \_ 未 \_ 在 Windows Server 2003 上執行的錯誤呼叫。</span><span class="sxs-lookup"><span data-stu-id="af310-106">It returns ERROR\_CALL\_NOT\_IMPLEMENTED on Windows Server 2003.</span></span> <span data-ttu-id="af310-107">應用程式應該使用 [**MprAdminPortDisconnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportdisconnect) 函式。\]</span><span class="sxs-lookup"><span data-stu-id="af310-107">Applications should use the [**MprAdminPortDisconnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportdisconnect) function.\]</span></span>

<span data-ttu-id="af310-108">**RasAdminPortDisconnect** 函式會中斷目前正在使用的通訊埠。</span><span class="sxs-lookup"><span data-stu-id="af310-108">The **RasAdminPortDisconnect** function disconnects a port that is currently in use.</span></span>

## <a name="syntax"></a><span data-ttu-id="af310-109">語法</span><span class="sxs-lookup"><span data-stu-id="af310-109">Syntax</span></span>


```C++
DWORD RasAdminPortDisconnect(
  _In_ const WCHAR *lpszServer,
  _In_ const WCHAR *lpszPort
);
```



## <a name="parameters"></a><span data-ttu-id="af310-110">參數</span><span class="sxs-lookup"><span data-stu-id="af310-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af310-111">*lpszServer* \[在\]</span><span class="sxs-lookup"><span data-stu-id="af310-111">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af310-112">以 null 結束的 Unicode 字串指標，指定 Windows NT/Windows 2000 RAS 伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="af310-112">Pointer to a null-terminated Unicode string that specifies the name of the Windows NT/Windows 2000 RAS server.</span></span> <span data-ttu-id="af310-113">\\ \\ 請以下列格式指定開頭為 "" 字元的名稱： \\ \\ *servername*。</span><span class="sxs-lookup"><span data-stu-id="af310-113">Specify the name with leading "\\\\" characters, in the form: \\\\*servername*.</span></span>

</dd> <dt>

<span data-ttu-id="af310-114">*lpszPort* \[在\]</span><span class="sxs-lookup"><span data-stu-id="af310-114">*lpszPort* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af310-115">以 null 結束的 Unicode 字串指標，指定伺服器上的埠名稱。</span><span class="sxs-lookup"><span data-stu-id="af310-115">Pointer to a null-terminated Unicode string that specifies the name of the port on the server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af310-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="af310-116">Return value</span></span>

<span data-ttu-id="af310-117">如果函式成功，則傳回值為「錯誤 \_ 成功」。</span><span class="sxs-lookup"><span data-stu-id="af310-117">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="af310-118">如果函式失敗，則傳回值可以是下列其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="af310-118">If the function fails, the return value can be one of the following error codes.</span></span>



| <span data-ttu-id="af310-119">值</span><span class="sxs-lookup"><span data-stu-id="af310-119">Value</span></span>                                                                                               | <span data-ttu-id="af310-120">意義</span><span class="sxs-lookup"><span data-stu-id="af310-120">Meaning</span></span>                                      |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="af310-121"><dt>**錯誤 \_ 不正確 \_ 埠**</dt></span><span class="sxs-lookup"><span data-stu-id="af310-121"><dt>**ERROR\_INVALID\_PORT**</dt></span></span> </dl> | <span data-ttu-id="af310-122">指定的埠無效。</span><span class="sxs-lookup"><span data-stu-id="af310-122">The specified port is invalid.</span></span><br/>    |
| <dl> <span data-ttu-id="af310-123"><dt>**NERR \_ UserNotFound**</dt></span><span class="sxs-lookup"><span data-stu-id="af310-123"><dt>**NERR\_UserNotFound**</dt></span></span> </dl>   | <span data-ttu-id="af310-124">埠目前不在使用中。</span><span class="sxs-lookup"><span data-stu-id="af310-124">The port is not currently in use.</span></span><br/> |



 

<span data-ttu-id="af310-125">此函數沒有任何延伸的錯誤資訊;請勿呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)。</span><span class="sxs-lookup"><span data-stu-id="af310-125">There is no extended error information for this function; do not call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="requirements"></a><span data-ttu-id="af310-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="af310-126">Requirements</span></span>



| <span data-ttu-id="af310-127">需求</span><span class="sxs-lookup"><span data-stu-id="af310-127">Requirement</span></span> | <span data-ttu-id="af310-128">值</span><span class="sxs-lookup"><span data-stu-id="af310-128">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="af310-129">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="af310-129">End of client support</span></span><br/> | <span data-ttu-id="af310-130">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="af310-130">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="af310-131">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="af310-131">End of server support</span></span><br/> | <span data-ttu-id="af310-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="af310-132">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="af310-133">標頭</span><span class="sxs-lookup"><span data-stu-id="af310-133">Header</span></span><br/>                | <dl> <span data-ttu-id="af310-134"><dt>Rassapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="af310-134"><dt>Rassapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="af310-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="af310-135">Library</span></span><br/>               | <dl> <span data-ttu-id="af310-136"><dt>Rassapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="af310-136"><dt>Rassapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="af310-137">DLL</span><span class="sxs-lookup"><span data-stu-id="af310-137">DLL</span></span><br/>                   | <dl> <span data-ttu-id="af310-138"><dt>Rassapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="af310-138"><dt>Rassapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af310-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="af310-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af310-140">遠端存取服務 (RAS) 總覽</span><span class="sxs-lookup"><span data-stu-id="af310-140">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="af310-141">RAS 伺服器管理功能</span><span class="sxs-lookup"><span data-stu-id="af310-141">RAS Server Administration Functions</span></span>](ras-server-administration-functions.md)
</dt> </dl>

 

