---
description: 有許多支援的備份類型&\# 郵件; 增量、差異和完整&\# 郵件; vss 感知，以及備份設定什麼嗎至 vss。
ms.assetid: eddf29bc-221b-4b10-9842-a893b62fa846
title: VSS 備份設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4e4c4f383a208781722053b47ba9ae5bcbf1db7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106967135"
---
# <a name="vss-backup-configurations"></a><span data-ttu-id="92e61-103">VSS 備份設定</span><span class="sxs-lookup"><span data-stu-id="92e61-103">VSS Backup Configurations</span></span>

<span data-ttu-id="92e61-104">有一些可支援的傳統備份類型（累加、差異和完整），也就是 VSS 的認知，以及備份設定什麼嗎至 VSS。</span><span class="sxs-lookup"><span data-stu-id="92e61-104">There are a number of conventionally supported backup types—incremental, differential, and full—that VSS is aware of, as well as a backup configuration peculiar to VSS.</span></span>

<span data-ttu-id="92e61-105">在定義備份設定時，系統要求者和系統的寫入器會指出資料如何寫入儲存裝置、如何部署陰影複製機制，以及需要儲存哪些資訊。</span><span class="sxs-lookup"><span data-stu-id="92e61-105">In defining a backup configuration, a requester and the writers on a system indicate how data will be written to a storage device, how the shadow copy mechanism will be deployed, and what information needs to be saved.</span></span> <span data-ttu-id="92e61-106">寫入器與要求者之間的互動取決於要求者想要執行的備份類型，以及每個寫入器可支援的 (或架構) 類型：</span><span class="sxs-lookup"><span data-stu-id="92e61-106">Interaction between writers and requesters is determined by the type of backup a requester wants to perform and the kinds (or schemas) that each writer can support:</span></span>

-   [<span data-ttu-id="92e61-107">VSS 備份狀態</span><span class="sxs-lookup"><span data-stu-id="92e61-107">VSS Backup State</span></span>](vss-backup-state.md)
-   [<span data-ttu-id="92e61-108">寫入器備份架構支援</span><span class="sxs-lookup"><span data-stu-id="92e61-108">Writer Backup Schema Support</span></span>](writer-backup-schema-support.md)
-   [<span data-ttu-id="92e61-109">檔案層級架構支援</span><span class="sxs-lookup"><span data-stu-id="92e61-109">File Level Schema Support</span></span>](file-level-schema-support.md)

 

 



