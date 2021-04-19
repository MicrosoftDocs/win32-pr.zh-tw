---
title: 'RasAdminPortClearStatistics 函式 (Rassapi) '
description: RasAdminPortClearStatistics 函式會重設計數器，此計數器代表 RAS \_ 埠統計資料結構中 RasAdminPortGetInfo 函數所報告的各種統計資料 \_ 。 計數器會重設為零，並開始累積。
ms.assetid: d2ce4652-1034-4ded-aa26-2678c719d5b9
keywords:
- RasAdminPortClearStatistics 函式 RAS
topic_type:
- apiref
api_name:
- RasAdminPortClearStatistics
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57943fbefcba1625c7badff25827c62eaca8a8c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977707"
---
# <a name="rasadminportclearstatistics-function"></a><span data-ttu-id="a4b14-105">RasAdminPortClearStatistics 函式</span><span class="sxs-lookup"><span data-stu-id="a4b14-105">RasAdminPortClearStatistics function</span></span>

<span data-ttu-id="a4b14-106">\[這項功能僅提供給 Windows NT Server 4.0 的回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="a4b14-106">\[This function is provided only for backward compatibility with Windows NT Server 4.0.</span></span> <span data-ttu-id="a4b14-107">它會傳回 \_ \_ 未 \_ 在 Windows Server 2003 上執行的錯誤呼叫。</span><span class="sxs-lookup"><span data-stu-id="a4b14-107">It returns ERROR\_CALL\_NOT\_IMPLEMENTED on Windows Server 2003.</span></span> <span data-ttu-id="a4b14-108">應用程式應該使用 [**MprAdminPortClearStats**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats) 函式。\]</span><span class="sxs-lookup"><span data-stu-id="a4b14-108">Applications should use the [**MprAdminPortClearStats**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats) function.\]</span></span>

<span data-ttu-id="a4b14-109">**RasAdminPortClearStatistics** 函式會重設計數器，此計數器代表 [**RAS \_ 埠 \_ 統計資料**](ras-port-statistics-str.md)結構中 [**RasAdminPortGetInfo**](rasadminportgetinfo.md)函數所報告的各種統計資料。</span><span class="sxs-lookup"><span data-stu-id="a4b14-109">The **RasAdminPortClearStatistics** function resets the counters representing the various statistics reported by the [**RasAdminPortGetInfo**](rasadminportgetinfo.md) function in the [**RAS\_PORT\_STATISTICS**](ras-port-statistics-str.md) structure.</span></span> <span data-ttu-id="a4b14-110">計數器會重設為零，並開始累積。</span><span class="sxs-lookup"><span data-stu-id="a4b14-110">The counters are reset to zero and start accumulating.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4b14-111">語法</span><span class="sxs-lookup"><span data-stu-id="a4b14-111">Syntax</span></span>


```C++
DWORD RasAdminPortClearStatistics(
  _In_ const WCHAR *lpszServer,
  _In_ const WCHAR *lpszPort
);
```



## <a name="parameters"></a><span data-ttu-id="a4b14-112">參數</span><span class="sxs-lookup"><span data-stu-id="a4b14-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4b14-113">*lpszServer* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a4b14-113">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4b14-114">以 null 結束的 Unicode 字串指標，指定 RAS 伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="a4b14-114">Pointer to a null-terminated Unicode string that specifies the name of the RAS server.</span></span> <span data-ttu-id="a4b14-115">\\ \\ 請以下列格式指定開頭為 "" 字元的名稱： \\ \\ *servername*。</span><span class="sxs-lookup"><span data-stu-id="a4b14-115">Specify the name with leading "\\\\" characters, in the form: \\\\*servername*.</span></span>

</dd> <dt>

<span data-ttu-id="a4b14-116">*lpszPort* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a4b14-116">*lpszPort* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4b14-117">以 null 結束的 Unicode 字串指標，指定伺服器上的埠名稱。</span><span class="sxs-lookup"><span data-stu-id="a4b14-117">Pointer to a null-terminated Unicode string that specifies the name of the port on the server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4b14-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="a4b14-118">Return value</span></span>

<span data-ttu-id="a4b14-119">如果函式成功，則傳回值為「錯誤 \_ 成功」。</span><span class="sxs-lookup"><span data-stu-id="a4b14-119">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="a4b14-120">如果函式失敗，則傳回值可能是下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="a4b14-120">If the function fails, the return value can be the following error code.</span></span>



