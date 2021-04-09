---
title: 主題元素
description: 主題元素
ms.assetid: fe7e793e-1774-412c-aed2-721ed2cf1bb3
keywords:
- Windows Media Player 的外觀，主題元素
- 外觀，主題元素
- 主題元素
- 外觀的參考，主題元素
- 元素，主題
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8cd0d40b4b020cf5416569417401af9e4f3a33b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839644"
---
# <a name="theme-element"></a><span data-ttu-id="dbd55-108">主題元素</span><span class="sxs-lookup"><span data-stu-id="dbd55-108">THEME Element</span></span>

<span data-ttu-id="dbd55-109">**主題** 元素是面板的父層級元素，並包含一或多個 **VIEW** 元素，這些元素接著會包含面板中的所有其他專案。</span><span class="sxs-lookup"><span data-stu-id="dbd55-109">The **THEME** element is the parent-level element of a skin, and contains one or more **VIEW** elements, which in turn contain all other elements within a skin.</span></span> <span data-ttu-id="dbd55-110">在腳本程式碼中，**主題** 專案是透過 **主題** 全域屬性來存取，而不是透過 [**主題**] 專案不支援的 **識別碼** 屬性所指定的名稱來存取。</span><span class="sxs-lookup"><span data-stu-id="dbd55-110">Within script code, the **THEME** element is accessed through the **theme** global attribute rather than through a name specified by an **id** attribute, which is not supported by the **THEME** element.</span></span>

<span data-ttu-id="dbd55-111">**主題** 元素支援下列屬性。</span><span class="sxs-lookup"><span data-stu-id="dbd55-111">The **THEME** element supports the following attributes.</span></span>



| <span data-ttu-id="dbd55-112">屬性</span><span class="sxs-lookup"><span data-stu-id="dbd55-112">Attribute</span></span>                                | <span data-ttu-id="dbd55-113">描述</span><span class="sxs-lookup"><span data-stu-id="dbd55-113">Description</span></span>                                                                                                                     |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dbd55-114">作者</span><span class="sxs-lookup"><span data-stu-id="dbd55-114">author</span></span>](theme-author.md)               | <span data-ttu-id="dbd55-115">指定或抓取面板的作者名稱。</span><span class="sxs-lookup"><span data-stu-id="dbd55-115">Specifies or retrieves the name of the author of the skin.</span></span>                                                                      |
| [<span data-ttu-id="dbd55-116">authorVersion</span><span class="sxs-lookup"><span data-stu-id="dbd55-116">authorVersion</span></span>](theme-authorversion.md) | <span data-ttu-id="dbd55-117">指定或抓取作者指派的面板版本號碼。</span><span class="sxs-lookup"><span data-stu-id="dbd55-117">Specifies or retrieves the version number of the skin as assigned by the author.</span></span>                                                |
| [<span data-ttu-id="dbd55-118">版權</span><span class="sxs-lookup"><span data-stu-id="dbd55-118">copyright</span></span>](theme-copyright.md)         | <span data-ttu-id="dbd55-119">指定或抓取面板的著作權字串。</span><span class="sxs-lookup"><span data-stu-id="dbd55-119">Specifies or retrieves the copyright string for the skin.</span></span>                                                                       |
| [<span data-ttu-id="dbd55-120">currentViewID</span><span class="sxs-lookup"><span data-stu-id="dbd55-120">currentViewID</span></span>](theme-currentviewid.md) | <span data-ttu-id="dbd55-121">指定或抓取目前顯示的 **視圖**。</span><span class="sxs-lookup"><span data-stu-id="dbd55-121">Specifies or retrieves the currently displayed **VIEW**.</span></span>                                                                        |
| [<span data-ttu-id="dbd55-122">title</span><span class="sxs-lookup"><span data-stu-id="dbd55-122">title</span></span>](theme-title.md)                 | <span data-ttu-id="dbd55-123">指定或抓取面板的標題。</span><span class="sxs-lookup"><span data-stu-id="dbd55-123">Specifies or retrieves the title of the skin.</span></span>                                                                                   |
| [<span data-ttu-id="dbd55-124">version</span><span class="sxs-lookup"><span data-stu-id="dbd55-124">version</span></span>](theme-version.md)             | <span data-ttu-id="dbd55-125">指定或抓取用來撰寫面板的 Windows Media Player 版本號碼。</span><span class="sxs-lookup"><span data-stu-id="dbd55-125">Specifies or retrieves the Windows Media Player version number for which the skin was authored.</span></span> <span data-ttu-id="dbd55-126">只能在設計階段設定。</span><span class="sxs-lookup"><span data-stu-id="dbd55-126">Can only be set at design time.</span></span> |



 

