---
title: TabbedToUnknownElement
description: TabbedToUnknownElement
ms.assetid: B0447B19-E281-4D30-8ED8-FC0EE13571C8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 612476d81779c882eeca807a9c3b82c41594f218
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372037"
---
# <a name="tabbedtounknownelement"></a><span data-ttu-id="953ed-103">TabbedToUnknownElement</span><span class="sxs-lookup"><span data-stu-id="953ed-103">TabbedToUnknownElement</span></span>

## <a name="text"></a><span data-ttu-id="953ed-104">Text</span><span class="sxs-lookup"><span data-stu-id="953ed-104">Text</span></span>

<span data-ttu-id="953ed-105">Tab 鍵已移至目標 hwnd 外部的專案。</span><span class="sxs-lookup"><span data-stu-id="953ed-105">Tabbing has gone to an element outside the target hwnd.</span></span>

## <a name="type"></a><span data-ttu-id="953ed-106">類型</span><span class="sxs-lookup"><span data-stu-id="953ed-106">Type</span></span>

<span data-ttu-id="953ed-107">錯誤</span><span class="sxs-lookup"><span data-stu-id="953ed-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="953ed-108">描述</span><span class="sxs-lookup"><span data-stu-id="953ed-108">Description</span></span>

<span data-ttu-id="953ed-109">使用標準鍵盤流覽 (Tab 或 Shift + Tab) 會導致焦點移至驗證目標的 HWND 之外。</span><span class="sxs-lookup"><span data-stu-id="953ed-109">Using standard keyboard navigation (Tab or Shift+Tab) causes focus to shift outside the HWND of the verification target.</span></span>

<span data-ttu-id="953ed-110">AccChecker 會在執行任何驗證工作之前，將元素樹狀結構向上移至所選驗證目標的最上層 HWND。</span><span class="sxs-lookup"><span data-stu-id="953ed-110">AccChecker moves up the element tree to the top-level HWND for the chosen verification target before running any verification tasks.</span></span> <span data-ttu-id="953ed-111">如果選擇要驗證的 HWND 是更複雜的工作區的一部分，這會減少產生的偽造錯誤數目。</span><span class="sxs-lookup"><span data-stu-id="953ed-111">This reduces the number of spurious errors generated if an HWND chosen for verification is part of a more complex client area.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="953ed-112">可能的原因</span><span class="sxs-lookup"><span data-stu-id="953ed-112">Possible causes</span></span>

-   <span data-ttu-id="953ed-113">驗證目標不需要有定位的執行，就能提供完整的功能。</span><span class="sxs-lookup"><span data-stu-id="953ed-113">The verification target doesn't require a tabbing implementation to provide full functionality.</span></span>
-   <span data-ttu-id="953ed-114">驗證期間的使用者互動，例如將焦點移至非目標 HWND，並干擾驗證程式。</span><span class="sxs-lookup"><span data-stu-id="953ed-114">User interaction during verification, such as moving focus to a non-target HWND, interfered with the verification process.</span></span>

 

 




