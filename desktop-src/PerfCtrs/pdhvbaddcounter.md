---
description: PdhVbAddCounter 函式會在指定的查詢物件中建立計數器專案，並在成功完成時傳回該計數器的控制碼。
ms.assetid: 20a9e6cd-bf0d-497d-b660-88e786e2f004
title: PdhVbAddCounter 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbAddCounter
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 19f97abeec74af0d08f340b70aa139e1bec7bf1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983495"
---
# <a name="pdhvbaddcounter-function"></a><span data-ttu-id="be52b-103">PdhVbAddCounter 函式</span><span class="sxs-lookup"><span data-stu-id="be52b-103">PdhVbAddCounter function</span></span>

<span data-ttu-id="be52b-104">**PdhVbAddCounter** 函式會在指定的查詢物件中建立計數器專案，並在成功完成時傳回該計數器的控制碼。</span><span class="sxs-lookup"><span data-stu-id="be52b-104">The **PdhVbAddCounter** function creates a counter entry in the specified query object, and returns a handle to that counter upon successful completion.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="be52b-105">本主題所描述的功能可能會在未來變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="be52b-105">The function that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="be52b-106">相反地，Microsoft 建議您使用 [效能計數器](performance-counters-functions.md)函式中所述的功能。</span><span class="sxs-lookup"><span data-stu-id="be52b-106">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="be52b-107">函數 PdhVbAddCounter ( \_ Byval QueryHandle long，Byval \_ CounterPath as String，long \_ \_ ) long</span><span class="sxs-lookup"><span data-stu-id="be52b-107">Function PdhVbAddCounter( \_ ByVal QueryHandle As Long, \_ ByVal CounterPath As String, \_ ByVal CounterHandle As Long \_ ) As Long</span></span>

## <a name="parameters"></a><span data-ttu-id="be52b-108">參數</span><span class="sxs-lookup"><span data-stu-id="be52b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be52b-109">*QueryHandle*</span><span class="sxs-lookup"><span data-stu-id="be52b-109">*QueryHandle*</span></span> 
</dt> <dd>

