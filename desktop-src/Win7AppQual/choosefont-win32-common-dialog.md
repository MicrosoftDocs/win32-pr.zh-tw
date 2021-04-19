---
description: .
ms.assetid: ee1df9f2-585f-4208-ad49-a0f6ba76f53a
title: ChooseFont () Win32 通用對話方塊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e55a31d1f4d5530e04fe455135952eb94cc4bda
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106986609"
---
# <a name="choosefont-win32-common-dialog"></a><span data-ttu-id="e0531-103">ChooseFont () Win32 通用對話方塊</span><span class="sxs-lookup"><span data-stu-id="e0531-103">ChooseFont() Win32 Common Dialog</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="e0531-104">受影響的平臺</span><span class="sxs-lookup"><span data-stu-id="e0531-104">Affected Platforms</span></span>

<span data-ttu-id="e0531-105">**客戶** 端-Windows 7</span><span class="sxs-lookup"><span data-stu-id="e0531-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="e0531-106">**伺服器** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e0531-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="e0531-107">功能影響</span><span class="sxs-lookup"><span data-stu-id="e0531-107">Feature Impact</span></span>

<span data-ttu-id="e0531-108">**嚴重性** -低</span><span class="sxs-lookup"><span data-stu-id="e0531-108">**Severity** - Low</span></span>  
<span data-ttu-id="e0531-109">**頻率** -中型</span><span class="sxs-lookup"><span data-stu-id="e0531-109">**Frequency** - Medium</span></span>  




## <a name="description"></a><span data-ttu-id="e0531-110">Description</span><span class="sxs-lookup"><span data-stu-id="e0531-110">Description</span></span>

<span data-ttu-id="e0531-111">Windows 7 包含 ChooseFont () Win32 通用對話方塊的數項更新。</span><span class="sxs-lookup"><span data-stu-id="e0531-111">Windows 7 includes several updates to the ChooseFont() Win32 common dialog.</span></span> <span data-ttu-id="e0531-112">這些分為兩種類別：</span><span class="sxs-lookup"><span data-stu-id="e0531-112">These fall into two categories:</span></span>

-   <span data-ttu-id="e0531-113">對話方塊的視覺效果重新整理</span><span class="sxs-lookup"><span data-stu-id="e0531-113">Visual refresh of the dialog</span></span>
-   <span data-ttu-id="e0531-114">新顯示/隱藏字體功能的支援</span><span class="sxs-lookup"><span data-stu-id="e0531-114">Support for new show/hide fonts feature</span></span>

<span data-ttu-id="e0531-115">**對話方塊** 重新整理會更新標準範本，讓對話方塊與 Windows 中的其他對話版面配置更具線。</span><span class="sxs-lookup"><span data-stu-id="e0531-115">The **dialog refresh** updates the standard template to bring the dialog more in line with other dialog layouts in Windows.</span></span> <span data-ttu-id="e0531-116">它會將 WYSIWYG 引進字型顯示清單，以協助使用者選擇字型。</span><span class="sxs-lookup"><span data-stu-id="e0531-116">It introduces WYSIWYG to the font display lists to help users choose fonts.</span></span> <span data-ttu-id="e0531-117">它也包含字型 CPL 的連結，可讓希望自訂其字型清單的使用者輕鬆存取。</span><span class="sxs-lookup"><span data-stu-id="e0531-117">It also includes a link to the Fonts CPL to provide easy access for users wishing to customize their font lists.</span></span>

<span data-ttu-id="e0531-118">**顯示/隱藏** 字型是新的 Windows 7 平臺功能，因此字型挑選清單中預設不會顯示不適合目前使用者語言設定的字型 (輸入方法) 。</span><span class="sxs-lookup"><span data-stu-id="e0531-118">**Show/hide fonts** is a new Windows 7 platform feature whereby fonts not appropriate for the current user's language settings (input methods) are not presented by default in font selection lists.</span></span> <span data-ttu-id="e0531-119">使用者可以自訂要顯示在字型 CPL 中的字型，也可以停用此功能。</span><span class="sxs-lookup"><span data-stu-id="e0531-119">Users may customize the fonts that they wish to appear in the Fonts CPL or may disable this feature.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="e0531-120">影響的表現</span><span class="sxs-lookup"><span data-stu-id="e0531-120">Manifestation of Impact</span></span>

