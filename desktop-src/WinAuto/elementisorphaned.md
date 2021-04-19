---
title: ElementIsOrphaned
description: ElementIsOrphaned
ms.assetid: EB603052-2B0F-418C-947E-827453440F46
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1878556af6f1954224bc9b5eadfd4d77e6e3419
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969487"
---
# <a name="elementisorphaned"></a><span data-ttu-id="cf655-103">ElementIsOrphaned</span><span class="sxs-lookup"><span data-stu-id="cf655-103">ElementIsOrphaned</span></span>

## <a name="text"></a><span data-ttu-id="cf655-104">Text</span><span class="sxs-lookup"><span data-stu-id="cf655-104">Text</span></span>

<span data-ttu-id="cf655-105">元素是樹狀結構中的孤立 IAccessible</span><span class="sxs-lookup"><span data-stu-id="cf655-105">Element is an orphaned IAccessible in the tree</span></span>

## <a name="type"></a><span data-ttu-id="cf655-106">類型</span><span class="sxs-lookup"><span data-stu-id="cf655-106">Type</span></span>

<span data-ttu-id="cf655-107">錯誤</span><span class="sxs-lookup"><span data-stu-id="cf655-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="cf655-108">描述</span><span class="sxs-lookup"><span data-stu-id="cf655-108">Description</span></span>

<span data-ttu-id="cf655-109">針對指定座標取得之物件 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面的位址是專案樹狀結構中孤立元素的參考。</span><span class="sxs-lookup"><span data-stu-id="cf655-109">The address of the object's [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface obtained for the given coordinates is a reference to an orphaned element in the element tree.</span></span>

<span data-ttu-id="cf655-110">這個問題適用于依賴螢幕閱讀程式和鍵盤進行導覽的人員，因為元素將被視為不可見，而且不會向使用者宣告。</span><span class="sxs-lookup"><span data-stu-id="cf655-110">This issue is a problem for people who rely on a screen-reader and keyboard for navigation because elements will be treated as invisible and will not be announced to the user.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="cf655-111">可能的原因</span><span class="sxs-lookup"><span data-stu-id="cf655-111">Possible causes</span></span>

-   <span data-ttu-id="cf655-112">驗證期間的使用者互動，例如將焦點移至非目標 HWND，並干擾驗證程式。</span><span class="sxs-lookup"><span data-stu-id="cf655-112">User interaction during verification, such as moving focus to a non-target HWND, interfered with the verification process.</span></span>
-   <span data-ttu-id="cf655-113">不正確或不正確 MSAA 執行。</span><span class="sxs-lookup"><span data-stu-id="cf655-113">An incorrect or invalid MSAA implementation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cf655-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="cf655-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cf655-115">流覽點擊測試和螢幕位置</span><span class="sxs-lookup"><span data-stu-id="cf655-115">Navigation Through Hit Testing and Screen Location</span></span>](navigation-through-hit-testing-and-screen-location.md)
</dt> <dt>

[<span data-ttu-id="cf655-116">**AccessibleObjectFromPoint**</span><span class="sxs-lookup"><span data-stu-id="cf655-116">**AccessibleObjectFromPoint**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
</dt> </dl>

 

 




