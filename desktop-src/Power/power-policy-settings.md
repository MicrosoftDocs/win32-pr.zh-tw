---
description: 描述構成電源配置的電源原則設定。
ms.assetid: cd515cd6-67f4-45d0-b769-3abc7a56faa8
title: 電源原則設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f490c758a890faf314be1ddffe9ac7a503bd473
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103693023"
---
# <a name="power-policy-settings"></a><span data-ttu-id="bd771-103">電源原則設定</span><span class="sxs-lookup"><span data-stu-id="bd771-103">Power Policy Settings</span></span>

<span data-ttu-id="bd771-104">電源計劃和方案包含喜好設定和原則設定。</span><span class="sxs-lookup"><span data-stu-id="bd771-104">Power plans and schemes consist of preferences and policy settings.</span></span>

<span data-ttu-id="bd771-105">電源計劃是由一組電源設定喜好設定所組成。</span><span class="sxs-lookup"><span data-stu-id="bd771-105">A power plan consists of a group of power setting preferences.</span></span> <span data-ttu-id="bd771-106">這些喜好設定包含每個電源設定的 AC 和 DC 值。</span><span class="sxs-lookup"><span data-stu-id="bd771-106">These preferences consist of both an AC and DC value for each of the power settings.</span></span> <span data-ttu-id="bd771-107">每個電源計劃都是透過唯一的 **GUID** 和易記名稱來識別。</span><span class="sxs-lookup"><span data-stu-id="bd771-107">Each power plan is identified through a unique **GUID** as well as a friendly name.</span></span> <span data-ttu-id="bd771-108">Windows Vista 有三個預設的電源計劃：省電、平衡和高效能。</span><span class="sxs-lookup"><span data-stu-id="bd771-108">Windows Vista has three default power plans: Power Saver, Balanced, and High Performance.</span></span> <span data-ttu-id="bd771-109">您可以自訂這些計畫，也可以建立其他方案。</span><span class="sxs-lookup"><span data-stu-id="bd771-109">These plans can be customized, and additional plans can be created.</span></span> <span data-ttu-id="bd771-110">所有電源計劃都有一個特質屬性，指出方案的整體電源節省行為。</span><span class="sxs-lookup"><span data-stu-id="bd771-110">All power plans have a personality attribute that indicates the overall power savings behavior of the plan.</span></span>

<span data-ttu-id="bd771-111">下表顯示三個電源計劃特質。</span><span class="sxs-lookup"><span data-stu-id="bd771-111">The following table shows the three power plan personalities.</span></span> 

| <span data-ttu-id="bd771-112">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="bd771-112">Display name</span></span>     | <span data-ttu-id="bd771-113">Description</span><span class="sxs-lookup"><span data-stu-id="bd771-113">Description</span></span>                                                                   | <span data-ttu-id="bd771-114">**GUID**</span><span class="sxs-lookup"><span data-stu-id="bd771-114">**GUID**</span></span>                             |
|------------------|-------------------------------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="bd771-115">節能程式</span><span class="sxs-lookup"><span data-stu-id="bd771-115">Power Saver</span></span>      | <span data-ttu-id="bd771-116">提供降低的效能，可能會增加省電量。</span><span class="sxs-lookup"><span data-stu-id="bd771-116">Delivers reduced performance which may increase power savings.</span></span>                | <span data-ttu-id="bd771-117">a1841308-3541-4fab-bc81-f71556f20b4a</span><span class="sxs-lookup"><span data-stu-id="bd771-117">a1841308-3541-4fab-bc81-f71556f20b4a</span></span> |
| <span data-ttu-id="bd771-118">平衡</span><span class="sxs-lookup"><span data-stu-id="bd771-118">Balanced</span></span>         | <span data-ttu-id="bd771-119">根據需求自動平衡效能和耗電量。</span><span class="sxs-lookup"><span data-stu-id="bd771-119">Automatically balances performance and power consumption according to demand.</span></span> | <span data-ttu-id="bd771-120">381b4222-f694-41f0-9685-ff5bb260df2e</span><span class="sxs-lookup"><span data-stu-id="bd771-120">381b4222-f694-41f0-9685-ff5bb260df2e</span></span> |
| <span data-ttu-id="bd771-121">高效能</span><span class="sxs-lookup"><span data-stu-id="bd771-121">High Performance</span></span> | <span data-ttu-id="bd771-122">以較高的耗電量來提供最高的效能。</span><span class="sxs-lookup"><span data-stu-id="bd771-122">Delivers maximum performance at the expense of higher power consumption.</span></span>      | <span data-ttu-id="bd771-123">8c5e7fda-e8bf-4a96-9a85-a6e23a8c635c</span><span class="sxs-lookup"><span data-stu-id="bd771-123">8c5e7fda-e8bf-4a96-9a85-a6e23a8c635c</span></span> |



 

