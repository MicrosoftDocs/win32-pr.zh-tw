---
title: CertSelection 複雜類型
description: 瞭解 CertSelection 複雜類型。 此類型會決定使用者選取憑證的方式。
ms.assetid: f5a37258-8ab0-4736-9721-6c2800769c74
keywords:
- CertSelection 複雜類型 EAPHost
topic_type:
- apiref
api_name:
- CertSelection
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ba22df8dca61696f214e495542319168183dd2bf
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104316474"
---
# <a name="certselection-complex-type"></a><span data-ttu-id="79e18-105">CertSelection 複雜類型</span><span class="sxs-lookup"><span data-stu-id="79e18-105">CertSelection Complex Type</span></span>

<span data-ttu-id="79e18-106">**CertSelection** 複雜型別決定使用者選取憑證的方式。</span><span class="sxs-lookup"><span data-stu-id="79e18-106">The **CertSelection** complex type determines how the user selects a certificate.</span></span>

``` syntax
<xs:complexType name="CertSelection">
    <xs:sequence>
        <xs:element name="SimpleCertSelection"
            type="boolean"
            minOccurs="0"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="79e18-107">子元素</span><span class="sxs-lookup"><span data-stu-id="79e18-107">Child elements</span></span>



| <span data-ttu-id="79e18-108">元素</span><span class="sxs-lookup"><span data-stu-id="79e18-108">Element</span></span>                                                                                                     | <span data-ttu-id="79e18-109">類型</span><span class="sxs-lookup"><span data-stu-id="79e18-109">Type</span></span>    | <span data-ttu-id="79e18-110">Description</span><span class="sxs-lookup"><span data-stu-id="79e18-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="79e18-111">**SimpleCertSelection**</span><span class="sxs-lookup"><span data-stu-id="79e18-111">**SimpleCertSelection**</span></span>](eaptlsconnectionpropertiesv1schema-simplecertselection-certselection-element.md) | <span data-ttu-id="79e18-112">boolean</span><span class="sxs-lookup"><span data-stu-id="79e18-112">boolean</span></span> | <span data-ttu-id="79e18-113">預設為 TRUE。</span><span class="sxs-lookup"><span data-stu-id="79e18-113">Is TRUE by default.</span></span> <span data-ttu-id="79e18-114">如果 [**SimpleCertSelection**](eaptlsconnectionpropertiesv1schema-simplecertselection-certselection-element.md) 為 TRUE，則 eap-tls 會執行簡單的憑證搜尋，而不需要選取憑證的任何下拉式清單。</span><span class="sxs-lookup"><span data-stu-id="79e18-114">If [**SimpleCertSelection**](eaptlsconnectionpropertiesv1schema-simplecertselection-certselection-element.md) is TRUE, EAP-TLS performs a simple certificate search without any drop-down lists for the selection of certificates.</span></span> <span data-ttu-id="79e18-115">如果 **SimpleCertSelection** 為 FALSE，則 eap-tls 會向使用者說明要選取的適當憑證。</span><span class="sxs-lookup"><span data-stu-id="79e18-115">If **SimpleCertSelection** is FALSE, EAP-TLS illustrates to the user the suitable certificate to be selected.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="79e18-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="79e18-116">Requirements</span></span>



| <span data-ttu-id="79e18-117">角色</span><span class="sxs-lookup"><span data-stu-id="79e18-117">Role</span></span> | <span data-ttu-id="79e18-118">最低支援作業系統版本</span><span class="sxs-lookup"><span data-stu-id="79e18-118">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="79e18-119">用戶端</span><span class="sxs-lookup"><span data-stu-id="79e18-119">Client</span></span><br/> | <span data-ttu-id="79e18-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="79e18-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="79e18-121">伺服器</span><span class="sxs-lookup"><span data-stu-id="79e18-121">Server</span></span><br/> | <span data-ttu-id="79e18-122">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="79e18-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="79e18-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="79e18-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79e18-124">EAPHost 和舊版架構</span><span class="sxs-lookup"><span data-stu-id="79e18-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="79e18-125">eaptlsconnectionpropertiesv1 架構</span><span class="sxs-lookup"><span data-stu-id="79e18-125">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="79e18-126">eaptlsconnectionpropertiesv1 架構複雜類型</span><span class="sxs-lookup"><span data-stu-id="79e18-126">eaptlsconnectionpropertiesv1 Schema Complex Types</span></span>](eaptlsconnectionpropertiesv1schema-complex-types.md)
</dt> </dl>

 

 





