---
title: EapMethodType) 元素的 VendorType (
description: 瞭解 (EapMethodType) 元素的 VendorType。 此元素是方法的廠商定義型別。
ms.assetid: baa43e60-05e2-43f9-bb38-896725be76b4
keywords:
- VendorType 元素 EAPHost
topic_type:
- apiref
api_name:
- VendorType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 29030672cea0deff59f7f3026dcac98d6ff1c178
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104463696"
---
# <a name="vendortype-eapmethodtype-element"></a><span data-ttu-id="1aebe-105">EapMethodType) 元素的 VendorType (</span><span class="sxs-lookup"><span data-stu-id="1aebe-105">VendorType (EapMethodType) Element</span></span>

<span data-ttu-id="1aebe-106">**VendorType (EapMethodType)** 元素是該方法的廠商定義型別。</span><span class="sxs-lookup"><span data-stu-id="1aebe-106">The **VendorType (EapMethodType)** element is the vendor defined type for the method.</span></span>

<span data-ttu-id="1aebe-107">**VendorType** 元素是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="1aebe-107">The **VendorType** element is optional.</span></span> <span data-ttu-id="1aebe-108">如果使用，則 **是由** 網際網路指派的號碼授權單位 (IANA) 發出的唯一號碼。</span><span class="sxs-lookup"><span data-stu-id="1aebe-108">If used, the **VendorType** is a unique number issued by Internet Assigned Numbers Authority (IANA).</span></span>

``` syntax
<xs:element name="VendorType"
    type="unsignedInt"
 />
```

<span data-ttu-id="1aebe-109">**VendorType** 元素是由 [**EapMethodType**](eapcommonschema-eapmethodtype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="1aebe-109">The **VendorType** element is defined by the [**EapMethodType**](eapcommonschema-eapmethodtype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="1aebe-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="1aebe-110">Requirements</span></span>



| <span data-ttu-id="1aebe-111">角色</span><span class="sxs-lookup"><span data-stu-id="1aebe-111">Role</span></span> | <span data-ttu-id="1aebe-112">最低支援作業系統版本</span><span class="sxs-lookup"><span data-stu-id="1aebe-112">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="1aebe-113">用戶端</span><span class="sxs-lookup"><span data-stu-id="1aebe-113">Client</span></span><br/> | <span data-ttu-id="1aebe-114">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1aebe-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1aebe-115">伺服器</span><span class="sxs-lookup"><span data-stu-id="1aebe-115">Server</span></span><br/> | <span data-ttu-id="1aebe-116">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1aebe-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1aebe-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1aebe-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="1aebe-118">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="1aebe-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="1aebe-119">**EapMethodType**</span><span class="sxs-lookup"><span data-stu-id="1aebe-119">**EapMethodType**</span></span>](eapcommonschema-eapmethodtype-complextype.md)
</dt> <dt>

[<span data-ttu-id="1aebe-120">EAPHost 和舊版架構</span><span class="sxs-lookup"><span data-stu-id="1aebe-120">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="1aebe-121">eapcommon 架構</span><span class="sxs-lookup"><span data-stu-id="1aebe-121">eapcommon Schema</span></span>](eapcommonschema-schema.md)
</dt> </dl>

 

 





