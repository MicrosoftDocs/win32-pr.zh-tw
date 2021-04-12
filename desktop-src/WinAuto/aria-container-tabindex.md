---
title: ARIA 容器 Tabindex 錯誤
description: ARIA 容器 Tabindex 錯誤
ms.assetid: CCEA9490-903D-423D-B9FD-641E8B7D3E0B
keywords:
- AriaContainerTabIndexErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b6af684b401627181aaef656215240a312393f2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372555"
---
# <a name="aria-container-tabindex-error"></a><span data-ttu-id="a19af-104">ARIA 容器 Tabindex 錯誤</span><span class="sxs-lookup"><span data-stu-id="a19af-104">ARIA Container Tabindex Error</span></span>

## <a name="text"></a><span data-ttu-id="a19af-105">Text</span><span class="sxs-lookup"><span data-stu-id="a19af-105">Text</span></span>

<span data-ttu-id="a19af-106">元素是具有已定義之作用中子系的可設定焦點容器，但沒有大於或等於0的 **tabindex** 值。</span><span class="sxs-lookup"><span data-stu-id="a19af-106">Element is a focusable container with active descendants defined but without **tabindex** value greater or equal to 0.</span></span>

## <a name="type"></a><span data-ttu-id="a19af-107">類型</span><span class="sxs-lookup"><span data-stu-id="a19af-107">Type</span></span>

<span data-ttu-id="a19af-108">錯誤</span><span class="sxs-lookup"><span data-stu-id="a19af-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="a19af-109">描述</span><span class="sxs-lookup"><span data-stu-id="a19af-109">Description</span></span>

<span data-ttu-id="a19af-110">此錯誤適用于具有 **aria activedescendant** 屬性、未停用的元素，而且沒有將 **tabindex** 屬性設定為大於或等於0的值。</span><span class="sxs-lookup"><span data-stu-id="a19af-110">This error applies to elements that have the **aria-activedescendant** attribute, are not disabled, and do not have the **tabindex** attribute set to a value that is greater than or equal to 0.</span></span> <span data-ttu-id="a19af-111">這些元素必須是定位順序，因為它們負責處理其子項目的鍵盤事件。</span><span class="sxs-lookup"><span data-stu-id="a19af-111">These elements must be in tab order because they are responsible for handling keyboard events for their child elements.</span></span>

<span data-ttu-id="a19af-112">若要修正這個錯誤，請將 **tabindex** 屬性設定為大於或等於0的值。</span><span class="sxs-lookup"><span data-stu-id="a19af-112">To fix this error, set the **tabindex** attribute to a value that is greater than or equal to 0.</span></span>

## <a name="example"></a><span data-ttu-id="a19af-113">範例</span><span class="sxs-lookup"><span data-stu-id="a19af-113">Example</span></span>


```HTML
<div role="listbox" id="listbox1" tabindex="0" aria-activedescendant="listbox1-1"> 
       <div role="option" id="listbox1-1" class="selected">Item 1</div> 
       <div role="option" id="listbox1-2">Item 2</div> 

       <div role="option" id="listbox1-3">Item 3</div>
      ... 
<div>
```



## <a name="related-topics"></a><span data-ttu-id="a19af-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="a19af-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a19af-115">沒有作用中子系的 ARIA 容器角色 () Tabindex 錯誤</span><span class="sxs-lookup"><span data-stu-id="a19af-115">ARIA Container Role (without active descendant) Tabindex Error</span></span>](aria-container--no-active-descendant--tabindex.md)
</dt> </dl>

 

 




