---
description: 列出並說明 GINA 的責任。
ms.assetid: 5cffe4a6-6475-441e-bf81-f3cbcf1fee3f
title: GINA 的責任
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40c3481aea9f5a92a485c42fb00b43d7062012d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026708"
---
# <a name="responsibilities-of-the-gina"></a><span data-ttu-id="0d766-103">GINA 的責任</span><span class="sxs-lookup"><span data-stu-id="0d766-103">Responsibilities of the GINA</span></span>

> [!Note]  
> <span data-ttu-id="0d766-104">在 Windows Vista 中會忽略 GINA Dll。</span><span class="sxs-lookup"><span data-stu-id="0d766-104">GINA DLLs are ignored in Windows Vista.</span></span>

 

<span data-ttu-id="0d766-105">[*GINA*](../secgloss/g-gly.md) DLL 具有下列責任：</span><span class="sxs-lookup"><span data-stu-id="0d766-105">A [*GINA*](../secgloss/g-gly.md) DLL has the following responsibilities:</span></span>

-   <span data-ttu-id="0d766-106">SAS 監視</span><span class="sxs-lookup"><span data-stu-id="0d766-106">SAS monitoring</span></span>

    <span data-ttu-id="0d766-107">GINA 負責辨識 (SAS) 的 [*安全注意順序*](../secgloss/s-gly.md) 、監視 sas 事件，以及在發生 sas 時通知 Winlogon。</span><span class="sxs-lookup"><span data-stu-id="0d766-107">The GINA is responsible for recognizing a [*secure attention sequence*](../secgloss/s-gly.md) (SAS), monitoring for SAS events, and notifying Winlogon when a SAS has occurred.</span></span> <span data-ttu-id="0d766-108">請注意，您可以定義一個以上的 SAS，而定義的 SASs 集合可能會隨著時間而變更。</span><span class="sxs-lookup"><span data-stu-id="0d766-108">Note that there can be more than one SAS defined, and the set of defined SASs can change over time.</span></span> <span data-ttu-id="0d766-109">例如，當 [*Winlogon*](../secgloss/w-gly.md) 處於已登入的狀態時，可能會有一組 SASs，另一組則處於登入狀態。</span><span class="sxs-lookup"><span data-stu-id="0d766-109">For example, there can be one set of SASs when [*Winlogon*](../secgloss/w-gly.md) is in the logged-off state and another set when it is in the logged-on state.</span></span>

    <span data-ttu-id="0d766-110">Winlogon 提供使用 CTRL + ALT + DEL SAS 來協助 GINA 的服務。</span><span class="sxs-lookup"><span data-stu-id="0d766-110">Winlogon provides services to assist the GINA in using the CTRL+ALT+DEL SAS.</span></span>

-   <span data-ttu-id="0d766-111">SAS 處理</span><span class="sxs-lookup"><span data-stu-id="0d766-111">SAS processing</span></span>

    <span data-ttu-id="0d766-112">讓 GINA 可取代的原因之一，就是提供替代的識別和驗證機制。</span><span class="sxs-lookup"><span data-stu-id="0d766-112">One reason for making the GINA replaceable is to provide alternative identification and authentication mechanisms.</span></span> <span data-ttu-id="0d766-113">若要這樣做，GINA 必須顯示所有由 SAS 辨識所產生的使用者介面。</span><span class="sxs-lookup"><span data-stu-id="0d766-113">To do this, the GINA must present all user interfaces resulting from the recognition of a SAS.</span></span> <span data-ttu-id="0d766-114">當使用者未登入時，GINA 會負責呈現身分識別和驗證選項，以及任何其他未經過驗證的允許選項。</span><span class="sxs-lookup"><span data-stu-id="0d766-114">When no user is logged on, the GINA is responsible for presenting identification and authentication options as well as any other permissible options that are not authenticated.</span></span> <span data-ttu-id="0d766-115">當使用者登入時，GINA 會負責向使用者呈現相關的選項，以及採取適當的動作。</span><span class="sxs-lookup"><span data-stu-id="0d766-115">When a user is logged on, the GINA is responsible for presenting the relevant options to the user as well as taking whatever actions are deemed appropriate.</span></span> <span data-ttu-id="0d766-116">例如，在包含 [*智慧卡*](../secgloss/s-gly.md)的系統中，如果使用者移除智慧卡，可能會自動鎖定工作站。</span><span class="sxs-lookup"><span data-stu-id="0d766-116">For example, in a system that includes a [*smart card*](../secgloss/s-gly.md), it may be appropriate to automatically lock the workstation if the user removes the smart card.</span></span>

-   <span data-ttu-id="0d766-117">Shell 啟用</span><span class="sxs-lookup"><span data-stu-id="0d766-117">Shell activation</span></span>

    <span data-ttu-id="0d766-118">當使用者登入時，GINA 會負責為該使用者建立一或多個初始進程。</span><span class="sxs-lookup"><span data-stu-id="0d766-118">When a user logs on, the GINA is responsible for creating one or more initial processes for that user.</span></span> <span data-ttu-id="0d766-119"> (在本檔中，假設這些初始進程會向使用者呈現介面。</span><span class="sxs-lookup"><span data-stu-id="0d766-119">(In this documentation, it is assumed that these initial processes present an interface to the user.</span></span> <span data-ttu-id="0d766-120">不過，處理常式實際上可以是任何程式，且不一定需要與使用者互動。 ) 這些進程稱為 *使用者 shell* 或只是 *shell*。</span><span class="sxs-lookup"><span data-stu-id="0d766-120">However, the processes can actually be any processes and do not necessarily have to interact with the user.) These processes are referred to as the *user shell* or just the *shell*.</span></span> <span data-ttu-id="0d766-121">在 shell 啟用的過程中，GINA 必須將新登入的使用者權杖指派給處理常式。</span><span class="sxs-lookup"><span data-stu-id="0d766-121">As part of shell activation, the GINA must assign the newly logged-on user's token to the processes.</span></span> <span data-ttu-id="0d766-122">Winlogon 提供可協助 GINA 指派權杖的服務。</span><span class="sxs-lookup"><span data-stu-id="0d766-122">Winlogon provides a service to assist the GINA in assigning the token.</span></span>

 

 
