---
description: 識別 IHV。
ms.assetid: a99c231c-afd7-44e6-81af-3d49ffef8714
title: OUIHeader (IHV) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OUIHeader
api_type:
- Schema
api_location: ''
ms.openlocfilehash: a31feb123e31489c751b7844e06d5c344278778e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986329"
---
# <a name="ouiheader-ihv-element"></a><span data-ttu-id="111dd-103">OUIHeader (IHV) 元素</span><span class="sxs-lookup"><span data-stu-id="111dd-103">OUIHeader (IHV) Element</span></span>

<span data-ttu-id="111dd-104">OUIHeader (IHV) 元素會識別 IHV。</span><span class="sxs-lookup"><span data-stu-id="111dd-104">The OUIHeader (IHV) element identifies the IHV.</span></span>

<span data-ttu-id="111dd-105">Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 不支援這個元素。</span><span class="sxs-lookup"><span data-stu-id="111dd-105">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="OUIHeader">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="OUI">
                <xs:simpleType>
                    <xs:restriction
                        base="hexBinary"
                    >
                        <xs:length
                            value="3"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="type">
                <xs:simpleType>
                    <xs:restriction
                        base="hexBinary"
                    >
                        <xs:length
                            value="1"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
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

<span data-ttu-id="111dd-106">元素是由 [**IHV**](wlan-profileschema-ihv-wlanprofile-element.md) 元素定義。</span><span class="sxs-lookup"><span data-stu-id="111dd-106">The element is defined by the [**IHV**](wlan-profileschema-ihv-wlanprofile-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="111dd-107">子元素</span><span class="sxs-lookup"><span data-stu-id="111dd-107">Child elements</span></span>



| <span data-ttu-id="111dd-108">元素</span><span class="sxs-lookup"><span data-stu-id="111dd-108">Element</span></span>                                                   | <span data-ttu-id="111dd-109">類型</span><span class="sxs-lookup"><span data-stu-id="111dd-109">Type</span></span> | <span data-ttu-id="111dd-110">Description</span><span class="sxs-lookup"><span data-stu-id="111dd-110">Description</span></span>                                                                                |
|-----------------------------------------------------------|------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="111dd-111">**OUI**</span><span class="sxs-lookup"><span data-stu-id="111dd-111">**OUI**</span></span>](wlan-profileschema-oui-ouiheader-element.md)   |      | <span data-ttu-id="111dd-112">包含用來識別 IHV 的3個位元組 hexBinary。</span><span class="sxs-lookup"><span data-stu-id="111dd-112">Contains a 3 byte hexBinary that identifies the IHV.</span></span><br/>                            |
| [<span data-ttu-id="111dd-113">**類型**</span><span class="sxs-lookup"><span data-stu-id="111dd-113">**type**</span></span>](wlan-profileschema-type-ouiheader-element.md) |      | <span data-ttu-id="111dd-114">包含1個位元組的 hexBinary，用來區分 Nic 的相同 IHV。</span><span class="sxs-lookup"><span data-stu-id="111dd-114">Contains a 1 byte hexBinary that is used to differentiate NICs by the same IHV.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="111dd-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="111dd-115">Requirements</span></span>



| <span data-ttu-id="111dd-116">需求</span><span class="sxs-lookup"><span data-stu-id="111dd-116">Requirement</span></span> | <span data-ttu-id="111dd-117">值</span><span class="sxs-lookup"><span data-stu-id="111dd-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="111dd-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="111dd-118">Minimum supported client</span></span><br/> | <span data-ttu-id="111dd-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="111dd-119">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="111dd-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="111dd-120">Minimum supported server</span></span><br/> | <span data-ttu-id="111dd-121">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="111dd-121">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="111dd-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="111dd-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="111dd-123">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="111dd-123">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="111dd-124">**IHV**</span><span class="sxs-lookup"><span data-stu-id="111dd-124">**IHV**</span></span>](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="111dd-125">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="111dd-125">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="111dd-126">**IHV (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="111dd-126">**IHV (WLANProfile)**</span></span>](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> </dl>

 

 




