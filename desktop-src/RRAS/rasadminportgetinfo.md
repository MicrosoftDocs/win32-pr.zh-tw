---
title: 'RasAdminPortGetInfo 函式 (Rassapi) '
description: RasAdminPortGetInfo 函式會在指定的伺服器上抓取指定埠的相關資訊。
ms.assetid: 22837685-62a4-4e55-b88f-11019d5d4154
keywords:
- RasAdminPortGetInfo 函式 RAS
topic_type:
- apiref
api_name:
- RasAdminPortGetInfo
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8d80c55b3182ec930732344cb7857f99c0dc411
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983133"
---
# <a name="rasadminportgetinfo-function"></a><span data-ttu-id="45c35-104">RasAdminPortGetInfo 函式</span><span class="sxs-lookup"><span data-stu-id="45c35-104">RasAdminPortGetInfo function</span></span>

<span data-ttu-id="45c35-105">\[這項功能僅提供給 Windows NT Server 4.0 的回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="45c35-105">\[This function is provided only for backward compatibility with Windows NT Server 4.0.</span></span> <span data-ttu-id="45c35-106">它會傳回 \_ \_ 未 \_ 在 Windows Server 2003 上執行的錯誤呼叫。</span><span class="sxs-lookup"><span data-stu-id="45c35-106">It returns ERROR\_CALL\_NOT\_IMPLEMENTED on Windows Server 2003.</span></span> <span data-ttu-id="45c35-107">應用程式應該使用 [**MprAdminPortGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo) 函式。\]</span><span class="sxs-lookup"><span data-stu-id="45c35-107">Applications should use the [**MprAdminPortGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo) function.\]</span></span>

<span data-ttu-id="45c35-108">**RasAdminPortGetInfo** 函式會在指定的伺服器上抓取指定埠的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="45c35-108">The **RasAdminPortGetInfo** function retrieves information about a specified port on a specified server.</span></span>

## <a name="syntax"></a><span data-ttu-id="45c35-109">語法</span><span class="sxs-lookup"><span data-stu-id="45c35-109">Syntax</span></span>


```C++
DWORD RasAdminPortGetInfo(
  _In_  const WCHAR               *lpszServer,
  _In_  const WCHAR               *lpszPort,
  _Out_       RAS_PORT_1          *pRasPort1,
  _Out_       RAS_PORT_STATISTICS *pRasStats,
  _Out_       RAS_PARAMETERS      **ppRasParams
);
```



## <a name="parameters"></a><span data-ttu-id="45c35-110">參數</span><span class="sxs-lookup"><span data-stu-id="45c35-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45c35-111">*lpszServer* \[在\]</span><span class="sxs-lookup"><span data-stu-id="45c35-111">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45c35-112">以 null 結束的 Unicode 字串指標，指定 RAS 伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="45c35-112">Pointer to a null-terminated Unicode string that specifies the name of the RAS server.</span></span> <span data-ttu-id="45c35-113">\\ \\ 請以下列格式指定開頭為 "" 字元的名稱： \\ \\ *servername*。</span><span class="sxs-lookup"><span data-stu-id="45c35-113">Specify the name with leading "\\\\" characters, in the form: \\\\*servername*.</span></span>

</dd> <dt>

<span data-ttu-id="45c35-114">*lpszPort* \[在\]</span><span class="sxs-lookup"><span data-stu-id="45c35-114">*lpszPort* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45c35-115">以 null 結束的 Unicode 字串指標，指定伺服器上的埠名稱。</span><span class="sxs-lookup"><span data-stu-id="45c35-115">Pointer to a null-terminated Unicode string that specifies the name of the port on the server.</span></span>

</dd> <dt>

<span data-ttu-id="45c35-116">*pRasPort1* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="45c35-116">*pRasPort1* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="45c35-117">[**RAS \_ 埠 \_ 1**](ras-port-1-str.md)結構的指標，該函式會填入埠的狀態相關資訊。</span><span class="sxs-lookup"><span data-stu-id="45c35-117">Pointer to the [**RAS\_PORT\_1**](ras-port-1-str.md) structure that the function fills in with information about the state of the port.</span></span>

</dd> <dt>

<span data-ttu-id="45c35-118">*pRasStats* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="45c35-118">*pRasStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="45c35-119">[**RAS \_ 埠 \_ 統計**](ras-port-statistics-str.md)結構的指標，該函式會填入與埠相關的統計資料。</span><span class="sxs-lookup"><span data-stu-id="45c35-119">Pointer to the [**RAS\_PORT\_STATISTICS**](ras-port-statistics-str.md) structure that the function fills in with statistics about the port.</span></span>

</dd> <dt>

