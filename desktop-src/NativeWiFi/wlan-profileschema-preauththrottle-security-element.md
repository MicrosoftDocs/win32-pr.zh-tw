---
description: 指定嘗試對相鄰 Ap 進行嘗試的預先驗證次數。
ms.assetid: 7e89e962-7544-4efb-9e3c-c108bee22aea
title: preAuthThrottle (安全性) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- preAuthThrottle
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 499401affb264238a065c0861f1230f23936206e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511180"
---
# <a name="preauththrottle-security-element"></a><span data-ttu-id="19860-103">preAuthThrottle (安全性) 元素</span><span class="sxs-lookup"><span data-stu-id="19860-103">preAuthThrottle (security) Element</span></span>

<span data-ttu-id="19860-104">PreAuthThrottle (security) 元素會指定嘗試在鄰近 Ap 上嘗試的預先驗證次數。</span><span class="sxs-lookup"><span data-stu-id="19860-104">The preAuthThrottle (security) element specifies the number pre-authentication attempts to try on neighboring APs.</span></span> <span data-ttu-id="19860-105">只有在 [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) 設定為 "enabled" 的 WPA2 定義網路上，此元素才有效。</span><span class="sxs-lookup"><span data-stu-id="19860-105">This element is valid only for WPA2-defined networks with [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) set to "enabled".</span></span> <span data-ttu-id="19860-106">如果 **PMKCacheMode** 已啟用，且此元素不存在，則嘗試次數會預設為3。</span><span class="sxs-lookup"><span data-stu-id="19860-106">If **PMKCacheMode** is enabled, and this element is absent, the number of tries defaults to 3.</span></span>

<span data-ttu-id="19860-107">Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 不支援這個元素。</span><span class="sxs-lookup"><span data-stu-id="19860-107">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="preAuthThrottle"
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
                value="16"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="19860-108">元素是由 [**安全性**](wlan-profileschema-security-msm-element.md) 元素所定義。</span><span class="sxs-lookup"><span data-stu-id="19860-108">The element is defined by the [**security**](wlan-profileschema-security-msm-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="19860-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="19860-109">Requirements</span></span>



| <span data-ttu-id="19860-110">需求</span><span class="sxs-lookup"><span data-stu-id="19860-110">Requirement</span></span> | <span data-ttu-id="19860-111">值</span><span class="sxs-lookup"><span data-stu-id="19860-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="19860-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="19860-112">Minimum supported client</span></span><br/> | <span data-ttu-id="19860-113">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="19860-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="19860-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="19860-114">Minimum supported server</span></span><br/> | <span data-ttu-id="19860-115">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="19860-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="19860-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="19860-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="19860-117">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="19860-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="19860-118">**安全**</span><span class="sxs-lookup"><span data-stu-id="19860-118">**security**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> <dt>

<span data-ttu-id="19860-119">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="19860-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="19860-120">**(MSM) 的安全性**</span><span class="sxs-lookup"><span data-stu-id="19860-120">**security (MSM)**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 




