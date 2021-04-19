---
title: BaseEapParameters 複雜類型-使用者屬性
description: 定義專案，指定選取的舊版方法和方法特定的認證。
ms.assetid: bc42e536-f741-4821-8453-6c0631daad3e
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
ms.openlocfilehash: 451c03123634dd98a1f4a49292db0a807009f6f5
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "106985919"
---
# <a name="baseeapparameters-complex-type---user-properties"></a><span data-ttu-id="2d673-104">BaseEapParameters 複雜類型-使用者屬性</span><span class="sxs-lookup"><span data-stu-id="2d673-104">BaseEapParameters Complex Type - User properties</span></span>

<span data-ttu-id="2d673-105">**BaseEapParameters** 複雜型別會定義指定舊版方法的元素，以及特定方法的認證。</span><span class="sxs-lookup"><span data-stu-id="2d673-105">The **BaseEapParameters** complex type defines the element that specified the legacy method selected and method-specific credentials.</span></span>

<span data-ttu-id="2d673-106">方法可以定義 **BaseEapParameters** 內的組成元素;方法也會對 **BaseEapParameters** 中的元素執行架構驗證。</span><span class="sxs-lookup"><span data-stu-id="2d673-106">The method can define the constituent elements inside **BaseEapParameters**; the method also performs schema validation on the elements in **BaseEapParameters**.</span></span>

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

## <a name="child-elements"></a><span data-ttu-id="2d673-107">子元素</span><span class="sxs-lookup"><span data-stu-id="2d673-107">Child elements</span></span>



| <span data-ttu-id="2d673-108">元素</span><span class="sxs-lookup"><span data-stu-id="2d673-108">Element</span></span>                                                                      | <span data-ttu-id="2d673-109">類型</span><span class="sxs-lookup"><span data-stu-id="2d673-109">Type</span></span>    | <span data-ttu-id="2d673-110">Description</span><span class="sxs-lookup"><span data-stu-id="2d673-110">Description</span></span>                                                                                               |
|------------------------------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2d673-111">**類型**</span><span class="sxs-lookup"><span data-stu-id="2d673-111">**Type**</span></span>](baseeapuserpropertiesv1schema-type-baseeapparameters-element.md) | <span data-ttu-id="2d673-112">整數</span><span class="sxs-lookup"><span data-stu-id="2d673-112">integer</span></span> | <span data-ttu-id="2d673-113">定義所選方法類型的預留位置元素，以及方法特定的認證。</span><span class="sxs-lookup"><span data-stu-id="2d673-113">Defines the placeholder element for the method type selected and method specific credentials.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="2d673-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="2d673-114">Requirements</span></span>



| <span data-ttu-id="2d673-115">需求</span><span class="sxs-lookup"><span data-stu-id="2d673-115">Requirement</span></span> | <span data-ttu-id="2d673-116">值</span><span class="sxs-lookup"><span data-stu-id="2d673-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2d673-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2d673-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2d673-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2d673-118">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2d673-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2d673-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2d673-120">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2d673-120">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2d673-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2d673-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d673-122">EAPHost 和舊版架構</span><span class="sxs-lookup"><span data-stu-id="2d673-122">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="2d673-123">baseeapuserpropertiesv1 架構</span><span class="sxs-lookup"><span data-stu-id="2d673-123">baseeapuserpropertiesv1 Schema</span></span>](baseeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





