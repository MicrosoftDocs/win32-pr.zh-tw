---
title: namedValues 複雜類型
description: 定義名稱/值組，其中名稱與值相關聯。
ms.assetid: 07c512fd-3eab-4238-8d75-83827a958a1e
keywords:
- namedValues 複雜類型工作排程器
topic_type:
- apiref
api_name:
- namedValues
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5f18c9fddab58f33ffc724a3e8df7bd65583cb88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686073"
---
# <a name="namedvalues-complex-type"></a><span data-ttu-id="5cbb8-104">namedValues 複雜類型</span><span class="sxs-lookup"><span data-stu-id="5cbb8-104">namedValues Complex Type</span></span>

<span data-ttu-id="5cbb8-105">定義名稱/值組，其中名稱與值相關聯。</span><span class="sxs-lookup"><span data-stu-id="5cbb8-105">Defines a name-value pair in which the name is associated with the value.</span></span>

``` syntax
<xs:complexType name="namedValues">
    <xs:sequence>
        <xs:element name="Value"
            type="namedValue"
            minOccurs="1"
            maxOccurs="32"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="5cbb8-106">子元素</span><span class="sxs-lookup"><span data-stu-id="5cbb8-106">Child elements</span></span>



| <span data-ttu-id="5cbb8-107">元素</span><span class="sxs-lookup"><span data-stu-id="5cbb8-107">Element</span></span>                                                        | <span data-ttu-id="5cbb8-108">類型</span><span class="sxs-lookup"><span data-stu-id="5cbb8-108">Type</span></span>                                                | <span data-ttu-id="5cbb8-109">Description</span><span class="sxs-lookup"><span data-stu-id="5cbb8-109">Description</span></span>                                                                         |
|----------------------------------------------------------------|-----------------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="5cbb8-110">**值**</span><span class="sxs-lookup"><span data-stu-id="5cbb8-110">**Value**</span></span>](taskschedulerschema-value-namedvalues-element.md) | [<span data-ttu-id="5cbb8-111">**namedValue**</span><span class="sxs-lookup"><span data-stu-id="5cbb8-111">**namedValue**</span></span>](schema-namedvalue-complextype.md) | <span data-ttu-id="5cbb8-112">指定與名稱/值配對中的名稱相關聯的值。</span><span class="sxs-lookup"><span data-stu-id="5cbb8-112">Specifies the value that is associated with a name in a name-value pair.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="5cbb8-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="5cbb8-113">Requirements</span></span>



| <span data-ttu-id="5cbb8-114">需求</span><span class="sxs-lookup"><span data-stu-id="5cbb8-114">Requirement</span></span> | <span data-ttu-id="5cbb8-115">值</span><span class="sxs-lookup"><span data-stu-id="5cbb8-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5cbb8-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5cbb8-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5cbb8-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5cbb8-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5cbb8-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5cbb8-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5cbb8-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5cbb8-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





