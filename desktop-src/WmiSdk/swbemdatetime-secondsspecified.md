---
description: 指出 CIM 日期時間值中的秒陣列件是否包含間隔或萬用字元值的布林值。
ms.assetid: 9f9b75c3-ae08-49a6-b747-294831601a62
ms.tgt_platform: multiple
title: 'SWbemDateTime. SecondsSpecified 屬性 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.SecondsSpecified
- ISWbemDateTime.SecondsSpecified
- ISWbemDateTime.get_SecondsSpecified
- ISWbemDateTime.put_SecondsSpecified
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: e0cf97eff544d6e244890014108506f39b1934b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852272"
---
# <a name="swbemdatetimesecondsspecified-property"></a><span data-ttu-id="1e2a4-103">SWbemDateTime. SecondsSpecified 屬性</span><span class="sxs-lookup"><span data-stu-id="1e2a4-103">SWbemDateTime.SecondsSpecified property</span></span>

<span data-ttu-id="1e2a4-104">[**SWbemDateTime**](swbemdatetime.md)物件的 **SecondsSpecified** 屬性是一個布林值，指出 CIM [**DATETIME**](datetime.md)值中的秒陣列件是否包含間隔或萬用字元值。</span><span class="sxs-lookup"><span data-stu-id="1e2a4-104">The **SecondsSpecified** property of the [**SWbemDateTime**](swbemdatetime.md) object is a Boolean value that indicates whether the seconds component in the CIM [**DATETIME**](datetime.md) value contains an interval or a wildcard value.</span></span> <span data-ttu-id="1e2a4-105">如果 **SecondsSpecified** 為 **TRUE** 且 [**IsInterval**](swbemdatetime-isinterval.md) 為 **FALSE**，則 [**SWbemDateTime**](swbemdatetime-seconds.md) 會包含日期值。</span><span class="sxs-lookup"><span data-stu-id="1e2a4-105">If **SecondsSpecified** is **TRUE** and [**IsInterval**](swbemdatetime-isinterval.md) is **FALSE**, then [**SWbemDateTime.Seconds**](swbemdatetime-seconds.md) contains a date value.</span></span> <span data-ttu-id="1e2a4-106">包含間隔的日期時間值不能轉換成 **VT \_ 日期** 格式或 **FILETIME** 格式。</span><span class="sxs-lookup"><span data-stu-id="1e2a4-106">A datetime value that contains an interval cannot be converted into either the **VT\_DATE** format or the **FILETIME** format.</span></span> <span data-ttu-id="1e2a4-107">如果 **SecondsSpecified** 為 **FALSE** 且 **IsInterval** 為 **TRUE**，則 **SWbemDateTime** 會包含間隔。</span><span class="sxs-lookup"><span data-stu-id="1e2a4-107">If **SecondsSpecified** is **FALSE** and **IsInterval** is **TRUE**, then **SWbemDateTime.Seconds** contains an interval.</span></span>

<span data-ttu-id="1e2a4-108">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="1e2a4-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="1e2a4-109">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="1e2a4-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e2a4-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="1e2a4-110">Syntax</span></span>


```VB
SWbemDateTime.SecondsSpecified As Boolean
```



## <a name="property-value"></a><span data-ttu-id="1e2a4-111">屬性值</span><span class="sxs-lookup"><span data-stu-id="1e2a4-111">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="1e2a4-112">範例</span><span class="sxs-lookup"><span data-stu-id="1e2a4-112">Examples</span></span>

<span data-ttu-id="1e2a4-113">如需使用 [**SWbemDateTime**](swbemdatetime.md) 物件將 CIM [**日期時間**](datetime.md) 值轉換成 **FILETIME** 格式或 **VT \_ 日期** 格式的範例，請參閱 [WMI 工作：日期和時間](wmi-tasks--dates-and-times.md)。</span><span class="sxs-lookup"><span data-stu-id="1e2a4-113">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="1e2a4-114">如需 CIM **DATETIME** 格式的說明，請參閱 [日期和時間格式](date-and-time-format.md)。</span><span class="sxs-lookup"><span data-stu-id="1e2a4-114">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1e2a4-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="1e2a4-115">Requirements</span></span>



| <span data-ttu-id="1e2a4-116">需求</span><span class="sxs-lookup"><span data-stu-id="1e2a4-116">Requirement</span></span> | <span data-ttu-id="1e2a4-117">值</span><span class="sxs-lookup"><span data-stu-id="1e2a4-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1e2a4-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1e2a4-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1e2a4-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1e2a4-119">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1e2a4-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1e2a4-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1e2a4-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1e2a4-121">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1e2a4-122">標頭</span><span class="sxs-lookup"><span data-stu-id="1e2a4-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e2a4-123"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="1e2a4-123"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="1e2a4-124">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="1e2a4-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="1e2a4-125"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="1e2a4-125"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="1e2a4-126">DLL</span><span class="sxs-lookup"><span data-stu-id="1e2a4-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e2a4-127"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e2a4-127"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="1e2a4-128">CLSID</span><span class="sxs-lookup"><span data-stu-id="1e2a4-128">CLSID</span></span><br/>                    | <span data-ttu-id="1e2a4-129">CLSID \_ SWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="1e2a4-129">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="1e2a4-130">IID</span><span class="sxs-lookup"><span data-stu-id="1e2a4-130">IID</span></span><br/>                      | <span data-ttu-id="1e2a4-131">IID \_ ISWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="1e2a4-131">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="1e2a4-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1e2a4-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e2a4-133">**SWbemDateTime。秒數**</span><span class="sxs-lookup"><span data-stu-id="1e2a4-133">**SWbemDateTime.Seconds**</span></span>](swbemdatetime-seconds.md)
</dt> <dt>

[<span data-ttu-id="1e2a4-134">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="1e2a4-134">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="1e2a4-135">Datetime</span><span class="sxs-lookup"><span data-stu-id="1e2a4-135">DATETIME</span></span>](datetime.md)
</dt> </dl>

 

 




