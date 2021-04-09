---
title: 提供者 (SystemPropertiesType) 元素
description: 識別記錄事件的提供者。
ms.assetid: 4560c938-4e2a-40d5-97f9-85a38141ac8f
keywords:
- Provider 元素 EventLog
topic_type:
- apiref
api_name:
- Provider
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c3dc6ae072ed6491915067bea4395a1a84369b15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024749"
---
# <a name="provider-systempropertiestype-element"></a><span data-ttu-id="d89e0-104">提供者 (SystemPropertiesType) 元素</span><span class="sxs-lookup"><span data-stu-id="d89e0-104">Provider (SystemPropertiesType) Element</span></span>

<span data-ttu-id="d89e0-105">識別記錄事件的提供者。</span><span class="sxs-lookup"><span data-stu-id="d89e0-105">Identifies the provider that logged the event.</span></span>

``` syntax
<xs:element name="Provider">
    <xs:complexType>
        <xs:attribute name="Name"
            type="anyURI"
            use="optional"
         />
        <xs:attribute name="Guid"
            type="GUIDType"
            use="optional"
         />
        <xs:attribute name="EventSourceName"
            type="string"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="d89e0-106">**Provider** 元素是由 [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="d89e0-106">The **Provider** element is defined by the [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) complex type.</span></span>

## <a name="attributes"></a><span data-ttu-id="d89e0-107">屬性</span><span class="sxs-lookup"><span data-stu-id="d89e0-107">Attributes</span></span>



| <span data-ttu-id="d89e0-108">名稱</span><span class="sxs-lookup"><span data-stu-id="d89e0-108">Name</span></span>            | <span data-ttu-id="d89e0-109">類型</span><span class="sxs-lookup"><span data-stu-id="d89e0-109">Type</span></span>                                                | <span data-ttu-id="d89e0-110">Description</span><span class="sxs-lookup"><span data-stu-id="d89e0-110">Description</span></span>                                                                                                                                        |
|-----------------|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d89e0-111">EventSourceName</span><span class="sxs-lookup"><span data-stu-id="d89e0-111">EventSourceName</span></span> | <span data-ttu-id="d89e0-112">字串</span><span class="sxs-lookup"><span data-stu-id="d89e0-112">string</span></span>                                              | <span data-ttu-id="d89e0-113">如果事件來源來自舊版 [事件記錄](/windows/desktop/EventLog/event-logging) API) ，則發佈事件 (事件來源的名稱。</span><span class="sxs-lookup"><span data-stu-id="d89e0-113">The name of the event source that published the event (if the event source is from the legacy [Event Logging](/windows/desktop/EventLog/event-logging) API).</span></span><br/> |
| <span data-ttu-id="d89e0-114">Guid</span><span class="sxs-lookup"><span data-stu-id="d89e0-114">Guid</span></span>            | [<span data-ttu-id="d89e0-115">**GUIDType**</span><span class="sxs-lookup"><span data-stu-id="d89e0-115">**GUIDType**</span></span>](eventschema-guidtype-simpletype.md) | <span data-ttu-id="d89e0-116">可唯一識別提供者的全域唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="d89e0-116">The globally unique identifier that uniquely identifies the provider.</span></span><br/>                                                                   |
| <span data-ttu-id="d89e0-117">Name</span><span class="sxs-lookup"><span data-stu-id="d89e0-117">Name</span></span>            | <span data-ttu-id="d89e0-118">anyURI</span><span class="sxs-lookup"><span data-stu-id="d89e0-118">anyURI</span></span>                                              | <span data-ttu-id="d89e0-119">記錄事件之事件提供者的名稱。</span><span class="sxs-lookup"><span data-stu-id="d89e0-119">The name of the event provider that logged the event.</span></span><br/>                                                                                   |



## <a name="requirements"></a><span data-ttu-id="d89e0-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="d89e0-120">Requirements</span></span>



| <span data-ttu-id="d89e0-121">需求</span><span class="sxs-lookup"><span data-stu-id="d89e0-121">Requirement</span></span> | <span data-ttu-id="d89e0-122">值</span><span class="sxs-lookup"><span data-stu-id="d89e0-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d89e0-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d89e0-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d89e0-124">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d89e0-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d89e0-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d89e0-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d89e0-126">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d89e0-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d89e0-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d89e0-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="d89e0-128">**父元素**</span><span class="sxs-lookup"><span data-stu-id="d89e0-128">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="d89e0-129">**系統 (的系統事件)**</span><span class="sxs-lookup"><span data-stu-id="d89e0-129">**System (EventType)**</span></span>](eventschema-system-eventtype-element.md)
</dt> </dl>

 

