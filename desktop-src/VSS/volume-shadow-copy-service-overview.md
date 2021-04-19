---
description: 磁碟區陰影複製服務 (VSS) 是一組 COM Api，可執行架構以允許在系統上的應用程式繼續寫入磁片區時執行磁片區備份。
ms.assetid: 263b0200-4869-4fb0-ad50-240166d2d32f
title: 磁碟區陰影複製服務總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2710ee47e20953b7a7ea86d5b0cb3318fc49bdef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972423"
---
# <a name="volume-shadow-copy-service-overview"></a><span data-ttu-id="97421-103">磁碟區陰影複製服務總覽</span><span class="sxs-lookup"><span data-stu-id="97421-103">Volume Shadow Copy Service Overview</span></span>

<span data-ttu-id="97421-104">磁碟區陰影複製服務 (VSS) 是一組 COM Api，可執行架構以允許在系統上的應用程式繼續寫入磁片區時執行磁片區備份。</span><span class="sxs-lookup"><span data-stu-id="97421-104">The Volume Shadow Copy Service (VSS) is a set of COM APIs that implements a framework to allow volume backups to be performed while applications on a system continue to write to the volumes.</span></span>

<span data-ttu-id="97421-105">VSS 提供一致的介面，可讓使用者應用程式在磁片 ([*寫入*](vssgloss-w.md) 器) 上更新資料的使用者應用程式，以及 ([*請求*](vssgloss-r.md) 者) 的應用程式之間進行協調。</span><span class="sxs-lookup"><span data-stu-id="97421-105">VSS provides a consistent interface that allows coordination between user applications that update data on disk ([*writers*](vssgloss-w.md)) and those that back up applications ([*requesters*](vssgloss-r.md)).</span></span>

-   [<span data-ttu-id="97421-106">VSS 的新功能</span><span class="sxs-lookup"><span data-stu-id="97421-106">What's New in VSS</span></span>](what-s-new-in-vss.md)
-   [<span data-ttu-id="97421-107">關於磁碟區陰影複製服務</span><span class="sxs-lookup"><span data-stu-id="97421-107">About the Volume Shadow Copy Service</span></span>](about-the-volume-shadow-copy-service.md)
-   [<span data-ttu-id="97421-108">使用磁碟區陰影複製服務</span><span class="sxs-lookup"><span data-stu-id="97421-108">Using the Volume Shadow Copy Service</span></span>](using-the-volume-shadow-copy-service.md)
-   [<span data-ttu-id="97421-109">VSS 執行詳細資料</span><span class="sxs-lookup"><span data-stu-id="97421-109">VSS Implementation Details</span></span>](vss-implementation-details.md)
-   [<span data-ttu-id="97421-110">針對 VSS 應用程式進行疑難排解</span><span class="sxs-lookup"><span data-stu-id="97421-110">Troubleshooting VSS Applications</span></span>](troubleshooting-vss-applications.md)

 

 



