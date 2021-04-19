---
description: 指定電腦是否使用內建的自動設定 (自動設定) 服務來管理無線連線。
ms.assetid: c255e0a0-65ae-44a8-95cb-1a000394109d
title: '適用于 WLAN 的 enableAutoConfig (globalFlags) 元素 (LAN_policy) '
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
ms.openlocfilehash: 5105b8e634aa5affa8648b763a82bbd60cbaec17
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/02/2021
ms.locfileid: "107001054"
---
# <a name="enableautoconfig-globalflags-element-lan_policy-for-wlan"></a><span data-ttu-id="4ee5c-103">適用于 WLAN 的 enableAutoConfig (globalFlags) 元素 (LAN_policy) </span><span class="sxs-lookup"><span data-stu-id="4ee5c-103">enableAutoConfig (globalFlags) Element (LAN_policy) for WLAN</span></span> 

<span data-ttu-id="4ee5c-104">**EnableAutoConfig** (globalFlags) 元素會指定電腦是否使用內建的自動設定 (自動設定) 服務來管理無線連線。</span><span class="sxs-lookup"><span data-stu-id="4ee5c-104">The **enableAutoConfig** (globalFlags) element specifies whether machines use the built-in automatic configuration (AutoConfig) service to manage wireless connections.</span></span> <span data-ttu-id="4ee5c-105">當 **enableAutoConfig** 的值為 FALSE 時，電腦不能使用自動設定來管理無線連線，而且自動設定服務只會回應啟用服務的要求。</span><span class="sxs-lookup"><span data-stu-id="4ee5c-105">When **enableAutoConfig** has a value of FALSE, machines must not use AutoConfig to manage wireless connections, and the AutoConfig service only responds to requests to enable the service.</span></span> <span data-ttu-id="4ee5c-106">當 **enableAutoConfig** 的值為 TRUE 時，電腦可能會使用自動設定服務。</span><span class="sxs-lookup"><span data-stu-id="4ee5c-106">When **enableAutoConfig** has a value of TRUE, machines may use the AutoConfig service.</span></span>

<span data-ttu-id="4ee5c-107">此為必要元素。</span><span class="sxs-lookup"><span data-stu-id="4ee5c-107">This element is mandatory.</span></span> <span data-ttu-id="4ee5c-108">當設定檔由自動設定服務建立時，此元素的預設值會是 TRUE。</span><span class="sxs-lookup"><span data-stu-id="4ee5c-108">When a profile is created by the AutoConfig service, this element will have the default value of TRUE.</span></span>

``` syntax
<xs:element name="enableAutoConfig"
    type="boolean"
 />
```

<span data-ttu-id="4ee5c-109">**EnableAutoConfig** 元素是由 [**globalFlags**](wlan-policyschema-globalflags-wlanpolicy-element.md)元素定義。</span><span class="sxs-lookup"><span data-stu-id="4ee5c-109">The **enableAutoConfig** element is defined by the [**globalFlags**](wlan-policyschema-globalflags-wlanpolicy-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ee5c-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="4ee5c-110">Requirements</span></span>



| <span data-ttu-id="4ee5c-111">需求</span><span class="sxs-lookup"><span data-stu-id="4ee5c-111">Requirement</span></span> | <span data-ttu-id="4ee5c-112">值</span><span class="sxs-lookup"><span data-stu-id="4ee5c-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4ee5c-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4ee5c-113">Minimum supported client</span></span><br/> | <span data-ttu-id="4ee5c-114">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4ee5c-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4ee5c-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4ee5c-115">Minimum supported server</span></span><br/> | <span data-ttu-id="4ee5c-116">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4ee5c-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4ee5c-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4ee5c-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="4ee5c-118">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="4ee5c-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="4ee5c-119">**globalFlags**</span><span class="sxs-lookup"><span data-stu-id="4ee5c-119">**globalFlags**</span></span>](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="4ee5c-120">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="4ee5c-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="4ee5c-121">**globalFlags (WLANPolicy)**</span><span class="sxs-lookup"><span data-stu-id="4ee5c-121">**globalFlags (WLANPolicy)**</span></span>](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> </dl>

 

 




