---
title: UiaElementIsOrphaned
description: UiaElementIsOrphaned
ms.assetid: F85F08E7-5A9C-4F08-B680-8B251D51168A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0ec0861a586fd5275a674d9ef8ba6a0e72364b2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106964974"
---
# <a name="uiaelementisorphaned"></a><span data-ttu-id="2c917-103">UiaElementIsOrphaned</span><span class="sxs-lookup"><span data-stu-id="2c917-103">UiaElementIsOrphaned</span></span>

## <a name="text"></a><span data-ttu-id="2c917-104">Text</span><span class="sxs-lookup"><span data-stu-id="2c917-104">Text</span></span>

<span data-ttu-id="2c917-105">元素是樹狀結構中的孤立 AutomationElement</span><span class="sxs-lookup"><span data-stu-id="2c917-105">Element is an orphaned AutomationElement in the tree</span></span>

## <a name="type"></a><span data-ttu-id="2c917-106">類型</span><span class="sxs-lookup"><span data-stu-id="2c917-106">Type</span></span>

<span data-ttu-id="2c917-107">錯誤</span><span class="sxs-lookup"><span data-stu-id="2c917-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="2c917-108">描述</span><span class="sxs-lookup"><span data-stu-id="2c917-108">Description</span></span>

<span data-ttu-id="2c917-109">針對指定座標取得之物件 [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) 介面的位址是專案樹狀結構中孤立元素的參考。</span><span class="sxs-lookup"><span data-stu-id="2c917-109">The address of the object's [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) interface obtained for the given coordinates is a reference to an orphaned element in the element tree.</span></span>

<span data-ttu-id="2c917-110">這個問題適用于依賴螢幕閱讀程式和鍵盤進行導覽的人員，因為元素將被視為不可見，而且不會向使用者宣告。</span><span class="sxs-lookup"><span data-stu-id="2c917-110">This issue is a problem for people who rely on a screen-reader and keyboard for navigation because elements will be treated as invisible and will not be announced to the user.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="2c917-111">可能的原因</span><span class="sxs-lookup"><span data-stu-id="2c917-111">Possible causes</span></span>

-   <span data-ttu-id="2c917-112">驗證期間的使用者互動，例如將焦點移至非目標 HWND，並干擾驗證程式。</span><span class="sxs-lookup"><span data-stu-id="2c917-112">User interaction during verification, such as moving focus to a non-target HWND, interfered with the verification process.</span></span>
-   <span data-ttu-id="2c917-113">消費者介面自動化的執行不正確或無效。</span><span class="sxs-lookup"><span data-stu-id="2c917-113">An incorrect or invalid UI Automation implementation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2c917-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="2c917-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c917-115">**IUIAutomationElement.ElementFromPoint**</span><span class="sxs-lookup"><span data-stu-id="2c917-115">**IUIAutomationElement.ElementFromPoint**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint)
</dt> </dl>

 

 