<span data-ttu-id="dbd55-127">**主題** 元素支援下列方法。</span><span class="sxs-lookup"><span data-stu-id="dbd55-127">The **THEME** element supports the following methods.</span></span>



| <span data-ttu-id="dbd55-128">方法</span><span class="sxs-lookup"><span data-stu-id="dbd55-128">Method</span></span>                                         | <span data-ttu-id="dbd55-129">描述</span><span class="sxs-lookup"><span data-stu-id="dbd55-129">Description</span></span>                                                                                                     |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dbd55-130">closeView</span><span class="sxs-lookup"><span data-stu-id="dbd55-130">closeView</span></span>](theme-closeview.md)               | <span data-ttu-id="dbd55-131">關閉開啟的 **視圖**。</span><span class="sxs-lookup"><span data-stu-id="dbd55-131">Closes an open **VIEW**.</span></span>                                                                                        |
| [<span data-ttu-id="dbd55-132">loadPreference</span><span class="sxs-lookup"><span data-stu-id="dbd55-132">loadPreference</span></span>](theme-loadpreference.md)     | <span data-ttu-id="dbd55-133">從登錄載入喜好設定。</span><span class="sxs-lookup"><span data-stu-id="dbd55-133">Loads a preference from the registry.</span></span>                                                                           |
| [<span data-ttu-id="dbd55-134">logString</span><span class="sxs-lookup"><span data-stu-id="dbd55-134">logString</span></span>](theme-logstring.md)               | <span data-ttu-id="dbd55-135">如果啟用記錄功能，則將使用者定義的字串記錄至錯誤檔。</span><span class="sxs-lookup"><span data-stu-id="dbd55-135">Logs a user-defined string to the error file, if logging is enabled.</span></span>                                            |
| [<span data-ttu-id="dbd55-136">openDialog</span><span class="sxs-lookup"><span data-stu-id="dbd55-136">openDialog</span></span>](theme-opendialog.md)             | <span data-ttu-id="dbd55-137">開啟 [檔案] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="dbd55-137">Opens a file dialog box.</span></span>                                                                                        |
| [<span data-ttu-id="dbd55-138">openView</span><span class="sxs-lookup"><span data-stu-id="dbd55-138">openView</span></span>](theme-openview.md)                 | <span data-ttu-id="dbd55-139">在新視窗中開啟一個 **VIEW** 。</span><span class="sxs-lookup"><span data-stu-id="dbd55-139">Opens a **VIEW** in a new window.</span></span>                                                                               |
| [<span data-ttu-id="dbd55-140">openViewRelative</span><span class="sxs-lookup"><span data-stu-id="dbd55-140">openViewRelative</span></span>](theme-openviewrelative.md) | <span data-ttu-id="dbd55-141">在相對於面板左上角的指定初始位置，在新視窗中開啟一個 **VIEW** 。</span><span class="sxs-lookup"><span data-stu-id="dbd55-141">Opens a **VIEW** in a new window at a specified initial position relative to the upper-left corner of the skin.</span></span> |
| [<span data-ttu-id="dbd55-142">playSound</span><span class="sxs-lookup"><span data-stu-id="dbd55-142">playSound</span></span>](theme-playsound.md)               | <span data-ttu-id="dbd55-143">播放指定的音效檔。</span><span class="sxs-lookup"><span data-stu-id="dbd55-143">Plays the specified sound file.</span></span>                                                                                 |
| [<span data-ttu-id="dbd55-144">savePreference</span><span class="sxs-lookup"><span data-stu-id="dbd55-144">savePreference</span></span>](theme-savepreference.md)     | <span data-ttu-id="dbd55-145">將喜好設定儲存在登錄中。</span><span class="sxs-lookup"><span data-stu-id="dbd55-145">Saves a preference in the registry.</span></span>                                                                             |
| [<span data-ttu-id="dbd55-146">showErrorDialog</span><span class="sxs-lookup"><span data-stu-id="dbd55-146">showErrorDialog</span></span>](theme-showerrordialog.md)   | <span data-ttu-id="dbd55-147">顯示 [標準錯誤] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="dbd55-147">Displays the standard error dialog box.</span></span>                                                                         |



 

<span data-ttu-id="dbd55-148">**主題** 元素不支援事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="dbd55-148">The **THEME** element does not support event handlers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dbd55-149">相關主題</span><span class="sxs-lookup"><span data-stu-id="dbd55-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dbd55-150">**外觀程式設計參考**</span><span class="sxs-lookup"><span data-stu-id="dbd55-150">**Skin Programming Reference**</span></span>](skin-programming-reference.md)
</dt> </dl>

 

 




