---
title: TreeMightBeCyclic
description: TreeMightBeCyclic
ms.assetid: 9A997949-A1A2-448C-9739-BE176621F1B4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9647f4429ba17226f342a8dceb3c51b033d08b4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315280"
---
# <a name="treemightbecyclic"></a><span data-ttu-id="21931-103">TreeMightBeCyclic</span><span class="sxs-lookup"><span data-stu-id="21931-103">TreeMightBeCyclic</span></span>

## <a name="text"></a><span data-ttu-id="21931-104">Text</span><span class="sxs-lookup"><span data-stu-id="21931-104">Text</span></span>

<span data-ttu-id="21931-105">樹狀結構是 {0} 層級深度。</span><span class="sxs-lookup"><span data-stu-id="21931-105">Tree is {0} levels deep.</span></span> <span data-ttu-id="21931-106">這可能表示存取範圍樹狀結構是迴圈的，因此似乎是無限的。</span><span class="sxs-lookup"><span data-stu-id="21931-106">This might indicate that the accessibility tree is cyclic, and thus it would appear to be infinite.</span></span>

## <a name="type"></a><span data-ttu-id="21931-107">類型</span><span class="sxs-lookup"><span data-stu-id="21931-107">Type</span></span>

<span data-ttu-id="21931-108">錯誤</span><span class="sxs-lookup"><span data-stu-id="21931-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="21931-109">描述</span><span class="sxs-lookup"><span data-stu-id="21931-109">Description</span></span>

<span data-ttu-id="21931-110">專案樹狀結構是迴圈的，樹狀目錄深度可能是無限的。</span><span class="sxs-lookup"><span data-stu-id="21931-110">The element tree is cyclic and the tree depth might be infinite.</span></span>

<span data-ttu-id="21931-111">這個問題會讓依賴螢幕讀取器和鍵盤進行流覽的人員遇到問題，因為目標應用程式中的專案的控制不會有明顯的限制。</span><span class="sxs-lookup"><span data-stu-id="21931-111">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because there will be no apparent limit to the traversal of elements in the target application.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="21931-112">可能的原因</span><span class="sxs-lookup"><span data-stu-id="21931-112">Possible causes</span></span>

<span data-ttu-id="21931-113">多個專案（或其父代）是未正確執行定位的自訂控制項。</span><span class="sxs-lookup"><span data-stu-id="21931-113">Multiple elements, or their parents, are custom controls that do not implement tabbing correctly.</span></span> <span data-ttu-id="21931-114">例如，[MSAA [狀態](state-property.md) ] 屬性未正確更新。</span><span class="sxs-lookup"><span data-stu-id="21931-114">For example, the MSAA [State](state-property.md) property is not updated correctly.</span></span>

## <a name="related-topics"></a><span data-ttu-id="21931-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="21931-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="21931-116">鍵盤使用者介面設計指導方針</span><span class="sxs-lookup"><span data-stu-id="21931-116">Guidelines for Keyboard User Interface Design</span></span>](/previous-versions/windows/desktop/dnacc/guidelines-for-keyboard-user-interface-design)
</dt> <dt>

[<span data-ttu-id="21931-117">Windows 使用者經驗互動指導方針-鍵盤</span><span class="sxs-lookup"><span data-stu-id="21931-117">Windows User Experience Interaction Guidelines - Keyboard</span></span>](https://msdn.microsoft.com/library/bb545460.aspx#guidelines)
</dt> </dl>

 

 