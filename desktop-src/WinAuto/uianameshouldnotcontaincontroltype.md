---
title: UiaNameShouldNotContainControlType
description: UiaNameShouldNotContainControlType
ms.assetid: 96F7A5FC-1879-4706-9E67-5B43D57F7281
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6178ca4cd4c4b2ed0deb0070116b597ba3bd1bc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839723"
---
# <a name="uianameshouldnotcontaincontroltype"></a><span data-ttu-id="c9226-103">UiaNameShouldNotContainControlType</span><span class="sxs-lookup"><span data-stu-id="c9226-103">UiaNameShouldNotContainControlType</span></span>

## <a name="text"></a><span data-ttu-id="c9226-104">Text</span><span class="sxs-lookup"><span data-stu-id="c9226-104">Text</span></span>

<span data-ttu-id="c9226-105">元素的名稱 ({0}) 不應包含 ControlType (的文字 {1}) </span><span class="sxs-lookup"><span data-stu-id="c9226-105">Element's Name ({0}) should not contain the text of the ControlType ({1})</span></span>

## <a name="type"></a><span data-ttu-id="c9226-106">類型</span><span class="sxs-lookup"><span data-stu-id="c9226-106">Type</span></span>

<span data-ttu-id="c9226-107">警告</span><span class="sxs-lookup"><span data-stu-id="c9226-107">Warning</span></span>

## <a name="description"></a><span data-ttu-id="c9226-108">描述</span><span class="sxs-lookup"><span data-stu-id="c9226-108">Description</span></span>

<span data-ttu-id="c9226-109">元素的名稱會併入其 UIA 控制項類型。</span><span class="sxs-lookup"><span data-stu-id="c9226-109">The name of an element incorporates its UIA control type.</span></span> <span data-ttu-id="c9226-110">例如，如果具有按鈕控制項類型之專案的 [UIA Name] 屬性設定為 [我的按鈕]，就會發生這個警告。</span><span class="sxs-lookup"><span data-stu-id="c9226-110">For example, this warning can occur if the UIA Name property for an element with the Button control type is set to "My Button".</span></span>

<span data-ttu-id="c9226-111">這個問題會讓依賴螢幕讀取器和鍵盤進行導覽的人員遇到問題，因為控制項類型將會讀取兩次，或是使用者可能 unpronounceable 或非直覺。</span><span class="sxs-lookup"><span data-stu-id="c9226-111">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because the control type will be read twice, or it may be unpronounceable or non-intuitive for users.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="c9226-112">可能的原因</span><span class="sxs-lookup"><span data-stu-id="c9226-112">Possible causes</span></span>

-   <span data-ttu-id="c9226-113">元素或其父系有不正確指派的名稱或標籤。</span><span class="sxs-lookup"><span data-stu-id="c9226-113">The element or its parent has an incorrectly assigned name or label.</span></span>
-   <span data-ttu-id="c9226-114">元素或其父系具有尚未修改為易記名稱的預設名稱。</span><span class="sxs-lookup"><span data-stu-id="c9226-114">The element or its parent has a default name that has not been revised to a friendly name.</span></span> <span data-ttu-id="c9226-115">例如，button1。</span><span class="sxs-lookup"><span data-stu-id="c9226-115">For example, button1.</span></span>
-   <span data-ttu-id="c9226-116">開發人員並不知道螢幕讀取器會讀取名稱和控制項類型。</span><span class="sxs-lookup"><span data-stu-id="c9226-116">A developer is not aware that screen readers read names and control types.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c9226-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="c9226-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9226-118">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="c9226-118">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)
</dt> <dt>

[<span data-ttu-id="c9226-119">**IUIAutomationElement::CurrentName**</span><span class="sxs-lookup"><span data-stu-id="c9226-119">**IUIAutomationElement::CurrentName**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname)
</dt> </dl>

 

 




