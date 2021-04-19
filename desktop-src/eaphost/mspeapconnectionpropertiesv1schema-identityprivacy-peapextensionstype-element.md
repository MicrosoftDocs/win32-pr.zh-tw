---
title: 'IdentityPrivacy (PeapExtensionsType) 元素 (v1) '
description: 指出是否傳送使用者的真實身分識別或匿名身分識別。 |IdentityPrivacy (PeapExtensionsType) 元素
ms.assetid: 1ae5b6e8-b1f8-45a7-ad22-fdb57cc756a2
keywords:
- 元素 EAPHost
topic_type:
- apiref
api_name:
- Username
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 748cf3ae8d5a4da4f8885332a72326bced45b398
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/05/2021
ms.locfileid: "106999770"
---
# <a name="identityprivacy-peapextensionstype-element"></a><span data-ttu-id="5f333-105">IdentityPrivacy (PeapExtensionsType) 元素</span><span class="sxs-lookup"><span data-stu-id="5f333-105">IdentityPrivacy (PeapExtensionsType) Element</span></span>

<span data-ttu-id="5f333-106">**IdentityPrivacy (PeapExtensionsType)** 元素指出是否傳送使用者的真實身分識別或匿名身分識別。</span><span class="sxs-lookup"><span data-stu-id="5f333-106">The **IdentityPrivacy (PeapExtensionsType)** element indicates whether a user's true identity or an anonymous identity is sent.</span></span>

``` syntax
<xs:element
    minOccurs="0"
    ref="extendedPeap:IdentityPrivacy"
 />
```

<span data-ttu-id="5f333-107">元素是由 [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) 元素所定義。</span><span class="sxs-lookup"><span data-stu-id="5f333-107">The element is defined by the [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f333-108">備註</span><span class="sxs-lookup"><span data-stu-id="5f333-108">Remarks</span></span>

<span data-ttu-id="5f333-109">**IdentityPrivacy** 元素是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="5f333-109">The **IdentityPrivacy** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f333-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="5f333-110">Requirements</span></span>



| <span data-ttu-id="5f333-111">需求</span><span class="sxs-lookup"><span data-stu-id="5f333-111">Requirement</span></span> | <span data-ttu-id="5f333-112">值</span><span class="sxs-lookup"><span data-stu-id="5f333-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="5f333-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5f333-113">Minimum supported client</span></span><br/> | <span data-ttu-id="5f333-114">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5f333-114">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="5f333-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5f333-115">Minimum supported server</span></span><br/> | <span data-ttu-id="5f333-116">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5f333-116">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5f333-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5f333-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="5f333-118">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="5f333-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="5f333-119">**PeapExtensionsType**</span><span class="sxs-lookup"><span data-stu-id="5f333-119">**PeapExtensionsType**</span></span>](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> <dt>

<span data-ttu-id="5f333-120">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="5f333-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="5f333-121">**PeapExtensions**</span><span class="sxs-lookup"><span data-stu-id="5f333-121">**PeapExtensions**</span></span>](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
<span data-ttu-id="5f333-122"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="5f333-122"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="5f333-123">EAPHost 和舊版架構</span><span class="sxs-lookup"><span data-stu-id="5f333-123">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="5f333-124">mspeapconnectionpropertiesv1 架構</span><span class="sxs-lookup"><span data-stu-id="5f333-124">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="5f333-125">mspeapconnectionpropertiesv1 架構元素</span><span class="sxs-lookup"><span data-stu-id="5f333-125">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> <dt>

[<span data-ttu-id="5f333-126">**IdentityPrivacy (PeapExtensionsType)**</span><span class="sxs-lookup"><span data-stu-id="5f333-126">**IdentityPrivacy(PeapExtensionsType)**</span></span>](mspeapconnectionpropertiesv2-identityprivacy-peapextensionstype-element.md)
</dt> </dl>

 

 





