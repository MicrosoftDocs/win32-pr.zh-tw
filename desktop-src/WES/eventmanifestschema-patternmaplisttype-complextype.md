---
title: PatternMapListType 複雜類型
description: 未使用。 定義用來改變訊息字串的正則運算式組清單。
ms.assetid: f7b92821-a959-4b91-9e7e-47d0136ee61f
keywords:
- PatternMapListType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- PatternMapListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5d1bb655dcf13c70fb989756cb9f5716301934c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317099"
---
# <a name="patternmaplisttype-complex-type"></a><span data-ttu-id="de834-105">PatternMapListType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="de834-105">PatternMapListType Complex Type</span></span>

<span data-ttu-id="de834-106">未使用。</span><span class="sxs-lookup"><span data-stu-id="de834-106">Not used.</span></span> <span data-ttu-id="de834-107">定義用來改變訊息字串的正則運算式組清單。</span><span class="sxs-lookup"><span data-stu-id="de834-107">Defines a list of regular expression pairs that are used to alter the message string.</span></span>

``` syntax
<xs:complexType name="PatternMapListType">
    <xs:sequence>
        <xs:element name="patternMap"
            type="PatternMapType"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="de834-108">子元素</span><span class="sxs-lookup"><span data-stu-id="de834-108">Child elements</span></span>



| <span data-ttu-id="de834-109">元素</span><span class="sxs-lookup"><span data-stu-id="de834-109">Element</span></span>                                                                         | <span data-ttu-id="de834-110">類型</span><span class="sxs-lookup"><span data-stu-id="de834-110">Type</span></span>                                                                     | <span data-ttu-id="de834-111">Description</span><span class="sxs-lookup"><span data-stu-id="de834-111">Description</span></span>                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="de834-112">**patternMap**</span><span class="sxs-lookup"><span data-stu-id="de834-112">**patternMap**</span></span>](eventmanifestschema-patternmap-patternmaplisttype-element.md) | [<span data-ttu-id="de834-113">**PatternMapType**</span><span class="sxs-lookup"><span data-stu-id="de834-113">**PatternMapType**</span></span>](eventmanifestschema-patternmaptype-complextype.md) | <span data-ttu-id="de834-114">定義兩個正則運算式之間的對應。</span><span class="sxs-lookup"><span data-stu-id="de834-114">Defines a mapping between two regular expressions.</span></span> <span data-ttu-id="de834-115">其中一個運算式可用來在訊息字串中尋找相符的字串，而另一個運算式則是用來在服務將字串放回訊息字串之前變更字串。</span><span class="sxs-lookup"><span data-stu-id="de834-115">One expression is used to find a matching string in the message string and the other is used to alter the string before the service places it back in the message string.</span></span> <span data-ttu-id="de834-116">使用符合的第一個模式對應，且不會嘗試其他模式。</span><span class="sxs-lookup"><span data-stu-id="de834-116">The first pattern mapping that matches is used and other patterns are not tried.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="de834-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="de834-117">Requirements</span></span>



| <span data-ttu-id="de834-118">需求</span><span class="sxs-lookup"><span data-stu-id="de834-118">Requirement</span></span> | <span data-ttu-id="de834-119">值</span><span class="sxs-lookup"><span data-stu-id="de834-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="de834-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="de834-120">Minimum supported client</span></span><br/> | <span data-ttu-id="de834-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="de834-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="de834-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="de834-122">Minimum supported server</span></span><br/> | <span data-ttu-id="de834-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="de834-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