<span data-ttu-id="e0531-121">**對話方塊視覺效果重新整理**</span><span class="sxs-lookup"><span data-stu-id="e0531-121">**Dialog visual refresh**</span></span>

<span data-ttu-id="e0531-122">我們在 Windows 7 中引進了兩個新範本 (一個用於載入 comctl32.dll 6 版或更新版本的應用程式，而另一個則適用于載入舊版) 的應用程式。</span><span class="sxs-lookup"><span data-stu-id="e0531-122">We have introduced two new templates in Windows 7 (one for applications that load version 6 or later of comctl32.dll and another for applications loading earlier versions).</span></span>

-   <span data-ttu-id="e0531-123">基於應用程式相容性的理由，這些新範本只會針對未攔截 ChooseFont 訊息佇列的應用程式載入。</span><span class="sxs-lookup"><span data-stu-id="e0531-123">For application compatibility reasons, these new templates will only be loaded for applications that do not hook the ChooseFont message queue.</span></span> <span data-ttu-id="e0531-124">連結訊息佇列的應用程式將會繼續看到舊的對話版面配置。</span><span class="sxs-lookup"><span data-stu-id="e0531-124">Applications that hook the message queue will continue to see the old dialog layout.</span></span>
-   <span data-ttu-id="e0531-125">提供自己範本的應用程式將會繼續使用它們。</span><span class="sxs-lookup"><span data-stu-id="e0531-125">Applications that provide their own templates will continue to be able to use them.</span></span>

<span data-ttu-id="e0531-126">未取得新範本的應用程式將不會看到任何來自 Vista 的對話版面配置變更。</span><span class="sxs-lookup"><span data-stu-id="e0531-126">Applications that do not get the new templates will see no dialog layout changes from Vista.</span></span> <span data-ttu-id="e0531-127">但仍應取得新的 WYSIWYG 字型預覽。</span><span class="sxs-lookup"><span data-stu-id="e0531-127">They should however still get the new WYSIWYG font preview.</span></span>

<span data-ttu-id="e0531-128">**顯示/隱藏字型**</span><span class="sxs-lookup"><span data-stu-id="e0531-128">**Show/hide fonts**</span></span>

<span data-ttu-id="e0531-129">針對所有版本的 ChooseFont，此對話方塊會使用目前使用者的顯示/隱藏字型設定來決定要顯示的字型清單。</span><span class="sxs-lookup"><span data-stu-id="e0531-129">For all versions of ChooseFont, the dialog will use the current user's show/hide font settings to determine the font list to display.</span></span> <span data-ttu-id="e0531-130">這會導致在大部分的情況下顯示較少的字型清單。</span><span class="sxs-lookup"><span data-stu-id="e0531-130">This will result in the display of fewer font lists in most instances.</span></span>

## <a name="end-user-mitigation"></a><span data-ttu-id="e0531-131">使用者緩和</span><span class="sxs-lookup"><span data-stu-id="e0531-131">End-user Mitigation</span></span>

