---
description: 將字串 FILETIME 格式的日期轉換為 CIM 日期時間格式。
ms.assetid: e375afda-5e94-46d6-b1ac-e801e0f4a620
ms.tgt_platform: multiple
title: 'SWbemDateTime. SetFileTime 方法 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.SetFileTime
- ISWbemDateTime.SetFileTime
- ISWbemDateTime.SetFileTime
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: ca3e36a284e3700e166e86f6786218bada8f369e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114877"
---
# <a name="swbemdatetimesetfiletime-method"></a><span data-ttu-id="a7496-103">SWbemDateTime. SetFileTime 方法</span><span class="sxs-lookup"><span data-stu-id="a7496-103">SWbemDateTime.SetFileTime method</span></span>

<span data-ttu-id="a7496-104">[**SWbemDateTime**](swbemdatetime.md)物件的 **SetFileTime** 方法會將字串 **FILETIME** 格式的日期轉換為 [CIM 日期時間](date-and-time-format.md)格式。</span><span class="sxs-lookup"><span data-stu-id="a7496-104">The **SetFileTime** method of the [**SWbemDateTime**](swbemdatetime.md) object converts a date in the string **FILETIME** format to the [CIM datetime](date-and-time-format.md) format.</span></span>

<span data-ttu-id="a7496-105">**FILETIME** 格式是64位的日期時間結構，表示自1月 1 1601 日開始起算的 100-毫微秒單位數。</span><span class="sxs-lookup"><span data-stu-id="a7496-105">The **FILETIME** format is a 64-bit datetime structure that represents the number of 100-nanosecond units since the beginning of January 1, 1601.</span></span> <span data-ttu-id="a7496-106">Windows Management Instrumentation (WMI) 會將 **FILETIME** 值視為不帶正負號64位數位的字串表示。</span><span class="sxs-lookup"><span data-stu-id="a7496-106">Windows Management Instrumentation (WMI) treats **FILETIME** values as string representations of unsigned 64-bit numbers.</span></span>

<span data-ttu-id="a7496-107">如需語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="a7496-107">For the syntax explanation, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a7496-108">語法</span><span class="sxs-lookup"><span data-stu-id="a7496-108">Syntax</span></span>


```VB
SWbemDateTime.SetFileTime( _
  ByVal strFileTime, _
  [ ByVal bIsLocal ] _
)
```



## <a name="parameters"></a><span data-ttu-id="a7496-109">參數</span><span class="sxs-lookup"><span data-stu-id="a7496-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7496-110">*strFileTime* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a7496-110">*strFileTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7496-111">用來設定物件的 **FILETIME** 值。</span><span class="sxs-lookup"><span data-stu-id="a7496-111">**FILETIME** value used to set the object.</span></span>

</dd> <dt>

<span data-ttu-id="a7496-112">*bIsLocal* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="a7496-112">*bIsLocal* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a7496-113">若 **為 TRUE**，則會將 *strFileTime* 視為當地時間。</span><span class="sxs-lookup"><span data-stu-id="a7496-113">If **TRUE**, *strFileTime* is interpreted as a local time.</span></span> <span data-ttu-id="a7496-114">國際標準時間 (UTC) 屬性包含轉換成正確 UTC 位移的本地時間。</span><span class="sxs-lookup"><span data-stu-id="a7496-114">The Coordinated Universal Time (UTC) property contains the local time converted to the correct UTC offset.</span></span> <span data-ttu-id="a7496-115">當 *bIsLocal* 為 **FALSE** 時，會將 *strFileTime* 直接轉換為 UTC 值，位移為 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="a7496-115">When *bIsLocal* is **FALSE**, then *strFileTime* is converted directly into a UTC value with an offset of 0 (zero).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7496-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="a7496-116">Return value</span></span>

<span data-ttu-id="a7496-117">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="a7496-117">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a7496-118">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="a7496-118">Error codes</span></span>

