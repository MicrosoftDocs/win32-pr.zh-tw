---
description: 具有至少一個 queuable 介面的元件是 queuable 元件。
ms.assetid: 8183f640-4bf3-4555-8837-90a26130c618
title: 建立 Queuable 元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03533168a24da1e1f7279a6f2108e25717054103
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104385931"
---
# <a name="creating-queuable-components"></a><span data-ttu-id="0faf9-103">建立 Queuable 元件</span><span class="sxs-lookup"><span data-stu-id="0faf9-103">Creating Queuable Components</span></span>

<span data-ttu-id="0faf9-104">具有至少一個 queuable 介面的元件是 *queuable 元件*。</span><span class="sxs-lookup"><span data-stu-id="0faf9-104">A component with at least one queuable interface is a *queuable component*.</span></span> <span data-ttu-id="0faf9-105">對於要由佇列叫用的元件，介面必須標示為 queuable，而且元件必須安裝在佇列應用程式中。</span><span class="sxs-lookup"><span data-stu-id="0faf9-105">For a component to be invoked by a queue, the interfaces must be marked as queuable and the component must be installed in a queued application.</span></span> <span data-ttu-id="0faf9-106">不過，queuable 元件可以是非佇列應用程式的元件。</span><span class="sxs-lookup"><span data-stu-id="0faf9-106">However, a queuable component can be a component of a non-queued application.</span></span>

<span data-ttu-id="0faf9-107">Queuable 介面必須只包含 in 參數-沒有 out 參數和傳回值。</span><span class="sxs-lookup"><span data-stu-id="0faf9-107">A queuable interface must contain only in parameters—no out parameters and no return values.</span></span> <span data-ttu-id="0faf9-108">這些特性是藉由在元件安裝期間分析類型資訊來進行驗證。</span><span class="sxs-lookup"><span data-stu-id="0faf9-108">These characteristics are verified by analyzing the type information during component installation.</span></span> <span data-ttu-id="0faf9-109">如果未 queuable 介面，則無法啟用包含元件之應用程式的佇列。</span><span class="sxs-lookup"><span data-stu-id="0faf9-109">If the interface is not queuable, the queue of the application containing the component cannot be activated.</span></span>

<span data-ttu-id="0faf9-110">若要將 COM + 介面指定為 queuable，請使用下列步驟：</span><span class="sxs-lookup"><span data-stu-id="0faf9-110">To specify a COM+ interface as queuable, use the following steps:</span></span>

1.  <span data-ttu-id="0faf9-111">在 [元件服務] 系統管理工具的主控台樹中，于 [ **元件服務**] 下，開啟與您要管理之電腦相關聯的 [ **Com + 應用程式** ] 資料夾。</span><span class="sxs-lookup"><span data-stu-id="0faf9-111">In the console tree of the Component Services administrative tool, under **Component Services**, open the **COM+ Applications** folder associated with the computer you wish to manage.</span></span>

2.  <span data-ttu-id="0faf9-112">開啟您想要進行 queuable 之 COM + 應用程式元件的 [ **介面** ] 資料夾。</span><span class="sxs-lookup"><span data-stu-id="0faf9-112">Open the **Interfaces** folder of the component of the COM+ application that you want to make queuable.</span></span>

3.  <span data-ttu-id="0faf9-113">以滑鼠右鍵按一下您要標示為 queuable 的介面，然後按一下 [ **屬性**]。</span><span class="sxs-lookup"><span data-stu-id="0faf9-113">Right-click the interface that you want to mark as queuable, and then click **Properties**.</span></span>

4.  <span data-ttu-id="0faf9-114">在 [屬性] 對話方塊中，選取 [ **佇列** ] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="0faf9-114">Select the **Queuing** tab in the properties dialog.</span></span>

5.  <span data-ttu-id="0faf9-115">啟用標示為已 **排入佇列** 的核取方塊。</span><span class="sxs-lookup"><span data-stu-id="0faf9-115">Activate the check box labeled **Queued**.</span></span>

    > [!Note]  
    > <span data-ttu-id="0faf9-116">如果 [已 **排入佇列** ] 核取方塊呈現灰色，則介面不符合上述的 queuable 條件約束。</span><span class="sxs-lookup"><span data-stu-id="0faf9-116">If the **Queued** check box is grayed out, the interface does not satisfy the queuable constraints described above.</span></span>

     

6.  <span data-ttu-id="0faf9-117">按一下 [確定]  。</span><span class="sxs-lookup"><span data-stu-id="0faf9-117">Click **OK**.</span></span>

    <span data-ttu-id="0faf9-118">Queuable 元件的識別方式是將 QUEUEABLE 屬性宏新增至介面定義語言的介面區段 (IDL) 原始程式檔，以取得 queuable 的所有介面。</span><span class="sxs-lookup"><span data-stu-id="0faf9-118">A queuable component can be identified as such by adding the QUEUEABLE attribute macro to the Interface section of the Interface Definition Language (IDL) source file for all interfaces that are queuable.</span></span>

    ``` syntax
#include "mtxattr.h"
    [ object, dual, uuid(), helpstring(IShiphip"), QUEUEABLE ]
    interface IShip:IDispatch{
       [propput, id(1)] HRESULT CustomerId ([in] long CustId);
       [propput, id(2)] HRESULT OrderId ([in] long OrderID);
       [id(3)] HRESULT LineItem ([in] long Qty);
       [id(4)] HRESULT Process ();
    }
    ```

## <a name="related-topics"></a><span data-ttu-id="0faf9-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="0faf9-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0faf9-120">建立元件佇列</span><span class="sxs-lookup"><span data-stu-id="0faf9-120">Creating Component Queues</span></span>](creating-component-queues.md)
</dt> <dt>

[<span data-ttu-id="0faf9-121">開發已排入佇列的元件</span><span class="sxs-lookup"><span data-stu-id="0faf9-121">Developing Queued Components</span></span>](developing-queued-components.md)
</dt> </dl>

 

 



