---
description: 與資源管理相關的虛擬化 WMI 類別。
ms.assetid: 70184AEA-EA2E-4CC8-8DB3-828833E7C4C2
title: 資源管理類別
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b435f4aebf125b445737bb6b0aa68b427838159
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983739"
---
# <a name="resource-management-classes"></a><span data-ttu-id="26098-103">資源管理類別</span><span class="sxs-lookup"><span data-stu-id="26098-103">Resource management classes</span></span>

<span data-ttu-id="26098-104">以下是與資源管理相關的虛擬化 WMI 類別。</span><span class="sxs-lookup"><span data-stu-id="26098-104">The following are virtualization WMI classes related to resource management.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="26098-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="26098-105">In this section</span></span>



| <span data-ttu-id="26098-106">主題</span><span class="sxs-lookup"><span data-stu-id="26098-106">Topic</span></span>                                                                                                        | <span data-ttu-id="26098-107">描述</span><span class="sxs-lookup"><span data-stu-id="26098-107">Description</span></span>                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="26098-108">**Msvm \_ AbstractResourcePoolSettingData**</span><span class="sxs-lookup"><span data-stu-id="26098-108">**Msvm\_AbstractResourcePoolSettingData**</span></span>](msvm-abstractresourcepoolsettingdata.md)<br/>             | <span data-ttu-id="26098-109">表示非配置相關之 [**Msvm \_ ResourcePool**](msvm-resourcepool.md) 實例的設定。</span><span class="sxs-lookup"><span data-stu-id="26098-109">Represents the settings of a [**Msvm\_ResourcePool**](msvm-resourcepool.md) instance that are not allocation related.</span></span><br/>                                |
| [<span data-ttu-id="26098-110">**Msvm \_ AllocationCapabilities**</span><span class="sxs-lookup"><span data-stu-id="26098-110">**Msvm\_AllocationCapabilities**</span></span>](msvm-allocationcapabilities.md)<br/>                               | <span data-ttu-id="26098-111">定義用戶端可以探索虛擬資源預設設定之有效範圍的方法。</span><span class="sxs-lookup"><span data-stu-id="26098-111">Defines the means by which a client can discover the valid range of default settings for a virtual resource.</span></span><br/>                                          |
| [<span data-ttu-id="26098-112">**Msvm \_ ElementAllocatedFromPool**</span><span class="sxs-lookup"><span data-stu-id="26098-112">**Msvm\_ElementAllocatedFromPool**</span></span>](msvm-elementallocatedfrompool.md)<br/>                           | <span data-ttu-id="26098-113">將已配置資源的實例與從中配置資源的資源集區產生關聯。</span><span class="sxs-lookup"><span data-stu-id="26098-113">Associates an instance of an allocated resource with the resource pool from which it was allocated.</span></span><br/>                                                   |
| [<span data-ttu-id="26098-114">**Msvm \_ ElementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="26098-114">**Msvm\_ElementCapabilities**</span></span>](msvm-elementcapabilities.md)<br/>                                     | <span data-ttu-id="26098-115">代表 managed 元素與其功能之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="26098-115">Represents the association between managed elements and their capabilities.</span></span><br/>                                                                           |
| [<span data-ttu-id="26098-116">**Msvm \_ FeatureSettingData**</span><span class="sxs-lookup"><span data-stu-id="26098-116">**Msvm\_FeatureSettingData**</span></span>](msvm-featuresettingdata.md)<br/>                                       | <span data-ttu-id="26098-117">抽象類別，表示系統或元件之特定功能的設定。</span><span class="sxs-lookup"><span data-stu-id="26098-117">An abstract class that represents settings for a specific feature of a system or component.</span></span><br/>                                                           |
| [<span data-ttu-id="26098-118">**Msvm \_ FeatureSettingsDefineCapabilities**</span><span class="sxs-lookup"><span data-stu-id="26098-118">**Msvm\_FeatureSettingsDefineCapabilities**</span></span>](msvm-featuresettingsdefinecapabilities.md)<br/>         | <span data-ttu-id="26098-119">提供乙太網路交換器功能實例與資源的最小值、最大值、增量和預設設定之間的連結。</span><span class="sxs-lookup"><span data-stu-id="26098-119">Provides a link between the Ethernet switch feature capabilities instance and the minimum, maximum, incremental, and default settings for a resource.</span></span><br/> |
| [<span data-ttu-id="26098-120">**Msvm \_ ResourceAllocationFromPool**</span><span class="sxs-lookup"><span data-stu-id="26098-120">**Msvm\_ResourceAllocationFromPool**</span></span>](msvm-resourceallocationfrompool.md)<br/>                       | <span data-ttu-id="26098-121">將資源配置的實例與其配置來源的資源集區產生關聯。</span><span class="sxs-lookup"><span data-stu-id="26098-121">Associates an instance of a resource allocation with the resource pool from which it is allocated.</span></span><br/>                                                    |
| [<span data-ttu-id="26098-122">**Msvm \_ ResourceAllocationSettingData**</span><span class="sxs-lookup"><span data-stu-id="26098-122">**Msvm\_ResourceAllocationSettingData**</span></span>](msvm-resourceallocationsettingdata.md)<br/>                 | <span data-ttu-id="26098-123">代表虛擬資源目前和記錄的配置狀態。</span><span class="sxs-lookup"><span data-stu-id="26098-123">Represents the current and recorded allocation states of a virtual resource.</span></span><br/>                                                                          |
| [<span data-ttu-id="26098-124">**Msvm \_ ResourcePool**</span><span class="sxs-lookup"><span data-stu-id="26098-124">**Msvm\_ResourcePool**</span></span>](msvm-resourcepool.md)<br/>                                                   | <span data-ttu-id="26098-125">描述可在虛擬機器中使用的虛擬資源類型。</span><span class="sxs-lookup"><span data-stu-id="26098-125">Describes a type of virtual resource available for use in virtual machines.</span></span><br/>                                                                           |
| [<span data-ttu-id="26098-126">**Msvm \_ ResourcePoolConfigurationCapabilities**</span><span class="sxs-lookup"><span data-stu-id="26098-126">**Msvm\_ResourcePoolConfigurationCapabilities**</span></span>](msvm-resourcepoolconfigurationcapabilities.md)<br/> | <span data-ttu-id="26098-127">描述相關聯 [**Msvm \_ ResourcePoolConfigurationService**](msvm-resourcepoolconfigurationservice.md) 類別的功能。</span><span class="sxs-lookup"><span data-stu-id="26098-127">Describes the capabilities of the associated [**Msvm\_ResourcePoolConfigurationService**](msvm-resourcepoolconfigurationservice.md) class.</span></span><br/>           |
| [<span data-ttu-id="26098-128">**Msvm \_ ResourcePoolConfigurationService**</span><span class="sxs-lookup"><span data-stu-id="26098-128">**Msvm\_ResourcePoolConfigurationService**</span></span>](msvm-resourcepoolconfigurationservice.md)<br/>           | <span data-ttu-id="26098-129">提供資源集區的主動管理。</span><span class="sxs-lookup"><span data-stu-id="26098-129">Provides for active management of resource pools.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="26098-130">**Msvm \_ ResourcePoolSettingData**</span><span class="sxs-lookup"><span data-stu-id="26098-130">**Msvm\_ResourcePoolSettingData**</span></span>](msvm-resourcepoolsettingdata.md)<br/>                             | <span data-ttu-id="26098-131">表示非配置相關之 [**Msvm \_ ResourcePool**](msvm-resourcepool.md) 實例的設定。</span><span class="sxs-lookup"><span data-stu-id="26098-131">Represents the settings of a [**Msvm\_ResourcePool**](msvm-resourcepool.md) instance that are not allocation related.</span></span><br/>                                |
| [<span data-ttu-id="26098-132">**Msvm \_ SettingsDefineCapabilities**</span><span class="sxs-lookup"><span data-stu-id="26098-132">**Msvm\_SettingsDefineCapabilities**</span></span>](msvm-settingsdefinecapabilities.md)<br/>                       | <span data-ttu-id="26098-133">提供功能實例與資源的最小值、最大值、增量和預設設定之間的連結。</span><span class="sxs-lookup"><span data-stu-id="26098-133">Provides a link between the capabilities instance and the minimum, maximum, incremental, and default settings for a resource.</span></span><br/>                         |



 

 

 




