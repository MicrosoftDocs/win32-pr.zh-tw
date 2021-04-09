---
title: ConvertPluginCLSID 子機碼
description: ConvertPluginCLSID 子機碼
ms.assetid: 2bf5b6ad-31e9-40c2-a682-c7ad813e8f7a
keywords:
- Windows Media Player，ConvertPluginCLSID 子機碼
- Windows Media Player、副檔名
- Windows Media Player，登錄
- 登錄、副檔名
- registry，ConvertPluginCLSID 子機碼
- 登錄，Windows Media Player 的設定
- 副檔名登錄設定
- ConvertPluginCLSID 子機碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4229617c3999708d89fac976e94b2747b5a69145
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021541"
---
# <a name="convertpluginclsid-subkey"></a><span data-ttu-id="88778-111">ConvertPluginCLSID 子機碼</span><span class="sxs-lookup"><span data-stu-id="88778-111">ConvertPluginCLSID Subkey</span></span>

<span data-ttu-id="88778-112">當 Windows Media Player 11 遇到自訂副檔名時，它會尋找符合擴充功能的登錄子機碼。</span><span class="sxs-lookup"><span data-stu-id="88778-112">When Windows Media Player 11 encounters a custom file name extension, it looks for a registry subkey that matches the extension.</span></span> <span data-ttu-id="88778-113">此子機碼描述于副檔名登錄 [設定](file-name-extension-registry-settings.md)中。</span><span class="sxs-lookup"><span data-stu-id="88778-113">The subkey is described in [File Name Extension Registry Settings](file-name-extension-registry-settings.md).</span></span> <span data-ttu-id="88778-114">在某些情況下，延伸的子機碼具有名為 **ConvertPluginCLSID** 的子機碼。</span><span class="sxs-lookup"><span data-stu-id="88778-114">In some cases, the extension's subkey has a subkey named **ConvertPluginCLSID**.</span></span>

<span data-ttu-id="88778-115">例如，假設您已建立副檔名為 (的自訂檔案格式。 xyz) 和轉換外掛程式，可將檔案轉換成 Windows Media Player 所支援的格式，然後您可以在下列其中一或兩個子機碼中儲存外掛程式的類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="88778-115">For example, suppose you have created a custom file format (with file name extension .xyz) and a conversion plug-in that converts the files to a format supported by Windows Media Player Then you would store the class ID of the plug-in in one or both of the following subkeys.</span></span>

<span data-ttu-id="88778-116">**HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ 多媒體 \\ WMPlayer \\ 擴充功能 \\ 。 xyz \\ ConvertPluginCLSID**</span><span class="sxs-lookup"><span data-stu-id="88778-116">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Multimedia\\WMPlayer\\Extensions\\.xyz\\ConvertPluginCLSID**</span></span>

<span data-ttu-id="88778-117">**HKEY \_ 目前的 \_ 使用者 \\ 軟體 \\ Microsoft \\ MediaPlayer \\ Player 擴充功能 \\ \\ 。 xyz \\ ConvertPluginCLSID**</span><span class="sxs-lookup"><span data-stu-id="88778-117">**HKEY\_CURRENT\_USER\\Software\\Microsoft\\MediaPlayer\\Player\\Extensions\\.xyz\\ConvertPluginCLSID**</span></span>

<span data-ttu-id="88778-118">**ConvertPluginCLSID** 子機碼會指定外掛程式的類別識別碼，Windows Media Player 可以用來將媒體檔案從其自訂格式轉換為播放程式所支援的格式。</span><span class="sxs-lookup"><span data-stu-id="88778-118">The **ConvertPluginCLSID** subkey specifies the class IDs of plug-ins that Windows Media Player can use to convert a media file from its custom format to a format supported by the Player.</span></span>

<span data-ttu-id="88778-119">**ConvertPluginCLSID** 子機碼具有下列專案。</span><span class="sxs-lookup"><span data-stu-id="88778-119">The **ConvertPluginCLSID** subkey has the following entries.</span></span>

-   <span data-ttu-id="88778-120">代表預設轉換外掛程式的預設專案。</span><span class="sxs-lookup"><span data-stu-id="88778-120">A default entry that represents the default conversion plug-in.</span></span>
-   <span data-ttu-id="88778-121">代表預設轉換外掛程式的已命名專案。</span><span class="sxs-lookup"><span data-stu-id="88778-121">A named entry that represents the default conversion plug-in.</span></span>
-   <span data-ttu-id="88778-122">代表替代轉換外掛程式的其他已命名專案。</span><span class="sxs-lookup"><span data-stu-id="88778-122">Additional named entries that represent alternate conversion plug-ins.</span></span>

<span data-ttu-id="88778-123">例如，假設自訂檔案格式具有預設轉換外掛程式和兩個替代的轉換外掛程式。 **ConvertPluginCLSID** 子機碼底下的登錄專案會有下列格式。</span><span class="sxs-lookup"><span data-stu-id="88778-123">For example, suppose a custom file format has a default conversion plug-in and two alternate conversion plug-ins. The registry entries under the **ConvertPluginCLSID** subkey would have the following form.</span></span>



