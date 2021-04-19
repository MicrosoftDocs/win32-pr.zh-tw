---
description: PdhVbGetLogFileSize 函數會傳回指定之記錄檔的大小。 此函數會呼叫 PdhGetLogFileSize。
ms.assetid: 8f4fbb68-b0f5-4163-ae6e-5b7139a35adf
title: PdhVbGetLogFileSize 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbGetLogFileSize
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 0b9f490477704086bd9aa8c53dd32456d486471e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979154"
---
# <a name="pdhvbgetlogfilesize-function"></a><span data-ttu-id="6f5a1-104">PdhVbGetLogFileSize 函式</span><span class="sxs-lookup"><span data-stu-id="6f5a1-104">PdhVbGetLogFileSize function</span></span>

<span data-ttu-id="6f5a1-105">**PdhVbGetLogFileSize** 函數會傳回指定之記錄檔的大小。</span><span class="sxs-lookup"><span data-stu-id="6f5a1-105">The **PdhVbGetLogFileSize** function returns the size of the specified log file.</span></span> <span data-ttu-id="6f5a1-106">此函數會呼叫 [**PdhGetLogFileSize**](/windows/desktop/api/Pdh/nf-pdh-pdhgetlogfilesize)。</span><span class="sxs-lookup"><span data-stu-id="6f5a1-106">This function calls [**PdhGetLogFileSize**](/windows/desktop/api/Pdh/nf-pdh-pdhgetlogfilesize).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6f5a1-107">本主題所描述的功能可能會在未來變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="6f5a1-107">The function that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="6f5a1-108">相反地，Microsoft 建議您使用 [效能計數器](performance-counters-functions.md)函式中所述的功能。</span><span class="sxs-lookup"><span data-stu-id="6f5a1-108">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="6f5a1-109">函式 PdhVbGetLogFileSize ( \_ ByVal HLog 作為 PDH \_ hLog， \_ ByRef LlSize， \_ ) 為 DWORD 的 LONG</span><span class="sxs-lookup"><span data-stu-id="6f5a1-109">Function PdhVbGetLogFileSize( \_ ByVal hLog As PDH\_HLOG, \_ ByRef llSize As LONG \_ ) As DWORD</span></span>

## <a name="parameters"></a><span data-ttu-id="6f5a1-110">參數</span><span class="sxs-lookup"><span data-stu-id="6f5a1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f5a1-111">*hLog* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6f5a1-111">*hLog* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f5a1-112">記錄檔的控制碼。</span><span class="sxs-lookup"><span data-stu-id="6f5a1-112">Handle to the log file.</span></span> <span data-ttu-id="6f5a1-113">[**PdhOpenLog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga)函數會傳回這個控制碼。</span><span class="sxs-lookup"><span data-stu-id="6f5a1-113">This handle is returned by the [**PdhOpenLog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga) function.</span></span>

</dd> <dt>

<span data-ttu-id="6f5a1-114">*llSize* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6f5a1-114">*llSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6f5a1-115">接收記錄檔大小之變數的指標（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="6f5a1-115">Pointer to a variable that receives the size of the log file, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f5a1-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="6f5a1-116">Return value</span></span>

<span data-ttu-id="6f5a1-117">如果函數成功，它會傳回0。</span><span class="sxs-lookup"><span data-stu-id="6f5a1-117">If the function succeeds, it returns 0.</span></span>

