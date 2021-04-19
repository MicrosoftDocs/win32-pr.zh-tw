---
title: 'EapType 元素 (eaptlsconnectionpropertiesv1schema) '
description: 這個元素是 BaseEapConnectionProperties 架構中 EapType 元素的衍生型別。 適用于 eaptlsconnectionpropertiesv1schema。
ms.assetid: cf92d500-f815-48e2-a7d5-1364cb13a1f0
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
ms.openlocfilehash: b74341d9b1fdd9121f1d67e2a941d931be049e0f
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/02/2021
ms.locfileid: "106984916"
---
# <a name="eaptype-element-eaptlsconnectionpropertiesv1schema"></a><span data-ttu-id="f2ae5-105">EapType 元素 (eaptlsconnectionpropertiesv1schema) </span><span class="sxs-lookup"><span data-stu-id="f2ae5-105">EapType element (eaptlsconnectionpropertiesv1schema)</span></span>

<span data-ttu-id="f2ae5-106">**EapType** 元素是 [BaseEapConnectionProperties](baseeapconnectionpropertiesv1schema-schema.md)架構中 [**EapType**](baseeapconnectionpropertiesv1schema-eaptype-element.md)元素的衍生型別。</span><span class="sxs-lookup"><span data-stu-id="f2ae5-106">The **EapType** element is a derived type of the [**EapType**](baseeapconnectionpropertiesv1schema-eaptype-element.md) element from the [BaseEapConnectionProperties](baseeapconnectionpropertiesv1schema-schema.md) schema.</span></span>

<span data-ttu-id="f2ae5-107">這個衍生的 **EapType** 元素包含下列元素： [**CredentialsSource**](eaptlsconnectionpropertiesv1schema-credentialssource-eaptype-element.md)、 [**ServerValidation**](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md)、 [**DifferentUsername**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md)、 [**PerformServerValidation**](eaptlsconnectionpropertiesv1schema-performservervalidation-peapextensionstype-element.md)、 [**AcceptServerName**](eaptlsconnectionpropertiesv1schema-tlsextensionstype-peapextensionstype-element.md)和 [**TLSExtensions**](eaptlsconnectionpropertiesv1schema-acceptservername-peapextensionstype-element.md)。</span><span class="sxs-lookup"><span data-stu-id="f2ae5-107">This derived **EapType** element contains the following elements: [**CredentialsSource**](eaptlsconnectionpropertiesv1schema-credentialssource-eaptype-element.md), [**ServerValidation**](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md), [**DifferentUsername**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md), [**PerformServerValidation**](eaptlsconnectionpropertiesv1schema-performservervalidation-peapextensionstype-element.md), [**AcceptServerName**](eaptlsconnectionpropertiesv1schema-tlsextensionstype-peapextensionstype-element.md), and [**TLSExtensions**](eaptlsconnectionpropertiesv1schema-acceptservername-peapextensionstype-element.md).</span></span>

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
                    <xs:element name="CredentialsSource"
                        type="CredentialsSourceParameters"
                        minOccurs="0"
                     />
                    <xs:element name="ServerValidation"
                        type="ServerValidationParameters"
                        minOccurs="0"
                     />
                    <xs:element name="DifferentUsername"
                        type="boolean"
                        minOccurs="0"
                     />
                    <xs:element
                        minOccurs="0"
                        maxOccurs="1"
                        ref="extendedTLS: PerformServerValidation"
                     />
                    <xs:element
                        minOccurs="0"
                        maxOccurs="1"
                        ref="extendedTLS: AcceptServerName"
                     />
                    <xs:element
                        minOccurs="0"
                        maxOccurs="1"
                        ref="extendedTLS: TLSExtensions"
                     />
                </xs:sequence>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="f2ae5-108">子元素</span><span class="sxs-lookup"><span data-stu-id="f2ae5-108">Child elements</span></span>



