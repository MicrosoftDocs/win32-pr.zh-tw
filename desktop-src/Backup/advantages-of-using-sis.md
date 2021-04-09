---
title: 使用 SIS 的優點
description: 使用 SIS 和 SIS 備份架構的優點如下所示。
ms.assetid: c72a14a1-92ae-4875-ae73-e277ed2b0c0d
keywords:
- 單一實例存放區 (SIS) 備份，優點
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcd1856ce54e817c25830f15f133c7d76c6a80fc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020903"
---
# <a name="advantages-of-using-sis"></a><span data-ttu-id="95099-104">使用 SIS 的優點</span><span class="sxs-lookup"><span data-stu-id="95099-104">Advantages of Using SIS</span></span>

<span data-ttu-id="95099-105">使用 SIS 和 SIS 備份架構的優點如下：</span><span class="sxs-lookup"><span data-stu-id="95099-105">The advantages of using SIS and the SIS backup architecture are the following:</span></span>

-   <span data-ttu-id="95099-106">Sis 架構會自動維護 SIS 連結和支援檔案之間的連線，因為您的備份應用程式會呼叫 SIS 備份 API 函數。</span><span class="sxs-lookup"><span data-stu-id="95099-106">The connections between the SIS links and the backing files are automatically maintained by the SIS architecture as your backup applications call the SIS backup API functions.</span></span>
-   <span data-ttu-id="95099-107">SIS 重新分析點的內容對您的備份和還原應用程式而言是不透明的，以確保升級至 SIS 內部不需要變更 SIS API 或您的備份與還原呼叫 SIS API 函式的應用程式。</span><span class="sxs-lookup"><span data-stu-id="95099-107">The contents of the SIS reparse points are opaque to your backup and restore applications, ensuring that upgrades to the SIS internals will not require a change in the SIS API or your backup and restore applications that call SIS API functions.</span></span> <span data-ttu-id="95099-108">您只需要使用名為 Sisbkup.dll 的新版本 SIS DLL 重新編譯應用程式。</span><span class="sxs-lookup"><span data-stu-id="95099-108">You need only recompile your application with a new version of the SIS DLL, named Sisbkup.dll.</span></span>
-   <span data-ttu-id="95099-109">由於 SIS 是實作為檔案系統篩選器驅動程式，因此它會持續追蹤 SIS 連結與支援檔案之間的連線。</span><span class="sxs-lookup"><span data-stu-id="95099-109">Because SIS is implemented as a file system filter driver, it constantly tracks the connections between the SIS links and the backing files.</span></span> <span data-ttu-id="95099-110">當備份和還原檔案時，SIS 備份可確保備份和還原每個備份檔案的實例，無論指向它的 SIS 連結數目為何。</span><span class="sxs-lookup"><span data-stu-id="95099-110">When the files are backed up and restored, SIS backup ensures that only one instance of the backing file will be backed up and restored, regardless of the number of SIS links that point to it.</span></span>

 

 




