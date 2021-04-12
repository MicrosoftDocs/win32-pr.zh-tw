---
title: UiaNameLengthTooLong
description: UiaNameLengthTooLong
ms.assetid: 01AF3F1E-9A3F-48B4-8219-6E80BAFC82EE
keywords:
- UIA_NamePropertyId 識別碼 AutomationElement. NameProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ab786b7167dab4a25384ce3abe2509babcf1f82
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372533"
---
# <a name="uianamelengthtoolong"></a><span data-ttu-id="6a300-104">UiaNameLengthTooLong</span><span class="sxs-lookup"><span data-stu-id="6a300-104">UiaNameLengthTooLong</span></span>

## <a name="text"></a><span data-ttu-id="6a300-105">Text</span><span class="sxs-lookup"><span data-stu-id="6a300-105">Text</span></span>

<span data-ttu-id="6a300-106">元素的名稱不應傳回長度超過字元的字串 {0}</span><span class="sxs-lookup"><span data-stu-id="6a300-106">Element's name should not return a string longer than {0} character</span></span>

## <a name="type"></a><span data-ttu-id="6a300-107">類型</span><span class="sxs-lookup"><span data-stu-id="6a300-107">Type</span></span>

<span data-ttu-id="6a300-108">錯誤</span><span class="sxs-lookup"><span data-stu-id="6a300-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="6a300-109">描述</span><span class="sxs-lookup"><span data-stu-id="6a300-109">Description</span></span>

<span data-ttu-id="6a300-110">元素名稱包含太多字元。</span><span class="sxs-lookup"><span data-stu-id="6a300-110">The name of an element contains too many characters.</span></span> <span data-ttu-id="6a300-111">例如，用來取出專案之 UIA 名稱的 [**IUIAutomationElement：： CurrentName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname) 方法會傳回大於限制的字串。</span><span class="sxs-lookup"><span data-stu-id="6a300-111">For example, the [**IUIAutomationElement::CurrentName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname) method used to retrieve the UIA name of an element returns a string greater than the limit.</span></span>

<span data-ttu-id="6a300-112">這個問題會讓依賴螢幕讀取器和鍵盤進行導覽的人員遇到問題，因為元素可能有 unpronounceable、非直覺的名稱。</span><span class="sxs-lookup"><span data-stu-id="6a300-112">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because an element might have an unpronounceable, non-intuitive name.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="6a300-113">可能的原因</span><span class="sxs-lookup"><span data-stu-id="6a300-113">Possible causes</span></span>

<span data-ttu-id="6a300-114">元素或其父系有不正確指派的名稱或標籤。</span><span class="sxs-lookup"><span data-stu-id="6a300-114">The element or its parent has an incorrectly assigned name or label.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6a300-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="6a300-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a300-116">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="6a300-116">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)
</dt> <dt>

[<span data-ttu-id="6a300-117">**IUIAutomationElement::CurrentName**</span><span class="sxs-lookup"><span data-stu-id="6a300-117">**IUIAutomationElement::CurrentName**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname)
</dt> </dl>

 

 