<span data-ttu-id="a7496-119">完成 **SetFileTime** 方法之後， [Err](/previous-versions//sbf5ze0e(v=vs.85)) 物件可能會包含下列清單中的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="a7496-119">After completing the **SetFileTime** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain the error code in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="a7496-120">**wbemErrInvalidSyntax** -2147749921 (0x80041021) </span><span class="sxs-lookup"><span data-stu-id="a7496-120">**wbemErrInvalidSyntax** - 2147749921 (0x80041021)</span></span>
</dt> <dd>

<span data-ttu-id="a7496-121">*StrFileTime* 的格式無效。</span><span class="sxs-lookup"><span data-stu-id="a7496-121">The format of *strFileTime* is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a7496-122">備註</span><span class="sxs-lookup"><span data-stu-id="a7496-122">Remarks</span></span>

<span data-ttu-id="a7496-123">成功呼叫 **SetFileTime** 之後， [**日期時間**](datetime.md) 值一律會轉譯為絕對 (**Datetime**) 值，而且 [**IsInterval**](swbemdatetime-isinterval.md) 會設定為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="a7496-123">After a successful call to **SetFileTime**, the [**datetime**](datetime.md) value is always interpreted as an absolute (**datetime**) value, and [**IsInterval**](swbemdatetime-isinterval.md) is set to **FALSE**.</span></span>

## <a name="examples"></a><span data-ttu-id="a7496-124">範例</span><span class="sxs-lookup"><span data-stu-id="a7496-124">Examples</span></span>

<span data-ttu-id="a7496-125">如需使用 [**SWbemDateTime**](swbemdatetime.md) 物件將 CIM [**日期時間**](datetime.md) 值轉換成 **FILETIME** 格式或 **VT \_ 日期** 格式的範例，請參閱 [WMI 工作：日期和時間](wmi-tasks--dates-and-times.md)。</span><span class="sxs-lookup"><span data-stu-id="a7496-125">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="a7496-126">如需 CIM **DATETIME** 格式的說明，請參閱 [日期和時間格式](date-and-time-format.md)。</span><span class="sxs-lookup"><span data-stu-id="a7496-126">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a7496-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="a7496-127">Requirements</span></span>



| <span data-ttu-id="a7496-128">需求</span><span class="sxs-lookup"><span data-stu-id="a7496-128">Requirement</span></span> | <span data-ttu-id="a7496-129">值</span><span class="sxs-lookup"><span data-stu-id="a7496-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a7496-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a7496-130">Minimum supported client</span></span><br/> | <span data-ttu-id="a7496-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a7496-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a7496-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a7496-132">Minimum supported server</span></span><br/> | <span data-ttu-id="a7496-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a7496-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a7496-134">標頭</span><span class="sxs-lookup"><span data-stu-id="a7496-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7496-135"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="a7496-135"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a7496-136">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="a7496-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="a7496-137"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a7496-137"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a7496-138">DLL</span><span class="sxs-lookup"><span data-stu-id="a7496-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7496-139"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7496-139"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="a7496-140">CLSID</span><span class="sxs-lookup"><span data-stu-id="a7496-140">CLSID</span></span><br/>                    | <span data-ttu-id="a7496-141">CLSID \_ SWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="a7496-141">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="a7496-142">IID</span><span class="sxs-lookup"><span data-stu-id="a7496-142">IID</span></span><br/>                      | <span data-ttu-id="a7496-143">IID \_ ISWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="a7496-143">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="a7496-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a7496-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7496-145">**SWbemDateTime.SetVarDate**</span><span class="sxs-lookup"><span data-stu-id="a7496-145">**SWbemDateTime.SetVarDate**</span></span>](swbemdatetime-setvardate.md)
</dt> <dt>

[<span data-ttu-id="a7496-146">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="a7496-146">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="a7496-147">**Datetime**</span><span class="sxs-lookup"><span data-stu-id="a7496-147">**DATETIME**</span></span>](datetime.md)
</dt> </dl>

 

