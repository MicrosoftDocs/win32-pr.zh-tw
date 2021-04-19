---
description: 指定用戶端上 PMK 快取中的專案數。
ms.assetid: 3a53f7fd-7f12-43d3-94e6-a11bec389a34
title: PMKCacheSize (安全性) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PMKCacheSize
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 1b21054ddc97c51212ea3a06207617ad85228270
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971376"
---
# <a name="pmkcachesize-security-element"></a><span data-ttu-id="9e2ab-103">PMKCacheSize (安全性) 元素</span><span class="sxs-lookup"><span data-stu-id="9e2ab-103">PMKCacheSize (security) Element</span></span>

<span data-ttu-id="9e2ab-104">PMKCacheSize (security) 元素會指定用戶端上 PMK 快取中的專案數。</span><span class="sxs-lookup"><span data-stu-id="9e2ab-104">The PMKCacheSize (security) element specifies the number of entries in the PMK cache on the client.</span></span> <span data-ttu-id="9e2ab-105">只有在 [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) 設定為 "enabled" 的 WPA2 定義網路上，此元素才有效。</span><span class="sxs-lookup"><span data-stu-id="9e2ab-105">This element is valid only for WPA2-defined networks with [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) set to "enabled".</span></span> <span data-ttu-id="9e2ab-106">如果 **PMKCacheMode** 已啟用，且此元素不存在，則快取的大小會預設為128個專案。</span><span class="sxs-lookup"><span data-stu-id="9e2ab-106">If **PMKCacheMode** is enabled, and this element is absent, the size of the cache defaults to 128 entries.</span></span>

<span data-ttu-id="9e2ab-107">PMK 快取會在 [802.11 i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) 規格中說明。</span><span class="sxs-lookup"><span data-stu-id="9e2ab-107">PMK caching is described in the [802.11i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) specification.</span></span>

<span data-ttu-id="9e2ab-108">Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 不支援這個元素。</span><span class="sxs-lookup"><span data-stu-id="9e2ab-108">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="PMKCacheSize"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:minInclusive
                value="1"
             />
            <xs:maxInclusive
                value="255"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="9e2ab-109">元素是由 [**安全性**](wlan-profileschema-security-msm-element.md) 元素所定義。</span><span class="sxs-lookup"><span data-stu-id="9e2ab-109">The element is defined by the [**security**](wlan-profileschema-security-msm-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e2ab-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="9e2ab-110">Requirements</span></span>



| <span data-ttu-id="9e2ab-111">需求</span><span class="sxs-lookup"><span data-stu-id="9e2ab-111">Requirement</span></span> | <span data-ttu-id="9e2ab-112">值</span><span class="sxs-lookup"><span data-stu-id="9e2ab-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9e2ab-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9e2ab-113">Minimum supported client</span></span><br/> | <span data-ttu-id="9e2ab-114">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9e2ab-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9e2ab-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9e2ab-115">Minimum supported server</span></span><br/> | <span data-ttu-id="9e2ab-116">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9e2ab-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9e2ab-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9e2ab-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="9e2ab-118">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="9e2ab-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="9e2ab-119">**安全**</span><span class="sxs-lookup"><span data-stu-id="9e2ab-119">**security**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> <dt>

<span data-ttu-id="9e2ab-120">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="9e2ab-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="9e2ab-121">**(MSM) 的安全性**</span><span class="sxs-lookup"><span data-stu-id="9e2ab-121">**security (MSM)**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 




