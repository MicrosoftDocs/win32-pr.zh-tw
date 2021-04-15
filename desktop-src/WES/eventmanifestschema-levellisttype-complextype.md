---
title: LevelListType 複雜類型
description: 定義嚴重性層級的清單，以指定事件的詳細程度。
ms.assetid: 82102f8a-271e-4c3d-9b0a-1e20eaa87497
keywords:
- LevelListType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- LevelListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4456ade3977603948997304393a1c9414cb0c458
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466961"
---
# <a name="levellisttype-complex-type"></a><span data-ttu-id="5e5a1-104">LevelListType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="5e5a1-104">LevelListType Complex Type</span></span>

<span data-ttu-id="5e5a1-105">定義嚴重性層級的清單，以指定事件的詳細程度。</span><span class="sxs-lookup"><span data-stu-id="5e5a1-105">Defines a list of severity levels that specify the verbosity of an event.</span></span>

``` syntax
<xs:complexType name="LevelListType">
    <xs:sequence>
        <xs:element name="level"
            type="LevelType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="5e5a1-106">子元素</span><span class="sxs-lookup"><span data-stu-id="5e5a1-106">Child elements</span></span>



| <span data-ttu-id="5e5a1-107">元素</span><span class="sxs-lookup"><span data-stu-id="5e5a1-107">Element</span></span>                                                          | <span data-ttu-id="5e5a1-108">類型</span><span class="sxs-lookup"><span data-stu-id="5e5a1-108">Type</span></span>                                                           | <span data-ttu-id="5e5a1-109">Description</span><span class="sxs-lookup"><span data-stu-id="5e5a1-109">Description</span></span>                                                                                 |
|------------------------------------------------------------------|----------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5e5a1-110">**水準**</span><span class="sxs-lookup"><span data-stu-id="5e5a1-110">**level**</span></span>](eventmanifestschema-level-levellisttype-element.md) | [<span data-ttu-id="5e5a1-111">**LevelType**</span><span class="sxs-lookup"><span data-stu-id="5e5a1-111">**LevelType**</span></span>](eventmanifestschema-leveltype-complextype.md) | <span data-ttu-id="5e5a1-112">定義嚴重性值，以判斷記錄期間事件的詳細程度。</span><span class="sxs-lookup"><span data-stu-id="5e5a1-112">Defines a severity value that determines the verbosity of events during logging.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="5e5a1-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="5e5a1-113">Requirements</span></span>



| <span data-ttu-id="5e5a1-114">需求</span><span class="sxs-lookup"><span data-stu-id="5e5a1-114">Requirement</span></span> | <span data-ttu-id="5e5a1-115">值</span><span class="sxs-lookup"><span data-stu-id="5e5a1-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5e5a1-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5e5a1-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5e5a1-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5e5a1-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5e5a1-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5e5a1-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5e5a1-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5e5a1-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





