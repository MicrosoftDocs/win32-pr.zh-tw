---
description: 指定要用來連接到無線區域網路的驗證方法。
ms.assetid: fb6c5cce-05d6-41a2-acf4-9ae2713079dd
title: 驗證 (authEncryption) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- authentication
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 02895da685c78484c907af51745264abb81086da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191739"
---
# <a name="authentication-authencryption-element"></a><span data-ttu-id="b69ea-103">驗證 (authEncryption) 元素</span><span class="sxs-lookup"><span data-stu-id="b69ea-103">authentication (authEncryption) Element</span></span>

<span data-ttu-id="b69ea-104">Authentication (authEncryption) 元素會指定要用來連線到無線區域網路的驗證方法。</span><span class="sxs-lookup"><span data-stu-id="b69ea-104">The authentication (authEncryption) element specifies the authentication method to be used to connect to the wireless LAN.</span></span>

``` syntax
<xs:element name="authentication">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="open"
             />
            <xs:enumeration
                value="shared"
             />
            <xs:enumeration
                value="WPA"
             />
            <xs:enumeration
                value="WPAPSK"
             />
            <xs:enumeration
                value="WPA2"
             />
            <xs:enumeration
                value="WPA2PSK"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="b69ea-105">元素是由 [**authEncryption**](wlan-profileschema-authencryption-security-element.md) 元素所定義。</span><span class="sxs-lookup"><span data-stu-id="b69ea-105">The element is defined by the [**authEncryption**](wlan-profileschema-authencryption-security-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="b69ea-106">備註</span><span class="sxs-lookup"><span data-stu-id="b69ea-106">Remarks</span></span>

<span data-ttu-id="b69ea-107">下表描述列舉值。</span><span class="sxs-lookup"><span data-stu-id="b69ea-107">The following table describes the enumeration values.</span></span>



| <span data-ttu-id="b69ea-108">值</span><span class="sxs-lookup"><span data-stu-id="b69ea-108">Value</span></span>   | <span data-ttu-id="b69ea-109">描述</span><span class="sxs-lookup"><span data-stu-id="b69ea-109">Description</span></span>                            |
|---------|----------------------------------------|
| <span data-ttu-id="b69ea-110">開啟</span><span class="sxs-lookup"><span data-stu-id="b69ea-110">open</span></span>    | <span data-ttu-id="b69ea-111">開啟802.11 驗證。</span><span class="sxs-lookup"><span data-stu-id="b69ea-111">Open 802.11 authentication.</span></span>            |
| <span data-ttu-id="b69ea-112">共用</span><span class="sxs-lookup"><span data-stu-id="b69ea-112">shared</span></span>  | <span data-ttu-id="b69ea-113">共用的802.11 驗證。</span><span class="sxs-lookup"><span data-stu-id="b69ea-113">Shared 802.11 authentication.</span></span>          |
| <span data-ttu-id="b69ea-114">WPA</span><span class="sxs-lookup"><span data-stu-id="b69ea-114">WPA</span></span>     | <span data-ttu-id="b69ea-115">WPA-Enterprise 802.11 驗證。</span><span class="sxs-lookup"><span data-stu-id="b69ea-115">WPA-Enterprise 802.11 authentication.</span></span>  |
| <span data-ttu-id="b69ea-116">WPAPSK</span><span class="sxs-lookup"><span data-stu-id="b69ea-116">WPAPSK</span></span>  | <span data-ttu-id="b69ea-117">WPA-Personal 802.11 驗證。</span><span class="sxs-lookup"><span data-stu-id="b69ea-117">WPA-Personal 802.11 authentication.</span></span>    |
| <span data-ttu-id="b69ea-118">WPA2</span><span class="sxs-lookup"><span data-stu-id="b69ea-118">WPA2</span></span>    | <span data-ttu-id="b69ea-119">WPA2-Enterprise 802.11 驗證。</span><span class="sxs-lookup"><span data-stu-id="b69ea-119">WPA2-Enterprise 802.11 authentication.</span></span> |
| <span data-ttu-id="b69ea-120">WPA2PSK</span><span class="sxs-lookup"><span data-stu-id="b69ea-120">WPA2PSK</span></span> | <span data-ttu-id="b69ea-121">WPA2-Personal 802.11 驗證。</span><span class="sxs-lookup"><span data-stu-id="b69ea-121">WPA2-Personal 802.11 authentication.</span></span>   |



 

<span data-ttu-id="b69ea-122">如需802.11 驗證方法的詳細資訊，請參閱 [WPA](https://en.wikipedia.org/wiki/Wi-Fi_Protected_Access)、 [802.1 x](https://ieeexplore.ieee.org/document/1438730)和 [802.11 i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) 規格。</span><span class="sxs-lookup"><span data-stu-id="b69ea-122">For more information about 802.11 authentication methods, see the [WPA](https://en.wikipedia.org/wiki/Wi-Fi_Protected_Access), [802.1X](https://ieeexplore.ieee.org/document/1438730), and [802.11i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) specifications.</span></span>

## <a name="examples"></a><span data-ttu-id="b69ea-123">範例</span><span class="sxs-lookup"><span data-stu-id="b69ea-123">Examples</span></span>

<span data-ttu-id="b69ea-124">若要查看使用 **驗證** 元素的範例設定檔，請參閱 [無線設定檔範例](wireless-profile-samples.md)。</span><span class="sxs-lookup"><span data-stu-id="b69ea-124">To view sample profiles that use the **authentication** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b69ea-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="b69ea-125">Requirements</span></span>



| <span data-ttu-id="b69ea-126">需求</span><span class="sxs-lookup"><span data-stu-id="b69ea-126">Requirement</span></span> | <span data-ttu-id="b69ea-127">值</span><span class="sxs-lookup"><span data-stu-id="b69ea-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="b69ea-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b69ea-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b69ea-129">Windows Vista、Windows XP （僅含 SP3） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b69ea-129">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b69ea-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b69ea-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b69ea-131">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b69ea-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="b69ea-132">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="b69ea-132">Redistributable</span></span><br/>          | <span data-ttu-id="b69ea-133">適用于 Windows XP SP2 的無線區域網路 API</span><span class="sxs-lookup"><span data-stu-id="b69ea-133">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="b69ea-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b69ea-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="b69ea-135">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="b69ea-135">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="b69ea-136">**authEncryption**</span><span class="sxs-lookup"><span data-stu-id="b69ea-136">**authEncryption**</span></span>](wlan-profileschema-authencryption-security-element.md)
</dt> <dt>

<span data-ttu-id="b69ea-137">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="b69ea-137">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="b69ea-138">**authEncryption (安全性)**</span><span class="sxs-lookup"><span data-stu-id="b69ea-138">**authEncryption (security)**</span></span>](wlan-profileschema-authencryption-security-element.md)
</dt> </dl>

 

 




