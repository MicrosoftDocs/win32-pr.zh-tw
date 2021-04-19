---
title: '工具列擴充樣式 (CommCtrl .h) '
description: 本節列出工具列控制項支援的延伸樣式。
ms.assetid: da31dbbf-8d0a-4711-a1af-382c62e653cd
topic_type:
- apiref
api_name:
- TBSTYLE_EX_DRAWDDARROWS
- TBSTYLE_EX_HIDECLIPPEDBUTTONS
- TBSTYLE_EX_DOUBLEBUFFER
- TBSTYLE_EX_MIXEDBUTTONS
- TBSTYLE_EX_MULTICOLUMN
- TBSTYLE_EX_VERTICAL
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 056e48753485364017f04f7b84e609b19473bf5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994029"
---
# <a name="toolbar-extended-styles"></a><span data-ttu-id="a45f8-103">工具列擴充樣式</span><span class="sxs-lookup"><span data-stu-id="a45f8-103">Toolbar Extended Styles</span></span>

<span data-ttu-id="a45f8-104">本節列出工具列控制項支援的延伸樣式。</span><span class="sxs-lookup"><span data-stu-id="a45f8-104">This section lists the extended styles supported by toolbar controls.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="a45f8-105">常數</span><span class="sxs-lookup"><span data-stu-id="a45f8-105">Constant</span></span></th>
<th style="text-align: left;"><span data-ttu-id="a45f8-106">描述</span><span class="sxs-lookup"><span data-stu-id="a45f8-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="TBSTYLE_EX_DRAWDDARROWS"></span><span id="tbstyle_ex_drawddarrows"></span><dl> <span data-ttu-id="a45f8-107"><dt><strong>TBSTYLE_EX_DRAWDDARROWS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a45f8-107"><dt><strong>TBSTYLE_EX_DRAWDDARROWS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="a45f8-108"><a href="common-control-versions.md">版本 4.71</a>。</span><span class="sxs-lookup"><span data-stu-id="a45f8-108"><a href="common-control-versions.md">Version 4.71</a>.</span></span> <span data-ttu-id="a45f8-109">此樣式可讓按鈕具有個別的下拉式箭號。</span><span class="sxs-lookup"><span data-stu-id="a45f8-109">This style allows buttons to have a separate dropdown arrow.</span></span> <span data-ttu-id="a45f8-110">具有 <a href="toolbar-control-and-button-styles.md"><strong>BTNS_DROPDOWN</strong></a> 樣式的按鈕會以下拉式箭號繪製在按鈕右邊的個別區段中。</span><span class="sxs-lookup"><span data-stu-id="a45f8-110">Buttons that have the <a href="toolbar-control-and-button-styles.md"><strong>BTNS_DROPDOWN</strong></a> style will be drawn with a dropdown arrow in a separate section, to the right of the button.</span></span> <span data-ttu-id="a45f8-111">如果按一下箭號，則只會按下按鈕的箭號部分，而工具列控制項會傳送 <a href="tbn-dropdown.md">TBN_DROPDOWN</a> 的通知碼，以提示應用程式顯示下拉式功能表。</span><span class="sxs-lookup"><span data-stu-id="a45f8-111">If the arrow is clicked, only the arrow portion of the button will depress, and the toolbar control will send a <a href="tbn-dropdown.md">TBN_DROPDOWN</a> notification code to prompt the application to display the dropdown menu.</span></span> <span data-ttu-id="a45f8-112">如果按一下按鈕的主要部分，工具列控制項會傳送具有按鈕識別碼的 WM_COMMAND 訊息。</span><span class="sxs-lookup"><span data-stu-id="a45f8-112">If the main part of the button is clicked, the toolbar control sends a WM_COMMAND message with the button's ID.</span></span> <span data-ttu-id="a45f8-113">應用程式通常會透過啟動功能表上的第一個命令來回應。</span><span class="sxs-lookup"><span data-stu-id="a45f8-113">The application normally responds by launching the first command on the menu.</span></span><br/> <span data-ttu-id="a45f8-114">在許多情況下，您可能只想要在具有分隔箭號的工具列上有一些下拉式按鈕。</span><span class="sxs-lookup"><span data-stu-id="a45f8-114">There are many situations where you may want to have only some of the dropdown buttons on a toolbar with separated arrows.</span></span> <span data-ttu-id="a45f8-115">若要這樣做，請設定 TBSTYLE_EX_DRAWDDARROWS 延伸樣式。</span><span class="sxs-lookup"><span data-stu-id="a45f8-115">To do so, set the TBSTYLE_EX_DRAWDDARROWS extended style.</span></span> <span data-ttu-id="a45f8-116">將沒有 <a href="toolbar-control-and-button-styles.md"><strong>BTNS_WHOLEDROPDOWN</strong></a> 樣式的分隔箭號提供給那些按鈕。</span><span class="sxs-lookup"><span data-stu-id="a45f8-116">Give those buttons that will not have separated arrows the <a href="toolbar-control-and-button-styles.md"><strong>BTNS_WHOLEDROPDOWN</strong></a> style.</span></span> <span data-ttu-id="a45f8-117">具有此樣式的按鈕會在影像旁邊顯示箭號。</span><span class="sxs-lookup"><span data-stu-id="a45f8-117">Buttons with this style will have an arrow displayed next to the image.</span></span> <span data-ttu-id="a45f8-118">不過，箭號不會分開，而且按一下按鈕的任何部分時，工具列控制項會傳送 <a href="tbn-dropdown.md">TBN_DROPDOWN</a> 的通知碼。</span><span class="sxs-lookup"><span data-stu-id="a45f8-118">However, the arrow will not be separate and when any part of the button is clicked, the toolbar control will send a <a href="tbn-dropdown.md">TBN_DROPDOWN</a> notification code.</span></span> <span data-ttu-id="a45f8-119">若要避免重新繪製問題，應該先設定此樣式，然後才會顯示工具列控制項。</span><span class="sxs-lookup"><span data-stu-id="a45f8-119">To prevent repainting problems, this style should be set before the toolbar control becomes visible.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="TBSTYLE_EX_HIDECLIPPEDBUTTONS"></span><span id="tbstyle_ex_hideclippedbuttons"></span><dl> <span data-ttu-id="a45f8-120"><dt><strong>TBSTYLE_EX_HIDECLIPPEDBUTTONS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a45f8-120"><dt><strong>TBSTYLE_EX_HIDECLIPPEDBUTTONS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="a45f8-121"><a href="common-control-versions.md">版本 5.81</a>。</span><span class="sxs-lookup"><span data-stu-id="a45f8-121"><a href="common-control-versions.md">Version 5.81</a>.</span></span> <span data-ttu-id="a45f8-122">此樣式會隱藏部分裁剪的按鈕。</span><span class="sxs-lookup"><span data-stu-id="a45f8-122">This style hides partially clipped buttons.</span></span> <span data-ttu-id="a45f8-123">此樣式最常見的用法是針對屬於 Rebar 控制項一部分的工具列。</span><span class="sxs-lookup"><span data-stu-id="a45f8-123">The most common use of this style is for toolbars that are part of a rebar control.</span></span> <span data-ttu-id="a45f8-124">如果連續的頻外涵蓋某個按鈕的一部分，將不會顯示該按鈕。</span><span class="sxs-lookup"><span data-stu-id="a45f8-124">If an adjacent band covers part of a button, the button will not be displayed.</span></span> <span data-ttu-id="a45f8-125">但是，如果 Rebar 帶 <a href="/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa"><strong>RBBS_USECHEVRON</strong></a> 樣式，則按鈕會顯示在箭號的下拉式功能表中。</span><span class="sxs-lookup"><span data-stu-id="a45f8-125">However, if the rebar band has the <a href="/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa"><strong>RBBS_USECHEVRON</strong></a> style, the button will be displayed on the chevron's dropdown menu.</span></span> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="TBSTYLE_EX_DOUBLEBUFFER"></span><span id="tbstyle_ex_doublebuffer"></span><dl> <span data-ttu-id="a45f8-126"><dt><strong>TBSTYLE_EX_DOUBLEBUFFER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a45f8-126"><dt><strong>TBSTYLE_EX_DOUBLEBUFFER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="a45f8-127"><a href="common-control-versions.md">第6版</a>。</span><span class="sxs-lookup"><span data-stu-id="a45f8-127"><a href="common-control-versions.md">Version 6</a>.</span></span> <span data-ttu-id="a45f8-128">此樣式需要將工具列雙重緩衝。</span><span class="sxs-lookup"><span data-stu-id="a45f8-128">This style requires the toolbar to be double buffered.</span></span> <span data-ttu-id="a45f8-129">雙重緩衝是一種機制，可偵測工具列何時變更。</span><span class="sxs-lookup"><span data-stu-id="a45f8-129">Double buffering is a mechanism that detects when the toolbar has changed.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="a45f8-130">Comctl32.dll 第6版不是可轉散發套件，但包含在 Windows 或更新版本中。</span><span class="sxs-lookup"><span data-stu-id="a45f8-130">Comctl32.dll version 6 is not redistributable but it is included in Windows or later.</span></span> <span data-ttu-id="a45f8-131">若要使用 Comctl32.dll 第6版，請在資訊清單中指定它。</span><span class="sxs-lookup"><span data-stu-id="a45f8-131">To use Comctl32.dll version 6, specify it in a manifest.</span></span> <span data-ttu-id="a45f8-132">如需資訊清單的詳細資訊，請參閱 <a href="cookbook-overview.md">啟用視覺化樣式</a>。</span><span class="sxs-lookup"><span data-stu-id="a45f8-132">For more information on manifests, see <a href="cookbook-overview.md">Enabling Visual Styles</a>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="TBSTYLE_EX_MIXEDBUTTONS"></span><span id="tbstyle_ex_mixedbuttons"></span><dl> <span data-ttu-id="a45f8-133"><dt><strong>TBSTYLE_EX_MIXEDBUTTONS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a45f8-133"><dt><strong>TBSTYLE_EX_MIXEDBUTTONS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="a45f8-134"><a href="common-control-versions.md">版本 5.81</a>。</span><span class="sxs-lookup"><span data-stu-id="a45f8-134"><a href="common-control-versions.md">Version 5.81</a>.</span></span> <span data-ttu-id="a45f8-135">此樣式可讓您設定所有按鈕的文字，但只會顯示具有 [ <a href="toolbar-control-and-button-styles.md"><strong>BTNS_SHOWTEXT</strong></a> ] 按鈕樣式的按鈕。</span><span class="sxs-lookup"><span data-stu-id="a45f8-135">This style allows you to set text for all buttons, but only display it for those buttons with the <a href="toolbar-control-and-button-styles.md"><strong>BTNS_SHOWTEXT</strong></a> button style.</span></span> <span data-ttu-id="a45f8-136">您也必須設定 <a href="toolbar-control-and-button-styles.md"><strong>TBSTYLE_LIST</strong></a> 的樣式。</span><span class="sxs-lookup"><span data-stu-id="a45f8-136">The <a href="toolbar-control-and-button-styles.md"><strong>TBSTYLE_LIST</strong></a> style must also be set.</span></span> <span data-ttu-id="a45f8-137">一般來說，當按鈕未顯示文字時，您的應用程式必須處理 <a href="tbn-getinfotip.md">TBN_GETINFOTIP</a> 或 <a href="ttn-getdispinfo.md">TTN_GETDISPINFO</a> ，才能顯示工具提示。</span><span class="sxs-lookup"><span data-stu-id="a45f8-137">Normally, when a button does not display text, your application must handle <a href="tbn-getinfotip.md">TBN_GETINFOTIP</a> or <a href="ttn-getdispinfo.md">TTN_GETDISPINFO</a> to display a tooltip.</span></span> <span data-ttu-id="a45f8-138">使用 TBSTYLE_EX_MIXEDBUTTONS 擴充樣式，已設定但未顯示在按鈕上的文字將會自動做為按鈕的工具提示文字使用。</span><span class="sxs-lookup"><span data-stu-id="a45f8-138">With the TBSTYLE_EX_MIXEDBUTTONS extended style, text that is set but not displayed on a button will automatically be used as the button's tooltip text.</span></span> <span data-ttu-id="a45f8-139">如果您的應用程式需要更多的彈性來指定工具提示文字，則只需要處理 TBN_GETINFOTIP 或 TTN_GETDISPINFO。</span><span class="sxs-lookup"><span data-stu-id="a45f8-139">Your application only needs to handle TBN_GETINFOTIP or or TTN_GETDISPINFO if it needs more flexibility in specifying the tooltip text.</span></span> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="TBSTYLE_EX_MULTICOLUMN"></span><span id="tbstyle_ex_multicolumn"></span><dl> <span data-ttu-id="a45f8-140"><dt><strong>TBSTYLE_EX_MULTICOLUMN</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a45f8-140"><dt><strong>TBSTYLE_EX_MULTICOLUMN</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="a45f8-141"><a href="common-control-versions.md">版本 5.82</a>。</span><span class="sxs-lookup"><span data-stu-id="a45f8-141"><a href="common-control-versions.md">Version 5.82</a>.</span></span> <span data-ttu-id="a45f8-142"><strong>適用于內部用途;不建議在應用程式中使用。</strong></span><span class="sxs-lookup"><span data-stu-id="a45f8-142"><strong>Intended for internal use; not recommended for use in applications.</strong></span></span> <span data-ttu-id="a45f8-143">此樣式可讓工具列成為垂直方向，並將工具列按鈕組織成資料行。</span><span class="sxs-lookup"><span data-stu-id="a45f8-143">This style gives the toolbar a vertical orientation and organizes the toolbar buttons into columns.</span></span> <span data-ttu-id="a45f8-144">按鈕會垂直往下傳送，直到按鈕超過工具列的周框高度為止 (請參閱 <a href="tb-setboundingsize.md"><strong>TB_SETBOUNDINGSIZE</strong></a>) ，然後再建立新的資料行。</span><span class="sxs-lookup"><span data-stu-id="a45f8-144">The buttons flow down vertically until a button has exceeded the bounding height of the toolbar (see <a href="tb-setboundingsize.md"><strong>TB_SETBOUNDINGSIZE</strong></a>), and then a new column is created.</span></span> <span data-ttu-id="a45f8-145">工具列會以這種方式來流動按鈕，直到所有按鈕都定位為止。</span><span class="sxs-lookup"><span data-stu-id="a45f8-145">The toolbar flows the buttons in this manner until all buttons are positioned.</span></span> <span data-ttu-id="a45f8-146">若要使用這個樣式，也必須設定 TBSTYLE_EX_VERTICAL 的樣式。</span><span class="sxs-lookup"><span data-stu-id="a45f8-146">To use this style, the TBSTYLE_EX_VERTICAL style must also be set.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="a45f8-147">未來的 Comctl32.dll 版本可能不支援這個樣式。</span><span class="sxs-lookup"><span data-stu-id="a45f8-147">This style may not be supported in future versions of Comctl32.dll.</span></span> <span data-ttu-id="a45f8-148">此外，這個樣式不會在 commctrl 中定義。</span><span class="sxs-lookup"><span data-stu-id="a45f8-148">Also, this style is not defined in commctrl.h.</span></span> <span data-ttu-id="a45f8-149">將下列定義新增至您應用程式的原始程式檔，以使用此樣式： <code>#define TBSTYLE_EX_MULTICOLUMN 0x00000002</code>
</span><span class="sxs-lookup"><span data-stu-id="a45f8-149">Add the following definition to the source files of your application to use this style: <code>#define TBSTYLE_EX_MULTICOLUMN 0x00000002</code>
</span></span></blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="TBSTYLE_EX_VERTICAL"></span><span id="tbstyle_ex_vertical"></span><dl> <span data-ttu-id="a45f8-150"><dt><strong>TBSTYLE_EX_VERTICAL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a45f8-150"><dt><strong>TBSTYLE_EX_VERTICAL</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="a45f8-151"><a href="common-control-versions.md">版本 5.82</a>。</span><span class="sxs-lookup"><span data-stu-id="a45f8-151"><a href="common-control-versions.md">Version 5.82</a>.</span></span> <span data-ttu-id="a45f8-152"><strong>適用于內部用途;不建議在應用程式中使用。</strong></span><span class="sxs-lookup"><span data-stu-id="a45f8-152"><strong>Intended for internal use; not recommended for use in applications.</strong></span></span> <span data-ttu-id="a45f8-153">此樣式可讓工具列成為垂直方向。</span><span class="sxs-lookup"><span data-stu-id="a45f8-153">This style gives the toolbar a vertical orientation.</span></span> <span data-ttu-id="a45f8-154">工具列按鈕是從上到下，而不是水準方向。</span><span class="sxs-lookup"><span data-stu-id="a45f8-154">Toolbar buttons flow from top to bottom instead of horizontally.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="a45f8-155">未來的 Comctl32.dll 版本可能不支援這個樣式。</span><span class="sxs-lookup"><span data-stu-id="a45f8-155">This style may not be supported in future versions of Comctl32.dll.</span></span> <span data-ttu-id="a45f8-156">此外，這個樣式不會在 commctrl 中定義。</span><span class="sxs-lookup"><span data-stu-id="a45f8-156">Also, this style is not defined in commctrl.h.</span></span> <span data-ttu-id="a45f8-157">將下列定義新增至您應用程式的原始程式檔，以使用此樣式： <code>#define TBSTYLE_EX_VERTICAL 0x00000004</code>
</span><span class="sxs-lookup"><span data-stu-id="a45f8-157">Add the following definition to the source files of your application to use this style: <code>#define TBSTYLE_EX_VERTICAL 0x00000004</code>
</span></span></blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="a45f8-158">備註</span><span class="sxs-lookup"><span data-stu-id="a45f8-158">Remarks</span></span>

