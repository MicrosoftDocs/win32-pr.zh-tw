---
title: IdentityPrivacy (PeapExtensionsType) 元素
description: 指出是否傳送使用者的真實身分識別或匿名身分識別。 |IdentityPrivacy (PeapExtensionsType) 元素
ms.assetid: 57b8747e-6919-4243-a379-3a85c4a2023a
keywords:
- IdentityPrivacy 元素 EAPHost
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
ms.openlocfilehash: 2701352ee0e192dfd2d33fc2647b9ec6df96dd5c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104514421"
---
# <a name="the-identityprivacy-peapextensionstype-element"></a><span data-ttu-id="3d497-105">IdentityPrivacy (PeapExtensionsType) 元素</span><span class="sxs-lookup"><span data-stu-id="3d497-105">The IdentityPrivacy (PeapExtensionsType) Element</span></span>

<span data-ttu-id="3d497-106">**IdentityPrivacy (PeapExtensionsType)** 元素指出是否傳送使用者的真實身分識別或匿名身分識別。</span><span class="sxs-lookup"><span data-stu-id="3d497-106">The **IdentityPrivacy (PeapExtensionsType)** element indicates whether a user's true identity or an anonymous identity is sent.</span></span>

``` syntax
<xs:element name="IdentityPrivacy"
    type="IdentityPrivacyParameters"
 />
```

<span data-ttu-id="3d497-107">**IdentityPrivacy** 元素是由 [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)元素定義。</span><span class="sxs-lookup"><span data-stu-id="3d497-107">The **IdentityPrivacy** element is defined by the [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d497-108">備註</span><span class="sxs-lookup"><span data-stu-id="3d497-108">Remarks</span></span>

<span data-ttu-id="3d497-109">**IdentityPrivacy** 元素是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="3d497-109">The **IdentityPrivacy** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d497-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="3d497-110">Requirements</span></span>



| <span data-ttu-id="3d497-111">需求</span><span class="sxs-lookup"><span data-stu-id="3d497-111">Requirement</span></span> | <span data-ttu-id="3d497-112">值</span><span class="sxs-lookup"><span data-stu-id="3d497-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="3d497-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3d497-113">Minimum supported client</span></span><br/> | <span data-ttu-id="3d497-114">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3d497-114">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="3d497-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3d497-115">Minimum supported server</span></span><br/> | <span data-ttu-id="3d497-116">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3d497-116">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3d497-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3d497-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="3d497-118">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="3d497-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="3d497-119">**PeapExtensionsType**</span><span class="sxs-lookup"><span data-stu-id="3d497-119">**PeapExtensionsType**</span></span>](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> <dt>

<span data-ttu-id="3d497-120">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="3d497-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="3d497-121">**PeapExtensions**</span><span class="sxs-lookup"><span data-stu-id="3d497-121">**PeapExtensions**</span></span>](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
<span data-ttu-id="3d497-122"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="3d497-122"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="3d497-123">EAPHost 和舊版架構</span><span class="sxs-lookup"><span data-stu-id="3d497-123">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="3d497-124">mspeapconnectionpropertiesv2 架構</span><span class="sxs-lookup"><span data-stu-id="3d497-124">mspeapconnectionpropertiesv2 Schema</span></span>](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[<span data-ttu-id="3d497-125">mspeapconnectionpropertiesv2 架構元素</span><span class="sxs-lookup"><span data-stu-id="3d497-125">mspeapconnectionpropertiesv2 Schema Elements</span></span>](mspeapconnectionpropertiesv2schema-elements.md)
</dt> </dl>

 

 





