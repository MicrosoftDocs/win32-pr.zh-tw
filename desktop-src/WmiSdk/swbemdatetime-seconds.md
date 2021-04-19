---
description: 取得或設定值，這個值表示 datetime 值的秒陣列件。
ms.assetid: 194d4309-6abf-4c5f-99f8-60d2c835af6c
ms.tgt_platform: multiple
title: 'SWbemDateTime： Seconds 屬性 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Seconds
- ISWbemDateTime.Seconds
- ISWbemDateTime.get_Seconds
- ISWbemDateTime.put_Seconds
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 0ef4ef15f13bf3d8dfc9272b2a3b734c3678f8e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106993053"
---
# <a name="swbemdatetimeseconds-property"></a><span data-ttu-id="22879-103">SWbemDateTime. Seconds 屬性</span><span class="sxs-lookup"><span data-stu-id="22879-103">SWbemDateTime.Seconds property</span></span>

<span data-ttu-id="22879-104">[**SWbemDateTime**](swbemdatetime.md)物件的 **seconds** 屬性會取得或設定值，這個值表示 datetime 值的秒陣列件。</span><span class="sxs-lookup"><span data-stu-id="22879-104">The **Seconds** property of the [**SWbemDateTime**](swbemdatetime.md) object gets or sets a value that represents the seconds component of the datetime value.</span></span>

<span data-ttu-id="22879-105">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="22879-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="22879-106">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="22879-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="22879-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="22879-107">Syntax</span></span>


```VB
SWbemDateTime.Seconds As Long
```



## <a name="property-value"></a><span data-ttu-id="22879-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="22879-108">Property value</span></span>

## <a name="error-codes"></a><span data-ttu-id="22879-109">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="22879-109">Error codes</span></span>

<span data-ttu-id="22879-110">當您取得或設定 **Seconds** 屬性之後， [Err](/previous-versions//sbf5ze0e(v=vs.85)) 物件可能會包含下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="22879-110">After you get or set the **Seconds** property, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="22879-111">**wbemErrValueOutOfRange** -2147749931 (0x8004102B) </span><span class="sxs-lookup"><span data-stu-id="22879-111">**wbemErrValueOutOfRange** - 2147749931 (0x8004102B)</span></span>
</dt> <dd>

<span data-ttu-id="22879-112">值不在0到59的範圍內。</span><span class="sxs-lookup"><span data-stu-id="22879-112">The value was not in the range of 0 through 59.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="22879-113">備註</span><span class="sxs-lookup"><span data-stu-id="22879-113">Remarks</span></span>

<span data-ttu-id="22879-114">如果 [**SWbemDateTime. 分鐘**](swbemdatetime-minutes.md)屬性已設定為1，則 **SWbemDateTime** 的屬性可能會包含不正確的值。</span><span class="sxs-lookup"><span data-stu-id="22879-114">The **SWbemDateTime.Seconds** property may contain an incorrect value if the [**SWbemDateTime.Minutes**](swbemdatetime-minutes.md) property has been set to 1.</span></span> <span data-ttu-id="22879-115">它包含的值會位移1秒，因為 CIM [**DATETIME**](datetime.md) 值轉譯成 **VT \_ 日期** 值時，會發生舍入錯誤。</span><span class="sxs-lookup"><span data-stu-id="22879-115">It contains a value that is offset by one second because of a rounding error that occurs when a CIM [**DATETIME**](datetime.md) value is translated to a **VT\_DATE** value.</span></span> <span data-ttu-id="22879-116">如果 [ **分鐘** ] 屬性設定為 0 (零) ，則 [ **秒** ] 屬性會傳回正確的值。</span><span class="sxs-lookup"><span data-stu-id="22879-116">If the **Minutes** property is set to 0 (zero) instead, then the **Seconds** property returns the correct value.</span></span>

## <a name="examples"></a><span data-ttu-id="22879-117">範例</span><span class="sxs-lookup"><span data-stu-id="22879-117">Examples</span></span>

<span data-ttu-id="22879-118">如需使用 [**SWbemDateTime**](swbemdatetime.md) 物件將 CIM [**日期時間**](datetime.md) 值轉換成 **FILETIME** 格式或 **VT \_ 日期** 格式的範例，請參閱 [WMI 工作：日期和時間](wmi-tasks--dates-and-times.md)。</span><span class="sxs-lookup"><span data-stu-id="22879-118">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="22879-119">如需 CIM **DATETIME** 格式的說明，請參閱 [日期和時間格式](date-and-time-format.md)。</span><span class="sxs-lookup"><span data-stu-id="22879-119">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="22879-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="22879-120">Requirements</span></span>



| <span data-ttu-id="22879-121">需求</span><span class="sxs-lookup"><span data-stu-id="22879-121">Requirement</span></span> | <span data-ttu-id="22879-122">值</span><span class="sxs-lookup"><span data-stu-id="22879-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="22879-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="22879-123">Minimum supported client</span></span><br/> | <span data-ttu-id="22879-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="22879-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="22879-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="22879-125">Minimum supported server</span></span><br/> | <span data-ttu-id="22879-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="22879-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="22879-127">標頭</span><span class="sxs-lookup"><span data-stu-id="22879-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="22879-128"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="22879-128"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="22879-129">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="22879-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="22879-130"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="22879-130"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="22879-131">DLL</span><span class="sxs-lookup"><span data-stu-id="22879-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="22879-132"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22879-132"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="22879-133">CLSID</span><span class="sxs-lookup"><span data-stu-id="22879-133">CLSID</span></span><br/>                    | <span data-ttu-id="22879-134">CLSID \_ SWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="22879-134">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="22879-135">IID</span><span class="sxs-lookup"><span data-stu-id="22879-135">IID</span></span><br/>                      | <span data-ttu-id="22879-136">IID \_ ISWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="22879-136">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="22879-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="22879-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22879-138">**SWbemDateTime.SecondsSpecified**</span><span class="sxs-lookup"><span data-stu-id="22879-138">**SWbemDateTime.SecondsSpecified**</span></span>](swbemdatetime-secondsspecified.md)
</dt> <dt>

[<span data-ttu-id="22879-139">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="22879-139">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="22879-140">**Datetime**</span><span class="sxs-lookup"><span data-stu-id="22879-140">**DATETIME**</span></span>](datetime.md)
</dt> </dl>

 

