---
description: 指出將保留 PMK 快取的時間長度（以分鐘為單位）。
ms.assetid: d9e3b839-48f6-490c-ab83-067368cdcca2
title: PMKCacheTTL (安全性) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PMKCacheTTL
api_type:
- Schema
api_location: ''
ms.openlocfilehash: bdfe0edb163dc2bc9766ba8562defb026bbe21fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972020"
---
# <a name="pmkcachettl-security-element"></a><span data-ttu-id="bb260-103">PMKCacheTTL (安全性) 元素</span><span class="sxs-lookup"><span data-stu-id="bb260-103">PMKCacheTTL (security) Element</span></span>

<span data-ttu-id="bb260-104">PMKCacheTTL (security) 元素指出 PMK 快取將保留的時間長度（以分鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="bb260-104">The PMKCacheTTL (security) element indicates the length of time, in minutes, that a PMK cache will be kept.</span></span> <span data-ttu-id="bb260-105">只有在 [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) 設定為 "enabled" 的 WPA2 定義網路上，此元素才有效。</span><span class="sxs-lookup"><span data-stu-id="bb260-105">This element is valid only for WPA2-defined networks with [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) set to "enabled".</span></span>

<span data-ttu-id="bb260-106">PMK 快取會在 [802.11 i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) 規格中說明。</span><span class="sxs-lookup"><span data-stu-id="bb260-106">PMK caching is described in the [802.11i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) specification.</span></span>

<span data-ttu-id="bb260-107">Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 不支援這個元素。</span><span class="sxs-lookup"><span data-stu-id="bb260-107">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="PMKCacheTTL"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:minInclusive
                value="5"
             />
            <xs:maxInclusive
                value="1440"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="bb260-108">元素是由 [**安全性**](wlan-profileschema-security-msm-element.md) 元素所定義。</span><span class="sxs-lookup"><span data-stu-id="bb260-108">The element is defined by the [**security**](wlan-profileschema-security-msm-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb260-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="bb260-109">Requirements</span></span>



| <span data-ttu-id="bb260-110">需求</span><span class="sxs-lookup"><span data-stu-id="bb260-110">Requirement</span></span> | <span data-ttu-id="bb260-111">值</span><span class="sxs-lookup"><span data-stu-id="bb260-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="bb260-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bb260-112">Minimum supported client</span></span><br/> | <span data-ttu-id="bb260-113">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bb260-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="bb260-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bb260-114">Minimum supported server</span></span><br/> | <span data-ttu-id="bb260-115">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bb260-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bb260-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bb260-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="bb260-117">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="bb260-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="bb260-118">**安全**</span><span class="sxs-lookup"><span data-stu-id="bb260-118">**security**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> <dt>

<span data-ttu-id="bb260-119">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="bb260-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="bb260-120">**(MSM) 的安全性**</span><span class="sxs-lookup"><span data-stu-id="bb260-120">**security (MSM)**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 




