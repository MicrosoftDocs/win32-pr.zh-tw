---
description: 指定是否封鎖對所有基礎結構網路的存取。
ms.assetid: d57ae27c-3cd3-4e53-b5c9-cd3cbb91289b
title: denyAllESS (networkFilter) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- denyAllESS
api_type:
- Schema
api_location: ''
ms.openlocfilehash: c3e83aeb14e0572f8e2ccc49bf2d04718afa7f30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191263"
---
# <a name="denyalless-networkfilter-element"></a><span data-ttu-id="fff2a-103">denyAllESS (networkFilter) 元素</span><span class="sxs-lookup"><span data-stu-id="fff2a-103">denyAllESS (networkFilter) Element</span></span>

<span data-ttu-id="fff2a-104">DenyAllESS (networkFilter) 元素會指定是否封鎖對所有基礎結構網路的存取。</span><span class="sxs-lookup"><span data-stu-id="fff2a-104">The denyAllESS (networkFilter) element specifies if access to all infrastructure networks is blocked.</span></span> <span data-ttu-id="fff2a-105">當 **denyAllESS** 的值為 TRUE 時，電腦無法連線到基礎結構網路。否則，機器可能會連接到基礎結構網路。</span><span class="sxs-lookup"><span data-stu-id="fff2a-105">When **denyAllESS** has a value of TRUE, machines cannot connect to an infrastructure network; otherwise, machines may connect to infrastructure networks.</span></span>

<span data-ttu-id="fff2a-106">此元素的預設值為 FALSE。</span><span class="sxs-lookup"><span data-stu-id="fff2a-106">The default value for this element is FALSE.</span></span> <span data-ttu-id="fff2a-107">如果設定檔中未指定 **denyAllESS** ，則根據預設，電腦會連線到基礎結構網路。</span><span class="sxs-lookup"><span data-stu-id="fff2a-107">If **denyAllESS** is not specified in a profile, then by default machines may connect to infrastructure networks.</span></span>

``` syntax
<xs:element name="denyAllESS"
    type="boolean"
 />
```

<span data-ttu-id="fff2a-108">**DenyAllESS** 元素是由 [**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md)元素定義。</span><span class="sxs-lookup"><span data-stu-id="fff2a-108">The **denyAllESS** element is defined by the [**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="fff2a-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="fff2a-109">Requirements</span></span>



| <span data-ttu-id="fff2a-110">需求</span><span class="sxs-lookup"><span data-stu-id="fff2a-110">Requirement</span></span> | <span data-ttu-id="fff2a-111">值</span><span class="sxs-lookup"><span data-stu-id="fff2a-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fff2a-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fff2a-112">Minimum supported client</span></span><br/> | <span data-ttu-id="fff2a-113">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fff2a-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="fff2a-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fff2a-114">Minimum supported server</span></span><br/> | <span data-ttu-id="fff2a-115">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fff2a-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fff2a-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fff2a-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="fff2a-117">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="fff2a-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="fff2a-118">**networkFilter**</span><span class="sxs-lookup"><span data-stu-id="fff2a-118">**networkFilter**</span></span>](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="fff2a-119">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="fff2a-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="fff2a-120">**networkFilter (WLANPolicy)**</span><span class="sxs-lookup"><span data-stu-id="fff2a-120">**networkFilter (WLANPolicy)**</span></span>](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> </dl>

 

 




