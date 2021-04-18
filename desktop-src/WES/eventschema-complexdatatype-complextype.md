---
title: ComplexDataType 複雜類型
description: 定義包含一或多個資料項目的結構。
ms.assetid: 1495daef-1dfd-4f62-9543-569cc74102f4
keywords:
- ComplexDataType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- ComplexDataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 598f2cc02f1e3675ff0c8fd6eae7f9a5e02b9407
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968581"
---
# <a name="complexdatatype-complex-type"></a><span data-ttu-id="22bc4-104">ComplexDataType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="22bc4-104">ComplexDataType Complex Type</span></span>

<span data-ttu-id="22bc4-105">定義包含一或多個資料項目的結構。</span><span class="sxs-lookup"><span data-stu-id="22bc4-105">Defines a structure that contains one or more data items.</span></span>

``` syntax
<xs:complexType name="ComplexDataType">
    <xs:sequence>
        <xs:element name="Data"
            type="DataType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
    <xs:attribute name="Name"
        type="string"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="22bc4-106">子元素</span><span class="sxs-lookup"><span data-stu-id="22bc4-106">Child elements</span></span>



| <span data-ttu-id="22bc4-107">元素</span><span class="sxs-lookup"><span data-stu-id="22bc4-107">Element</span></span>                                                  | <span data-ttu-id="22bc4-108">類型</span><span class="sxs-lookup"><span data-stu-id="22bc4-108">Type</span></span>                                                      | <span data-ttu-id="22bc4-109">Description</span><span class="sxs-lookup"><span data-stu-id="22bc4-109">Description</span></span>                                                                                                             |
|----------------------------------------------------------|-----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="22bc4-110">**資料**</span><span class="sxs-lookup"><span data-stu-id="22bc4-110">**Data**</span></span>](eventschema-data-complexdatatype-element.md) | [<span data-ttu-id="22bc4-111">**資料類型**</span><span class="sxs-lookup"><span data-stu-id="22bc4-111">**DataType**</span></span>](eventschema-datafieldtype-complextype.md) | <span data-ttu-id="22bc4-112">結構中資料項目的清單。</span><span class="sxs-lookup"><span data-stu-id="22bc4-112">The list of data items in the structure.</span></span> <span data-ttu-id="22bc4-113">專案清單的順序與範本中所定義的順序相同。</span><span class="sxs-lookup"><span data-stu-id="22bc4-113">The list of items are in the same order as defined in the template.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="22bc4-114">屬性</span><span class="sxs-lookup"><span data-stu-id="22bc4-114">Attributes</span></span>



| <span data-ttu-id="22bc4-115">名稱</span><span class="sxs-lookup"><span data-stu-id="22bc4-115">Name</span></span> | <span data-ttu-id="22bc4-116">類型</span><span class="sxs-lookup"><span data-stu-id="22bc4-116">Type</span></span>   | <span data-ttu-id="22bc4-117">描述</span><span class="sxs-lookup"><span data-stu-id="22bc4-117">Description</span></span>                                                                                                                                                                                                                  |
|------|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22bc4-118">名稱</span><span class="sxs-lookup"><span data-stu-id="22bc4-118">Name</span></span> | <span data-ttu-id="22bc4-119">字串</span><span class="sxs-lookup"><span data-stu-id="22bc4-119">string</span></span> | <span data-ttu-id="22bc4-120">結構的名稱。</span><span class="sxs-lookup"><span data-stu-id="22bc4-120">The name of the structure.</span></span> <span data-ttu-id="22bc4-121">這是您在範本中定義結構時所指定的名稱， (查看 [**TemplateItemType**](eventmanifestschema-templateitemtype-complextype.md) 複雜類型) 。</span><span class="sxs-lookup"><span data-stu-id="22bc4-121">This is the name that is specified when you defined the structure in the template (see the [**TemplateItemType**](eventmanifestschema-templateitemtype-complextype.md) complex type).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="22bc4-122">備註</span><span class="sxs-lookup"><span data-stu-id="22bc4-122">Remarks</span></span>

<span data-ttu-id="22bc4-123">[**EvtRender**](/windows/desktop/api/WinEvt/nf-winevt-evtrender)函式會以二進位 blob 的形式呈現結構的內容;函數不會轉譯結構的個別資料項目。</span><span class="sxs-lookup"><span data-stu-id="22bc4-123">The [**EvtRender**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) function renders the contents of a structure as a binary blob; the function does not render the individual data items of the structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="22bc4-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="22bc4-124">Requirements</span></span>



| <span data-ttu-id="22bc4-125">需求</span><span class="sxs-lookup"><span data-stu-id="22bc4-125">Requirement</span></span> | <span data-ttu-id="22bc4-126">值</span><span class="sxs-lookup"><span data-stu-id="22bc4-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="22bc4-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="22bc4-127">Minimum supported client</span></span><br/> | <span data-ttu-id="22bc4-128">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="22bc4-128">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="22bc4-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="22bc4-129">Minimum supported server</span></span><br/> | <span data-ttu-id="22bc4-130">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="22bc4-130">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





