---
description: 包含獨立硬體廠商所使用的各種安全性設定。
ms.assetid: 237c5d98-3f3c-4279-b2ad-b0d05df041f9
title: 安全性 (IHV) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- security
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 6ace1bb0ca31f40fdc9d10fba13832797d8d4306
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106982470"
---
# <a name="security-ihv-element"></a><span data-ttu-id="a28d4-103">安全性 (IHV) 元素</span><span class="sxs-lookup"><span data-stu-id="a28d4-103">security (IHV) Element</span></span>

<span data-ttu-id="a28d4-104">安全性 (IHV) 元素包含獨立硬體廠商所使用的各種安全性設定。</span><span class="sxs-lookup"><span data-stu-id="a28d4-104">The security (IHV) element contains various security settings used by independent hardware vendors.</span></span>

<span data-ttu-id="a28d4-105">Microsoft 安全性設定和 IHV 安全性設定都是互斥的。</span><span class="sxs-lookup"><span data-stu-id="a28d4-105">Microsoft security settings and IHV security settings are mutually exclusive.</span></span> <span data-ttu-id="a28d4-106">如果相同的設定檔中有這兩組安全性設定，則設定檔無效。</span><span class="sxs-lookup"><span data-stu-id="a28d4-106">If both sets of security settings are present in the same profile, the profile is invalid.</span></span>

<span data-ttu-id="a28d4-107">Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 不支援這個元素。</span><span class="sxs-lookup"><span data-stu-id="a28d4-107">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="security">
    <xs:complexType>
        <xs:sequence>
            <xs:any
                processContents="lax"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="a28d4-108">**安全性** 元素是由 [**IHV**](wlan-profileschema-ihv-wlanprofile-element.md)元素所定義。</span><span class="sxs-lookup"><span data-stu-id="a28d4-108">The **security** element is defined by the [**IHV**](wlan-profileschema-ihv-wlanprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="a28d4-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="a28d4-109">Requirements</span></span>



| <span data-ttu-id="a28d4-110">需求</span><span class="sxs-lookup"><span data-stu-id="a28d4-110">Requirement</span></span> | <span data-ttu-id="a28d4-111">值</span><span class="sxs-lookup"><span data-stu-id="a28d4-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a28d4-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a28d4-112">Minimum supported client</span></span><br/> | <span data-ttu-id="a28d4-113">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a28d4-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a28d4-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a28d4-114">Minimum supported server</span></span><br/> | <span data-ttu-id="a28d4-115">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a28d4-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a28d4-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a28d4-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="a28d4-117">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="a28d4-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="a28d4-118">**IHV**</span><span class="sxs-lookup"><span data-stu-id="a28d4-118">**IHV**</span></span>](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="a28d4-119">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="a28d4-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="a28d4-120">**IHV (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="a28d4-120">**IHV (WLANProfile)**</span></span>](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> </dl>

 

 




