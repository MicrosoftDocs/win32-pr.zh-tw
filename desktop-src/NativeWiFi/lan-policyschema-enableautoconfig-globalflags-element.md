---
description: 指定電腦是否使用內建的自動設定服務來管理需要第2層驗證 (（例如 802.1 X) ）之有線網路的連接。
ms.assetid: c7a0f6bc-4d42-4d95-8483-2c480f4d8db9
title: 'enableAutoConfig (globalFlags) 元素 (LAN_policy) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- enableAutoConfig
api_type:
- Schema
api_location: ''
ms.openlocfilehash: af1ca32f177140bbfc6563f74df5afc519ee0c75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103693840"
---
# <a name="enableautoconfig-globalflags-element-lan_policy"></a><span data-ttu-id="2a542-103">enableAutoConfig (globalFlags) 元素 (LAN_policy) </span><span class="sxs-lookup"><span data-stu-id="2a542-103">enableAutoConfig (globalFlags) Element (LAN_policy)</span></span>

<span data-ttu-id="2a542-104">**EnableAutoConfig** (globalFlags) 元素會指定電腦是否使用內建的自動設定服務來管理需要第2層 (驗證的有線網路連線，例如 802.1 x) 。</span><span class="sxs-lookup"><span data-stu-id="2a542-104">The **enableAutoConfig** (globalFlags) element specifies whether machines use the built-in automatic configuration service to manage connections to wired networks that require layer 2 authentication (such as 802.1X).</span></span>

<span data-ttu-id="2a542-105">當 **enableAutoConfig** 的值為 FALSE 時，電腦不能使用內建的自動設定服務來管理需要第2層驗證的連接。</span><span class="sxs-lookup"><span data-stu-id="2a542-105">When **enableAutoConfig** has a value of FALSE, machines must not use built-in automatic configuration service to manage connections that require layer 2 authentication.</span></span> <span data-ttu-id="2a542-106">相反地， [**profileList**](lan-policyschema-profilelist-lanpolicy-element.md) 元素中指定的網路是唯一可供連接的網路。</span><span class="sxs-lookup"><span data-stu-id="2a542-106">Instead, the network specified in the [**profileList**](lan-policyschema-profilelist-lanpolicy-element.md) element is the only network available for connection.</span></span> <span data-ttu-id="2a542-107">自動設定服務只會回應啟用服務的要求。</span><span class="sxs-lookup"><span data-stu-id="2a542-107">The automatic configuration service will only respond to requests to enable the service.</span></span>

<span data-ttu-id="2a542-108">當 **enableAutoConfig** 的值為 TRUE 時，電腦可能會使用內建的自動設定服務來連線到需要第2層驗證的有線網路。</span><span class="sxs-lookup"><span data-stu-id="2a542-108">When **enableAutoConfig** has a value of TRUE, machines may use the built-in automatic configuration service to connect to wired networks that require layer 2 authentication.</span></span>

``` syntax
<xs:element name="enableAutoConfig"
    type="boolean"
 />
```

<span data-ttu-id="2a542-109">**EnableAutoConfig** 元素是由 [**globalFlags**](lan-policyschema-globalflags-lanpolicy-element.md)元素定義。</span><span class="sxs-lookup"><span data-stu-id="2a542-109">The **enableAutoConfig** element is defined by the [**globalFlags**](lan-policyschema-globalflags-lanpolicy-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a542-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="2a542-110">Requirements</span></span>



| <span data-ttu-id="2a542-111">需求</span><span class="sxs-lookup"><span data-stu-id="2a542-111">Requirement</span></span> | <span data-ttu-id="2a542-112">值</span><span class="sxs-lookup"><span data-stu-id="2a542-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2a542-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2a542-113">Minimum supported client</span></span><br/> | <span data-ttu-id="2a542-114">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2a542-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2a542-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2a542-115">Minimum supported server</span></span><br/> | <span data-ttu-id="2a542-116">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2a542-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2a542-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2a542-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="2a542-118">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="2a542-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="2a542-119">**globalFlags**</span><span class="sxs-lookup"><span data-stu-id="2a542-119">**globalFlags**</span></span>](lan-policyschema-globalflags-lanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="2a542-120">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="2a542-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="2a542-121">**globalFlags (LANPolicy)**</span><span class="sxs-lookup"><span data-stu-id="2a542-121">**globalFlags (LANPolicy)**</span></span>](lan-policyschema-globalflags-lanpolicy-element.md)
</dt> </dl>

 

 




