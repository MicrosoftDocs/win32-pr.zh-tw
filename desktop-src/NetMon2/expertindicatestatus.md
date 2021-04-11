---
description: ExpertIndicateStatus 函式會指出完成捕獲檔案的專家分析完成百分比。
ms.assetid: 6dbaa6d3-6068-4a28-9d9f-bcc7a25da407
title: 'ExpertIndicateStatus 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertIndicateStatus
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: ac707a774b667b96a4d612e9eaf7da2c779c0327
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112240"
---
# <a name="expertindicatestatus-function"></a><span data-ttu-id="e999e-103">ExpertIndicateStatus 函式</span><span class="sxs-lookup"><span data-stu-id="e999e-103">ExpertIndicateStatus function</span></span>

<span data-ttu-id="e999e-104">**ExpertIndicateStatus** 函式會指出專家的 capture 分析完成百分比。</span><span class="sxs-lookup"><span data-stu-id="e999e-104">The **ExpertIndicateStatus** function indicates the percentage of completion of the expert's analysis of the capture file.</span></span>

## <a name="syntax"></a><span data-ttu-id="e999e-105">語法</span><span class="sxs-lookup"><span data-stu-id="e999e-105">Syntax</span></span>


```C++
DWORD WINAPI ExpertIndicateStatus(
  _In_  HEXPERTKEY              hExpertKey,
  _In_  EXPERTSTATUSENUMERATION Status,
  _In_  DWORD                   SubStatus,
  _In_  char                    *sztext,
  _Out_ long                    PercentDone
);
```



## <a name="parameters"></a><span data-ttu-id="e999e-106">參數</span><span class="sxs-lookup"><span data-stu-id="e999e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e999e-107">*hExpertKey* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e999e-107">*hExpertKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e999e-108">獨特的專家識別碼。</span><span class="sxs-lookup"><span data-stu-id="e999e-108">Unique expert identifier.</span></span> <span data-ttu-id="e999e-109">網路監視器在呼叫 [Run](run.md)函式時，將 *hExpertKey* 傳遞給專家。</span><span class="sxs-lookup"><span data-stu-id="e999e-109">Network Monitor passes *hExpertKey* to the expert when it calls the [Run](run.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="e999e-110">*狀態* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e999e-110">*Status* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e999e-111">分析目前的狀態。</span><span class="sxs-lookup"><span data-stu-id="e999e-111">Current status of the analysis.</span></span> <span data-ttu-id="e999e-112">指定下列其中一個 [EXPERTSTATUSENUMERATION](expertstatusenumeration.md) 值。</span><span class="sxs-lookup"><span data-stu-id="e999e-112">Specify one of the following [EXPERTSTATUSENUMERATION](expertstatusenumeration.md) values.</span></span>



| <span data-ttu-id="e999e-113">值</span><span class="sxs-lookup"><span data-stu-id="e999e-113">Value</span></span>                                                                                                                                                                                 | <span data-ttu-id="e999e-114">意義</span><span class="sxs-lookup"><span data-stu-id="e999e-114">Meaning</span></span>                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <span id="EXPERTSTATUS_INACTIVE"></span><span id="expertstatus_inactive"></span><dl> <span data-ttu-id="e999e-115"><dt>**EXPERTSTATUS \_ 非使用中**</dt></span><span class="sxs-lookup"><span data-stu-id="e999e-115"><dt>**EXPERTSTATUS\_INACTIVE**</dt></span></span> </dl> | <span data-ttu-id="e999e-116">專家從未開始。</span><span class="sxs-lookup"><span data-stu-id="e999e-116">The expert never started.</span></span> <br/>                                          |
| <span id="EXPERTSTATUS_STARTING"></span><span id="expertstatus_starting"></span><dl> <span data-ttu-id="e999e-117"><dt>**EXPERTSTATUS \_ 開始**</dt></span><span class="sxs-lookup"><span data-stu-id="e999e-117"><dt>**EXPERTSTATUS\_STARTING**</dt></span></span> </dl> | <span data-ttu-id="e999e-118">專家即將開始。</span><span class="sxs-lookup"><span data-stu-id="e999e-118">The expert is starting.</span></span> <br/>                                            |
| <span id="EXPERTSTATUS_RUNNING"></span><span id="expertstatus_running"></span><dl> <span data-ttu-id="e999e-119"><dt>**EXPERTSTATUS \_ 正在執行**</dt></span><span class="sxs-lookup"><span data-stu-id="e999e-119"><dt>**EXPERTSTATUS\_RUNNING**</dt></span></span> </dl>    | <span data-ttu-id="e999e-120">專家正在正常執行。</span><span class="sxs-lookup"><span data-stu-id="e999e-120">The expert is running normally.</span></span> <br/>                                    |
| <span id="EXPERTSTATUS_PROBLEM"></span><span id="expertstatus_problem"></span><dl> <span data-ttu-id="e999e-121"><dt>**EXPERTSTATUS \_ 問題**</dt></span><span class="sxs-lookup"><span data-stu-id="e999e-121"><dt>**EXPERTSTATUS\_PROBLEM**</dt></span></span> </dl>    | <span data-ttu-id="e999e-122">子狀態參數中指定的問題已停止專家。</span><span class="sxs-lookup"><span data-stu-id="e999e-122">A problem specified in the SubStatus parameter stopped the expert.</span></span> <br/> |
| <span id="EXPERTSTATUS_ABORTED"></span><span id="expertstatus_aborted"></span><dl> <span data-ttu-id="e999e-123"><dt>**EXPERTSTATUS 已 \_ 中止**</dt></span><span class="sxs-lookup"><span data-stu-id="e999e-123"><dt>**EXPERTSTATUS\_ABORTED**</dt></span></span> </dl>    | <span data-ttu-id="e999e-124">網路監視器已停止專家。</span><span class="sxs-lookup"><span data-stu-id="e999e-124">Network Monitor stopped the expert.</span></span> <br/>                                |
| <span id="EXPERTSTATUS_DONE"></span><span id="expertstatus_done"></span><dl> <span data-ttu-id="e999e-125"><dt>**EXPERTSTATUS \_ 完成**</dt></span><span class="sxs-lookup"><span data-stu-id="e999e-125"><dt>**EXPERTSTATUS\_DONE**</dt></span></span> </dl>             | <span data-ttu-id="e999e-126">專家已成功完成分析。</span><span class="sxs-lookup"><span data-stu-id="e999e-126">The expert finished the analysis successfully.</span></span> <br/>                     |



 

