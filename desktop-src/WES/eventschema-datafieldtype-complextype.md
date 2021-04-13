---
title: " (Windows 事件記錄檔的 DataType 複雜類型) "
description: 定義資料項目。
ms.assetid: f3b7de63-1ac1-429d-9e36-1f13c26c9618
keywords:
- DataType 複雜型別 EventLog
topic_type:
- apiref
api_name:
- DataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d3ac6e545cbe8567bbe041568c442f762743ad0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317399"
---
# <a name="datatype-complex-type"></a><span data-ttu-id="02c32-104">DataType 複雜型別</span><span class="sxs-lookup"><span data-stu-id="02c32-104">DataType Complex Type</span></span>

<span data-ttu-id="02c32-105">定義資料項目。</span><span class="sxs-lookup"><span data-stu-id="02c32-105">Defines a data item.</span></span>

``` syntax
<xs:complexType name="DataType">
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="Name"
                type="string"
                use="optional"
             />
            <xs:attribute name="Type"
                type="QName"
                use="optional"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="02c32-106">屬性</span><span class="sxs-lookup"><span data-stu-id="02c32-106">Attributes</span></span>



| <span data-ttu-id="02c32-107">名稱</span><span class="sxs-lookup"><span data-stu-id="02c32-107">Name</span></span> | <span data-ttu-id="02c32-108">類型</span><span class="sxs-lookup"><span data-stu-id="02c32-108">Type</span></span>   | <span data-ttu-id="02c32-109">描述</span><span class="sxs-lookup"><span data-stu-id="02c32-109">Description</span></span>                                                                                                                                                              |
|------|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02c32-110">名稱</span><span class="sxs-lookup"><span data-stu-id="02c32-110">Name</span></span> | <span data-ttu-id="02c32-111">字串</span><span class="sxs-lookup"><span data-stu-id="02c32-111">string</span></span> | <span data-ttu-id="02c32-112">在範本中定義的資料項目名稱 (查看 [**TemplateItemType**](eventmanifestschema-templateitemtype-complextype.md) 複雜類型) 。</span><span class="sxs-lookup"><span data-stu-id="02c32-112">The name of a data item that was defined in the template (see the [**TemplateItemType**](eventmanifestschema-templateitemtype-complextype.md) complex type).</span></span><br/> |
| <span data-ttu-id="02c32-113">類型</span><span class="sxs-lookup"><span data-stu-id="02c32-113">Type</span></span> | <span data-ttu-id="02c32-114">QName</span><span class="sxs-lookup"><span data-stu-id="02c32-114">QName</span></span>  | <span data-ttu-id="02c32-115">未使用。</span><span class="sxs-lookup"><span data-stu-id="02c32-115">Not used.</span></span><br/>                                                                                                                                                     |



## <a name="remarks"></a><span data-ttu-id="02c32-116">備註</span><span class="sxs-lookup"><span data-stu-id="02c32-116">Remarks</span></span>

<span data-ttu-id="02c32-117">資料項目可以是最上層資料項目或結構中的資料項目。</span><span class="sxs-lookup"><span data-stu-id="02c32-117">The data item can be a top-level data item or a data item in a structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="02c32-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="02c32-118">Requirements</span></span>



| <span data-ttu-id="02c32-119">需求</span><span class="sxs-lookup"><span data-stu-id="02c32-119">Requirement</span></span> | <span data-ttu-id="02c32-120">值</span><span class="sxs-lookup"><span data-stu-id="02c32-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="02c32-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="02c32-121">Minimum supported client</span></span><br/> | <span data-ttu-id="02c32-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="02c32-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="02c32-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="02c32-123">Minimum supported server</span></span><br/> | <span data-ttu-id="02c32-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="02c32-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





