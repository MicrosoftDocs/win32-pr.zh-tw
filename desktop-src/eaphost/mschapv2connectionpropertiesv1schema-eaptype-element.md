---
title: 'EapType 元素 (mschapv2connectionpropertiesv1schema) '
description: 這是 baseeapconnectionpropertiesv1 架構中 EapType 元素的衍生型別。 這是出現在 EapHostConfig 架構之 Config 元素內的最上層元素。
ms.assetid: dbd63387-f8ed-4308-903f-7a555f3410f7
keywords:
- EapType 元素 EAPHost
topic_type:
- apiref
api_name:
- EapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3e9b7db3d3e3ab1ba90427a65a5544b87939ca88
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/02/2021
ms.locfileid: "106996542"
---
# <a name="eaptype-element-mschapv2connectionpropertiesv1schema"></a><span data-ttu-id="b24a7-105">EapType 元素 (mschapv2connectionpropertiesv1schema) </span><span class="sxs-lookup"><span data-stu-id="b24a7-105">EapType Element (mschapv2connectionpropertiesv1schema)</span></span>

<span data-ttu-id="b24a7-106">**EapType** 元素是 [Baseeapconnectionpropertiesv1](baseeapconnectionpropertiesv1schema-schema.md)架構中 [EapType](baseeapconnectionpropertiesv1schema-eaptype-element.md)元素的衍生型別。</span><span class="sxs-lookup"><span data-stu-id="b24a7-106">The **EapType** element is a derived type of the [EapType](baseeapconnectionpropertiesv1schema-eaptype-element.md) element from the [baseeapconnectionpropertiesv1](baseeapconnectionpropertiesv1schema-schema.md) schema.</span></span> <span data-ttu-id="b24a7-107">這是出現在 [EapHostConfig](eaphostconfigschema-elements.md) 架構之 Config 元素內的最上層元素。</span><span class="sxs-lookup"><span data-stu-id="b24a7-107">This is the top element that appears inside the Config element of the [EapHostConfig](eaphostconfigschema-elements.md) schema</span></span>

``` syntax
<xs:element name="EapType"
    substitutionGroup="EapType"
>
    <xs:complexType>
        <xs:complexContent>
            <xs:extension
                base="BaseEapTypeParameters"
            >
                <xs:sequence>
                    <xs:element name="UseWinLogonCredentials"
                        type="boolean"
                        default="true"
                        minOccurs="0"
                     />
                    <xs:any
                        processContents="lax"
                        minOccurs="0"
                        maxOccurs="unbounded"
                        namespace="##other"
                     />
                </xs:sequence>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="b24a7-108">子元素</span><span class="sxs-lookup"><span data-stu-id="b24a7-108">Child elements</span></span>



| <span data-ttu-id="b24a7-109">元素</span><span class="sxs-lookup"><span data-stu-id="b24a7-109">Element</span></span>                                                                                                       | <span data-ttu-id="b24a7-110">類型</span><span class="sxs-lookup"><span data-stu-id="b24a7-110">Type</span></span>    | <span data-ttu-id="b24a7-111">Description</span><span class="sxs-lookup"><span data-stu-id="b24a7-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b24a7-112">**UseWinLogonCredentials**</span><span class="sxs-lookup"><span data-stu-id="b24a7-112">**UseWinLogonCredentials**</span></span>](mschapv2connectionpropertiesv1schema-usewinlogoncredentials-eaptype-element.md) | <span data-ttu-id="b24a7-113">boolean</span><span class="sxs-lookup"><span data-stu-id="b24a7-113">boolean</span></span> | <span data-ttu-id="b24a7-114">控制 winlogin 認證的使用。</span><span class="sxs-lookup"><span data-stu-id="b24a7-114">Controls use of the winlogin credentials.</span></span> <span data-ttu-id="b24a7-115">若為 TRUE，則表示 EAP MS-CHAPv2 從 winlogon 取得認證。</span><span class="sxs-lookup"><span data-stu-id="b24a7-115">If TRUE, then EAP MS-CHAPv2 obtains credentials from winlogon.</span></span> <span data-ttu-id="b24a7-116">如果為 FALSE，則表示 EAP MS-CHAPv2 取得使用者的認證。</span><span class="sxs-lookup"><span data-stu-id="b24a7-116">If FALSE, then EAP MS-CHAPv2 obtains credentials from the user.</span></span> <br/> <span data-ttu-id="b24a7-117">[**UseWinLogonCredentials (EapType)**](mschapv2connectionpropertiesv1schema-usewinlogoncredentials-eaptype-element.md)元素是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="b24a7-117">The [**UseWinLogonCredentials (EapType)**](mschapv2connectionpropertiesv1schema-usewinlogoncredentials-eaptype-element.md) element is optional.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="b24a7-118">備註</span><span class="sxs-lookup"><span data-stu-id="b24a7-118">Remarks</span></span>

<span data-ttu-id="b24a7-119">**ProcessContents** 元素可讓架構的未來增強功能。</span><span class="sxs-lookup"><span data-stu-id="b24a7-119">The **processContents** element enables future enhancements to the schema.</span></span> <span data-ttu-id="b24a7-120">**ProcessContents** 元素是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="b24a7-120">The **processContents** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="b24a7-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="b24a7-121">Requirements</span></span>



| <span data-ttu-id="b24a7-122">需求</span><span class="sxs-lookup"><span data-stu-id="b24a7-122">Requirement</span></span> | <span data-ttu-id="b24a7-123">值</span><span class="sxs-lookup"><span data-stu-id="b24a7-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b24a7-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b24a7-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b24a7-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b24a7-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b24a7-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b24a7-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b24a7-127">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b24a7-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b24a7-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b24a7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b24a7-129">EAPHost 和舊版架構</span><span class="sxs-lookup"><span data-stu-id="b24a7-129">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="b24a7-130">mschapv2connectionpropertiesv1 架構</span><span class="sxs-lookup"><span data-stu-id="b24a7-130">mschapv2connectionpropertiesv1 Schema</span></span>](mschapv2connectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





