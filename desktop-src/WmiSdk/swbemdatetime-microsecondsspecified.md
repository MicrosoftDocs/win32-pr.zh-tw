---
description: 布林值，指出 CIM 日期時間值中的微秒元件是否包含間隔或萬用字元值。
ms.assetid: 65244ece-2326-4edc-b982-57e2046ec33e
ms.tgt_platform: multiple
title: 'SWbemDateTime. MicrosecondsSpecified 屬性 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.MicrosecondsSpecified
- ISWbemDateTime.MicrosecondsSpecified
- ISWbemDateTime.get_MicrosecondsSpecified
- ISWbemDateTime.put_MicrosecondsSpecified
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: d4fa9d99cf323e19ccd298786896f789bbb08be6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974190"
---
# <a name="swbemdatetimemicrosecondsspecified-property"></a><span data-ttu-id="c37ca-103">SWbemDateTime. MicrosecondsSpecified 屬性</span><span class="sxs-lookup"><span data-stu-id="c37ca-103">SWbemDateTime.MicrosecondsSpecified property</span></span>

<span data-ttu-id="c37ca-104">[**SWbemDateTime**](swbemdatetime.md)物件的 **MicrosecondsSpecified** 屬性是一個布林值，指出 CIM datetime 值中的微秒元件是否包含間隔或萬用字元值。</span><span class="sxs-lookup"><span data-stu-id="c37ca-104">The **MicrosecondsSpecified** property of the [**SWbemDateTime**](swbemdatetime.md) object is a Boolean value that indicates whether the microseconds component in the CIM datetime value contains an interval or a wildcard value.</span></span> <span data-ttu-id="c37ca-105">如果 **MicrosecondsSpecified** 為 **TRUE** 且 [**IsInterval**](swbemdatetime-isinterval.md) 為 **FALSE**，則 [**SWbemDateTime**](swbemdatetime-microseconds.md) 會包含日期時間值。</span><span class="sxs-lookup"><span data-stu-id="c37ca-105">If **MicrosecondsSpecified** is **TRUE** and [**IsInterval**](swbemdatetime-isinterval.md) is **FALSE**, then [**SWbemDateTime.Microseconds**](swbemdatetime-microseconds.md) contains a datetime value.</span></span> <span data-ttu-id="c37ca-106">包含間隔的日期時間值不能轉換成 **VT \_ 日期** 格式或 **FILETIME** 格式。</span><span class="sxs-lookup"><span data-stu-id="c37ca-106">A datetime value that contains an interval cannot be converted into either the **VT\_DATE** format or the **FILETIME** format.</span></span> <span data-ttu-id="c37ca-107">如果 [**HoursSpecified**](swbemdatetime-hoursspecified.md) 為 **FALSE** 且 **IsInterval** 為 **TRUE**，則 **SWbemDateTime** 會包含間隔。</span><span class="sxs-lookup"><span data-stu-id="c37ca-107">If [**HoursSpecified**](swbemdatetime-hoursspecified.md) is **FALSE** and **IsInterval** is **TRUE**, then **SWbemDateTime.Microseconds** contains an interval.</span></span>

<span data-ttu-id="c37ca-108">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="c37ca-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="c37ca-109">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="c37ca-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="c37ca-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="c37ca-110">Syntax</span></span>


```VB
SWbemDateTime.MicrosecondsSpecified As Boolean
```



## <a name="property-value"></a><span data-ttu-id="c37ca-111">屬性值</span><span class="sxs-lookup"><span data-stu-id="c37ca-111">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="c37ca-112">範例</span><span class="sxs-lookup"><span data-stu-id="c37ca-112">Examples</span></span>

<span data-ttu-id="c37ca-113">如需使用 [**SWbemDateTime**](swbemdatetime.md) 物件將 CIM [**日期時間**](datetime.md) 值轉換成 **FILETIME** 格式或 **VT \_ 日期** 格式的範例，請參閱 [WMI 工作：日期和時間](wmi-tasks--dates-and-times.md)。</span><span class="sxs-lookup"><span data-stu-id="c37ca-113">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="c37ca-114">如需 CIM **DATETIME** 格式的說明，請參閱 [日期和時間格式](date-and-time-format.md)。</span><span class="sxs-lookup"><span data-stu-id="c37ca-114">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c37ca-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="c37ca-115">Requirements</span></span>



| <span data-ttu-id="c37ca-116">需求</span><span class="sxs-lookup"><span data-stu-id="c37ca-116">Requirement</span></span> | <span data-ttu-id="c37ca-117">值</span><span class="sxs-lookup"><span data-stu-id="c37ca-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c37ca-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c37ca-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c37ca-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c37ca-119">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c37ca-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c37ca-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c37ca-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c37ca-121">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c37ca-122">標頭</span><span class="sxs-lookup"><span data-stu-id="c37ca-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c37ca-123"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="c37ca-123"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c37ca-124">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="c37ca-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="c37ca-125"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c37ca-125"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c37ca-126">DLL</span><span class="sxs-lookup"><span data-stu-id="c37ca-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c37ca-127"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c37ca-127"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="c37ca-128">CLSID</span><span class="sxs-lookup"><span data-stu-id="c37ca-128">CLSID</span></span><br/>                    | <span data-ttu-id="c37ca-129">CLSID \_ SWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="c37ca-129">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="c37ca-130">IID</span><span class="sxs-lookup"><span data-stu-id="c37ca-130">IID</span></span><br/>                      | <span data-ttu-id="c37ca-131">IID \_ ISWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="c37ca-131">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="c37ca-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c37ca-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c37ca-133">**SWbemDateTime 微秒**</span><span class="sxs-lookup"><span data-stu-id="c37ca-133">**SWbemDateTime.Microseconds**</span></span>](swbemdatetime-microseconds.md)
</dt> <dt>

[<span data-ttu-id="c37ca-134">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="c37ca-134">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="c37ca-135">Datetime</span><span class="sxs-lookup"><span data-stu-id="c37ca-135">DATETIME</span></span>](datetime.md)
</dt> </dl>

 

 




