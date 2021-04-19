---
description: 定義允許的網路。
ms.assetid: 6dd90924-ded4-427d-a6cd-7742acf89c21
title: network (允許清單) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- network
api_type:
- Schema
api_location: ''
ms.openlocfilehash: eb89a3037b7684c4e20e26ef3a2b0502be69251a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106994532"
---
# <a name="network-allowlist-element"></a><span data-ttu-id="9279e-103">network (允許清單) 元素</span><span class="sxs-lookup"><span data-stu-id="9279e-103">network (allowList) Element</span></span>

<span data-ttu-id="9279e-104">Network (允許清單) 元素會定義允許的網路。</span><span class="sxs-lookup"><span data-stu-id="9279e-104">The network (allowList) element defines an allowed network.</span></span> <span data-ttu-id="9279e-105">必須允許電腦連線到允許的網路。</span><span class="sxs-lookup"><span data-stu-id="9279e-105">A machine must be allowed to connect to an allowed network.</span></span>

``` syntax
<xs:element name="network"
    type="networkItemType"
 />
```

<span data-ttu-id="9279e-106">**Network** 元素是由 [**允許清單**](wlan-policyschema-allowlist-networkfilter-element.md)元素定義。</span><span class="sxs-lookup"><span data-stu-id="9279e-106">The **network** element is defined by the [**allowList**](wlan-policyschema-allowlist-networkfilter-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="9279e-107">規格需求</span><span class="sxs-lookup"><span data-stu-id="9279e-107">Requirements</span></span>



| <span data-ttu-id="9279e-108">需求</span><span class="sxs-lookup"><span data-stu-id="9279e-108">Requirement</span></span> | <span data-ttu-id="9279e-109">值</span><span class="sxs-lookup"><span data-stu-id="9279e-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9279e-110">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9279e-110">Minimum supported client</span></span><br/> | <span data-ttu-id="9279e-111">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9279e-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9279e-112">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9279e-112">Minimum supported server</span></span><br/> | <span data-ttu-id="9279e-113">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9279e-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9279e-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9279e-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="9279e-115">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="9279e-115">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="9279e-116">**允許清單**</span><span class="sxs-lookup"><span data-stu-id="9279e-116">**allowList**</span></span>](wlan-policyschema-allowlist-networkfilter-element.md)
</dt> <dt>

<span data-ttu-id="9279e-117">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="9279e-117">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="9279e-118">**允許清單 (networkFilter)**</span><span class="sxs-lookup"><span data-stu-id="9279e-118">**allowList (networkFilter)**</span></span>](wlan-policyschema-allowlist-networkfilter-element.md)
</dt> </dl>

 

 




