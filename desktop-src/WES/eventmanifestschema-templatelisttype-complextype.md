---
title: TemplateListType 複雜類型
description: 定義範本清單，以指定要包含在事件中的資料。 |TemplateListType 複雜類型
ms.assetid: 7f676746-6773-4ae2-8330-60d432c29e3a
keywords:
- TemplateListType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- TemplateListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a60b31fd88d05f00229f27a616a29483a29bd49d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103696469"
---
# <a name="templatelisttype-complex-type"></a><span data-ttu-id="c48b6-105">TemplateListType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="c48b6-105">TemplateListType Complex Type</span></span>

<span data-ttu-id="c48b6-106">定義範本清單，以指定要包含在事件中的資料。</span><span class="sxs-lookup"><span data-stu-id="c48b6-106">Defines a list of templates that specify the data to include with the events.</span></span>

``` syntax
<xs:complexType name="TemplateListType">
    <xs:sequence>
        <xs:element name="template"
            type="TemplateItemType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="c48b6-107">子元素</span><span class="sxs-lookup"><span data-stu-id="c48b6-107">Child elements</span></span>



| <span data-ttu-id="c48b6-108">元素</span><span class="sxs-lookup"><span data-stu-id="c48b6-108">Element</span></span>                                                                   | <span data-ttu-id="c48b6-109">類型</span><span class="sxs-lookup"><span data-stu-id="c48b6-109">Type</span></span>                                                                         | <span data-ttu-id="c48b6-110">Description</span><span class="sxs-lookup"><span data-stu-id="c48b6-110">Description</span></span>                                                           |
|---------------------------------------------------------------------------|------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="c48b6-111">**範本**</span><span class="sxs-lookup"><span data-stu-id="c48b6-111">**template**</span></span>](eventmanifestschema-template-templatelisttype-element.md) | [<span data-ttu-id="c48b6-112">**TemplateItemType**</span><span class="sxs-lookup"><span data-stu-id="c48b6-112">**TemplateItemType**</span></span>](eventmanifestschema-templateitemtype-complextype.md) | <span data-ttu-id="c48b6-113">此範本會定義要包含在事件中的資料。</span><span class="sxs-lookup"><span data-stu-id="c48b6-113">A template that defines the data to include with an event.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="c48b6-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="c48b6-114">Requirements</span></span>



| <span data-ttu-id="c48b6-115">需求</span><span class="sxs-lookup"><span data-stu-id="c48b6-115">Requirement</span></span> | <span data-ttu-id="c48b6-116">值</span><span class="sxs-lookup"><span data-stu-id="c48b6-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c48b6-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c48b6-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c48b6-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c48b6-118">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c48b6-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c48b6-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c48b6-120">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c48b6-120">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





