---
title: 'EapType 元素 (mspeapuserpropertiesv1schema) '
description: 這個元素是 baseeapuserpropertiesv1 架構中 EapType 元素的衍生型別。 適用于 mspeapuserpropertiesv1schema。
ms.assetid: 921c1f95-900a-4fd2-bb42-341e5ba39b23
keywords:
- EapType 元素 EAPHost
topic_type:
- apiref
api_name:
- EapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ccedc72baf3a677acc3a318895defbc97bb26287
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/02/2021
ms.locfileid: "106998649"
---
# <a name="eaptype-element-mspeapuserpropertiesv1schema"></a><span data-ttu-id="63379-105">EapType 元素 (mspeapuserpropertiesv1schema) </span><span class="sxs-lookup"><span data-stu-id="63379-105">EapType Element (mspeapuserpropertiesv1schema)</span></span>

<span data-ttu-id="63379-106">**EapType** 元素是 [Baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md)架構中 [**EapType**](baseeapuserpropertiesv1schema-eaptype-element.md)元素的衍生型別。</span><span class="sxs-lookup"><span data-stu-id="63379-106">The **EapType** element is a derived type of the [**EapType**](baseeapuserpropertiesv1schema-eaptype-element.md) element from the [baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md) schema.</span></span>

``` syntax
<xs:element name="EapType
        "
    substitutionGroup="EapType"
>
    <xs:complexType>
        <xs:complexContent>
            <xs:extension
                base="BaseEapTypeParameters"
            >
                <xs:sequence>
                    <xs:element
                        minOccurs="0"
                        maxOccurs="unbounded"
                        ref="Eap"
                     />
                    <xs:element name="PeapExtensions"
                        type="PeapExtensionsType"
                        minOccurs="0"
                     />
                </xs:sequence>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="63379-107">子元素</span><span class="sxs-lookup"><span data-stu-id="63379-107">Child elements</span></span>



| <span data-ttu-id="63379-108">元素</span><span class="sxs-lookup"><span data-stu-id="63379-108">Element</span></span>                                                                               | <span data-ttu-id="63379-109">類型</span><span class="sxs-lookup"><span data-stu-id="63379-109">Type</span></span>                                                                                      | <span data-ttu-id="63379-110">Description</span><span class="sxs-lookup"><span data-stu-id="63379-110">Description</span></span>                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="63379-111">**Eap**</span><span class="sxs-lookup"><span data-stu-id="63379-111">**Eap**</span></span>](baseeapuserpropertiesv1schema-eap-element.md)                              |                                                                                           | <span data-ttu-id="63379-112">[**Eap**](baseeapuserpropertiesv1schema-eap-element.md)元素會識別要搭配該方法使用的內部方法和認證。</span><span class="sxs-lookup"><span data-stu-id="63379-112">The [**Eap**](baseeapuserpropertiesv1schema-eap-element.md) element identifies the inner method and the credentials to be used with that method.</span></span> <span data-ttu-id="63379-113">當您針對 PEAP 來賓存取設定 PEAP 設定時，不會出現這個元素。</span><span class="sxs-lookup"><span data-stu-id="63379-113">When PEAP configuration is configured for PEAP guest access, this element is absent.</span></span><br/>                                  |
| [<span data-ttu-id="63379-114">**PeapExtensions**</span><span class="sxs-lookup"><span data-stu-id="63379-114">**PeapExtensions**</span></span>](mspeapuserpropertiesv1schema-peapextensions-eaptype-element.md) | [<span data-ttu-id="63379-115">**PeapExtensionsType**</span><span class="sxs-lookup"><span data-stu-id="63379-115">**PeapExtensionsType**</span></span>](mspeapuserpropertiesv1schema-peapextensionstype-complextype.md) | <span data-ttu-id="63379-116">[**PeapExtensions**](mspeapuserpropertiesv1schema-peapextensions-eaptype-element.md)元素可讓架構的未來增強功能。</span><span class="sxs-lookup"><span data-stu-id="63379-116">The [**PeapExtensions**](mspeapuserpropertiesv1schema-peapextensions-eaptype-element.md) element enables future enhancements to the schema.</span></span> <br/> <span data-ttu-id="63379-117">[**PeapExtensions**](mspeapuserpropertiesv1schema-peapextensions-eaptype-element.md)元素是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="63379-117">The [**PeapExtensions**](mspeapuserpropertiesv1schema-peapextensions-eaptype-element.md) element is optional.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="63379-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="63379-118">Requirements</span></span>



| <span data-ttu-id="63379-119">需求</span><span class="sxs-lookup"><span data-stu-id="63379-119">Requirement</span></span> | <span data-ttu-id="63379-120">值</span><span class="sxs-lookup"><span data-stu-id="63379-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="63379-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="63379-121">Minimum supported client</span></span><br/> | <span data-ttu-id="63379-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="63379-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="63379-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="63379-123">Minimum supported server</span></span><br/> | <span data-ttu-id="63379-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="63379-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="63379-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="63379-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63379-126">EAPHost 和舊版架構</span><span class="sxs-lookup"><span data-stu-id="63379-126">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="63379-127">mspeapuserpropertiesv1 架構</span><span class="sxs-lookup"><span data-stu-id="63379-127">mspeapuserpropertiesv1 Schema</span></span>](mspeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





