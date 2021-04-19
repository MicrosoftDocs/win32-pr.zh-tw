---
description: PdhVbUpdateLog 函數函數會更新目前的查詢，並將新的資料寫入記錄檔。 此函數會呼叫 PdhUpdateLog。
ms.assetid: a7a3ad18-2d61-448e-9764-ba363398e804
title: PdhVbUpdateLog 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbUpdateLog
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: c02e533f57481004b0a7de9f779399b20bddc0af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974450"
---
# <a name="pdhvbupdatelog-function"></a><span data-ttu-id="34f69-104">PdhVbUpdateLog 函式</span><span class="sxs-lookup"><span data-stu-id="34f69-104">PdhVbUpdateLog function</span></span>

<span data-ttu-id="34f69-105">**PdhVbUpdateLog** 函數函數會更新目前的查詢，並將新的資料寫入記錄檔。</span><span class="sxs-lookup"><span data-stu-id="34f69-105">The **PdhVbUpdateLog** function function updates the current query and writes new data to the log file.</span></span> <span data-ttu-id="34f69-106">此函數會呼叫 [**PdhUpdateLog**](/windows/desktop/api/Pdh/nf-pdh-pdhupdateloga)。</span><span class="sxs-lookup"><span data-stu-id="34f69-106">This function calls [**PdhUpdateLog**](/windows/desktop/api/Pdh/nf-pdh-pdhupdateloga).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="34f69-107">本主題所描述的功能可能會在未來變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="34f69-107">The function that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="34f69-108">相反地，Microsoft 建議您使用 [效能計數器](performance-counters-functions.md)函式中所述的功能。</span><span class="sxs-lookup"><span data-stu-id="34f69-108">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="34f69-109">Function PdhVbUpdateLog ( \_ Byval HLog 作為 PDH \_ hLog， \_ BYVAL szUserString as LPCTSTR \_ ) </span><span class="sxs-lookup"><span data-stu-id="34f69-109">Function PdhVbUpdateLog( \_ ByVal hLog As PDH\_HLOG, \_ ByVal szUserString As LPCTSTR \_ )</span></span>

## <a name="parameters"></a><span data-ttu-id="34f69-110">參數</span><span class="sxs-lookup"><span data-stu-id="34f69-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34f69-111">*hLog* \[在\]</span><span class="sxs-lookup"><span data-stu-id="34f69-111">*hLog* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34f69-112">要更新之記錄檔的控制碼。</span><span class="sxs-lookup"><span data-stu-id="34f69-112">Handle to the log file to be updated.</span></span> <span data-ttu-id="34f69-113">[**PdhVbOpenLog**](pdhvbopenlog.md)函數會傳回這個控制碼。</span><span class="sxs-lookup"><span data-stu-id="34f69-113">This handle is returned by the [**PdhVbOpenLog**](pdhvbopenlog.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="34f69-114">*szUserString* \[在\]</span><span class="sxs-lookup"><span data-stu-id="34f69-114">*szUserString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34f69-115">字串的指標，指定要加入至記錄檔的資料。</span><span class="sxs-lookup"><span data-stu-id="34f69-115">Pointer to a string that specifies the data to be added to the log file.</span></span> <span data-ttu-id="34f69-116">這通常用於記錄檔中的批註。</span><span class="sxs-lookup"><span data-stu-id="34f69-116">This is generally used for comments within the log file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34f69-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="34f69-117">Return value</span></span>

<span data-ttu-id="34f69-118">如果函數成功，它會傳回0。</span><span class="sxs-lookup"><span data-stu-id="34f69-118">If the function succeeds, it returns 0.</span></span>

