---
title: " (EapMethodType) 元素的 VendorId"
description: 如果類型 (EapMethodType) 元素為 254 (擴充的 EAP 方法) ，則會參考定義方法的廠商。
ms.assetid: 14992940-2fe5-4f85-91c0-1f61345ee90f
keywords:
- VendorId 元素 EAPHost
topic_type:
- apiref
api_name:
- VendorId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9091cdbd7620baf6ec5dc893bd2100b2f04585ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508651"
---
# <a name="vendorid-eapmethodtype-element"></a><span data-ttu-id="db11c-104"> (EapMethodType) 元素的 VendorId</span><span class="sxs-lookup"><span data-stu-id="db11c-104">VendorId (EapMethodType) Element</span></span>

<span data-ttu-id="db11c-105">如果 [**類型 (EapMethodType)**](eapcommonschema-type-eapmethodtype-element.md)元素是 254 (擴充的 EAP 方法) ，則 **(EapMethodType)** 元素會參考定義方法的廠商。</span><span class="sxs-lookup"><span data-stu-id="db11c-105">The **VendorId (EapMethodType)** element refers to the vendor who defined the method if the [**Type (EapMethodType)**](eapcommonschema-type-eapmethodtype-element.md) element is 254 (an expanded EAP method).</span></span>

<span data-ttu-id="db11c-106">**VendorId** 是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="db11c-106">The **VendorId** is optional.</span></span> <span data-ttu-id="db11c-107">如果使用，則 **是由** 網際網路指派的號碼授權單位所發出的唯一號碼 (IANA) 。</span><span class="sxs-lookup"><span data-stu-id="db11c-107">If used, the **VendorId** is a unique number issued by Internet Assigned Numbers Authority (IANA).</span></span>

``` syntax
<xs:element name="VendorId"
    type="unsignedInt"
 />
```

<span data-ttu-id="db11c-108">**VendorId** 元素是由 [**EapMethodType**](eapcommonschema-eapmethodtype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="db11c-108">The **VendorId** element is defined by the [**EapMethodType**](eapcommonschema-eapmethodtype-complextype.md) complex type.</span></span>

## <a name="remarks"></a><span data-ttu-id="db11c-109">備註</span><span class="sxs-lookup"><span data-stu-id="db11c-109">Remarks</span></span>

<span data-ttu-id="db11c-110">針對特定方法， [**作者**](eapcommonschema-authorid-eapmethodtype-element.md) 和 **VendorId** 元素不需要相同的。</span><span class="sxs-lookup"><span data-stu-id="db11c-110">The [**AuthorId**](eapcommonschema-authorid-eapmethodtype-element.md) and **VendorId** elements do not need to be the same for a particular method.</span></span>

## <a name="requirements"></a><span data-ttu-id="db11c-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="db11c-111">Requirements</span></span>



| <span data-ttu-id="db11c-112">需求</span><span class="sxs-lookup"><span data-stu-id="db11c-112">Requirement</span></span> | <span data-ttu-id="db11c-113">值</span><span class="sxs-lookup"><span data-stu-id="db11c-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="db11c-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="db11c-114">Minimum supported client</span></span><br/> | <span data-ttu-id="db11c-115">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="db11c-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="db11c-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="db11c-116">Minimum supported server</span></span><br/> | <span data-ttu-id="db11c-117">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="db11c-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="db11c-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="db11c-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="db11c-119">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="db11c-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="db11c-120">**EapMethodType**</span><span class="sxs-lookup"><span data-stu-id="db11c-120">**EapMethodType**</span></span>](eapcommonschema-eapmethodtype-complextype.md)
</dt> <dt>

[<span data-ttu-id="db11c-121">EAPHost 和舊版架構</span><span class="sxs-lookup"><span data-stu-id="db11c-121">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="db11c-122">eapcommon 架構</span><span class="sxs-lookup"><span data-stu-id="db11c-122">eapcommon Schema</span></span>](eapcommonschema-schema.md)
</dt> </dl>

 

 





