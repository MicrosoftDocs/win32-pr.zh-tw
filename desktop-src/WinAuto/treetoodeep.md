---
title: TreeTooDeep
description: TreeTooDeep
ms.assetid: 3FD4A1BE-4710-4A1F-9ED7-98D7FCBCD304
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 681a929eca288584e9bd9ccd7b32920b10a72131
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682665"
---
# <a name="treetoodeep"></a><span data-ttu-id="93ba7-103">TreeTooDeep</span><span class="sxs-lookup"><span data-stu-id="93ba7-103">TreeTooDeep</span></span>

## <a name="text"></a><span data-ttu-id="93ba7-104">Text</span><span class="sxs-lookup"><span data-stu-id="93ba7-104">Text</span></span>

<span data-ttu-id="93ba7-105">樹狀結構是 {0} 層級深度。</span><span class="sxs-lookup"><span data-stu-id="93ba7-105">Tree is {0} levels deep.</span></span>

## <a name="type"></a><span data-ttu-id="93ba7-106">類型</span><span class="sxs-lookup"><span data-stu-id="93ba7-106">Type</span></span>

<span data-ttu-id="93ba7-107">警告</span><span class="sxs-lookup"><span data-stu-id="93ba7-107">Warning</span></span>

## <a name="description"></a><span data-ttu-id="93ba7-108">描述</span><span class="sxs-lookup"><span data-stu-id="93ba7-108">Description</span></span>

<span data-ttu-id="93ba7-109">元素樹狀結構可能太深。</span><span class="sxs-lookup"><span data-stu-id="93ba7-109">The element tree might be too deep.</span></span>

<span data-ttu-id="93ba7-110">這個問題會讓依賴螢幕讀取器和鍵盤進行導覽的人員遇到問題，因為進行中的元素似乎需要很長的時間，而且可能會出現迴圈。</span><span class="sxs-lookup"><span data-stu-id="93ba7-110">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because traversing elements will seem to take a long time and may appear cyclic.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="93ba7-111">可能的原因</span><span class="sxs-lookup"><span data-stu-id="93ba7-111">Possible causes</span></span>

-   <span data-ttu-id="93ba7-112">多個元素或其父代是未正確執行 tab 鍵的自訂控制項。</span><span class="sxs-lookup"><span data-stu-id="93ba7-112">Multiple elements or their parents are custom controls that do not implement tabbing correctly.</span></span> <span data-ttu-id="93ba7-113">例如，[MSAA 狀態] 屬性未正確更新。</span><span class="sxs-lookup"><span data-stu-id="93ba7-113">For example, the MSAA State property is not updated correctly.</span></span>
-   <span data-ttu-id="93ba7-114">應用程式 UI 過於複雜。</span><span class="sxs-lookup"><span data-stu-id="93ba7-114">The application UI is overly complex.</span></span>

## <a name="related-topics"></a><span data-ttu-id="93ba7-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="93ba7-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="93ba7-116">鍵盤使用者介面設計指導方針</span><span class="sxs-lookup"><span data-stu-id="93ba7-116">Guidelines for Keyboard User Interface Design</span></span>](/previous-versions/windows/desktop/dnacc/guidelines-for-keyboard-user-interface-design)
</dt> <dt>

[<span data-ttu-id="93ba7-117">Windows 使用者經驗互動指導方針-鍵盤</span><span class="sxs-lookup"><span data-stu-id="93ba7-117">Windows User Experience Interaction Guidelines - Keyboard</span></span>](https://msdn.microsoft.com/library/bb545460.aspx#guidelines)
</dt> </dl>

 

 