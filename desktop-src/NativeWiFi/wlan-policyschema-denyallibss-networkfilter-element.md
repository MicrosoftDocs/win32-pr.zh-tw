---
description: 指定是否封鎖對所有特定網路的存取。
ms.assetid: 9001ccbb-c158-44d7-8d31-38c91881886e
title: denyAllIBSS (networkFilter) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- denyAllIBSS
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 78a34b506f4db72d8b61d7c0918c93658e18a062
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106966702"
---
# <a name="denyallibss-networkfilter-element"></a><span data-ttu-id="cd585-103">denyAllIBSS (networkFilter) 元素</span><span class="sxs-lookup"><span data-stu-id="cd585-103">denyAllIBSS (networkFilter) Element</span></span>

<span data-ttu-id="cd585-104">DenyAllIBSS (networkFilter) 元素會指定是否封鎖對所有特定網路的存取。</span><span class="sxs-lookup"><span data-stu-id="cd585-104">The denyAllIBSS (networkFilter) element specifies if access to all ad-hoc networks is blocked.</span></span> <span data-ttu-id="cd585-105">當 **denyAllIBSS** 的值為 TRUE 時，電腦無法連線至臨機操作網路。否則，機器可能會連接到臨機操作網路。</span><span class="sxs-lookup"><span data-stu-id="cd585-105">When **denyAllIBSS** has a value of TRUE, machines cannot connect to an ad-hoc network; otherwise, machines may connect to ad-hoc networks.</span></span>

<span data-ttu-id="cd585-106">此元素的預設值為 FALSE。</span><span class="sxs-lookup"><span data-stu-id="cd585-106">The default value for this element is FALSE.</span></span> <span data-ttu-id="cd585-107">如果設定檔中未指定 **denyAllIBSS** ，則根據預設，電腦會連線至臨機操作網路。</span><span class="sxs-lookup"><span data-stu-id="cd585-107">If **denyAllIBSS** is not specified in a profile, then by default machines may connect to ad-hoc networks.</span></span>

``` syntax
<xs:element name="denyAllIBSS"
    type="boolean"
 />
```

<span data-ttu-id="cd585-108">**DenyAllIBSS** 元素是由 [**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md)元素定義。</span><span class="sxs-lookup"><span data-stu-id="cd585-108">The **denyAllIBSS** element is defined by the [**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd585-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="cd585-109">Requirements</span></span>



| <span data-ttu-id="cd585-110">需求</span><span class="sxs-lookup"><span data-stu-id="cd585-110">Requirement</span></span> | <span data-ttu-id="cd585-111">值</span><span class="sxs-lookup"><span data-stu-id="cd585-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cd585-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cd585-112">Minimum supported client</span></span><br/> | <span data-ttu-id="cd585-113">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cd585-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="cd585-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cd585-114">Minimum supported server</span></span><br/> | <span data-ttu-id="cd585-115">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cd585-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cd585-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cd585-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="cd585-117">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="cd585-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="cd585-118">**networkFilter**</span><span class="sxs-lookup"><span data-stu-id="cd585-118">**networkFilter**</span></span>](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="cd585-119">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="cd585-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="cd585-120">**networkFilter (WLANPolicy)**</span><span class="sxs-lookup"><span data-stu-id="cd585-120">**networkFilter (WLANPolicy)**</span></span>](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> </dl>

 

 




