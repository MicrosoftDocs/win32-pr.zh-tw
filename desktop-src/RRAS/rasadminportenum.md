---
title: 'RasAdminPortEnum 函式 (Rassapi) '
description: RasAdminPortEnum 函式會列舉指定的 RAS 伺服器上的所有埠。 針對伺服器上的每個通訊埠，此函式 \_ \_ 會傳回包含埠相關資訊的 RAS 埠0結構。
ms.assetid: ad23727c-8f54-4b10-9bc7-1425ac22bc88
keywords:
- RasAdminPortEnum 函式 RAS
topic_type:
- apiref
api_name:
- RasAdminPortEnum
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5e4841627ce5df3feee3f885b399a070388ed55
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001567"
---
# <a name="rasadminportenum-function"></a><span data-ttu-id="38ed4-105">RasAdminPortEnum 函式</span><span class="sxs-lookup"><span data-stu-id="38ed4-105">RasAdminPortEnum function</span></span>

<span data-ttu-id="38ed4-106">\[這項功能僅提供給 Windows NT Server 4.0 的回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="38ed4-106">\[This function is provided only for backward compatibility with Windows NT Server 4.0.</span></span> <span data-ttu-id="38ed4-107">它會傳回 \_ \_ 未 \_ 在 Windows Server 2003 上執行的錯誤呼叫。</span><span class="sxs-lookup"><span data-stu-id="38ed4-107">It returns ERROR\_CALL\_NOT\_IMPLEMENTED on Windows Server 2003.</span></span> <span data-ttu-id="38ed4-108">應用程式應該使用 [**MprAdminPortEnum**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportenum) 函式。\]</span><span class="sxs-lookup"><span data-stu-id="38ed4-108">Applications should use the [**MprAdminPortEnum**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportenum) function.\]</span></span>

