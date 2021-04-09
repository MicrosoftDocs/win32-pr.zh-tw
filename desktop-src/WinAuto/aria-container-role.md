---
title: ARIA 容器角色錯誤
description: ARIA 容器角色錯誤
ms.assetid: AF207293-1172-43D0-B92C-C3070876DF54
keywords:
- AriaContainerRoleErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d02554c868816c05981fa9f008c8f79f0a3eb0f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932522"
---
# <a name="aria-container-role-error"></a><span data-ttu-id="6075b-104">ARIA 容器角色錯誤</span><span class="sxs-lookup"><span data-stu-id="6075b-104">ARIA Container Role Error</span></span>

## <a name="text"></a><span data-ttu-id="6075b-105">Text</span><span class="sxs-lookup"><span data-stu-id="6075b-105">Text</span></span>

<span data-ttu-id="6075b-106">已定義使用中子 **系的元素** 沒有容器角色 (**combobox**、 **方格**、 **listbox**、 **menu**、 **menubar**、 **radiogroup**、 **tree**、 **treegrid**、 **tablist**、 **row**) 。</span><span class="sxs-lookup"><span data-stu-id="6075b-106">Element with **active-descendant** defined does not have a container role (**combobox**, **grid**, **listbox**, **menu**, **menubar**, **radiogroup**, **tree**, **treegrid**, **tablist**, **row**).</span></span>

## <a name="type"></a><span data-ttu-id="6075b-107">類型</span><span class="sxs-lookup"><span data-stu-id="6075b-107">Type</span></span>

<span data-ttu-id="6075b-108">錯誤</span><span class="sxs-lookup"><span data-stu-id="6075b-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="6075b-109">描述</span><span class="sxs-lookup"><span data-stu-id="6075b-109">Description</span></span>

<span data-ttu-id="6075b-110">此錯誤適用于具有 **aria activedescendant** 屬性的元素。</span><span class="sxs-lookup"><span data-stu-id="6075b-110">This error applies to elements that have the **aria-activedescendant** attribute.</span></span>

<span data-ttu-id="6075b-111">元素似乎是已設定 **aria activedescendant** 屬性的容器，但元素的 role 屬性沒有對容器有效的值。</span><span class="sxs-lookup"><span data-stu-id="6075b-111">An element appears to be a container that has the **aria-activedescendant** attribute set, but the element's role attribute doesn’t have a value that is valid for a container.</span></span>

<span data-ttu-id="6075b-112">若要修正這個錯誤，請將 **角色** 屬性設定為 Web 協助工具方案可存取的豐富網際網路應用程式 (WAI-ARIA) 角色值對容器元素有效 **：下拉式方塊、\*\*\*\*方格**、 **listbox**、 **menu**、 **menubar**、 **radiogroup**、 **tablist**、 **tree** 或 **treegrid**。</span><span class="sxs-lookup"><span data-stu-id="6075b-112">To fix this error, set the **role** attribute to a Web Accessibility Initiative - Accessible Rich Internet Applications (WAI-ARIA) role value that is valid for a container element: **combobox**, **grid**, **listbox**, **menu**, **menubar**, **radiogroup**, **tablist**, **tree**, or **treegrid**.</span></span>

## <a name="example"></a><span data-ttu-id="6075b-113">範例</span><span class="sxs-lookup"><span data-stu-id="6075b-113">Example</span></span>


```HTML
<div role="listbox" id="listbox1" tabindex="0" aria-activedescendant="listbox1-1">
  <div role="option" id="listbox1-1" class="selected">Item 1</div>
  <div role="option" id="listbox1-2">Item 2</div>
  <div role="option" id="listbox1-3">Item 3</div>
  ...
<div>
```



## <a name="related-topics"></a><span data-ttu-id="6075b-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="6075b-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6075b-115">ARIA 角色錯誤</span><span class="sxs-lookup"><span data-stu-id="6075b-115">ARIA Role Error</span></span>](aria-role-invalid.md)
</dt> </dl>

 

 




