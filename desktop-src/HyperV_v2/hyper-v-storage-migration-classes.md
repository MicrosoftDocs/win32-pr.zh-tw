---
description: Hyper-v 遷移 API 會定義下列程式設計項目。
ms.assetid: E1FE7351-2F14-4C8F-AF5C-9009CC61CE22
title: Hyper-v 遷移 API 參考
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e40a05bc976cf1722aba558eeca9c7b04cdf7287
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974997"
---
# <a name="hyper-v-migration-api-reference"></a><span data-ttu-id="93c22-103">Hyper-v 遷移 API 參考</span><span class="sxs-lookup"><span data-stu-id="93c22-103">Hyper-V migration API reference</span></span>

<span data-ttu-id="93c22-104">Hyper-v 遷移 API 會定義下列程式設計項目。</span><span class="sxs-lookup"><span data-stu-id="93c22-104">The Hyper-V migration API defines the following programming elements.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="93c22-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="93c22-105">In this section</span></span>



| <span data-ttu-id="93c22-106">主題</span><span class="sxs-lookup"><span data-stu-id="93c22-106">Topic</span></span>                                                                                                                                | <span data-ttu-id="93c22-107">描述</span><span class="sxs-lookup"><span data-stu-id="93c22-107">Description</span></span>                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="93c22-108">**Msvm \_ MigrationJob**</span><span class="sxs-lookup"><span data-stu-id="93c22-108">**Msvm\_MigrationJob**</span></span>](msvm-migrationjob.md)<br/>                                                                           | <span data-ttu-id="93c22-109">此類別代表由虛擬系統移轉服務為儲存或虛擬系統移轉所建立的遷移作業工作。</span><span class="sxs-lookup"><span data-stu-id="93c22-109">This class represents a migration operation job created for storage or virtual system migration by the virtual system migration service.</span></span><br/>                                                 |
| [<span data-ttu-id="93c22-110">**Msvm \_ VirtualSystemMigrationCapabilities**</span><span class="sxs-lookup"><span data-stu-id="93c22-110">**Msvm\_VirtualSystemMigrationCapabilities**</span></span>](msvm-virtualsystemmigrationcapabilities.md)<br/>                               | <span data-ttu-id="93c22-111">定義用戶端可以探索遷移服務所提供之方法的方式，以及虛擬系統移轉設定資料的有效範圍。</span><span class="sxs-lookup"><span data-stu-id="93c22-111">Defines the means by which a client can discover the methods provided by the migration service, and valid range of virtual system migration setting data.</span></span><br/>                                |
| [<span data-ttu-id="93c22-112">**Msvm \_ VirtualSystemMigrationNetworkSettingData**</span><span class="sxs-lookup"><span data-stu-id="93c22-112">**Msvm\_VirtualSystemMigrationNetworkSettingData**</span></span>](msvm-virtualsystemmigrationnetworksettingdata.md)<br/>                   | <span data-ttu-id="93c22-113">代表虛擬系統移轉服務接聽傳入虛擬系統移轉的網路。</span><span class="sxs-lookup"><span data-stu-id="93c22-113">Represents the network on which the virtual system migration service is listening for incoming virtual system migration.</span></span><br/>                                                                 |
| [<span data-ttu-id="93c22-114">**Msvm \_ VirtualSystemMigrationService**</span><span class="sxs-lookup"><span data-stu-id="93c22-114">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)<br/>                                         | <span data-ttu-id="93c22-115">表示虛擬系統移轉服務。</span><span class="sxs-lookup"><span data-stu-id="93c22-115">Represents the virtual system migration service.</span></span> <span data-ttu-id="93c22-116">它是用來遷移虛擬系統，或將虛擬系統的儲存體從一個虛擬化平臺遷移到另一個虛擬化平臺。</span><span class="sxs-lookup"><span data-stu-id="93c22-116">It is used for migrating a virtual system or for migrating the storage of a virtual system from one virtualization platform to another.</span></span><br/> |
| [<span data-ttu-id="93c22-117">**Msvm \_ VirtualSystemMigrationServiceSettingData**</span><span class="sxs-lookup"><span data-stu-id="93c22-117">**Msvm\_VirtualSystemMigrationServiceSettingData**</span></span>](msvm-virtualsystemmigrationservicesettingdata.md)<br/>                   | <span data-ttu-id="93c22-118">代表主機上虛擬系統移轉服務的設定。</span><span class="sxs-lookup"><span data-stu-id="93c22-118">Represents the settings for the virtual system migration service on a host.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="93c22-119">**Msvm \_ VirtualSystemMigrationServiceSettingDataComponent**</span><span class="sxs-lookup"><span data-stu-id="93c22-119">**Msvm\_VirtualSystemMigrationServiceSettingDataComponent**</span></span>](msvm-virtualsystemmigrationservicesettingdatacomponent.md)<br/> | <span data-ttu-id="93c22-120">用來表示虛擬系統移轉服務之虛擬系統移轉網路設定的關聯。</span><span class="sxs-lookup"><span data-stu-id="93c22-120">An association used to represent virtual system migration network settings of the virtual system migration service.</span></span><br/>                                                                      |
| [<span data-ttu-id="93c22-121">**Msvm \_ VirtualSystemMigrationSettingData**</span><span class="sxs-lookup"><span data-stu-id="93c22-121">**Msvm\_VirtualSystemMigrationSettingData**</span></span>](msvm-virtualsystemmigrationsettingdata.md)<br/>                                 | <span data-ttu-id="93c22-122">代表遷移虛擬系統和附加至虛擬系統之存放裝置的遷移設定。</span><span class="sxs-lookup"><span data-stu-id="93c22-122">Represents the migration settings for migrating a virtual system and the storage attached to a virtual system.</span></span><br/>                                                                           |



 

 

 




