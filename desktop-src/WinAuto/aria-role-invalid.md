---
title: ARIA 角色錯誤
description: ARIA 角色錯誤
ms.assetid: FEEB4F28-4A71-4417-A2F9-ABCB86B44F0F
keywords:
- AriaRoleErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df04ad94d68ae1e8e2e8d3352aa349834a2389fa
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/09/2020
ms.locfileid: "106995156"
---
# <a name="aria-role-error"></a><span data-ttu-id="82e57-104">ARIA 角色錯誤</span><span class="sxs-lookup"><span data-stu-id="82e57-104">ARIA Role Error</span></span>

## <a name="text"></a><span data-ttu-id="82e57-105">Text</span><span class="sxs-lookup"><span data-stu-id="82e57-105">Text</span></span>

<span data-ttu-id="82e57-106">元素有不正確 WAI-ARIA 角色。</span><span class="sxs-lookup"><span data-stu-id="82e57-106">Element has invalid WAI-ARIA role.</span></span>

## <a name="type"></a><span data-ttu-id="82e57-107">類型</span><span class="sxs-lookup"><span data-stu-id="82e57-107">Type</span></span>

<span data-ttu-id="82e57-108">錯誤</span><span class="sxs-lookup"><span data-stu-id="82e57-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="82e57-109">描述</span><span class="sxs-lookup"><span data-stu-id="82e57-109">Description</span></span>

<span data-ttu-id="82e57-110">此錯誤適用于具有 [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) 屬性的所有元素。</span><span class="sxs-lookup"><span data-stu-id="82e57-110">This error applies to all elements that have the [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) attribute.</span></span> <span data-ttu-id="82e57-111">這表示 **role** 屬性不是有效的 Web 協助工具計畫可存取的豐富網際網路應用程式， (WAI-aria) 角色值，如 WAI-aria 規格所定義。</span><span class="sxs-lookup"><span data-stu-id="82e57-111">It indicates that the **role** attribute is not a valid Web Accessibility Initiative - Accessible Rich Internet Applications (WAI-ARIA) role value as defined by the WAI-ARIA specification.</span></span> <span data-ttu-id="82e57-112">設定有效的角色有助於確保螢幕讀取器和其他輔助技術工具可以正確地解讀元素。</span><span class="sxs-lookup"><span data-stu-id="82e57-112">Setting a valid role helps ensure that the element is correctly interpreted by screen readers and other assistive technology tools.</span></span>

<span data-ttu-id="82e57-113">若要修正這個錯誤，請將 [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) 屬性設為有效的 WAI-ARIA 角色值。</span><span class="sxs-lookup"><span data-stu-id="82e57-113">To fix this error, set the [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) attribute to a valid WAI-ARIA role value.</span></span> <span data-ttu-id="82e57-114">請注意，abstract WAI-ARIA 角色無效。</span><span class="sxs-lookup"><span data-stu-id="82e57-114">Note that abstract WAI-ARIA roles are not valid.</span></span>

## <a name="example"></a><span data-ttu-id="82e57-115">範例</span><span class="sxs-lookup"><span data-stu-id="82e57-115">Example</span></span>


```HTML
<!—The invalid role will not expose this element as a button. -->
<div role="backbutton" tabindex="0" aria-label="Back" onclick="mouseAction(event)" onkeyup="keyAction(event)" >

<!—Setting the correct role will expose this as a button that can be clicked. -->
<div role="button" tabindex="0" aria-label="Back" onclick="mouseAction(event)" onkeyup="keyAction(event)" >
```



## <a name="related-topics"></a><span data-ttu-id="82e57-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="82e57-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82e57-117">ARIA 容器角色錯誤</span><span class="sxs-lookup"><span data-stu-id="82e57-117">ARIA Container Role Error</span></span>](aria-container-role.md)
</dt> </dl>

 

 




