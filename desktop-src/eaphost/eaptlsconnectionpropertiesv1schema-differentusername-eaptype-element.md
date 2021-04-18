---
title: DifferentUsername (EapType) 元素
description: 瞭解 DifferentUsername (EapType) 元素。 此元素決定要使用的使用者名稱。
ms.assetid: f0ce41a9-c774-4d12-8a5a-a8eb1eb84cb0
keywords:
- DifferentUsername 元素 EAPHost
topic_type:
- apiref
api_name:
- DifferentUsername
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 505e23c74d4c1c8c74a50906809d0acc9ce06c42
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "106968934"
---
# <a name="differentusername-eaptype-element"></a><span data-ttu-id="29241-105">DifferentUsername (EapType) 元素</span><span class="sxs-lookup"><span data-stu-id="29241-105">DifferentUsername (EapType) Element</span></span>

<span data-ttu-id="29241-106">**DifferentUsername (EapType)** 元素會決定要使用的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="29241-106">The **DifferentUsername (EapType)** element determines which user name EAP-TLS is to use.</span></span>

``` syntax
<xs:element name="DifferentUsername"
    type="boolean"
 />
```

<span data-ttu-id="29241-107">**DifferentUsername** 元素是由 [**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md)元素定義。</span><span class="sxs-lookup"><span data-stu-id="29241-107">The **DifferentUsername** element is defined by the [**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="29241-108">備註</span><span class="sxs-lookup"><span data-stu-id="29241-108">Remarks</span></span>

<span data-ttu-id="29241-109">如果 **DifferentUserName** 元素為 TRUE，則 eap-tls 應該使用憑證上所顯示的名稱以外的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="29241-109">If the **DifferentUserName** element is TRUE, EAP-TLS should use a user name other than the name that appears on the certificate.</span></span> <span data-ttu-id="29241-110">如果 **DifferentUserName** 元素為 FALSE，則 eap-tls 會使用憑證上出現的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="29241-110">If the **DifferentUserName** element is FALSE, EAP-TLS uses the user name that appears on the certificate.</span></span>

<span data-ttu-id="29241-111">**DifferentUserName** 元素是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="29241-111">The **DifferentUserName** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="29241-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="29241-112">Requirements</span></span>



| <span data-ttu-id="29241-113">角色</span><span class="sxs-lookup"><span data-stu-id="29241-113">Role</span></span> | <span data-ttu-id="29241-114">最低支援作業系統版本</span><span class="sxs-lookup"><span data-stu-id="29241-114">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="29241-115">用戶端</span><span class="sxs-lookup"><span data-stu-id="29241-115">Client</span></span><br/> | <span data-ttu-id="29241-116">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="29241-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="29241-117">伺服器</span><span class="sxs-lookup"><span data-stu-id="29241-117">Server</span></span><br/> | <span data-ttu-id="29241-118">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="29241-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="29241-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="29241-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="29241-120">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="29241-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="29241-121">**EapType**</span><span class="sxs-lookup"><span data-stu-id="29241-121">**EapType**</span></span>](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="29241-122">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="29241-122">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="29241-123">**EapType**</span><span class="sxs-lookup"><span data-stu-id="29241-123">**EapType**</span></span>](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
<span data-ttu-id="29241-124"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="29241-124"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="29241-125">EAPHost 和舊版架構</span><span class="sxs-lookup"><span data-stu-id="29241-125">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="29241-126">eaptlsconnectionpropertiesv1 架構</span><span class="sxs-lookup"><span data-stu-id="29241-126">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="29241-127">eaptlsconnectionpropertiesv1 架構元素</span><span class="sxs-lookup"><span data-stu-id="29241-127">eaptlsconnectionpropertiesv1 Schema Elements</span></span>](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





