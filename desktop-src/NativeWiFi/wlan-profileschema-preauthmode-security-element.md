---
description: 指出用戶端是否會使用預先驗證。
ms.assetid: 305d77b6-fe2d-45c6-ac91-5769f91de152
title: preAuthMode (安全性) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- preAuthMode
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 6ac74f193fb89c260b1a121b673f239147658865
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973628"
---
# <a name="preauthmode-security-element"></a><span data-ttu-id="9cdb8-103">preAuthMode (安全性) 元素</span><span class="sxs-lookup"><span data-stu-id="9cdb8-103">preAuthMode (security) Element</span></span>

<span data-ttu-id="9cdb8-104">PreAuthMode (security) 元素會指出用戶端是否會使用預先驗證。</span><span class="sxs-lookup"><span data-stu-id="9cdb8-104">The preAuthMode (security) element indicates whether pre-authentication will be used by the client.</span></span> <span data-ttu-id="9cdb8-105">WPA2 安全快速漫遊需要預先驗證。</span><span class="sxs-lookup"><span data-stu-id="9cdb8-105">Pre-authentication is necessary for WPA2 secure fast roaming.</span></span> <span data-ttu-id="9cdb8-106">只有在 [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) 設定為 "enabled" 的 WPA2 定義網路上，此元素才有效。</span><span class="sxs-lookup"><span data-stu-id="9cdb8-106">This element is valid only for WPA2-defined networks with [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) set to "enabled".</span></span> <span data-ttu-id="9cdb8-107">如果 **PMKCacheMode** 已啟用，且此元素不存在，則預設值為「已停用」。</span><span class="sxs-lookup"><span data-stu-id="9cdb8-107">If **PMKCacheMode** is enabled, and this element is absent, the default value is "disabled".</span></span>

<span data-ttu-id="9cdb8-108">Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 不支援這個元素。</span><span class="sxs-lookup"><span data-stu-id="9cdb8-108">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="preAuthMode"
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

<span data-ttu-id="9cdb8-109">元素是由 [**安全性**](wlan-profileschema-security-msm-element.md) 元素所定義。</span><span class="sxs-lookup"><span data-stu-id="9cdb8-109">The element is defined by the [**security**](wlan-profileschema-security-msm-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="9cdb8-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="9cdb8-110">Requirements</span></span>



| <span data-ttu-id="9cdb8-111">需求</span><span class="sxs-lookup"><span data-stu-id="9cdb8-111">Requirement</span></span> | <span data-ttu-id="9cdb8-112">值</span><span class="sxs-lookup"><span data-stu-id="9cdb8-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9cdb8-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9cdb8-113">Minimum supported client</span></span><br/> | <span data-ttu-id="9cdb8-114">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9cdb8-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9cdb8-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9cdb8-115">Minimum supported server</span></span><br/> | <span data-ttu-id="9cdb8-116">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9cdb8-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9cdb8-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9cdb8-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="9cdb8-118">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="9cdb8-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="9cdb8-119">**安全**</span><span class="sxs-lookup"><span data-stu-id="9cdb8-119">**security**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> <dt>

<span data-ttu-id="9cdb8-120">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="9cdb8-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="9cdb8-121">**(MSM) 的安全性**</span><span class="sxs-lookup"><span data-stu-id="9cdb8-121">**security (MSM)**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 




