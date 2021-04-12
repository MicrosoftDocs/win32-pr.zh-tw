---
description: 將 VT 日期格式的日期轉換 \_ 為 CIM 日期時間格式。
ms.assetid: 24c39d44-22ac-44ac-9e05-72a5b666ab19
ms.tgt_platform: multiple
title: 'SWbemDateTime. SetVarDate 方法 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.SetVarDate
- ISWbemDateTime.SetVarDate
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 8641bad2c59f100b689c74e23faf727bc80d2f49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320531"
---
# <a name="swbemdatetimesetvardate-method"></a><span data-ttu-id="c5ea2-103">SWbemDateTime. SetVarDate 方法</span><span class="sxs-lookup"><span data-stu-id="c5ea2-103">SWbemDateTime.SetVarDate method</span></span>

<span data-ttu-id="c5ea2-104">[**SWbemDateTime**](swbemdatetime.md)物件的 **SetVarDate** 方法會將 **VT \_ 日期** 格式的日期轉換為 [CIM 日期時間](date-and-time-format.md)格式。</span><span class="sxs-lookup"><span data-stu-id="c5ea2-104">The **SetVarDate** method of the [**SWbemDateTime**](swbemdatetime.md) object converts a date in the **VT\_DATE** format to the [CIM datetime](date-and-time-format.md) format.</span></span>

<span data-ttu-id="c5ea2-105">**VT \_ 日期** 值是 Visual Basic 和 ActiveX 使用的 variant datetime 值。</span><span class="sxs-lookup"><span data-stu-id="c5ea2-105">A **VT\_DATE** value is a variant datetime value that Visual Basic and ActiveX use.</span></span>

<span data-ttu-id="c5ea2-106">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="c5ea2-106">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c5ea2-107">語法</span><span class="sxs-lookup"><span data-stu-id="c5ea2-107">Syntax</span></span>


```VB
SWbemDateTime.SetVarDate( _
  ByVal vdate, _
  [ ByVal bIsLocal ] _
)
```



## <a name="parameters"></a><span data-ttu-id="c5ea2-108">參數</span><span class="sxs-lookup"><span data-stu-id="c5ea2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5ea2-109">*vdate* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c5ea2-109">*vdate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5ea2-110">要設定物件的變異日期值。</span><span class="sxs-lookup"><span data-stu-id="c5ea2-110">The variant date value to set the object.</span></span> <span data-ttu-id="c5ea2-111">此參數必須是 **VT \_ 日期** 格式。</span><span class="sxs-lookup"><span data-stu-id="c5ea2-111">This parameter must be in the **VT\_DATE** format.</span></span>

</dd> <dt>

<span data-ttu-id="c5ea2-112">*bIsLocal* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="c5ea2-112">*bIsLocal* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c5ea2-113">若為 **TRUE**，則會將 *vdate* 視為當地時間，而國際標準時間 (UTC) 屬性包含轉換成正確 UTC 位移的當地時間。</span><span class="sxs-lookup"><span data-stu-id="c5ea2-113">If **TRUE**, *vdate* is interpreted as a local time, and the Coordinated Universal Time (UTC) property contains the local time that is converted to the correct UTC offset.</span></span> <span data-ttu-id="c5ea2-114">當 *bIsLocal* 為 **FALSE** 時，會將 *vdate* 直接轉換為 UTC 值，且位移為零 (0) 。</span><span class="sxs-lookup"><span data-stu-id="c5ea2-114">When *bIsLocal* is **FALSE**, then *vdate* is converted directly into a UTC value with an offset of zero (0).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5ea2-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="c5ea2-115">Return value</span></span>

<span data-ttu-id="c5ea2-116">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="c5ea2-116">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c5ea2-117">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="c5ea2-117">Error codes</span></span>

