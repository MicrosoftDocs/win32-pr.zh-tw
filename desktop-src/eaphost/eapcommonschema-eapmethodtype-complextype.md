---
title: EapMethodType 複雜類型
description: 定義可唯一識別單一 EAP 方法類型、VendorId、VendorType 和作者的元素。
ms.assetid: 3ef96187-7376-438d-9d47-a87d5a6c9b8b
keywords:
- EapMethodType 複雜類型 EAPHost
topic_type:
- apiref
api_name:
- EapMethodType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cea2448111266696398d1581aaecdbec2fb5859e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685993"
---
# <a name="eapmethodtype-complex-type"></a><span data-ttu-id="a235d-104">EapMethodType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="a235d-104">EapMethodType Complex Type</span></span>

<span data-ttu-id="a235d-105">**EapMethodType** 複雜型別會定義可唯一識別單一 EAP 方法的專案： [**type**](eapcommonschema-type-eapmethodtype-element.md)、 [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md)、 [**VendorType**](eapcommonschema-vendortype-eapmethodtype-element.md)和 [**作者**](eapcommonschema-authorid-eapmethodtype-element.md)。</span><span class="sxs-lookup"><span data-stu-id="a235d-105">The **EapMethodType** complex type defines the elements that uniquely identify a single EAP method: [**Type**](eapcommonschema-type-eapmethodtype-element.md), [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md), [**VendorType**](eapcommonschema-vendortype-eapmethodtype-element.md), and [**AuthorId**](eapcommonschema-authorid-eapmethodtype-element.md).</span></span>

<span data-ttu-id="a235d-106">[**型**](eapcommonschema-type-eapmethodtype-element.md)別 [**和作者**](eapcommonschema-authorid-eapmethodtype-element.md)是必要元素，而只有當 **type** 元素是 254 (擴充的 EAP 方法) 時，才需要使用 [**VendorType**](eapcommonschema-vendortype-eapmethodtype-element.md)和 [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md) 。</span><span class="sxs-lookup"><span data-stu-id="a235d-106">[**Type**](eapcommonschema-type-eapmethodtype-element.md) and [**AuthorId**](eapcommonschema-authorid-eapmethodtype-element.md) are mandatory elements, whereas [**VendorType**](eapcommonschema-vendortype-eapmethodtype-element.md) and [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md) are required only when the **Type** element is 254 (an expanded EAP method).</span></span>

