---
title: QueryType 複雜類型
description: 定義一組選取器和抑制器查詢，用來在結果集中包含或排除事件。
ms.assetid: 223d0127-f097-45f8-8511-1a56d9c41e84
keywords:
- QueryType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- QueryType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 50c0779b90a6f2e74a873b13d79c6e2083afd0ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094524"
---
# <a name="querytype-complex-type"></a><span data-ttu-id="456b3-104">QueryType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="456b3-104">QueryType Complex Type</span></span>

<span data-ttu-id="456b3-105">定義一組選取器和抑制器查詢，用來在結果集中包含或排除事件。</span><span class="sxs-lookup"><span data-stu-id="456b3-105">Defines a set of selector and suppressor queries that are used to include events in or exclude events from the result set.</span></span>

``` syntax
<xs:complexType name="QueryType">
    <xs:choice
        maxOccurs="unbounded"
    >
        <xs:element name="Select">
            <xs:complexType
                mixed="true"
            >
                <xs:attribute name="Path"
                    type="anyURI"
                 />
            </xs:complexType>
        </xs:element>
        <xs:element name="Suppress">
            <xs:complexType
                mixed="true"
            >
                <xs:attribute name="Path"
                    type="anyURI"
                 />
            </xs:complexType>
        </xs:element>
    </xs:choice>
    <xs:attribute name="Id"
        type="long"
        use="optional"
     />
    <xs:attribute name="Path"
        type="anyURI"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="456b3-106">子元素</span><span class="sxs-lookup"><span data-stu-id="456b3-106">Child elements</span></span>



| <span data-ttu-id="456b3-107">元素</span><span class="sxs-lookup"><span data-stu-id="456b3-107">Element</span></span>                                                    | <span data-ttu-id="456b3-108">類型</span><span class="sxs-lookup"><span data-stu-id="456b3-108">Type</span></span> | <span data-ttu-id="456b3-109">Description</span><span class="sxs-lookup"><span data-stu-id="456b3-109">Description</span></span>                                                                                                                                                                            |
|------------------------------------------------------------|------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="456b3-110">**選擇**</span><span class="sxs-lookup"><span data-stu-id="456b3-110">**Select**</span></span>](queryschema-select-querytype-element.md)     |      | <span data-ttu-id="456b3-111">XPath 查詢，識別要包含在查詢結果集中的事件。</span><span class="sxs-lookup"><span data-stu-id="456b3-111">An XPath query that identifies the events to include in the query result set.</span></span> <span data-ttu-id="456b3-112">在此元素的文字本文中指定 XPath。</span><span class="sxs-lookup"><span data-stu-id="456b3-112">Specify the XPath in the text body of this element.</span></span> <span data-ttu-id="456b3-113">XPath 的限制為32個運算式。</span><span class="sxs-lookup"><span data-stu-id="456b3-113">The XPath is limited to 32 expressions.</span></span><br/>   |
| [<span data-ttu-id="456b3-114">**隱藏**</span><span class="sxs-lookup"><span data-stu-id="456b3-114">**Suppress**</span></span>](queryschema-suppress-querytype-element.md) |      | <span data-ttu-id="456b3-115">XPath 查詢，識別要從查詢結果集排除的事件。</span><span class="sxs-lookup"><span data-stu-id="456b3-115">An XPath query that identifies the events to exclude from the query result set.</span></span> <span data-ttu-id="456b3-116">在此元素的文字本文中指定 XPath。</span><span class="sxs-lookup"><span data-stu-id="456b3-116">Specify the XPath in the text body of this element.</span></span> <span data-ttu-id="456b3-117">XPath 的限制為32個運算式。</span><span class="sxs-lookup"><span data-stu-id="456b3-117">The XPath is limited to 32 expressions.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="456b3-118">屬性</span><span class="sxs-lookup"><span data-stu-id="456b3-118">Attributes</span></span>



| <span data-ttu-id="456b3-119">名稱</span><span class="sxs-lookup"><span data-stu-id="456b3-119">Name</span></span> | <span data-ttu-id="456b3-120">類型</span><span class="sxs-lookup"><span data-stu-id="456b3-120">Type</span></span>   | <span data-ttu-id="456b3-121">Description</span><span class="sxs-lookup"><span data-stu-id="456b3-121">Description</span></span>                                                                                                                                                                                         |
|------|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="456b3-122">識別碼</span><span class="sxs-lookup"><span data-stu-id="456b3-122">Id</span></span>   | <span data-ttu-id="456b3-123">long</span><span class="sxs-lookup"><span data-stu-id="456b3-123">long</span></span>   | <span data-ttu-id="456b3-124">可在您的查詢清單中唯一識別此查詢的識別碼。</span><span class="sxs-lookup"><span data-stu-id="456b3-124">An identifier that uniquely identifies this query in your list of queries.</span></span> <span data-ttu-id="456b3-125">識別碼以零為基底。</span><span class="sxs-lookup"><span data-stu-id="456b3-125">The identifier is zero-based.</span></span> <span data-ttu-id="456b3-126">如果您的查詢清單包含一個以上的查詢，則必須指定識別碼。</span><span class="sxs-lookup"><span data-stu-id="456b3-126">You must specify an identifier if your query list contains more than one query.</span></span><br/> |
| <span data-ttu-id="456b3-127">路徑</span><span class="sxs-lookup"><span data-stu-id="456b3-127">Path</span></span> | <span data-ttu-id="456b3-128">anyURI</span><span class="sxs-lookup"><span data-stu-id="456b3-128">anyURI</span></span> | <span data-ttu-id="456b3-129">通道的名稱或包含事件之記錄檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="456b3-129">The name of the channel or the path to the log file that contains the events.</span></span><br/>                                                                                                            |
| <span data-ttu-id="456b3-130">路徑</span><span class="sxs-lookup"><span data-stu-id="456b3-130">Path</span></span> | <span data-ttu-id="456b3-131">anyURI</span><span class="sxs-lookup"><span data-stu-id="456b3-131">anyURI</span></span> | <span data-ttu-id="456b3-132">通道的名稱或包含事件之記錄檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="456b3-132">The name of the channel or the path to the log file that contains the events.</span></span><br/>                                                                                                            |
| <span data-ttu-id="456b3-133">路徑</span><span class="sxs-lookup"><span data-stu-id="456b3-133">Path</span></span> | <span data-ttu-id="456b3-134">anyURI</span><span class="sxs-lookup"><span data-stu-id="456b3-134">anyURI</span></span> | <span data-ttu-id="456b3-135">未使用。</span><span class="sxs-lookup"><span data-stu-id="456b3-135">Not used.</span></span><br/>                                                                                                                                                                                |



## <a name="remarks"></a><span data-ttu-id="456b3-136">備註</span><span class="sxs-lookup"><span data-stu-id="456b3-136">Remarks</span></span>

<span data-ttu-id="456b3-137">查詢必須至少有一個 select 語句。</span><span class="sxs-lookup"><span data-stu-id="456b3-137">The query must have at least one select statement.</span></span> <span data-ttu-id="456b3-138">針對每個隱藏語句，至少必須有一個指定相同路徑的 select 語句。</span><span class="sxs-lookup"><span data-stu-id="456b3-138">For each suppress statement, there must be at least one select statement that specifies the same path.</span></span> <span data-ttu-id="456b3-139">如果 select 和抑制查詢傳回相同的事件，則會優先使用隱藏語句。</span><span class="sxs-lookup"><span data-stu-id="456b3-139">If the select and suppress query return the same events, the suppress statement takes precedence.</span></span> <span data-ttu-id="456b3-140">如果您選取多個來源的事件，則會以時間戳記順序傳回事件。</span><span class="sxs-lookup"><span data-stu-id="456b3-140">If you select events from multiple sources, the events are returned in time stamp order.</span></span> <span data-ttu-id="456b3-141">如果您使用系統時間戳記，而事件率很高，則有一個以上的事件可能會有相同的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="456b3-141">If you use the system time stamp and the rate of events is high, it is possible that more than one event will have the same time stamp.</span></span> <span data-ttu-id="456b3-142">發生這種情況時，事件的順序會變得不明確，而且事件可能會依順序出現。</span><span class="sxs-lookup"><span data-stu-id="456b3-142">When this occurs, the ordering of events becomes ambiguous and the events may appear out of order.</span></span>

<span data-ttu-id="456b3-143">如果您為查詢清單中的其中一個查詢指定路徑，則所有查詢都必須指定路徑。</span><span class="sxs-lookup"><span data-stu-id="456b3-143">If you specify a path for one of the queries in the list of queries, all of the queries must specify a path.</span></span> <span data-ttu-id="456b3-144">如果您未指定所有查詢的路徑，則必須在呼叫 [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) 或 [**EvtSubscribe**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) 函式時指定路徑。</span><span class="sxs-lookup"><span data-stu-id="456b3-144">If you do not specify a path for all of the queries, you must specify the path when calling the [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) or [**EvtSubscribe**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="456b3-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="456b3-145">Requirements</span></span>



| <span data-ttu-id="456b3-146">需求</span><span class="sxs-lookup"><span data-stu-id="456b3-146">Requirement</span></span> | <span data-ttu-id="456b3-147">值</span><span class="sxs-lookup"><span data-stu-id="456b3-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="456b3-148">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="456b3-148">Minimum supported client</span></span><br/> | <span data-ttu-id="456b3-149">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="456b3-149">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="456b3-150">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="456b3-150">Minimum supported server</span></span><br/> | <span data-ttu-id="456b3-151">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="456b3-151">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





