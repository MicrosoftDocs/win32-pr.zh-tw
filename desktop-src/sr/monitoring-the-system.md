---
title: 監視系統
description: 監視系統
ms.assetid: e0318aca-4e3e-4272-ba31-c770d6b05272
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da7d18f42ac091b9c73c4d9a9ac3929bed235310
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104371809"
---
# <a name="monitoring-the-system"></a><span data-ttu-id="22212-103">監視系統</span><span class="sxs-lookup"><span data-stu-id="22212-103">Monitoring the System</span></span>

<span data-ttu-id="22212-104">在 Windows Vista 和更新版本中系統還原會在產生還原點時，儲存磁片區的複本。</span><span class="sxs-lookup"><span data-stu-id="22212-104">System Restore in Windows Vista and later saves a copy of the volume when generating a restore point.</span></span> <span data-ttu-id="22212-105">系統還原在安裝時，系統磁片磁碟機上至少需要 300 MB 的可用磁碟空間。</span><span class="sxs-lookup"><span data-stu-id="22212-105">System Restore requires a minimum of 300 MB of free disk space on the system drive at installation.</span></span>

<span data-ttu-id="22212-106">在 Windows XP 中系統還原會監視一組核心的系統和應用程式檔，並在進行系統變更之前，先封存這些檔案的狀態。</span><span class="sxs-lookup"><span data-stu-id="22212-106">System Restore in Windows XP monitors a core set of system and application files, archiving the states of these files before system changes are made.</span></span> <span data-ttu-id="22212-107">系統還原也會儲存登錄和一些動態系統檔案的完整快照。</span><span class="sxs-lookup"><span data-stu-id="22212-107">System Restore also saves a full snapshot of the registry and some dynamic system files.</span></span> <span data-ttu-id="22212-108">系統還原在安裝時，系統磁片磁碟機上至少需要 200 MB 的可用磁碟空間。</span><span class="sxs-lookup"><span data-stu-id="22212-108">System Restore requires a minimum of 200 MB of free disk space on the system drive at installation.</span></span> <span data-ttu-id="22212-109">當可用磁碟空間量低於任何磁片磁碟機上的 50 MB 時，系統還原切換為待命模式，並停止建立還原點。</span><span class="sxs-lookup"><span data-stu-id="22212-109">When the amount of free disk space falls below 50 MB on any drive, System Restore switches to standby mode and stops creating restore points.</span></span> <span data-ttu-id="22212-110">屆時會刪除所有還原點。</span><span class="sxs-lookup"><span data-stu-id="22212-110">All restore points are deleted at that time.</span></span> <span data-ttu-id="22212-111">當系統磁片磁碟機上有 200 MB 的可用磁碟空間時，系統還原重新開機並繼續建立還原點。</span><span class="sxs-lookup"><span data-stu-id="22212-111">System Restore reactivates and resumes creating restore points as soon as 200 MB of disk space is free on the system drive.</span></span> <span data-ttu-id="22212-112">在檔案% windir% \\ system32 還原Filelist.xml 中，指定監視或排除監視的檔案 \\ \\ 。</span><span class="sxs-lookup"><span data-stu-id="22212-112">The files that are monitored or excluded from monitoring are specified in the file %windir%\\system32\\restore\\Filelist.xml.</span></span> <span data-ttu-id="22212-113">如需詳細資訊，請參閱 [監視](monitored-file-extensions.md)的副檔名。</span><span class="sxs-lookup"><span data-stu-id="22212-113">For more information, see [Monitored File Name Extensions](monitored-file-extensions.md).</span></span>

 

 




