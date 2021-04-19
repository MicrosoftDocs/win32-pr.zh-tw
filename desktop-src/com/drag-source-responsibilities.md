---
title: 拖曳來源責任
description: 拖曳來源責任
ms.assetid: bafef0c1-f78e-424a-9ed0-07764a60b22d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45ce91a795815148f442c19530a552cf7c843332
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "106978585"
---
# <a name="drag-source-responsibilities"></a><span data-ttu-id="1616a-103">拖曳來源責任</span><span class="sxs-lookup"><span data-stu-id="1616a-103">Drag Source Responsibilities</span></span>

<span data-ttu-id="1616a-104">拖曳來源負責下列工作：</span><span class="sxs-lookup"><span data-stu-id="1616a-104">The drag source is responsible for the following tasks:</span></span>

-   <span data-ttu-id="1616a-105">針對公開 [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) 和 [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) 介面的放置目標提供資料傳輸物件。</span><span class="sxs-lookup"><span data-stu-id="1616a-105">Providing a data-transfer object for the drop target that exposes the [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) and [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) interfaces.</span></span>
-   <span data-ttu-id="1616a-106">正在產生指標和來源意見反應。</span><span class="sxs-lookup"><span data-stu-id="1616a-106">Generating pointer and source feedback.</span></span>
-   <span data-ttu-id="1616a-107">判斷何時取消拖曳作業或發生卸載作業。</span><span class="sxs-lookup"><span data-stu-id="1616a-107">Determining when the drag operation has been canceled or a drop operation has occurred.</span></span>
-   <span data-ttu-id="1616a-108">針對卸載作業所造成的原始資料執行任何動作，例如刪除資料或建立其連結。</span><span class="sxs-lookup"><span data-stu-id="1616a-108">Performing any action on the original data caused by the drop operation, such as deleting the data or creating a link to it.</span></span>

<span data-ttu-id="1616a-109">主要工作是建立可公開 [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) 和 [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) 介面的資料傳輸物件。</span><span class="sxs-lookup"><span data-stu-id="1616a-109">The main task is creating a data-transfer object that exposes the [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) and [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) interfaces.</span></span> <span data-ttu-id="1616a-110">拖曳來源可能包含或可能不包含所選資料的複本。</span><span class="sxs-lookup"><span data-stu-id="1616a-110">The drag source might or might not include a copy of the selected data.</span></span> <span data-ttu-id="1616a-111">包括它並非強制性的，但這麼做可協助防止意外的變更，並允許剪貼簿作業程式碼與拖放程式碼相同。</span><span class="sxs-lookup"><span data-stu-id="1616a-111">Including it is not mandatory, but doing so helps protect against inadvertent changes and allows the Clipboard operations code to be identical to the drag and drop code.</span></span>

<span data-ttu-id="1616a-112">當拖曳作業正在進行時，拖曳來源會負責設定滑鼠指標，並在適當的情況下，為使用者提供其他來源意見反應。</span><span class="sxs-lookup"><span data-stu-id="1616a-112">While a drag operation is in progress, the drag source is responsible for setting the mouse pointer and, if appropriate, for providing additional source feedback to the user.</span></span> <span data-ttu-id="1616a-113">拖曳來源無法提供任何追蹤滑鼠位置的意見反應，而不是實際設定實際指標 (查看 [**SetCursor**](/windows/win32/api/winuser/nf-winuser-setcursor) 函數) 。</span><span class="sxs-lookup"><span data-stu-id="1616a-113">The drag source cannot provide any feedback that tracks the mouse position other than by actually setting the real pointer (see the [**SetCursor**](/windows/win32/api/winuser/nf-winuser-setcursor) function).</span></span> <span data-ttu-id="1616a-114">必須強制執行此規則，以避免與放置目標所提供的意見反應衝突。</span><span class="sxs-lookup"><span data-stu-id="1616a-114">This rule must be enforced to avoid conflicts with the feedback provided by the drop target.</span></span> <span data-ttu-id="1616a-115"> (拖曳來源也可以是放置目標。</span><span class="sxs-lookup"><span data-stu-id="1616a-115">(A drag source can also be a drop target.</span></span> <span data-ttu-id="1616a-116">在卸載本身時，來源/目標當然可以提供目標意見反應來追蹤滑鼠的位置。</span><span class="sxs-lookup"><span data-stu-id="1616a-116">When dropping on itself, the source/target can, of course, provide target feedback to track the mouse position.</span></span> <span data-ttu-id="1616a-117">不過，在這種情況下，它是追蹤滑鼠，而不是來源的放置目標。 ) 根據放置目標所提供的意見反應，來源會設定適當的指標。</span><span class="sxs-lookup"><span data-stu-id="1616a-117">In this case, however, it is the drop target tracking the mouse, not the source.) Based on the feedback offered by the drop target, the source sets an appropriate pointer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1616a-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="1616a-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1616a-119">拖放功能</span><span class="sxs-lookup"><span data-stu-id="1616a-119">Drag and Drop</span></span>](drag-and-drop.md)
</dt> </dl>

 

 