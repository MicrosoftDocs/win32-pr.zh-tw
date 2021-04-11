---
description: 布林值，指出是否應該將 CIM 日期時間值中的任何欄位解釋為間隔。
ms.assetid: ba5fcf17-7c26-4960-9da9-e380d90e5f3e
ms.tgt_platform: multiple
title: 'SWbemDateTime. IsInterval 屬性 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.IsInterval
- ISWbemDateTime.IsInterval
- ISWbemDateTime.get_IsInterval
- ISWbemDateTime.put_IsInterval
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 468ea16de4f1206a9a15c58c2c7891df8afd4c19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195230"
---
# <a name="swbemdatetimeisinterval-property"></a><span data-ttu-id="35b27-103">SWbemDateTime. IsInterval 屬性</span><span class="sxs-lookup"><span data-stu-id="35b27-103">SWbemDateTime.IsInterval property</span></span>

<span data-ttu-id="35b27-104">[**SWbemDateTime**](swbemdatetime.md)物件的 **IsInterval** 屬性是布林值，指出是否應該將 CIM datetime 值中的任何欄位解釋為間隔。</span><span class="sxs-lookup"><span data-stu-id="35b27-104">The **IsInterval** property of the [**SWbemDateTime**](swbemdatetime.md) object is a Boolean value that indicates whether any field in a CIM datetime value should be interpreted as an interval.</span></span>

<span data-ttu-id="35b27-105">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="35b27-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="35b27-106">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="35b27-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="35b27-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="35b27-107">Syntax</span></span>


```VB
SWbemDateTime.IsInterval As boolean
```



## <a name="property-value"></a><span data-ttu-id="35b27-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="35b27-108">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="35b27-109">範例</span><span class="sxs-lookup"><span data-stu-id="35b27-109">Examples</span></span>

<span data-ttu-id="35b27-110">如需使用 [**SWbemDateTime**](swbemdatetime.md) 物件將 CIM 日期時間值轉換成 **FILETIME** 格式或 **VT \_ 日期** 格式的範例，請參閱 [WMI 工作：日期和時間](wmi-tasks--dates-and-times.md)。</span><span class="sxs-lookup"><span data-stu-id="35b27-110">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM datetime values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="35b27-111">如需 CIM datetime 格式的說明，請參閱 [日期和時間格式](date-and-time-format.md)。</span><span class="sxs-lookup"><span data-stu-id="35b27-111">For a description of the CIM datetime format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="35b27-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="35b27-112">Requirements</span></span>



| <span data-ttu-id="35b27-113">需求</span><span class="sxs-lookup"><span data-stu-id="35b27-113">Requirement</span></span> | <span data-ttu-id="35b27-114">值</span><span class="sxs-lookup"><span data-stu-id="35b27-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="35b27-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="35b27-115">Minimum supported client</span></span><br/> | <span data-ttu-id="35b27-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="35b27-116">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="35b27-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="35b27-117">Minimum supported server</span></span><br/> | <span data-ttu-id="35b27-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="35b27-118">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="35b27-119">標頭</span><span class="sxs-lookup"><span data-stu-id="35b27-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="35b27-120"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="35b27-120"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="35b27-121">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="35b27-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="35b27-122"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="35b27-122"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="35b27-123">DLL</span><span class="sxs-lookup"><span data-stu-id="35b27-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35b27-124"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35b27-124"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="35b27-125">CLSID</span><span class="sxs-lookup"><span data-stu-id="35b27-125">CLSID</span></span><br/>                    | <span data-ttu-id="35b27-126">CLSID \_ SWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="35b27-126">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="35b27-127">IID</span><span class="sxs-lookup"><span data-stu-id="35b27-127">IID</span></span><br/>                      | <span data-ttu-id="35b27-128">IID \_ ISWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="35b27-128">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="35b27-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="35b27-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35b27-130">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="35b27-130">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="35b27-131">日期和時間格式</span><span class="sxs-lookup"><span data-stu-id="35b27-131">Date and Time Format</span></span>](date-and-time-format.md)
</dt> </dl>

 

 




