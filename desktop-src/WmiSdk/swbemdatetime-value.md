---
description: 取得或設定 DMTF (分散式管理工作強制) 格式的原始 CIM 日期。
ms.assetid: 426a60d5-c364-406e-8346-049a13d59c7f
ms.tgt_platform: multiple
title: 'SWbemDateTime： Value 屬性 (>wbemdisp.tlb. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Value
- ISWbemDateTime.Value
- ISWbemDateTime.get_Value
- ISWbemDateTime.put_Value
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2ecb3a42a865559ba9b3c3e5fbec7302f975fa0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114876"
---
# <a name="swbemdatetimevalue-property"></a><span data-ttu-id="86e8a-103">SWbemDateTime。 Value 屬性</span><span class="sxs-lookup"><span data-stu-id="86e8a-103">SWbemDateTime.Value property</span></span>

<span data-ttu-id="86e8a-104">[**SWbemDateTime**](swbemdatetime.md)物件的 **Value** 屬性會取得或設定 DMTF (分散式管理工作強制) 格式的原始 CIM 日期。</span><span class="sxs-lookup"><span data-stu-id="86e8a-104">The **Value** property of the [**SWbemDateTime**](swbemdatetime.md) object gets or sets the raw CIM date in the DMTF (Distributed Management Task Force) format.</span></span> <span data-ttu-id="86e8a-105">DMTF 格式是 [**日期時間**](datetime.md) 值的字串表示。</span><span class="sxs-lookup"><span data-stu-id="86e8a-105">The DMTF format is a string representation of the [**DATETIME**](datetime.md) value.</span></span> <span data-ttu-id="86e8a-106">這個屬性是 **SWbemDateTime** 物件的預設屬性。</span><span class="sxs-lookup"><span data-stu-id="86e8a-106">This property is the default property for **SWbemDateTime** objects.</span></span> <span data-ttu-id="86e8a-107">**Value** 屬性的預設值為 00000101000000.000000 + 000。</span><span class="sxs-lookup"><span data-stu-id="86e8a-107">The **Value** property has a default value of 00000101000000.000000+000.</span></span>

<span data-ttu-id="86e8a-108">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="86e8a-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="86e8a-109">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="86e8a-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="86e8a-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="86e8a-110">Syntax</span></span>


```VB
SWbemDateTime.Value As String
```



## <a name="property-value"></a><span data-ttu-id="86e8a-111">屬性值</span><span class="sxs-lookup"><span data-stu-id="86e8a-111">Property value</span></span>

## <a name="error-codes"></a><span data-ttu-id="86e8a-112">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="86e8a-112">Error codes</span></span>

<span data-ttu-id="86e8a-113">當您取得或設定 **Value** 屬性之後， [Err](/previous-versions//sbf5ze0e(v=vs.85)) 物件可能會包含下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="86e8a-113">After you get or set the **Value** property, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="86e8a-114">**wbemErrInvalidSyntax** -2147749921 (0x80041021) </span><span class="sxs-lookup"><span data-stu-id="86e8a-114">**wbemErrInvalidSyntax** - 2147749921 (0x80041021)</span></span>
</dt> <dd>

<span data-ttu-id="86e8a-115">*StrValue* 的格式無效。</span><span class="sxs-lookup"><span data-stu-id="86e8a-115">The format of *strValue* is not valid.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="86e8a-116">範例</span><span class="sxs-lookup"><span data-stu-id="86e8a-116">Examples</span></span>

<span data-ttu-id="86e8a-117">如需使用 [**SWbemDateTime**](swbemdatetime.md) 物件將 CIM [**日期時間**](datetime.md) 值轉換成 **FILETIME** 格式或 **VT \_ 日期** 格式的範例，請參閱 [WMI 工作：日期和時間](wmi-tasks--dates-and-times.md)。</span><span class="sxs-lookup"><span data-stu-id="86e8a-117">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="86e8a-118">如需 CIM **DATETIME** 格式的說明，請參閱 [日期和時間格式](date-and-time-format.md)。</span><span class="sxs-lookup"><span data-stu-id="86e8a-118">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="86e8a-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="86e8a-119">Requirements</span></span>



| <span data-ttu-id="86e8a-120">需求</span><span class="sxs-lookup"><span data-stu-id="86e8a-120">Requirement</span></span> | <span data-ttu-id="86e8a-121">值</span><span class="sxs-lookup"><span data-stu-id="86e8a-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="86e8a-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="86e8a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="86e8a-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="86e8a-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="86e8a-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="86e8a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="86e8a-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="86e8a-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="86e8a-126">標頭</span><span class="sxs-lookup"><span data-stu-id="86e8a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="86e8a-127"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="86e8a-127"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="86e8a-128">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="86e8a-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="86e8a-129"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="86e8a-129"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="86e8a-130">DLL</span><span class="sxs-lookup"><span data-stu-id="86e8a-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="86e8a-131"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86e8a-131"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="86e8a-132">CLSID</span><span class="sxs-lookup"><span data-stu-id="86e8a-132">CLSID</span></span><br/>                    | <span data-ttu-id="86e8a-133">CLSID \_ SWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="86e8a-133">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="86e8a-134">IID</span><span class="sxs-lookup"><span data-stu-id="86e8a-134">IID</span></span><br/>                      | <span data-ttu-id="86e8a-135">IID \_ ISWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="86e8a-135">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="86e8a-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="86e8a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86e8a-137">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="86e8a-137">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="86e8a-138">**Datetime**</span><span class="sxs-lookup"><span data-stu-id="86e8a-138">**DATETIME**</span></span>](datetime.md)
</dt> </dl>

 

