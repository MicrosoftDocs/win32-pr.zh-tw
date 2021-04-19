---
description: 指定網路類型。
ms.assetid: fe3044ab-6e93-48f8-b8cb-fdf984987232
title: networkType (networkItemType) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- networkType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: c63b8afdaf699fde6871c198a8235772c59da1ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978337"
---
# <a name="networktype-networkitemtype-element"></a><span data-ttu-id="7c0e2-103">networkType (networkItemType) 元素</span><span class="sxs-lookup"><span data-stu-id="7c0e2-103">networkType (networkItemType) Element</span></span>

<span data-ttu-id="7c0e2-104">NetworkType (networkItemType) 元素會指定網路類型。</span><span class="sxs-lookup"><span data-stu-id="7c0e2-104">The networkType (networkItemType) element specifies a network type.</span></span> <span data-ttu-id="7c0e2-105">網路類型有兩種：基礎結構網路 (ESS) 和臨機操作網路 (IBSS) 。</span><span class="sxs-lookup"><span data-stu-id="7c0e2-105">There are two types of networks: infrastructure networks (ESS) and ad-hoc networks (IBSS).</span></span>

``` syntax
<xs:element name="networkType"
    type="networkTypeType"
 />
```

<span data-ttu-id="7c0e2-106">**NetworkType** 元素是由 [**networkItemType**](wlan-policyschema-networkitemtype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="7c0e2-106">The **networkType** element is defined by the [**networkItemType**](wlan-policyschema-networkitemtype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c0e2-107">規格需求</span><span class="sxs-lookup"><span data-stu-id="7c0e2-107">Requirements</span></span>



| <span data-ttu-id="7c0e2-108">需求</span><span class="sxs-lookup"><span data-stu-id="7c0e2-108">Requirement</span></span> | <span data-ttu-id="7c0e2-109">值</span><span class="sxs-lookup"><span data-stu-id="7c0e2-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7c0e2-110">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7c0e2-110">Minimum supported client</span></span><br/> | <span data-ttu-id="7c0e2-111">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7c0e2-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7c0e2-112">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7c0e2-112">Minimum supported server</span></span><br/> | <span data-ttu-id="7c0e2-113">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7c0e2-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7c0e2-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7c0e2-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="7c0e2-115">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="7c0e2-115">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="7c0e2-116">**networkItemType**</span><span class="sxs-lookup"><span data-stu-id="7c0e2-116">**networkItemType**</span></span>](wlan-policyschema-networkitemtype-complextype.md)
</dt> <dt>

<span data-ttu-id="7c0e2-117">**架構實例中可能的直接父元素**</span><span class="sxs-lookup"><span data-stu-id="7c0e2-117">**Possible immediate parent elements in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="7c0e2-118">**network (允許清單)**</span><span class="sxs-lookup"><span data-stu-id="7c0e2-118">**network (allowList)**</span></span>](wlan-policyschema-network-allowlist-element.md)
</dt> <dt>

[<span data-ttu-id="7c0e2-119">**network (封鎖清單)**</span><span class="sxs-lookup"><span data-stu-id="7c0e2-119">**network (blockList)**</span></span>](wlan-policyschema-network-blocklist-element.md)
</dt> </dl>

 

 




