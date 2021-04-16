---
description: 指定已拒絕的網路是否出現在 [連接到網路] 嚮導中。
ms.assetid: d0a13a80-2532-4383-8946-2536cc1f5e12
title: showDeniedNetwork (globalFlags) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- showDeniedNetwork
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 33049dad00e5fda22e3f739d3dc200a282481a8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512528"
---
# <a name="showdeniednetwork-globalflags-element"></a><span data-ttu-id="22281-103">showDeniedNetwork (globalFlags) 元素</span><span class="sxs-lookup"><span data-stu-id="22281-103">showDeniedNetwork (globalFlags) Element</span></span>

<span data-ttu-id="22281-104">**ShowDeniedNetwork** (globalFlags) 元素會指定已拒絕的網路是否出現在 [**連接到網路**] 嚮導中。</span><span class="sxs-lookup"><span data-stu-id="22281-104">The **showDeniedNetwork** (globalFlags) element specifies whether denied networks appear in the **Connect to a Network** wizard.</span></span> <span data-ttu-id="22281-105">群組原則或使用者設定可能會拒絕網路。</span><span class="sxs-lookup"><span data-stu-id="22281-105">Networks may be denied by group policy or by user settings.</span></span> <span data-ttu-id="22281-106">當 **showDeniedNetwork** 的值為 TRUE 時，拒絕的網路會出現在 [ **連接到網路** ] 嚮導中;否則，已拒絕的網路不會出現在嚮導中。</span><span class="sxs-lookup"><span data-stu-id="22281-106">When **showDeniedNetwork** has a value of TRUE, denied networks appear in the **Connect to a Network** wizard; otherwise, denied networks do not appear in the wizard.</span></span>

<span data-ttu-id="22281-107">此為必要元素。</span><span class="sxs-lookup"><span data-stu-id="22281-107">This element is mandatory.</span></span> <span data-ttu-id="22281-108">當設定檔是由自動設定服務建立時，此元素將採用預設值 FALSE。</span><span class="sxs-lookup"><span data-stu-id="22281-108">When a profile is created by the AutoConfig service, this element will take the default value of FALSE.</span></span>

``` syntax
<xs:element name="showDeniedNetwork"
    type="boolean"
 />
```

<span data-ttu-id="22281-109">**ShowDeniedNetwork** 元素是由 [**globalFlags**](wlan-policyschema-globalflags-wlanpolicy-element.md)元素定義。</span><span class="sxs-lookup"><span data-stu-id="22281-109">The **showDeniedNetwork** element is defined by the [**globalFlags**](wlan-policyschema-globalflags-wlanpolicy-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="22281-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="22281-110">Requirements</span></span>



| <span data-ttu-id="22281-111">需求</span><span class="sxs-lookup"><span data-stu-id="22281-111">Requirement</span></span> | <span data-ttu-id="22281-112">值</span><span class="sxs-lookup"><span data-stu-id="22281-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="22281-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="22281-113">Minimum supported client</span></span><br/> | <span data-ttu-id="22281-114">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="22281-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="22281-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="22281-115">Minimum supported server</span></span><br/> | <span data-ttu-id="22281-116">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="22281-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="22281-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="22281-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="22281-118">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="22281-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="22281-119">**globalFlags**</span><span class="sxs-lookup"><span data-stu-id="22281-119">**globalFlags**</span></span>](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="22281-120">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="22281-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="22281-121">**globalFlags (WLANPolicy)**</span><span class="sxs-lookup"><span data-stu-id="22281-121">**globalFlags (WLANPolicy)**</span></span>](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> </dl>

 

 