<span data-ttu-id="c5ea2-118">完成 **SetVarDate** 方法之後， [Err](/previous-versions//sbf5ze0e(v=vs.85)) 物件可能會包含下列清單中的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c5ea2-118">After completing the **SetVarDate** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain the error code in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="c5ea2-119">**wbemErrInvalidSyntax** -2147749921 (0x80041021) </span><span class="sxs-lookup"><span data-stu-id="c5ea2-119">**wbemErrInvalidSyntax** - 2147749921 (0x80041021)</span></span>
</dt> <dd>

<span data-ttu-id="c5ea2-120">*Vdate* 的格式無效。</span><span class="sxs-lookup"><span data-stu-id="c5ea2-120">The format of *vdate* is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c5ea2-121">備註</span><span class="sxs-lookup"><span data-stu-id="c5ea2-121">Remarks</span></span>

<span data-ttu-id="c5ea2-122">成功呼叫 **SetVarDate** 之後，會將 [**DATETIME**](datetime.md) 值視為絕對 datetime 值，而不是間隔，而 [**IsInterval**](swbemdatetime-isinterval.md) 屬性會設定為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="c5ea2-122">After a successful call to **SetVarDate**, the [**DATETIME**](datetime.md) value is interpreted as an absolute datetime value instead of an interval, and the [**IsInterval**](swbemdatetime-isinterval.md) property is set to **FALSE**.</span></span>

<span data-ttu-id="c5ea2-123">內建 Visual Basic 或 VBScript 函數 [CDate](/previous-versions//2dt118h2(v=vs.85))以 **VT \_ 日期** 格式提供 [**日期時間**](datetime.md)值給 **SetVarDate** 輸入。</span><span class="sxs-lookup"><span data-stu-id="c5ea2-123">The intrinsic Visual Basic or VBScript function [CDate](/previous-versions//2dt118h2(v=vs.85)) provides a [**datetime**](datetime.md) value in the **VT\_DATE** format for input to **SetVarDate**.</span></span>

## <a name="examples"></a><span data-ttu-id="c5ea2-124">範例</span><span class="sxs-lookup"><span data-stu-id="c5ea2-124">Examples</span></span>

<span data-ttu-id="c5ea2-125">如需使用 [**SWbemDateTime**](swbemdatetime.md) 物件將 CIM [**日期時間**](datetime.md) 值轉換成 **FILETIME** 格式或 **VT \_ 日期** 格式的範例，請參閱 [WMI 工作：日期和時間](wmi-tasks--dates-and-times.md)。</span><span class="sxs-lookup"><span data-stu-id="c5ea2-125">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="c5ea2-126">如需 CIM **DATETIME** 格式的說明，請參閱 [日期和時間格式](date-and-time-format.md)。</span><span class="sxs-lookup"><span data-stu-id="c5ea2-126">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

<span data-ttu-id="c5ea2-127">在 TechNet 資源庫中將 [日期轉換為 WMI Date-Time 格式](https://Gallery.TechNet.Microsoft.Com/33beff76-1b5f-4ba1-a8ea-5e124eb74306) VBScript 程式碼範例使用 SetVarDate，將一般日期時間值轉換成 UTC 日期時間格式。</span><span class="sxs-lookup"><span data-stu-id="c5ea2-127">The [Convert Date to WMI Date-Time Format](https://Gallery.TechNet.Microsoft.Com/33beff76-1b5f-4ba1-a8ea-5e124eb74306) VBScript code sample in the TechNet Gallery uses SetVarDate to convert a regular date-time value into the UTC date-time format.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5ea2-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="c5ea2-128">Requirements</span></span>



| <span data-ttu-id="c5ea2-129">需求</span><span class="sxs-lookup"><span data-stu-id="c5ea2-129">Requirement</span></span> | <span data-ttu-id="c5ea2-130">值</span><span class="sxs-lookup"><span data-stu-id="c5ea2-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c5ea2-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c5ea2-131">Minimum supported client</span></span><br/> | <span data-ttu-id="c5ea2-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c5ea2-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c5ea2-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c5ea2-133">Minimum supported server</span></span><br/> | <span data-ttu-id="c5ea2-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c5ea2-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c5ea2-135">標頭</span><span class="sxs-lookup"><span data-stu-id="c5ea2-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5ea2-136"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="c5ea2-136"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c5ea2-137">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="c5ea2-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="c5ea2-138"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c5ea2-138"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c5ea2-139">DLL</span><span class="sxs-lookup"><span data-stu-id="c5ea2-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c5ea2-140"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c5ea2-140"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="c5ea2-141">CLSID</span><span class="sxs-lookup"><span data-stu-id="c5ea2-141">CLSID</span></span><br/>                    | <span data-ttu-id="c5ea2-142">CLSID \_ SWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="c5ea2-142">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="c5ea2-143">IID</span><span class="sxs-lookup"><span data-stu-id="c5ea2-143">IID</span></span><br/>                      | <span data-ttu-id="c5ea2-144">IID \_ ISWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="c5ea2-144">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="c5ea2-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c5ea2-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5ea2-146">**SWbemDateTime.SetFileTime**</span><span class="sxs-lookup"><span data-stu-id="c5ea2-146">**SWbemDateTime.SetFileTime**</span></span>](swbemdatetime-setfiletime.md)
</dt> <dt>

[<span data-ttu-id="c5ea2-147">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="c5ea2-147">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="c5ea2-148">**Datetime**</span><span class="sxs-lookup"><span data-stu-id="c5ea2-148">**DATETIME**</span></span>](datetime.md)
</dt> </dl>

 

