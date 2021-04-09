---
title: 外觀程式設計參考
description: 外觀程式設計參考
ms.assetid: 914f6045-7252-4a06-a514-d31ef6d2d03b
keywords:
- Windows Media Player，外觀
- Windows Media Player 的外觀，程式設計參考
- 外觀，程式設計參考
- 外觀參考
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30194f0048f4ef66cf32b7c5f3f94c2bd4e190ab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671659"
---
# <a name="skin-programming-reference"></a><span data-ttu-id="5ca1d-107">外觀程式設計參考</span><span class="sxs-lookup"><span data-stu-id="5ca1d-107">Skin Programming Reference</span></span>

<span data-ttu-id="5ca1d-108">面板程式設計參考記錄下列專案及其相關聯的屬性、方法和事件。</span><span class="sxs-lookup"><span data-stu-id="5ca1d-108">The Skin Programming Reference documents the following elements and their associated attributes, methods, and events.</span></span>

<span data-ttu-id="5ca1d-109">除非另有說明，否則本節中的元素和屬性需要 Windows Media Player 7.0 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="5ca1d-109">The elements and attributes in this section require Windows Media Player 7.0 or later unless otherwise noted.</span></span>



| <span data-ttu-id="5ca1d-110">元素</span><span class="sxs-lookup"><span data-stu-id="5ca1d-110">Element</span></span>                                                  | <span data-ttu-id="5ca1d-111">描述</span><span class="sxs-lookup"><span data-stu-id="5ca1d-111">Description</span></span>                                                                         |
|----------------------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="5ca1d-112">環境屬性</span><span class="sxs-lookup"><span data-stu-id="5ca1d-112">Ambient Attributes</span></span>](ambient-attributes.md)             | <span data-ttu-id="5ca1d-113">套用至所有具有例外狀況之面板元素的屬性。</span><span class="sxs-lookup"><span data-stu-id="5ca1d-113">Attributes that apply to all skin elements with exceptions noted.</span></span>                   |
| [<span data-ttu-id="5ca1d-114">環境事件處理常式</span><span class="sxs-lookup"><span data-stu-id="5ca1d-114">Ambient Event Handlers</span></span>](ambient-event-handlers.md)     | <span data-ttu-id="5ca1d-115">可以由大部分的外觀元素所執行的事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="5ca1d-115">Event handlers that can be implemented by most skin elements.</span></span>                       |
| [<span data-ttu-id="5ca1d-116">環境事件屬性</span><span class="sxs-lookup"><span data-stu-id="5ca1d-116">Ambient Event Attributes</span></span>](ambient-event-attributes.md) | <span data-ttu-id="5ca1d-117">當引發事件時，詳細說明 Windows Media Player 狀態的屬性。</span><span class="sxs-lookup"><span data-stu-id="5ca1d-117">Attributes detailing the state of Windows Media Player when an event is fired.</span></span>      |
| [<span data-ttu-id="5ca1d-118">AUTOMENU</span><span class="sxs-lookup"><span data-stu-id="5ca1d-118">AUTOMENU</span></span>](automenu-element.md)                         | <span data-ttu-id="5ca1d-119">提供在面板中顯示快速存取面板的方法。</span><span class="sxs-lookup"><span data-stu-id="5ca1d-119">Provides a way to display the Quick Access Panel in a skin.</span></span>                         |
| [<span data-ttu-id="5ca1d-120">按鈕</span><span class="sxs-lookup"><span data-stu-id="5ca1d-120">BUTTON</span></span>](button-element.md)                             | <span data-ttu-id="5ca1d-121">獨立按鈕。</span><span class="sxs-lookup"><span data-stu-id="5ca1d-121">A standalone button.</span></span>                                                                |
| [<span data-ttu-id="5ca1d-122">BUTTONELEMENT</span><span class="sxs-lookup"><span data-stu-id="5ca1d-122">BUTTONELEMENT</span></span>](buttonelement-element.md)               | <span data-ttu-id="5ca1d-123">按鈕群組內的按鈕。</span><span class="sxs-lookup"><span data-stu-id="5ca1d-123">A button within a button group.</span></span>                                                     |
| [<span data-ttu-id="5ca1d-124">BUTTONGROUP</span><span class="sxs-lookup"><span data-stu-id="5ca1d-124">BUTTONGROUP</span></span>](buttongroup-element.md)                   | <span data-ttu-id="5ca1d-125">按鈕元素群組。</span><span class="sxs-lookup"><span data-stu-id="5ca1d-125">A group of button elements.</span></span>                                                         |
| [<span data-ttu-id="5ca1d-126">COLUMN</span><span class="sxs-lookup"><span data-stu-id="5ca1d-126">COLUMN</span></span>](column-element.md)                             | <span data-ttu-id="5ca1d-127">表示播放清單控制項內的資料行。</span><span class="sxs-lookup"><span data-stu-id="5ca1d-127">Represents a column within a playlist control.</span></span>                                      |
| [<span data-ttu-id="5ca1d-128">控制</span><span class="sxs-lookup"><span data-stu-id="5ca1d-128">CONTROLS</span></span>](controls-element.md)                         | <span data-ttu-id="5ca1d-129">提供從面板記憶體取 [控制項](controls-object.md) 物件的許可權。</span><span class="sxs-lookup"><span data-stu-id="5ca1d-129">Provides access to the [Controls](controls-object.md) object from within a skin.</span></span>   |
| [<span data-ttu-id="5ca1d-130">CUSTOMSLIDER</span><span class="sxs-lookup"><span data-stu-id="5ca1d-130">CUSTOMSLIDER</span></span>](customslider-element.md)                 | <span data-ttu-id="5ca1d-131">可自訂的滑杆控制項。</span><span class="sxs-lookup"><span data-stu-id="5ca1d-131">A customizable slider control.</span></span>                                                      |
| [<span data-ttu-id="5ca1d-132">編輯方塊</span><span class="sxs-lookup"><span data-stu-id="5ca1d-132">EDITBOX</span></span>](editbox-element.md)                           | <span data-ttu-id="5ca1d-133">提供一種方式，讓使用者在面板內輸入文字。</span><span class="sxs-lookup"><span data-stu-id="5ca1d-133">Provides a way for users to enter text within a skin.</span></span>                               |
| [<span data-ttu-id="5ca1d-134">影響</span><span class="sxs-lookup"><span data-stu-id="5ca1d-134">EFFECTS</span></span>](effects-element.md)                           | <span data-ttu-id="5ca1d-135">包含並控制效果集合的元素。</span><span class="sxs-lookup"><span data-stu-id="5ca1d-135">An element that contains and controls a collection of effects.</span></span>                      |
| [<span data-ttu-id="5ca1d-136">EQUALIZERSETTINGS</span><span class="sxs-lookup"><span data-stu-id="5ca1d-136">EQUALIZERSETTINGS</span></span>](equalizersettings-element.md)       | <span data-ttu-id="5ca1d-137">允許操作圖形等化器的元素。</span><span class="sxs-lookup"><span data-stu-id="5ca1d-137">An element allowing manipulation of the graphic equalizer.</span></span>                          |
| [<span data-ttu-id="5ca1d-138">專案</span><span class="sxs-lookup"><span data-stu-id="5ca1d-138">ITEM</span></span>](item-element.md)                                 | <span data-ttu-id="5ca1d-139">代表清單方塊或快顯控制項中的專案。</span><span class="sxs-lookup"><span data-stu-id="5ca1d-139">Represents an item in a list box or pop-up control.</span></span>                                 |
| [<span data-ttu-id="5ca1d-140">LISTBOX</span><span class="sxs-lookup"><span data-stu-id="5ca1d-140">LISTBOX</span></span>](listbox-element.md)                           | <span data-ttu-id="5ca1d-141">提供一種方式，讓使用者從清單中選取專案。</span><span class="sxs-lookup"><span data-stu-id="5ca1d-141">Provides a way for users to select items from a list.</span></span>                               |
| [<span data-ttu-id="5ca1d-142">球員</span><span class="sxs-lookup"><span data-stu-id="5ca1d-142">PLAYER</span></span>](player-element.md)                             | <span data-ttu-id="5ca1d-143">提供從面板內 [播放 Player](player-object.md) 物件的存取權。</span><span class="sxs-lookup"><span data-stu-id="5ca1d-143">Provides access to the [Player](player-object.md) object from within a skin.</span></span>       |
| [<span data-ttu-id="5ca1d-144">播放 清單</span><span class="sxs-lookup"><span data-stu-id="5ca1d-144">PLAYLIST</span></span>](playlist-element.md)                         | <span data-ttu-id="5ca1d-145">用來控制台內播放清單外觀的元素。</span><span class="sxs-lookup"><span data-stu-id="5ca1d-145">An element for controlling the appearance of a playlist within a skin.</span></span>              |
| [<span data-ttu-id="5ca1d-146">彈出</span><span class="sxs-lookup"><span data-stu-id="5ca1d-146">POPUP</span></span>](popup-element.md)                               | <span data-ttu-id="5ca1d-147">提供一種方式，讓使用者從清單中選取專案。</span><span class="sxs-lookup"><span data-stu-id="5ca1d-147">Provides a way for users to select items from a list.</span></span>                               |
| [<span data-ttu-id="5ca1d-148">PROGRESSBAR</span><span class="sxs-lookup"><span data-stu-id="5ca1d-148">PROGRESSBAR</span></span>](progressbar-element.md)                   | <span data-ttu-id="5ca1d-149">提供一種方式，以水準或垂直控制項顯示進度資訊。</span><span class="sxs-lookup"><span data-stu-id="5ca1d-149">Provides a way to display progress information in a horizontal or vertical control.</span></span> |
| [<span data-ttu-id="5ca1d-150">設定</span><span class="sxs-lookup"><span data-stu-id="5ca1d-150">SETTINGS</span></span>](settings-element.md)                         | <span data-ttu-id="5ca1d-151">提供從面板記憶體取 [設定](settings-object.md) 物件的許可權。</span><span class="sxs-lookup"><span data-stu-id="5ca1d-151">Provides access to the [Settings](settings-object.md) object from within a skin.</span></span>   |
| [<span data-ttu-id="5ca1d-152">滑 塊</span><span class="sxs-lookup"><span data-stu-id="5ca1d-152">SLIDER</span></span>](slider-element.md)                             | <span data-ttu-id="5ca1d-153">滑杆控制項。</span><span class="sxs-lookup"><span data-stu-id="5ca1d-153">A slider control.</span></span>                                                                   |
| [<span data-ttu-id="5ca1d-154">視圖</span><span class="sxs-lookup"><span data-stu-id="5ca1d-154">SUBVIEW</span></span>](subview-element.md)                           | <span data-ttu-id="5ca1d-155">可以移動或隱藏的視圖內的子區段。</span><span class="sxs-lookup"><span data-stu-id="5ca1d-155">Subsections within a view that can be moved or hidden.</span></span>                              |
| [<span data-ttu-id="5ca1d-156">文本</span><span class="sxs-lookup"><span data-stu-id="5ca1d-156">TEXT</span></span>](text-element.md)                                 | <span data-ttu-id="5ca1d-157">包含文字的控制項。</span><span class="sxs-lookup"><span data-stu-id="5ca1d-157">A control containing text.</span></span>                                                          |
| [<span data-ttu-id="5ca1d-158">主題</span><span class="sxs-lookup"><span data-stu-id="5ca1d-158">THEME</span></span>](theme-element.md)                               | <span data-ttu-id="5ca1d-159">識別面板檔案的主要元素。</span><span class="sxs-lookup"><span data-stu-id="5ca1d-159">The main element identifying a skin file.</span></span>                                           |
| [<span data-ttu-id="5ca1d-160">視頻</span><span class="sxs-lookup"><span data-stu-id="5ca1d-160">VIDEO</span></span>](video-element.md)                               | <span data-ttu-id="5ca1d-161">用來指定影片視窗外觀的元素。</span><span class="sxs-lookup"><span data-stu-id="5ca1d-161">An element for specifying the appearance of a video window.</span></span>                         |
| [<span data-ttu-id="5ca1d-162">VIDEOSETTINGS</span><span class="sxs-lookup"><span data-stu-id="5ca1d-162">VIDEOSETTINGS</span></span>](videosettings-element.md)               | <span data-ttu-id="5ca1d-163">允許控制各種影片設定的元素。</span><span class="sxs-lookup"><span data-stu-id="5ca1d-163">An element allowing control of various video settings.</span></span>                              |
| [<span data-ttu-id="5ca1d-164">VIEW</span><span class="sxs-lookup"><span data-stu-id="5ca1d-164">VIEW</span></span>](view-element.md)                                 | <span data-ttu-id="5ca1d-165">針對每個媒體類別，指定使用者介面 (UI) 的外觀。</span><span class="sxs-lookup"><span data-stu-id="5ca1d-165">Specifies what the user interface (UI) looks like for each category of media.</span></span>       |
| [<span data-ttu-id="5ca1d-166">其他</span><span class="sxs-lookup"><span data-stu-id="5ca1d-166">Miscellaneous</span></span>](miscellaneous.md)                       | <span data-ttu-id="5ca1d-167">用於建立面板的特製化屬性和其他主題。</span><span class="sxs-lookup"><span data-stu-id="5ca1d-167">Specialized attributes and other miscellaneous topics for use in creating skins.</span></span>    |



 

## <a name="related-topics"></a><span data-ttu-id="5ca1d-168">相關主題</span><span class="sxs-lookup"><span data-stu-id="5ca1d-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ca1d-169">**Windows Media Player 的外觀**</span><span class="sxs-lookup"><span data-stu-id="5ca1d-169">**Windows Media Player Skins**</span></span>](windows-media-player-skins.md)
</dt> </dl>

 

 