</dd> <dt>

<span data-ttu-id="e999e-127">子 *狀態* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e999e-127">*SubStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e999e-128">*狀態* 參數所提供之資訊的延伸或澄清。</span><span class="sxs-lookup"><span data-stu-id="e999e-128">Extension or clarification of information provided by the *Status* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="e999e-129">*sztext* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e999e-129">*sztext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e999e-130">選擇性的文字狀態指標。</span><span class="sxs-lookup"><span data-stu-id="e999e-130">Optional text status indicator.</span></span>

<span data-ttu-id="e999e-131">此參數值可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="e999e-131">This parameter value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e999e-132">*PercentDone* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e999e-132">*PercentDone* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e999e-133">專家已處理的捕獲資料百分比。</span><span class="sxs-lookup"><span data-stu-id="e999e-133">Percentage of the capture data that the expert has processed.</span></span>

<span data-ttu-id="e999e-134">當專家成功完成捕獲檔案的分析時，系統會將百分比設定為100。</span><span class="sxs-lookup"><span data-stu-id="e999e-134">When the expert successfully completes analysis of a capture file, the system sets the percentage to 100.</span></span> <span data-ttu-id="e999e-135">將會忽略大於99的任何數位。</span><span class="sxs-lookup"><span data-stu-id="e999e-135">Any number greater than 99 will be ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e999e-136">傳回值</span><span class="sxs-lookup"><span data-stu-id="e999e-136">Return value</span></span>

<span data-ttu-id="e999e-137">如果函式成功，則傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="e999e-137">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="e999e-138">如果函式不成功，則傳回值為 NMERR \_ 專家 \_ 終止; 專家必須立即清除並返回，而不需要完成 capture。</span><span class="sxs-lookup"><span data-stu-id="e999e-138">If the function is unsuccessful, the return value is NMERR\_EXPERT\_TERMINATE; the expert must immediately clean up and return without completing the capture.</span></span>

## <a name="remarks"></a><span data-ttu-id="e999e-139">備註</span><span class="sxs-lookup"><span data-stu-id="e999e-139">Remarks</span></span>

<span data-ttu-id="e999e-140">**ExpertIndicateStatus** 函式只能由執行 [執行](run.md)或 [設定](configure.md)匯出函數的專家呼叫。</span><span class="sxs-lookup"><span data-stu-id="e999e-140">The **ExpertIndicateStatus** function can only be called by experts that implement the [Run](run.md) or [Configure](configure.md) export function.</span></span>

## <a name="requirements"></a><span data-ttu-id="e999e-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="e999e-141">Requirements</span></span>



| <span data-ttu-id="e999e-142">需求</span><span class="sxs-lookup"><span data-stu-id="e999e-142">Requirement</span></span> | <span data-ttu-id="e999e-143">值</span><span class="sxs-lookup"><span data-stu-id="e999e-143">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e999e-144">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e999e-144">Minimum supported client</span></span><br/> | <span data-ttu-id="e999e-145">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e999e-145">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="e999e-146">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e999e-146">Minimum supported server</span></span><br/> | <span data-ttu-id="e999e-147">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e999e-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e999e-148">標頭</span><span class="sxs-lookup"><span data-stu-id="e999e-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="e999e-149"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="e999e-149"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="e999e-150">程式庫</span><span class="sxs-lookup"><span data-stu-id="e999e-150">Library</span></span><br/>                  | <dl> <span data-ttu-id="e999e-151"><dt>Nmapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e999e-151"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="e999e-152">DLL</span><span class="sxs-lookup"><span data-stu-id="e999e-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e999e-153"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e999e-153"><dt>Nmapi.dll</dt></span></span> </dl> |
