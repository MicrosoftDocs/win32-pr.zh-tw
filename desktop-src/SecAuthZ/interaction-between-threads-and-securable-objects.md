---
description: 在存取檢查中，系統會比較執行緒存取權杖中的安全性資訊與物件安全描述項中的安全性資訊。
ms.assetid: 40871179-d383-43d0-810d-0805c88dbbd6
title: 執行緒和安全物件之間的互動
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f3e2b18f707ece4d651eeca1c6897bb67aad334
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851692"
---
# <a name="interaction-between-threads-and-securable-objects"></a><span data-ttu-id="55c8c-103">執行緒和安全物件之間的互動</span><span class="sxs-lookup"><span data-stu-id="55c8c-103">Interaction Between Threads and Securable Objects</span></span>

<span data-ttu-id="55c8c-104">當執行緒嘗試使用 [安全物件](securable-objects.md)時，系統會先執行存取檢查，然後才允許執行緒繼續執行。</span><span class="sxs-lookup"><span data-stu-id="55c8c-104">When a thread attempts to use a [securable object](securable-objects.md), the system performs an access check before allowing the thread to proceed.</span></span> <span data-ttu-id="55c8c-105">在存取檢查中，系統會比較執行緒 [*存取權杖*](/windows/desktop/SecGloss/a-gly) 中的安全性資訊與物件 [*安全描述項*](/windows/desktop/SecGloss/s-gly)中的安全性資訊。</span><span class="sxs-lookup"><span data-stu-id="55c8c-105">In an access check, the system compares the security information in the thread's [*access token*](/windows/desktop/SecGloss/a-gly) against the security information in the object's [*security descriptor*](/windows/desktop/SecGloss/s-gly).</span></span>

-   <span data-ttu-id="55c8c-106">存取權杖包含 (Sid) 的 [*安全識別碼*](/windows/desktop/SecGloss/s-gly) ，可識別與執行緒相關聯的使用者。</span><span class="sxs-lookup"><span data-stu-id="55c8c-106">The access token contains [*security identifiers*](/windows/desktop/SecGloss/s-gly) (SIDs) that identify the user associated with the thread.</span></span>
-   <span data-ttu-id="55c8c-107">安全描述項會識別物件的擁有者，並且包含 (DACL) 的 [*任意存取控制清單*](/windows/desktop/SecGloss/d-gly) 。</span><span class="sxs-lookup"><span data-stu-id="55c8c-107">The security descriptor identifies the object's owner and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL).</span></span> <span data-ttu-id="55c8c-108">DACL 包含 (Ace) 的 [*存取控制專案*](/windows/desktop/SecGloss/a-gly) ，其中每個專案都會指定特定使用者或群組允許或拒絕的存取權。</span><span class="sxs-lookup"><span data-stu-id="55c8c-108">The DACL contains [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs), each of which specify the access rights allowed or denied to a specific user or group.</span></span>

<span data-ttu-id="55c8c-109">系統會檢查物件的 DACL，尋找套用至使用者的 Ace，並從執行緒的存取權杖將 Sid 分組。</span><span class="sxs-lookup"><span data-stu-id="55c8c-109">The system checks the object's DACL, looking for ACEs that apply to the user and group SIDs from the thread's access token.</span></span> <span data-ttu-id="55c8c-110">系統會檢查每個 ACE，直到授與或拒絕存取權，或直到沒有其他 Ace 需要檢查為止。</span><span class="sxs-lookup"><span data-stu-id="55c8c-110">The system checks each ACE until access is either granted or denied or until there are no more ACEs to check.</span></span> <span data-ttu-id="55c8c-111">當然， (ACL) 的 [*存取控制清單*](/windows/desktop/SecGloss/a-gly) 可能會有數個適用于權杖 Sid 的 ace。</span><span class="sxs-lookup"><span data-stu-id="55c8c-111">Conceivably, an [*access control list*](/windows/desktop/SecGloss/a-gly) (ACL) could have several ACEs that apply to the token's SIDs.</span></span> <span data-ttu-id="55c8c-112">而且，如果發生這種情況，每個 ACE 授與的存取權限就會累積。</span><span class="sxs-lookup"><span data-stu-id="55c8c-112">And, if this occurs, the access rights granted by each ACE accumulate.</span></span> <span data-ttu-id="55c8c-113">例如，如果一個 ACE 授與群組的讀取權限，而另一個 ACE 授與屬於群組成員之使用者的寫入權限，則使用者可以同時擁有該物件的讀取和寫入存取權。</span><span class="sxs-lookup"><span data-stu-id="55c8c-113">For example, if one ACE grants read access to a group and another ACE grants write access to a user who is a member of the group, the user can have both read and write access to the object.</span></span>

<span data-ttu-id="55c8c-114">下圖顯示這些安全性資訊區塊之間的關聯性：</span><span class="sxs-lookup"><span data-stu-id="55c8c-114">The following illustration shows the relationship between these blocks of security information:</span></span>

![進程、ace 和 dacl 之間的關聯性](images/cssec-02.png)

 

 