<span data-ttu-id="be52b-110">要指派此計數器的查詢識別碼。</span><span class="sxs-lookup"><span data-stu-id="be52b-110">ID of the query to which this counter is to be assigned.</span></span> <span data-ttu-id="be52b-111">[**PdhVbOpenQuery**](pdhvbopenquery.md)函數會傳回這個值。</span><span class="sxs-lookup"><span data-stu-id="be52b-111">This value is returned by the [**PdhVbOpenQuery**](pdhvbopenquery.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="be52b-112">*CounterPath*</span><span class="sxs-lookup"><span data-stu-id="be52b-112">*CounterPath*</span></span> 
</dt> <dd>

<span data-ttu-id="be52b-113">文字字串，指定要加入至查詢的計數器路徑名稱。</span><span class="sxs-lookup"><span data-stu-id="be52b-113">Text string that specifies the name of the counter path to add to the query.</span></span> <span data-ttu-id="be52b-114">此字串的內容必須是有效的計數器路徑，如同從計數器瀏覽器或其他來源取得。</span><span class="sxs-lookup"><span data-stu-id="be52b-114">The contents of this string must be a valid counter path, as obtained from the counter browser or other source.</span></span>

</dd> <dt>

<span data-ttu-id="be52b-115">*CounterHandle*</span><span class="sxs-lookup"><span data-stu-id="be52b-115">*CounterHandle*</span></span> 
</dt> <dd>

<span data-ttu-id="be52b-116">在查詢中識別此計數器的唯一參考。</span><span class="sxs-lookup"><span data-stu-id="be52b-116">Unique reference that identifies this counter in the query.</span></span> <span data-ttu-id="be52b-117">在呼叫函式之前，此變數必須初始化為零。</span><span class="sxs-lookup"><span data-stu-id="be52b-117">This variable must be initialized to zero before the function is called.</span></span> <span data-ttu-id="be52b-118">只有當函式成功完成時，才會在傳回時包含有效的值。</span><span class="sxs-lookup"><span data-stu-id="be52b-118">It contains a valid value on return only if the function completes successfully.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be52b-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="be52b-119">Return value</span></span>

<span data-ttu-id="be52b-120">如果函式成功，它會傳回等於 ERROR SUCCESS 的 **長** 整數 \_ ，以及 *CounterHandle* 變數中的新控制碼。</span><span class="sxs-lookup"><span data-stu-id="be52b-120">If the function succeeds, it returns a **Long** integer equal to ERROR\_SUCCESS and a new handle in the *CounterHandle* variable.</span></span>

<span data-ttu-id="be52b-121">如果函式失敗，則傳回值為 [系統錯誤碼](/windows/desktop/Debug/system-error-codes) 或 [PDH 錯誤碼](pdh-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="be52b-121">If the function fails, the return value is a [system error code](/windows/desktop/Debug/system-error-codes) or a [PDH error code](pdh-error-codes.md).</span></span> <span data-ttu-id="be52b-122">以下是可能的值。</span><span class="sxs-lookup"><span data-stu-id="be52b-122">The following are possible values.</span></span>



| <span data-ttu-id="be52b-123">傳回碼</span><span class="sxs-lookup"><span data-stu-id="be52b-123">Return code</span></span>                                                                                                     | <span data-ttu-id="be52b-124">Description</span><span class="sxs-lookup"><span data-stu-id="be52b-124">Description</span></span>                                                                   |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="be52b-125"><dt>**PDH \_ 不正確 \_ 引數**</dt></span><span class="sxs-lookup"><span data-stu-id="be52b-125"><dt>**PDH\_INVALID\_ARGUMENT**</dt></span></span> </dl>           | <span data-ttu-id="be52b-126">一或多個引數無效或不正確。</span><span class="sxs-lookup"><span data-stu-id="be52b-126">One or more of the arguments is invalid or incorrect.</span></span><br/>              |
| <dl> <span data-ttu-id="be52b-127"><dt>**PDH \_ 記憶體 \_ 配置 \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="be52b-127"><dt>**PDH\_MEMORY\_ALLOCATION\_FAILURE**</dt></span></span> </dl> | <span data-ttu-id="be52b-128">無法配置記憶體緩衝區。</span><span class="sxs-lookup"><span data-stu-id="be52b-128">A memory buffer could not be allocated.</span></span><br/>                            |
| <dl> <span data-ttu-id="be52b-129"><dt>**PDH \_ 不正確 \_ 控制碼**</dt></span><span class="sxs-lookup"><span data-stu-id="be52b-129"><dt>**PDH\_INVALID\_HANDLE**</dt></span></span> </dl>             | <span data-ttu-id="be52b-130">查詢控制碼無效。</span><span class="sxs-lookup"><span data-stu-id="be52b-130">The query handle is not valid.</span></span><br/>                                     |
| <dl> <span data-ttu-id="be52b-131"><dt>**PDH \_ CSTATUS \_ 沒有 \_ 計數器**</dt></span><span class="sxs-lookup"><span data-stu-id="be52b-131"><dt>**PDH\_CSTATUS\_NO\_COUNTER**</dt></span></span> </dl>        | <span data-ttu-id="be52b-132">找不到指定的計數器。</span><span class="sxs-lookup"><span data-stu-id="be52b-132">The specified counter was not found.</span></span><br/>                               |
| <dl> <span data-ttu-id="be52b-133"><dt>**PDH \_ CSTATUS \_ 沒有 \_ 物件**</dt></span><span class="sxs-lookup"><span data-stu-id="be52b-133"><dt>**PDH\_CSTATUS\_NO\_OBJECT**</dt></span></span> </dl>         | <span data-ttu-id="be52b-134">找不到指定的物件。</span><span class="sxs-lookup"><span data-stu-id="be52b-134">The specified object could not be found.</span></span><br/>                           |
| <dl> <span data-ttu-id="be52b-135"><dt>**PDH \_ CSTATUS \_ 沒有 \_ 電腦**</dt></span><span class="sxs-lookup"><span data-stu-id="be52b-135"><dt>**PDH\_CSTATUS\_NO\_MACHINE**</dt></span></span> </dl>        | <span data-ttu-id="be52b-136">無法建立電腦專案。</span><span class="sxs-lookup"><span data-stu-id="be52b-136">A computer entry could not be created.</span></span><br/>                             |
| <dl> <span data-ttu-id="be52b-137"><dt>**PDH \_ CSTATUS \_ 不良 \_ COUNTERNAME**</dt></span><span class="sxs-lookup"><span data-stu-id="be52b-137"><dt>**PDH\_CSTATUS\_BAD\_COUNTERNAME**</dt></span></span> </dl>   | <span data-ttu-id="be52b-138">傳入了空的計數器名稱路徑字串。</span><span class="sxs-lookup"><span data-stu-id="be52b-138">An empty counter name path string was passed in.</span></span><br/>                   |
| <dl> <span data-ttu-id="be52b-139"><dt>**\_ \_ 找不到 PDH 函數 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="be52b-139"><dt>**PDH\_FUNCTION\_NOT\_FOUND**</dt></span></span> </dl>        | <span data-ttu-id="be52b-140">無法判斷此計數器的計算函數。</span><span class="sxs-lookup"><span data-stu-id="be52b-140">The calculation function for this counter could not be determined.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="be52b-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="be52b-141">Requirements</span></span>



| <span data-ttu-id="be52b-142">需求</span><span class="sxs-lookup"><span data-stu-id="be52b-142">Requirement</span></span> | <span data-ttu-id="be52b-143">值</span><span class="sxs-lookup"><span data-stu-id="be52b-143">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="be52b-144">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="be52b-144">Minimum supported client</span></span><br/> | <span data-ttu-id="be52b-145">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="be52b-145">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="be52b-146">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="be52b-146">Minimum supported server</span></span><br/> | <span data-ttu-id="be52b-147">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="be52b-147">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="be52b-148">程式庫</span><span class="sxs-lookup"><span data-stu-id="be52b-148">Library</span></span><br/>                  | <dl> <span data-ttu-id="be52b-149"><dt>Pdh. .lib</dt></span><span class="sxs-lookup"><span data-stu-id="be52b-149"><dt>Pdh.lib</dt></span></span> </dl> |
| <span data-ttu-id="be52b-150">DLL</span><span class="sxs-lookup"><span data-stu-id="be52b-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be52b-151"><dt>Pdh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be52b-151"><dt>Pdh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be52b-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="be52b-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be52b-153">**PdhVbOpenQuery**</span><span class="sxs-lookup"><span data-stu-id="be52b-153">**PdhVbOpenQuery**</span></span>](pdhvbopenquery.md)
</dt> </dl>

 

