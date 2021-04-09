---
title: principalsType 複雜類型
description: 定義主體元素的子項目。
ms.assetid: a501534b-eb0f-480f-a2c9-d2015262a9a7
keywords:
- principalsType 複雜類型工作排程器
topic_type:
- apiref
api_name:
- principalsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 56cd26a4dff31ce86b218e5a4a2662d678327625
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934013"
---
# <a name="principalstype-complex-type"></a><span data-ttu-id="53a13-104">principalsType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="53a13-104">principalsType Complex Type</span></span>

<span data-ttu-id="53a13-105">定義 [**主體**](taskschedulerschema-principals-tasktype-element.md) 元素的子項目。</span><span class="sxs-lookup"><span data-stu-id="53a13-105">Defines the child element for the [**Principals**](taskschedulerschema-principals-tasktype-element.md) element.</span></span>

``` syntax
<xs:complexType name="principalsType">
    <xs:sequence>
        <xs:element name="Principal"
            type="principalType"
            maxOccurs="1"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="53a13-106">子元素</span><span class="sxs-lookup"><span data-stu-id="53a13-106">Child elements</span></span>



| <span data-ttu-id="53a13-107">元素</span><span class="sxs-lookup"><span data-stu-id="53a13-107">Element</span></span>                                                                  | <span data-ttu-id="53a13-108">類型</span><span class="sxs-lookup"><span data-stu-id="53a13-108">Type</span></span>                                                                   | <span data-ttu-id="53a13-109">Description</span><span class="sxs-lookup"><span data-stu-id="53a13-109">Description</span></span>                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="53a13-110">**主要**</span><span class="sxs-lookup"><span data-stu-id="53a13-110">**Principal**</span></span>](taskschedulerschema-principal-principaltype-element.md) | [<span data-ttu-id="53a13-111">**principalType**</span><span class="sxs-lookup"><span data-stu-id="53a13-111">**principalType**</span></span>](taskschedulerschema-principaltype-complextype.md) | <span data-ttu-id="53a13-112">指定主體的安全性認證。</span><span class="sxs-lookup"><span data-stu-id="53a13-112">Specifies the security credentials for a principal.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="53a13-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="53a13-113">Requirements</span></span>



| <span data-ttu-id="53a13-114">需求</span><span class="sxs-lookup"><span data-stu-id="53a13-114">Requirement</span></span> | <span data-ttu-id="53a13-115">值</span><span class="sxs-lookup"><span data-stu-id="53a13-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="53a13-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="53a13-116">Minimum supported client</span></span><br/> | <span data-ttu-id="53a13-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="53a13-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="53a13-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="53a13-118">Minimum supported server</span></span><br/> | <span data-ttu-id="53a13-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="53a13-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





