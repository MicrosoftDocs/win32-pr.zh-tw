---
description: PdhVbGetCounterPathElements 函式會將完整的效能計數器路徑字串剖析成其個別元素。
ms.assetid: 5459c7dd-e8b6-48cd-a33f-cafdc64dd9ee
title: PdhVbGetCounterPathElements 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbGetCounterPathElements
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 003374141b0454d730ba4b844715bd6f00b544da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106976898"
---
# <a name="pdhvbgetcounterpathelements-function"></a><span data-ttu-id="5b524-103">PdhVbGetCounterPathElements 函式</span><span class="sxs-lookup"><span data-stu-id="5b524-103">PdhVbGetCounterPathElements function</span></span>

<span data-ttu-id="5b524-104">**PdhVbGetCounterPathElements** 函式會將完整的效能計數器路徑字串剖析成其個別元素。</span><span class="sxs-lookup"><span data-stu-id="5b524-104">The **PdhVbGetCounterPathElements** function parses a fully qualified performance counter path string into its individual elements.</span></span> <span data-ttu-id="5b524-105">在此函式中使用字串變數時，每個字串變數的大小必須相同 (*BufferSize*) 和已進行維度和初始化。</span><span class="sxs-lookup"><span data-stu-id="5b524-105">Each of the string variables must be the same size (*BufferSize*) and dimensioned and initialized before it is used in this function.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5b524-106">本主題所描述的功能可能會在未來變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="5b524-106">The function that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="5b524-107">相反地，Microsoft 建議您使用 [效能計數器](performance-counters-functions.md)函式中所述的功能。</span><span class="sxs-lookup"><span data-stu-id="5b524-107">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="5b524-108">函數 PdhVbGetCounterPathElements ( \_ Byval PathString As string， \_ Byval MachineName as string，byval ObjectName as string，byval InstanceName as string，Byval ParentInstance as string，Byval \_ \_ \_ \_ CounterName as \_ \_ string，byval 的 long ) </span><span class="sxs-lookup"><span data-stu-id="5b524-108">Function PdhVbGetCounterPathElements( \_ ByVal PathString As String, \_ ByVal MachineName As String, \_ ByVal ObjectName As String, \_ ByVal InstanceName As String, \_ ByVal ParentInstance As String, \_ ByVal CounterName As String, \_ ByVal BufferSize As Long \_ ) As Long</span></span>

## <a name="parameters"></a><span data-ttu-id="5b524-109">參數</span><span class="sxs-lookup"><span data-stu-id="5b524-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b524-110">*PathString*</span><span class="sxs-lookup"><span data-stu-id="5b524-110">*PathString*</span></span> 
</dt> <dd>

<span data-ttu-id="5b524-111">要分解成其個別元素的計數器路徑字串。</span><span class="sxs-lookup"><span data-stu-id="5b524-111">Counter path string that is to be broken up into its individual elements.</span></span>

</dd> <dt>

<span data-ttu-id="5b524-112">*MachineName*</span><span class="sxs-lookup"><span data-stu-id="5b524-112">*MachineName*</span></span> 
</dt> <dd>

<span data-ttu-id="5b524-113">要接收電腦名稱稱的字串。</span><span class="sxs-lookup"><span data-stu-id="5b524-113">String to receive the computer name.</span></span>

</dd> <dt>

<span data-ttu-id="5b524-114">*ObjectName*</span><span class="sxs-lookup"><span data-stu-id="5b524-114">*ObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="5b524-115">要接收物件名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="5b524-115">String to receive the object name.</span></span>

</dd> <dt>

<span data-ttu-id="5b524-116">*InstanceName*</span><span class="sxs-lookup"><span data-stu-id="5b524-116">*InstanceName*</span></span> 
</dt> <dd>

<span data-ttu-id="5b524-117">要接收實例名稱的字串（如果使用的話）。</span><span class="sxs-lookup"><span data-stu-id="5b524-117">String to receive the instance name, if used.</span></span>

</dd> <dt>

<span data-ttu-id="5b524-118">*ParentInstance*</span><span class="sxs-lookup"><span data-stu-id="5b524-118">*ParentInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="5b524-119">要接收父實例的字串（如果使用的話）。</span><span class="sxs-lookup"><span data-stu-id="5b524-119">String to receive the parent instance, if used.</span></span>

</dd> <dt>

<span data-ttu-id="5b524-120">*CounterName*</span><span class="sxs-lookup"><span data-stu-id="5b524-120">*CounterName*</span></span> 
</dt> <dd>

<span data-ttu-id="5b524-121">要接收計數器名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="5b524-121">String to receive the counter name.</span></span>

</dd> <dt>

