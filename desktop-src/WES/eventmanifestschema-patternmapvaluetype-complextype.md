---
title: PatternMapValueType 複雜類型
description: 未使用。 定義用來在訊息字串中尋找相符字串的正則運算式，並加以修改。
ms.assetid: 2ae8a268-64c0-45d1-8339-988b13d884a3
keywords:
- PatternMapValueType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- PatternMapValueType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 55b57b63f3e5c9e5a5c4cd15974c89f6d28439f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685465"
---
# <a name="patternmapvaluetype-complex-type"></a><span data-ttu-id="b4aa9-105">PatternMapValueType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="b4aa9-105">PatternMapValueType Complex Type</span></span>

<span data-ttu-id="b4aa9-106">未使用。</span><span class="sxs-lookup"><span data-stu-id="b4aa9-106">Not used.</span></span> <span data-ttu-id="b4aa9-107">定義用來在訊息字串中尋找相符字串的正則運算式，並加以修改。</span><span class="sxs-lookup"><span data-stu-id="b4aa9-107">Defines the regular expressions used to find a matching string in the message string and alter it.</span></span>

``` syntax
<xs:complexType name="PatternMapValueType">
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="name"
                type="string"
                use="required"
             />
            <xs:attribute name="value"
                type="string"
                use="required"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="b4aa9-108">屬性</span><span class="sxs-lookup"><span data-stu-id="b4aa9-108">Attributes</span></span>



| <span data-ttu-id="b4aa9-109">名稱</span><span class="sxs-lookup"><span data-stu-id="b4aa9-109">Name</span></span>  | <span data-ttu-id="b4aa9-110">類型</span><span class="sxs-lookup"><span data-stu-id="b4aa9-110">Type</span></span>   | <span data-ttu-id="b4aa9-111">描述</span><span class="sxs-lookup"><span data-stu-id="b4aa9-111">Description</span></span>                                                                                               |
|-------|--------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4aa9-112">NAME</span><span class="sxs-lookup"><span data-stu-id="b4aa9-112">name</span></span>  | <span data-ttu-id="b4aa9-113">字串</span><span class="sxs-lookup"><span data-stu-id="b4aa9-113">string</span></span> | <span data-ttu-id="b4aa9-114">用來在訊息字串中尋找相符字串的正則運算式。</span><span class="sxs-lookup"><span data-stu-id="b4aa9-114">The regular expression used to find a matching string in the message string.</span></span><br/>                   |
| <span data-ttu-id="b4aa9-115">value</span><span class="sxs-lookup"><span data-stu-id="b4aa9-115">value</span></span> | <span data-ttu-id="b4aa9-116">字串</span><span class="sxs-lookup"><span data-stu-id="b4aa9-116">string</span></span> | <span data-ttu-id="b4aa9-117">用來改變在訊息字串中找到之相符字串的正則運算式。</span><span class="sxs-lookup"><span data-stu-id="b4aa9-117">The regular expression used to alter the matching string that was found in the message string.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="b4aa9-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="b4aa9-118">Requirements</span></span>



| <span data-ttu-id="b4aa9-119">需求</span><span class="sxs-lookup"><span data-stu-id="b4aa9-119">Requirement</span></span> | <span data-ttu-id="b4aa9-120">值</span><span class="sxs-lookup"><span data-stu-id="b4aa9-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b4aa9-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b4aa9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b4aa9-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b4aa9-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b4aa9-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b4aa9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b4aa9-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b4aa9-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





