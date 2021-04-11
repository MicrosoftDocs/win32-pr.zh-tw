---
description: 取得或設定值，這個值表示 datetime 值的小時元件。
ms.assetid: 83f084fa-57a5-4467-acea-7e19de82a91f
ms.tgt_platform: multiple
title: 'SWbemDateTime Hours 屬性 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Hours
- ISWbemDateTime.Hours
- ISWbemDateTime.get_Hours
- ISWbemDateTime.put_Hours
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 27edb3c209e2e95ae7aff20930d260f8f6d44427
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194695"
---
# <a name="swbemdatetimehours-property"></a><span data-ttu-id="88895-103">SWbemDateTime Hours 屬性</span><span class="sxs-lookup"><span data-stu-id="88895-103">SWbemDateTime.Hours property</span></span>

<span data-ttu-id="88895-104">[**SWbemDateTime**](swbemdatetime.md)物件的 **hours** 屬性會取得或設定值，這個值表示 datetime 值的小時元件。</span><span class="sxs-lookup"><span data-stu-id="88895-104">The **Hours** property of the [**SWbemDateTime**](swbemdatetime.md) object gets or sets a value that represents the hours component of the datetime value.</span></span>

<span data-ttu-id="88895-105">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="88895-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="88895-106">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="88895-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="88895-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="88895-107">Syntax</span></span>


```VB
SWbemDateTime.Hours As Long
```



## <a name="property-value"></a><span data-ttu-id="88895-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="88895-108">Property value</span></span>

## <a name="error-codes"></a><span data-ttu-id="88895-109">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="88895-109">Error codes</span></span>

<span data-ttu-id="88895-110">當您取得或設定 **Hours** 屬性之後， [Err](/previous-versions//sbf5ze0e(v=vs.85)) 物件可能會包含下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="88895-110">After you get or set the **Hours** property, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="88895-111">**wbemErrValueOutOfRange** -2147749931 (0x8004102B) </span><span class="sxs-lookup"><span data-stu-id="88895-111">**wbemErrValueOutOfRange** - 2147749931 (0x8004102B)</span></span>
</dt> <dd>

<span data-ttu-id="88895-112">值不在0到23的範圍內。</span><span class="sxs-lookup"><span data-stu-id="88895-112">The value was not in the range of 0 through 23.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="88895-113">範例</span><span class="sxs-lookup"><span data-stu-id="88895-113">Examples</span></span>

<span data-ttu-id="88895-114">如需使用 [**SWbemDateTime**](swbemdatetime.md) 物件將 CIM [**日期時間**](datetime.md) 值轉換成 **FILETIME** 格式或 **VT \_ 日期** 格式的範例，請參閱 [WMI 工作：日期和時間](wmi-tasks--dates-and-times.md)。</span><span class="sxs-lookup"><span data-stu-id="88895-114">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="88895-115">如需 CIM **DATETIME** 格式的說明，請參閱 [日期和時間格式](date-and-time-format.md)。</span><span class="sxs-lookup"><span data-stu-id="88895-115">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="88895-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="88895-116">Requirements</span></span>



| <span data-ttu-id="88895-117">需求</span><span class="sxs-lookup"><span data-stu-id="88895-117">Requirement</span></span> | <span data-ttu-id="88895-118">值</span><span class="sxs-lookup"><span data-stu-id="88895-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="88895-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="88895-119">Minimum supported client</span></span><br/> | <span data-ttu-id="88895-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="88895-120">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="88895-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="88895-121">Minimum supported server</span></span><br/> | <span data-ttu-id="88895-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="88895-122">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="88895-123">標頭</span><span class="sxs-lookup"><span data-stu-id="88895-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="88895-124"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="88895-124"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="88895-125">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="88895-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="88895-126"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="88895-126"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="88895-127">DLL</span><span class="sxs-lookup"><span data-stu-id="88895-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="88895-128"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="88895-128"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="88895-129">CLSID</span><span class="sxs-lookup"><span data-stu-id="88895-129">CLSID</span></span><br/>                    | <span data-ttu-id="88895-130">CLSID \_ SWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="88895-130">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="88895-131">IID</span><span class="sxs-lookup"><span data-stu-id="88895-131">IID</span></span><br/>                      | <span data-ttu-id="88895-132">IID \_ ISWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="88895-132">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="88895-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="88895-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88895-134">**SWbemDateTime.HoursSpecified**</span><span class="sxs-lookup"><span data-stu-id="88895-134">**SWbemDateTime.HoursSpecified**</span></span>](swbemdatetime-hoursspecified.md)
</dt> <dt>

[<span data-ttu-id="88895-135">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="88895-135">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="88895-136">**Datetime**</span><span class="sxs-lookup"><span data-stu-id="88895-136">**DATETIME**</span></span>](datetime.md)
</dt> </dl>

 

