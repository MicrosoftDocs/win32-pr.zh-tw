---
title: EapHostUserCredentials 元素
description: 包含 EapMethod 專案，以及認證或 CredentialsBlob 元素。
ms.assetid: 6d0d41c8-560c-4d42-83c9-865053aef47a
keywords:
- EapHostUserCredentials 元素 EAPHost
topic_type:
- apiref
api_name:
- EapHostUserCredentials
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 690770091219e51b3ebb550a1a72e50f76b20542
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104873"
---
# <a name="eaphostusercredentials-element"></a><span data-ttu-id="f71a8-104">EapHostUserCredentials 元素</span><span class="sxs-lookup"><span data-stu-id="f71a8-104">EapHostUserCredentials Element</span></span>

<span data-ttu-id="f71a8-105">**EapHostUserCredentials** 元素包含 [**EapMethod**](eaphostusercredentialsschema-eapmethod-eaphostusercredentials-element.md)元素，以及 [**認證**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md)或 [**CredentialsBlob**](eaphostusercredentialsschema-credentialsblob-eaphostusercredentials-element.md)元素。</span><span class="sxs-lookup"><span data-stu-id="f71a8-105">The **EapHostUserCredentials** element contains the [**EapMethod**](eaphostusercredentialsschema-eapmethod-eaphostusercredentials-element.md) element, and [**Credentials**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md) or [**CredentialsBlob**](eaphostusercredentialsschema-credentialsblob-eaphostusercredentials-element.md) element.</span></span>

``` syntax
<xs:element name="EapHostUserCredentials">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="EapMethod"
                type="EapMethodType"
             />
            <xs:choice>
                <xs:element name="Credentials"
                    type="BaseEapMethodUserCredentials"
                 />
                <xs:element name="CredentialsBlob"
                    type="hexBinary"
                 />
            </xs:choice>
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="f71a8-106">子元素</span><span class="sxs-lookup"><span data-stu-id="f71a8-106">Child elements</span></span>



| <span data-ttu-id="f71a8-107">元素</span><span class="sxs-lookup"><span data-stu-id="f71a8-107">Element</span></span>                                                                                                | <span data-ttu-id="f71a8-108">類型</span><span class="sxs-lookup"><span data-stu-id="f71a8-108">Type</span></span>                                                                                                                | <span data-ttu-id="f71a8-109">Description</span><span class="sxs-lookup"><span data-stu-id="f71a8-109">Description</span></span>                                                                                      |
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f71a8-110">**認證**</span><span class="sxs-lookup"><span data-stu-id="f71a8-110">**Credentials**</span></span>](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md)         | [<span data-ttu-id="f71a8-111">**BaseEapMethodUserCredentials**</span><span class="sxs-lookup"><span data-stu-id="f71a8-111">**BaseEapMethodUserCredentials**</span></span>](baseeapmethodusercredentialsschema-baseeapmethodusercredentials-complextype.md) | <span data-ttu-id="f71a8-112">當方法設定為 XML 文字格式，而非二進位 BLOB 時，會使用。</span><span class="sxs-lookup"><span data-stu-id="f71a8-112">Is used when the method configuration is in XML text form instead of a binary BLOB.</span></span><br/>   |
| [<span data-ttu-id="f71a8-113">**CredentialsBlob**</span><span class="sxs-lookup"><span data-stu-id="f71a8-113">**CredentialsBlob**</span></span>](eaphostusercredentialsschema-credentialsblob-eaphostusercredentials-element.md) | <span data-ttu-id="f71a8-114">hexBinary</span><span class="sxs-lookup"><span data-stu-id="f71a8-114">hexBinary</span></span>                                                                                                           | <span data-ttu-id="f71a8-115">當方法設定為二進位 BLOB 而非 XML 文字格式時，就會使用。</span><span class="sxs-lookup"><span data-stu-id="f71a8-115">Is used when the method configuration is a binary BLOB instead of in XML text format.</span></span><br/> |
| [<span data-ttu-id="f71a8-116">**EapMethod**</span><span class="sxs-lookup"><span data-stu-id="f71a8-116">**EapMethod**</span></span>](eaphostusercredentialsschema-eapmethod-eaphostusercredentials-element.md)             | [<span data-ttu-id="f71a8-117">**EapMethodType**</span><span class="sxs-lookup"><span data-stu-id="f71a8-117">**EapMethodType**</span></span>](eapcommonschema-eapmethodtype-complextype.md)                                                  | <span data-ttu-id="f71a8-118">識別所參考的方法。</span><span class="sxs-lookup"><span data-stu-id="f71a8-118">Identifies the method being referred to.</span></span> <br/>                                             |



## <a name="remarks"></a><span data-ttu-id="f71a8-119">備註</span><span class="sxs-lookup"><span data-stu-id="f71a8-119">Remarks</span></span>

<span data-ttu-id="f71a8-120">[**認證**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md)和 [**CredentialsBlob**](eaphostusercredentialsschema-credentialsblob-eaphostusercredentials-element.md)元素不能同時使用。</span><span class="sxs-lookup"><span data-stu-id="f71a8-120">The [**Credentials**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md) and [**CredentialsBlob**](eaphostusercredentialsschema-credentialsblob-eaphostusercredentials-element.md) elements cannot be both be used simultaneously.</span></span>

<span data-ttu-id="f71a8-121">有其他命名空間的延伸點。</span><span class="sxs-lookup"><span data-stu-id="f71a8-121">There is an extension point for other namespaces.</span></span>

<span data-ttu-id="f71a8-122">**ProcessContents** 元素可讓架構的未來增強功能。</span><span class="sxs-lookup"><span data-stu-id="f71a8-122">The **processContents** element enables future enhancements to the schema.</span></span> <span data-ttu-id="f71a8-123">**ProcessContents** 元素是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="f71a8-123">The **processContents** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="f71a8-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="f71a8-124">Requirements</span></span>



| <span data-ttu-id="f71a8-125">需求</span><span class="sxs-lookup"><span data-stu-id="f71a8-125">Requirement</span></span> | <span data-ttu-id="f71a8-126">值</span><span class="sxs-lookup"><span data-stu-id="f71a8-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f71a8-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f71a8-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f71a8-128">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f71a8-128">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f71a8-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f71a8-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f71a8-130">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f71a8-130">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f71a8-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f71a8-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f71a8-132">EAPHost 和舊版架構</span><span class="sxs-lookup"><span data-stu-id="f71a8-132">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="f71a8-133">eaphostusercredentials 架構</span><span class="sxs-lookup"><span data-stu-id="f71a8-133">eaphostusercredentials Schema</span></span>](eaphostusercredentialsschema-schema.md)
</dt> </dl>

 

 





