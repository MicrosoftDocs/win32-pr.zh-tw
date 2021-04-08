---
title: WinEvents 基礎結構
description: Microsoft Windows 作業系統包含一個稱為 WinEvents 的功能，可讓在 Windows 桌面上執行的進程和應用程式交換特定類型的資訊。
ms.assetid: ba97b00b-4a4c-4889-ae9c-8e92eb742849
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8846582a6d18f304cc08e3cb13ddb444cb278d7
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "103679544"
---
# <a name="winevents"></a><span data-ttu-id="923aa-103">WinEvents</span><span class="sxs-lookup"><span data-stu-id="923aa-103">WinEvents</span></span>

<span data-ttu-id="923aa-104">Microsoft Windows 作業系統包含一個稱為 *WinEvents* 的功能，可讓在 Windows 桌面上執行的進程和應用程式交換特定類型的資訊。</span><span class="sxs-lookup"><span data-stu-id="923aa-104">The Microsoft Windows operating system includes a feature, called *WinEvents*, that enables processes and applications running on the Windows desktop to exchange certain types of information.</span></span> <span data-ttu-id="923aa-105">使用 Microsoft 消費者介面自動化和 Microsoft Active Accessibility 的協助工具工具是 WinEvents 的主要使用者。</span><span class="sxs-lookup"><span data-stu-id="923aa-105">Accessibility tools that use Microsoft UI Automation and Microsoft Active Accessibility are among the primary users of the WinEvents.</span></span>

<span data-ttu-id="923aa-106">在協助工具的內容中，消費者介面自動化提供者和 Microsoft Active Accessibility 伺服器會使用 WinEvents 來通知用戶端應用程式 UI 中的變更，例如當 UI 元素建立或終結時，或專案名稱、狀態或值變更時。</span><span class="sxs-lookup"><span data-stu-id="923aa-106">In the context of accessibility, UI Automation providers and Microsoft Active Accessibility servers use WinEvents to notify clients of changes in an application UI, such as when a UI element has been created or destroyed, or when an element name, state, or value has changed.</span></span>

<span data-ttu-id="923aa-107">本節提供的建議、指導方針和範例可協助用戶端處理 WinEvents，以及協助伺服器判斷何時觸發適當的 New-winevent。</span><span class="sxs-lookup"><span data-stu-id="923aa-107">This section provides suggestions, guidelines, and examples to help clients handle WinEvents and to help servers determine when to trigger the appropriate WinEvent.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="923aa-108">本節內容</span><span class="sxs-lookup"><span data-stu-id="923aa-108">In this section</span></span>

-   [<span data-ttu-id="923aa-109">什麼是 WinEvents？</span><span class="sxs-lookup"><span data-stu-id="923aa-109">What Are WinEvents?</span></span>](what-are-winevents.md)
-   [<span data-ttu-id="923aa-110">註冊攔截函式</span><span class="sxs-lookup"><span data-stu-id="923aa-110">Registering a Hook Function</span></span>](registering-a-hook-function.md)
-   [<span data-ttu-id="923aa-111">系統層級和 Object-Level 事件</span><span class="sxs-lookup"><span data-stu-id="923aa-111">System-Level and Object-Level Events</span></span>](system-level-and-object-level-events.md)
-   [<span data-ttu-id="923aa-112">內容內部和跨內容攔截函式</span><span class="sxs-lookup"><span data-stu-id="923aa-112">In-Context and Out-of-Context Hook Functions</span></span>](in-context-and-out-of-context-hook-functions.md)
-   [<span data-ttu-id="923aa-113">防止在攔截函式中重新進入</span><span class="sxs-lookup"><span data-stu-id="923aa-113">Guarding Against Reentrancy in Hook Functions</span></span>](guarding-against-reentrancy-in-hook-functions.md)
-   [<span data-ttu-id="923aa-114">配置 New-winevent 識別碼</span><span class="sxs-lookup"><span data-stu-id="923aa-114">Allocation of WinEvent IDs</span></span>](allocation-of-winevent-ids.md)

<span data-ttu-id="923aa-115">如需 Microsoft Active Accessibility 中事件通知程式的總覽，請參閱[技術總覽](technical-overview.md)中的[WinEvents](winevents-overview.md) 。</span><span class="sxs-lookup"><span data-stu-id="923aa-115">For an overview of the event notification process in Microsoft Active Accessibility, see [WinEvents](winevents-overview.md) in the [Technical Overview](technical-overview.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="923aa-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="923aa-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="923aa-117">一般基礎結構</span><span class="sxs-lookup"><span data-stu-id="923aa-117">Common Infrastructure</span></span>](common-infrastructure.md)
</dt> </dl>

 

 




