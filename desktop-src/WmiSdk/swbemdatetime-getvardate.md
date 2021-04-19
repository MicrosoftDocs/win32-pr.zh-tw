---
description: 將 CIM DATETIME 格式的日期和時間值轉換成 VT \_ 日期格式。
ms.assetid: e63e7acc-89d4-458a-a1ab-4d4a65cf7f8b
ms.tgt_platform: multiple
title: 'SWbemDateTime. GetVarDate 方法 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.GetVarDate
- ISWbemDateTime.GetVarDate
- ISWbemDateTime.GetVarDate
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: b4d0c71e4748774eacab4b234092178179a4a774
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974191"
---
# <a name="swbemdatetimegetvardate-method"></a><span data-ttu-id="bd6c5-103">SWbemDateTime. GetVarDate 方法</span><span class="sxs-lookup"><span data-stu-id="bd6c5-103">SWbemDateTime.GetVarDate method</span></span>

<span data-ttu-id="bd6c5-104">[**SWbemDateTime**](swbemdatetime.md)物件的 **GetVarDate** 方法會將 CIM [**DATETIME**](datetime.md)格式的日期和時間值轉換成 **VT \_ 日期** 格式。</span><span class="sxs-lookup"><span data-stu-id="bd6c5-104">The **GetVarDate** method of the [**SWbemDateTime**](swbemdatetime.md) object converts a date and time value in the CIM [**DATETIME**](datetime.md) format to the **VT\_DATE** format.</span></span>

<span data-ttu-id="bd6c5-105">**VT \_ 日期** 格式是 Visual Basic 和 ActiveX 使用的 automation variant [**DATETIME**](datetime.md)值。</span><span class="sxs-lookup"><span data-stu-id="bd6c5-105">The **VT\_DATE** format is an automation variant [**DATETIME**](datetime.md) value that Visual Basic and ActiveX use.</span></span>

<span data-ttu-id="bd6c5-106">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="bd6c5-106">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="bd6c5-107">語法</span><span class="sxs-lookup"><span data-stu-id="bd6c5-107">Syntax</span></span>


```VB
vdate = .GetVarDate( _
  [ ByVal bIsLocal ] _
)
```



## <a name="parameters"></a><span data-ttu-id="bd6c5-108">參數</span><span class="sxs-lookup"><span data-stu-id="bd6c5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd6c5-109">*bIsLocal* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="bd6c5-109">*bIsLocal* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bd6c5-110">指出傳回的值是否會被視為當地時間。</span><span class="sxs-lookup"><span data-stu-id="bd6c5-110">Indicates whether the returned value is interpreted as local time.</span></span> <span data-ttu-id="bd6c5-111">國際標準時間 (UTC) 屬性包含轉換成正確 UTC 位移的本地時間。</span><span class="sxs-lookup"><span data-stu-id="bd6c5-111">The Coordinated Universal Time (UTC) property contains the local time converted to the correct UTC offset.</span></span> <span data-ttu-id="bd6c5-112">如果值為 **FALSE**，則會將值視為 UTC，並將零 (0) 位移。</span><span class="sxs-lookup"><span data-stu-id="bd6c5-112">If the value is **FALSE**, then the value is interpreted as UTC with a zero (0) offset.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd6c5-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="bd6c5-113">Return value</span></span>

<span data-ttu-id="bd6c5-114">以 **VT \_ 日期** 格式的日期和時間值。</span><span class="sxs-lookup"><span data-stu-id="bd6c5-114">The date and time value in the **VT\_DATE** format.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd6c5-115">備註</span><span class="sxs-lookup"><span data-stu-id="bd6c5-115">Remarks</span></span>

<span data-ttu-id="bd6c5-116">**VT \_日期** 和 **FILETIME** 值不能包含萬用字元欄位。</span><span class="sxs-lookup"><span data-stu-id="bd6c5-116">**VT\_DATE** and **FILETIME** values cannot contain wildcard fields.</span></span>

<span data-ttu-id="bd6c5-117">如果下列任何一個屬性為 **FALSE**，則 **GetVarDate** 方法會失敗 (**wbemErrFailed**) ：</span><span class="sxs-lookup"><span data-stu-id="bd6c5-117">The **GetVarDate** method fails (**wbemErrFailed**) if any of the following properties are **FALSE**:</span></span>

-   [<span data-ttu-id="bd6c5-118">**YearSpecified**</span><span class="sxs-lookup"><span data-stu-id="bd6c5-118">**YearSpecified**</span></span>](swbemdatetime-yearspecified.md)
-   [<span data-ttu-id="bd6c5-119">**MonthSpecified**</span><span class="sxs-lookup"><span data-stu-id="bd6c5-119">**MonthSpecified**</span></span>](swbemdatetime-monthspecified.md)
-   [<span data-ttu-id="bd6c5-120">**DaySpecified**</span><span class="sxs-lookup"><span data-stu-id="bd6c5-120">**DaySpecified**</span></span>](swbemdatetime-dayspecified.md)
-   [<span data-ttu-id="bd6c5-121">**HoursSpecified**</span><span class="sxs-lookup"><span data-stu-id="bd6c5-121">**HoursSpecified**</span></span>](swbemdatetime-hoursspecified.md)
-   [<span data-ttu-id="bd6c5-122">**MinutesSpecified**</span><span class="sxs-lookup"><span data-stu-id="bd6c5-122">**MinutesSpecified**</span></span>](swbemdatetime-minutesspecified.md)
-   [<span data-ttu-id="bd6c5-123">**SecondsSpecified**</span><span class="sxs-lookup"><span data-stu-id="bd6c5-123">**SecondsSpecified**</span></span>](swbemdatetime-secondsspecified.md)
-   [<span data-ttu-id="bd6c5-124">**MicrosecondsSpecified**</span><span class="sxs-lookup"><span data-stu-id="bd6c5-124">**MicrosecondsSpecified**</span></span>](swbemdatetime-microsecondsspecified.md)
-   [<span data-ttu-id="bd6c5-125">**UTCSpecified**</span><span class="sxs-lookup"><span data-stu-id="bd6c5-125">**UTCSpecified**</span></span>](swbemdatetime-utcspecified.md)