<span data-ttu-id="6f5a1-118">如果函式失敗，則傳回值為 [系統錯誤碼](/windows/desktop/Debug/system-error-codes) 或 [PDH 錯誤碼](pdh-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="6f5a1-118">If the function fails, the return value is a [system error code](/windows/desktop/Debug/system-error-codes) or a [PDH error code](pdh-error-codes.md).</span></span> <span data-ttu-id="6f5a1-119">以下是可能的值。</span><span class="sxs-lookup"><span data-stu-id="6f5a1-119">The following are possible values.</span></span>



| <span data-ttu-id="6f5a1-120">傳回碼</span><span class="sxs-lookup"><span data-stu-id="6f5a1-120">Return code</span></span>                                                                                                | <span data-ttu-id="6f5a1-121">Description</span><span class="sxs-lookup"><span data-stu-id="6f5a1-121">Description</span></span>                                                                                            |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6f5a1-122"><dt>**PDH \_ \_ 緩衝區不足**</dt></span><span class="sxs-lookup"><span data-stu-id="6f5a1-122"><dt>**PDH\_INSUFFICIENT\_BUFFER**</dt></span></span> </dl>   | <span data-ttu-id="6f5a1-123">要求的資料大於提供的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="6f5a1-123">The requested data is larger than the buffer supplied.</span></span> <span data-ttu-id="6f5a1-124">無法傳回要求的資料。</span><span class="sxs-lookup"><span data-stu-id="6f5a1-124">Unable to return the requested data.</span></span><br/> |
| <dl> <span data-ttu-id="6f5a1-125"><dt>**PDH \_ 不正確 \_ 引數**</dt></span><span class="sxs-lookup"><span data-stu-id="6f5a1-125"><dt>**PDH\_INVALID\_ARGUMENT**</dt></span></span> </dl>      | <span data-ttu-id="6f5a1-126">一或多個字串緩衝區的大小不正確。</span><span class="sxs-lookup"><span data-stu-id="6f5a1-126">One or more of the string buffers is not the correct size.</span></span><br/>                                  |
| <dl> <span data-ttu-id="6f5a1-127"><dt>**PDH \_ 不正確 \_ 控制碼**</dt></span><span class="sxs-lookup"><span data-stu-id="6f5a1-127"><dt>**PDH\_INVALID\_HANDLE**</dt></span></span> </dl>        | <span data-ttu-id="6f5a1-128">控制碼不是有效的 PDH 物件。</span><span class="sxs-lookup"><span data-stu-id="6f5a1-128">The handle is not a valid PDH object.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="6f5a1-129"><dt>**PDH \_ 記錄 \_ 檔 \_ 開啟 \_ 錯誤**</dt></span><span class="sxs-lookup"><span data-stu-id="6f5a1-129"><dt>**PDH\_LOG\_FILE\_OPEN\_ERROR**</dt></span></span> </dl> | <span data-ttu-id="6f5a1-130">無法開啟指定的記錄檔。</span><span class="sxs-lookup"><span data-stu-id="6f5a1-130">Unable to open the specified log file.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="6f5a1-131"><dt>**\_ \_ \_ 找不到 PDH 檔案**</dt></span><span class="sxs-lookup"><span data-stu-id="6f5a1-131"><dt>**PDH\_FILE\_NOT\_FOUND**</dt></span></span> </dl>       | <span data-ttu-id="6f5a1-132">找不到指定的檔案。</span><span class="sxs-lookup"><span data-stu-id="6f5a1-132">Unable to find the specified file.</span></span><br/>                                                          |



 

## <a name="requirements"></a><span data-ttu-id="6f5a1-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="6f5a1-133">Requirements</span></span>



| <span data-ttu-id="6f5a1-134">需求</span><span class="sxs-lookup"><span data-stu-id="6f5a1-134">Requirement</span></span> | <span data-ttu-id="6f5a1-135">值</span><span class="sxs-lookup"><span data-stu-id="6f5a1-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6f5a1-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6f5a1-136">Minimum supported client</span></span><br/> | <span data-ttu-id="6f5a1-137">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6f5a1-137">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6f5a1-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6f5a1-138">Minimum supported server</span></span><br/> | <span data-ttu-id="6f5a1-139">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6f5a1-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6f5a1-140">程式庫</span><span class="sxs-lookup"><span data-stu-id="6f5a1-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="6f5a1-141"><dt>Pdh. .lib</dt></span><span class="sxs-lookup"><span data-stu-id="6f5a1-141"><dt>Pdh.lib</dt></span></span> </dl> |
| <span data-ttu-id="6f5a1-142">DLL</span><span class="sxs-lookup"><span data-stu-id="6f5a1-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f5a1-143"><dt>Pdh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f5a1-143"><dt>Pdh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f5a1-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6f5a1-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f5a1-145">**PdhGetLogFileSize**</span><span class="sxs-lookup"><span data-stu-id="6f5a1-145">**PdhGetLogFileSize**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhgetlogfilesize)
</dt> <dt>

[<span data-ttu-id="6f5a1-146">**PdhVbOpenLog**</span><span class="sxs-lookup"><span data-stu-id="6f5a1-146">**PdhVbOpenLog**</span></span>](pdhvbopenlog.md)
</dt> <dt>

[<span data-ttu-id="6f5a1-147">**PdhVbUpdateLog**</span><span class="sxs-lookup"><span data-stu-id="6f5a1-147">**PdhVbUpdateLog**</span></span>](pdhvbupdatelog.md)
</dt> </dl>

 

