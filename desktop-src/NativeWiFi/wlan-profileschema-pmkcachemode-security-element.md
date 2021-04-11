---
description: 指出是否會使用 PMK 快取。
ms.assetid: 5650c893-6047-4e99-a2be-22722d6a809a
title: PMKCacheMode (安全性) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PMKCacheMode
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 609660d6f3161cbaaa5e0505daf9c6b9180b6c32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112732"
---
# <a name="pmkcachemode-security-element"></a><span data-ttu-id="58f0d-103">PMKCacheMode (安全性) 元素</span><span class="sxs-lookup"><span data-stu-id="58f0d-103">PMKCacheMode (security) Element</span></span>

<span data-ttu-id="58f0d-104">PMKCacheMode (security) 元素指出是否會使用 PMK 快取。</span><span class="sxs-lookup"><span data-stu-id="58f0d-104">The PMKCacheMode (security) element indicates whether PMK caching will be used.</span></span> <span data-ttu-id="58f0d-105">此元素只對 WPA2 定義的網路有效。</span><span class="sxs-lookup"><span data-stu-id="58f0d-105">This element is valid only for WPA2-defined networks.</span></span> <span data-ttu-id="58f0d-106">PMK 快取會在 [802.11 i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) 規格中說明。</span><span class="sxs-lookup"><span data-stu-id="58f0d-106">PMK caching is described in the [802.11i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) specification.</span></span>

<span data-ttu-id="58f0d-107">Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 不支援這個元素。</span><span class="sxs-lookup"><span data-stu-id="58f0d-107">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="PMKCacheMode"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="disabled"
             />
            <xs:enumeration
                value="enabled"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="58f0d-108">元素是由 [**安全性**](wlan-profileschema-security-msm-element.md) 元素所定義。</span><span class="sxs-lookup"><span data-stu-id="58f0d-108">The element is defined by the [**security**](wlan-profileschema-security-msm-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="58f0d-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="58f0d-109">Requirements</span></span>



| <span data-ttu-id="58f0d-110">需求</span><span class="sxs-lookup"><span data-stu-id="58f0d-110">Requirement</span></span> | <span data-ttu-id="58f0d-111">值</span><span class="sxs-lookup"><span data-stu-id="58f0d-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="58f0d-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="58f0d-112">Minimum supported client</span></span><br/> | <span data-ttu-id="58f0d-113">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="58f0d-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="58f0d-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="58f0d-114">Minimum supported server</span></span><br/> | <span data-ttu-id="58f0d-115">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="58f0d-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="58f0d-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="58f0d-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="58f0d-117">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="58f0d-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="58f0d-118">**安全**</span><span class="sxs-lookup"><span data-stu-id="58f0d-118">**security**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> <dt>

<span data-ttu-id="58f0d-119">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="58f0d-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="58f0d-120">**(MSM) 的安全性**</span><span class="sxs-lookup"><span data-stu-id="58f0d-120">**security (MSM)**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 




