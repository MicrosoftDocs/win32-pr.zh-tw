---
description: 包含一或多個適用于無線區域網路的 Ssid。
ms.assetid: f9c46db8-2933-48e1-8cb3-effeb13c43ed
title: SSIDConfig (WLANProfile) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SSIDConfig
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 5665b385c3264ff9d36e79ad671c8f9e8377d4bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849623"
---
# <a name="ssidconfig-wlanprofile-element"></a><span data-ttu-id="76180-103">SSIDConfig (WLANProfile) 元素</span><span class="sxs-lookup"><span data-stu-id="76180-103">SSIDConfig (WLANProfile) Element</span></span>

<span data-ttu-id="76180-104">SSIDConfig (WLANProfile) 元素包含一個或多個適用于無線區域網路的 Ssid。</span><span class="sxs-lookup"><span data-stu-id="76180-104">The SSIDConfig (WLANProfile) element contains one or more SSIDs for wireless LANs.</span></span>

``` syntax
<xs:element name="SSIDConfig"
    maxOccurs="256"
>
    <xs:complexType>
        <xs:sequence>
            <xs:element name="SSID"
                maxOccurs="256"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="hex"
                            minOccurs="0"
                        >
                            <xs:simpleType>
                                <xs:restriction
                                    base="hexBinary"
                                >
                                    <xs:minLength
                                        value="1"
                                     />
                                    <xs:maxLength
                                        value="32"
                                     />
                                </xs:restriction>
                            </xs:simpleType>
                        </xs:element>
                        <xs:element name="name"
                            minOccurs="0"
                        >
                            <xs:simpleType>
                                <xs:restriction
                                    base="string"
                                >
                                    <xs:minLength
                                        value="1"
                                     />
                                    <xs:maxLength
                                        value="32"
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
            <xs:element name="nonBroadcast"
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

<span data-ttu-id="76180-105">**SSIDConfig** 元素是由 [**WLANProfile**](wlan-profileschema-wlanprofile-element.md)元素定義。</span><span class="sxs-lookup"><span data-stu-id="76180-105">The **SSIDConfig** element is defined by the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="76180-106">子元素</span><span class="sxs-lookup"><span data-stu-id="76180-106">Child elements</span></span>



| <span data-ttu-id="76180-107">元素</span><span class="sxs-lookup"><span data-stu-id="76180-107">Element</span></span>                                                                    | <span data-ttu-id="76180-108">類型</span><span class="sxs-lookup"><span data-stu-id="76180-108">Type</span></span>                                                              | <span data-ttu-id="76180-109">Description</span><span class="sxs-lookup"><span data-stu-id="76180-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------------------|-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="76180-110">**hex**</span><span class="sxs-lookup"><span data-stu-id="76180-110">**hex**</span></span>](wlan-profileschema-hex-ssid-element.md)                         |                                                                   | <span data-ttu-id="76180-111">包含十六進位格式的無線區域網路 SSID。</span><span class="sxs-lookup"><span data-stu-id="76180-111">Contains the SSID of a wireless LAN in hexadecimal format.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="76180-112">**名字**</span><span class="sxs-lookup"><span data-stu-id="76180-112">**name**</span></span>](wlan-profileschema-name-ssid-element.md)                       |                                                                   | <span data-ttu-id="76180-113">包含無線區域網路的 SSID (區分大小寫) 名稱。</span><span class="sxs-lookup"><span data-stu-id="76180-113">Contains the (case-sensitive) name of the SSID of a wireless LAN.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="76180-114">**廣播**</span><span class="sxs-lookup"><span data-stu-id="76180-114">**nonBroadcast**</span></span>](wlan-profileschema-nonbroadcast-ssidconfig-element.md) | [<span data-ttu-id="76180-115">boolean</span><span class="sxs-lookup"><span data-stu-id="76180-115">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="76180-116">指出網路是否會廣播其 SSID。</span><span class="sxs-lookup"><span data-stu-id="76180-116">Indicates whether the network broadcasts its SSID.</span></span><br/> <span data-ttu-id="76180-117">如果 [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) 設定為 ESS，此值可以是 **TRUE** 或 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="76180-117">If [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) is set to ESS, this value can be either **TRUE** or **FALSE**.</span></span> <span data-ttu-id="76180-118">如果這個元素不存在，則預設值為 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="76180-118">The default value is **TRUE** if this element is absent.</span></span><br/> <span data-ttu-id="76180-119">如果 [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) 設定為 IBSS，則這個值必須是 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="76180-119">If [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) is set to IBSS, this value must be **FALSE**.</span></span><br/> <span data-ttu-id="76180-120">Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 不支援這個元素。</span><span class="sxs-lookup"><span data-stu-id="76180-120">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/> |
| [<span data-ttu-id="76180-121">**Ssid**</span><span class="sxs-lookup"><span data-stu-id="76180-121">**SSID**</span></span>](wlan-profileschema-ssid-ssidconfig-element.md)                 |                                                                   | <span data-ttu-id="76180-122">包含無線區域網路的 SSID。</span><span class="sxs-lookup"><span data-stu-id="76180-122">Contains an SSID for a wireless LAN.</span></span><br/> <span data-ttu-id="76180-123">Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 設定檔中最多隻能出現一個 [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md)元素。</span><span class="sxs-lookup"><span data-stu-id="76180-123">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** At most one [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element can appear in a profile.</span></span><br/>                                                                                                                                                                                                                                                                                                        |



## <a name="examples"></a><span data-ttu-id="76180-124">範例</span><span class="sxs-lookup"><span data-stu-id="76180-124">Examples</span></span>

<span data-ttu-id="76180-125">若要查看使用 **SSIDConfig** 元素的範例設定檔，請參閱 [無線設定檔範例](wireless-profile-samples.md)。</span><span class="sxs-lookup"><span data-stu-id="76180-125">To view sample profiles that use the **SSIDConfig** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="76180-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="76180-126">Requirements</span></span>



| <span data-ttu-id="76180-127">需求</span><span class="sxs-lookup"><span data-stu-id="76180-127">Requirement</span></span> | <span data-ttu-id="76180-128">值</span><span class="sxs-lookup"><span data-stu-id="76180-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="76180-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="76180-129">Minimum supported client</span></span><br/> | <span data-ttu-id="76180-130">Windows Vista、Windows XP （僅含 SP3） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="76180-130">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="76180-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="76180-131">Minimum supported server</span></span><br/> | <span data-ttu-id="76180-132">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="76180-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="76180-133">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="76180-133">Redistributable</span></span><br/>          | <span data-ttu-id="76180-134">適用于 Windows XP SP2 的無線區域網路 API</span><span class="sxs-lookup"><span data-stu-id="76180-134">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="76180-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="76180-135">See also</span></span>

<dl> <dt>

<span data-ttu-id="76180-136">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="76180-136">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="76180-137">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="76180-137">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="76180-138">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="76180-138">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="76180-139">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="76180-139">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 