| <span data-ttu-id="88778-124">名稱</span><span class="sxs-lookup"><span data-stu-id="88778-124">Name</span></span>                                                                          | <span data-ttu-id="88778-125">類型</span><span class="sxs-lookup"><span data-stu-id="88778-125">Type</span></span>        | <span data-ttu-id="88778-126">值</span><span class="sxs-lookup"><span data-stu-id="88778-126">Value</span></span>                                                                |
|-------------------------------------------------------------------------------|-------------|----------------------------------------------------------------------|
| <span data-ttu-id="88778-127">預設</span><span class="sxs-lookup"><span data-stu-id="88778-127">Default</span></span>                                                                       | <span data-ttu-id="88778-128">**REG \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="88778-128">**REG\_SZ**</span></span> | <span data-ttu-id="88778-129">預設轉換外掛程式的類別識別碼（登錄格式）。</span><span class="sxs-lookup"><span data-stu-id="88778-129">The class ID, in registry format, of the default conversion plug-in.</span></span> |
| <span data-ttu-id="88778-130">預設轉換外掛程式的類別識別碼（登錄格式）。</span><span class="sxs-lookup"><span data-stu-id="88778-130">The class ID, in registry format, of the default conversion plug-in.</span></span>          | <span data-ttu-id="88778-131">**REG \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="88778-131">**REG\_SZ**</span></span> | <span data-ttu-id="88778-132">預設轉換外掛程式的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="88778-132">The friendly name of the default conversion plug-in.</span></span>                 |
| <span data-ttu-id="88778-133">第一個替代轉換外掛程式的類別識別碼（登錄格式）。</span><span class="sxs-lookup"><span data-stu-id="88778-133">The class ID, in registry format, of the first alternate conversion plug-in.</span></span>  | <span data-ttu-id="88778-134">**REG \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="88778-134">**REG\_SZ**</span></span> | <span data-ttu-id="88778-135">第一個替代轉換外掛程式的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="88778-135">The friendly name of the first alternate conversion plug-in.</span></span>         |
| <span data-ttu-id="88778-136">第二個替代轉換外掛程式的類別識別碼（登錄格式）。</span><span class="sxs-lookup"><span data-stu-id="88778-136">The class ID, in registry format, of the second alternate conversion plug-in.</span></span> | <span data-ttu-id="88778-137">**REG \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="88778-137">**REG\_SZ**</span></span> | <span data-ttu-id="88778-138">第二個替代轉換外掛程式的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="88778-138">The friendly name of the second alternate conversion plug-in.</span></span>        |



 

<span data-ttu-id="88778-139">請注意，預設的轉換外掛程式會以兩個登錄專案表示：預設專案和已命名的專案。</span><span class="sxs-lookup"><span data-stu-id="88778-139">Note that the default conversion plug-in is represented by two registry entries: the default entry and a named entry.</span></span> <span data-ttu-id="88778-140">Windows Media Player 使用預設專案來判斷哪個外掛程式是主要) 轉換外掛程式的預設 (。</span><span class="sxs-lookup"><span data-stu-id="88778-140">Windows Media Player uses the default entry to determine which plug-in is the default (primary) conversion plug-in.</span></span> <span data-ttu-id="88778-141">Windows Media Player 會使用已命名的專案來取得所有轉換外掛程式的易記名稱，包括預設外掛程式。</span><span class="sxs-lookup"><span data-stu-id="88778-141">Windows Media Player uses the named entries to obtain friendly names for all conversion plug-ins, including the default plug-in.</span></span>

<span data-ttu-id="88778-142">轉換外掛程式的易記名稱是由建立外掛程式的公司所決定。</span><span class="sxs-lookup"><span data-stu-id="88778-142">The friendly name of a conversion plug-in is determined by the company that creates the plug-in.</span></span> <span data-ttu-id="88778-143">Windows Media Player 可能會在其使用者介面中顯示易記名稱。</span><span class="sxs-lookup"><span data-stu-id="88778-143">Windows Media Player might display the friendly name in its user interface.</span></span>

<span data-ttu-id="88778-144">當 Windows Media Player 嘗試將檔案從自訂格式轉換成標準格式時，會先載入預設外掛程式。</span><span class="sxs-lookup"><span data-stu-id="88778-144">When Windows Media Player attempts to convert a file from a custom format to a standard format, it first loads the default plug-in.</span></span> <span data-ttu-id="88778-145">如果預設外掛程式無法轉換檔案，並傳回 NS \_ E \_ WMP \_ convert \_ 外掛程式 \_ 未知的檔案擁有者 \_ \_ ，則 Player 會載入每個替代外掛程式，直到成功轉換或沒有其他外掛程式可供嘗試為止。</span><span class="sxs-lookup"><span data-stu-id="88778-145">If the default plug-in fails to convert the file and returns NS\_E\_WMP\_CONVERT\_PLUGIN\_UNKNOWN\_FILE\_OWNER, the Player loads each alternate plug-in until a successful conversion happens or there are no more plug-ins to try.</span></span> <span data-ttu-id="88778-146">如果找不到副檔名的轉換外掛程式，播放程式就不會顯示警告訊息。</span><span class="sxs-lookup"><span data-stu-id="88778-146">The Player does not display a warning message if no conversion plug-in is found for the file name extension.</span></span>

<span data-ttu-id="88778-147">Windows Media Player 11 支援 **ConvertPluginCLSID** 登錄專案。</span><span class="sxs-lookup"><span data-stu-id="88778-147">The **ConvertPluginCLSID** registry entry is supported by Windows Media Player 11.</span></span>

## <a name="related-topics"></a><span data-ttu-id="88778-148">相關主題</span><span class="sxs-lookup"><span data-stu-id="88778-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88778-149">**副檔名登錄設定**</span><span class="sxs-lookup"><span data-stu-id="88778-149">**File Name Extension Registry Settings**</span></span>](file-name-extension-registry-settings.md)
</dt> <dt>

[<span data-ttu-id="88778-150">**Windows Media Player 轉換外掛程式**</span><span class="sxs-lookup"><span data-stu-id="88778-150">**Windows Media Player Conversion Plug-ins**</span></span>](windows-media-player-conversion-plug-ins.md)
</dt> </dl>

 

 




