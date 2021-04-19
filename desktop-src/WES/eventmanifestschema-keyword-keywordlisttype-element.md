---
title: 關鍵字 (KeywordListType) 元素
description: 定義可識別事件類別目錄的關鍵字。 |關鍵字 (KeywordListType) 元素
ms.assetid: c921eb01-f1b0-455c-8ff9-06895f1e40f9
keywords:
- 關鍵字元素 EventLog
topic_type:
- apiref
api_name:
- keyword
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f4b1b0b60502339db55c3227add9bb5a263200aa
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106986707"
---
# <a name="keyword-keywordlisttype-element"></a><span data-ttu-id="e5294-105">關鍵字 (KeywordListType) 元素</span><span class="sxs-lookup"><span data-stu-id="e5294-105">keyword (KeywordListType) Element</span></span>

<span data-ttu-id="e5294-106">定義可識別事件類別目錄的關鍵字。</span><span class="sxs-lookup"><span data-stu-id="e5294-106">Defines a keyword that identifies a category of events.</span></span> <span data-ttu-id="e5294-107">關鍵字是您附加至事件的標籤，用來根據事件的使用方式將事件分組。</span><span class="sxs-lookup"><span data-stu-id="e5294-107">A keyword is a tag that you attach to an event to group events based on their usage.</span></span>

``` syntax
<xs:element name="keyword"
    type="KeywordType"
 />
```

<span data-ttu-id="e5294-108">**關鍵字** 元素是由 [**KeywordListType**](eventmanifestschema-keywordlisttype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="e5294-108">The **keyword** element is defined by the [**KeywordListType**](eventmanifestschema-keywordlisttype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5294-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="e5294-109">Requirements</span></span>



| <span data-ttu-id="e5294-110">需求</span><span class="sxs-lookup"><span data-stu-id="e5294-110">Requirement</span></span> | <span data-ttu-id="e5294-111">值</span><span class="sxs-lookup"><span data-stu-id="e5294-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e5294-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e5294-112">Minimum supported client</span></span><br/> | <span data-ttu-id="e5294-113">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e5294-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e5294-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e5294-114">Minimum supported server</span></span><br/> | <span data-ttu-id="e5294-115">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e5294-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e5294-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e5294-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="e5294-117">**父元素**</span><span class="sxs-lookup"><span data-stu-id="e5294-117">**Parent elements**</span></span>
</dt> <dt>

[<span data-ttu-id="e5294-118">**關鍵字 (ProviderType)**</span><span class="sxs-lookup"><span data-stu-id="e5294-118">**keywords (ProviderType)**</span></span>](eventmanifestschema-keywords-providertype-element.md)
</dt> <dt>

[<span data-ttu-id="e5294-119">**關鍵字 (MetadataType)**</span><span class="sxs-lookup"><span data-stu-id="e5294-119">**keywords (MetadataType)**</span></span>](eventmanifestschema-keywords-metadatatype-element.md)
</dt> </dl>

 

 





