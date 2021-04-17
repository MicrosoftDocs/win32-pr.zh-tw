---
description: 將 CIM DATETIME 格式的日期和時間值轉換成 FILETIME 格式。
ms.assetid: 08e0761d-e735-454a-8429-2bd1eb331123
ms.tgt_platform: multiple
title: 'SWbemDateTime. GetFileTime 方法 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.GetFileTime
- ISWbemDateTime.GetFileTime
- ISWbemDateTime.GetFileTime
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3f8a8c85cb4c78be578187b1f55afce078fe7bd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104469452"
---
# <a name="swbemdatetimegetfiletime-method"></a><span data-ttu-id="15965-103">SWbemDateTime. GetFileTime 方法</span><span class="sxs-lookup"><span data-stu-id="15965-103">SWbemDateTime.GetFileTime method</span></span>

<span data-ttu-id="15965-104">[**SWbemDateTime**](swbemdatetime.md)物件的 **GetFileTime** 方法會將 CIM [DATETIME](datetime.md)格式的日期和時間值轉換成 FILETIME 格式。</span><span class="sxs-lookup"><span data-stu-id="15965-104">The **GetFileTime** method of the [**SWbemDateTime**](swbemdatetime.md) object converts a date and time value in the CIM [DATETIME](datetime.md) format to the FILETIME format.</span></span>

<span data-ttu-id="15965-105">如果參數設定為 **TRUE**，則傳回值代表用戶端的本機時間。</span><span class="sxs-lookup"><span data-stu-id="15965-105">If the parameter is set to **TRUE**, then the return value represents a local time for the client.</span></span> <span data-ttu-id="15965-106">否則，傳回值為國際標準時間 (UTC) 時間。</span><span class="sxs-lookup"><span data-stu-id="15965-106">Otherwise, the return value is a Coordinated Universal Time (UTC) time.</span></span> <span data-ttu-id="15965-107">**FILETIME** [DATETIME](datetime.md)結構是64位的值，代表自1月 1 1601 日開始起算的 100-毫微秒單位數。</span><span class="sxs-lookup"><span data-stu-id="15965-107">A **FILETIME** [DATETIME](datetime.md) structure is a 64-bit value that represents the number of 100-nanosecond units since the beginning of January 1, 1601.</span></span> <span data-ttu-id="15965-108">Windows Management Instrumentation (WMI) 會將 **FILETIME** 值視為不帶正負號64位數位的字串表示。</span><span class="sxs-lookup"><span data-stu-id="15965-108">Windows Management Instrumentation (WMI) treats **FILETIME** values as string representations of unsigned 64-bit numbers.</span></span>

<span data-ttu-id="15965-109">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="15965-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="15965-110">語法</span><span class="sxs-lookup"><span data-stu-id="15965-110">Syntax</span></span>


```VB
vDate = .GetFileTime( _
  [ ByVal bIsLocaL ] _
)
```



## <a name="parameters"></a><span data-ttu-id="15965-111">參數</span><span class="sxs-lookup"><span data-stu-id="15965-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15965-112">*bIsLocaL* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="15965-112">*bIsLocaL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="15965-113">指出傳回的值是否會被視為當地時間。</span><span class="sxs-lookup"><span data-stu-id="15965-113">Indicates whether the returned value is interpreted as local time.</span></span> <span data-ttu-id="15965-114">UTC 屬性接著會包含轉換成正確國際標準時間的當地時間 (UTC) 位移。</span><span class="sxs-lookup"><span data-stu-id="15965-114">The UTC property then contains the local time converted to the correct Coordinated Universal Times (UTC) offset.</span></span> <span data-ttu-id="15965-115">如果值為 **FALSE**，則會將值視為 UTC，並將零 (0) 位移。</span><span class="sxs-lookup"><span data-stu-id="15965-115">If the value is **FALSE**, then the value is interpreted as UTC with a zero (0) offset.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15965-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="15965-116">Return value</span></span>

<span data-ttu-id="15965-117">**FILETIME** 格式的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="15965-117">The date and time in the **FILETIME** format.</span></span>

## <a name="error-codes"></a><span data-ttu-id="15965-118">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="15965-118">Error codes</span></span>

