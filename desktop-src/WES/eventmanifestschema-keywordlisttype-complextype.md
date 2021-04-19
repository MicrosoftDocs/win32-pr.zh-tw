---
title: KeywordListType 複雜類型
description: 定義分類事件的關鍵字清單。 |KeywordListType 複雜類型
ms.assetid: 7aeb5ca1-b23f-40f5-a77b-894deaf9c6bb
keywords:
- KeywordListType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- KeywordListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7132e2e85015aaf9d38adbd6278ea4d3e1296446
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106989155"
---
# <a name="keywordlisttype-complex-type"></a><span data-ttu-id="f9c16-105">KeywordListType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="f9c16-105">KeywordListType Complex Type</span></span>

<span data-ttu-id="f9c16-106">定義分類事件的關鍵字清單。</span><span class="sxs-lookup"><span data-stu-id="f9c16-106">Defines a list of keywords that categorize events.</span></span>

``` syntax
<xs:complexType name="KeywordListType">
    <xs:sequence>
        <xs:element name="keyword"
            type="KeywordType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="f9c16-107">子元素</span><span class="sxs-lookup"><span data-stu-id="f9c16-107">Child elements</span></span>



| <span data-ttu-id="f9c16-108">元素</span><span class="sxs-lookup"><span data-stu-id="f9c16-108">Element</span></span>                                                                | <span data-ttu-id="f9c16-109">類型</span><span class="sxs-lookup"><span data-stu-id="f9c16-109">Type</span></span>                                                               | <span data-ttu-id="f9c16-110">Description</span><span class="sxs-lookup"><span data-stu-id="f9c16-110">Description</span></span>                                                                                                  |
|------------------------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f9c16-111">**關鍵 字**</span><span class="sxs-lookup"><span data-stu-id="f9c16-111">**keyword**</span></span>](eventmanifestschema-keyword-keywordlisttype-element.md) | [<span data-ttu-id="f9c16-112">**KeywordType**</span><span class="sxs-lookup"><span data-stu-id="f9c16-112">**KeywordType**</span></span>](eventmanifestschema-keywordtype-complextype.md) | <span data-ttu-id="f9c16-113">定義可識別事件類別目錄的關鍵字。</span><span class="sxs-lookup"><span data-stu-id="f9c16-113">Defines a keyword that identifies a category of events.</span></span> <span data-ttu-id="f9c16-114">您可以指定最多48個關鍵字。</span><span class="sxs-lookup"><span data-stu-id="f9c16-114">You can specify a maximum of 48 keywords.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="f9c16-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="f9c16-115">Requirements</span></span>



| <span data-ttu-id="f9c16-116">需求</span><span class="sxs-lookup"><span data-stu-id="f9c16-116">Requirement</span></span> | <span data-ttu-id="f9c16-117">值</span><span class="sxs-lookup"><span data-stu-id="f9c16-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f9c16-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f9c16-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f9c16-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f9c16-119">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f9c16-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f9c16-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f9c16-121">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f9c16-121">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





