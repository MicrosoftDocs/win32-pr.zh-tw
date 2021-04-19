---
description: 包含獨立硬體廠商的各種設定。
ms.assetid: 4ad8c991-7849-41d6-9852-1ecadc372a2d
title: IHV (WLANProfile) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IHV
api_type:
- Schema
api_location: ''
ms.openlocfilehash: d2d2902522c84ebe2939d42301a491521ac8a70f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974972"
---
# <a name="ihv-wlanprofile-element"></a><span data-ttu-id="fcc24-103">IHV (WLANProfile) 元素</span><span class="sxs-lookup"><span data-stu-id="fcc24-103">IHV (WLANProfile) Element</span></span>

<span data-ttu-id="fcc24-104">IHV (WLANProfile) 元素包含獨立硬體廠商的各種設定。</span><span class="sxs-lookup"><span data-stu-id="fcc24-104">The IHV (WLANProfile) element contains various settings for independent hardware vendors.</span></span> <span data-ttu-id="fcc24-105">如果設定檔包含 IHV 安全性設定，則會覆寫任何 Microsoft 定義的安全性。</span><span class="sxs-lookup"><span data-stu-id="fcc24-105">If a profile includes IHV security settings, they override any Microsoft-defined security.</span></span>

<span data-ttu-id="fcc24-106">Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 不支援這個元素。</span><span class="sxs-lookup"><span data-stu-id="fcc24-106">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="IHV"
    minOccurs="0"
>
    <xs:complexType>
        <xs:sequence>
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
            <xs:element name="connectivity"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:any
                            processContents="lax"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:element name="security"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:any
                            processContents="lax"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:element name="useMSOneX"
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

<span data-ttu-id="fcc24-107">元素是由 [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) 元素所定義。</span><span class="sxs-lookup"><span data-stu-id="fcc24-107">The element is defined by the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="fcc24-108">子元素</span><span class="sxs-lookup"><span data-stu-id="fcc24-108">Child elements</span></span>



