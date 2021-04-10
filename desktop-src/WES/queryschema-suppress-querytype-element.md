---
title: 隱藏 (QueryType) 元素
description: XPath 查詢，識別要從查詢結果集排除的事件。
ms.assetid: 41304a3c-bde1-49c3-8cb3-e95fc428bd96
keywords:
- 隱藏元素 EventLog
topic_type:
- apiref
api_name:
- Suppress
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3a1d7fcec98d32167155ebcafc4f13d2a727d59a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106331"
---
# <a name="suppress-querytype-element"></a><span data-ttu-id="22940-104">隱藏 (QueryType) 元素</span><span class="sxs-lookup"><span data-stu-id="22940-104">Suppress (QueryType) Element</span></span>

<span data-ttu-id="22940-105">XPath 查詢，識別要從查詢結果集排除的事件。</span><span class="sxs-lookup"><span data-stu-id="22940-105">An XPath query that identifies the events to exclude from the query result set.</span></span>

``` syntax
<xs:element name="Suppress">
    <xs:complexType
        mixed="true"
    >
        <xs:attribute name="Path"
            type="anyURI"
         />
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="22940-106">**隱藏** 專案是由 [**QueryType**](queryschema-querytype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="22940-106">The **Suppress** element is defined by the [**QueryType**](queryschema-querytype-complextype.md) complex type.</span></span>

## <a name="attributes"></a><span data-ttu-id="22940-107">屬性</span><span class="sxs-lookup"><span data-stu-id="22940-107">Attributes</span></span>



| <span data-ttu-id="22940-108">名稱</span><span class="sxs-lookup"><span data-stu-id="22940-108">Name</span></span> | <span data-ttu-id="22940-109">類型</span><span class="sxs-lookup"><span data-stu-id="22940-109">Type</span></span>   | <span data-ttu-id="22940-110">Description</span><span class="sxs-lookup"><span data-stu-id="22940-110">Description</span></span>                                                                              |
|------|--------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="22940-111">路徑</span><span class="sxs-lookup"><span data-stu-id="22940-111">Path</span></span> | <span data-ttu-id="22940-112">anyURI</span><span class="sxs-lookup"><span data-stu-id="22940-112">anyURI</span></span> | <span data-ttu-id="22940-113">通道的名稱或包含事件之記錄檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="22940-113">The name of the channel or the path to the log file that contains the events.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="22940-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="22940-114">Requirements</span></span>



| <span data-ttu-id="22940-115">需求</span><span class="sxs-lookup"><span data-stu-id="22940-115">Requirement</span></span> | <span data-ttu-id="22940-116">值</span><span class="sxs-lookup"><span data-stu-id="22940-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="22940-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="22940-117">Minimum supported client</span></span><br/> | <span data-ttu-id="22940-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="22940-118">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="22940-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="22940-119">Minimum supported server</span></span><br/> | <span data-ttu-id="22940-120">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="22940-120">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="22940-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="22940-121">See also</span></span>

<dl> <dt>

<span data-ttu-id="22940-122">**父元素**</span><span class="sxs-lookup"><span data-stu-id="22940-122">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="22940-123">**查詢 (QueryListType)**</span><span class="sxs-lookup"><span data-stu-id="22940-123">**Query (QueryListType)**</span></span>](queryschema-query-querylisttype-element.md)
</dt> </dl>

 

 





