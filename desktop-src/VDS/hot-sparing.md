---
description: 熱備份
ms.assetid: 2faf2f3f-f459-4e41-9c8e-042c7b72281b
title: 熱備份
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a4d007e9219ea79ae3bda31be595c33b537661a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979418"
---
# <a name="hot-sparing"></a><span data-ttu-id="baccc-103">熱備份</span><span class="sxs-lookup"><span data-stu-id="baccc-103">Hot Sparing</span></span>

<span data-ttu-id="baccc-104">\[從 Windows 8 和 Windows Server 2012 開始， [虛擬磁碟服務](virtual-disk-service-portal.md) COM 介面會被 [Windows 儲存體管理 API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)取代。\]</span><span class="sxs-lookup"><span data-stu-id="baccc-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="baccc-105">熱備份是磁片或磁片磁碟機故障或磁片磁碟機故障或磁片磁碟機的替代磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="baccc-105">Hot sparing is the substitution of one disk or drive for a failing or failed disk or drive.</span></span> <span data-ttu-id="baccc-106"> (硬體提供者對磁片磁碟機採取行動;軟體提供者可在磁片上運作。 ) 您可以在子系統中的所有 Lun 之間共用熱備用磁片磁碟機，或將其與特定 LUN 建立關聯。</span><span class="sxs-lookup"><span data-stu-id="baccc-106">(Hardware providers act on drives; software providers act on disks.) You can share a hot spare drive among all the LUNs in the subsystem or associate it with a specific LUN.</span></span> <span data-ttu-id="baccc-107">同樣地，您可以將熱備用磁片與單一磁片區、套件和軟體提供者建立關聯，或在 SAN 上的所有主機之間共用。</span><span class="sxs-lookup"><span data-stu-id="baccc-107">Likewise, you can associate a hot spare disk with a single volume, pack, and software provider, or share it among all hosts on a SAN.</span></span>

<span data-ttu-id="baccc-108">如果相關聯的磁片區或 LUN 具有容錯功能，您可以用熱備用空間來取代故障的磁片或磁片磁碟機，並重建任何受影響的同位 RAID 或鏡像。</span><span class="sxs-lookup"><span data-stu-id="baccc-108">If the associated volume or LUN is fault tolerant, you can substitute a hot spare for a failed disk or drive and rebuild any affected parity RAID or mirrors.</span></span> <span data-ttu-id="baccc-109">即使相關聯的磁片區或 LUN 無法容錯，您也可以更換故障磁片的熱備用。</span><span class="sxs-lookup"><span data-stu-id="baccc-109">You can substitute a hot spare for a failing disk even if the associated volume or LUN is not fault tolerant.</span></span> <span data-ttu-id="baccc-110">假設您可以在發生重大資料遺失之前判斷即將發生的失敗，您可以暫時將熱備用映射鏡像至故障的磁片或磁片磁碟機，然後移除故障的磁片或磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="baccc-110">Assuming that you can determine the impending failure prior to catastrophic data loss, you can temporarily mirror the hot spare to the failing disk or drive and then remove the failing disk or drive.</span></span>

<span data-ttu-id="baccc-111">熱備用可以是自動或手動。</span><span class="sxs-lookup"><span data-stu-id="baccc-111">Hot sparing can be automatic or manual.</span></span> <span data-ttu-id="baccc-112">如果提供者會執行自動熱備份，它會動態地執行替代。</span><span class="sxs-lookup"><span data-stu-id="baccc-112">If a provider implements automatic hot sparing, it performs the substitution dynamically.</span></span> <span data-ttu-id="baccc-113">手動熱備份需要操作員或應用程式介入。</span><span class="sxs-lookup"><span data-stu-id="baccc-113">Manual hot sparing requires operator or application intervention.</span></span> <span data-ttu-id="baccc-114">熱備用可以包含部分資料或從先前使用的格式。</span><span class="sxs-lookup"><span data-stu-id="baccc-114">A hot spare can contain partial data or formatting from a previous use.</span></span> <span data-ttu-id="baccc-115">發生替代時，VDS 會覆寫熱備用。</span><span class="sxs-lookup"><span data-stu-id="baccc-115">VDS overwrites the hot spare when the substitution occurs.</span></span>

<span data-ttu-id="baccc-116">您無法使用熱備用來進行一般系結作業。</span><span class="sxs-lookup"><span data-stu-id="baccc-116">You cannot use a hot spare for ordinary binding operations.</span></span> <span data-ttu-id="baccc-117">如果熱備件大於失敗的磁片或磁片磁碟機，則任何多餘的空間都會保持未使用，直到明確宣告可供系結使用為止。</span><span class="sxs-lookup"><span data-stu-id="baccc-117">If the hot spare is larger than the failed disk or drive, any excess space remains unused until it is explicitly declared available for binding.</span></span> <span data-ttu-id="baccc-118">使用熱備用復原後，磁片或磁片磁碟機就不再是熱備用。</span><span class="sxs-lookup"><span data-stu-id="baccc-118">Once the hot spare has been used for recovery, the disk or drive is no longer a hot spare.</span></span> <span data-ttu-id="baccc-119">換句話說，1 16 gb 主軸無法作為 2 8 gb 的熱備件。</span><span class="sxs-lookup"><span data-stu-id="baccc-119">In other words, one 16-gigabyte spindle cannot act as two 8-gigabyte hot spares.</span></span>

 

 
