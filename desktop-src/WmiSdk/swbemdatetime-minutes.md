---
description: 取得或設定值，這個值表示 datetime 值的分鐘元件。
ms.assetid: a52a66c2-f7ab-48d0-bdee-a07984ed3bc2
ms.tgt_platform: multiple
title: 'SWbemDateTime：分鐘屬性 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Minutes
- ISWbemDateTime.Minutes
- ISWbemDateTime.get_Minutes
- ISWbemDateTime.put_Minutes
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: cce55d731916d0e8180de1bde495566d4ed22c49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975319"
---
# <a name="swbemdatetimeminutes-property"></a><span data-ttu-id="dcbed-103">SWbemDateTime 分鐘屬性</span><span class="sxs-lookup"><span data-stu-id="dcbed-103">SWbemDateTime.Minutes property</span></span>

<span data-ttu-id="dcbed-104">[**SWbemDateTime**](swbemdatetime.md)物件的 **分鐘** 屬性會取得或設定值，這個值表示 datetime 值的分鐘元件。</span><span class="sxs-lookup"><span data-stu-id="dcbed-104">The **Minutes** property of the [**SWbemDateTime**](swbemdatetime.md) object gets or sets a value that represents the minutes component of the datetime value.</span></span>

<span data-ttu-id="dcbed-105">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="dcbed-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="dcbed-106">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="dcbed-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcbed-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="dcbed-107">Syntax</span></span>


```VB
SWbemDateTime.Minutes As Long
```



## <a name="property-value"></a><span data-ttu-id="dcbed-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="dcbed-108">Property value</span></span>

## <a name="error-codes"></a><span data-ttu-id="dcbed-109">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="dcbed-109">Error codes</span></span>

<span data-ttu-id="dcbed-110">取得或設定 **分鐘** 屬性之後， [Err](/previous-versions//sbf5ze0e(v=vs.85)) 物件可能會包含下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="dcbed-110">After you get or set the **Minutes** property, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="dcbed-111">**wbemErrValueOutOfRange** -2147749931 (0x8004102B) </span><span class="sxs-lookup"><span data-stu-id="dcbed-111">**wbemErrValueOutOfRange** - 2147749931 (0x8004102B)</span></span>
</dt> <dd>

<span data-ttu-id="dcbed-112">值不在0到59的範圍內。</span><span class="sxs-lookup"><span data-stu-id="dcbed-112">The value was not in the range of 0 through 59.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dcbed-113">備註</span><span class="sxs-lookup"><span data-stu-id="dcbed-113">Remarks</span></span>

<span data-ttu-id="dcbed-114">如果 [ **SWbemDateTime** ] 屬性設定為1，則 [ [**SWbemDateTime**](swbemdatetime-seconds.md) ] 屬性所包含的值會以一秒位移，這是當 CIM 日期 **時間** 值轉譯成 **VT \_ 日期** 值時所發生的舍入錯誤。</span><span class="sxs-lookup"><span data-stu-id="dcbed-114">If the **SWbemDateTime.Minutes** property is set to 1, then the [**SWbemDateTime.Seconds**](swbemdatetime-seconds.md) property contains a value that is offset by one second a rounding error that occurs when a CIM **datetime** value is translated to a **VT\_DATE** value.</span></span> <span data-ttu-id="dcbed-115">如果 [ **分鐘** ] 屬性是設定為0，則 [ **秒** ] 屬性會傳回正確的值。</span><span class="sxs-lookup"><span data-stu-id="dcbed-115">If the **Minutes** property is set to 0 instead, then the **Seconds** property returns the correct value.</span></span>

## <a name="examples"></a><span data-ttu-id="dcbed-116">範例</span><span class="sxs-lookup"><span data-stu-id="dcbed-116">Examples</span></span>

<span data-ttu-id="dcbed-117">如需使用 [**SWbemDateTime**](swbemdatetime.md) 物件將 CIM [**日期時間**](datetime.md) 值轉換成 **FILETIME** 格式或 **VT \_ 日期** 格式的範例，請參閱 [WMI 工作：日期和時間](wmi-tasks--dates-and-times.md)。</span><span class="sxs-lookup"><span data-stu-id="dcbed-117">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="dcbed-118">如需 CIM **DATETIME** 格式的說明，請參閱 [日期和時間格式](date-and-time-format.md)。</span><span class="sxs-lookup"><span data-stu-id="dcbed-118">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dcbed-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="dcbed-119">Requirements</span></span>



| <span data-ttu-id="dcbed-120">需求</span><span class="sxs-lookup"><span data-stu-id="dcbed-120">Requirement</span></span> | <span data-ttu-id="dcbed-121">值</span><span class="sxs-lookup"><span data-stu-id="dcbed-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dcbed-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dcbed-122">Minimum supported client</span></span><br/> | <span data-ttu-id="dcbed-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dcbed-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dcbed-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dcbed-124">Minimum supported server</span></span><br/> | <span data-ttu-id="dcbed-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dcbed-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dcbed-126">標頭</span><span class="sxs-lookup"><span data-stu-id="dcbed-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="dcbed-127"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="dcbed-127"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="dcbed-128">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="dcbed-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="dcbed-129"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="dcbed-129"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="dcbed-130">DLL</span><span class="sxs-lookup"><span data-stu-id="dcbed-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dcbed-131"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dcbed-131"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="dcbed-132">CLSID</span><span class="sxs-lookup"><span data-stu-id="dcbed-132">CLSID</span></span><br/>                    | <span data-ttu-id="dcbed-133">CLSID \_ SWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="dcbed-133">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="dcbed-134">IID</span><span class="sxs-lookup"><span data-stu-id="dcbed-134">IID</span></span><br/>                      | <span data-ttu-id="dcbed-135">IID \_ ISWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="dcbed-135">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="dcbed-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dcbed-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcbed-137">**SWbemDateTime.MinutesSpecified**</span><span class="sxs-lookup"><span data-stu-id="dcbed-137">**SWbemDateTime.MinutesSpecified**</span></span>](swbemdatetime-minutesspecified.md)
</dt> <dt>

[<span data-ttu-id="dcbed-138">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="dcbed-138">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="dcbed-139">**Datetime**</span><span class="sxs-lookup"><span data-stu-id="dcbed-139">**DATETIME**</span></span>](datetime.md)
</dt> </dl>

 

