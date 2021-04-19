---
title: BaseEapParameters 複雜類型-連接屬性
description: 定義方法類型和特定方法設定的預留位置元素。
ms.assetid: 510debce-545c-4ce1-965b-e4b2185b7983
keywords:
- BaseEapParameters 複雜類型 EAPHost
topic_type:
- apiref
api_name:
- BaseEapParameters
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f3bfb9f6c833900967525467202421cf94166405
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "106992356"
---
# <a name="baseeapparameters-complex-type---connection-properties"></a><span data-ttu-id="e6743-104">BaseEapParameters 複雜類型-連接屬性</span><span class="sxs-lookup"><span data-stu-id="e6743-104">BaseEapParameters Complex Type - Connection properties</span></span>

<span data-ttu-id="e6743-105">**BaseEapParameters** 複雜型別會定義方法類型和特定方法設定的預留位置元素。</span><span class="sxs-lookup"><span data-stu-id="e6743-105">The **BaseEapParameters** complex type defines the placeholder element for method type and method-specific configuration.</span></span>

``` syntax
<xs:complexType name="BaseEapParameters">
    <xs:sequence>
        <xs:element name="Type"
            type="integer"
         />
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##any"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="e6743-106">子元素</span><span class="sxs-lookup"><span data-stu-id="e6743-106">Child elements</span></span>



| <span data-ttu-id="e6743-107">元素</span><span class="sxs-lookup"><span data-stu-id="e6743-107">Element</span></span>                                                                            | <span data-ttu-id="e6743-108">類型</span><span class="sxs-lookup"><span data-stu-id="e6743-108">Type</span></span>    | <span data-ttu-id="e6743-109">Description</span><span class="sxs-lookup"><span data-stu-id="e6743-109">Description</span></span>                                     |
|------------------------------------------------------------------------------------|---------|-------------------------------------------------|
| [<span data-ttu-id="e6743-110">**類型**</span><span class="sxs-lookup"><span data-stu-id="e6743-110">**Type**</span></span>](baseeapconnectionpropertiesv1schema-type-baseeapparameters-element.md) | <span data-ttu-id="e6743-111">整數</span><span class="sxs-lookup"><span data-stu-id="e6743-111">integer</span></span> | <span data-ttu-id="e6743-112">此處允許任何架構實例。</span><span class="sxs-lookup"><span data-stu-id="e6743-112">Any schema instance is allowed here.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="e6743-113">備註</span><span class="sxs-lookup"><span data-stu-id="e6743-113">Remarks</span></span>

<span data-ttu-id="e6743-114">在 **BaseEapParameters** 中，方法可以定義構成元素。</span><span class="sxs-lookup"><span data-stu-id="e6743-114">In **BaseEapParameters** the method can define the constituent elements.</span></span> <span data-ttu-id="e6743-115">方法也會對 **BaseEapParameters** 中的元素執行架構驗證。</span><span class="sxs-lookup"><span data-stu-id="e6743-115">The method also performs schema validation on the elements in **BaseEapParameters**.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6743-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="e6743-116">Requirements</span></span>



| <span data-ttu-id="e6743-117">需求</span><span class="sxs-lookup"><span data-stu-id="e6743-117">Requirement</span></span> | <span data-ttu-id="e6743-118">值</span><span class="sxs-lookup"><span data-stu-id="e6743-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e6743-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e6743-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e6743-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e6743-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e6743-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e6743-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e6743-122">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e6743-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e6743-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e6743-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6743-124">EAPHost 和舊版架構</span><span class="sxs-lookup"><span data-stu-id="e6743-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="e6743-125">baseeapconnectionpropertiesv1 架構</span><span class="sxs-lookup"><span data-stu-id="e6743-125">baseeapconnectionpropertiesv1 Schema</span></span>](baseeapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





