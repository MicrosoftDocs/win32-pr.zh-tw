---
description: 指定無線網路 (SSID) 的服務組識別元。
ms.assetid: 103808f2-9e5f-4605-b42a-337a13455294
title: networkName (networkItemType) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- networkName
api_type:
- Schema
api_location: ''
ms.openlocfilehash: da635c392a29419e7b151cc2c4fb080ff7d3fca9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851792"
---
# <a name="networkname-networkitemtype-element"></a><span data-ttu-id="50655-103">networkName (networkItemType) 元素</span><span class="sxs-lookup"><span data-stu-id="50655-103">networkName (networkItemType) Element</span></span>

<span data-ttu-id="50655-104">NetworkName (networkItemType) 元素會指定無線網路 (SSID) 的服務組識別元。</span><span class="sxs-lookup"><span data-stu-id="50655-104">The networkName (networkItemType) element specifies the service set identifier (SSID) of a wireless network.</span></span>

``` syntax
<xs:element name="networkName"
    type="networkNameType"
 />
```

<span data-ttu-id="50655-105">**NetworkName** 元素是由 [**networkItemType**](wlan-policyschema-networkitemtype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="50655-105">The **networkName** element is defined by the [**networkItemType**](wlan-policyschema-networkitemtype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="50655-106">規格需求</span><span class="sxs-lookup"><span data-stu-id="50655-106">Requirements</span></span>



| <span data-ttu-id="50655-107">需求</span><span class="sxs-lookup"><span data-stu-id="50655-107">Requirement</span></span> | <span data-ttu-id="50655-108">值</span><span class="sxs-lookup"><span data-stu-id="50655-108">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="50655-109">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="50655-109">Minimum supported client</span></span><br/> | <span data-ttu-id="50655-110">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="50655-110">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="50655-111">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="50655-111">Minimum supported server</span></span><br/> | <span data-ttu-id="50655-112">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="50655-112">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="50655-113">另請參閱</span><span class="sxs-lookup"><span data-stu-id="50655-113">See also</span></span>

<dl> <dt>

<span data-ttu-id="50655-114">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="50655-114">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="50655-115">**networkItemType**</span><span class="sxs-lookup"><span data-stu-id="50655-115">**networkItemType**</span></span>](wlan-policyschema-networkitemtype-complextype.md)
</dt> <dt>

<span data-ttu-id="50655-116">**架構實例中可能的直接父元素**</span><span class="sxs-lookup"><span data-stu-id="50655-116">**Possible immediate parent elements in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="50655-117">**network (允許清單)**</span><span class="sxs-lookup"><span data-stu-id="50655-117">**network (allowList)**</span></span>](wlan-policyschema-network-allowlist-element.md)
</dt> <dt>

[<span data-ttu-id="50655-118">**network (封鎖清單)**</span><span class="sxs-lookup"><span data-stu-id="50655-118">**network (blockList)**</span></span>](wlan-policyschema-network-blocklist-element.md)
</dt> </dl>

 

 