<span data-ttu-id="45c35-120">*ppRasParams* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="45c35-120">*ppRasParams* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="45c35-121">指標變數的指標，此變數會接收 [**RAS \_ 參數**](ras-parameters-str.md) 結構陣列的位址。</span><span class="sxs-lookup"><span data-stu-id="45c35-121">Pointer to a pointer variable that receives the address of an array of [**RAS\_PARAMETERS**](ras-parameters-str.md) structures.</span></span> <span data-ttu-id="45c35-122">每個結構都包含媒體專用索引鍵的名稱，例如 MAXCONNECTBPS 及其相關聯的值。</span><span class="sxs-lookup"><span data-stu-id="45c35-122">Each structure contains the name of a media-specific key, such as MAXCONNECTBPS, and its associated value.</span></span> <span data-ttu-id="45c35-123">當應用程式完成此記憶體時，請呼叫 [**RasAdminFreeBuffer**](rasadminfreebuffer.md) 函式來釋放它。</span><span class="sxs-lookup"><span data-stu-id="45c35-123">When the application is finished with this memory, free it by calling the [**RasAdminFreeBuffer**](rasadminfreebuffer.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45c35-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="45c35-124">Return value</span></span>

<span data-ttu-id="45c35-125">如果函式成功，則傳回值為「錯誤 \_ 成功」。</span><span class="sxs-lookup"><span data-stu-id="45c35-125">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="45c35-126">如果函式失敗，則傳回值可以是下列其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="45c35-126">If the function fails, the return value can be one of the following error codes.</span></span>



| <span data-ttu-id="45c35-127">值</span><span class="sxs-lookup"><span data-stu-id="45c35-127">Value</span></span>                                                                                                     | <span data-ttu-id="45c35-128">意義</span><span class="sxs-lookup"><span data-stu-id="45c35-128">Meaning</span></span>                                                                          |
|-----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="45c35-129"><dt>**錯誤 \_ 開發人員 \_ 不 \_ 存在**</dt></span><span class="sxs-lookup"><span data-stu-id="45c35-129"><dt>**ERROR\_DEV\_NOT\_EXIST**</dt></span></span> </dl>     | <span data-ttu-id="45c35-130">指定的埠無效。</span><span class="sxs-lookup"><span data-stu-id="45c35-130">The specified port is invalid.</span></span><br/>                                        |
| <dl> <span data-ttu-id="45c35-131"><dt>**錯誤 \_ 沒有 \_ 足夠的 \_ 記憶體**</dt></span><span class="sxs-lookup"><span data-stu-id="45c35-131"><dt>**ERROR\_NOT\_ENOUGH\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="45c35-132">記憶體不足，無法配置 *ppRasParams* 陣列的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="45c35-132">Insufficient memory to allocate a buffer for the *ppRasParams* array.</span></span><br/> |



 

<span data-ttu-id="45c35-133">此函數沒有任何延伸的錯誤資訊;請勿呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)。</span><span class="sxs-lookup"><span data-stu-id="45c35-133">There is no extended error information for this function; do not call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="requirements"></a><span data-ttu-id="45c35-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="45c35-134">Requirements</span></span>



| <span data-ttu-id="45c35-135">需求</span><span class="sxs-lookup"><span data-stu-id="45c35-135">Requirement</span></span> | <span data-ttu-id="45c35-136">值</span><span class="sxs-lookup"><span data-stu-id="45c35-136">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="45c35-137">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="45c35-137">End of client support</span></span><br/> | <span data-ttu-id="45c35-138">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="45c35-138">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="45c35-139">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="45c35-139">End of server support</span></span><br/> | <span data-ttu-id="45c35-140">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="45c35-140">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="45c35-141">標頭</span><span class="sxs-lookup"><span data-stu-id="45c35-141">Header</span></span><br/>                | <dl> <span data-ttu-id="45c35-142"><dt>Rassapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="45c35-142"><dt>Rassapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="45c35-143">程式庫</span><span class="sxs-lookup"><span data-stu-id="45c35-143">Library</span></span><br/>               | <dl> <span data-ttu-id="45c35-144"><dt>Rassapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="45c35-144"><dt>Rassapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="45c35-145">DLL</span><span class="sxs-lookup"><span data-stu-id="45c35-145">DLL</span></span><br/>                   | <dl> <span data-ttu-id="45c35-146"><dt>Rassapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="45c35-146"><dt>Rassapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45c35-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="45c35-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45c35-148">遠端存取服務 (RAS) 總覽</span><span class="sxs-lookup"><span data-stu-id="45c35-148">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="45c35-149">RAS 伺服器管理功能</span><span class="sxs-lookup"><span data-stu-id="45c35-149">RAS Server Administration Functions</span></span>](ras-server-administration-functions.md)
</dt> <dt>

[<span data-ttu-id="45c35-150">**RAS \_ 參數**</span><span class="sxs-lookup"><span data-stu-id="45c35-150">**RAS\_PARAMETERS**</span></span>](ras-parameters-str.md)
</dt> <dt>

[<span data-ttu-id="45c35-151">**RAS \_ 埠 \_ 1**</span><span class="sxs-lookup"><span data-stu-id="45c35-151">**RAS\_PORT\_1**</span></span>](ras-port-1-str.md)
</dt> <dt>

[<span data-ttu-id="45c35-152">**RAS \_ 埠 \_ 統計資料**</span><span class="sxs-lookup"><span data-stu-id="45c35-152">**RAS\_PORT\_STATISTICS**</span></span>](ras-port-statistics-str.md)
</dt> <dt>

[<span data-ttu-id="45c35-153">**RasAdminFreeBuffer**</span><span class="sxs-lookup"><span data-stu-id="45c35-153">**RasAdminFreeBuffer**</span></span>](rasadminfreebuffer.md)
</dt> </dl>

 

