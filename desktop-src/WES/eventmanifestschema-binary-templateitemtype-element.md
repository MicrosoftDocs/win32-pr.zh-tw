---
title: 二元 (TemplateItemType) 元素
description: 包含事件記錄檔 API 所提供的二進位資料。
ms.assetid: 3ad9c119-9395-49d3-b920-9a071bcc6a04
keywords:
- 二元元素 EventLog
topic_type:
- apiref
api_name:
- binary
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3c3e281da662b4cdd0ecacc81a88f1a5728f90da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966143"
---
# <a name="binary-templateitemtype-element"></a><span data-ttu-id="4c7e5-104">二元 (TemplateItemType) 元素</span><span class="sxs-lookup"><span data-stu-id="4c7e5-104">binary (TemplateItemType) Element</span></span>

<span data-ttu-id="4c7e5-105">包含 [事件記錄](/windows/desktop/EventLog/event-logging) 檔 API 所提供的二進位資料。</span><span class="sxs-lookup"><span data-stu-id="4c7e5-105">Contains the binary data that is supplied by the [Event Log](/windows/desktop/EventLog/event-logging) API.</span></span>

``` syntax
<xs:element name="binary">
    <xs:complexType>
        <xs:attribute name="name"
            type="string"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="4c7e5-106">**二元** 元素是由 [**TemplateItemType**](eventmanifestschema-templateitemtype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="4c7e5-106">The **binary** element is defined by the [**TemplateItemType**](eventmanifestschema-templateitemtype-complextype.md) complex type.</span></span>

## <a name="attributes"></a><span data-ttu-id="4c7e5-107">屬性</span><span class="sxs-lookup"><span data-stu-id="4c7e5-107">Attributes</span></span>



| <span data-ttu-id="4c7e5-108">名稱</span><span class="sxs-lookup"><span data-stu-id="4c7e5-108">Name</span></span> | <span data-ttu-id="4c7e5-109">類型</span><span class="sxs-lookup"><span data-stu-id="4c7e5-109">Type</span></span>   | <span data-ttu-id="4c7e5-110">描述</span><span class="sxs-lookup"><span data-stu-id="4c7e5-110">Description</span></span>                                          |
|------|--------|------------------------------------------------------|
| <span data-ttu-id="4c7e5-111">NAME</span><span class="sxs-lookup"><span data-stu-id="4c7e5-111">name</span></span> | <span data-ttu-id="4c7e5-112">字串</span><span class="sxs-lookup"><span data-stu-id="4c7e5-112">string</span></span> | <span data-ttu-id="4c7e5-113">與二進位資料相關聯的名稱。</span><span class="sxs-lookup"><span data-stu-id="4c7e5-113">The name associated with the binary data.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="4c7e5-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="4c7e5-114">Requirements</span></span>



| <span data-ttu-id="4c7e5-115">需求</span><span class="sxs-lookup"><span data-stu-id="4c7e5-115">Requirement</span></span> | <span data-ttu-id="4c7e5-116">值</span><span class="sxs-lookup"><span data-stu-id="4c7e5-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4c7e5-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4c7e5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4c7e5-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4c7e5-118">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4c7e5-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4c7e5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4c7e5-120">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4c7e5-120">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4c7e5-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4c7e5-121">See also</span></span>

<dl> <dt>

<span data-ttu-id="4c7e5-122">**父元素**</span><span class="sxs-lookup"><span data-stu-id="4c7e5-122">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="4c7e5-123">**範本 (TemplateListType)**</span><span class="sxs-lookup"><span data-stu-id="4c7e5-123">**template (TemplateListType)**</span></span>](eventmanifestschema-template-templatelisttype-element.md)
</dt> </dl>

 