| <span data-ttu-id="f2ae5-109">元素</span><span class="sxs-lookup"><span data-stu-id="f2ae5-109">Element</span></span>                                                                                                                               | <span data-ttu-id="f2ae5-110">類型</span><span class="sxs-lookup"><span data-stu-id="f2ae5-110">Type</span></span>                                                                                                              | <span data-ttu-id="f2ae5-111">Description</span><span class="sxs-lookup"><span data-stu-id="f2ae5-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f2ae5-112">**extendedTLS: PerformServerValidation**</span><span class="sxs-lookup"><span data-stu-id="f2ae5-112">**extendedTLS: PerformServerValidation**</span></span>](eaptlsconnectionpropertiesv1schema-performservervalidation-peapextensionstype-element.md) |                                                                                                                   | <span data-ttu-id="f2ae5-113">Windows 7 和更新版本：指出是否執行伺服器驗證。</span><span class="sxs-lookup"><span data-stu-id="f2ae5-113">Windows 7 and later: indicates whether server validation is performed.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [<span data-ttu-id="f2ae5-114">**extendedTLS: AcceptServerName**</span><span class="sxs-lookup"><span data-stu-id="f2ae5-114">**extendedTLS: AcceptServerName**</span></span>](eaptlsconnectionpropertiesv1schema-tlsextensionstype-peapextensionstype-element.md)              |                                                                                                                   | <span data-ttu-id="f2ae5-115">Windows 7 和更新版本：指出是否已讀取伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="f2ae5-115">Windows 7 and later: indicates whether the name of a server is read.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="f2ae5-116">**extendedTLS: TLSExtensions**</span><span class="sxs-lookup"><span data-stu-id="f2ae5-116">**extendedTLS: TLSExtensions**</span></span>](eaptlsconnectionpropertiesv1schema-acceptservername-peapextensionstype-element.md)                  |                                                                                                                   | <span data-ttu-id="f2ae5-117">Windows 7 和更新版本：讓架構的未來增強功能。</span><span class="sxs-lookup"><span data-stu-id="f2ae5-117">Windows 7 and later: enables future enhancements to the schema.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="f2ae5-118">**CredentialsSource**</span><span class="sxs-lookup"><span data-stu-id="f2ae5-118">**CredentialsSource**</span></span>](eaptlsconnectionpropertiesv1schema-credentialssource-eaptype-element.md)                                     | [<span data-ttu-id="f2ae5-119">**CredentialsSourceParameters**</span><span class="sxs-lookup"><span data-stu-id="f2ae5-119">**CredentialsSourceParameters**</span></span>](eaptlsconnectionpropertiesv1schema-credentialssourceparameters-complextype.md) | <span data-ttu-id="f2ae5-120">包含 EAP 傳輸層級安全性 (EAP-TLS) 憑證位置的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f2ae5-120">Contains information about the location of the EAP Transport Level Security (EAP-TLS) certificate.</span></span> <br/> <span data-ttu-id="f2ae5-121">[**CredentialsSource**](eaptlsconnectionpropertiesv1schema-credentialssource-eaptype-element.md)元素是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="f2ae5-121">The [**CredentialsSource**](eaptlsconnectionpropertiesv1schema-credentialssource-eaptype-element.md) element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="f2ae5-122">**DifferentUsername**</span><span class="sxs-lookup"><span data-stu-id="f2ae5-122">**DifferentUsername**</span></span>](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md)                                     | <span data-ttu-id="f2ae5-123">boolean</span><span class="sxs-lookup"><span data-stu-id="f2ae5-123">boolean</span></span>                                                                                                           | <span data-ttu-id="f2ae5-124">決定要使用的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="f2ae5-124">Determines which user name EAP-TLS is to use.</span></span> <br/> <span data-ttu-id="f2ae5-125">如果 [**DifferentUsername**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md) 元素為 **TRUE**，則 eap-tls 應該使用憑證上所顯示的名稱以外的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="f2ae5-125">If the [**DifferentUsername**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md) element is **TRUE**, EAP-TLS should use a user name other than the name that appears on the certificate.</span></span> <span data-ttu-id="f2ae5-126">如果 [**DifferentUsername**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md) 元素為 **FALSE**，則 eap-tls 會使用憑證上出現的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="f2ae5-126">If the [**DifferentUsername**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md) element is **FALSE**, EAP-TLS uses the user name that appears on the certificate.</span></span><br/> <span data-ttu-id="f2ae5-127">[**DifferentUsername**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md)元素是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="f2ae5-127">The [**DifferentUsername**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md) element is optional.</span></span> <br/> |
| [<span data-ttu-id="f2ae5-128">**ServerValidation**</span><span class="sxs-lookup"><span data-stu-id="f2ae5-128">**ServerValidation**</span></span>](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md)                                       | [<span data-ttu-id="f2ae5-129">**ServerValidationParameters**</span><span class="sxs-lookup"><span data-stu-id="f2ae5-129">**ServerValidationParameters**</span></span>](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md)   | <span data-ttu-id="f2ae5-130">包含如何執行伺服器驗證的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f2ae5-130">Contains information about how to perform server validation.</span></span> <span data-ttu-id="f2ae5-131">[**ServerValidation**](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md)元素是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="f2ae5-131">The [**ServerValidation**](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md) element is optional.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                        |



## <a name="requirements"></a><span data-ttu-id="f2ae5-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="f2ae5-132">Requirements</span></span>



| <span data-ttu-id="f2ae5-133">需求</span><span class="sxs-lookup"><span data-stu-id="f2ae5-133">Requirement</span></span> | <span data-ttu-id="f2ae5-134">值</span><span class="sxs-lookup"><span data-stu-id="f2ae5-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f2ae5-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f2ae5-135">Minimum supported client</span></span><br/> | <span data-ttu-id="f2ae5-136">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f2ae5-136">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f2ae5-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f2ae5-137">Minimum supported server</span></span><br/> | <span data-ttu-id="f2ae5-138">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f2ae5-138">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f2ae5-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f2ae5-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2ae5-140">EAPHost 和舊版架構</span><span class="sxs-lookup"><span data-stu-id="f2ae5-140">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="f2ae5-141">eaptlsconnectionpropertiesv1 架構</span><span class="sxs-lookup"><span data-stu-id="f2ae5-141">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="f2ae5-142">eaptlsconnectionpropertiesv1 架構元素</span><span class="sxs-lookup"><span data-stu-id="f2ae5-142">eaptlsconnectionpropertiesv1 Schema Elements</span></span>](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





