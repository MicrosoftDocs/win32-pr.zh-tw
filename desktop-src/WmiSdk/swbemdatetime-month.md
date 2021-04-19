---
description: 取得或設定值，這個值表示日期時間值的月份元件。
ms.assetid: 05818f0a-7e15-4ddd-a6a7-9d16ae82cd3c
ms.tgt_platform: multiple
title: 'SWbemDateTime： Month 屬性 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Month
- ISWbemDateTime.Month
- ISWbemDateTime.get_Month
- ISWbemDateTime.put_Month
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 73769d73cffc5b9731cfd55785e2fa087182b33b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980704"
---
# <a name="swbemdatetimemonth-property"></a><span data-ttu-id="39c66-103">SWbemDateTime 月份屬性</span><span class="sxs-lookup"><span data-stu-id="39c66-103">SWbemDateTime.Month property</span></span>

<span data-ttu-id="39c66-104">[**SWbemDateTime**](swbemdatetime.md)物件的 **month** 屬性會取得或設定值，這個值表示 datetime 值的 month 元件。</span><span class="sxs-lookup"><span data-stu-id="39c66-104">The **Month** property of the [**SWbemDateTime**](swbemdatetime.md) object gets or sets a value that represents the month component of the datetime value.</span></span> <span data-ttu-id="39c66-105">此數位必須介於01到12的範圍內，否則會傳回錯誤 **wbemValueOutOfRange** 。</span><span class="sxs-lookup"><span data-stu-id="39c66-105">The number must be in the range of 01 through 12 or the error **wbemValueOutOfRange** is returned.</span></span>

<span data-ttu-id="39c66-106">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="39c66-106">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="39c66-107">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="39c66-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="39c66-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="39c66-108">Syntax</span></span>


```VB
SWbemDateTime.Month As Long
```



## <a name="property-value"></a><span data-ttu-id="39c66-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="39c66-109">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="39c66-110">範例</span><span class="sxs-lookup"><span data-stu-id="39c66-110">Examples</span></span>

<span data-ttu-id="39c66-111">如需使用 [**SWbemDateTime**](swbemdatetime.md) 物件將 CIM [**日期時間**](datetime.md) 值轉換成 **FILETIME** 格式或 **VT \_ 日期** 格式的範例，請參閱 [WMI 工作：日期和時間](wmi-tasks--dates-and-times.md)。</span><span class="sxs-lookup"><span data-stu-id="39c66-111">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="39c66-112">如需 CIM **DATETIME** 格式的說明，請參閱 [日期和時間格式](date-and-time-format.md)。</span><span class="sxs-lookup"><span data-stu-id="39c66-112">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="39c66-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="39c66-113">Requirements</span></span>



| <span data-ttu-id="39c66-114">需求</span><span class="sxs-lookup"><span data-stu-id="39c66-114">Requirement</span></span> | <span data-ttu-id="39c66-115">值</span><span class="sxs-lookup"><span data-stu-id="39c66-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="39c66-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="39c66-116">Minimum supported client</span></span><br/> | <span data-ttu-id="39c66-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="39c66-117">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="39c66-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="39c66-118">Minimum supported server</span></span><br/> | <span data-ttu-id="39c66-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="39c66-119">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="39c66-120">標頭</span><span class="sxs-lookup"><span data-stu-id="39c66-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="39c66-121"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="39c66-121"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="39c66-122">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="39c66-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="39c66-123"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="39c66-123"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="39c66-124">DLL</span><span class="sxs-lookup"><span data-stu-id="39c66-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39c66-125"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39c66-125"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="39c66-126">CLSID</span><span class="sxs-lookup"><span data-stu-id="39c66-126">CLSID</span></span><br/>                    | <span data-ttu-id="39c66-127">CLSID \_ SWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="39c66-127">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="39c66-128">IID</span><span class="sxs-lookup"><span data-stu-id="39c66-128">IID</span></span><br/>                      | <span data-ttu-id="39c66-129">IID \_ ISWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="39c66-129">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="39c66-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="39c66-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39c66-131">**SWbemDateTime.MonthSpecified**</span><span class="sxs-lookup"><span data-stu-id="39c66-131">**SWbemDateTime.MonthSpecified**</span></span>](swbemdatetime-monthspecified.md)
</dt> <dt>

[<span data-ttu-id="39c66-132">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="39c66-132">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="39c66-133">Datetime</span><span class="sxs-lookup"><span data-stu-id="39c66-133">DATETIME</span></span>](datetime.md)
</dt> </dl>

 

 