<span data-ttu-id="15965-119">完成 **GetFileTime** 方法之後， [Err](/previous-versions//sbf5ze0e(v=vs.85)) 物件可能會包含下列清單中的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="15965-119">After completing the **GetFileTime** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain the error code in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="15965-120">**wbemErrFailed** -2147749889 (0x80041001) </span><span class="sxs-lookup"><span data-stu-id="15965-120">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="15965-121">呼叫失敗。</span><span class="sxs-lookup"><span data-stu-id="15965-121">The call failed.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="15965-122">備註</span><span class="sxs-lookup"><span data-stu-id="15965-122">Remarks</span></span>

<span data-ttu-id="15965-123">**VT \_日期** 和 **FILETIME** 值不能包含萬用字元欄位。</span><span class="sxs-lookup"><span data-stu-id="15965-123">**VT\_DATE** and **FILETIME** values cannot contain wildcard fields.</span></span>

<span data-ttu-id="15965-124">如果下列任何一個屬性為 **FALSE**，則 **GetFileTime** 方法會失敗 (wbemErrFailed) ：</span><span class="sxs-lookup"><span data-stu-id="15965-124">The **GetFileTime** method fails (wbemErrFailed) if any of the following properties are **FALSE**:</span></span>

-   [<span data-ttu-id="15965-125">**YearSpecified**</span><span class="sxs-lookup"><span data-stu-id="15965-125">**YearSpecified**</span></span>](swbemdatetime-yearspecified.md)
-   [<span data-ttu-id="15965-126">**MonthSpecified**</span><span class="sxs-lookup"><span data-stu-id="15965-126">**MonthSpecified**</span></span>](swbemdatetime-monthspecified.md)
-   [<span data-ttu-id="15965-127">**DaySpecified**</span><span class="sxs-lookup"><span data-stu-id="15965-127">**DaySpecified**</span></span>](swbemdatetime-dayspecified.md)
-   [<span data-ttu-id="15965-128">**HoursSpecified**</span><span class="sxs-lookup"><span data-stu-id="15965-128">**HoursSpecified**</span></span>](swbemdatetime-hoursspecified.md)
-   [<span data-ttu-id="15965-129">**MinutesSpecified**</span><span class="sxs-lookup"><span data-stu-id="15965-129">**MinutesSpecified**</span></span>](swbemdatetime-minutesspecified.md)
-   [<span data-ttu-id="15965-130">**SecondsSpecified**</span><span class="sxs-lookup"><span data-stu-id="15965-130">**SecondsSpecified**</span></span>](swbemdatetime-secondsspecified.md)
-   [<span data-ttu-id="15965-131">**MicrosecondsSpecified**</span><span class="sxs-lookup"><span data-stu-id="15965-131">**MicrosecondsSpecified**</span></span>](swbemdatetime-microsecondsspecified.md)
-   [<span data-ttu-id="15965-132">**UTCSpecified**</span><span class="sxs-lookup"><span data-stu-id="15965-132">**UTCSpecified**</span></span>](swbemdatetime-utcspecified.md)

<span data-ttu-id="15965-133">從 [**SetFileTime**](swbemdatetime-setfiletime.md)成功傳回時，這些屬性全都會設定為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="15965-133">On a successful return from [**SetFileTime**](swbemdatetime-setfiletime.md), all of these properties are set to **TRUE**.</span></span>

## <a name="examples"></a><span data-ttu-id="15965-134">範例</span><span class="sxs-lookup"><span data-stu-id="15965-134">Examples</span></span>

<span data-ttu-id="15965-135">如需使用 [**SWbemDateTime**](swbemdatetime.md) 物件將 CIM [**日期時間**](datetime.md) 值轉換成 **FILETIME** 格式或 **VT \_ 日期** 格式的範例，請參閱 [WMI 工作：日期和時間](wmi-tasks--dates-and-times.md)。</span><span class="sxs-lookup"><span data-stu-id="15965-135">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="15965-136">如需 CIM **DATETIME** 格式的說明，請參閱 [日期和時間格式](date-and-time-format.md)。</span><span class="sxs-lookup"><span data-stu-id="15965-136">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="15965-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="15965-137">Requirements</span></span>



| <span data-ttu-id="15965-138">需求</span><span class="sxs-lookup"><span data-stu-id="15965-138">Requirement</span></span> | <span data-ttu-id="15965-139">值</span><span class="sxs-lookup"><span data-stu-id="15965-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="15965-140">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="15965-140">Minimum supported client</span></span><br/> | <span data-ttu-id="15965-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="15965-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="15965-142">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="15965-142">Minimum supported server</span></span><br/> | <span data-ttu-id="15965-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="15965-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="15965-144">標頭</span><span class="sxs-lookup"><span data-stu-id="15965-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="15965-145"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="15965-145"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="15965-146">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="15965-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="15965-147"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="15965-147"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="15965-148">DLL</span><span class="sxs-lookup"><span data-stu-id="15965-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15965-149"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15965-149"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="15965-150">CLSID</span><span class="sxs-lookup"><span data-stu-id="15965-150">CLSID</span></span><br/>                    | <span data-ttu-id="15965-151">CLSID \_ SWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="15965-151">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="15965-152">IID</span><span class="sxs-lookup"><span data-stu-id="15965-152">IID</span></span><br/>                      | <span data-ttu-id="15965-153">IID \_ ISWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="15965-153">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="15965-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="15965-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15965-155">**SWbemDateTime. GetVarDate**</span><span class="sxs-lookup"><span data-stu-id="15965-155">**SWbemDateTime.GetVarDate**</span></span>](swbemdatetime-getvardate.md)
</dt> <dt>

[<span data-ttu-id="15965-156">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="15965-156">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="15965-157">**Datetime**</span><span class="sxs-lookup"><span data-stu-id="15965-157">**DATETIME**</span></span>](datetime.md)
</dt> </dl>

 

