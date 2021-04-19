---
description: 布林值，指出 CIM 日期時間值中的通用協調時間 (UTC) 元件是否包含間隔或萬用字元值。
ms.assetid: 9cb04351-294b-48ba-8d1c-2f28cb9ce463
ms.tgt_platform: multiple
title: 'SWbemDateTime. UTCSpecified 屬性 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.UTCSpecified
- ISWbemDateTime.UTCSpecified
- ISWbemDateTime.get_UTCSpecified
- ISWbemDateTime.put_UTCSpecified
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: e2ada5bbbfa68e6cb63c0e060d6c3a12c0f771a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980538"
---
# <a name="swbemdatetimeutcspecified-property"></a><span data-ttu-id="6af71-103">SWbemDateTime. UTCSpecified 屬性</span><span class="sxs-lookup"><span data-stu-id="6af71-103">SWbemDateTime.UTCSpecified property</span></span>

<span data-ttu-id="6af71-104">[**SWbemDateTime**](swbemdatetime.md)物件的 **UTCSpecified** 屬性是一個布林值，指出 CIM 日期時間值中的國際座標時間 (UTC) 元件是否包含間隔或萬用字元值。</span><span class="sxs-lookup"><span data-stu-id="6af71-104">The **UTCSpecified** property of the [**SWbemDateTime**](swbemdatetime.md) object is a Boolean value that indicates whether the Universal Coordinated Time (UTC) component in the CIM datetime value contains an interval or a wildcard value.</span></span> <span data-ttu-id="6af71-105">如果 **UTCSpecified** 為 **TRUE** 且 [**IsInterval**](swbemdatetime-isinterval.md) 為 **FALSE**，則 [**SWbemDateTime. UTC**](swbemdatetime-utc.md) 會包含 [**日期時間**](datetime.md) 值。</span><span class="sxs-lookup"><span data-stu-id="6af71-105">If **UTCSpecified** is **TRUE** and [**IsInterval**](swbemdatetime-isinterval.md) is **FALSE**, then [**SWbemDateTime.UTC**](swbemdatetime-utc.md) contains a [**DATETIME**](datetime.md) value.</span></span> <span data-ttu-id="6af71-106">包含間隔的 **日期時間** 值不能轉換成 **VT \_ 日期** 格式或 **FILETIME** 格式。</span><span class="sxs-lookup"><span data-stu-id="6af71-106">A **DATETIME** value that contains an interval cannot be converted into either the **VT\_DATE** format or the **FILETIME** format.</span></span> <span data-ttu-id="6af71-107">如果 **UTCSpecified** 為 **FALSE** 且 **IsInterval** 為 **TRUE**，則 **SWbemDateTime. UTC** 包含間隔。</span><span class="sxs-lookup"><span data-stu-id="6af71-107">If **UTCSpecified** is **FALSE** and **IsInterval** is **TRUE**, then **SWbemDateTime.UTC** contains an interval.</span></span>

<span data-ttu-id="6af71-108">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="6af71-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="6af71-109">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="6af71-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6af71-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="6af71-110">Syntax</span></span>


```VB
SWbemDateTime.UTCSpecified As Boolean
```



## <a name="property-value"></a><span data-ttu-id="6af71-111">屬性值</span><span class="sxs-lookup"><span data-stu-id="6af71-111">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="6af71-112">範例</span><span class="sxs-lookup"><span data-stu-id="6af71-112">Examples</span></span>

<span data-ttu-id="6af71-113">如需使用 [**SWbemDateTime**](swbemdatetime.md) 物件將 CIM [**日期時間**](datetime.md) 值轉換成 **FILETIME** 格式或 **VT \_ 日期** 格式的範例，請參閱 [WMI 工作：日期和時間](wmi-tasks--dates-and-times.md)。</span><span class="sxs-lookup"><span data-stu-id="6af71-113">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="6af71-114">如需 CIM datetime 格式的說明，請參閱 [日期和時間格式](date-and-time-format.md)。</span><span class="sxs-lookup"><span data-stu-id="6af71-114">For a description of the CIM datetime format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6af71-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="6af71-115">Requirements</span></span>



| <span data-ttu-id="6af71-116">需求</span><span class="sxs-lookup"><span data-stu-id="6af71-116">Requirement</span></span> | <span data-ttu-id="6af71-117">值</span><span class="sxs-lookup"><span data-stu-id="6af71-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6af71-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6af71-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6af71-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6af71-119">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6af71-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6af71-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6af71-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6af71-121">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6af71-122">標頭</span><span class="sxs-lookup"><span data-stu-id="6af71-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="6af71-123"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="6af71-123"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="6af71-124">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="6af71-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="6af71-125"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6af71-125"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6af71-126">DLL</span><span class="sxs-lookup"><span data-stu-id="6af71-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6af71-127"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6af71-127"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="6af71-128">CLSID</span><span class="sxs-lookup"><span data-stu-id="6af71-128">CLSID</span></span><br/>                    | <span data-ttu-id="6af71-129">CLSID \_ SWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="6af71-129">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="6af71-130">IID</span><span class="sxs-lookup"><span data-stu-id="6af71-130">IID</span></span><br/>                      | <span data-ttu-id="6af71-131">IID \_ ISWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="6af71-131">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="6af71-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6af71-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6af71-133">**SWbemDateTime UTC**</span><span class="sxs-lookup"><span data-stu-id="6af71-133">**SWbemDateTime.UTC**</span></span>](swbemdatetime-utc.md)
</dt> <dt>

[<span data-ttu-id="6af71-134">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="6af71-134">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="6af71-135">Datetime</span><span class="sxs-lookup"><span data-stu-id="6af71-135">DATETIME</span></span>](datetime.md)
</dt> </dl>

 

 