``` syntax
<xs:complexType name="EapMethodType">
    <xs:sequence>
        <xs:element name="Type"
            type="unsignedByte"
         />
        <xs:element name="VendorId"
            type="unsignedInt"
            default="0"
            minOccurs="0"
         />
        <xs:element name="VendorType"
            type="unsignedInt"
            default="0"
            minOccurs="0"
         />
        <xs:element name="AuthorId"
            type="unsignedInt"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="a235d-107">子元素</span><span class="sxs-lookup"><span data-stu-id="a235d-107">Child elements</span></span>



| <span data-ttu-id="a235d-108">元素</span><span class="sxs-lookup"><span data-stu-id="a235d-108">Element</span></span>                                                                | <span data-ttu-id="a235d-109">類型</span><span class="sxs-lookup"><span data-stu-id="a235d-109">Type</span></span>         | <span data-ttu-id="a235d-110">Description</span><span class="sxs-lookup"><span data-stu-id="a235d-110">Description</span></span>                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a235d-111">**作者**</span><span class="sxs-lookup"><span data-stu-id="a235d-111">**AuthorId**</span></span>](eapcommonschema-authorid-eapmethodtype-element.md)     | <span data-ttu-id="a235d-112">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a235d-112">unsignedInt</span></span>  | <span data-ttu-id="a235d-113">指的是方法作者。</span><span class="sxs-lookup"><span data-stu-id="a235d-113">Refers to the method author.</span></span> <br/>                                                                                                                                                                                                                 |
| [<span data-ttu-id="a235d-114">**類型**</span><span class="sxs-lookup"><span data-stu-id="a235d-114">**Type**</span></span>](eapcommonschema-type-eapmethodtype-element.md)             | <span data-ttu-id="a235d-115">unsignedByte</span><span class="sxs-lookup"><span data-stu-id="a235d-115">unsignedByte</span></span> | <span data-ttu-id="a235d-116">代表 EAP 方法類型。</span><span class="sxs-lookup"><span data-stu-id="a235d-116">Refers to the EAP method type.</span></span> <br/>                                                                                                                                                                                                               |
| [<span data-ttu-id="a235d-117">**VendorId**</span><span class="sxs-lookup"><span data-stu-id="a235d-117">**VendorId**</span></span>](eapcommonschema-vendorid-eapmethodtype-element.md)     | <span data-ttu-id="a235d-118">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a235d-118">unsignedInt</span></span>  | <span data-ttu-id="a235d-119">代表定義方法的廠商-如果 [**Type**](eapcommonschema-type-eapmethodtype-element.md) 元素是 254 (擴充的 EAP 方法) 。</span><span class="sxs-lookup"><span data-stu-id="a235d-119">Refers to the vendor who defined the method - if the [**Type**](eapcommonschema-type-eapmethodtype-element.md) element is 254 (an expanded EAP method).</span></span> <span data-ttu-id="a235d-120">[**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md)是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="a235d-120">The [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md) is optional.</span></span> <br/> |
| [<span data-ttu-id="a235d-121">**VendorType**</span><span class="sxs-lookup"><span data-stu-id="a235d-121">**VendorType**</span></span>](eapcommonschema-vendortype-eapmethodtype-element.md) | <span data-ttu-id="a235d-122">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a235d-122">unsignedInt</span></span>  | <span data-ttu-id="a235d-123">是方法的廠商定義型別。</span><span class="sxs-lookup"><span data-stu-id="a235d-123">Is the vendor defined type for the method.</span></span> <span data-ttu-id="a235d-124">[**VendorType**](eapcommonschema-vendortype-eapmethodtype-element.md)是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="a235d-124">The [**VendorType**](eapcommonschema-vendortype-eapmethodtype-element.md) is optional.</span></span> <br/>                                                                                                           |



## <a name="remarks"></a><span data-ttu-id="a235d-125">備註</span><span class="sxs-lookup"><span data-stu-id="a235d-125">Remarks</span></span>

<span data-ttu-id="a235d-126">針對特定方法， [**作者**](eapcommonschema-authorid-eapmethodtype-element.md) 和 [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md) 元素不需要相同的。</span><span class="sxs-lookup"><span data-stu-id="a235d-126">The [**AuthorId**](eapcommonschema-authorid-eapmethodtype-element.md) and [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md) elements do not need to be the same for a particular method.</span></span>

<span data-ttu-id="a235d-127">[**作者**](eapcommonschema-authorid-eapmethodtype-element.md)、[**類型**](eapcommonschema-type-eapmethodtype-element.md)、 [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md)和 [**VendorType**](eapcommonschema-vendortype-eapmethodtype-element.md)元素都是由網際網路指派的數位授權單位所發出的唯一號碼 (IANA) 。</span><span class="sxs-lookup"><span data-stu-id="a235d-127">The [**AuthorId**](eapcommonschema-authorid-eapmethodtype-element.md), [**Type**](eapcommonschema-type-eapmethodtype-element.md), [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md) and [**VendorType**](eapcommonschema-vendortype-eapmethodtype-element.md) elements are each a unique number issued by the Internet Assigned Numbers Authority (IANA).</span></span>

## <a name="requirements"></a><span data-ttu-id="a235d-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="a235d-128">Requirements</span></span>



| <span data-ttu-id="a235d-129">需求</span><span class="sxs-lookup"><span data-stu-id="a235d-129">Requirement</span></span> | <span data-ttu-id="a235d-130">值</span><span class="sxs-lookup"><span data-stu-id="a235d-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a235d-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a235d-131">Minimum supported client</span></span><br/> | <span data-ttu-id="a235d-132">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a235d-132">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a235d-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a235d-133">Minimum supported server</span></span><br/> | <span data-ttu-id="a235d-134">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a235d-134">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a235d-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a235d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a235d-136">EAPHost 和舊版架構</span><span class="sxs-lookup"><span data-stu-id="a235d-136">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="a235d-137">eapcommon 架構</span><span class="sxs-lookup"><span data-stu-id="a235d-137">eapcommon Schema</span></span>](eapcommonschema-schema.md)
</dt> </dl>

 

 





