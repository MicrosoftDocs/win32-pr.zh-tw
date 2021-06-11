---
title: 'IdentityPrivacy (PeapExtensionsType) 元素 (v1) '
description: IdentityPrivacy (PeapExtensionsType) 元素指出是否在 mspeapconnectionpropertiesv1 架構中傳送使用者的真實身分識別。
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
ms.openlocfilehash: 7195ce43fb3f1a1f1710fe7aee3f5f74e18f3786
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989213"
---
# <a name="identityprivacy-peapextensionstype-element"></a><span data-ttu-id="12270-104">IdentityPrivacy (PeapExtensionsType) 元素</span><span class="sxs-lookup"><span data-stu-id="12270-104">IdentityPrivacy (PeapExtensionsType) Element</span></span>

<span data-ttu-id="12270-105">**IdentityPrivacy (PeapExtensionsType)** 元素指出是否傳送使用者的真實身分識別或匿名身分識別。</span><span class="sxs-lookup"><span data-stu-id="12270-105">The **IdentityPrivacy (PeapExtensionsType)** element indicates whether a user's true identity or an anonymous identity is sent.</span></span>

``` syntax
<xs:element
    minOccurs="0"
    ref="extendedPeap:IdentityPrivacy"
 />
```

<span data-ttu-id="12270-106">元素是由 [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) 元素所定義。</span><span class="sxs-lookup"><span data-stu-id="12270-106">The element is defined by the [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="12270-107">備註</span><span class="sxs-lookup"><span data-stu-id="12270-107">Remarks</span></span>

<span data-ttu-id="12270-108">**IdentityPrivacy** 元素是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="12270-108">The **IdentityPrivacy** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="12270-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="12270-109">Requirements</span></span>



| <span data-ttu-id="12270-110">需求</span><span class="sxs-lookup"><span data-stu-id="12270-110">Requirement</span></span> | <span data-ttu-id="12270-111">值</span><span class="sxs-lookup"><span data-stu-id="12270-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="12270-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="12270-112">Minimum supported client</span></span><br/> | <span data-ttu-id="12270-113">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="12270-113">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="12270-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="12270-114">Minimum supported server</span></span><br/> | <span data-ttu-id="12270-115">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="12270-115">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="12270-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="12270-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="12270-117">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="12270-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="12270-118">**PeapExtensionsType**</span><span class="sxs-lookup"><span data-stu-id="12270-118">**PeapExtensionsType**</span></span>](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> <dt>

<span data-ttu-id="12270-119">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="12270-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="12270-120">**PeapExtensions**</span><span class="sxs-lookup"><span data-stu-id="12270-120">**PeapExtensions**</span></span>](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
<span data-ttu-id="12270-121"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="12270-121"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="12270-122">EAPHost 和舊版架構</span><span class="sxs-lookup"><span data-stu-id="12270-122">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="12270-123">mspeapconnectionpropertiesv1 架構</span><span class="sxs-lookup"><span data-stu-id="12270-123">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="12270-124">mspeapconnectionpropertiesv1 架構元素</span><span class="sxs-lookup"><span data-stu-id="12270-124">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> <dt>

[<span data-ttu-id="12270-125">**IdentityPrivacy (PeapExtensionsType)**</span><span class="sxs-lookup"><span data-stu-id="12270-125">**IdentityPrivacy(PeapExtensionsType)**</span></span>](mspeapconnectionpropertiesv2-identityprivacy-peapextensionstype-element.md)
</dt> </dl>

 

 





