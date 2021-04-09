---
title: patternMap (PatternMapListType) 元素
description: 定義兩個正則運算式之間的對應。 其中一個運算式可用來在訊息字串中尋找相符的字串，而另一個運算式則用來在服務將字串放回訊息字串之前變更字串。
ms.assetid: 5cf28d38-4cc3-4a7b-a64b-3ad1cb42ebef
keywords:
- patternMap 元素 EventLog
topic_type:
- apiref
api_name:
- patternMap
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3ae29d60e39515a7c4b4db334f947abc44df5ddc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024524"
---
# <a name="patternmap-patternmaplisttype-element"></a><span data-ttu-id="37629-105">patternMap (PatternMapListType) 元素</span><span class="sxs-lookup"><span data-stu-id="37629-105">patternMap (PatternMapListType) Element</span></span>

<span data-ttu-id="37629-106">定義兩個正則運算式之間的對應。</span><span class="sxs-lookup"><span data-stu-id="37629-106">Defines a mapping between two regular expressions.</span></span> <span data-ttu-id="37629-107">其中一個運算式可用來在訊息字串中尋找相符的字串，而另一個運算式則用來在服務將字串放回訊息字串之前變更字串。</span><span class="sxs-lookup"><span data-stu-id="37629-107">One expression is used to find a matching string in the message string, and the other is used to alter the string before the service places it back in the message string.</span></span>

``` syntax
<xs:element name="patternMap"
    type="PatternMapType"
 />
```

<span data-ttu-id="37629-108">**PatternMap** 元素是由 [**PatternMapListType**](eventmanifestschema-patternmaplisttype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="37629-108">The **patternMap** element is defined by the [**PatternMapListType**](eventmanifestschema-patternmaplisttype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="37629-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="37629-109">Requirements</span></span>



| <span data-ttu-id="37629-110">需求</span><span class="sxs-lookup"><span data-stu-id="37629-110">Requirement</span></span> | <span data-ttu-id="37629-111">值</span><span class="sxs-lookup"><span data-stu-id="37629-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="37629-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="37629-112">Minimum supported client</span></span><br/> | <span data-ttu-id="37629-113">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="37629-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="37629-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="37629-114">Minimum supported server</span></span><br/> | <span data-ttu-id="37629-115">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="37629-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="37629-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="37629-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="37629-117">**父元素**</span><span class="sxs-lookup"><span data-stu-id="37629-117">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="37629-118">**patternMaps (NamedQueryType)**</span><span class="sxs-lookup"><span data-stu-id="37629-118">**patternMaps (NamedQueryType)**</span></span>](eventmanifestschema-patternmaps-namedquerytype-element.md)
</dt> </dl>

 

 





