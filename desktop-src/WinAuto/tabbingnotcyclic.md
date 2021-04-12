---
title: TabbingNotCyclic
description: TabbingNotCyclic
ms.assetid: F6BCC613-1EA1-438C-AC09-8A282870E021
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e08fd2e9f6613e07840f432b646c1bdc06a34b5f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023699"
---
# <a name="tabbingnotcyclic"></a><span data-ttu-id="bc699-103">TabbingNotCyclic</span><span class="sxs-lookup"><span data-stu-id="bc699-103">TabbingNotCyclic</span></span>

## <a name="text"></a><span data-ttu-id="bc699-104">Text</span><span class="sxs-lookup"><span data-stu-id="bc699-104">Text</span></span>

<span data-ttu-id="bc699-105">此應用程式中的定位鍵不是迴圈的。</span><span class="sxs-lookup"><span data-stu-id="bc699-105">The tabbing in this application is not cyclic.</span></span> <span data-ttu-id="bc699-106">向前或向後定位將 {0} 不會回到相同的控制項。</span><span class="sxs-lookup"><span data-stu-id="bc699-106">Tabbing forwards or backwards {0} times doesn't come back to the same control.</span></span>

## <a name="type"></a><span data-ttu-id="bc699-107">類型</span><span class="sxs-lookup"><span data-stu-id="bc699-107">Type</span></span>

<span data-ttu-id="bc699-108">錯誤</span><span class="sxs-lookup"><span data-stu-id="bc699-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="bc699-109">描述</span><span class="sxs-lookup"><span data-stu-id="bc699-109">Description</span></span>

<span data-ttu-id="bc699-110">使用標準鍵盤導覽 (Tab 或 Shift + Tab) 時，您無法在起始元素變成結束元素之前，先移動驗證目標的專案樹狀結構， (藉由反轉遍歷方向來) 使用相同數目的按鍵。</span><span class="sxs-lookup"><span data-stu-id="bc699-110">When using standard keyboard navigation (Tab or Shift+Tab), it isn't possible to traverse the element tree of the verification target until the starting element becomes the ending element (using the same number of keystrokes) by reversing the direction of traversal.</span></span> <span data-ttu-id="bc699-111">例如，向前 (Tab) x 次的 tab 鍵，從專案 A (0) 到專案 A (x) ，然後將反向定位 (Shift + Tab) x 次不會導致元素 A (重新取得焦點。</span><span class="sxs-lookup"><span data-stu-id="bc699-111">For example, tabbing forward (Tab) x times from element A(0) to element A(x) and then tabbing backward (Shift+Tab) x times does not result in element A(0) regaining focus.</span></span>

<span data-ttu-id="bc699-112">這個問題會讓依賴螢幕讀取器和鍵盤進行導覽的人員遇到問題，因為在流覽之後，沒有可預測的方法可以返回控制項。</span><span class="sxs-lookup"><span data-stu-id="bc699-112">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because there is no predictable way to return to a control after it has been visited.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="bc699-113">可能的原因</span><span class="sxs-lookup"><span data-stu-id="bc699-113">Possible causes</span></span>

-   <span data-ttu-id="bc699-114">元素或其父代是未正確執行 tab 鍵的自訂控制項。</span><span class="sxs-lookup"><span data-stu-id="bc699-114">The element or its parent is a custom control that doesn't implement tabbing correctly.</span></span> <span data-ttu-id="bc699-115">例如，未正確設定 MSAA 狀態屬性。</span><span class="sxs-lookup"><span data-stu-id="bc699-115">For example, the MSAA State property isn't set correctly.</span></span>
-   <span data-ttu-id="bc699-116">某些應用程式（例如 [記事本]）會顯示此行為本質。</span><span class="sxs-lookup"><span data-stu-id="bc699-116">Some applications, such as the Notepad, exhibit this behavior innately.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bc699-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="bc699-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc699-118">鍵盤使用者介面設計指導方針</span><span class="sxs-lookup"><span data-stu-id="bc699-118">Guidelines for Keyboard User Interface Design</span></span>](/previous-versions/windows/desktop/dnacc/guidelines-for-keyboard-user-interface-design)
</dt> </dl>

 

 