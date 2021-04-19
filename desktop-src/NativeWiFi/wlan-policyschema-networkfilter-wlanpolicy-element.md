---
description: 針對機器定義允許和拒絕的網路清單。
ms.assetid: 21502c97-36a4-4cd6-9dd0-ee44c4cc522f
title: networkFilter (WLANPolicy) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- networkFilter
api_type:
- Schema
api_location: ''
ms.openlocfilehash: d78a23ba1a456f1ad45745fcc25580c27de148c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985487"
---
# <a name="networkfilter-wlanpolicy-element"></a><span data-ttu-id="f3266-103">networkFilter (WLANPolicy) 元素</span><span class="sxs-lookup"><span data-stu-id="f3266-103">networkFilter (WLANPolicy) Element</span></span>

<span data-ttu-id="f3266-104">NetworkFilter (WLANPolicy) 元素會定義電腦允許和拒絕的網路清單。</span><span class="sxs-lookup"><span data-stu-id="f3266-104">The networkFilter (WLANPolicy) element defines the list of allowed and denied networks for machines.</span></span>

``` syntax
<xs:element name="networkFilter">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="allowList"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="network"
                            type="networkItemType"
                            maxOccurs="unbounded"
                         />
                        <xs:any
                            processContents="lax"
                            minOccurs="0"
                            maxOccurs="unbounded"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:element name="blockList"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="network"
                            type="networkItemType"
                            maxOccurs="unbounded"
                         />
                        <xs:any
                            processContents="lax"
                            minOccurs="0"
                            maxOccurs="unbounded"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:element name="denyAllIBSS"
                type="boolean"
                minOccurs="0"
             />
            <xs:element name="denyAllESS"
                type="boolean"
                minOccurs="0"
             />
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

<span data-ttu-id="f3266-105">**NetworkFilter** 元素是由 [**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md)元素定義。</span><span class="sxs-lookup"><span data-stu-id="f3266-105">The **networkFilter** element is defined by the [**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="f3266-106">子元素</span><span class="sxs-lookup"><span data-stu-id="f3266-106">Child elements</span></span>



| <span data-ttu-id="f3266-107">元素</span><span class="sxs-lookup"><span data-stu-id="f3266-107">Element</span></span>                                                                    | <span data-ttu-id="f3266-108">類型</span><span class="sxs-lookup"><span data-stu-id="f3266-108">Type</span></span>                                                                     | <span data-ttu-id="f3266-109">Description</span><span class="sxs-lookup"><span data-stu-id="f3266-109">Description</span></span>                                                                                    |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f3266-110">**允許清單**</span><span class="sxs-lookup"><span data-stu-id="f3266-110">**allowList**</span></span>](wlan-policyschema-allowlist-networkfilter-element.md)     |                                                                          | <span data-ttu-id="f3266-111">必須允許任何電腦連接的無線區域網路網路清單。</span><span class="sxs-lookup"><span data-stu-id="f3266-111">The list of wireless LAN networks to which any machine must be allowed to connect.</span></span> <br/> |
| [<span data-ttu-id="f3266-112">**封鎖清單**</span><span class="sxs-lookup"><span data-stu-id="f3266-112">**blockList**</span></span>](wlan-policyschema-blocklist-networkfilter-element.md)     |                                                                          | <span data-ttu-id="f3266-113">電腦不能連線的無線區域網路網路清單。</span><span class="sxs-lookup"><span data-stu-id="f3266-113">The list of wireless LAN networks to which a machine must not connect.</span></span><br/>              |
| [<span data-ttu-id="f3266-114">**denyAllESS**</span><span class="sxs-lookup"><span data-stu-id="f3266-114">**denyAllESS**</span></span>](wlan-policyschema-denyalless-networkfilter-element.md)   | <span data-ttu-id="f3266-115">boolean</span><span class="sxs-lookup"><span data-stu-id="f3266-115">boolean</span></span>                                                                  | <span data-ttu-id="f3266-116">指定是否封鎖對所有基礎結構網路的存取。</span><span class="sxs-lookup"><span data-stu-id="f3266-116">Specifies if access to all infrastructure networks is blocked.</span></span> <br/>                     |
| [<span data-ttu-id="f3266-117">**denyAllIBSS**</span><span class="sxs-lookup"><span data-stu-id="f3266-117">**denyAllIBSS**</span></span>](wlan-policyschema-denyallibss-networkfilter-element.md) | <span data-ttu-id="f3266-118">boolean</span><span class="sxs-lookup"><span data-stu-id="f3266-118">boolean</span></span>                                                                  | <span data-ttu-id="f3266-119">指定是否封鎖對所有特定網路的存取。</span><span class="sxs-lookup"><span data-stu-id="f3266-119">Specifies if access to all ad-hoc networks is blocked.</span></span> <br/>                             |
| [<span data-ttu-id="f3266-120">**network**</span><span class="sxs-lookup"><span data-stu-id="f3266-120">**network**</span></span>](wlan-policyschema-network-allowlist-element.md)             | [<span data-ttu-id="f3266-121">**networkItemType**</span><span class="sxs-lookup"><span data-stu-id="f3266-121">**networkItemType**</span></span>](wlan-policyschema-networkitemtype-complextype.md) | <span data-ttu-id="f3266-122">允許的網路。</span><span class="sxs-lookup"><span data-stu-id="f3266-122">An allowed network.</span></span> <br/>                                                                |
| [<span data-ttu-id="f3266-123">**network**</span><span class="sxs-lookup"><span data-stu-id="f3266-123">**network**</span></span>](wlan-policyschema-network-blocklist-element.md)             | [<span data-ttu-id="f3266-124">**networkItemType**</span><span class="sxs-lookup"><span data-stu-id="f3266-124">**networkItemType**</span></span>](wlan-policyschema-networkitemtype-complextype.md) | <span data-ttu-id="f3266-125">封鎖的網路。</span><span class="sxs-lookup"><span data-stu-id="f3266-125">A blocked network.</span></span> <br/>                                                                 |



## <a name="requirements"></a><span data-ttu-id="f3266-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="f3266-126">Requirements</span></span>



| <span data-ttu-id="f3266-127">需求</span><span class="sxs-lookup"><span data-stu-id="f3266-127">Requirement</span></span> | <span data-ttu-id="f3266-128">值</span><span class="sxs-lookup"><span data-stu-id="f3266-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f3266-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f3266-129">Minimum supported client</span></span><br/> | <span data-ttu-id="f3266-130">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f3266-130">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f3266-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f3266-131">Minimum supported server</span></span><br/> | <span data-ttu-id="f3266-132">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f3266-132">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f3266-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f3266-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="f3266-134">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="f3266-134">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="f3266-135">**WLANPolicy**</span><span class="sxs-lookup"><span data-stu-id="f3266-135">**WLANPolicy**</span></span>](wlan-policyschema-wlanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="f3266-136">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="f3266-136">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="f3266-137">**WLANPolicy**</span><span class="sxs-lookup"><span data-stu-id="f3266-137">**WLANPolicy**</span></span>](wlan-policyschema-wlanpolicy-element.md)
</dt> </dl>

 

 




