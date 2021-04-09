---
title: PeapExtensionsTypeV2 複雜類型
description: 瞭解 PeapExtensionsTypeV2 複雜類型。 此類型可讓架構的未來增強功能。
ms.assetid: cb011182-afec-4813-bd56-add894c74c9c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 869e67f16bc9b42929d227755e08bf6924dcc737
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103933626"
---
# <a name="peapextensionstypev2-complex-type"></a><span data-ttu-id="b7865-104">PeapExtensionsTypeV2 複雜類型</span><span class="sxs-lookup"><span data-stu-id="b7865-104">PeapExtensionsTypeV2 Complex Type</span></span>

<span data-ttu-id="b7865-105">**PeapExtensionsTypeV2** 複雜型別可讓架構的未來增強功能。</span><span class="sxs-lookup"><span data-stu-id="b7865-105">The **PeapExtensionsTypeV2** complex type enables future enhancements to the schema.</span></span>


```XML
<xs:complexType name="PeapExtensionsTypeV2">
    <xs:sequence>
        <xs:any processContents="lax" 
            minOccurs="0" 
            maxOccurs="unbounded" 
            namespace="##other"
        />
    <xs:sequence>
</xs:complexType>

```



## <a name="remarks"></a><span data-ttu-id="b7865-106">備註</span><span class="sxs-lookup"><span data-stu-id="b7865-106">Remarks</span></span>

<span data-ttu-id="b7865-107">**PeapExtensionsTypeV2** 元素是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="b7865-107">The **PeapExtensionsTypeV2** element is optional.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b7865-108">相關主題</span><span class="sxs-lookup"><span data-stu-id="b7865-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7865-109">EAPHost 和舊版架構</span><span class="sxs-lookup"><span data-stu-id="b7865-109">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="b7865-110">mspeapconnectionpropertiesv2 架構</span><span class="sxs-lookup"><span data-stu-id="b7865-110">mspeapconnectionpropertiesv2 Schema</span></span>](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[<span data-ttu-id="b7865-111">mspeapconnectionpropertiesv2 複雜類型</span><span class="sxs-lookup"><span data-stu-id="b7865-111">mspeapconnectionpropertiesv2 Complex Types</span></span>](mspeapconnectionpropertiesv2schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="b7865-112">**PeapExtensionsType**</span><span class="sxs-lookup"><span data-stu-id="b7865-112">**PeapExtensionsType**</span></span>](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> </dl>

 

 




