---
title: 智慧卡 (CredentialsSourceParameters) 元素
description: 表示 EAP-TLS 應該從智慧卡讀取憑證。
ms.assetid: 0755b0bf-520a-4ae6-a8fc-2f69ae12b066
keywords:
- 智慧卡元素 EAPHost
topic_type:
- apiref
api_name:
- SmartCard
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 14581a06064a242a0f66e763e0b848d7d74bce50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966514"
---
# <a name="smartcard-credentialssourceparameters-element"></a><span data-ttu-id="70a1a-104">智慧卡 (CredentialsSourceParameters) 元素</span><span class="sxs-lookup"><span data-stu-id="70a1a-104">SmartCard (CredentialsSourceParameters) Element</span></span>

<span data-ttu-id="70a1a-105">**智慧卡 (CredentialsSourceParameters)** 元素表示 eap-tls 應該從智慧卡讀取憑證。</span><span class="sxs-lookup"><span data-stu-id="70a1a-105">The **SmartCard (CredentialsSourceParameters)** element indicates that EAP-TLS should read the certificate from the Smart Card.</span></span>

``` syntax
<xs:element name="SmartCard"
    type="emptyString"
 />
```

<span data-ttu-id="70a1a-106">**智慧卡** 元素是由 [**CredentialsSourceParameters**](eaptlsconnectionpropertiesv1schema-credentialssourceparameters-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="70a1a-106">The **SmartCard** element is defined by the [**CredentialsSourceParameters**](eaptlsconnectionpropertiesv1schema-credentialssourceparameters-complextype.md) complex type.</span></span>

## <a name="remarks"></a><span data-ttu-id="70a1a-107">備註</span><span class="sxs-lookup"><span data-stu-id="70a1a-107">Remarks</span></span>

<span data-ttu-id="70a1a-108">[**CertificateStore**](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md)和 **智慧卡** 元素不能同時使用。</span><span class="sxs-lookup"><span data-stu-id="70a1a-108">The [**CertificateStore**](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md) and **SmartCard** elements cannot both be used simultaneously.</span></span>

## <a name="requirements"></a><span data-ttu-id="70a1a-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="70a1a-109">Requirements</span></span>



| <span data-ttu-id="70a1a-110">需求</span><span class="sxs-lookup"><span data-stu-id="70a1a-110">Requirement</span></span> | <span data-ttu-id="70a1a-111">值</span><span class="sxs-lookup"><span data-stu-id="70a1a-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="70a1a-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="70a1a-112">Minimum supported client</span></span><br/> | <span data-ttu-id="70a1a-113">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="70a1a-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="70a1a-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="70a1a-114">Minimum supported server</span></span><br/> | <span data-ttu-id="70a1a-115">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="70a1a-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="70a1a-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="70a1a-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="70a1a-117">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="70a1a-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="70a1a-118">**CredentialsSourceParameters**</span><span class="sxs-lookup"><span data-stu-id="70a1a-118">**CredentialsSourceParameters**</span></span>](eaptlsconnectionpropertiesv1schema-credentialssourceparameters-complextype.md)
</dt> <dt>

<span data-ttu-id="70a1a-119">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="70a1a-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="70a1a-120">**CredentialsSource (EapType)**</span><span class="sxs-lookup"><span data-stu-id="70a1a-120">**CredentialsSource (EapType)**</span></span>](eaptlsconnectionpropertiesv1schema-credentialssource-eaptype-element.md)
<span data-ttu-id="70a1a-121"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="70a1a-121"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="70a1a-122">EAPHost 和舊版架構</span><span class="sxs-lookup"><span data-stu-id="70a1a-122">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="70a1a-123">eaptlsconnectionpropertiesv1 架構</span><span class="sxs-lookup"><span data-stu-id="70a1a-123">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="70a1a-124">eaptlsconnectionpropertiesv1 架構元素</span><span class="sxs-lookup"><span data-stu-id="70a1a-124">eaptlsconnectionpropertiesv1 Schema Elements</span></span>](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





