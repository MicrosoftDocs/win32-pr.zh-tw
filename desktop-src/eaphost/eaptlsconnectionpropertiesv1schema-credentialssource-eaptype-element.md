---
title: CredentialsSource (EapType) 元素
description: 瞭解 CredentialsSource (EapType) 元素。 此元素包含 EAP-TLS 憑證位置的相關資訊。
ms.assetid: 6ef48e5e-7c71-472f-ab01-0a43a97ecd96
keywords:
- CredentialsSource 元素 EAPHost
topic_type:
- apiref
api_name:
- CredentialsSource
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d68eccf44b7e2c248e366d8e3d8f05f4e7dd4774
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "106969938"
---
# <a name="credentialssource-eaptype-element"></a><span data-ttu-id="82fd8-105">CredentialsSource (EapType) 元素</span><span class="sxs-lookup"><span data-stu-id="82fd8-105">CredentialsSource (EapType) Element</span></span>

<span data-ttu-id="82fd8-106">**CredentialsSource (EapType)** 元素包含 eap-tls 憑證位置的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="82fd8-106">The **CredentialsSource (EapType)** element contains information about the location of the EAP-TLS certificate.</span></span>

``` syntax
<xs:element name="CredentialsSource"
    type="CredentialsSourceParameters"
 />
```

<span data-ttu-id="82fd8-107">**CredentialsSource** 元素是由 [**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md)元素定義。</span><span class="sxs-lookup"><span data-stu-id="82fd8-107">The **CredentialsSource** element is defined by the [**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="82fd8-108">備註</span><span class="sxs-lookup"><span data-stu-id="82fd8-108">Remarks</span></span>

<span data-ttu-id="82fd8-109">**CredentialSource** 元素是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="82fd8-109">The **CredentialSource** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="82fd8-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="82fd8-110">Requirements</span></span>



| <span data-ttu-id="82fd8-111">角色</span><span class="sxs-lookup"><span data-stu-id="82fd8-111">Role</span></span> | <span data-ttu-id="82fd8-112">最低支援作業系統版本</span><span class="sxs-lookup"><span data-stu-id="82fd8-112">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="82fd8-113">用戶端</span><span class="sxs-lookup"><span data-stu-id="82fd8-113">Client</span></span><br/> | <span data-ttu-id="82fd8-114">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="82fd8-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="82fd8-115">伺服器</span><span class="sxs-lookup"><span data-stu-id="82fd8-115">Server</span></span><br/> | <span data-ttu-id="82fd8-116">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="82fd8-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="82fd8-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="82fd8-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="82fd8-118">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="82fd8-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="82fd8-119">**EapType**</span><span class="sxs-lookup"><span data-stu-id="82fd8-119">**EapType**</span></span>](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="82fd8-120">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="82fd8-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="82fd8-121">**EapType**</span><span class="sxs-lookup"><span data-stu-id="82fd8-121">**EapType**</span></span>](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
<span data-ttu-id="82fd8-122"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="82fd8-122"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="82fd8-123">EAPHost 和舊版架構</span><span class="sxs-lookup"><span data-stu-id="82fd8-123">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="82fd8-124">eaptlsconnectionpropertiesv1 架構</span><span class="sxs-lookup"><span data-stu-id="82fd8-124">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="82fd8-125">eaptlsconnectionpropertiesv1 架構元素</span><span class="sxs-lookup"><span data-stu-id="82fd8-125">eaptlsconnectionpropertiesv1 Schema Elements</span></span>](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