| <span data-ttu-id="fcc24-109">元素</span><span class="sxs-lookup"><span data-stu-id="fcc24-109">Element</span></span>                                                             | <span data-ttu-id="fcc24-110">類型</span><span class="sxs-lookup"><span data-stu-id="fcc24-110">Type</span></span>                                                              | <span data-ttu-id="fcc24-111">Description</span><span class="sxs-lookup"><span data-stu-id="fcc24-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fcc24-112">**連接**</span><span class="sxs-lookup"><span data-stu-id="fcc24-112">**connectivity**</span></span>](wlan-profileschema-connectivity-ihv-element.md) |                                                                   | <span data-ttu-id="fcc24-113">包含與 IHV 相關的連線能力設定。</span><span class="sxs-lookup"><span data-stu-id="fcc24-113">Contains IHV-related connectivity settings.</span></span><br/>                                                                                                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="fcc24-114">**OUI**</span><span class="sxs-lookup"><span data-stu-id="fcc24-114">**OUI**</span></span>](wlan-profileschema-oui-ouiheader-element.md)             |                                                                   | <span data-ttu-id="fcc24-115">包含用來識別 IHV 的3個位元組 hexBinary。</span><span class="sxs-lookup"><span data-stu-id="fcc24-115">Contains a 3 byte hexBinary that identifies the IHV.</span></span><br/>                                                                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="fcc24-116">**OUIHeader**</span><span class="sxs-lookup"><span data-stu-id="fcc24-116">**OUIHeader**</span></span>](wlan-profileschema-ouiheader-ihv-element.md)       |                                                                   | <span data-ttu-id="fcc24-117">識別 IHV。</span><span class="sxs-lookup"><span data-stu-id="fcc24-117">Identifies the IHV.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="fcc24-118">**安全**</span><span class="sxs-lookup"><span data-stu-id="fcc24-118">**security**</span></span>](wlan-profileschema-security-ihv-element.md)         |                                                                   | <span data-ttu-id="fcc24-119">包含 IHV 特定的安全性設定。</span><span class="sxs-lookup"><span data-stu-id="fcc24-119">Contains IHV-specific security settings.</span></span> <span data-ttu-id="fcc24-120">Microsoft 安全性設定和 IHV 安全性設定都是互斥的。</span><span class="sxs-lookup"><span data-stu-id="fcc24-120">Microsoft security settings and IHV security settings are mutually exclusive.</span></span> <span data-ttu-id="fcc24-121">如果這兩個安全性設定都存在，則整個設定檔無效。</span><span class="sxs-lookup"><span data-stu-id="fcc24-121">The entire profile is invalid if both security settings are present.</span></span><br/>                                                                                                                                                                                            |
| [<span data-ttu-id="fcc24-122">**類型**</span><span class="sxs-lookup"><span data-stu-id="fcc24-122">**type**</span></span>](wlan-profileschema-type-ouiheader-element.md)           |                                                                   | <span data-ttu-id="fcc24-123">包含1個位元組的 hexBinary，用來區分 Nic 的相同 IHV。</span><span class="sxs-lookup"><span data-stu-id="fcc24-123">Contains a 1 byte hexBinary that is used to differentiate NICs by the same IHV.</span></span><br/>                                                                                                                                                                                                                                                                                                        |
| [<span data-ttu-id="fcc24-124">**useMSOneX**</span><span class="sxs-lookup"><span data-stu-id="fcc24-124">**useMSOneX**</span></span>](wlan-profileschema-usemsonex-ihv-element.md)       | [<span data-ttu-id="fcc24-125">boolean</span><span class="sxs-lookup"><span data-stu-id="fcc24-125">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="fcc24-126">指定 IHV 安全性元件所使用之 802.1 X 安全性設定的來源。</span><span class="sxs-lookup"><span data-stu-id="fcc24-126">Specifies the origin of 802.1X security settings used by an IHV security component.</span></span> <span data-ttu-id="fcc24-127">當 [**useMSOneX**](wlan-profileschema-usemsonex-ihv-element.md) 為 true 時，IHV 安全性元件會使用 Microsoft 定義的 802.1 x 設定。</span><span class="sxs-lookup"><span data-stu-id="fcc24-127">When [**useMSOneX**](wlan-profileschema-usemsonex-ihv-element.md) is true, IHV security components use Microsoft-defined 802.1X settings.</span></span> <span data-ttu-id="fcc24-128">當 **useMSOneX** 為 false 時，IHV 安全性元件會使用廠商提供的 802.1 x 設定。</span><span class="sxs-lookup"><span data-stu-id="fcc24-128">When **useMSOneX** is false, IHV security components use vendor-supplied 802.1X settings.</span></span> <span data-ttu-id="fcc24-129">依預設， **useMSOneX** 為 false。</span><span class="sxs-lookup"><span data-stu-id="fcc24-129">By default, **useMSOneX** is false.</span></span> <span data-ttu-id="fcc24-130">這是選擇性的項目。</span><span class="sxs-lookup"><span data-stu-id="fcc24-130">This element is optional.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="fcc24-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="fcc24-131">Requirements</span></span>



| <span data-ttu-id="fcc24-132">需求</span><span class="sxs-lookup"><span data-stu-id="fcc24-132">Requirement</span></span> | <span data-ttu-id="fcc24-133">值</span><span class="sxs-lookup"><span data-stu-id="fcc24-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fcc24-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fcc24-134">Minimum supported client</span></span><br/> | <span data-ttu-id="fcc24-135">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fcc24-135">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="fcc24-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fcc24-136">Minimum supported server</span></span><br/> | <span data-ttu-id="fcc24-137">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fcc24-137">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fcc24-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fcc24-138">See also</span></span>

<dl> <dt>

<span data-ttu-id="fcc24-139">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="fcc24-139">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="fcc24-140">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="fcc24-140">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="fcc24-141">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="fcc24-141">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="fcc24-142">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="fcc24-142">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 
