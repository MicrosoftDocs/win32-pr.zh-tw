---
title: 'EapType 元素 (eaptlsuserpropertiesv1schema) '
description: 這個元素是 baseeapuserpropertiesv1 架構中 EapType 元素的衍生型別。 適用于 eaptlsuserpropertiesv1schema。
ms.assetid: c9117803-dbf0-498d-8f86-f44ac2e6b2dc
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
ms.openlocfilehash: 53e5c1404c70542f3604b94aa6cae9c8fc39fd21
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/02/2021
ms.locfileid: "106999566"
---
# <a name="eaptype-element-eaptlsuserpropertiesv1schema"></a><span data-ttu-id="39470-105">EapType 元素 (eaptlsuserpropertiesv1schema) </span><span class="sxs-lookup"><span data-stu-id="39470-105">EapType element (eaptlsuserpropertiesv1schema)</span></span>

<span data-ttu-id="39470-106">**EapType** 元素是 [Baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md)架構中 [**EapType**](baseeapuserpropertiesv1schema-eaptype-element.md)元素的衍生型別。</span><span class="sxs-lookup"><span data-stu-id="39470-106">The **EapType** element is a derived type of the [**EapType**](baseeapuserpropertiesv1schema-eaptype-element.md) element from the [baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md) schema.</span></span>

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
                    <xs:element
                        ref="Username"
                     />
                    <xs:element name="UserCert"
                        type="hexBinary"
                     />
                    <xs:any
                        processContents="lax"
                        minOccurs="0"
                        maxOccurs="unbounded"
                        namespace="##other"
                     />
                </xs:sequence>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="39470-107">子元素</span><span class="sxs-lookup"><span data-stu-id="39470-107">Child elements</span></span>



| <span data-ttu-id="39470-108">元素</span><span class="sxs-lookup"><span data-stu-id="39470-108">Element</span></span>                                                                   | <span data-ttu-id="39470-109">類型</span><span class="sxs-lookup"><span data-stu-id="39470-109">Type</span></span>      | <span data-ttu-id="39470-110">Description</span><span class="sxs-lookup"><span data-stu-id="39470-110">Description</span></span>                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="39470-111">**使用者**</span><span class="sxs-lookup"><span data-stu-id="39470-111">**Username**</span></span>](eaptlsuserpropertiesv1schema-username-element.md)         |           | <span data-ttu-id="39470-112">捕捉要在 EAP-Identity 回應中傳送的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="39470-112">Captures the user name to be sent in the EAP-Identity response.</span></span> <span data-ttu-id="39470-113">如果 [**Username**](eaptlsuserpropertiesv1schema-username-element.md) 專案不存在，則 eap-tls 會使用 [**UserCert**](eaptlsuserpropertiesv1schema-usercert-eaptype-element.md) 元素中所參考之憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="39470-113">If the [**Username**](eaptlsuserpropertiesv1schema-username-element.md) element is absent, then EAP-TLS uses the name in the certificate referred to in the [**UserCert**](eaptlsuserpropertiesv1schema-usercert-eaptype-element.md) element.</span></span><br/> |
| [<span data-ttu-id="39470-114">**UserCert**</span><span class="sxs-lookup"><span data-stu-id="39470-114">**UserCert**</span></span>](eaptlsuserpropertiesv1schema-usercert-eaptype-element.md) | <span data-ttu-id="39470-115">hexBinary</span><span class="sxs-lookup"><span data-stu-id="39470-115">hexBinary</span></span> | <span data-ttu-id="39470-116">指應用於驗證的憑證 SHA-1 雜湊。</span><span class="sxs-lookup"><span data-stu-id="39470-116">Refers to the SHA-1 hash of the certificate that should be used for authentication.</span></span><br/>                                                                                                                                                                                                                             |



## <a name="remarks"></a><span data-ttu-id="39470-117">備註</span><span class="sxs-lookup"><span data-stu-id="39470-117">Remarks</span></span>

<span data-ttu-id="39470-118">**ProcessContents** 元素可讓架構的未來增強功能。</span><span class="sxs-lookup"><span data-stu-id="39470-118">The **processContents** element enables future enhancements to the schema.</span></span> <span data-ttu-id="39470-119">**ProcessContents** 元素是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="39470-119">The **processContents** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="39470-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="39470-120">Requirements</span></span>



| <span data-ttu-id="39470-121">需求</span><span class="sxs-lookup"><span data-stu-id="39470-121">Requirement</span></span> | <span data-ttu-id="39470-122">值</span><span class="sxs-lookup"><span data-stu-id="39470-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="39470-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="39470-123">Minimum supported client</span></span><br/> | <span data-ttu-id="39470-124">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="39470-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="39470-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="39470-125">Minimum supported server</span></span><br/> | <span data-ttu-id="39470-126">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="39470-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="39470-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="39470-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39470-128">EAPHost 和舊版架構</span><span class="sxs-lookup"><span data-stu-id="39470-128">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="39470-129">eaptlsuserpropertiesv1 架構</span><span class="sxs-lookup"><span data-stu-id="39470-129">eaptlsuserpropertiesv1 Schema</span></span>](eaptlsuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





