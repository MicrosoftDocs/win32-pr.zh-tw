---
title: EapHostConfig 元素
description: 包含 EapMethod 元素和 Config 或 ConfigBlob 元素。 無法同時使用 Config 和 ConfigBlob 元素。
ms.assetid: 6c42d71e-0c61-48e4-a447-cfd1eae90297
keywords:
- EapHostConfig 元素 EAPHost
topic_type:
- apiref
api_name:
- EapHostConfig
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 125b5fa2cab8bf3f9da12bd842a1a102beee3fb0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024518"
---
# <a name="eaphostconfig-element"></a><span data-ttu-id="04172-105">EapHostConfig 元素</span><span class="sxs-lookup"><span data-stu-id="04172-105">EapHostConfig Element</span></span>

<span data-ttu-id="04172-106">**EapHostConfig** 元素包含 [**EapMethod**](eaphostconfigschema-eapmethod-eaphostconfig-element.md)元素和 [**Config**](eaphostconfigschema-config-eaphostconfig-element.md)或 [**ConfigBlob**](eaphostconfigschema-configblob-eaphostconfig-element.md)元素。</span><span class="sxs-lookup"><span data-stu-id="04172-106">The **EapHostConfig** element contains the [**EapMethod**](eaphostconfigschema-eapmethod-eaphostconfig-element.md) element and [**Config**](eaphostconfigschema-config-eaphostconfig-element.md) or [**ConfigBlob**](eaphostconfigschema-configblob-eaphostconfig-element.md) element.</span></span>

<span data-ttu-id="04172-107">無法同時使用 [**Config**](eaphostconfigschema-config-eaphostconfig-element.md) 和 [**ConfigBlob**](eaphostconfigschema-configblob-eaphostconfig-element.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="04172-107">The [**Config**](eaphostconfigschema-config-eaphostconfig-element.md) and [**ConfigBlob**](eaphostconfigschema-configblob-eaphostconfig-element.md) elements cannot both be used simultaneously.</span></span>

``` syntax
<xs:element name="EapHostConfig">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="EapMethod"
                type="EapMethodType"
             />
            <xs:choice>
                <xs:element name="Config"
                    type="BaseEapMethodConfig"
                 />
                <xs:element name="ConfigBlob"
                    type="hexBinary"
                 />
            </xs:choice>
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="04172-108">子元素</span><span class="sxs-lookup"><span data-stu-id="04172-108">Child elements</span></span>



| <span data-ttu-id="04172-109">元素</span><span class="sxs-lookup"><span data-stu-id="04172-109">Element</span></span>                                                                    | <span data-ttu-id="04172-110">類型</span><span class="sxs-lookup"><span data-stu-id="04172-110">Type</span></span>                                                                                     | <span data-ttu-id="04172-111">Description</span><span class="sxs-lookup"><span data-stu-id="04172-111">Description</span></span>                                                                                          |
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="04172-112">**配置**</span><span class="sxs-lookup"><span data-stu-id="04172-112">**Config**</span></span>](eaphostconfigschema-config-eaphostconfig-element.md)         | [<span data-ttu-id="04172-113">**BaseEapMethodConfig**</span><span class="sxs-lookup"><span data-stu-id="04172-113">**BaseEapMethodConfig**</span></span>](baseeapmethodconfigschema-baseeapmethodconfig-complextype.md) | <span data-ttu-id="04172-114">當方法設定為 XML 文字格式，而非二進位 BLOB 時，會使用。</span><span class="sxs-lookup"><span data-stu-id="04172-114">Is used when the method configuration is in XML text form instead of a binary BLOB.</span></span><br/>       |
| [<span data-ttu-id="04172-115">**ConfigBlob**</span><span class="sxs-lookup"><span data-stu-id="04172-115">**ConfigBlob**</span></span>](eaphostconfigschema-configblob-eaphostconfig-element.md) | <span data-ttu-id="04172-116">hexBinary</span><span class="sxs-lookup"><span data-stu-id="04172-116">hexBinary</span></span>                                                                                | <span data-ttu-id="04172-117">當方法設定為二進位 BLOB 格式，而不是字串文字格式時，就會使用。</span><span class="sxs-lookup"><span data-stu-id="04172-117">Is used when the method configuration is in binary BLOB form instead of string text form.</span></span><br/> |
| [<span data-ttu-id="04172-118">**EapMethod**</span><span class="sxs-lookup"><span data-stu-id="04172-118">**EapMethod**</span></span>](eaphostconfigschema-eapmethod-eaphostconfig-element.md)   | [<span data-ttu-id="04172-119">**EapMethodType**</span><span class="sxs-lookup"><span data-stu-id="04172-119">**EapMethodType**</span></span>](eapcommonschema-eapmethodtype-complextype.md)                       | <span data-ttu-id="04172-120">識別所參考的方法。</span><span class="sxs-lookup"><span data-stu-id="04172-120">Identifies the method being referred to.</span></span> <br/>                                                 |



## <a name="remarks"></a><span data-ttu-id="04172-121">備註</span><span class="sxs-lookup"><span data-stu-id="04172-121">Remarks</span></span>

<span data-ttu-id="04172-122">**ProcessContents** 元素可讓架構的未來增強功能。</span><span class="sxs-lookup"><span data-stu-id="04172-122">The **processContents** element enables future enhancements to the schema.</span></span> <span data-ttu-id="04172-123">**ProcessContents** 元素是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="04172-123">The **processContents** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="04172-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="04172-124">Requirements</span></span>



| <span data-ttu-id="04172-125">需求</span><span class="sxs-lookup"><span data-stu-id="04172-125">Requirement</span></span> | <span data-ttu-id="04172-126">值</span><span class="sxs-lookup"><span data-stu-id="04172-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="04172-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="04172-127">Minimum supported client</span></span><br/> | <span data-ttu-id="04172-128">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="04172-128">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="04172-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="04172-129">Minimum supported server</span></span><br/> | <span data-ttu-id="04172-130">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="04172-130">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="04172-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="04172-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04172-132">EAPHost 和舊版架構</span><span class="sxs-lookup"><span data-stu-id="04172-132">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="04172-133">eaphostconfig 架構</span><span class="sxs-lookup"><span data-stu-id="04172-133">eaphostconfig Schema</span></span>](eaphostconfigschema-schema.md)
</dt> </dl>

 

 





