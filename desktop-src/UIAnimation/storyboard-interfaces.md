---
title: 分鏡指令碼介面
description: 本節包含支援分鏡腳本的 Windows 動畫管理員介面參考規格。
ms.assetid: 372D6348-3DF2-48EB-B495-BAD4E5DAAAD3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fba60c480ef4c316731da6eefbe5334616a72b5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023664"
---
# <a name="storyboard-interfaces"></a><span data-ttu-id="19147-103">分鏡指令碼介面</span><span class="sxs-lookup"><span data-stu-id="19147-103">Storyboard Interfaces</span></span>

<span data-ttu-id="19147-104">本節包含支援分鏡腳本的 Windows 動畫管理員介面參考規格。</span><span class="sxs-lookup"><span data-stu-id="19147-104">This section contains the reference specifications for the Windows Animation Manager interfaces that support storyboards.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="19147-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="19147-105">In this section</span></span>



| <span data-ttu-id="19147-106">主題</span><span class="sxs-lookup"><span data-stu-id="19147-106">Topic</span></span>                                                                                                 | <span data-ttu-id="19147-107">描述</span><span class="sxs-lookup"><span data-stu-id="19147-107">Description</span></span>                                                                                                           |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="19147-108">**IUIAnimationStoryboard**</span><span class="sxs-lookup"><span data-stu-id="19147-108">**IUIAnimationStoryboard**</span></span>](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationstoryboard)<br/>                                   | <span data-ttu-id="19147-109">定義分鏡腳本，其中包含一組相對於彼此同步的轉換。</span><span class="sxs-lookup"><span data-stu-id="19147-109">Defines a storyboard, which contains a group of transitions that are synchronized relative to one another.</span></span><br/> |
| [<span data-ttu-id="19147-110">**IUIAnimationStoryboard2**</span><span class="sxs-lookup"><span data-stu-id="19147-110">**IUIAnimationStoryboard2**</span></span>](/windows/win32/api/uianimation/nn-uianimation-iuianimationstoryboard2)<br/>                                 | <span data-ttu-id="19147-111">定義分鏡腳本，其中包含一組相對於彼此同步的轉換。</span><span class="sxs-lookup"><span data-stu-id="19147-111">Defines a storyboard, which contains a group of transitions that are synchronized relative to one another.</span></span><br/> |
| [<span data-ttu-id="19147-112">**IUIAnimationStoryboardEventHandler**</span><span class="sxs-lookup"><span data-stu-id="19147-112">**IUIAnimationStoryboardEventHandler**</span></span>](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationstoryboardeventhandler)<br/>           | <span data-ttu-id="19147-113">定義處理分鏡腳本狀態和更新事件的方法。</span><span class="sxs-lookup"><span data-stu-id="19147-113">Defines methods for handling status and update events for a storyboard.</span></span><br/>                                    |
| [<span data-ttu-id="19147-114">**IUIAnimationStoryboardEventHandler2**</span><span class="sxs-lookup"><span data-stu-id="19147-114">**IUIAnimationStoryboardEventHandler2**</span></span>](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationstoryboardeventhandler2)<br/>         | <span data-ttu-id="19147-115">定義處理分鏡腳本事件的方法。</span><span class="sxs-lookup"><span data-stu-id="19147-115">Defines methods for handling storyboard events.</span></span> <br/>                                                           |
| [<span data-ttu-id="19147-116">**IUIAnimationLoopIterationChangeHandler2**</span><span class="sxs-lookup"><span data-stu-id="19147-116">**IUIAnimationLoopIterationChangeHandler2**</span></span>](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationloopiterationchangehandler2)<br/> | <span data-ttu-id="19147-117">定義處理分鏡腳本迴圈反復專案事件的方法。</span><span class="sxs-lookup"><span data-stu-id="19147-117">Defines a method for handling storyboard loop iteration events.</span></span><br/>                                            |
| [<span data-ttu-id="19147-118">**IUIAnimationPriorityComparison**</span><span class="sxs-lookup"><span data-stu-id="19147-118">**IUIAnimationPriorityComparison**</span></span>](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationprioritycomparison)<br/>                   | <span data-ttu-id="19147-119">定義優先順序比較的方法，動畫管理員會使用此方法來解決排程衝突。</span><span class="sxs-lookup"><span data-stu-id="19147-119">Defines a method for priority comparison that the animation manager uses to resolve scheduling conflicts.</span></span><br/>  |
| [<span data-ttu-id="19147-120">**IUIAnimationPriorityComparison2**</span><span class="sxs-lookup"><span data-stu-id="19147-120">**IUIAnimationPriorityComparison2**</span></span>](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationprioritycomparison2)<br/>                 | <span data-ttu-id="19147-121">定義方法，透過優先權比較來解決排程衝突。</span><span class="sxs-lookup"><span data-stu-id="19147-121">Defines a method that resolves scheduling conflicts through priority comparison.</span></span><br/>                           |



 

## <a name="related-topics"></a><span data-ttu-id="19147-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="19147-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19147-123">介面</span><span class="sxs-lookup"><span data-stu-id="19147-123">Interfaces</span></span>](windows-animation-reference.md)
</dt> </dl>

 

