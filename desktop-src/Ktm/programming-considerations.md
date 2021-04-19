---
description: 深入瞭解：撰寫資源管理員的程式設計考慮
ms.assetid: 7f1e61e8-15e1-4a25-b864-eeadcac61108
title: 撰寫資源管理員的程式設計考慮
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bae64ead32c747a0e8499dcdc8821d36f01f06e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980322"
---
# <a name="programming-considerations-for-writing-resource-managers"></a><span data-ttu-id="5ae70-103">撰寫資源管理員的程式設計考慮</span><span class="sxs-lookup"><span data-stu-id="5ae70-103">Programming Considerations For Writing Resource Managers</span></span>

<span data-ttu-id="5ae70-104">使用核心交易管理員 API 將交易支援新增至您的應用程式時，請考慮下列事項：</span><span class="sxs-lookup"><span data-stu-id="5ae70-104">When using the Kernel Transaction Manager API to add transaction support to your applications, consider the following:</span></span>

-   <span data-ttu-id="5ae70-105">當您撰寫自己的 resource manager 時，您應該具備交易管理技術和通訊協定的良好、實用知識。</span><span class="sxs-lookup"><span data-stu-id="5ae70-105">When you are writing your own resource manager, you should have a good, working knowledge of transaction management techniques and protocols.</span></span>
-   <span data-ttu-id="5ae70-106">如果您未正確寫入資源管理員，您可以使用不當處理的復原作業來損毀自己的資料。</span><span class="sxs-lookup"><span data-stu-id="5ae70-106">If you do not write resource managers correctly, you can corrupt your own data with improperly handled recovery operations.</span></span> <span data-ttu-id="5ae70-107">您也可以釘選交易記錄的結尾，並將交易記錄填滿檔案系統。</span><span class="sxs-lookup"><span data-stu-id="5ae70-107">You can also pin the tail of transaction log and fill up your file system with transaction logs.</span></span>
-   <span data-ttu-id="5ae70-108">如果您的記錄大小原則未設定為防止記錄檔大小增加，則您的 resource manager 不會停止交易。</span><span class="sxs-lookup"><span data-stu-id="5ae70-108">If your log size policy is not set to prevent the log from increasing in size, your resource manager will not stop transactions.</span></span> <span data-ttu-id="5ae70-109">您的資源管理員必須停止更新系統，使其不會溢出檔案系統資源。</span><span class="sxs-lookup"><span data-stu-id="5ae70-109">Your resource manager must stop updating the system so it does not overrun the file system resources.</span></span>
-   <span data-ttu-id="5ae70-110">資源管理員應該使用 (Acl) 的存取控制清單來控制記錄檔的存取權;否則，可能會發生阻絕服務攻擊。</span><span class="sxs-lookup"><span data-stu-id="5ae70-110">Resource managers should use access control lists (ACLs) to control access to the log files; otherwise, denial of service attacks are possible.</span></span>
-   <span data-ttu-id="5ae70-111">快取資料的任何 resource manager 或交易參與者都必須登記預先準備的通知。</span><span class="sxs-lookup"><span data-stu-id="5ae70-111">Any resource manager or transaction participant that caches data must enlist for pre-prepare notifications.</span></span> <span data-ttu-id="5ae70-112">收到預先準備通知時，您必須排清所有資料，以便任何下游資源管理員都可以在準備階段之前登記。</span><span class="sxs-lookup"><span data-stu-id="5ae70-112">When a pre-prepare notification is received, you must flush all your data, so that any downstream resource managers can enlist before the prepare phase.</span></span> <span data-ttu-id="5ae70-113">該交易中的任何進一步工作都不能快取。</span><span class="sxs-lookup"><span data-stu-id="5ae70-113">Any further work in that transaction must not be cached.</span></span>
-   <span data-ttu-id="5ae70-114">當交易仍為使用中時，請勿關閉登記控制碼;這將會回復交易。</span><span class="sxs-lookup"><span data-stu-id="5ae70-114">Do not close an enlistment handle while the transaction is still active; this will cause the transaction to be rolled back.</span></span>

 

 



