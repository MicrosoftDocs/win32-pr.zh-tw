---
title: SimpleCertSelection (CertSelection) 元素
description: 瞭解 SimpleCertSelection (CertSelection) 元素。 此元素決定使用者選取憑證的方式。
ms.assetid: 28454877-fd07-4b47-9544-f2b4e91c6651
keywords:
- SimpleCertSelection 元素 EAPHost
topic_type:
- apiref
api_name:
- SimpleCertSelection
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 30af9872f7583232e91b037c5b8961e18c7ce863
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104024105"
---
# <a name="simplecertselection-certselection-element"></a><span data-ttu-id="393e7-105">SimpleCertSelection (CertSelection) 元素</span><span class="sxs-lookup"><span data-stu-id="393e7-105">SimpleCertSelection (CertSelection) Element</span></span>

<span data-ttu-id="393e7-106">**SimpleCertSelection (CertSelection)** 元素會決定使用者選取憑證的方式。</span><span class="sxs-lookup"><span data-stu-id="393e7-106">The **SimpleCertSelection (CertSelection)** element determines how the user selects a certificate.</span></span>

``` syntax
<xs:element name="SimpleCertSelection"
    type="boolean"
 />
```

<span data-ttu-id="393e7-107">**SimpleCertSelection** 元素是由 [**CertSelection**](eaptlsconnectionpropertiesv1schema-certselection-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="393e7-107">The **SimpleCertSelection** element is defined by the [**CertSelection**](eaptlsconnectionpropertiesv1schema-certselection-complextype.md) complex type.</span></span>

## <a name="remarks"></a><span data-ttu-id="393e7-108">備註</span><span class="sxs-lookup"><span data-stu-id="393e7-108">Remarks</span></span>

<span data-ttu-id="393e7-109">依預設， **SimpleCertSelection** 為 TRUE。</span><span class="sxs-lookup"><span data-stu-id="393e7-109">**SimpleCertSelection** is TRUE by default.</span></span> <span data-ttu-id="393e7-110">如果 **SimpleCertSelection** 為 TRUE，則 eap-tls 會執行簡單的憑證搜尋，而不需要選取憑證的任何下拉式清單。</span><span class="sxs-lookup"><span data-stu-id="393e7-110">If **SimpleCertSelection** is TRUE, EAP-TLS performs a simple certificate search without any drop-down lists for the selection of certificates.</span></span> <span data-ttu-id="393e7-111">如果 **SimpleCertSelection** 為 FALSE，則 eap-tls 會向使用者說明要選取的適當憑證。</span><span class="sxs-lookup"><span data-stu-id="393e7-111">If **SimpleCertSelection** is FALSE, EAP-TLS illustrates to the user the suitable certificate to be selected.</span></span>

## <a name="requirements"></a><span data-ttu-id="393e7-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="393e7-112">Requirements</span></span>



| <span data-ttu-id="393e7-113">角色</span><span class="sxs-lookup"><span data-stu-id="393e7-113">Role</span></span> | <span data-ttu-id="393e7-114">支援 OS 的最低版本</span><span class="sxs-lookup"><span data-stu-id="393e7-114">Minimum supported OS</span></span> |
|------|----------------------|
| <span data-ttu-id="393e7-115">用戶端</span><span class="sxs-lookup"><span data-stu-id="393e7-115">Client</span></span><br/> | <span data-ttu-id="393e7-116">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="393e7-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="393e7-117">伺服器</span><span class="sxs-lookup"><span data-stu-id="393e7-117">Server</span></span><br/> | <span data-ttu-id="393e7-118">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="393e7-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="393e7-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="393e7-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="393e7-120">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="393e7-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="393e7-121">**CertSelection**</span><span class="sxs-lookup"><span data-stu-id="393e7-121">**CertSelection**</span></span>](eaptlsconnectionpropertiesv1schema-certselection-complextype.md)
</dt> <dt>

<span data-ttu-id="393e7-122">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="393e7-122">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="393e7-123">**CertificateStore (CredentialsSourceParameters)**</span><span class="sxs-lookup"><span data-stu-id="393e7-123">**CertificateStore (CredentialsSourceParameters)**</span></span>](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md)
<span data-ttu-id="393e7-124"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="393e7-124"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="393e7-125">EAPHost 和舊版架構</span><span class="sxs-lookup"><span data-stu-id="393e7-125">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="393e7-126">eaptlsconnectionpropertiesv1 架構</span><span class="sxs-lookup"><span data-stu-id="393e7-126">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="393e7-127">eaptlsconnectionpropertiesv1 架構元素</span><span class="sxs-lookup"><span data-stu-id="393e7-127">eaptlsconnectionpropertiesv1 Schema Elements</span></span>](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





