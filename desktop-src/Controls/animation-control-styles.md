---
title: '動畫控制項樣式 (CommCtrl .h) '
description: 此區段會列出與動畫控制項搭配使用的視窗樣式。
ms.assetid: ad4fc4fd-166d-4871-9f60-5133a48681aa
topic_type:
- apiref
api_name:
- ACS_AUTOPLAY
- ACS_CENTER
- ACS_TIMER
- ACS_TRANSPARENT
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d779b92c51420bc6bd9ad238bcff538dbc85841f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976053"
---
# <a name="animation-control-styles"></a><span data-ttu-id="587f5-103">動畫控制項樣式</span><span class="sxs-lookup"><span data-stu-id="587f5-103">Animation Control Styles</span></span>

<span data-ttu-id="587f5-104">此區段會列出與動畫控制項搭配使用的視窗樣式。</span><span class="sxs-lookup"><span data-stu-id="587f5-104">This section lists the window styles used with animation controls.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="587f5-105">常數</span><span class="sxs-lookup"><span data-stu-id="587f5-105">Constant</span></span></th>
<th style="text-align: left;"><span data-ttu-id="587f5-106">描述</span><span class="sxs-lookup"><span data-stu-id="587f5-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="ACS_AUTOPLAY"></span><span id="acs_autoplay"></span><dl> <span data-ttu-id="587f5-107"><dt><strong>ACS_AUTOPLAY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="587f5-107"><dt><strong>ACS_AUTOPLAY</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="587f5-108">當 AVI 剪輯開啟時，就會立即開始播放動畫。</span><span class="sxs-lookup"><span data-stu-id="587f5-108">Starts playing the animation as soon as the AVI clip is opened.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ACS_CENTER"></span><span id="acs_center"></span><dl> <span data-ttu-id="587f5-109"><dt><strong>ACS_CENTER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="587f5-109"><dt><strong>ACS_CENTER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="587f5-110">在動畫控制項的視窗中將動畫置中。</span><span class="sxs-lookup"><span data-stu-id="587f5-110">Centers the animation in the animation control's window.</span></span> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ACS_TIMER"></span><span id="acs_timer"></span><dl> <span data-ttu-id="587f5-111"><dt><strong>ACS_TIMER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="587f5-111"><dt><strong>ACS_TIMER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="587f5-112">根據預設，控制項會建立執行緒來播放 AVI 剪輯。</span><span class="sxs-lookup"><span data-stu-id="587f5-112">By default, the control creates a thread to play the AVI clip.</span></span> <span data-ttu-id="587f5-113">如果設定此旗標，控制項會在不建立執行緒的情況下播放剪輯;在內部，控制項會使用 Win32 計時器來同步播放。</span><span class="sxs-lookup"><span data-stu-id="587f5-113">If you set this flag, the control plays the clip without creating a thread; internally the control uses a Win32 timer to synchronize playback.</span></span> <br/> <span data-ttu-id="587f5-114"><strong>Comctl32.dll 第6版和更新版本：</strong> 不支援這個樣式。</span><span class="sxs-lookup"><span data-stu-id="587f5-114"><strong>Comctl32.dll version 6 and later:</strong> This style is not supported.</span></span> <span data-ttu-id="587f5-115">依預設，此控制項會在不建立執行緒的情況下，播放 AVI 剪輯。</span><span class="sxs-lookup"><span data-stu-id="587f5-115">By default, the control plays the AVI clip without creating a thread.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="587f5-116">Comctl32.dll 第6版無法轉散發。</span><span class="sxs-lookup"><span data-stu-id="587f5-116">Comctl32.dll version 6 is not redistributable.</span></span> <span data-ttu-id="587f5-117">若要使用 Comctl32.dll 第6版，請在資訊清單中指定它。</span><span class="sxs-lookup"><span data-stu-id="587f5-117">To use Comctl32.dll version 6, specify it in a manifest.</span></span> <span data-ttu-id="587f5-118">如需資訊清單的詳細資訊，請參閱 <a href="cookbook-overview.md">啟用視覺化樣式</a>。</span><span class="sxs-lookup"><span data-stu-id="587f5-118">For more information on manifests, see <a href="cookbook-overview.md">Enabling Visual Styles</a>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ACS_TRANSPARENT"></span><span id="acs_transparent"></span><dl> <span data-ttu-id="587f5-119"><dt><strong>ACS_TRANSPARENT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="587f5-119"><dt><strong>ACS_TRANSPARENT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="587f5-120">可讓您將動畫的背景色彩與基礎視窗的色彩進行比對，以建立 &quot; 透明 &quot; 背景。</span><span class="sxs-lookup"><span data-stu-id="587f5-120">Allows you to match an animation's background color to that of the underlying window, creating a &quot;transparent&quot; background.</span></span> <span data-ttu-id="587f5-121">動畫控制項的父系不能有 WS_CLIPCHILDREN 樣式 (請參閱 <a href="/windows/desktop/winmsg/window-styles">視窗樣式</a>) 。</span><span class="sxs-lookup"><span data-stu-id="587f5-121">The parent of the animation control must not have the WS_CLIPCHILDREN style (see <a href="/windows/desktop/winmsg/window-styles">Window Styles</a>).</span></span> <span data-ttu-id="587f5-122">控制項會將 <a href="wm-ctlcolorstatic.md"><strong>WM_CTLCOLORSTATIC</strong></a> 訊息傳送到其父系。</span><span class="sxs-lookup"><span data-stu-id="587f5-122">The control sends a <a href="wm-ctlcolorstatic.md"><strong>WM_CTLCOLORSTATIC</strong></a> message to its parent.</span></span> <span data-ttu-id="587f5-123">使用 <a href="/windows/desktop/api/wingdi/nf-wingdi-setbkcolor"><strong>SetBkColor</strong></a> 將裝置內容的背景色彩設定為適當的值。</span><span class="sxs-lookup"><span data-stu-id="587f5-123">Use <a href="/windows/desktop/api/wingdi/nf-wingdi-setbkcolor"><strong>SetBkColor</strong></a> to set the background color for the device context to an appropriate value.</span></span> <span data-ttu-id="587f5-124">控制項會將第一個框架的左上角圖元解釋為動畫的預設背景色彩。</span><span class="sxs-lookup"><span data-stu-id="587f5-124">The control interprets the upper-left pixel of the first frame as the animation's default background color.</span></span> <span data-ttu-id="587f5-125">它會將該色彩的所有圖元重新對應到您在回應 WM_CTLCOLORSTATIC 時所提供的值。</span><span class="sxs-lookup"><span data-stu-id="587f5-125">It will remap all pixels with that color to the value you supplied in response to WM_CTLCOLORSTATIC.</span></span> <br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="587f5-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="587f5-126">Requirements</span></span>



| <span data-ttu-id="587f5-127">需求</span><span class="sxs-lookup"><span data-stu-id="587f5-127">Requirement</span></span> | <span data-ttu-id="587f5-128">值</span><span class="sxs-lookup"><span data-stu-id="587f5-128">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="587f5-129">標頭</span><span class="sxs-lookup"><span data-stu-id="587f5-129">Header</span></span><br/> | <dl> <span data-ttu-id="587f5-130"><dt>CommCtrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="587f5-130"><dt>CommCtrl.h</dt></span></span> </dl> |



