---
title: PeapExtensionsType 複雜類型
description: 包含在 Windows 7 中所做的架構增強功能。 未來的架構增強功能將由 PeapExtensionsTypeV2 處理。
ms.assetid: a8fb8474-a375-4401-83b0-4fa87d637209
keywords:
- PeapExtensionsType 複雜類型 EAPHost
topic_type:
- apiref
api_name:
- PeapExtensionsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7cb8c698122c5a466ae95f728838425a5f10c665
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686243"
---
# <a name="peapextensionstype-complex-type"></a><span data-ttu-id="8df7d-105">PeapExtensionsType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="8df7d-105">PeapExtensionsType Complex Type</span></span>

<span data-ttu-id="8df7d-106">**PeapExtensionsType** 複雜類型包含在 Windows 7 中所做的架構增強功能。</span><span class="sxs-lookup"><span data-stu-id="8df7d-106">The **PeapExtensionsType** complex type contains schema enhancements made in Windows 7.</span></span> <span data-ttu-id="8df7d-107">未來的架構增強功能將由 [**PeapExtensionsTypeV2**](mspeapconnectionpropertiesv2-peapextensionstypev2-complextype.md)處理。</span><span class="sxs-lookup"><span data-stu-id="8df7d-107">Future schema enhancements will be handled by [**PeapExtensionsTypeV2**](mspeapconnectionpropertiesv2-peapextensionstypev2-complextype.md).</span></span>

``` syntax
<xs:complexType name="PeapExtensionsType">
    <xs:sequence>
        <xs:element
            minOccurs="0"
            ref="extendedPeap:PerformServerValidation"
         />
        <xs:element
            minOccurs="0"
            ref="extendedPeap:AcceptServerName"
         />
        <xs:element
            minOccurs="0"
            ref="extendedPeap:IdentityPrivacy"
         />
        <xs:element
            minOccurs="0"
            ref="extendedPeap:PeapExtensionsV2"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="8df7d-108">子元素</span><span class="sxs-lookup"><span data-stu-id="8df7d-108">Child elements</span></span>



| <span data-ttu-id="8df7d-109">元素</span><span class="sxs-lookup"><span data-stu-id="8df7d-109">Element</span></span>                                                                                                                               | <span data-ttu-id="8df7d-110">類型</span><span class="sxs-lookup"><span data-stu-id="8df7d-110">Type</span></span> | <span data-ttu-id="8df7d-111">Description</span><span class="sxs-lookup"><span data-stu-id="8df7d-111">Description</span></span>                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------|------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8df7d-112">**extendedPeap:PerformServerValidation**</span><span class="sxs-lookup"><span data-stu-id="8df7d-112">**extendedPeap:PerformServerValidation**</span></span>](mspeapconnectionpropertiesv1schema-performservervalidation-peapextensionstype-element.md) |      | <span data-ttu-id="8df7d-113">Windows 7 和更新版本：指出是否執行伺服器驗證。</span><span class="sxs-lookup"><span data-stu-id="8df7d-113">Windows 7 and later: indicates whether server validation is performed.</span></span><br/>                          |
| [<span data-ttu-id="8df7d-114">**extendedPeap:AcceptServerName**</span><span class="sxs-lookup"><span data-stu-id="8df7d-114">**extendedPeap:AcceptServerName**</span></span>](mspeapconnectionpropertiesv1schema-acceptservername-peapextensionstype-element.md)               |      | <span data-ttu-id="8df7d-115">Windows 7 和更新版本：指出是否已讀取伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="8df7d-115">Windows 7 and later: indicates whether the name of a server is read.</span></span><br/>                            |
| [<span data-ttu-id="8df7d-116">**extendedPeap:IdentityPrivacy**</span><span class="sxs-lookup"><span data-stu-id="8df7d-116">**extendedPeap:IdentityPrivacy**</span></span>](mspeapconnectionpropertiesv1schema-identityprivacy-peapextensionstype-element.md)                 |      | <span data-ttu-id="8df7d-117">Windows 7 和更新版本：指出是否傳送使用者的真實身分識別或匿名身分識別。</span><span class="sxs-lookup"><span data-stu-id="8df7d-117">Windows 7 and later: indicates whether a user's true identity or an anonymous identity is sent.</span></span><br/> |
| [<span data-ttu-id="8df7d-118">**extendedPeap:PeapExtensionsV2**</span><span class="sxs-lookup"><span data-stu-id="8df7d-118">**extendedPeap:PeapExtensionsV2**</span></span>](mspeapconnectionpropertiesv1-peapextensionsv2-peapextensionstype-element.md)                     |      | <span data-ttu-id="8df7d-119">Windows 7 和更新版本：讓架構的未來增強功能。</span><span class="sxs-lookup"><span data-stu-id="8df7d-119">Windows 7 and later: enables future enhancements to the schema.</span></span><br/>                                 |



## <a name="remarks"></a><span data-ttu-id="8df7d-120">備註</span><span class="sxs-lookup"><span data-stu-id="8df7d-120">Remarks</span></span>

<span data-ttu-id="8df7d-121">**PeapExtensionsType** 元素是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="8df7d-121">The **PeapExtensionsType** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="8df7d-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="8df7d-122">Requirements</span></span>



| <span data-ttu-id="8df7d-123">需求</span><span class="sxs-lookup"><span data-stu-id="8df7d-123">Requirement</span></span> | <span data-ttu-id="8df7d-124">值</span><span class="sxs-lookup"><span data-stu-id="8df7d-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="8df7d-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8df7d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="8df7d-126">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8df7d-126">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="8df7d-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8df7d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="8df7d-128">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8df7d-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8df7d-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8df7d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8df7d-130">EAPHost 和舊版架構</span><span class="sxs-lookup"><span data-stu-id="8df7d-130">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="8df7d-131">mspeapconnectionpropertiesv1 架構</span><span class="sxs-lookup"><span data-stu-id="8df7d-131">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="8df7d-132">mspeapconnectionpropertiesv1 架構複雜類型</span><span class="sxs-lookup"><span data-stu-id="8df7d-132">mspeapconnectionpropertiesv1 Schema Complex Types</span></span>](mspeapconnectionpropertiesv1schema-complex-types.md)
</dt> </dl>

 

 





