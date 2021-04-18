---
title: Windows 動畫工作
description: 本節所包含的主題說明使用 Windows 動畫管理員的應用程式所需的基本工作。
ms.assetid: 28103e5e-f00a-4ff5-820b-ece24a7ef21a
keywords:
- Windows 動畫視窗動畫，工作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a2007e53a738494e9b143b3aa8a6cf83290acb1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965812"
---
# <a name="windows-animation-tasks"></a><span data-ttu-id="efe66-104">Windows 動畫工作</span><span class="sxs-lookup"><span data-stu-id="efe66-104">Windows Animation Tasks</span></span>

<span data-ttu-id="efe66-105">本節所包含的主題說明使用 Windows 動畫管理員的應用程式所需的基本工作。</span><span class="sxs-lookup"><span data-stu-id="efe66-105">The topics contained in this section describe the basic tasks required of applications that use Windows Animation Manager.</span></span>

<span data-ttu-id="efe66-106">這些工作（依順序）包括：</span><span class="sxs-lookup"><span data-stu-id="efe66-106">These tasks, in order, include:</span></span>

## <a name="in-this-section"></a><span data-ttu-id="efe66-107">本節內容</span><span class="sxs-lookup"><span data-stu-id="efe66-107">In this section</span></span>



| <span data-ttu-id="efe66-108">主題</span><span class="sxs-lookup"><span data-stu-id="efe66-108">Topic</span></span>                                                                                                | <span data-ttu-id="efe66-109">描述</span><span class="sxs-lookup"><span data-stu-id="efe66-109">Description</span></span>                                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="efe66-110">建立主要動畫物件</span><span class="sxs-lookup"><span data-stu-id="efe66-110">Create the Main Animation Objects</span></span>](adding-animation-to-an-application.md)<br/>               | <span data-ttu-id="efe66-111">若要在您的應用程式中使用 Windows 動畫，第一個步驟就是建立一組小型的主要動畫物件。</span><span class="sxs-lookup"><span data-stu-id="efe66-111">To use Windows Animation in your application, the first step is to create a small set of main animation objects.</span></span><br/>                                                                                                                                                                           |
| [<span data-ttu-id="efe66-112">建立動畫變數</span><span class="sxs-lookup"><span data-stu-id="efe66-112">Create Animation Variables</span></span>](create-animation-variables.md)<br/>                              | <span data-ttu-id="efe66-113">應用程式必須針對每個要使用 Windows 動畫製作動畫的視覺特性建立動畫變數。</span><span class="sxs-lookup"><span data-stu-id="efe66-113">An application must create an animation variable for each visual characteristic that is to be animated using Windows Animation.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="efe66-114">更新動畫管理員並繪製畫面格</span><span class="sxs-lookup"><span data-stu-id="efe66-114">Update the Animation Manager and Draw Frames</span></span>](introducing-windows-animation-manager.md)<br/> | <span data-ttu-id="efe66-115">每次應用程式排程分鏡腳本時，應用程式都必須提供目前的時間給動畫管理員。</span><span class="sxs-lookup"><span data-stu-id="efe66-115">Each time an application schedules a storyboard, the application must supply the current time to the animation manager.</span></span> <span data-ttu-id="efe66-116">當您導向動畫管理員以更新其狀態，並將所有動畫變數設定為適當的插入值時，也需要目前的時間。</span><span class="sxs-lookup"><span data-stu-id="efe66-116">The current time is also required when directing the animation manager to update its state and set all animation variables to the appropriate interpolated values.</span></span><br/> |
| [<span data-ttu-id="efe66-117">讀取動畫變數值</span><span class="sxs-lookup"><span data-stu-id="efe66-117">Read the Animation Variable Values</span></span>](updating---application-driven-animation.md)<br/>         | <span data-ttu-id="efe66-118">每次您的應用程式繪製時，都應該讀取代表要進行動畫之視覺特性的動畫變數目前的值。</span><span class="sxs-lookup"><span data-stu-id="efe66-118">Each time your application paints, it should read the current values of the animation variables that represent the visual characteristics to be animated.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="efe66-119">建立分鏡腳本並新增轉換</span><span class="sxs-lookup"><span data-stu-id="efe66-119">Create a Storyboard and Add Transitions</span></span>](updating---timer-driven-animation.md)<br/>          | <span data-ttu-id="efe66-120">若要建立動畫，應用程式必須建立分鏡腳本。</span><span class="sxs-lookup"><span data-stu-id="efe66-120">To create an animation, an application must construct a storyboard.</span></span><br/>                                                                                                                                                                                                                        |
| [<span data-ttu-id="efe66-121">排程分鏡腳本</span><span class="sxs-lookup"><span data-stu-id="efe66-121">Schedule a Storyboard</span></span>](scheduling-a-storyboard.md)<br/>                                      | <span data-ttu-id="efe66-122">建立分鏡腳本之後，動畫管理員會進行排程。</span><span class="sxs-lookup"><span data-stu-id="efe66-122">After a storyboard is created, it is scheduled by the animation manager.</span></span><br/>                                                                                                                                                                                                                   |



 

## <a name="related-topics"></a><span data-ttu-id="efe66-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="efe66-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="efe66-124">Windows 動畫總覽</span><span class="sxs-lookup"><span data-stu-id="efe66-124">Windows Animation Overview</span></span>](scenic-animation-api-overview.md)
</dt> <dt>

[<span data-ttu-id="efe66-125">Windows 動畫參考</span><span class="sxs-lookup"><span data-stu-id="efe66-125">Windows Animation Reference</span></span>](windows-animation-reference.md)
</dt> <dt>

[<span data-ttu-id="efe66-126">Windows 動畫範例</span><span class="sxs-lookup"><span data-stu-id="efe66-126">Windows Animation Samples</span></span>](windows-animation-samples.md)
</dt> </dl>

 

 





