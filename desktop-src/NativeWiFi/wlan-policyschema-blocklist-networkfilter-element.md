---
description: 指定電腦不得連接的無線區域網路網路清單。
ms.assetid: 01db3f7e-1e27-4378-9c42-bc38192f9507
title: 封鎖清單 (networkFilter) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- blockList
api_type:
- Schema
api_location: ''
ms.openlocfilehash: e852286d00d93904bd185fef6c2f3444bb5987f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936587"
---
# <a name="blocklist-networkfilter-element"></a><span data-ttu-id="e3050-103">封鎖清單 (networkFilter) 元素</span><span class="sxs-lookup"><span data-stu-id="e3050-103">blockList (networkFilter) Element</span></span>

<span data-ttu-id="e3050-104">封鎖清單 (networkFilter) 元素會指定電腦不得連接的無線區域網路網路清單。</span><span class="sxs-lookup"><span data-stu-id="e3050-104">The blockList (networkFilter) element specifies the list of wireless LAN networks to which a machine must not connect.</span></span>

``` syntax
<xs:element name="blockList">
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

<span data-ttu-id="e3050-105">**封鎖清單** 元素是由 [**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md)元素定義。</span><span class="sxs-lookup"><span data-stu-id="e3050-105">The **blockList** element is defined by the [**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="e3050-106">子元素</span><span class="sxs-lookup"><span data-stu-id="e3050-106">Child elements</span></span>



| <span data-ttu-id="e3050-107">元素</span><span class="sxs-lookup"><span data-stu-id="e3050-107">Element</span></span>                                                        | <span data-ttu-id="e3050-108">類型</span><span class="sxs-lookup"><span data-stu-id="e3050-108">Type</span></span>                                                                     | <span data-ttu-id="e3050-109">Description</span><span class="sxs-lookup"><span data-stu-id="e3050-109">Description</span></span>                      |
|----------------------------------------------------------------|--------------------------------------------------------------------------|----------------------------------|
| [<span data-ttu-id="e3050-110">**network**</span><span class="sxs-lookup"><span data-stu-id="e3050-110">**network**</span></span>](wlan-policyschema-network-blocklist-element.md) | [<span data-ttu-id="e3050-111">**networkItemType**</span><span class="sxs-lookup"><span data-stu-id="e3050-111">**networkItemType**</span></span>](wlan-policyschema-networkitemtype-complextype.md) | <span data-ttu-id="e3050-112">封鎖的網路。</span><span class="sxs-lookup"><span data-stu-id="e3050-112">The blocked network.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="e3050-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="e3050-113">Requirements</span></span>



| <span data-ttu-id="e3050-114">需求</span><span class="sxs-lookup"><span data-stu-id="e3050-114">Requirement</span></span> | <span data-ttu-id="e3050-115">值</span><span class="sxs-lookup"><span data-stu-id="e3050-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e3050-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e3050-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e3050-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e3050-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e3050-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e3050-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e3050-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e3050-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e3050-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e3050-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="e3050-121">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="e3050-121">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="e3050-122">**networkFilter**</span><span class="sxs-lookup"><span data-stu-id="e3050-122">**networkFilter**</span></span>](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="e3050-123">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="e3050-123">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="e3050-124">**networkFilter (WLANPolicy)**</span><span class="sxs-lookup"><span data-stu-id="e3050-124">**networkFilter (WLANPolicy)**</span></span>](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> </dl>

 

 




