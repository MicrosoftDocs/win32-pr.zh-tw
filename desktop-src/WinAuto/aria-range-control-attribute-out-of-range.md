---
title: ARIA 範圍控制項屬性不相容
description: ARIA 範圍控制項屬性不相容
ms.assetid: 265AE578-D841-4931-9F4A-97BB86ECEC88
keywords:
- AriaRangeControlAttributesIncompatibleId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aef55ee57c4966896e666dd5a7ac1d20eb5257c6
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/09/2020
ms.locfileid: "104508183"
---
# <a name="aria-range-control-attributes-incompatible"></a><span data-ttu-id="d4471-104">ARIA 範圍控制項屬性不相容</span><span class="sxs-lookup"><span data-stu-id="d4471-104">ARIA Range Control Attributes Incompatible</span></span>

## <a name="text"></a><span data-ttu-id="d4471-105">Text</span><span class="sxs-lookup"><span data-stu-id="d4471-105">Text</span></span>

<span data-ttu-id="d4471-106">元素具有 **progressbar** 或 **滑杆** 角色，但公開的 **aria-valuenow** 值位於 **aria valuemin** 的 **aria valuemax** 範圍之外。</span><span class="sxs-lookup"><span data-stu-id="d4471-106">Element has **progressbar** or **slider** role but exposed **aria-valuenow** value is outside of **aria-valuemin** **aria-valuemax** range.</span></span>

## <a name="type"></a><span data-ttu-id="d4471-107">類型</span><span class="sxs-lookup"><span data-stu-id="d4471-107">Type</span></span>

<span data-ttu-id="d4471-108">錯誤</span><span class="sxs-lookup"><span data-stu-id="d4471-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="d4471-109">描述</span><span class="sxs-lookup"><span data-stu-id="d4471-109">Description</span></span>

<span data-ttu-id="d4471-110">此錯誤適用于 [**角色**](https://developer.mozilla.org/docs/Web/HTML/Reference) (隱含或明確) 等於 **progressbar**、**滑杆** 或數值 **調整的元素。**</span><span class="sxs-lookup"><span data-stu-id="d4471-110">This error applies to elements that have a [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) (implicit or explicit) equal to **progressbar**, **slider**, or **spinbutton**.</span></span>

<span data-ttu-id="d4471-111">此錯誤表示公開的 [**aria valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) 值不在 [**valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) 和 [**aria valuemax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) 屬性所定義的範圍內。</span><span class="sxs-lookup"><span data-stu-id="d4471-111">This error indicates that the exposed [**aria-valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) value is not in the range defined by the [**aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) and [**aria-valuemax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attributes.</span></span>

<span data-ttu-id="d4471-112">若要修正這個錯誤，請檢查您的執行，以確定已正確設定 [**aria valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) 和 [**aria valuemax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) 屬性，並已正確維護 [**aria valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) 屬性值。</span><span class="sxs-lookup"><span data-stu-id="d4471-112">To fix this error, check your implementation to ensure that the [**aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) and [**aria-valuemax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attributes are correctly set, and that the [**aria-valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attribute value is properly maintained.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d4471-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="d4471-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d4471-114">缺少 ARIA 範圍控制項屬性</span><span class="sxs-lookup"><span data-stu-id="d4471-114">ARIA Range Control Attributes Missing</span></span>](aria-range-control-attributes-missing.md)
</dt> </dl>

 

 




