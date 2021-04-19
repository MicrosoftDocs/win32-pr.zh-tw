---
title: 拖放
description: 拖放指的是使用滑鼠或其他指標裝置來指定資料來源和其目的地的資料傳輸。
ms.assetid: bba0ddf8-fcf9-4827-bf85-7ac597d33b4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dc4b425637432024d097acb8afdc5e169467c6a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106995551"
---
# <a name="drag-and-drop"></a><span data-ttu-id="59f19-103">拖放</span><span class="sxs-lookup"><span data-stu-id="59f19-103">Drag and Drop</span></span>

<span data-ttu-id="59f19-104">*拖放* 指的是使用滑鼠或其他指標裝置來指定資料來源和其目的地的資料傳輸。</span><span class="sxs-lookup"><span data-stu-id="59f19-104">*Drag and drop* refers to data transfers in which a mouse or other pointing device is used to specify both the data source and its destination.</span></span> <span data-ttu-id="59f19-105">在典型的拖放作業中，使用者會選取要傳送的物件，方法是將滑鼠指標移至該物件，然後按住左鍵或針對此用途指定的其他按鈕。</span><span class="sxs-lookup"><span data-stu-id="59f19-105">In a typical drag and drop operation, a user selects the object to be transferred by moving the mouse pointer to it and holding down either the left button or some other button designated for this purpose.</span></span> <span data-ttu-id="59f19-106">當繼續按住按鈕時，使用者可以藉由將物件拖曳至其目的地（可以是任何 OLE 容器）來起始轉移。</span><span class="sxs-lookup"><span data-stu-id="59f19-106">While continuing to hold down the button, the user initiates the transfer by dragging the object to its destination, which can be any OLE container.</span></span> <span data-ttu-id="59f19-107">拖放功能提供與 OLE 剪貼簿複製並貼上完全相同的功能，但新增了視覺效果的意見反應，並免除了功能表的需求。</span><span class="sxs-lookup"><span data-stu-id="59f19-107">Drag and drop provides exactly the same functionality as the OLE clipboard copy and paste but adds visual feedback and eliminates the need for menus.</span></span> <span data-ttu-id="59f19-108">事實上，如果應用程式支援剪貼簿複製並貼上，則需要額外的額外部分才能支援拖放。</span><span class="sxs-lookup"><span data-stu-id="59f19-108">In fact, if an application supports clipboard copy and paste, little extra is needed to support drag and drop.</span></span>

<span data-ttu-id="59f19-109">在 OLE 拖放作業期間，會使用下列三個不同的程式碼片段。</span><span class="sxs-lookup"><span data-stu-id="59f19-109">During an OLE drag and drop operation, the following three separate pieces of code are used.</span></span>



| <span data-ttu-id="59f19-110">拖放程式碼來源</span><span class="sxs-lookup"><span data-stu-id="59f19-110">Drag-and-drop code source</span></span>                               | <span data-ttu-id="59f19-111">執行和使用</span><span class="sxs-lookup"><span data-stu-id="59f19-111">Implementation and use</span></span>                                                                                                                                                                      |
|---------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59f19-112">[**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) 介面</span><span class="sxs-lookup"><span data-stu-id="59f19-112">[**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) interface</span></span><br/> | <span data-ttu-id="59f19-113">由包含拖曳資料的物件所執行，稱為 *拖曳來源*。</span><span class="sxs-lookup"><span data-stu-id="59f19-113">Implemented by the object containing the dragged data, referred to as the *drag source*.</span></span><br/>                                                                                         |
| <span data-ttu-id="59f19-114">[**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget) 介面</span><span class="sxs-lookup"><span data-stu-id="59f19-114">[**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget) interface</span></span><br/> | <span data-ttu-id="59f19-115">由預期接受卸載的物件所實，稱為「卸載目標」（ *drop target*）。</span><span class="sxs-lookup"><span data-stu-id="59f19-115">Implemented by the object that is intended to accept the drop, referred to as the *drop target*.</span></span><br/>                                                                                 |
| <span data-ttu-id="59f19-116">[**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop) 函式</span><span class="sxs-lookup"><span data-stu-id="59f19-116">[**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop) function</span></span><br/>    | <span data-ttu-id="59f19-117">由 OLE 所執行，可用來起始拖放作業。</span><span class="sxs-lookup"><span data-stu-id="59f19-117">Implemented by OLE and used to initiate a drag and drop operation.</span></span> <span data-ttu-id="59f19-118">作業進行之後，它會促進拖曳來源與放置目標之間的通訊。</span><span class="sxs-lookup"><span data-stu-id="59f19-118">After the operation is in progress, it facilitates communication between the drag source and the drop target.</span></span><br/> |



 

