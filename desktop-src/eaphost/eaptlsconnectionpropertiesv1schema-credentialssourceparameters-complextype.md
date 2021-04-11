---
title: CredentialsSourceParameters 複雜類型
description: 定義所需的元素，以指定要與 EAP-TLS 驗證搭配使用的憑證來源。
ms.assetid: 1482694e-3025-4231-8154-4be0301fe5ce
keywords:
- CredentialsSourceParameters 複雜類型 EAPHost
topic_type:
- apiref
api_name:
- CredentialsSourceParameters
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 912faa4a388d9a57225991959625a978ca0921f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104868"
---
# <a name="credentialssourceparameters-complex-type"></a><span data-ttu-id="78545-104">CredentialsSourceParameters 複雜類型</span><span class="sxs-lookup"><span data-stu-id="78545-104">CredentialsSourceParameters Complex Type</span></span>

<span data-ttu-id="78545-105">**CredentialsSourceParameters** 複雜型別會定義必要的元素，以指定要與 eap-tls 驗證搭配使用的憑證來源。</span><span class="sxs-lookup"><span data-stu-id="78545-105">The **CredentialsSourceParameters** complex type defines the element required to specify the source of the certificate to be used with an EAP-TLS authentication.</span></span>

<span data-ttu-id="78545-106">[**智慧卡**](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md)元素或 [**CertificateStore**](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md)元素之間有一個選擇。</span><span class="sxs-lookup"><span data-stu-id="78545-106">There is a choice between the [**SmartCard**](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md) element or [**CertificateStore**](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md) element.</span></span>

``` syntax
<xs:complexType name="CredentialsSourceParameters">
    <xs:choice>
        <xs:element name="SmartCard"
            type="emptyString"
         />
        <xs:element name="CertificateStore"
            type="CertSelection"
         />
    </xs:choice>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="78545-107">子元素</span><span class="sxs-lookup"><span data-stu-id="78545-107">Child elements</span></span>



| <span data-ttu-id="78545-108">元素</span><span class="sxs-lookup"><span data-stu-id="78545-108">Element</span></span>                                                                                                             | <span data-ttu-id="78545-109">類型</span><span class="sxs-lookup"><span data-stu-id="78545-109">Type</span></span>                                                                                  | <span data-ttu-id="78545-110">Description</span><span class="sxs-lookup"><span data-stu-id="78545-110">Description</span></span>                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="78545-111">**CertificateStore**</span><span class="sxs-lookup"><span data-stu-id="78545-111">**CertificateStore**</span></span>](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md) | [<span data-ttu-id="78545-112">**CertSelection**</span><span class="sxs-lookup"><span data-stu-id="78545-112">**CertSelection**</span></span>](eaptlsconnectionpropertiesv1schema-certselection-complextype.md) | <span data-ttu-id="78545-113">指出 EAP-TLS 應該從使用者的 [我的存放區] 或正在驗證的電腦讀取憑證。</span><span class="sxs-lookup"><span data-stu-id="78545-113">Indicates that EAP-TLS should read the certificate from the user's My Store, or the machine being authenticated.</span></span> <br/> |
| [<span data-ttu-id="78545-114">**智慧卡**</span><span class="sxs-lookup"><span data-stu-id="78545-114">**SmartCard**</span></span>](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md)               | [<span data-ttu-id="78545-115">**emptyString**</span><span class="sxs-lookup"><span data-stu-id="78545-115">**emptyString**</span></span>](eaptlsconnectionpropertiesv1schema-emptystring-simpletype.md)      | <span data-ttu-id="78545-116">表示 EAP-TLS 應該從智慧卡讀取憑證。</span><span class="sxs-lookup"><span data-stu-id="78545-116">Indicates that EAP-TLS should read the certificate from the Smart Card.</span></span> <br/>                                          |



## <a name="remarks"></a><span data-ttu-id="78545-117">備註</span><span class="sxs-lookup"><span data-stu-id="78545-117">Remarks</span></span>

<span data-ttu-id="78545-118">[**CertificateStore**](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md)和 [**智慧卡**](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md)元素不能同時使用。</span><span class="sxs-lookup"><span data-stu-id="78545-118">The [**CertificateStore**](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md) and [**SmartCard**](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md) elements cannot both be used simultaneously.</span></span>

## <a name="requirements"></a><span data-ttu-id="78545-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="78545-119">Requirements</span></span>



| <span data-ttu-id="78545-120">需求</span><span class="sxs-lookup"><span data-stu-id="78545-120">Requirement</span></span> | <span data-ttu-id="78545-121">值</span><span class="sxs-lookup"><span data-stu-id="78545-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="78545-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="78545-122">Minimum supported client</span></span><br/> | <span data-ttu-id="78545-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="78545-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="78545-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="78545-124">Minimum supported server</span></span><br/> | <span data-ttu-id="78545-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="78545-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="78545-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="78545-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78545-127">EAPHost 和舊版架構</span><span class="sxs-lookup"><span data-stu-id="78545-127">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="78545-128">eaptlsconnectionpropertiesv1 架構</span><span class="sxs-lookup"><span data-stu-id="78545-128">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="78545-129">eaptlsconnectionpropertiesv1 架構複雜類型</span><span class="sxs-lookup"><span data-stu-id="78545-129">eaptlsconnectionpropertiesv1 Schema Complex Types</span></span>](eaptlsconnectionpropertiesv1schema-complex-types.md)
</dt> </dl>

 

 





