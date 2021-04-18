---
title: 'TLSExtensions (v1 架構) '
description: 瞭解 TLSExtensions (EapType) 元素。 此元素可讓您針對架構進行未來的增強。
ms.assetid: f968d91d-e226-44a9-98db-347cbedfa201
keywords:
- 元素 EAPHost
topic_type:
- apiref
api_name:
- TLSExtensions
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 886f1ab2a6f00a4a8a9d530fa41865b2fd0cf0b8
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "106968516"
---
# <a name="tlsextensions-v1-schema"></a><span data-ttu-id="ccd19-105">TLSExtensions (v1 架構) </span><span class="sxs-lookup"><span data-stu-id="ccd19-105">TLSExtensions (v1 schema)</span></span>

<span data-ttu-id="ccd19-106">**TLSExtensions (EapType)** 專案可讓架構的未來增強功能。</span><span class="sxs-lookup"><span data-stu-id="ccd19-106">The **TLSExtensions (EapType)** element enables future enhancements to the schema.</span></span>

``` syntax
<xs:element
    minOccurs="0"
    maxOccurs="1"
    ref="extendedTLS: TLSExtensions"
 />
```

<span data-ttu-id="ccd19-107">元素是由 [**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) 元素所定義。</span><span class="sxs-lookup"><span data-stu-id="ccd19-107">The element is defined by the [**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="ccd19-108">備註</span><span class="sxs-lookup"><span data-stu-id="ccd19-108">Remarks</span></span>

<span data-ttu-id="ccd19-109">**TLSExtensions** 元素是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="ccd19-109">The **TLSExtensions** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="ccd19-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="ccd19-110">Requirements</span></span>



| <span data-ttu-id="ccd19-111">角色</span><span class="sxs-lookup"><span data-stu-id="ccd19-111">Role</span></span> | <span data-ttu-id="ccd19-112">最低支援作業系統版本</span><span class="sxs-lookup"><span data-stu-id="ccd19-112">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="ccd19-113">用戶端</span><span class="sxs-lookup"><span data-stu-id="ccd19-113">Client</span></span><br/> | <span data-ttu-id="ccd19-114">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ccd19-114">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="ccd19-115">伺服器</span><span class="sxs-lookup"><span data-stu-id="ccd19-115">Server</span></span><br/> | <span data-ttu-id="ccd19-116">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ccd19-116">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ccd19-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ccd19-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="ccd19-118">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="ccd19-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="ccd19-119">**EapType**</span><span class="sxs-lookup"><span data-stu-id="ccd19-119">**EapType**</span></span>](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="ccd19-120">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="ccd19-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="ccd19-121">**EapType**</span><span class="sxs-lookup"><span data-stu-id="ccd19-121">**EapType**</span></span>](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
<span data-ttu-id="ccd19-122"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="ccd19-122"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="ccd19-123">EAPHost 和舊版架構</span><span class="sxs-lookup"><span data-stu-id="ccd19-123">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="ccd19-124">eaptlsconnectionpropertiesv1 架構</span><span class="sxs-lookup"><span data-stu-id="ccd19-124">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="ccd19-125">eaptlsconnectionpropertiesv1 架構元素</span><span class="sxs-lookup"><span data-stu-id="ccd19-125">eaptlsconnectionpropertiesv1 Schema Elements</span></span>](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> <dt>

[<span data-ttu-id="ccd19-126">**TLSExtensions (TLSExtensionsType)**</span><span class="sxs-lookup"><span data-stu-id="ccd19-126">**TLSExtensions (TLSExtensionsType)**</span></span>](eaptlsconnectionpropertiesv2schema-performservervalidation-eaptype-element.md)
</dt> </dl>

 

 





