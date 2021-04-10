---
title: 二元 (EventDataType) 元素
description: 使用事件記錄撰寫之事件的二進位資料 blob。
ms.assetid: aec2557f-6d63-48e7-b4d7-584e99dfcce3
keywords:
- 二元元素 EventLog
topic_type:
- apiref
api_name:
- Binary
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cdfd00e2d25f3178ab44081f76725b3189f1010b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024606"
---
# <a name="binary-eventdatatype-element"></a><span data-ttu-id="55467-104">二元 (EventDataType) 元素</span><span class="sxs-lookup"><span data-stu-id="55467-104">Binary (EventDataType) Element</span></span>

<span data-ttu-id="55467-105">使用 [事件記錄](/windows/desktop/EventLog/event-logging)撰寫之事件的二進位資料 blob。</span><span class="sxs-lookup"><span data-stu-id="55467-105">A binary data blob for events that are written using [Event Logging](/windows/desktop/EventLog/event-logging).</span></span>

``` syntax
<xs:element name="Binary"
    type="hexBinary"
 />
```

<span data-ttu-id="55467-106">**二元** 元素是由 [**EventDataType**](eventschema-eventdatatype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="55467-106">The **Binary** element is defined by the [**EventDataType**](eventschema-eventdatatype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="55467-107">規格需求</span><span class="sxs-lookup"><span data-stu-id="55467-107">Requirements</span></span>



| <span data-ttu-id="55467-108">需求</span><span class="sxs-lookup"><span data-stu-id="55467-108">Requirement</span></span> | <span data-ttu-id="55467-109">值</span><span class="sxs-lookup"><span data-stu-id="55467-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="55467-110">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="55467-110">Minimum supported client</span></span><br/> | <span data-ttu-id="55467-111">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="55467-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="55467-112">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="55467-112">Minimum supported server</span></span><br/> | <span data-ttu-id="55467-113">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="55467-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="55467-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="55467-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="55467-115">**父元素**</span><span class="sxs-lookup"><span data-stu-id="55467-115">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="55467-116">**EventData (的事件)**</span><span class="sxs-lookup"><span data-stu-id="55467-116">**EventData (EventType)**</span></span>](eventschema-eventdata-eventtype-element.md)
</dt> </dl>

 

