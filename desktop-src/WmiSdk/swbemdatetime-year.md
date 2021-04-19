---
description: 取得或設定值，這個值表示日期時間值的年份元件。
ms.assetid: eab3738a-c92a-4602-b1ee-e2547da88308
ms.tgt_platform: multiple
title: 'SWbemDateTime Year 屬性 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Year
- ISWbemDateTime.Year
- ISWbemDateTime.get_Year
- ISWbemDateTime.put_Year
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 5fe8988b3772f0f5d976c38eb5e9cc44fb9c4ede
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988923"
---
# <a name="swbemdatetimeyear-property"></a><span data-ttu-id="d9145-103">SWbemDateTime Year 屬性</span><span class="sxs-lookup"><span data-stu-id="d9145-103">SWbemDateTime.Year property</span></span>

<span data-ttu-id="d9145-104">[**SWbemDateTime**](swbemdatetime.md)物件的 **year** 屬性會取得或設定值，這個值表示 [**DATETIME**](datetime.md)值的年份元件。</span><span class="sxs-lookup"><span data-stu-id="d9145-104">The **Year** property of the [**SWbemDateTime**](swbemdatetime.md) object gets or sets a value that represents the year component of the [**DATETIME**](datetime.md) value.</span></span> <span data-ttu-id="d9145-105">值必須在 0000-9999 的範圍內，否則會傳回錯誤 wbemErrValueOutOfRange。</span><span class="sxs-lookup"><span data-stu-id="d9145-105">The value must be in the range of 0000 - 9999 or the error wbemErrValueOutOfRange is returned.</span></span>

<span data-ttu-id="d9145-106">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="d9145-106">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="d9145-107">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="d9145-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9145-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d9145-108">Syntax</span></span>


```VB
SWbemDateTime.Year As Long
```



## <a name="property-value"></a><span data-ttu-id="d9145-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="d9145-109">Property value</span></span>

## <a name="error-codes"></a><span data-ttu-id="d9145-110">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="d9145-110">Error codes</span></span>

<span data-ttu-id="d9145-111">取得或設定 **Year** 屬性之後， [Err](/previous-versions//sbf5ze0e(v=vs.85)) 物件可能會包含下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d9145-111">After you get or set the **Year** property, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="d9145-112">**wbemErrValueOutOfRange** -2147749931 (0x8004102B) </span><span class="sxs-lookup"><span data-stu-id="d9145-112">**wbemErrValueOutOfRange** - 2147749931 (0x8004102B)</span></span>
</dt> <dd>

<span data-ttu-id="d9145-113">值不在0000到9999的範圍內。</span><span class="sxs-lookup"><span data-stu-id="d9145-113">The value was not in the range of 0000 through 9999.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="d9145-114">範例</span><span class="sxs-lookup"><span data-stu-id="d9145-114">Examples</span></span>

<span data-ttu-id="d9145-115">如需使用 [**SWbemDateTime**](swbemdatetime.md) 物件將 CIM [**日期時間**](datetime.md) 值轉換成 **FILETIME** 格式或 **VT \_ 日期** 格式的範例，請參閱 [WMI 工作：日期和時間](wmi-tasks--dates-and-times.md)。</span><span class="sxs-lookup"><span data-stu-id="d9145-115">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="d9145-116">如需 CIM **DATETIME** 格式的說明，請參閱 [日期和時間格式](date-and-time-format.md)。</span><span class="sxs-lookup"><span data-stu-id="d9145-116">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d9145-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="d9145-117">Requirements</span></span>



| <span data-ttu-id="d9145-118">需求</span><span class="sxs-lookup"><span data-stu-id="d9145-118">Requirement</span></span> | <span data-ttu-id="d9145-119">值</span><span class="sxs-lookup"><span data-stu-id="d9145-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d9145-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d9145-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d9145-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d9145-121">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d9145-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d9145-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d9145-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d9145-123">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d9145-124">標頭</span><span class="sxs-lookup"><span data-stu-id="d9145-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9145-125"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="d9145-125"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d9145-126">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="d9145-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="d9145-127"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d9145-127"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d9145-128">DLL</span><span class="sxs-lookup"><span data-stu-id="d9145-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d9145-129"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d9145-129"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="d9145-130">CLSID</span><span class="sxs-lookup"><span data-stu-id="d9145-130">CLSID</span></span><br/>                    | <span data-ttu-id="d9145-131">CLSID \_ SWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="d9145-131">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="d9145-132">IID</span><span class="sxs-lookup"><span data-stu-id="d9145-132">IID</span></span><br/>                      | <span data-ttu-id="d9145-133">IID \_ ISWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="d9145-133">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="d9145-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d9145-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9145-135">**SWbemDateTime.YearSpecified**</span><span class="sxs-lookup"><span data-stu-id="d9145-135">**SWbemDateTime.YearSpecified**</span></span>](swbemdatetime-yearspecified.md)
</dt> <dt>

[<span data-ttu-id="d9145-136">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="d9145-136">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="d9145-137">**Datetime**</span><span class="sxs-lookup"><span data-stu-id="d9145-137">**DATETIME**</span></span>](datetime.md)
</dt> </dl>

 

