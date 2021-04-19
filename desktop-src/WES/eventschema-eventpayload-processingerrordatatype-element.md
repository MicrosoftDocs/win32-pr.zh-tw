---
title: EventPayload (ProcessingErrorDataType) 元素
description: 包含事件的二進位事件資料，此事件會在處理事件資料時造成錯誤。
ms.assetid: 0ba72d72-8f43-40ca-b3ee-89fe27a4dd07
keywords:
- EventPayload 元素 EventLog
topic_type:
- apiref
api_name:
- EventPayload
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4dd20f95924282ae8cb0f1b0604c0e77d07766ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106984952"
---
# <a name="eventpayload-processingerrordatatype-element"></a><span data-ttu-id="46ff4-104">EventPayload (ProcessingErrorDataType) 元素</span><span class="sxs-lookup"><span data-stu-id="46ff4-104">EventPayload (ProcessingErrorDataType) Element</span></span>

<span data-ttu-id="46ff4-105">包含事件的二進位事件資料，此事件會在處理事件資料時造成錯誤。</span><span class="sxs-lookup"><span data-stu-id="46ff4-105">Contains binary event data for the event that caused an error when the event data was processed.</span></span>

``` syntax
<xs:element name="EventPayload"
    type="hexBinary"
 />
```

<span data-ttu-id="46ff4-106">**EventPayload** 元素是由 [**ProcessingErrorDataType**](eventschema-processingerrordatatype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="46ff4-106">The **EventPayload** element is defined by the [**ProcessingErrorDataType**](eventschema-processingerrordatatype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="46ff4-107">規格需求</span><span class="sxs-lookup"><span data-stu-id="46ff4-107">Requirements</span></span>



| <span data-ttu-id="46ff4-108">需求</span><span class="sxs-lookup"><span data-stu-id="46ff4-108">Requirement</span></span> | <span data-ttu-id="46ff4-109">值</span><span class="sxs-lookup"><span data-stu-id="46ff4-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="46ff4-110">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="46ff4-110">Minimum supported client</span></span><br/> | <span data-ttu-id="46ff4-111">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="46ff4-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="46ff4-112">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="46ff4-112">Minimum supported server</span></span><br/> | <span data-ttu-id="46ff4-113">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="46ff4-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="46ff4-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="46ff4-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="46ff4-115">**父元素**</span><span class="sxs-lookup"><span data-stu-id="46ff4-115">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="46ff4-116">**ProcessingErrorData (的事件)**</span><span class="sxs-lookup"><span data-stu-id="46ff4-116">**ProcessingErrorData (EventType)**</span></span>](eventschema-processingerrordata-eventtype-element.md)
</dt> </dl>

 

 