<span data-ttu-id="34f69-119">如果函式失敗，則傳回值為 [系統錯誤碼](/windows/desktop/Debug/system-error-codes) 或 [PDH 錯誤碼](pdh-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="34f69-119">If the function fails, the return value is a [system error code](/windows/desktop/Debug/system-error-codes) or a [PDH error code](pdh-error-codes.md).</span></span> <span data-ttu-id="34f69-120">以下是可能的值。</span><span class="sxs-lookup"><span data-stu-id="34f69-120">The following are possible values.</span></span>



| <span data-ttu-id="34f69-121">傳回碼</span><span class="sxs-lookup"><span data-stu-id="34f69-121">Return code</span></span>                                                                                                | <span data-ttu-id="34f69-122">Description</span><span class="sxs-lookup"><span data-stu-id="34f69-122">Description</span></span>                                                                                            |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="34f69-123"><dt>**PDH \_ \_ 緩衝區不足**</dt></span><span class="sxs-lookup"><span data-stu-id="34f69-123"><dt>**PDH\_INSUFFICIENT\_BUFFER**</dt></span></span> </dl>   | <span data-ttu-id="34f69-124">要求的資料大於提供的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="34f69-124">The requested data is larger than the buffer supplied.</span></span> <span data-ttu-id="34f69-125">無法傳回要求的資料。</span><span class="sxs-lookup"><span data-stu-id="34f69-125">Unable to return the requested data.</span></span><br/> |
| <dl> <span data-ttu-id="34f69-126"><dt>**PDH \_ 不正確 \_ 引數**</dt></span><span class="sxs-lookup"><span data-stu-id="34f69-126"><dt>**PDH\_INVALID\_ARGUMENT**</dt></span></span> </dl>      | <span data-ttu-id="34f69-127">一或多個字串緩衝區的大小不正確。</span><span class="sxs-lookup"><span data-stu-id="34f69-127">One or more of the string buffers is not the correct size.</span></span><br/>                                  |
| <dl> <span data-ttu-id="34f69-128"><dt>**PDH \_ 不正確 \_ 控制碼**</dt></span><span class="sxs-lookup"><span data-stu-id="34f69-128"><dt>**PDH\_INVALID\_HANDLE**</dt></span></span> </dl>        | <span data-ttu-id="34f69-129">控制碼不是有效的 PDH 物件。</span><span class="sxs-lookup"><span data-stu-id="34f69-129">The handle is not a valid PDH object.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="34f69-130"><dt>**PDH \_ 記錄 \_ 檔 \_ 開啟 \_ 錯誤**</dt></span><span class="sxs-lookup"><span data-stu-id="34f69-130"><dt>**PDH\_LOG\_FILE\_OPEN\_ERROR**</dt></span></span> </dl> | <span data-ttu-id="34f69-131">無法開啟指定的記錄檔。</span><span class="sxs-lookup"><span data-stu-id="34f69-131">Unable to open the specified log file.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="34f69-132"><dt>**\_ \_ \_ 找不到 PDH 檔案**</dt></span><span class="sxs-lookup"><span data-stu-id="34f69-132"><dt>**PDH\_FILE\_NOT\_FOUND**</dt></span></span> </dl>       | <span data-ttu-id="34f69-133">找不到指定的檔案。</span><span class="sxs-lookup"><span data-stu-id="34f69-133">Unable to find the specified file.</span></span><br/>                                                          |



 

## <a name="remarks"></a><span data-ttu-id="34f69-134">備註</span><span class="sxs-lookup"><span data-stu-id="34f69-134">Remarks</span></span>

<span data-ttu-id="34f69-135">必須有目前開啟的查詢，而且必須在呼叫此函式之前，將所需的計數器加入至該查詢。</span><span class="sxs-lookup"><span data-stu-id="34f69-135">There must be a currently opened query, and the desired counters must be added to it before this function is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="34f69-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="34f69-136">Requirements</span></span>



| <span data-ttu-id="34f69-137">需求</span><span class="sxs-lookup"><span data-stu-id="34f69-137">Requirement</span></span> | <span data-ttu-id="34f69-138">值</span><span class="sxs-lookup"><span data-stu-id="34f69-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="34f69-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="34f69-139">Minimum supported client</span></span><br/> | <span data-ttu-id="34f69-140">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="34f69-140">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="34f69-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="34f69-141">Minimum supported server</span></span><br/> | <span data-ttu-id="34f69-142">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="34f69-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="34f69-143">程式庫</span><span class="sxs-lookup"><span data-stu-id="34f69-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="34f69-144"><dt>Pdh. .lib</dt></span><span class="sxs-lookup"><span data-stu-id="34f69-144"><dt>Pdh.lib</dt></span></span> </dl> |
| <span data-ttu-id="34f69-145">DLL</span><span class="sxs-lookup"><span data-stu-id="34f69-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="34f69-146"><dt>Pdh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="34f69-146"><dt>Pdh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34f69-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="34f69-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34f69-148">**PdhUpdateLog**</span><span class="sxs-lookup"><span data-stu-id="34f69-148">**PdhUpdateLog**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhupdateloga)
</dt> <dt>

[<span data-ttu-id="34f69-149">**PdhVbGetLogFileSize**</span><span class="sxs-lookup"><span data-stu-id="34f69-149">**PdhVbGetLogFileSize**</span></span>](pdhvbgetlogfilesize.md)
</dt> <dt>

[<span data-ttu-id="34f69-150">**PdhVbOpenLog**</span><span class="sxs-lookup"><span data-stu-id="34f69-150">**PdhVbOpenLog**</span></span>](pdhvbopenlog.md)
</dt> </dl>

 

