---
title: '常數 (Windows 動畫參考) '
description: Windows 動畫管理員所定義之常數和列舉的參考檔集。
ms.assetid: c590cf68-28ce-4d7d-949d-2683ece3c12d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef2cceae981ea7cc0e2b78d9dadbea88075eb3ad
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "106967937"
---
# <a name="constants-windows-animation-reference"></a><span data-ttu-id="675eb-103">常數 (Windows 動畫參考) </span><span class="sxs-lookup"><span data-stu-id="675eb-103">Constants (Windows Animation Reference)</span></span>

<span data-ttu-id="675eb-104">Windows 動畫管理員所定義之常數和列舉的參考檔集。</span><span class="sxs-lookup"><span data-stu-id="675eb-104">Reference documentation for constants and enumerations defined by the Windows Animation Manager.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="675eb-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="675eb-105">In this section</span></span>



| <span data-ttu-id="675eb-106">主題</span><span class="sxs-lookup"><span data-stu-id="675eb-106">Topic</span></span>                                                                                                                             | <span data-ttu-id="675eb-107">描述</span><span class="sxs-lookup"><span data-stu-id="675eb-107">Description</span></span>                                                                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="675eb-108">**UI \_ 動畫 \_ 維度 \_ 未知**</span><span class="sxs-lookup"><span data-stu-id="675eb-108">**UI\_ANIMATION\_DIMENSION\_UNKNOWN**</span></span>](ui-animation-dimension-unknown.md)<br/>                                            | <span data-ttu-id="675eb-109">表示無法抓取要求的維度。</span><span class="sxs-lookup"><span data-stu-id="675eb-109">Indicates that the requested dimension cannot be retrieved.</span></span><br/>                                                                                                                                                                                                     |
| [<span data-ttu-id="675eb-110">**UI \_ 動畫 \_ 反復專案 \_ 無**</span><span class="sxs-lookup"><span data-stu-id="675eb-110">**UI\_ANIMATION\_ITERATION\_NONE**</span></span>](-ui-animation-iteration-none.md)<br/>                                                 | <span data-ttu-id="675eb-111">表示這是指定迴圈中的初始專案。</span><span class="sxs-lookup"><span data-stu-id="675eb-111">Indicates that this is the initial entry into a given loop.</span></span><br/>                                                                                                                                                                                                     |
| <span data-ttu-id="675eb-112">[**UI 動畫主要畫面格 \_ \_ \_ \_ 開始**](/previous-versions/windows/desktop/legacy/dd756780(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="675eb-112">[**UI\_ANIMATION\_KEYFRAME\_STORYBOARD\_START**](/previous-versions/windows/desktop/legacy/dd756780(v=vs.85))</span></span><br/>                           | <span data-ttu-id="675eb-113">表示每個分鏡腳本開頭的隱含主要畫面格。</span><span class="sxs-lookup"><span data-stu-id="675eb-113">Represents the implicit keyframe at the start of every storyboard.</span></span><br/>                                                                                                                                                                                              |
| [<span data-ttu-id="675eb-114">**UI \_ 動畫 \_ \_ 無限期重複**</span><span class="sxs-lookup"><span data-stu-id="675eb-114">**UI\_ANIMATION\_REPEAT\_INDEFINITELY**</span></span>](ui-animation-repeat-indefinitely.md)<br/>                                        | <span data-ttu-id="675eb-115">表示在呼叫 [**IUIAnimationStoryboard：：**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-conclude) until 方法之前，分鏡腳本中兩個主要畫面格之間的間隔應無限期重複。</span><span class="sxs-lookup"><span data-stu-id="675eb-115">Indicates that the interval between two keyframes in a storyboard should repeat indefinitely until the [**IUIAnimationStoryboard::Conclude**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-conclude) method is called.</span></span><br/>                                                            |
| [<span data-ttu-id="675eb-116">**UI \_ 動畫 \_ 會 \_ \_ \_ 在結束時無限期地重複 \_ 結束**</span><span class="sxs-lookup"><span data-stu-id="675eb-116">**UI\_ANIMATION\_REPEAT\_INDEFINITELY\_CONCLUDE\_AT\_END**</span></span>](ui-animation-repeat-indefinitely-conclude-at-end.md)<br/>     | <span data-ttu-id="675eb-117">表示在呼叫 [**IUIAnimationStoryboard：：**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-conclude) until 方法時，分鏡腳本中兩個主要畫面格之間的間隔應無限期地重複直到結束主要畫面上的主要畫面格迴圈結束。</span><span class="sxs-lookup"><span data-stu-id="675eb-117">Indicates that the interval between two keyframes in a storyboard should repeat indefinitely until the keyframe loop terminates on the ending keyframe when the [**IUIAnimationStoryboard::Conclude**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-conclude) method is called.</span></span><br/>   |
| [<span data-ttu-id="675eb-118">**UI \_ 動畫 \_ 會 \_ \_ \_ 在開始時無限期地重複結束 \_**</span><span class="sxs-lookup"><span data-stu-id="675eb-118">**UI\_ANIMATION\_REPEAT\_INDEFINITELY\_CONCLUDE\_AT\_START**</span></span>](ui-animation-repeat-indefinitely-conclude-at-start.md)<br/> | <span data-ttu-id="675eb-119">表示在呼叫 [**IUIAnimationStoryboard：：**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-conclude) until 方法時，分鏡腳本中兩個主要畫面格之間的間隔應無限期地重複直到開始的主要畫面格上的主要畫面格迴圈結束。</span><span class="sxs-lookup"><span data-stu-id="675eb-119">Indicates that the interval between two keyframes in a storyboard should repeat indefinitely until the keyframe loop terminates on the starting keyframe when the [**IUIAnimationStoryboard::Conclude**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-conclude) method is called.</span></span><br/> |
| [<span data-ttu-id="675eb-120">**\_最終 UI 動畫的 \_ 秒數 \_**</span><span class="sxs-lookup"><span data-stu-id="675eb-120">**UI\_ANIMATION\_SECONDS\_EVENTUALLY**</span></span>](ui-animation-seconds-eventually.md)<br/>                                          | <span data-ttu-id="675eb-121">指出 Windows 動畫可能會盡可能延遲已排程的分鏡腳本開始時間，以避免排程衝突。</span><span class="sxs-lookup"><span data-stu-id="675eb-121">Indicates that Windows Animation can delay the scheduled start of a storyboard for as much time as necessary to avoid scheduling conflicts.</span></span><br/>                                                                                                                     |
| [<span data-ttu-id="675eb-122">**UI \_ 動畫 \_ 不 \_ 限時數**</span><span class="sxs-lookup"><span data-stu-id="675eb-122">**UI\_ANIMATION\_SECONDS\_INFINITE**</span></span>](ui-animation-seconds-infinite.md)<br/>                                              | <span data-ttu-id="675eb-123">指出沒有任何已排程的事件。</span><span class="sxs-lookup"><span data-stu-id="675eb-123">Indicates that there are no scheduled events.</span></span><br/>                                                                                                                                                                                                                   |



 

## <a name="related-topics"></a><span data-ttu-id="675eb-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="675eb-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="675eb-125">Windows 動畫參考</span><span class="sxs-lookup"><span data-stu-id="675eb-125">Windows Animation Reference</span></span>](windows-animation-reference.md)
</dt> </dl>

 

