---
title: EnableIdentityPrivacy (IdentityPrivacyParameters) 元素
description: 指出是否傳送使用者的真實身分識別或匿名身分識別。 |EnableIdentityPrivacy (IdentityPrivacyParameters) 元素
ms.assetid: 7751e5fa-895e-47f7-99d9-aa7ef2451eb1
keywords:
- EnableIdentityPrivacy 元素 EAPHost
topic_type:
- apiref
api_name:
- Username
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4a96b49fe462f4ef8cedad550d1a6c87d680939
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322484"
---
# <a name="enableidentityprivacy-identityprivacyparameters-element"></a><span data-ttu-id="3a5b7-105">EnableIdentityPrivacy (IdentityPrivacyParameters) 元素</span><span class="sxs-lookup"><span data-stu-id="3a5b7-105">EnableIdentityPrivacy (IdentityPrivacyParameters) Element</span></span>

<span data-ttu-id="3a5b7-106">**EnableIdentityPrivacy (IdentityPrivacyParameters)** 元素指出是否傳送使用者的真實身分識別或匿名身分識別。</span><span class="sxs-lookup"><span data-stu-id="3a5b7-106">The **EnableIdentityPrivacy (IdentityPrivacyParameters)** element Indicates whether a user's true identity or an anonymous identity is sent.</span></span>

``` syntax
<xs:element name="EnableIdentityPrivacy"
    type="xs:Boolean"
    minOccurs="0"
 />
```

<span data-ttu-id="3a5b7-107">**EnableIdentityPrivacy** 元素是由 [IdentityPrivacyParameters](mspeapconnectionpropertiesv2-identityprivacyparameters-complextype.md)定義。</span><span class="sxs-lookup"><span data-stu-id="3a5b7-107">The **EnableIdentityPrivacy** element is defined by the [IdentityPrivacyParameters](mspeapconnectionpropertiesv2-identityprivacyparameters-complextype.md) .</span></span>

## <a name="remarks"></a><span data-ttu-id="3a5b7-108">備註</span><span class="sxs-lookup"><span data-stu-id="3a5b7-108">Remarks</span></span>

<span data-ttu-id="3a5b7-109">**EnableIdentityPrivacy** 元素是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="3a5b7-109">The **EnableIdentityPrivacy** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a5b7-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="3a5b7-110">Requirements</span></span>



| <span data-ttu-id="3a5b7-111">需求</span><span class="sxs-lookup"><span data-stu-id="3a5b7-111">Requirement</span></span> | <span data-ttu-id="3a5b7-112">值</span><span class="sxs-lookup"><span data-stu-id="3a5b7-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="3a5b7-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3a5b7-113">Minimum supported client</span></span><br/> | <span data-ttu-id="3a5b7-114">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3a5b7-114">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="3a5b7-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3a5b7-115">Minimum supported server</span></span><br/> | <span data-ttu-id="3a5b7-116">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3a5b7-116">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3a5b7-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3a5b7-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="3a5b7-118">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="3a5b7-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="3a5b7-119">IdentityPrivacyParameters</span><span class="sxs-lookup"><span data-stu-id="3a5b7-119">IdentityPrivacyParameters</span></span>](mspeapconnectionpropertiesv2-identityprivacyparameters-complextype.md)
</dt> <dt>

<span data-ttu-id="3a5b7-120">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="3a5b7-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="3a5b7-121">**PeapExtensions**</span><span class="sxs-lookup"><span data-stu-id="3a5b7-121">**PeapExtensions**</span></span>](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
<span data-ttu-id="3a5b7-122"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="3a5b7-122"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="3a5b7-123">EAPHost 和舊版架構</span><span class="sxs-lookup"><span data-stu-id="3a5b7-123">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="3a5b7-124">mspeapconnectionpropertiesv2 架構</span><span class="sxs-lookup"><span data-stu-id="3a5b7-124">mspeapconnectionpropertiesv2 Schema</span></span>](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[<span data-ttu-id="3a5b7-125">mspeapconnectionpropertiesv2 架構元素</span><span class="sxs-lookup"><span data-stu-id="3a5b7-125">mspeapconnectionpropertiesv2 Schema Elements</span></span>](mspeapconnectionpropertiesv2schema-elements.md)
</dt> </dl>

 

 