| <span data-ttu-id="a4b14-121">值</span><span class="sxs-lookup"><span data-stu-id="a4b14-121">Value</span></span>                                                                                                 | <span data-ttu-id="a4b14-122">意義</span><span class="sxs-lookup"><span data-stu-id="a4b14-122">Meaning</span></span>                                   |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="a4b14-123"><dt>**錯誤 \_ 開發人員 \_ 不 \_ 存在**</dt></span><span class="sxs-lookup"><span data-stu-id="a4b14-123"><dt>**ERROR\_DEV\_NOT\_EXIST**</dt></span></span> </dl> | <span data-ttu-id="a4b14-124">指定的埠無效。</span><span class="sxs-lookup"><span data-stu-id="a4b14-124">The specified port is invalid.</span></span><br/> |



 

<span data-ttu-id="a4b14-125">此函數沒有任何延伸的錯誤資訊;請勿呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)。</span><span class="sxs-lookup"><span data-stu-id="a4b14-125">There is no extended error information for this function; do not call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="a4b14-126">備註</span><span class="sxs-lookup"><span data-stu-id="a4b14-126">Remarks</span></span>

<span data-ttu-id="a4b14-127">**RasAdminPortClearStatistics** 函式會清除伺服器上的統計資料，而不是在進行呼叫的應用程式中的本機。</span><span class="sxs-lookup"><span data-stu-id="a4b14-127">The **RasAdminPortClearStatistics** function clears the statistics on the server, not locally within the application that makes the call.</span></span> <span data-ttu-id="a4b14-128">這表示，針對監視指定埠的任何其他應用程式，也會重設統計資料。</span><span class="sxs-lookup"><span data-stu-id="a4b14-128">This means that the statistics are also reset for any other application that is monitoring the specified port.</span></span>

<span data-ttu-id="a4b14-129">如果 *lpszPort* 埠是多重連結連接的一部分， **RasAdminPortClearStatistics** 會重設指定之埠的統計資料，而函式也會重設多重連結連接的累計統計資料。</span><span class="sxs-lookup"><span data-stu-id="a4b14-129">If the *lpszPort* port is part of a multilink connection, **RasAdminPortClearStatistics** resets the statistics for the specified port, The function also resets the cumulative statistics for the multilink connection.</span></span> <span data-ttu-id="a4b14-130">不過，此函式不會影響屬於多重連結連接之其他埠的個別統計資料。</span><span class="sxs-lookup"><span data-stu-id="a4b14-130">However, the function does not effect the individual statistics for other ports that are part of the multilink connection.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4b14-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="a4b14-131">Requirements</span></span>



| <span data-ttu-id="a4b14-132">需求</span><span class="sxs-lookup"><span data-stu-id="a4b14-132">Requirement</span></span> | <span data-ttu-id="a4b14-133">值</span><span class="sxs-lookup"><span data-stu-id="a4b14-133">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a4b14-134">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="a4b14-134">End of client support</span></span><br/> | <span data-ttu-id="a4b14-135">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="a4b14-135">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="a4b14-136">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="a4b14-136">End of server support</span></span><br/> | <span data-ttu-id="a4b14-137">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a4b14-137">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="a4b14-138">標頭</span><span class="sxs-lookup"><span data-stu-id="a4b14-138">Header</span></span><br/>                | <dl> <span data-ttu-id="a4b14-139"><dt>Rassapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="a4b14-139"><dt>Rassapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="a4b14-140">程式庫</span><span class="sxs-lookup"><span data-stu-id="a4b14-140">Library</span></span><br/>               | <dl> <span data-ttu-id="a4b14-141"><dt>Rassapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a4b14-141"><dt>Rassapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="a4b14-142">DLL</span><span class="sxs-lookup"><span data-stu-id="a4b14-142">DLL</span></span><br/>                   | <dl> <span data-ttu-id="a4b14-143"><dt>Rassapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4b14-143"><dt>Rassapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4b14-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a4b14-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4b14-145">遠端存取服務 (RAS) 總覽</span><span class="sxs-lookup"><span data-stu-id="a4b14-145">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="a4b14-146">RAS 伺服器管理功能</span><span class="sxs-lookup"><span data-stu-id="a4b14-146">RAS Server Administration Functions</span></span>](ras-server-administration-functions.md)
</dt> <dt>

[<span data-ttu-id="a4b14-147">**RAS \_ 埠 \_ 統計資料**</span><span class="sxs-lookup"><span data-stu-id="a4b14-147">**RAS\_PORT\_STATISTICS**</span></span>](ras-port-statistics-str.md)
</dt> <dt>

[<span data-ttu-id="a4b14-148">**RasAdminPortGetInfo**</span><span class="sxs-lookup"><span data-stu-id="a4b14-148">**RasAdminPortGetInfo**</span></span>](rasadminportgetinfo.md)
</dt> </dl>

 

