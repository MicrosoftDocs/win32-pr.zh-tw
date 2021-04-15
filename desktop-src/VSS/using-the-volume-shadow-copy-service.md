---
description: VSS 備份和還原作業各自都會使用通訊協定來與使用大型儲存體 (寫入器) 的系統互動，以及 (要求者) 進行備份。
ms.assetid: c4dae5ce-0dfa-46ec-909f-8ae79d50a9cb
title: 使用磁碟區陰影複製服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06a1c81d79de30085f783feb02b7a7d47d5dc765
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511529"
---
# <a name="using-the-volume-shadow-copy-service"></a><span data-ttu-id="09fde-103">使用磁碟區陰影複製服務</span><span class="sxs-lookup"><span data-stu-id="09fde-103">Using the Volume Shadow Copy Service</span></span>

<span data-ttu-id="09fde-104">VSS 備份和還原作業各自都會使用通訊協定來與使用大型儲存體 (寫入器) 的系統互動，以及 (要求者) 進行備份。</span><span class="sxs-lookup"><span data-stu-id="09fde-104">VSS backup and restore operations each use a protocol for the interaction of the systems that use mass storage (writers) and those that back it up (requesters).</span></span>

<span data-ttu-id="09fde-105">備份和還原作業主要是由要求者驅動，藉由產生可供寫入器處理的全系統 COM 事件，來控制寫入器和提供者的行為。</span><span class="sxs-lookup"><span data-stu-id="09fde-105">Both backup and restore operations are primarily driven by the requester, which controls writer and provider behavior by generating systemwide COM events for the writer to process.</span></span> <span data-ttu-id="09fde-106">因為事件產生的方法是非同步，所以寫入器對要求者的狀態有有限的控制權，可透過 VSS 取得的非同步處理常式 (查看 [**IVssAsync**](/windows/desktop/api/Vss/nn-vss-ivssasync)) 。</span><span class="sxs-lookup"><span data-stu-id="09fde-106">Because event-generating methods are asynchronous, writers do have limited control into the requester's state through the asynchronous handlers available to VSS (see [**IVssAsync**](/windows/desktop/api/Vss/nn-vss-ivssasync)).</span></span>

<span data-ttu-id="09fde-107">這項互動需要基本的資料結構，描述檔案和檔案群組 ([*元件*](vssgloss-c.md)) ，以及元資料模型，以允許儲存備份資訊和允許寫入器/要求者通訊。</span><span class="sxs-lookup"><span data-stu-id="09fde-107">This interaction requires basic data structures describing files and groups of files ([*components*](vssgloss-c.md)), as well as a metadata model to allow the storage of backup information and to permit writer/requester communication.</span></span>

-   [<span data-ttu-id="09fde-108">VSS 應用程式相容性</span><span class="sxs-lookup"><span data-stu-id="09fde-108">VSS Application Compatibility</span></span>](usage-conventions.md)
-   [<span data-ttu-id="09fde-109">設定 VSS</span><span class="sxs-lookup"><span data-stu-id="09fde-109">Configuring VSS</span></span>](configuring-vss.md)
-   [<span data-ttu-id="09fde-110">VSS 中繼資料</span><span class="sxs-lookup"><span data-stu-id="09fde-110">VSS Metadata</span></span>](vss-metadata.md)
-   [<span data-ttu-id="09fde-111">使用 Selectability 和邏輯路徑</span><span class="sxs-lookup"><span data-stu-id="09fde-111">Working with Selectability and Logical Paths</span></span>](working-with-selectability-and-logical-paths.md)
-   [<span data-ttu-id="09fde-112">在 VSS 下處理備份的總覽</span><span class="sxs-lookup"><span data-stu-id="09fde-112">Overview of Processing a Backup Under VSS</span></span>](overview-of-processing-a-backup-under-vss.md)
-   [<span data-ttu-id="09fde-113">在 VSS 下處理還原的總覽</span><span class="sxs-lookup"><span data-stu-id="09fde-113">Overview of Processing a Restore Under VSS</span></span>](overview-of-processing-a-restore-under-vss.md)

 

 



