---
description: 包含與 IHV 相關的連線能力設定。 目前未執行。
ms.assetid: d943e82a-8660-4df7-8f5c-42ed83f17313
title: " (IHV) 元素的連線能力"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- connectivity
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 257addbcbd721e5930405e3954dcb348f367af93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691552"
---
# <a name="connectivity-ihv-element"></a><span data-ttu-id="af5f5-104"> (IHV) 元素的連線能力</span><span class="sxs-lookup"><span data-stu-id="af5f5-104">connectivity (IHV) Element</span></span>

<span data-ttu-id="af5f5-105"> (IHV) 元素的連線能力包含與 IHV 相關的連線設定。</span><span class="sxs-lookup"><span data-stu-id="af5f5-105">The connectivity (IHV) element contains IHV-related connectivity settings.</span></span> <span data-ttu-id="af5f5-106">目前未執行。</span><span class="sxs-lookup"><span data-stu-id="af5f5-106">It is not currently implemented.</span></span>

<span data-ttu-id="af5f5-107">Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 不支援這個元素。</span><span class="sxs-lookup"><span data-stu-id="af5f5-107">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
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
```

<span data-ttu-id="af5f5-108">元素是由 [**IHV**](wlan-profileschema-ihv-wlanprofile-element.md) 元素定義。</span><span class="sxs-lookup"><span data-stu-id="af5f5-108">The element is defined by the [**IHV**](wlan-profileschema-ihv-wlanprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="af5f5-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="af5f5-109">Requirements</span></span>



| <span data-ttu-id="af5f5-110">需求</span><span class="sxs-lookup"><span data-stu-id="af5f5-110">Requirement</span></span> | <span data-ttu-id="af5f5-111">值</span><span class="sxs-lookup"><span data-stu-id="af5f5-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="af5f5-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="af5f5-112">Minimum supported client</span></span><br/> | <span data-ttu-id="af5f5-113">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="af5f5-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="af5f5-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="af5f5-114">Minimum supported server</span></span><br/> | <span data-ttu-id="af5f5-115">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="af5f5-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="af5f5-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="af5f5-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="af5f5-117">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="af5f5-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="af5f5-118">**IHV**</span><span class="sxs-lookup"><span data-stu-id="af5f5-118">**IHV**</span></span>](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="af5f5-119">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="af5f5-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="af5f5-120">**IHV (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="af5f5-120">**IHV (WLANProfile)**</span></span>](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> </dl>

 

 