<span data-ttu-id="5b524-122">*BufferSize*</span><span class="sxs-lookup"><span data-stu-id="5b524-122">*BufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="5b524-123">當做此函式呼叫之參數使用的每個字串變數大小上限。</span><span class="sxs-lookup"><span data-stu-id="5b524-123">Maximum size of each string variable used as a parameter to this function call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b524-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="5b524-124">Return value</span></span>

<span data-ttu-id="5b524-125">如果函式成功，它會傳回相當於 ERROR SUCCESS 的 **長** 整數 \_ 。</span><span class="sxs-lookup"><span data-stu-id="5b524-125">If the function succeeds, it returns a **Long** integer equal to ERROR\_SUCCESS.</span></span>

<span data-ttu-id="5b524-126">如果函式失敗，則傳回值為 [系統錯誤碼](/windows/desktop/Debug/system-error-codes) 或 [PDH 錯誤碼](pdh-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="5b524-126">If the function fails, the return value is a [system error code](/windows/desktop/Debug/system-error-codes) or a [PDH error code](pdh-error-codes.md).</span></span> <span data-ttu-id="5b524-127">以下是可能的值。</span><span class="sxs-lookup"><span data-stu-id="5b524-127">The following are possible values.</span></span>



| <span data-ttu-id="5b524-128">傳回碼</span><span class="sxs-lookup"><span data-stu-id="5b524-128">Return code</span></span>                                                                                                     | <span data-ttu-id="5b524-129">Description</span><span class="sxs-lookup"><span data-stu-id="5b524-129">Description</span></span>                                                                                    |
|-----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5b524-130"><dt>**PDH \_ 不正確 \_ 引數**</dt></span><span class="sxs-lookup"><span data-stu-id="5b524-130"><dt>**PDH\_INVALID\_ARGUMENT**</dt></span></span> </dl>           | <span data-ttu-id="5b524-131">一或多個字串緩衝區的大小不正確。</span><span class="sxs-lookup"><span data-stu-id="5b524-131">One or more of the string buffers is not the correct size.</span></span><br/>                          |
| <dl> <span data-ttu-id="5b524-132"><dt>**PDH \_ 更多 \_ 資料**</dt></span><span class="sxs-lookup"><span data-stu-id="5b524-132"><dt>**PDH\_MORE\_DATA**</dt></span></span> </dl>                  | <span data-ttu-id="5b524-133">一或多個計數器路徑元素對傳回緩衝區長度而言太大。</span><span class="sxs-lookup"><span data-stu-id="5b524-133">One or more of the counter path elements is too large for the return buffer length.</span></span><br/> |
| <dl> <span data-ttu-id="5b524-134"><dt>**PDH \_ 記憶體 \_ 配置 \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="5b524-134"><dt>**PDH\_MEMORY\_ALLOCATION\_FAILURE**</dt></span></span> </dl> | <span data-ttu-id="5b524-135">無法配置暫存記憶體緩衝區。</span><span class="sxs-lookup"><span data-stu-id="5b524-135">A temporary memory buffer could not be allocated.</span></span><br/>                                   |



 

## <a name="requirements"></a><span data-ttu-id="5b524-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="5b524-136">Requirements</span></span>



| <span data-ttu-id="5b524-137">需求</span><span class="sxs-lookup"><span data-stu-id="5b524-137">Requirement</span></span> | <span data-ttu-id="5b524-138">值</span><span class="sxs-lookup"><span data-stu-id="5b524-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5b524-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5b524-139">Minimum supported client</span></span><br/> | <span data-ttu-id="5b524-140">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5b524-140">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5b524-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5b524-141">Minimum supported server</span></span><br/> | <span data-ttu-id="5b524-142">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5b524-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5b524-143">程式庫</span><span class="sxs-lookup"><span data-stu-id="5b524-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="5b524-144"><dt>Pdh. .lib</dt></span><span class="sxs-lookup"><span data-stu-id="5b524-144"><dt>Pdh.lib</dt></span></span> </dl> |
| <span data-ttu-id="5b524-145">DLL</span><span class="sxs-lookup"><span data-stu-id="5b524-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5b524-146"><dt>Pdh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b524-146"><dt>Pdh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b524-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5b524-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b524-148">**PdhVbCreateCounterPathList**</span><span class="sxs-lookup"><span data-stu-id="5b524-148">**PdhVbCreateCounterPathList**</span></span>](pdhvbcreatecounterpathlist.md)
</dt> <dt>

[<span data-ttu-id="5b524-149">**PdhVbGetCounterPathFromList**</span><span class="sxs-lookup"><span data-stu-id="5b524-149">**PdhVbGetCounterPathFromList**</span></span>](pdhvbgetcounterpathfromlist.md)
</dt> <dt>

[<span data-ttu-id="5b524-150">**PdhVbGetOneCounterPath**</span><span class="sxs-lookup"><span data-stu-id="5b524-150">**PdhVbGetOneCounterPath**</span></span>](pdhvbgetonecounterpath.md)
</dt> </dl>

 