<span data-ttu-id="e0531-132">**顯示/隱藏字型：** 若要停用字型隱藏，使用者應該移至字型 CPL 中的 [字型設定] 頁面，並取消選取 [</span><span class="sxs-lookup"><span data-stu-id="e0531-132">**Show/Hide Fonts:** To disable font hiding, users should go to the Font Settings page in the Fonts CPL and deselect the '</span></span>

<span data-ttu-id="e0531-133">「隱藏以語言設定為基礎的字型」核取方塊</span><span class="sxs-lookup"><span data-stu-id="e0531-133">"Hide fonts based on language settings" checkbox</span></span>

## <a name="developer-mitigation"></a><span data-ttu-id="e0531-134">開發人員緩和</span><span class="sxs-lookup"><span data-stu-id="e0531-134">Developer Mitigation</span></span>

-   <span data-ttu-id="e0531-135">**視覺效果** 重新整理：提供專屬範本的應用程式開發人員可能會想要重新整理，使其符合適當的新 Windows 7 範本。</span><span class="sxs-lookup"><span data-stu-id="e0531-135">**Visual refresh:** Applications developers who provide their own templates may want to refresh this to be in line with the appropriate new Windows 7 template.</span></span> <span data-ttu-id="e0531-136">新的範本可在 Font-family 範本檔中使用。</span><span class="sxs-lookup"><span data-stu-id="e0531-136">The new templates are available in the Font.dlg template file.</span></span>

    <span data-ttu-id="e0531-137">**注意：** 新發佈的範本包含額外的 SysLink 控制項，可提供快捷方式，讓使用者啟動字型 CPL 以顯示更多字型。</span><span class="sxs-lookup"><span data-stu-id="e0531-137">**Note:** The new published template contains an additional SysLink control that provides a shortcut that allows users to launch the Fonts CPL to display more fonts.</span></span> <span data-ttu-id="e0531-138">連結控制項需要第6版的 Windows 通用控制項程式庫 (comctl32.dll) 。</span><span class="sxs-lookup"><span data-stu-id="e0531-138">The link control requires version 6 of the Windows common control library (comctl32.dll).</span></span> <span data-ttu-id="e0531-139">開發人員應提供資訊清單或指示詞，以指定使用第6版的 DLL （如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="e0531-139">Developers should provide a manifest or directive that specifies the use of version 6 of the DLL if available.</span></span> <span data-ttu-id="e0531-140">當應用程式使用舊版的通用控制項程式庫時，請改為使用「按鈕」控制項類型。</span><span class="sxs-lookup"><span data-stu-id="e0531-140">Where an application uses an earlier version of the common control library, use the "PUSHBUTTON" control type instead.</span></span>

-   <span data-ttu-id="e0531-141">**顯示/隱藏字型：** 開發人員可以停用此功能，方法是 \_ 在 CHOOSEFONT 結構的 flags 成員中提供額外的旗標 (CF INACTIVEFONTS) 。</span><span class="sxs-lookup"><span data-stu-id="e0531-141">**Show/Hide Fonts:** Developers may disable this feature by providing an additional flag (CF\_INACTIVEFONTS) in the flags member of the CHOOSEFONT structure.</span></span> <span data-ttu-id="e0531-142">設定此旗標會使所有已安裝的字型顯示在字型清單中。</span><span class="sxs-lookup"><span data-stu-id="e0531-142">Setting this flag causes all installed fonts to display in the font list.</span></span>
-   <span data-ttu-id="e0531-143">**顯示/隱藏字型：** 提供 ChooseFont 說明內容的應用程式可能會想要新增內容，以說明為什麼要減少字型清單，並將使用者導向字型 CPL 以自訂其字型清單。</span><span class="sxs-lookup"><span data-stu-id="e0531-143">**Show/Hide Fonts:** Applications that provide ChooseFont help content may wish to add content to explain why the font list is reduced and direct users to the Fonts CPL to customize their font lists.</span></span>

## <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="e0531-144">相容性、效能、可靠性和可用性測試</span><span class="sxs-lookup"><span data-stu-id="e0531-144">Compatibility, Performance, Reliability, and Usability Testing</span></span>

<span data-ttu-id="e0531-145">應用程式掛上 ChooseFont 訊息佇列以自訂對話方塊的開發人員應確認其應用程式保留所有現有的功能。</span><span class="sxs-lookup"><span data-stu-id="e0531-145">Developers whose applications hook the ChooseFont message queue to customize the dialog should verify that their applications retain all existing functionality.</span></span>

<span data-ttu-id="e0531-146">使用旗標大幅修剪字型清單的應用程式，應該確保顯示的字型清單保持可接受。</span><span class="sxs-lookup"><span data-stu-id="e0531-146">Applications that heavily trim the font list using flags should ensure that the font list presented remains acceptable.</span></span>

 

 



