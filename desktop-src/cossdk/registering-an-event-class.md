---
description: 如此一來，訂閱者就可以找到事件類別並訂閱它，事件類別必須在 COM + 類別目錄中註冊。
ms.assetid: b9d59b9d-52ba-4c71-9226-9cb5b93ec3d4
title: 註冊事件類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89a5968b8cb5981db3eb39c446104e1801a18e2e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103688823"
---
# <a name="registering-an-event-class"></a><span data-ttu-id="46871-103">註冊事件類別</span><span class="sxs-lookup"><span data-stu-id="46871-103">Registering an Event Class</span></span>

<span data-ttu-id="46871-104">如此一來，訂閱者就可以找到事件類別並訂閱它，事件類別必須在 COM + 類別目錄中註冊。</span><span class="sxs-lookup"><span data-stu-id="46871-104">So that subscribers can find an event class and subscribe to it, event classes must be registered in the COM+ catalog.</span></span> <span data-ttu-id="46871-105">COM + 需要一個描述事件介面和方法的類型程式庫，讓它能夠適當地比對和連接訂閱者和發行者。</span><span class="sxs-lookup"><span data-stu-id="46871-105">COM+ requires a type library that describes the event interfaces and methods so that it can properly match and connect subscribers and publishers.</span></span> <span data-ttu-id="46871-106">類型程式庫必須位於或隨附于自行註冊的 DLL。</span><span class="sxs-lookup"><span data-stu-id="46871-106">The type library must reside in or be accompanied by a self-registering DLL.</span></span>

<span data-ttu-id="46871-107">您可以使用 [元件服務] 系統管理工具或 COM + 系統管理功能，在 COM + 類別目錄中註冊事件類別。</span><span class="sxs-lookup"><span data-stu-id="46871-107">You can use the Component Services administrative tool or the COM+ Administrative functions to register an event class in the COM+ catalog.</span></span>

<span data-ttu-id="46871-108">**使用元件服務系統管理工具註冊事件類別**</span><span class="sxs-lookup"><span data-stu-id="46871-108">**To register an event class with the Component Services administrative tool**</span></span>

1.  <span data-ttu-id="46871-109">建立新的 COM+ 應用程式。</span><span class="sxs-lookup"><span data-stu-id="46871-109">Create a new COM+ application.</span></span>

2.  <span data-ttu-id="46871-110">開啟應用程式資料夾，然後選取 [ **元件**]。</span><span class="sxs-lookup"><span data-stu-id="46871-110">Open the application folder and select **Components**.</span></span>

3.  <span data-ttu-id="46871-111">在 [ **動作** ] 功能表上，按一下 [ **新增**]。</span><span class="sxs-lookup"><span data-stu-id="46871-111">On the **Action** menu, click **New**.</span></span> <span data-ttu-id="46871-112"> (您也可以選取 [ **元件** ] 資料夾、按一下滑鼠右鍵、指向 [ **新增**]，然後按一下 [ **元件**]。 ) </span><span class="sxs-lookup"><span data-stu-id="46871-112">(You can also select the **Components** folder, right-click, point to **New**, and then click **Component**.)</span></span>

4.  <span data-ttu-id="46871-113">按一下 [ **安裝新的事件類別 (es])**。</span><span class="sxs-lookup"><span data-stu-id="46871-113">Click **Install new event class(es)**.</span></span>

5.  <span data-ttu-id="46871-114">輸入事件類別元件 DLL 的路徑。</span><span class="sxs-lookup"><span data-stu-id="46871-114">Enter the path to the event class component DLL.</span></span>

6.  <span data-ttu-id="46871-115">按一下 [確定]  。</span><span class="sxs-lookup"><span data-stu-id="46871-115">Click **OK**.</span></span>

<span data-ttu-id="46871-116">事件類別會在 COM + 目錄中註冊，並可由有興趣取得事件類別所提供之資訊的訂閱者找到。</span><span class="sxs-lookup"><span data-stu-id="46871-116">The event class is registered in the COM+ catalog and can be located by subscribers interested in obtaining the information provided by the event class.</span></span> <span data-ttu-id="46871-117">如需如何使用 COM + 系統管理介面註冊事件類別的詳細資訊，請參閱 [**ICOMAdminCatalog：： InstallEventClass**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installeventclass)。</span><span class="sxs-lookup"><span data-stu-id="46871-117">For information about how to register the event class by using the COM+ administrative interfaces, see [**ICOMAdminCatalog::InstallEventClass**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installeventclass).</span></span>

## <a name="related-topics"></a><span data-ttu-id="46871-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="46871-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="46871-119">註冊訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="46871-119">Registering a Subscription</span></span>](registering-a-subscription.md)
</dt> </dl>

 

 



