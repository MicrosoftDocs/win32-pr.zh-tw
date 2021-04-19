---
description: 取得或設定日期時間值的國際標準時間 (UTC) 標記法。
ms.assetid: 43d9d0c8-5521-410f-825b-6b00c3dd0039
ms.tgt_platform: multiple
title: 'SWbemDateTime. UTC 屬性 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.UTC
- ISWbemDateTime.UTC
- ISWbemDateTime.get_UTC
- ISWbemDateTime.put_UTC
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 80a4c32e47b94289f66999fdbf1f7daf5f9f03cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106998477"
---
# <a name="swbemdatetimeutc-property"></a><span data-ttu-id="f29fc-103">SWbemDateTime UTC 屬性</span><span class="sxs-lookup"><span data-stu-id="f29fc-103">SWbemDateTime.UTC property</span></span>

<span data-ttu-id="f29fc-104">[**SWbemDateTime**](swbemdatetime.md)物件的 **utc** 屬性會取得或設定 **日期時間** 值的國際標準時間 (utc) 標記法。</span><span class="sxs-lookup"><span data-stu-id="f29fc-104">The **UTC** property of the [**SWbemDateTime**](swbemdatetime.md) object gets or sets the Coordinated Universal Times (UTC) representation of the **datetime** value.</span></span> <span data-ttu-id="f29fc-105">UTC 是由世界時間標準所設定的時間。</span><span class="sxs-lookup"><span data-stu-id="f29fc-105">UTC is the time as set by the World Time Standard.</span></span> <span data-ttu-id="f29fc-106">UTC 已更換格林尼治平均時間 (GMT) 。</span><span class="sxs-lookup"><span data-stu-id="f29fc-106">UTC has replaced Greenwich Mean Time (GMT).</span></span> <span data-ttu-id="f29fc-107">具有零位移的 UTC 值與 GMT 的值相同，且具有零位移。</span><span class="sxs-lookup"><span data-stu-id="f29fc-107">A UTC value with a zero offset is the same as GMT with a zero offset.</span></span> <span data-ttu-id="f29fc-108">帶正負號的數位必須在-720 到720的範圍內，否則會傳回錯誤 **wbemErrValueOutOfRange** 。</span><span class="sxs-lookup"><span data-stu-id="f29fc-108">The signed number must be in the range of -720 through 720 or the error **wbemErrValueOutOfRange** is returned.</span></span>

<span data-ttu-id="f29fc-109">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="f29fc-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="f29fc-110">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="f29fc-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f29fc-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="f29fc-111">Syntax</span></span>


```VB
SWbemDateTime.UTC As Long
```



## <a name="property-value"></a><span data-ttu-id="f29fc-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="f29fc-112">Property value</span></span>

## <a name="error-codes"></a><span data-ttu-id="f29fc-113">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="f29fc-113">Error codes</span></span>

<span data-ttu-id="f29fc-114">取得或設定 **UTC** 屬性之後， [Err](/previous-versions//sbf5ze0e(v=vs.85)) 物件可能會包含下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f29fc-114">After you get or set the **UTC** property, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="f29fc-115">**wbemErrValueOutOfRange** -2147749931 (0x8004102B) </span><span class="sxs-lookup"><span data-stu-id="f29fc-115">**wbemErrValueOutOfRange** - 2147749931 (0x8004102B)</span></span>
</dt> <dd>

<span data-ttu-id="f29fc-116">值不在-720 到720的範圍內。</span><span class="sxs-lookup"><span data-stu-id="f29fc-116">The value was not in the range of -720 through 720.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="f29fc-117">範例</span><span class="sxs-lookup"><span data-stu-id="f29fc-117">Examples</span></span>

<span data-ttu-id="f29fc-118">如需使用 [**SWbemDateTime**](swbemdatetime.md) 物件將 CIM [**日期時間**](datetime.md) 值轉換成 **FILETIME** 格式或 **VT \_ 日期** 格式的範例，請參閱 [WMI 工作：日期和時間](wmi-tasks--dates-and-times.md)。</span><span class="sxs-lookup"><span data-stu-id="f29fc-118">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="f29fc-119">如需 CIM **DATETIME** 格式的說明，請參閱 [日期和時間格式](date-and-time-format.md)。</span><span class="sxs-lookup"><span data-stu-id="f29fc-119">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f29fc-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="f29fc-120">Requirements</span></span>



| <span data-ttu-id="f29fc-121">需求</span><span class="sxs-lookup"><span data-stu-id="f29fc-121">Requirement</span></span> | <span data-ttu-id="f29fc-122">值</span><span class="sxs-lookup"><span data-stu-id="f29fc-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f29fc-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f29fc-123">Minimum supported client</span></span><br/> | <span data-ttu-id="f29fc-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f29fc-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f29fc-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f29fc-125">Minimum supported server</span></span><br/> | <span data-ttu-id="f29fc-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f29fc-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f29fc-127">標頭</span><span class="sxs-lookup"><span data-stu-id="f29fc-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="f29fc-128"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="f29fc-128"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="f29fc-129">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="f29fc-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="f29fc-130"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f29fc-130"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f29fc-131">DLL</span><span class="sxs-lookup"><span data-stu-id="f29fc-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f29fc-132"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f29fc-132"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="f29fc-133">CLSID</span><span class="sxs-lookup"><span data-stu-id="f29fc-133">CLSID</span></span><br/>                    | <span data-ttu-id="f29fc-134">CLSID \_ SWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="f29fc-134">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="f29fc-135">IID</span><span class="sxs-lookup"><span data-stu-id="f29fc-135">IID</span></span><br/>                      | <span data-ttu-id="f29fc-136">IID \_ ISWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="f29fc-136">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="f29fc-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f29fc-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f29fc-138">**SWbemDateTime.UTCSpecified**</span><span class="sxs-lookup"><span data-stu-id="f29fc-138">**SWbemDateTime.UTCSpecified**</span></span>](swbemdatetime-utcspecified.md)
</dt> <dt>

[<span data-ttu-id="f29fc-139">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="f29fc-139">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="f29fc-140">**Datetime**</span><span class="sxs-lookup"><span data-stu-id="f29fc-140">**DATETIME**</span></span>](datetime.md)
</dt> </dl>

 

