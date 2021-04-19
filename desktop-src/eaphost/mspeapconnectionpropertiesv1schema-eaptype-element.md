---
title: 'EapType 元素 (mspeapconnectionpropertiesv1schema) '
description: 這個元素是 BaseEapConnectionProperties 架構中 EapType 元素的衍生型別。 適用于 mspeapconnectionpropertiesv1schema。
ms.assetid: 13238968-f3ef-4e9c-a525-d1f6efbaee0d
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
ms.openlocfilehash: 3336e943170afa0ec1f239d4cf7a0c603a0c8e71
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/02/2021
ms.locfileid: "106995981"
---
# <a name="eaptype-element-mspeapconnectionpropertiesv1schema"></a><span data-ttu-id="fca05-105">EapType 元素 (mspeapconnectionpropertiesv1schema) </span><span class="sxs-lookup"><span data-stu-id="fca05-105">EapType element (mspeapconnectionpropertiesv1schema)</span></span>

<span data-ttu-id="fca05-106">**EapType** 元素是 [BaseEapConnectionProperties](baseeapconnectionpropertiesv1schema-schema.md)架構中 [**EapType**](baseeapconnectionpropertiesv1schema-eaptype-element.md)元素的衍生型別。</span><span class="sxs-lookup"><span data-stu-id="fca05-106">The **EapType** element is a derived type of the [**EapType**](baseeapconnectionpropertiesv1schema-eaptype-element.md) element from the [BaseEapConnectionProperties](baseeapconnectionpropertiesv1schema-schema.md) schema.</span></span>

<span data-ttu-id="fca05-107">這個衍生的 **EapType** 元素包含下列元素： [**ServerValidation**](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md)、 [**IdentityPrivacy**](mspeapconnectionpropertiesv2-identityprivacy-peapextensionstype-element.md)、 [**FastReconnect**](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md)、 [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md)、 [**Eap**](baseeapconnectionpropertiesv1schema-eap-element.md)、 [**EnableQuarantineChecks**](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md)、 [**RequireCryptoBinding**](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md) 和 [**PeapExtensions**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)。</span><span class="sxs-lookup"><span data-stu-id="fca05-107">This derived **EapType** element contains the following elements: [**ServerValidation**](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md), [**IdentityPrivacy**](mspeapconnectionpropertiesv2-identityprivacy-peapextensionstype-element.md), [**FastReconnect**](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md), [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md), [**Eap**](baseeapconnectionpropertiesv1schema-eap-element.md), [**EnableQuarantineChecks**](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md), [**RequireCryptoBinding**](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md) and [**PeapExtensions**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md).</span></span>