> [!Note]  
> <span data-ttu-id="bd771-124">支援 [新式待命](/windows-hardware/design/device-experiences/modern-standby) 模式的裝置只允許 **平衡** 的電源計劃。</span><span class="sxs-lookup"><span data-stu-id="bd771-124">Devices that support [Modern Standby](/windows-hardware/design/device-experiences/modern-standby) mode only allow the **Balanced** power plan.</span></span> <span data-ttu-id="bd771-125">**新式待命** 是電源設定管理的較新且更簡化的解決方案。</span><span class="sxs-lookup"><span data-stu-id="bd771-125">**Modern Standby** is the newer, more streamlined solution to power settings management.</span></span>

 

<span data-ttu-id="bd771-126">每部電腦都有一個主動式電源計劃。</span><span class="sxs-lookup"><span data-stu-id="bd771-126">Each computer has a single, active power plan.</span></span> <span data-ttu-id="bd771-127">根據預設，未具許可權使用者可以存取系統電源設定。</span><span class="sxs-lookup"><span data-stu-id="bd771-127">By default, nonprivileged users are able to access system power settings.</span></span> <span data-ttu-id="bd771-128">您可以透過 [電源設定] 上的 Acl 或群組原則，來控制所有或個別電源設定的存取權。</span><span class="sxs-lookup"><span data-stu-id="bd771-128">Access to all or individual power settings can be controlled through ACLs on the power settings or through Group Policy.</span></span> <span data-ttu-id="bd771-129">應用程式應該呼叫 [**PowerSettingAccessCheck**](/windows/desktop/api/PowrProf/nf-powrprof-powersettingaccesscheck) ，以判斷使用者是否具有電源設定的存取權。</span><span class="sxs-lookup"><span data-stu-id="bd771-129">Applications should call [**PowerSettingAccessCheck**](/windows/desktop/api/PowrProf/nf-powrprof-powersettingaccesscheck) to determine if the user has access to the power setting.</span></span>

<span data-ttu-id="bd771-130">每個電源設定都是由唯一的 **GUID** 來識別，並包含好記的名稱、描述、允許的值，以及 AC 和 DC 的預設值。</span><span class="sxs-lookup"><span data-stu-id="bd771-130">Each power setting is identified by a unique **GUID** and includes a friendly name, description, allowable values, and default values for AC and DC.</span></span> <span data-ttu-id="bd771-131">您可以使用 [**PowerCreateSetting**](/windows/desktop/api/PowrProf/nf-powrprof-powercreatesetting) 函式來建立自訂電源設定。</span><span class="sxs-lookup"><span data-stu-id="bd771-131">Custom power settings can be created using the [**PowerCreateSetting**](/windows/desktop/api/PowrProf/nf-powrprof-powercreatesetting) function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bd771-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="bd771-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd771-133">電源配置</span><span class="sxs-lookup"><span data-stu-id="bd771-133">Power Schemes</span></span>](power-schemes.md)
</dt> </dl>

 

 
