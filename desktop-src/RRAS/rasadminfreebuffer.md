---
title: 'RasAdminFreeBuffer 函式 (Rassapi) '
description: RasAdminFreeBuffer 函式會釋出由 RAS 代表呼叫端所配置的記憶體。
ms.assetid: 6dfbba22-3af1-4771-8c22-506996f30c6b
keywords:
- RasAdminFreeBuffer 函式 RAS
topic_type:
- apiref
api_name:
- RasAdminFreeBuffer
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bf86a3005a2b865b2096eddc5ffa9c0c33f848a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991265"
---
# <a name="rasadminfreebuffer-function"></a><span data-ttu-id="53a52-104">RasAdminFreeBuffer 函式</span><span class="sxs-lookup"><span data-stu-id="53a52-104">RasAdminFreeBuffer function</span></span>

<span data-ttu-id="53a52-105">\[這項功能僅提供給 Windows NT Server 4.0 的回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="53a52-105">\[This function is provided only for backward compatibility with Windows NT Server 4.0.</span></span> <span data-ttu-id="53a52-106">它會傳回 \_ \_ 未 \_ 在 Windows Server 2003 上執行的錯誤呼叫。</span><span class="sxs-lookup"><span data-stu-id="53a52-106">It returns ERROR\_CALL\_NOT\_IMPLEMENTED on Windows Server 2003.</span></span> <span data-ttu-id="53a52-107">應用程式應該使用 [**MprAdminBufferFree**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminbufferfree) 函式。\]</span><span class="sxs-lookup"><span data-stu-id="53a52-107">Applications should use the [**MprAdminBufferFree**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminbufferfree) function.\]</span></span>

<span data-ttu-id="53a52-108">**RasAdminFreeBuffer** 函式會釋出由 RAS 代表呼叫端所配置的記憶體。</span><span class="sxs-lookup"><span data-stu-id="53a52-108">The **RasAdminFreeBuffer** function frees memory that was allocated by RAS on behalf of the caller.</span></span>

## <a name="syntax"></a><span data-ttu-id="53a52-109">語法</span><span class="sxs-lookup"><span data-stu-id="53a52-109">Syntax</span></span>


```C++
DWORD RasAdminFreeBuffer(
  _In_ PVOID Pointer
);
```



## <a name="parameters"></a><span data-ttu-id="53a52-110">參數</span><span class="sxs-lookup"><span data-stu-id="53a52-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53a52-111">*指標* \[在\]</span><span class="sxs-lookup"><span data-stu-id="53a52-111">*Pointer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53a52-112">要釋放之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="53a52-112">Pointer to the buffer to be freed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53a52-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="53a52-113">Return value</span></span>

<span data-ttu-id="53a52-114">如果函式成功，則傳回值為「錯誤 \_ 成功」。</span><span class="sxs-lookup"><span data-stu-id="53a52-114">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="53a52-115">如果函式失敗，則傳回值可能是下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="53a52-115">If the function fails, the return value can be the following error code.</span></span>



| <span data-ttu-id="53a52-116">值</span><span class="sxs-lookup"><span data-stu-id="53a52-116">Value</span></span>                                                                                                    | <span data-ttu-id="53a52-117">意義</span><span class="sxs-lookup"><span data-stu-id="53a52-117">Meaning</span></span>                                        |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="53a52-118"><dt>**錯誤 \_ 不正確 \_ 參數**</dt></span><span class="sxs-lookup"><span data-stu-id="53a52-118"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl> | <span data-ttu-id="53a52-119">*指標* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="53a52-119">The *Pointer* parameter is invalid.</span></span><br/> |



 

<span data-ttu-id="53a52-120">此函數沒有任何延伸的錯誤資訊;請勿呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)。</span><span class="sxs-lookup"><span data-stu-id="53a52-120">There is no extended error information for this function; do not call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="53a52-121">備註</span><span class="sxs-lookup"><span data-stu-id="53a52-121">Remarks</span></span>

<span data-ttu-id="53a52-122">您可以使用 **RasAdminFreeBuffer** 函式來釋放 [**RasAdminPortEnum**](rasadminportenum.md) 和 [**RasAdminPortGetInfo**](rasadminportgetinfo.md) 函式所配置的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="53a52-122">Use the **RasAdminFreeBuffer** function to free the buffers allocated by the [**RasAdminPortEnum**](rasadminportenum.md) and [**RasAdminPortGetInfo**](rasadminportgetinfo.md) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="53a52-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="53a52-123">Requirements</span></span>



| <span data-ttu-id="53a52-124">需求</span><span class="sxs-lookup"><span data-stu-id="53a52-124">Requirement</span></span> | <span data-ttu-id="53a52-125">值</span><span class="sxs-lookup"><span data-stu-id="53a52-125">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="53a52-126">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="53a52-126">End of client support</span></span><br/> | <span data-ttu-id="53a52-127">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="53a52-127">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="53a52-128">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="53a52-128">End of server support</span></span><br/> | <span data-ttu-id="53a52-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="53a52-129">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="53a52-130">標頭</span><span class="sxs-lookup"><span data-stu-id="53a52-130">Header</span></span><br/>                | <dl> <span data-ttu-id="53a52-131"><dt>Rassapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="53a52-131"><dt>Rassapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="53a52-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="53a52-132">Library</span></span><br/>               | <dl> <span data-ttu-id="53a52-133"><dt>Rassapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="53a52-133"><dt>Rassapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="53a52-134">DLL</span><span class="sxs-lookup"><span data-stu-id="53a52-134">DLL</span></span><br/>                   | <dl> <span data-ttu-id="53a52-135"><dt>Rassapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53a52-135"><dt>Rassapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53a52-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="53a52-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53a52-137">遠端存取服務 (RAS) 總覽</span><span class="sxs-lookup"><span data-stu-id="53a52-137">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="53a52-138">RAS 伺服器管理功能</span><span class="sxs-lookup"><span data-stu-id="53a52-138">RAS Server Administration Functions</span></span>](ras-server-administration-functions.md)
</dt> <dt>

[<span data-ttu-id="53a52-139">**RasAdminPortEnum**</span><span class="sxs-lookup"><span data-stu-id="53a52-139">**RasAdminPortEnum**</span></span>](rasadminportenum.md)
</dt> <dt>

[<span data-ttu-id="53a52-140">**RasAdminPortGetInfo**</span><span class="sxs-lookup"><span data-stu-id="53a52-140">**RasAdminPortGetInfo**</span></span>](rasadminportgetinfo.md)
</dt> </dl>

 

