---
description: 在呼叫端內容中強制啟用
ms.assetid: bb228f39-0e04-497a-8404-18f7bc027bea
title: 在呼叫端內容中強制啟用
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c70af40f92056e679a9211964b8a614cbeaeb4a6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991797"
---
# <a name="enforcing-activation-in-the-callers-context"></a><span data-ttu-id="24168-103">在呼叫端的內容中強制啟用</span><span class="sxs-lookup"><span data-stu-id="24168-103">Enforcing Activation in the Caller's Context</span></span>

<span data-ttu-id="24168-104">您可以控制物件是否會在其本身的內容中啟用。</span><span class="sxs-lookup"><span data-stu-id="24168-104">You can control whether an object gets activated in its own context.</span></span> <span data-ttu-id="24168-105">當您使用 [元件服務] 系統管理工具要求在呼叫端的內容中啟用元件時，當 COM + 在內容中啟動元件的實例時，會發生下列情況：</span><span class="sxs-lookup"><span data-stu-id="24168-105">When you use the Component Services administrative tool to require component activation in the caller's context, the following occurs when COM+ activates an instance of the component in a context:</span></span>

-   <span data-ttu-id="24168-106">如果可能的話，會在建立者的內容中啟用物件。</span><span class="sxs-lookup"><span data-stu-id="24168-106">The object is activated in the creator's context if possible.</span></span>
-   <span data-ttu-id="24168-107">如果物件需要自己的內容，則物件啟用會失敗;\_ \_ \_ \_ \_ \_ 會傳回建立外部用戶端 \_ 內容的共同電子嘗試。</span><span class="sxs-lookup"><span data-stu-id="24168-107">Object activation fails if it requires its own context; CO\_E\_ATTEMPT\_TO\_CREATE\_OUTSIDE\_CLIENT\_CONTEXT is returned.</span></span>

<span data-ttu-id="24168-108">物件是否需要自己的內容，取決於其設定是否相對於呼叫端內容屬性的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="24168-108">Whether or not the object requires its own context depends on its configuration relative to the current state of the caller's context properties.</span></span> <span data-ttu-id="24168-109">如需詳細資訊，請參閱 [Com +](com--contexts.md)內容。</span><span class="sxs-lookup"><span data-stu-id="24168-109">For more detail, see [COM+ Contexts](com--contexts.md).</span></span>

<span data-ttu-id="24168-110">如果物件有自己的內容，您會想要在該層級上控制啟用的程度。</span><span class="sxs-lookup"><span data-stu-id="24168-110">You would want to control activation at that fine a level if some aspect of your object would not function properly if it has its own context.</span></span> <span data-ttu-id="24168-111">例如，如果元件不支援封送處理，而它有自己的內容，則對其進行的任何呼叫都將會失敗，因為跨內容呼叫會被攔截並執行輕量封送處理。</span><span class="sxs-lookup"><span data-stu-id="24168-111">For example, if the component does not support marshaling and it has its own context, any calls to it will fail because cross-context calls are intercepted and a lightweight marshal performed.</span></span>

<span data-ttu-id="24168-112">**若要在呼叫端的內容中強制啟用**</span><span class="sxs-lookup"><span data-stu-id="24168-112">**To enforce activation in the caller's context**</span></span>

1.  <span data-ttu-id="24168-113">在 [元件服務] 系統管理工具的詳細資料窗格中，以滑鼠右鍵按一下元件 (位於任何選取的 COM + 應用) 程式的 [ **元件** ] 資料夾中（您要在其中設定啟用屬性），然後按一下 [ **屬性**]。</span><span class="sxs-lookup"><span data-stu-id="24168-113">In the details pane of the Component Services administrative tool, right-click the component (located within the **Components** folder of any selected COM+ application) for which you are setting activation properties and then click **Properties**.</span></span>

2.  <span data-ttu-id="24168-114">在 [元件屬性] 對話方塊中，按一下 [ **啟用** ] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="24168-114">In the component properties dialog box, click the **Activation** tab.</span></span>

3.  <span data-ttu-id="24168-115">選取 [ **必須在呼叫端內容中啟用** ] 核取方塊。</span><span class="sxs-lookup"><span data-stu-id="24168-115">Select the **Must be activated in the callers context** check box.</span></span>

4.  <span data-ttu-id="24168-116">按一下 [確定]  。</span><span class="sxs-lookup"><span data-stu-id="24168-116">Click **OK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="24168-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="24168-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24168-118">COM + 即時啟用概念</span><span class="sxs-lookup"><span data-stu-id="24168-118">COM+ Just-in-Time Activation Concepts</span></span>](com--just-in-time-activation-concepts.md)
</dt> <dt>

[<span data-ttu-id="24168-119">在預設內容中強制啟用</span><span class="sxs-lookup"><span data-stu-id="24168-119">Enforcing Activation in the Default Context</span></span>](enforcing-activation-in-the-default-context.md)
</dt> </dl>

 

 



