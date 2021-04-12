---
title: 選取 (QueryType) 元素
description: XPath 查詢，識別要包含在查詢結果集中的事件。
ms.assetid: b6aa747b-3586-460b-b51c-52fb112739c3
keywords:
- Select 元素 EventLog
topic_type:
- apiref
api_name:
- Select
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b1735f5de49853357eed1ce00b8d181edf2279ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385146"
---
# <a name="select-querytype-element"></a><span data-ttu-id="7d59a-104">選取 (QueryType) 元素</span><span class="sxs-lookup"><span data-stu-id="7d59a-104">Select (QueryType) Element</span></span>

<span data-ttu-id="7d59a-105">XPath 查詢，識別要包含在查詢結果集中的事件。</span><span class="sxs-lookup"><span data-stu-id="7d59a-105">An XPath query that identifies the events to include in the query result set.</span></span>

``` syntax
<xs:element name="Select">
    <xs:complexType
        mixed="true"
    >
        <xs:attribute name="Path"
            type="anyURI"
         />
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="7d59a-106">**Select** 元素是由 [**QueryType**](queryschema-querytype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="7d59a-106">The **Select** element is defined by the [**QueryType**](queryschema-querytype-complextype.md) complex type.</span></span>

## <a name="attributes"></a><span data-ttu-id="7d59a-107">屬性</span><span class="sxs-lookup"><span data-stu-id="7d59a-107">Attributes</span></span>



| <span data-ttu-id="7d59a-108">名稱</span><span class="sxs-lookup"><span data-stu-id="7d59a-108">Name</span></span> | <span data-ttu-id="7d59a-109">類型</span><span class="sxs-lookup"><span data-stu-id="7d59a-109">Type</span></span>   | <span data-ttu-id="7d59a-110">Description</span><span class="sxs-lookup"><span data-stu-id="7d59a-110">Description</span></span>                                                                              |
|------|--------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d59a-111">路徑</span><span class="sxs-lookup"><span data-stu-id="7d59a-111">Path</span></span> | <span data-ttu-id="7d59a-112">anyURI</span><span class="sxs-lookup"><span data-stu-id="7d59a-112">anyURI</span></span> | <span data-ttu-id="7d59a-113">通道的名稱或包含事件之記錄檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="7d59a-113">The name of the channel or the path to the log file that contains the events.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="7d59a-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="7d59a-114">Requirements</span></span>



| <span data-ttu-id="7d59a-115">需求</span><span class="sxs-lookup"><span data-stu-id="7d59a-115">Requirement</span></span> | <span data-ttu-id="7d59a-116">值</span><span class="sxs-lookup"><span data-stu-id="7d59a-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="7d59a-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7d59a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7d59a-118">Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7d59a-118">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>       |
| <span data-ttu-id="7d59a-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7d59a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7d59a-120">Windows Server 2008 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7d59a-120">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7d59a-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7d59a-121">See also</span></span>

<dl> <dt>

<span data-ttu-id="7d59a-122">**父元素**</span><span class="sxs-lookup"><span data-stu-id="7d59a-122">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="7d59a-123">**查詢 (QueryListType)**</span><span class="sxs-lookup"><span data-stu-id="7d59a-123">**Query (QueryListType)**</span></span>](queryschema-query-querylisttype-element.md)
</dt> </dl>

 

 





