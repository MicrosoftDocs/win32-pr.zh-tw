---
title: EventDataType 複雜類型
description: 定義事件資料項目和包含事件資料的結構。
ms.assetid: 9531163f-34ce-4673-b2d8-636042915c73
keywords:
- EventDataType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- EventDataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6a93695db477ebb0c7b5652419198f8f5c6370dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685626"
---
# <a name="eventdatatype-complex-type"></a><span data-ttu-id="66502-104">EventDataType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="66502-104">EventDataType Complex Type</span></span>

<span data-ttu-id="66502-105">定義事件資料項目和包含事件資料的結構。</span><span class="sxs-lookup"><span data-stu-id="66502-105">Defines the event data items and structures that contains the event data.</span></span>

``` syntax
<xs:complexType name="EventDataType">
    <xs:sequence>
        <xs:choice
            minOccurs="0"
            maxOccurs="unbounded"
        >
            <xs:element name="Data"
                type="DataType"
             />
            <xs:element name="ComplexData"
                type="ComplexDataType"
             />
        </xs:choice>
        <xs:element name="Binary"
            type="hexBinary"
            minOccurs="0"
         />
    </xs:sequence>
    <xs:attribute name="Name"
        type="string"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="66502-106">子元素</span><span class="sxs-lookup"><span data-stu-id="66502-106">Child elements</span></span>



| <span data-ttu-id="66502-107">元素</span><span class="sxs-lookup"><span data-stu-id="66502-107">Element</span></span>                                                              | <span data-ttu-id="66502-108">類型</span><span class="sxs-lookup"><span data-stu-id="66502-108">Type</span></span>                                                               | <span data-ttu-id="66502-109">Description</span><span class="sxs-lookup"><span data-stu-id="66502-109">Description</span></span>                                                                                          |
|----------------------------------------------------------------------|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="66502-110">**二進位**</span><span class="sxs-lookup"><span data-stu-id="66502-110">**Binary**</span></span>](eventschema-binary-eventdatatype-element.md)           | <span data-ttu-id="66502-111">hexBinary</span><span class="sxs-lookup"><span data-stu-id="66502-111">hexBinary</span></span>                                                          | <span data-ttu-id="66502-112">使用 [事件記錄](/windows/desktop/EventLog/event-logging)撰寫之事件的二進位資料 blob。</span><span class="sxs-lookup"><span data-stu-id="66502-112">A binary data blob for events that are written using [Event Logging](/windows/desktop/EventLog/event-logging).</span></span><br/> |
| [<span data-ttu-id="66502-113">**ComplexData**</span><span class="sxs-lookup"><span data-stu-id="66502-113">**ComplexData**</span></span>](eventschema-complexdata-eventdatatype-element.md) | [<span data-ttu-id="66502-114">**ComplexDataType**</span><span class="sxs-lookup"><span data-stu-id="66502-114">**ComplexDataType**</span></span>](eventschema-complexdatatype-complextype.md) | <span data-ttu-id="66502-115">在事件的範本中定義的結構。</span><span class="sxs-lookup"><span data-stu-id="66502-115">A structure that is defined in the template for the event.</span></span><br/>                                |
| [<span data-ttu-id="66502-116">**資料**</span><span class="sxs-lookup"><span data-stu-id="66502-116">**Data**</span></span>](eventschema-data-eventdatatype-element.md)               | [<span data-ttu-id="66502-117">**資料類型**</span><span class="sxs-lookup"><span data-stu-id="66502-117">**DataType**</span></span>](eventschema-datafieldtype-complextype.md)          | <span data-ttu-id="66502-118">在事件的範本中定義的最上層資料項目。</span><span class="sxs-lookup"><span data-stu-id="66502-118">A top-level data item that is defined in the template for the event.</span></span><br/>                      |



## <a name="attributes"></a><span data-ttu-id="66502-119">屬性</span><span class="sxs-lookup"><span data-stu-id="66502-119">Attributes</span></span>



| <span data-ttu-id="66502-120">名稱</span><span class="sxs-lookup"><span data-stu-id="66502-120">Name</span></span> | <span data-ttu-id="66502-121">類型</span><span class="sxs-lookup"><span data-stu-id="66502-121">Type</span></span>   | <span data-ttu-id="66502-122">描述</span><span class="sxs-lookup"><span data-stu-id="66502-122">Description</span></span>                                                       |
|------|--------|-------------------------------------------------------------------|
| <span data-ttu-id="66502-123">名稱</span><span class="sxs-lookup"><span data-stu-id="66502-123">Name</span></span> | <span data-ttu-id="66502-124">字串</span><span class="sxs-lookup"><span data-stu-id="66502-124">string</span></span> | <span data-ttu-id="66502-125">包含資料項目的範本名稱。</span><span class="sxs-lookup"><span data-stu-id="66502-125">The name of the template that contains the data items.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="66502-126">備註</span><span class="sxs-lookup"><span data-stu-id="66502-126">Remarks</span></span>

<span data-ttu-id="66502-127">[**EvtRender**](/windows/desktop/api/WinEvt/nf-winevt-evtrender)函式會以二進位 blob 的形式呈現陣列和結構。</span><span class="sxs-lookup"><span data-stu-id="66502-127">The [**EvtRender**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) function renders arrays and structures as binary blobs.</span></span>

## <a name="requirements"></a><span data-ttu-id="66502-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="66502-128">Requirements</span></span>



| <span data-ttu-id="66502-129">需求</span><span class="sxs-lookup"><span data-stu-id="66502-129">Requirement</span></span> | <span data-ttu-id="66502-130">值</span><span class="sxs-lookup"><span data-stu-id="66502-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="66502-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="66502-131">Minimum supported client</span></span><br/> | <span data-ttu-id="66502-132">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="66502-132">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="66502-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="66502-133">Minimum supported server</span></span><br/> | <span data-ttu-id="66502-134">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="66502-134">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

