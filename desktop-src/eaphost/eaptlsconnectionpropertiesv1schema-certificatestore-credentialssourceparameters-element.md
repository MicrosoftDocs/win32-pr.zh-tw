---
title: CertificateStore (CredentialsSourceParameters) 元素
description: 指出 EAP-TLS 應該從使用者的 [我的存放區] 或正在驗證的電腦讀取憑證。
ms.assetid: 6b15c7cc-b686-4419-a962-e3dd6b4b84a6
keywords:
- CertificateStore 元素 EAPHost
topic_type:
- apiref
api_name:
- CertificateStore
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cc7c8841fe275d19752f8b774de5766b95824339
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508944"
---
# <a name="certificatestore-credentialssourceparameters-element"></a><span data-ttu-id="4c4b5-104">CertificateStore (CredentialsSourceParameters) 元素</span><span class="sxs-lookup"><span data-stu-id="4c4b5-104">CertificateStore (CredentialsSourceParameters) Element</span></span>

<span data-ttu-id="4c4b5-105">**CertificateStore (CredentialsSourceParameters)** 元素表示 eap-tls 應該從使用者的 [我的存放區] 或正在驗證的電腦讀取憑證。</span><span class="sxs-lookup"><span data-stu-id="4c4b5-105">The **CertificateStore (CredentialsSourceParameters)** element indicates that EAP-TLS should read the certificate from the user's My Store, or the machine being authenticated.</span></span>

``` syntax
<xs:element name="CertificateStore"
    type="CertSelection"
 />
```

<span data-ttu-id="4c4b5-106">**CertificateStore** 元素是由 [**CredentialsSourceParameters**](eaptlsconnectionpropertiesv1schema-credentialssourceparameters-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="4c4b5-106">The **CertificateStore** element is defined by the [**CredentialsSourceParameters**](eaptlsconnectionpropertiesv1schema-credentialssourceparameters-complextype.md) complex type.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c4b5-107">備註</span><span class="sxs-lookup"><span data-stu-id="4c4b5-107">Remarks</span></span>

<span data-ttu-id="4c4b5-108">**CertificateStore** 和 [**智慧卡**](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md)元素不能同時使用。</span><span class="sxs-lookup"><span data-stu-id="4c4b5-108">The **CertificateStore** and [**SmartCard**](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md) elements cannot both be used simultaneously.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c4b5-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="4c4b5-109">Requirements</span></span>



| <span data-ttu-id="4c4b5-110">需求</span><span class="sxs-lookup"><span data-stu-id="4c4b5-110">Requirement</span></span> | <span data-ttu-id="4c4b5-111">值</span><span class="sxs-lookup"><span data-stu-id="4c4b5-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4c4b5-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4c4b5-112">Minimum supported client</span></span><br/> | <span data-ttu-id="4c4b5-113">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4c4b5-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4c4b5-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4c4b5-114">Minimum supported server</span></span><br/> | <span data-ttu-id="4c4b5-115">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4c4b5-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4c4b5-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4c4b5-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="4c4b5-117">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="4c4b5-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="4c4b5-118">**CredentialsSourceParameters**</span><span class="sxs-lookup"><span data-stu-id="4c4b5-118">**CredentialsSourceParameters**</span></span>](eaptlsconnectionpropertiesv1schema-credentialssourceparameters-complextype.md)
</dt> <dt>

<span data-ttu-id="4c4b5-119">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="4c4b5-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="4c4b5-120">**CredentialsSource (EapType)**</span><span class="sxs-lookup"><span data-stu-id="4c4b5-120">**CredentialsSource (EapType)**</span></span>](eaptlsconnectionpropertiesv1schema-credentialssource-eaptype-element.md)
<span data-ttu-id="4c4b5-121"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="4c4b5-121"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="4c4b5-122">EAPHost 和舊版架構</span><span class="sxs-lookup"><span data-stu-id="4c4b5-122">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="4c4b5-123">eaptlsconnectionpropertiesv1 架構</span><span class="sxs-lookup"><span data-stu-id="4c4b5-123">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="4c4b5-124">eaptlsconnectionpropertiesv1 架構元素</span><span class="sxs-lookup"><span data-stu-id="4c4b5-124">eaptlsconnectionpropertiesv1 Schema Elements</span></span>](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





