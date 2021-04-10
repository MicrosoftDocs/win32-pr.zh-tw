---
title: TimeCreated (SystemPropertiesType) 元素
description: 識別事件記錄時間的時間戳記。
ms.assetid: 16b2b71b-078e-4862-b1be-ef7cec315bc5
keywords:
- TimeCreated 元素 EventLog
topic_type:
- apiref
api_name:
- TimeCreated
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 998bb03601f0ecbe87c571daa94b1f33e307d6af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934562"
---
# <a name="timecreated-systempropertiestype-element"></a><span data-ttu-id="55b2d-104">TimeCreated (SystemPropertiesType) 元素</span><span class="sxs-lookup"><span data-stu-id="55b2d-104">TimeCreated (SystemPropertiesType) Element</span></span>

<span data-ttu-id="55b2d-105">識別事件記錄時間的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="55b2d-105">The time stamp that identifies when the event was logged.</span></span>

``` syntax
<xs:element name="TimeCreated">
    <xs:complexType>
        <xs:attribute name="SystemTime"
            type="dateTime"
            use="required"
         />
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="55b2d-106">**TimeCreated** 元素是由 [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="55b2d-106">The **TimeCreated** element is defined by the [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) complex type.</span></span>

## <a name="attributes"></a><span data-ttu-id="55b2d-107">屬性</span><span class="sxs-lookup"><span data-stu-id="55b2d-107">Attributes</span></span>



| <span data-ttu-id="55b2d-108">名稱</span><span class="sxs-lookup"><span data-stu-id="55b2d-108">Name</span></span>       | <span data-ttu-id="55b2d-109">類型</span><span class="sxs-lookup"><span data-stu-id="55b2d-109">Type</span></span>     | <span data-ttu-id="55b2d-110">Description</span><span class="sxs-lookup"><span data-stu-id="55b2d-110">Description</span></span>                                              |
|------------|----------|----------------------------------------------------------|
| <span data-ttu-id="55b2d-111">SystemTime</span><span class="sxs-lookup"><span data-stu-id="55b2d-111">SystemTime</span></span> | <span data-ttu-id="55b2d-112">dateTime</span><span class="sxs-lookup"><span data-stu-id="55b2d-112">dateTime</span></span> | <span data-ttu-id="55b2d-113">記錄事件的系統時間。</span><span class="sxs-lookup"><span data-stu-id="55b2d-113">The system time of when the event was logged.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="55b2d-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="55b2d-114">Requirements</span></span>



| <span data-ttu-id="55b2d-115">需求</span><span class="sxs-lookup"><span data-stu-id="55b2d-115">Requirement</span></span> | <span data-ttu-id="55b2d-116">值</span><span class="sxs-lookup"><span data-stu-id="55b2d-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="55b2d-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="55b2d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="55b2d-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="55b2d-118">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="55b2d-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="55b2d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="55b2d-120">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="55b2d-120">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="55b2d-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="55b2d-121">See also</span></span>

<dl> <dt>

<span data-ttu-id="55b2d-122">**父元素**</span><span class="sxs-lookup"><span data-stu-id="55b2d-122">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="55b2d-123">**系統 (的系統事件)**</span><span class="sxs-lookup"><span data-stu-id="55b2d-123">**System (EventType)**</span></span>](eventschema-system-eventtype-element.md)
</dt> </dl>

 

 





