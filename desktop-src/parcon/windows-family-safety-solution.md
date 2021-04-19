---
description: Windows 系列安全性解決方案
ms.assetid: b89cf0c7-bf9f-4bcb-b008-8b7c792f3300
title: Windows 系列安全性解決方案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a2d8776893468df4f4877c7220436f505ab1e6f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985496"
---
# <a name="windows-family-safety-solution"></a><span data-ttu-id="931d3-103">Windows 系列安全性解決方案</span><span class="sxs-lookup"><span data-stu-id="931d3-103">Windows Family Safety Solution</span></span>

<span data-ttu-id="931d3-104">Microsoft 為更詳盡的解決方案所定義的主要需求如下。</span><span class="sxs-lookup"><span data-stu-id="931d3-104">Key requirements defined by Microsoft for a more comprehensive solution are as follows.</span></span> <span data-ttu-id="931d3-105">請注意，online 的定義主要是網際網路面向的技術，與通常會在電腦上限制的離線用戶端不同。</span><span class="sxs-lookup"><span data-stu-id="931d3-105">Note the definition for online is a primarily Internet-facing technology, unlike an offline client which is usually bounded at the computer.</span></span>

-   <span data-ttu-id="931d3-106">在作業系統使用者介面中提供單一、容易尋找的區域，讓您可以隨時探索到身分識別的所有家長監護原則、活動監視的控制權，以及身分識別的活動資料。</span><span class="sxs-lookup"><span data-stu-id="931d3-106">Provide a single, easy to find area in the operating system user interface where all parental controls policies, control of activity monitoring, and activity data for an identity may be readily discovered.</span></span>

-   <span data-ttu-id="931d3-107">支援監視受控制使用者的足夠活動，讓父系或守護者有合理的信心可探索有風險的活動。</span><span class="sxs-lookup"><span data-stu-id="931d3-107">Support monitoring of sufficient activity of the controlled user so that a parent or guardian has reasonable confidence that risky activities may be discovered.</span></span> <span data-ttu-id="931d3-108">此外，也可以重新設定受控制使用者的原則，以便探索非預期或未授權的變更。</span><span class="sxs-lookup"><span data-stu-id="931d3-108">Also, log reconfiguration of the controlled user's policies so that unintended or unauthorized changes are discoverable.</span></span>

-   <span data-ttu-id="931d3-109">透過標準的 Windows Vista 事件記錄介面公開活動監視功能，並提供現成的檢視器解決方案。</span><span class="sxs-lookup"><span data-stu-id="931d3-109">Expose activity monitoring capabilities through standard Windows Vista event logging interfaces, and provide an in-box viewer solution.</span></span> <span data-ttu-id="931d3-110">定義標準活動事件，並為 Isv 提供自訂事件產生的擴充性。</span><span class="sxs-lookup"><span data-stu-id="931d3-110">Define standard activity events, and provide for extensibility to custom event generation by ISVs.</span></span>

-   <span data-ttu-id="931d3-111">升階使用者的所有監視和限制都只會依據家長或監護人的選擇來開啟。</span><span class="sxs-lookup"><span data-stu-id="931d3-111">Promote that all monitoring and restrictions for a user are turned on only on an opt-in basis by parents or guardians.</span></span> <span data-ttu-id="931d3-112">在可能的情況下，限制功能對於非控制的使用者應該完全非使用中，以將安全性和應用程式相容性風險降至最低。</span><span class="sxs-lookup"><span data-stu-id="931d3-112">Wherever possible, restrictions functionality should be completely inactive for non-controlled users to minimize security and application compatibility risks.</span></span>

-   <span data-ttu-id="931d3-113">在可能的情況下，Microsoft 應該盡可能地避免依年齡或受控制使用者的其他參數來做出價值的判斷， (協力廠商可能會選擇) 。</span><span class="sxs-lookup"><span data-stu-id="931d3-113">Microsoft shall strive, whenever possible, not to make value judgments by age or other parameters for the controlled user (third parties may choose to do so).</span></span> <span data-ttu-id="931d3-114">這類決策會留給家長或監護人，通常會受到團體或組織的影響。</span><span class="sxs-lookup"><span data-stu-id="931d3-114">Such decisions are left up to the parent or guardian, often influenced by communities or organizations.</span></span>

-   <span data-ttu-id="931d3-115">在產品中提供用於離線活動監控和限制的產品，其中有幾個或沒有任何供應專案可供使用，其中有相關聯的安全性風險功能可在產品中使用，或 Microsoft 解決方案提供功能強大的功能，與作業系統的設計完全整合。</span><span class="sxs-lookup"><span data-stu-id="931d3-115">Provide implementations in the product for offline activity monitoring and restrictions where few or no offerings are available today, where the associated safety-risk functionality is available in the product, or where a Microsoft solution provides capable and robust functionality fully integrated with the design of the operating system.</span></span>

-   <span data-ttu-id="931d3-116">一般來說，升級應用程式會執行自己的記錄和限制，以獲得最佳的內容和 UI 體驗。</span><span class="sxs-lookup"><span data-stu-id="931d3-116">Generally, promote that applications perform their own logging and restrictions for best context and UI experience.</span></span>

    <span data-ttu-id="931d3-117">例外狀況：在所選區域中提供完整的線上活動監視和限制，讓取用者和產業受益于成本。</span><span class="sxs-lookup"><span data-stu-id="931d3-117">Exception: Provide comprehensive online activity monitoring and restrictions in selected areas where the benefit to consumers and industry outweigh the costs.</span></span>

-   <span data-ttu-id="931d3-118">使用公用 Api 來公開家長監護使用者介面設定和活動事件定義，讓協力廠商可以查詢狀態、修改設定和讀取活動記錄（如果它們是以足夠的 Windows 帳戶許可權執行的話）。</span><span class="sxs-lookup"><span data-stu-id="931d3-118">Expose parental controls user interface settings and activity event definitions by using public APIs so that third parties may query for state, modify settings, and read activity logs if they are running with sufficient Windows account privileges.</span></span>

<span data-ttu-id="931d3-119">最主要的目標是要提升協力廠商家長監護解決方案與現成功能的共存，並藉由整合、擴充或提供適合的替代功能，支援增加價值。</span><span class="sxs-lookup"><span data-stu-id="931d3-119">An overarching goal is to promote third-party parental controls solutions' coexistence with the in-box functionality, and support adding value by integrating with, extending, or providing alternative capabilities where suitable.</span></span>

 

 



