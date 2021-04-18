---
title: QueryListType 複雜類型
description: 定義查詢清單，其中可包含一組選取器和 suppressors，用來在結果集中包含或排除事件。
ms.assetid: 3b9944e8-5913-4a77-a8fd-7efa43f3063f
keywords:
- QueryListType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- QueryListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 58cc6e83fb681f6244288088ea217097dd109c23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968761"
---
# <a name="querylisttype-complex-type"></a><span data-ttu-id="99ae9-104">QueryListType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="99ae9-104">QueryListType Complex Type</span></span>

<span data-ttu-id="99ae9-105">定義查詢清單，其中可包含一組選取器和 suppressors，用來在結果集中包含或排除事件。</span><span class="sxs-lookup"><span data-stu-id="99ae9-105">Defines a list of queries that can contain a set of selectors and suppressors that are used to include events in or exclude events from the result set.</span></span>

``` syntax
<xs:complexType name="QueryListType">
    <xs:sequence
        maxOccurs="unbounded"
    >
        <xs:element name="Query"
            type="QueryType"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="99ae9-106">子元素</span><span class="sxs-lookup"><span data-stu-id="99ae9-106">Child elements</span></span>



| <span data-ttu-id="99ae9-107">元素</span><span class="sxs-lookup"><span data-stu-id="99ae9-107">Element</span></span>                                                  | <span data-ttu-id="99ae9-108">類型</span><span class="sxs-lookup"><span data-stu-id="99ae9-108">Type</span></span>                                                   | <span data-ttu-id="99ae9-109">Description</span><span class="sxs-lookup"><span data-stu-id="99ae9-109">Description</span></span>                                                                                                                     |
|----------------------------------------------------------|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="99ae9-110">**查詢**</span><span class="sxs-lookup"><span data-stu-id="99ae9-110">**Query**</span></span>](queryschema-query-querylisttype-element.md) | [<span data-ttu-id="99ae9-111">**QueryType**</span><span class="sxs-lookup"><span data-stu-id="99ae9-111">**QueryType**</span></span>](queryschema-querytype-complextype.md) | <span data-ttu-id="99ae9-112">定義一組選取器和 suppressors，用來在結果集中包含或排除事件。</span><span class="sxs-lookup"><span data-stu-id="99ae9-112">Defines a set of selectors and suppressors that are used to include events in or exclude events from the result set.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="99ae9-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="99ae9-113">Requirements</span></span>



| <span data-ttu-id="99ae9-114">需求</span><span class="sxs-lookup"><span data-stu-id="99ae9-114">Requirement</span></span> | <span data-ttu-id="99ae9-115">值</span><span class="sxs-lookup"><span data-stu-id="99ae9-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="99ae9-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="99ae9-116">Minimum supported client</span></span><br/> | <span data-ttu-id="99ae9-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="99ae9-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="99ae9-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="99ae9-118">Minimum supported server</span></span><br/> | <span data-ttu-id="99ae9-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="99ae9-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





