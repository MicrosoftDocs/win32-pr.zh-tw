---
description: 指定必須允許任何電腦連接的無線區域網路網路清單。
ms.assetid: e24557d8-dedf-4381-bba0-cdb7ea26083b
title: 允許清單 (networkFilter) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- allowList
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 5488f962a1ba526b34ca2d10144a150d7c1417d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971340"
---
# <a name="allowlist-networkfilter-element"></a><span data-ttu-id="417a0-103">允許清單 (networkFilter) 元素</span><span class="sxs-lookup"><span data-stu-id="417a0-103">allowList (networkFilter) Element</span></span>

<span data-ttu-id="417a0-104">允許清單 (networkFilter) 元素會指定必須允許任何電腦連接的無線區域網路網路清單。</span><span class="sxs-lookup"><span data-stu-id="417a0-104">The allowList (networkFilter) element specifies the list of wireless LAN networks to which any machine must be allowed to connect.</span></span>

``` syntax
<xs:element name="allowList">
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
```

<span data-ttu-id="417a0-105">**允許清單** 元素是由 [**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md)元素定義。</span><span class="sxs-lookup"><span data-stu-id="417a0-105">The **allowList** element is defined by the [**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="417a0-106">子元素</span><span class="sxs-lookup"><span data-stu-id="417a0-106">Child elements</span></span>



| <span data-ttu-id="417a0-107">元素</span><span class="sxs-lookup"><span data-stu-id="417a0-107">Element</span></span>                                                        | <span data-ttu-id="417a0-108">類型</span><span class="sxs-lookup"><span data-stu-id="417a0-108">Type</span></span>                                                                     | <span data-ttu-id="417a0-109">Description</span><span class="sxs-lookup"><span data-stu-id="417a0-109">Description</span></span>                                              |
|----------------------------------------------------------------|--------------------------------------------------------------------------|----------------------------------------------------------|
| [<span data-ttu-id="417a0-110">**network**</span><span class="sxs-lookup"><span data-stu-id="417a0-110">**network**</span></span>](wlan-policyschema-network-allowlist-element.md) | [<span data-ttu-id="417a0-111">**networkItemType**</span><span class="sxs-lookup"><span data-stu-id="417a0-111">**networkItemType**</span></span>](wlan-policyschema-networkitemtype-complextype.md) | <span data-ttu-id="417a0-112">電腦可以連接的網路。</span><span class="sxs-lookup"><span data-stu-id="417a0-112">The network to which the machine can connect.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="417a0-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="417a0-113">Requirements</span></span>



| <span data-ttu-id="417a0-114">需求</span><span class="sxs-lookup"><span data-stu-id="417a0-114">Requirement</span></span> | <span data-ttu-id="417a0-115">值</span><span class="sxs-lookup"><span data-stu-id="417a0-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="417a0-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="417a0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="417a0-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="417a0-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="417a0-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="417a0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="417a0-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="417a0-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="417a0-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="417a0-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="417a0-121">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="417a0-121">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="417a0-122">**networkFilter**</span><span class="sxs-lookup"><span data-stu-id="417a0-122">**networkFilter**</span></span>](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="417a0-123">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="417a0-123">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="417a0-124">**networkFilter (WLANPolicy)**</span><span class="sxs-lookup"><span data-stu-id="417a0-124">**networkFilter (WLANPolicy)**</span></span>](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> </dl>

 

 




