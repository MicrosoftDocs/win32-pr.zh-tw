---
description: 檔案系統中的最高層級組織是磁片區。 檔案系統位於磁片區上。
ms.assetid: d9ed58e6-2731-4fde-8368-f727420eb773
title: 磁碟區管理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acebdeda5b47a3f1a1753725c5419be36c2a65d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970405"
---
# <a name="volume-management"></a><span data-ttu-id="2929a-104">磁碟區管理</span><span class="sxs-lookup"><span data-stu-id="2929a-104">Volume Management</span></span>

<span data-ttu-id="2929a-105">檔案系統中的最高層級組織是 *磁片* 區。</span><span class="sxs-lookup"><span data-stu-id="2929a-105">The highest level of organization in the file system is the *volume*.</span></span> <span data-ttu-id="2929a-106">檔案系統位於磁片區上。</span><span class="sxs-lookup"><span data-stu-id="2929a-106">A file system resides on a volume.</span></span> <span data-ttu-id="2929a-107">磁片區至少包含一個磁片 *分區*，也就是實體磁片的邏輯除法 (如需詳細資訊，請參閱 [磁片裝置和磁碟分割](disk-devices-and-partitions.md)) 。</span><span class="sxs-lookup"><span data-stu-id="2929a-107">A volume contains at least one *partition*, which is a logical division of a physical disk (for more information, see [Disk Devices and Partitions](disk-devices-and-partitions.md)).</span></span> <span data-ttu-id="2929a-108">包含存在於某個資料分割之資料的磁片區稱為 *簡單磁片* 區，而包含多個資料分割之資料的磁片區稱為 *多重磁片* 區。</span><span class="sxs-lookup"><span data-stu-id="2929a-108">A volume that contains data that exists on one partition is called a *simple volume*, and a volume that contains data that exists on more than one partition is called a *multipartition volume*.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="2929a-109">本節內容</span><span class="sxs-lookup"><span data-stu-id="2929a-109">In this section</span></span>



| <span data-ttu-id="2929a-110">主題</span><span class="sxs-lookup"><span data-stu-id="2929a-110">Topic</span></span>                                                                     | <span data-ttu-id="2929a-111">描述</span><span class="sxs-lookup"><span data-stu-id="2929a-111">Description</span></span>                                                                      |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="2929a-112">關於磁片區管理</span><span class="sxs-lookup"><span data-stu-id="2929a-112">About Volume Management</span></span>](about-volume-management.md)<br/>         | <span data-ttu-id="2929a-113">磁片區是由稱為磁片區管理員的設備磁碟機所執行。</span><span class="sxs-lookup"><span data-stu-id="2929a-113">Volumes are implemented by a device driver called a volume manager.</span></span><br/>   |
| [<span data-ttu-id="2929a-114">使用磁片區管理</span><span class="sxs-lookup"><span data-stu-id="2929a-114">Using Volume Management</span></span>](using-volume-management.md)<br/>         | <span data-ttu-id="2929a-115">示範如何使用磁片區管理功能的範例。</span><span class="sxs-lookup"><span data-stu-id="2929a-115">Examples that demonstrate the use of the volume management functions.</span></span><br/> |
| [<span data-ttu-id="2929a-116">磁片區管理參考</span><span class="sxs-lookup"><span data-stu-id="2929a-116">Volume Management Reference</span></span>](volume-management-reference.md)<br/> | <span data-ttu-id="2929a-117">大量管理中使用的元素。</span><span class="sxs-lookup"><span data-stu-id="2929a-117">Elements used in volume management.</span></span><br/>                                   |



 

 

 




