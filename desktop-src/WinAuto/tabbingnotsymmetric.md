---
title: TabbingNotSymmetric
description: TabbingNotSymmetric
ms.assetid: 1E14ED9F-27C1-4054-B0A6-702167222196
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc19efbbbce0f299044726466dd8f87b133fc26d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092849"
---
# <a name="tabbingnotsymmetric"></a><span data-ttu-id="9916d-103">TabbingNotSymmetric</span><span class="sxs-lookup"><span data-stu-id="9916d-103">TabbingNotSymmetric</span></span>

## <a name="text"></a><span data-ttu-id="9916d-104">Text</span><span class="sxs-lookup"><span data-stu-id="9916d-104">Text</span></span>

<span data-ttu-id="9916d-105">向後定位和向前定位並不會產生相同的元素。</span><span class="sxs-lookup"><span data-stu-id="9916d-105">Tabbing backwards and forwards does not yield the same element.</span></span> <span data-ttu-id="9916d-106">預期 {0} 但已接收 {1}</span><span class="sxs-lookup"><span data-stu-id="9916d-106">Expected {0} but received {1}</span></span>

## <a name="type"></a><span data-ttu-id="9916d-107">類型</span><span class="sxs-lookup"><span data-stu-id="9916d-107">Type</span></span>

<span data-ttu-id="9916d-108">錯誤</span><span class="sxs-lookup"><span data-stu-id="9916d-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="9916d-109">描述</span><span class="sxs-lookup"><span data-stu-id="9916d-109">Description</span></span>

<span data-ttu-id="9916d-110">使用標準鍵盤流覽 (Tab 或 Shift + Tab) 時，如果迴圈的方向反轉，則無法在驗證目標的專案樹狀結構中重複執行的路徑。</span><span class="sxs-lookup"><span data-stu-id="9916d-110">When using standard keyboard navigation (Tab or Shift+Tab), it isn't possible to repeat the path of traversal through the element tree of the verification target if the direction of traversal is reversed.</span></span> <span data-ttu-id="9916d-111">例如，向前 (Tab) x 次的 tab 鍵，從專案 A (0) 到專案 A (x) ，然後將 (Shift + Tab) x 次，就會導致專案 A (0) 透過一組不同的中繼元素重新取得焦點。</span><span class="sxs-lookup"><span data-stu-id="9916d-111">For example, tabbing forward (Tab) x times from element A(0) to element A(x) and then tabbing backward (Shift+Tab) x times results in element A(0) regaining focus through a different set of intermediate elements.</span></span>

<span data-ttu-id="9916d-112">這個問題會讓依賴螢幕讀取器和鍵盤進行導覽的人員發生問題，因為進行中的動作會顯示為不穩定且無法預測。</span><span class="sxs-lookup"><span data-stu-id="9916d-112">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because traversing elements appears erratic and unpredictable.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="9916d-113">可能的原因</span><span class="sxs-lookup"><span data-stu-id="9916d-113">Possible causes</span></span>

-   <span data-ttu-id="9916d-114">多個元素或其父代是未正確執行 tab 鍵的自訂控制項。</span><span class="sxs-lookup"><span data-stu-id="9916d-114">Multiple elements or their parents are custom controls that don't implement tabbing correctly.</span></span> <span data-ttu-id="9916d-115">例如，未正確設定 MSAA 狀態屬性。</span><span class="sxs-lookup"><span data-stu-id="9916d-115">For example, the MSAA State property is not set correctly.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9916d-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="9916d-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9916d-117">鍵盤使用者介面設計指導方針</span><span class="sxs-lookup"><span data-stu-id="9916d-117">Guidelines for Keyboard User Interface Design</span></span>](/previous-versions/windows/desktop/dnacc/guidelines-for-keyboard-user-interface-design)
</dt> </dl>

 

 