<span data-ttu-id="38ed4-109">**RasAdminPortEnum** 函式會列舉指定的 RAS 伺服器上的所有埠。</span><span class="sxs-lookup"><span data-stu-id="38ed4-109">The **RasAdminPortEnum** function enumerates all ports on the specified RAS server.</span></span> <span data-ttu-id="38ed4-110">針對伺服器上的每個通訊埠，此函式會傳回包含埠相關資訊的 [**RAS \_ 埠 \_ 0**](ras-port-0-str.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="38ed4-110">For each port on the server, the function returns the [**RAS\_PORT\_0**](ras-port-0-str.md) structure that contains information about the port.</span></span>

## <a name="syntax"></a><span data-ttu-id="38ed4-111">語法</span><span class="sxs-lookup"><span data-stu-id="38ed4-111">Syntax</span></span>


```C++
DWORD RasAdminPortEnum(
  _In_  const WCHAR       *lpszServer,
  _Out_       PRAS_PORT_0 *ppRasPort0,
  _Out_       WORD        *pcEntriesRead
);
```



## <a name="parameters"></a><span data-ttu-id="38ed4-112">參數</span><span class="sxs-lookup"><span data-stu-id="38ed4-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38ed4-113">*lpszServer* \[在\]</span><span class="sxs-lookup"><span data-stu-id="38ed4-113">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38ed4-114">以 null 結束的 Unicode 字串指標，指定 RAS 伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="38ed4-114">Pointer to a null-terminated Unicode string that specifies the name of the RAS server.</span></span> <span data-ttu-id="38ed4-115">\\ \\ 請以下列格式指定開頭為 "" 字元的名稱： \\ \\ *servername*。</span><span class="sxs-lookup"><span data-stu-id="38ed4-115">Specify the name with leading "\\\\" characters, in the form: \\\\*servername*.</span></span>

</dd> <dt>

<span data-ttu-id="38ed4-116">*ppRasPort0* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="38ed4-116">*ppRasPort0* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="38ed4-117">變數的指標，此變數會接收包含 [**RAS \_ 埠 \_ 0**](ras-port-0-str.md) 結構陣列的緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="38ed4-117">Pointer to a variable that receives a pointer to a buffer that contains an array of [**RAS\_PORT\_0**](ras-port-0-str.md) structures.</span></span> <span data-ttu-id="38ed4-118">當應用程式完成記憶體時，請呼叫 [**RasAdminFreeBuffer**](rasadminfreebuffer.md) 函式來釋放它。</span><span class="sxs-lookup"><span data-stu-id="38ed4-118">When the application has finished with the memory, free it by calling the [**RasAdminFreeBuffer**](rasadminfreebuffer.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="38ed4-119">*pcEntriesRead* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="38ed4-119">*pcEntriesRead* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="38ed4-120">16位變數的指標，此變數會接收在 *ppRasPort0* 陣列中傳回的 [**RAS \_ 埠 \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_0)結構總數。</span><span class="sxs-lookup"><span data-stu-id="38ed4-120">Pointer to a 16-bit variable that receives the total number of [**RAS\_PORT\_0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_0) structures returned in the *ppRasPort0* array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38ed4-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="38ed4-121">Return value</span></span>

<span data-ttu-id="38ed4-122">如果函式成功，則傳回值為「錯誤 \_ 成功」。</span><span class="sxs-lookup"><span data-stu-id="38ed4-122">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="38ed4-123">如果函式失敗，則傳回值可能是下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="38ed4-123">If the function fails, the return value can be the following error code.</span></span>



| <span data-ttu-id="38ed4-124">值</span><span class="sxs-lookup"><span data-stu-id="38ed4-124">Value</span></span>                                                                                             | <span data-ttu-id="38ed4-125">意義</span><span class="sxs-lookup"><span data-stu-id="38ed4-125">Meaning</span></span>                                                                                                                                     |
|---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="38ed4-126"><dt>**NERR \_ ItemNotFound**</dt></span><span class="sxs-lookup"><span data-stu-id="38ed4-126"><dt>**NERR\_ItemNotFound**</dt></span></span> </dl> | <span data-ttu-id="38ed4-127">無法列舉任何埠。</span><span class="sxs-lookup"><span data-stu-id="38ed4-127">No ports could be enumerated.</span></span> <span data-ttu-id="38ed4-128">這可能是因為伺服器上所有設定的埠目前正在用於撥出。</span><span class="sxs-lookup"><span data-stu-id="38ed4-128">This could be because all configured ports on the server are currently being used for dialing out.</span></span><br/> |



 

<span data-ttu-id="38ed4-129">此函數沒有任何延伸的錯誤資訊;請勿呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)。</span><span class="sxs-lookup"><span data-stu-id="38ed4-129">There is no extended error information for this function; do not call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="requirements"></a><span data-ttu-id="38ed4-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="38ed4-130">Requirements</span></span>



| <span data-ttu-id="38ed4-131">需求</span><span class="sxs-lookup"><span data-stu-id="38ed4-131">Requirement</span></span> | <span data-ttu-id="38ed4-132">值</span><span class="sxs-lookup"><span data-stu-id="38ed4-132">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="38ed4-133">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="38ed4-133">End of client support</span></span><br/> | <span data-ttu-id="38ed4-134">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="38ed4-134">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="38ed4-135">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="38ed4-135">End of server support</span></span><br/> | <span data-ttu-id="38ed4-136">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="38ed4-136">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="38ed4-137">標頭</span><span class="sxs-lookup"><span data-stu-id="38ed4-137">Header</span></span><br/>                | <dl> <span data-ttu-id="38ed4-138"><dt>Rassapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="38ed4-138"><dt>Rassapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="38ed4-139">程式庫</span><span class="sxs-lookup"><span data-stu-id="38ed4-139">Library</span></span><br/>               | <dl> <span data-ttu-id="38ed4-140"><dt>Rassapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="38ed4-140"><dt>Rassapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="38ed4-141">DLL</span><span class="sxs-lookup"><span data-stu-id="38ed4-141">DLL</span></span><br/>                   | <dl> <span data-ttu-id="38ed4-142"><dt>Rassapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="38ed4-142"><dt>Rassapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38ed4-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="38ed4-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38ed4-144">遠端存取服務 (RAS) 總覽</span><span class="sxs-lookup"><span data-stu-id="38ed4-144">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="38ed4-145">RAS 伺服器管理功能</span><span class="sxs-lookup"><span data-stu-id="38ed4-145">RAS Server Administration Functions</span></span>](ras-server-administration-functions.md)
</dt> <dt>

[<span data-ttu-id="38ed4-146">**RAS \_ 埠 \_ 0**</span><span class="sxs-lookup"><span data-stu-id="38ed4-146">**RAS\_PORT\_0**</span></span>](ras-port-0-str.md)
</dt> <dt>

[<span data-ttu-id="38ed4-147">**RasAdminFreeBuffer**</span><span class="sxs-lookup"><span data-stu-id="38ed4-147">**RasAdminFreeBuffer**</span></span>](rasadminfreebuffer.md)
</dt> </dl>

 