<span data-ttu-id="a45f8-159">若要設定擴充樣式，請將 [工具列] 控制項傳送至 [ [**TB] \_ SETEXTENDEDSTYLE**](tb-setextendedstyle.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="a45f8-159">To set an extended style, send the toolbar control a [**TB\_SETEXTENDEDSTYLE**](tb-setextendedstyle.md) message.</span></span> <span data-ttu-id="a45f8-160">若要判斷目前設定的擴充樣式，請傳送 [**TB 的 \_ GETEXTENDEDSTYLE**](tb-getextendedstyle.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="a45f8-160">To determine what extended styles are currently set, send a [**TB\_GETEXTENDEDSTYLE**](tb-getextendedstyle.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="a45f8-161">規格需求</span><span class="sxs-lookup"><span data-stu-id="a45f8-161">Requirements</span></span>



| <span data-ttu-id="a45f8-162">需求</span><span class="sxs-lookup"><span data-stu-id="a45f8-162">Requirement</span></span> | <span data-ttu-id="a45f8-163">值</span><span class="sxs-lookup"><span data-stu-id="a45f8-163">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a45f8-164">標頭</span><span class="sxs-lookup"><span data-stu-id="a45f8-164">Header</span></span><br/> | <dl> <span data-ttu-id="a45f8-165"><dt>CommCtrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="a45f8-165"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 





