---
description: 讀取器是智慧卡系統中的標準裝置。 它們是透過驅動程式來控制，並且會透過隨插即用或透過主控台裝置專案，從系統引進和移除。
ms.assetid: 694902b9-e43c-4558-8fab-baa853f9fc4d
title: 智慧卡讀卡機
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b6f4f5c4d1d487f136fb25052d44659f4b073bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975835"
---
# <a name="smart-card-readers"></a><span data-ttu-id="37d5a-104">智慧卡讀卡機</span><span class="sxs-lookup"><span data-stu-id="37d5a-104">Smart Card Readers</span></span>

<span data-ttu-id="37d5a-105">讀取器是 [*智慧卡*](../secgloss/s-gly.md) 系統中的標準裝置。</span><span class="sxs-lookup"><span data-stu-id="37d5a-105">Readers are standard devices in a [*smart card*](../secgloss/s-gly.md) system.</span></span> <span data-ttu-id="37d5a-106">它們是透過驅動程式來控制，並且會透過隨插即用或透過主控台裝置專案，從系統引進和移除。</span><span class="sxs-lookup"><span data-stu-id="37d5a-106">They are controlled through drivers, and are introduced to and removed from the system through Plug and Play or through the Control Panel Devices item.</span></span>

<span data-ttu-id="37d5a-107">您必須定義每個讀取器，才能使用 [*智慧卡子系統*](../secgloss/s-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="37d5a-107">Each reader must be defined for use by the [*smart card subsystem*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="37d5a-108">子系統對於未特別提供給它的任何讀取器不負任何責任。</span><span class="sxs-lookup"><span data-stu-id="37d5a-108">The subsystem is not responsible for any reader not specifically given to it.</span></span>

<span data-ttu-id="37d5a-109">智慧卡讀卡機可以分成稱為「讀者群組」的邏輯群組。</span><span class="sxs-lookup"><span data-stu-id="37d5a-109">Smart card readers can be divided into logical groups called reader groups.</span></span> <span data-ttu-id="37d5a-110">這些群組可以由子系統定義，也可以由系統管理員和使用者定義。</span><span class="sxs-lookup"><span data-stu-id="37d5a-110">These groups can be defined by the subsystem, as well as defined by administrators and users.</span></span> <span data-ttu-id="37d5a-111">讀取器可以屬於一個以上的讀者群組</span><span class="sxs-lookup"><span data-stu-id="37d5a-111">A reader can belong to more than one reader group</span></span>

<span data-ttu-id="37d5a-112">智慧卡子系統會定義下列群組。</span><span class="sxs-lookup"><span data-stu-id="37d5a-112">The smart card subsystem defines the following groups.</span></span>



| <span data-ttu-id="37d5a-113">群組</span><span class="sxs-lookup"><span data-stu-id="37d5a-113">Group</span></span>                | <span data-ttu-id="37d5a-114">描述</span><span class="sxs-lookup"><span data-stu-id="37d5a-114">Description</span></span>                                                                                                                                                                                            |
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37d5a-115">捨棄 $ AllReaders</span><span class="sxs-lookup"><span data-stu-id="37d5a-115">SCard$AllReaders</span></span>     | <span data-ttu-id="37d5a-116">此群組包含系統中的所有讀取器。</span><span class="sxs-lookup"><span data-stu-id="37d5a-116">This group contains all the readers in the system.</span></span> <span data-ttu-id="37d5a-117">提供給智慧卡子系統的新讀取器會自動包含在全系統的讀取器群組捨棄 $ AllReaders 中。</span><span class="sxs-lookup"><span data-stu-id="37d5a-117">A new reader given to the smart card subsystem is automatically included in the system-wide reader group, SCard$AllReaders.</span></span>                         |
| <span data-ttu-id="37d5a-118">捨棄 $ DefaultReaders</span><span class="sxs-lookup"><span data-stu-id="37d5a-118">SCard$DefaultReaders</span></span> | <span data-ttu-id="37d5a-119">此預設群組（每個 [*終端*](../secgloss/t-gly.md)機各一個）包含所有指派給終端機但未保留給特定用途的讀取器。</span><span class="sxs-lookup"><span data-stu-id="37d5a-119">This default group, one for each [*terminal*](../secgloss/t-gly.md), contains all the readers assigned to the terminal that are not reserved for specific use.</span></span> |



 

 

 
