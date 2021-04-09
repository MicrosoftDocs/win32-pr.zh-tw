---
description: 取得或設定值，這個值表示 datetime 值的日元件。
ms.assetid: 60da99bc-560c-45bc-b787-f4bef8e5a509
ms.tgt_platform: multiple
title: 'SWbemDateTime Day 屬性 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Day
- ISWbemDateTime.Day
- ISWbemDateTime.get_Day
- ISWbemDateTime.put_Day
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 1de77a8e5d616284c3dc13a19bce2526db371c20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945107"
---
# <a name="swbemdatetimeday-property"></a><span data-ttu-id="5389c-103">SWbemDateTime Day 屬性</span><span class="sxs-lookup"><span data-stu-id="5389c-103">SWbemDateTime.Day property</span></span>

<span data-ttu-id="5389c-104">[**SWbemDateTime**](swbemdatetime.md)物件的 **day** 屬性會取得或設定值，這個值表示 datetime 值的日元件。</span><span class="sxs-lookup"><span data-stu-id="5389c-104">The **Day** property of the [**SWbemDateTime**](swbemdatetime.md) object gets or sets a value that represents the day component of the datetime value.</span></span> <span data-ttu-id="5389c-105">如果 [**IsInterval**](swbemdatetime-isinterval.md) 為 **FALSE**，則值必須在1到31的範圍內。</span><span class="sxs-lookup"><span data-stu-id="5389c-105">The value must be in the range of 1 through 31 if [**IsInterval**](swbemdatetime-isinterval.md) is **FALSE**.</span></span> <span data-ttu-id="5389c-106">不過，錯誤檢查不會區分月份的值。</span><span class="sxs-lookup"><span data-stu-id="5389c-106">However, error checking is not sensitive to the month value.</span></span> <span data-ttu-id="5389c-107">因此，如果 [**SWbemDateTime**](swbemdatetime-month.md) 的月份值小於 31 (天、四月、六月、九月、11月) ，則範圍內的值31不會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="5389c-107">Thus, the in-range value of 31 will not return an error in the cases where the [**SWbemDateTime.Month**](swbemdatetime-month.md) value is for a month of fewer than 31 days (February, April, June, September, November).</span></span>

<span data-ttu-id="5389c-108">**Day** 的預設值是01。</span><span class="sxs-lookup"><span data-stu-id="5389c-108">The default value for **Day** is 01.</span></span>

<span data-ttu-id="5389c-109">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="5389c-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="5389c-110">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="5389c-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="5389c-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="5389c-111">Syntax</span></span>


```VB
SWbemDateTime.Day As Long
```



## <a name="property-value"></a><span data-ttu-id="5389c-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="5389c-112">Property value</span></span>

## <a name="error-codes"></a><span data-ttu-id="5389c-113">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="5389c-113">Error codes</span></span>

<span data-ttu-id="5389c-114">取得或設定 **Day** 屬性之後， [Err](/previous-versions//sbf5ze0e(v=vs.85)) 物件可能會包含下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="5389c-114">After you get or set the **Day** property, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="5389c-115">**wbemErrValueOutOfRange** -2147749931 (0x8004102B) </span><span class="sxs-lookup"><span data-stu-id="5389c-115">**wbemErrValueOutOfRange** - 2147749931 (0x8004102B)</span></span>
</dt> <dd>

<span data-ttu-id="5389c-116">如果 [**IsInterval**](swbemdatetime-isinterval.md) 為 **TRUE** ，且正確值的範圍超過0到99999999。</span><span class="sxs-lookup"><span data-stu-id="5389c-116">If [**IsInterval**](swbemdatetime-isinterval.md) is **TRUE** and the range of correct values exceeds 0 through 99999999.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="5389c-117">範例</span><span class="sxs-lookup"><span data-stu-id="5389c-117">Examples</span></span>

<span data-ttu-id="5389c-118">如需使用 [**SWbemDateTime**](swbemdatetime.md) 物件將 CIM [**日期時間**](datetime.md) 值轉換成 **FILETIME** 格式或 **VT \_ 日期** 格式的範例，請參閱 [WMI 工作：日期和時間](wmi-tasks--dates-and-times.md)。</span><span class="sxs-lookup"><span data-stu-id="5389c-118">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="5389c-119">如需 CIM **DATETIME** 格式的說明，請參閱 [日期和時間格式](date-and-time-format.md)。</span><span class="sxs-lookup"><span data-stu-id="5389c-119">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5389c-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="5389c-120">Requirements</span></span>



| <span data-ttu-id="5389c-121">需求</span><span class="sxs-lookup"><span data-stu-id="5389c-121">Requirement</span></span> | <span data-ttu-id="5389c-122">值</span><span class="sxs-lookup"><span data-stu-id="5389c-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5389c-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5389c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="5389c-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5389c-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5389c-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5389c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="5389c-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5389c-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5389c-127">標頭</span><span class="sxs-lookup"><span data-stu-id="5389c-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="5389c-128"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="5389c-128"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="5389c-129">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="5389c-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="5389c-130"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5389c-130"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5389c-131">DLL</span><span class="sxs-lookup"><span data-stu-id="5389c-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5389c-132"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5389c-132"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="5389c-133">CLSID</span><span class="sxs-lookup"><span data-stu-id="5389c-133">CLSID</span></span><br/>                    | <span data-ttu-id="5389c-134">CLSID \_ SWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="5389c-134">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="5389c-135">IID</span><span class="sxs-lookup"><span data-stu-id="5389c-135">IID</span></span><br/>                      | <span data-ttu-id="5389c-136">IID \_ ISWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="5389c-136">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="5389c-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5389c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5389c-138">**SWbemDateTime.DaySpecified**</span><span class="sxs-lookup"><span data-stu-id="5389c-138">**SWbemDateTime.DaySpecified**</span></span>](swbemdatetime-dayspecified.md)
</dt> <dt>

[<span data-ttu-id="5389c-139">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="5389c-139">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="5389c-140">Datetime</span><span class="sxs-lookup"><span data-stu-id="5389c-140">DATETIME</span></span>](datetime.md)
</dt> </dl>

 