``` syntax
<xs:element name="EapType"
    substitutionGroup="EapType"
>
    <xs:complexType>
        <xs:complexContent>
            <xs:extension
                base="BaseEapTypeParameters"
            >
                <xs:sequence>
                    <xs:element name="ServerValidation"
                        type="ServerValidationParameters"
                        minOccurs="0"
                     />
                    <xs:element name="IdentityPrivacy"
                        type="IdentityPrivacyParameters"
                        minOccurs="0"
                     />
                    <xs:element name="FastReconnect"
                        type="boolean"
                        minOccurs="0"
                     />
                    <xs:element name="InnerEapOptional"
                        type="boolean"
                        minOccurs="0"
                     />
                    <xs:element
                        minOccurs="0"
                        maxOccurs="unbounded"
                        ref="Eap"
                     />
                    <xs:element name="EnableQuarantineChecks"
                        type="boolean"
                        default="false"
                        minOccurs="0"
                     />
                    <xs:element name="RequireCryptoBinding"
                        type="boolean"
                        default="false"
                        minOccurs="0"
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

## <a name="child-elements"></a><span data-ttu-id="fca05-108">子元素</span><span class="sxs-lookup"><span data-stu-id="fca05-108">Child elements</span></span>



| <span data-ttu-id="fca05-109">元素</span><span class="sxs-lookup"><span data-stu-id="fca05-109">Element</span></span>                                                                                                     | <span data-ttu-id="fca05-110">類型</span><span class="sxs-lookup"><span data-stu-id="fca05-110">Type</span></span>                                                                                                            | <span data-ttu-id="fca05-111">Description</span><span class="sxs-lookup"><span data-stu-id="fca05-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fca05-112">**Eap**</span><span class="sxs-lookup"><span data-stu-id="fca05-112">**Eap**</span></span>](baseeapconnectionpropertiesv1schema-eap-element.md)                                              |                                                                                                                 | <span data-ttu-id="fca05-113">描述內部方法和方法設定。</span><span class="sxs-lookup"><span data-stu-id="fca05-113">Describes the inner method and the method configuration.</span></span> <span data-ttu-id="fca05-114">如果 [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) 元素為 TRUE，則必須有 [**Eap**](baseeapconnectionpropertiesv1schema-eap-element.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="fca05-114">If the [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) element is TRUE, the [**Eap**](baseeapconnectionpropertiesv1schema-eap-element.md) element must be present.</span></span> <span data-ttu-id="fca05-115">如果 [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) 元素為 FALSE， [**Eap**](baseeapconnectionpropertiesv1schema-eap-element.md) 元素就必須不存在。</span><span class="sxs-lookup"><span data-stu-id="fca05-115">If the [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) element is FALSE, the [**Eap**](baseeapconnectionpropertiesv1schema-eap-element.md) element must be absent.</span></span><br/>           |
| [<span data-ttu-id="fca05-116">**EnableQuarantineChecks**</span><span class="sxs-lookup"><span data-stu-id="fca05-116">**EnableQuarantineChecks**</span></span>](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md) | <span data-ttu-id="fca05-117">boolean</span><span class="sxs-lookup"><span data-stu-id="fca05-117">boolean</span></span>                                                                                                         | <span data-ttu-id="fca05-118">指出是否 (NAP) 檢查來執行網路存取保護。</span><span class="sxs-lookup"><span data-stu-id="fca05-118">Indicates whether to perform Network Access Protection (NAP) checks.</span></span> <span data-ttu-id="fca05-119">如果 [**EnableQuarantineChecks**](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md) 元素為 TRUE，則 PEAP 會執行 NAP 檢查;若為 FALSE，則不會執行 NAP 檢查。</span><span class="sxs-lookup"><span data-stu-id="fca05-119">If the [**EnableQuarantineChecks**](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md) element is TRUE, then PEAP will perform NAP checks; if FALSE PEAP will not perform NAP checks.</span></span> <span data-ttu-id="fca05-120">[**EnableQuarantineChecks**](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md)元素是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="fca05-120">The [**EnableQuarantineChecks**](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md) element is optional.</span></span><br/>                                                                                |
| [<span data-ttu-id="fca05-121">**FastReconnect**</span><span class="sxs-lookup"><span data-stu-id="fca05-121">**FastReconnect**</span></span>](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md)                   | <span data-ttu-id="fca05-122">boolean</span><span class="sxs-lookup"><span data-stu-id="fca05-122">boolean</span></span>                                                                                                         | <span data-ttu-id="fca05-123">指出是否要執行快速重新連接。</span><span class="sxs-lookup"><span data-stu-id="fca05-123">Indicates whether to perform a fast reconnect.</span></span> <span data-ttu-id="fca05-124">如果 [**FastReconnect**](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md) 元素為 TRUE，則 PEAP 會嘗試執行快速重新連線;如果為 FALSE，則 PEAP 會執行完整驗證。</span><span class="sxs-lookup"><span data-stu-id="fca05-124">If the [**FastReconnect**](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md) element is TRUE, then PEAP attempts to perform a fast reconnect; if FALSE, PEAP performs the full authentication.</span></span> <span data-ttu-id="fca05-125">[**FastReconnect**](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md)元素是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="fca05-125">The [**FastReconnect**](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md) element is optional.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="fca05-126">**IdentityPrivacy**</span><span class="sxs-lookup"><span data-stu-id="fca05-126">**IdentityPrivacy**</span></span>](mspeapconnectionpropertiesv2-identityprivacy-peapextensionstype-element.md)          | [<span data-ttu-id="fca05-127">**IdentityPrivacyParameters**</span><span class="sxs-lookup"><span data-stu-id="fca05-127">**IdentityPrivacyParameters**</span></span>](mspeapconnectionpropertiesv2-identityprivacyparameters-complextype.md)         | <span data-ttu-id="fca05-128">Windows 7 或更新版本：指出是否傳送使用者的真實身分識別或匿名身分識別。</span><span class="sxs-lookup"><span data-stu-id="fca05-128">Windows 7 or later: Indicates whether a user's true identity or an anonymous identity is sent.</span></span> <span data-ttu-id="fca05-129">[**IdentityPrivacy**](mspeapconnectionpropertiesv2-identityprivacy-peapextensionstype-element.md)元素是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="fca05-129">The [**IdentityPrivacy**](mspeapconnectionpropertiesv2-identityprivacy-peapextensionstype-element.md) element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="fca05-130">**InnerEapOptional**</span><span class="sxs-lookup"><span data-stu-id="fca05-130">**InnerEapOptional**</span></span>](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md)             | <span data-ttu-id="fca05-131">boolean</span><span class="sxs-lookup"><span data-stu-id="fca05-131">boolean</span></span>                                                                                                         | <span data-ttu-id="fca05-132">指出是否要執行來賓存取。</span><span class="sxs-lookup"><span data-stu-id="fca05-132">Indicates whether to perform GUEST access.</span></span> <span data-ttu-id="fca05-133">如果 [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) 專案是 TRUE，則 [**Eap**](baseeapconnectionpropertiesv1schema-eap-element.md) 元素必須存在，並且描述內部方法及其設定;若為 FALSE，則 PEAP 會執行來賓存取。</span><span class="sxs-lookup"><span data-stu-id="fca05-133">If the [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) element is TRUE, then the [**Eap**](baseeapconnectionpropertiesv1schema-eap-element.md) element must be present and describe the inner method and its configuration; if FALSE, then PEAP will perform GUEST access.</span></span> <span data-ttu-id="fca05-134">[**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md)元素是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="fca05-134">The [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) element is optional.</span></span><br/>            |
| [<span data-ttu-id="fca05-135">**PeapExtensions**</span><span class="sxs-lookup"><span data-stu-id="fca05-135">**PeapExtensions**</span></span>](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)                 | [<span data-ttu-id="fca05-136">**PeapExtensionsType**</span><span class="sxs-lookup"><span data-stu-id="fca05-136">**PeapExtensionsType**</span></span>](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)                 | <span data-ttu-id="fca05-137">[**PeapExtensions**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)元素可讓架構的未來增強功能。</span><span class="sxs-lookup"><span data-stu-id="fca05-137">The [**PeapExtensions**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md) element enables future enhancements to the schema.</span></span> <span data-ttu-id="fca05-138">[**PeapExtensions**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)元素是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="fca05-138">The [**PeapExtensions**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md) element is optional.</span></span><br/>                                                                                                                                                                                                                                    |
| [<span data-ttu-id="fca05-139">**RequireCryptoBinding**</span><span class="sxs-lookup"><span data-stu-id="fca05-139">**RequireCryptoBinding**</span></span>](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md)     | <span data-ttu-id="fca05-140">boolean</span><span class="sxs-lookup"><span data-stu-id="fca05-140">boolean</span></span>                                                                                                         | <span data-ttu-id="fca05-141">指出是否要使用支援加密的伺服器進行驗證。</span><span class="sxs-lookup"><span data-stu-id="fca05-141">Indicates whether to authenticate with servers that support cryptobinding.</span></span> <span data-ttu-id="fca05-142">如果 [**RequireCryptoBinding**](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md) 元素為 TRUE，則 PEAP 會向不支援加密的伺服器進行驗證;若為 FALSE，則 PEAP 只會驗證支援加密的伺服器。</span><span class="sxs-lookup"><span data-stu-id="fca05-142">If the [**RequireCryptoBinding**](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md) element is TRUE, then PEAP will authenticate with servers that don't support cryptobinding; if FALSE, then PEAP will only authenticate with servers that support cryptobinding.</span></span> <span data-ttu-id="fca05-143">[**RequireCryptoBinding**](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md)元素是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="fca05-143">The [**RequireCryptoBinding**](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md) element is optional.</span></span><br/> |
| [<span data-ttu-id="fca05-144">**ServerValidation**</span><span class="sxs-lookup"><span data-stu-id="fca05-144">**ServerValidation**</span></span>](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md)             | [<span data-ttu-id="fca05-145">**ServerValidationParameters**</span><span class="sxs-lookup"><span data-stu-id="fca05-145">**ServerValidationParameters**</span></span>](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md) | <span data-ttu-id="fca05-146">包含如何執行伺服器驗證的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="fca05-146">Contains information about how to perform server validation.</span></span> <span data-ttu-id="fca05-147">[**ServerValidation**](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md)元素是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="fca05-147">The [**ServerValidation**](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md) element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                      |



## <a name="requirements"></a><span data-ttu-id="fca05-148">規格需求</span><span class="sxs-lookup"><span data-stu-id="fca05-148">Requirements</span></span>



| <span data-ttu-id="fca05-149">需求</span><span class="sxs-lookup"><span data-stu-id="fca05-149">Requirement</span></span> | <span data-ttu-id="fca05-150">值</span><span class="sxs-lookup"><span data-stu-id="fca05-150">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fca05-151">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fca05-151">Minimum supported client</span></span><br/> | <span data-ttu-id="fca05-152">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fca05-152">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="fca05-153">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fca05-153">Minimum supported server</span></span><br/> | <span data-ttu-id="fca05-154">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fca05-154">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fca05-155">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fca05-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fca05-156">EAPHost 和舊版架構</span><span class="sxs-lookup"><span data-stu-id="fca05-156">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="fca05-157">mspeapconnectionpropertiesv1 架構</span><span class="sxs-lookup"><span data-stu-id="fca05-157">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="fca05-158">mspeapconnectionpropertiesv1 架構元素</span><span class="sxs-lookup"><span data-stu-id="fca05-158">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