<span data-ttu-id="bd6c5-126">從 [**SetVarDate**](swbemdatetime-setvardate.md)成功傳回時，這些屬性全都會設定為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="bd6c5-126">On successful return from [**SetVarDate**](swbemdatetime-setvardate.md), all of these properties are set to **TRUE**.</span></span>

<span data-ttu-id="bd6c5-127">在成功呼叫 [**SetVarDate**](swbemdatetime-setvardate.md)之後， [**日期時間**](datetime.md) 值一律會被視為絕對 **日期時間** 值，而不是間隔，而 [**IsInterval**](swbemdatetime-isinterval.md) 會設定為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="bd6c5-127">After a successful call to [**SetVarDate**](swbemdatetime-setvardate.md), the [**DATETIME**](datetime.md) value is always interpreted as an absolute **DATETIME** value instead of an interval, and the [**IsInterval**](swbemdatetime-isinterval.md) is set to **FALSE**.</span></span>

<span data-ttu-id="bd6c5-128">如果 [**IsInterval**](swbemdatetime-isinterval.md) 設定為 **TRUE**，則呼叫 **GetVarDate** 會導致 **wbemErrFailed** 錯誤。</span><span class="sxs-lookup"><span data-stu-id="bd6c5-128">If [**IsInterval**](swbemdatetime-isinterval.md) is set to **TRUE**, then a call to **GetVarDate** results in the **wbemErrFailed** error.</span></span>

<span data-ttu-id="bd6c5-129">當您呼叫 **GetVarDate** 時，會遺失精確度，因為 [日期時間](datetime.md) 值的 ( s 為一微秒) 解析， **而 \_ VT 日期** 值的解析度是500毫秒。</span><span class="sxs-lookup"><span data-stu-id="bd6c5-129">Some loss of precision occurs when you call **GetVarDate**, because [datetime](datetime.md) values have a one microsecond ( s) resolution, and **VT\_DATE** values have a 500 millisecond resolution.</span></span>

## <a name="examples"></a><span data-ttu-id="bd6c5-130">範例</span><span class="sxs-lookup"><span data-stu-id="bd6c5-130">Examples</span></span>

<span data-ttu-id="bd6c5-131">如需使用 [**SWbemDateTime**](swbemdatetime.md) 物件將 CIM [**日期時間**](datetime.md) 值轉換成 **FILETIME** 或 **VT \_ 日期** 格式的範例，請參閱 [WMI 工作：日期和時間](wmi-tasks--dates-and-times.md)。</span><span class="sxs-lookup"><span data-stu-id="bd6c5-131">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="bd6c5-132">如需 CIM **DATETIME** 格式的說明，請參閱 [日期和時間格式](date-and-time-format.md)。</span><span class="sxs-lookup"><span data-stu-id="bd6c5-132">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bd6c5-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="bd6c5-133">Requirements</span></span>



| <span data-ttu-id="bd6c5-134">需求</span><span class="sxs-lookup"><span data-stu-id="bd6c5-134">Requirement</span></span> | <span data-ttu-id="bd6c5-135">值</span><span class="sxs-lookup"><span data-stu-id="bd6c5-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bd6c5-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bd6c5-136">Minimum supported client</span></span><br/> | <span data-ttu-id="bd6c5-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bd6c5-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bd6c5-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bd6c5-138">Minimum supported server</span></span><br/> | <span data-ttu-id="bd6c5-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bd6c5-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bd6c5-140">標頭</span><span class="sxs-lookup"><span data-stu-id="bd6c5-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd6c5-141"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="bd6c5-141"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="bd6c5-142">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="bd6c5-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="bd6c5-143"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="bd6c5-143"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="bd6c5-144">DLL</span><span class="sxs-lookup"><span data-stu-id="bd6c5-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd6c5-145"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd6c5-145"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="bd6c5-146">CLSID</span><span class="sxs-lookup"><span data-stu-id="bd6c5-146">CLSID</span></span><br/>                    | <span data-ttu-id="bd6c5-147">CLSID \_ SWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="bd6c5-147">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="bd6c5-148">IID</span><span class="sxs-lookup"><span data-stu-id="bd6c5-148">IID</span></span><br/>                      | <span data-ttu-id="bd6c5-149">IID \_ ISWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="bd6c5-149">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="bd6c5-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bd6c5-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd6c5-151">**SWbemDateTime.GetFileTime**</span><span class="sxs-lookup"><span data-stu-id="bd6c5-151">**SWbemDateTime.GetFileTime**</span></span>](swbemdatetime-getfiletime.md)
</dt> <dt>

[<span data-ttu-id="bd6c5-152">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="bd6c5-152">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="bd6c5-153">Datetime</span><span class="sxs-lookup"><span data-stu-id="bd6c5-153">DATETIME</span></span>](datetime.md)
</dt> </dl>

 

 