<span data-ttu-id="59f19-119">[**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource)和 [**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget)介面可以在容器或物件應用程式中實作為。</span><span class="sxs-lookup"><span data-stu-id="59f19-119">The [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) and [**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget) interfaces can be implemented in either a container or in an object application.</span></span> <span data-ttu-id="59f19-120">拖曳來源或卸載目標的角色不限於任何一種類型的 OLE 應用程式。</span><span class="sxs-lookup"><span data-stu-id="59f19-120">The role of drag source or drop target is not limited to any one type of OLE application.</span></span>

<span data-ttu-id="59f19-121">OLE 函式 [**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop) 會執行迴圈來追蹤滑鼠和鍵盤的移動，直到拖曳取消或發生卸載時為止。</span><span class="sxs-lookup"><span data-stu-id="59f19-121">The OLE function [**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop) implements a loop that tracks mouse and keyboard movement until such time as the drag is canceled or a drop occurs.</span></span> <span data-ttu-id="59f19-122">**DoDragDrop** 是拖放程式中的主要功能，可加速拖曳來源和放置目標之間的通訊。</span><span class="sxs-lookup"><span data-stu-id="59f19-122">**DoDragDrop** is the key function in the drag and drop process, facilitating communication between the drag source and drop target.</span></span>

<span data-ttu-id="59f19-123">在拖放作業期間，會向使用者顯示三種類型的意見反應。</span><span class="sxs-lookup"><span data-stu-id="59f19-123">During a drag and drop operation, three types of feedback can be displayed to the user.</span></span>



| <span data-ttu-id="59f19-124">意見反應類型</span><span class="sxs-lookup"><span data-stu-id="59f19-124">Type of feedback</span></span>            | <span data-ttu-id="59f19-125">Description</span><span class="sxs-lookup"><span data-stu-id="59f19-125">Description</span></span>                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59f19-126">來源意見反應</span><span class="sxs-lookup"><span data-stu-id="59f19-126">Source feedback</span></span><br/>  | <span data-ttu-id="59f19-127">在拖曳來源提供的情況下，來源意見反應會指出資料正在拖曳，而且在拖曳過程中不會變更。</span><span class="sxs-lookup"><span data-stu-id="59f19-127">Provided by the drag source, the source feedback indicates the data is being dragged and does not change during the course of the drag.</span></span> <span data-ttu-id="59f19-128">一般而言，資料會反白顯示，以表示已選取該資料。</span><span class="sxs-lookup"><span data-stu-id="59f19-128">Typically, the data is highlighted to signal it has been selected.</span></span><br/>                                                                                                                                            |
| <span data-ttu-id="59f19-129">指標意見反應</span><span class="sxs-lookup"><span data-stu-id="59f19-129">Pointer feedback</span></span><br/> | <span data-ttu-id="59f19-130">指標意見反應是由拖曳來源提供，指出當滑鼠在任何指定時間放開時，會發生什麼事。</span><span class="sxs-lookup"><span data-stu-id="59f19-130">Provided by the drag source, the pointer feedback indicates what happens if the mouse is released at any given moment.</span></span> <span data-ttu-id="59f19-131">指標意見反應會在使用者移動滑鼠和/或按下輔助按鍵時持續變更。</span><span class="sxs-lookup"><span data-stu-id="59f19-131">Pointer feedback changes continually as the user moves the mouse and/or presses a modifier key.</span></span> <span data-ttu-id="59f19-132">例如，如果指標移至無法接受 drop 的視窗，指標會變成「不允許」符號。</span><span class="sxs-lookup"><span data-stu-id="59f19-132">For example, if the pointer is moved into a window that cannot accept a drop, the pointer changes to the "not allowed" symbol.</span></span><br/> |
| <span data-ttu-id="59f19-133">目標意見反應</span><span class="sxs-lookup"><span data-stu-id="59f19-133">Target feedback</span></span><br/>  | <span data-ttu-id="59f19-134">由放置目標提供，目標意見反應會指出放置的發生位置。</span><span class="sxs-lookup"><span data-stu-id="59f19-134">Provided by the drop target, target feedback indicates where the drop is to occur.</span></span><br/>                                                                                                                                                                                                                                                                    |



 

<span data-ttu-id="59f19-135">如需詳細資訊，請參閱 [拖曳來源責任](drag-source-responsibilities.md)。</span><span class="sxs-lookup"><span data-stu-id="59f19-135">For more information, see [Drag Source Responsibilities](drag-source-responsibilities.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="59f19-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="59f19-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59f19-137">資料轉送</span><span class="sxs-lookup"><span data-stu-id="59f19-137">Data Transfer</span></span>](data-transfer.md)
</dt> </dl>

 

 





