---
title: TLSExtensionsType 複雜類型
description: 瞭解 TLSExtensionsType 複雜類型。 此類型可讓架構的未來增強功能。
ms.assetid: 5e4f8ef8-1adb-4683-8001-ba7d2d392523
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 833a93b9ecb0ba32a95e4c85856ac015f5135fb5
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103683115"
---
# <a name="tlsextensionstype-complex-type"></a><span data-ttu-id="ab1bd-104">TLSExtensionsType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="ab1bd-104">TLSExtensionsType Complex Type</span></span>

<span data-ttu-id="ab1bd-105">**TLSExtensionsType** 複雜型別可讓架構的未來增強功能。</span><span class="sxs-lookup"><span data-stu-id="ab1bd-105">The **TLSExtensionsType** complex type enables future enhancements to the schema.</span></span>


```XML
<xs:complexType name="TLSExtensionsType">
    <xs:sequence>
        <xs:any processContents="lax" 
            minOccurs="0" 
            maxOccurs="unbounded" 
            namespace="##other"
        />
    <xs:sequence>
</xs:complexType>

```



## <a name="remarks"></a><span data-ttu-id="ab1bd-106">備註</span><span class="sxs-lookup"><span data-stu-id="ab1bd-106">Remarks</span></span>

<span data-ttu-id="ab1bd-107">**TLSExtensionsType** 元素是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="ab1bd-107">The **TLSExtensionsType** element is optional.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ab1bd-108">相關主題</span><span class="sxs-lookup"><span data-stu-id="ab1bd-108">Related topics</span></span>

<dl> <span data-ttu-id="ab1bd-109"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="ab1bd-109"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="ab1bd-110">EAPHost 和舊版架構</span><span class="sxs-lookup"><span data-stu-id="ab1bd-110">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="ab1bd-111">eaptlsconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="ab1bd-111">eaptlsconnectionpropertiesv2</span></span>](eaptlsconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[<span data-ttu-id="ab1bd-112">eaptlsconnectionpropertiesv2 複雜類型</span><span class="sxs-lookup"><span data-stu-id="ab1bd-112">eaptlsconnectionpropertiesv2 Complex Types</span></span>](eaptlsconnectionpropertiesv2schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="ab1bd-113">**TLSExtensions (TLSExtensionsType)**</span><span class="sxs-lookup"><span data-stu-id="ab1bd-113">**TLSExtensions (TLSExtensionsType)**</span></span>](eaptlsconnectionpropertiesv2schema-performservervalidation-eaptype-element.md)
</dt> </dl>

 

 




