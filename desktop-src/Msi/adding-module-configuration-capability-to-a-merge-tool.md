---
description: Windows Installer 開發人員可以撰寫可讓終端使用者使用可設定合併模組的工具。
ms.assetid: 5857b788-f1dd-41d0-b0ee-0872494e3c2c
title: 將模組設定功能新增至合併工具
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba04d297ad93cffc553670c648577f650cd21407
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692811"
---
# <a name="adding-module-configuration-capability-to-a-merge-tool"></a><span data-ttu-id="7533e-103">將模組設定功能新增至合併工具</span><span class="sxs-lookup"><span data-stu-id="7533e-103">Adding Module Configuration Capability to a Merge Tool</span></span>

<span data-ttu-id="7533e-104">若要讓終端使用者使用可設定的合併模組，您可以撰寫合併和設定工具來執行下列作業：</span><span class="sxs-lookup"><span data-stu-id="7533e-104">To enable end users to use configurable merge modules, you can author merge and configuration tools to do the following:</span></span>

-   <span data-ttu-id="7533e-105">合併工具應該呼叫 Mergemod.dll 版本2.0 中的函式，以合併模組。</span><span class="sxs-lookup"><span data-stu-id="7533e-105">Merge tools should call the functions in Mergemod.dll version 2.0 to merge the module.</span></span> <span data-ttu-id="7533e-106">舊版的 Mergemod.dll 不能用來設定合併模組。</span><span class="sxs-lookup"><span data-stu-id="7533e-106">Earlier versions of Mergemod.dll cannot be used to configure merge modules.</span></span>
-   <span data-ttu-id="7533e-107">用戶端設定應用程式應與合併模組使用者互動，以收集可設定專案的使用者選擇。</span><span class="sxs-lookup"><span data-stu-id="7533e-107">Client configuration applications should interact with the merge module user to collect the user selections for configurable items.</span></span>
-   <span data-ttu-id="7533e-108">合併工具應該將撰寫的設定資訊公開給用戶端應用程式，讓用戶端可以使用此資訊來查詢使用者。</span><span class="sxs-lookup"><span data-stu-id="7533e-108">Merge tools should expose configuration information authored into the merge module to the client application so that the client can use this information to query the user.</span></span>
-   <span data-ttu-id="7533e-109">當合併工具在合併期間遇到可設定的專案時，應該呼叫用戶端設定工具，以取得從使用者取得的自訂資訊。</span><span class="sxs-lookup"><span data-stu-id="7533e-109">When a merge tool encounters a configurable item during a merge, it should call the client configuration tool for customization information obtained from the user.</span></span> <span data-ttu-id="7533e-110">合併工具應該對合併模組進行指定的變更。</span><span class="sxs-lookup"><span data-stu-id="7533e-110">The merge tool should make the specified changes to the merge module.</span></span>
-   <span data-ttu-id="7533e-111">設定應用程式應可讓使用者提供可設定專案的選項，但是所有可能的選項都不需要向使用者顯示。</span><span class="sxs-lookup"><span data-stu-id="7533e-111">Configuration applications should enable the user to provide choices for configurable items, but all the possible choices do not need to be revealed to the user.</span></span> <span data-ttu-id="7533e-112">合併工具可以針對使用者未選取的可設定專案使用預設值。</span><span class="sxs-lookup"><span data-stu-id="7533e-112">The merge tool can use default values for configurable items that the user does not select.</span></span>
-   <span data-ttu-id="7533e-113">如果使用者未提供自訂資訊，合併工具應該使用合併模組中指定的預設設定值。</span><span class="sxs-lookup"><span data-stu-id="7533e-113">If a user does not provide customization information, merge tools should use the default configuration values that are specified in the merge module.</span></span>
-   <span data-ttu-id="7533e-114">當使用者提供設定工具的特定選項之後，合併工具會呼叫 Mergemod.dll 來執行合併。</span><span class="sxs-lookup"><span data-stu-id="7533e-114">After a user gives the configuration tool specific selections, the merge tool calls Mergemod.dll to perform the merge.</span></span>

 

 



