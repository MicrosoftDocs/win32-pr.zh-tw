---
title: 註冊旗標
description: 註冊旗標
ms.assetid: ba1709c2-0fe5-4168-9aed-613d01eff21f
keywords:
- Windows Media Player 外掛程式、註冊旗標
- 外掛程式，註冊旗標
- 使用者介面外掛程式、註冊旗標
- UI 外掛程式、註冊旗標
- 旗標，使用者介面外掛程式
- 登錄，UI 外掛程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac609b45866cd5f18edf61dffc2d3b7ac3c397ac
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104023053"
---
# <a name="registration-flags"></a><span data-ttu-id="8ad60-109">註冊旗標</span><span class="sxs-lookup"><span data-stu-id="8ad60-109">Registration Flags</span></span>

<span data-ttu-id="8ad60-110">當 Windows Media Player 外掛程式 Wizard 建立新的 UI 外掛程式專案時，它會在登錄中建立一個機碼，其中包含外掛程式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="8ad60-110">When the Windows Media Player Plug-in Wizard creates a new UI plug-in project, it creates a key in the registry that contains information about the plug-in.</span></span> <span data-ttu-id="8ad60-111">此金鑰會建立在下列位置：</span><span class="sxs-lookup"><span data-stu-id="8ad60-111">This key is created in the following location:</span></span>


```C++
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MediaPlayer\UIPlugins\{ClassId}
```



<span data-ttu-id="8ad60-112">*ClassId* 是外掛程式的類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="8ad60-112">*ClassId* is the class id of the plug-in.</span></span>

<span data-ttu-id="8ad60-113">此索引鍵包含下列值。</span><span class="sxs-lookup"><span data-stu-id="8ad60-113">This key includes the following values.</span></span>



| <span data-ttu-id="8ad60-114">名稱</span><span class="sxs-lookup"><span data-stu-id="8ad60-114">Name</span></span>                     | <span data-ttu-id="8ad60-115">類型</span><span class="sxs-lookup"><span data-stu-id="8ad60-115">Type</span></span>       | <span data-ttu-id="8ad60-116">Description</span><span class="sxs-lookup"><span data-stu-id="8ad60-116">Description</span></span>                                                                                                                                                                               |
|--------------------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ad60-117">功能</span><span class="sxs-lookup"><span data-stu-id="8ad60-117">Capabilities</span></span>             | <span data-ttu-id="8ad60-118">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="8ad60-118">REG\_DWORD</span></span> | <span data-ttu-id="8ad60-119">DWORD 值，其中至少包含一個外掛程式類型旗標，該旗標可以使用二進位或作業結合一或多個外掛程式功能旗標。</span><span class="sxs-lookup"><span data-stu-id="8ad60-119">A DWORD value that consists of at least one plug-in type flag that may be combined with one or more plug-in capabilities flags by using binary OR operations.</span></span>                             |
| <span data-ttu-id="8ad60-120">Description</span><span class="sxs-lookup"><span data-stu-id="8ad60-120">Description</span></span>              | <span data-ttu-id="8ad60-121">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="8ad60-121">REG\_SZ</span></span>    | <span data-ttu-id="8ad60-122">字串，其中包含外掛程式的描述。</span><span class="sxs-lookup"><span data-stu-id="8ad60-122">A string that contains the description of the plug-in.</span></span> <span data-ttu-id="8ad60-123">外掛程式 wizard 會建立字串資源，並使用此值的 res 通訊協定) 來提供資源 (的 URL。</span><span class="sxs-lookup"><span data-stu-id="8ad60-123">The plug-in wizard creates a string resource and provides the URL of the resource (using the res protocol) for this value.</span></span>         |
| <span data-ttu-id="8ad60-124">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="8ad60-124">FriendlyName</span></span>             | <span data-ttu-id="8ad60-125">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="8ad60-125">REG\_SZ</span></span>    | <span data-ttu-id="8ad60-126">字串，包含外掛程式的使用者可讀取名稱。</span><span class="sxs-lookup"><span data-stu-id="8ad60-126">A string that contains the user-readable name for the plug-in.</span></span> <span data-ttu-id="8ad60-127">外掛程式 wizard 會建立字串資源，並使用此值的 res 通訊協定) 來提供資源 (的 URL。</span><span class="sxs-lookup"><span data-stu-id="8ad60-127">The plug-in wizard creates a string resource and provides the URL of the resource (using the res protocol) for this value.</span></span> |
| <span data-ttu-id="8ad60-128">UninstallPath (選用) </span><span class="sxs-lookup"><span data-stu-id="8ad60-128">UninstallPath (optional)</span></span> | <span data-ttu-id="8ad60-129">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="8ad60-129">REG\_SZ</span></span>    | <span data-ttu-id="8ad60-130">字串，包含卸載外掛程式之可執行檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="8ad60-130">A string that contains the path to an executable file that uninstalls the plug-in.</span></span>                                                                                                        |



 

<span data-ttu-id="8ad60-131">如需 res 通訊協定的詳細資訊，請參閱網際網路開發 SDK。</span><span class="sxs-lookup"><span data-stu-id="8ad60-131">For more information about the res protocol, see the Internet Development SDK.</span></span>

<span data-ttu-id="8ad60-132">下表詳細說明外掛程式類型旗標。</span><span class="sxs-lookup"><span data-stu-id="8ad60-132">The following table details the plug-in type flags.</span></span>



| <span data-ttu-id="8ad60-133">外掛程式類型旗標</span><span class="sxs-lookup"><span data-stu-id="8ad60-133">Plug-in Type Flag</span></span>                | <span data-ttu-id="8ad60-134">值</span><span class="sxs-lookup"><span data-stu-id="8ad60-134">Value</span></span> | <span data-ttu-id="8ad60-135">描述</span><span class="sxs-lookup"><span data-stu-id="8ad60-135">Description</span></span>                                       |
|----------------------------------|-------|---------------------------------------------------|
| <span data-ttu-id="8ad60-136">**外掛程式 \_ 類型 \_ 背景**</span><span class="sxs-lookup"><span data-stu-id="8ad60-136">**PLUGIN\_TYPE\_BACKGROUND**</span></span>     | <span data-ttu-id="8ad60-137">0x1</span><span class="sxs-lookup"><span data-stu-id="8ad60-137">0x1</span></span>   | <span data-ttu-id="8ad60-138">UI 外掛程式不會顯示使用者介面。</span><span class="sxs-lookup"><span data-stu-id="8ad60-138">The UI plug-in does not display a user interface.</span></span> |
| <span data-ttu-id="8ad60-139">**外掛程式 \_ 類型 \_ SEPARATEWINDOW**</span><span class="sxs-lookup"><span data-stu-id="8ad60-139">**PLUGIN\_TYPE\_SEPARATEWINDOW**</span></span> | <span data-ttu-id="8ad60-140">0x2</span><span class="sxs-lookup"><span data-stu-id="8ad60-140">0x2</span></span>   | <span data-ttu-id="8ad60-141">UI 外掛程式是個別的視窗外掛程式。</span><span class="sxs-lookup"><span data-stu-id="8ad60-141">The UI plug-in is a separate window plug-in.</span></span>      |
| <span data-ttu-id="8ad60-142">**外掛程式 \_ 類型 \_ DISPLAYAREA**</span><span class="sxs-lookup"><span data-stu-id="8ad60-142">**PLUGIN\_TYPE\_DISPLAYAREA**</span></span>    | <span data-ttu-id="8ad60-143">0x3</span><span class="sxs-lookup"><span data-stu-id="8ad60-143">0x3</span></span>   | <span data-ttu-id="8ad60-144">UI 外掛程式是顯示區域外掛程式。</span><span class="sxs-lookup"><span data-stu-id="8ad60-144">The UI plug-in is a display area plug-in.</span></span>         |
| <span data-ttu-id="8ad60-145">**外掛程式 \_ 類型 \_ SETTINGSAREA**</span><span class="sxs-lookup"><span data-stu-id="8ad60-145">**PLUGIN\_TYPE\_SETTINGSAREA**</span></span>   | <span data-ttu-id="8ad60-146">0x4</span><span class="sxs-lookup"><span data-stu-id="8ad60-146">0x4</span></span>   | <span data-ttu-id="8ad60-147">UI 外掛程式是設定區域外掛程式。</span><span class="sxs-lookup"><span data-stu-id="8ad60-147">The UI plug-in is a settings area plug-in.</span></span>        |
| <span data-ttu-id="8ad60-148">**外掛程式 \_ 類型 \_ METADATAAREA**</span><span class="sxs-lookup"><span data-stu-id="8ad60-148">**PLUGIN\_TYPE\_METADATAAREA**</span></span>   | <span data-ttu-id="8ad60-149">0x5</span><span class="sxs-lookup"><span data-stu-id="8ad60-149">0x5</span></span>   | <span data-ttu-id="8ad60-150">UI 外掛程式是中繼資料區域外掛程式。</span><span class="sxs-lookup"><span data-stu-id="8ad60-150">The UI plug-in is a metadata area plug-in.</span></span>        |



 

<span data-ttu-id="8ad60-151">下表詳細說明外掛程式功能旗標。</span><span class="sxs-lookup"><span data-stu-id="8ad60-151">The following table details the plug-in capabilities flags.</span></span>



| <span data-ttu-id="8ad60-152">外掛程式功能旗標</span><span class="sxs-lookup"><span data-stu-id="8ad60-152">Plug-in Capabilities Flag</span></span>             | <span data-ttu-id="8ad60-153">值</span><span class="sxs-lookup"><span data-stu-id="8ad60-153">Value</span></span>      | <span data-ttu-id="8ad60-154">描述</span><span class="sxs-lookup"><span data-stu-id="8ad60-154">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                         |
|---------------------------------------|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ad60-155">**外掛程式 \_ 旗標 \_ ACCEPTSMEDIA**</span><span class="sxs-lookup"><span data-stu-id="8ad60-155">**PLUGIN\_FLAGS\_ACCEPTSMEDIA**</span></span>       | <span data-ttu-id="8ad60-156">0x10000000</span><span class="sxs-lookup"><span data-stu-id="8ad60-156">0x10000000</span></span> | <span data-ttu-id="8ad60-157">當 Windows Media Player 呼叫 [**IWMPPluginUI：： SetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-setproperty)時，UI 外掛程式可以接受 **媒體** 物件指標陣列。</span><span class="sxs-lookup"><span data-stu-id="8ad60-157">The UI plug-in can accept **Media** object pointer arrays when Windows Media Player calls [**IWMPPluginUI::SetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-setproperty) .</span></span>                                                                                                                                                                                                                                                           |
| <span data-ttu-id="8ad60-158">**外掛程式 \_ 旗標 \_ ACCEPTSPLAYLISTS**</span><span class="sxs-lookup"><span data-stu-id="8ad60-158">**PLUGIN\_FLAGS\_ACCEPTSPLAYLISTS**</span></span>   | <span data-ttu-id="8ad60-159">0x8000000</span><span class="sxs-lookup"><span data-stu-id="8ad60-159">0x8000000</span></span>  | <span data-ttu-id="8ad60-160">當 Windows Media Player 呼叫 [**IWMPPluginUI：： SetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-setproperty)時，UI 外掛程式可以接受 **播放清單** 物件指標陣列。</span><span class="sxs-lookup"><span data-stu-id="8ad60-160">The UI plug-in can accept **Playlist** object pointer arrays when Windows Media Player calls [**IWMPPluginUI::SetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-setproperty) .</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="8ad60-161">**外掛程式 \_ 旗標 \_ HASPRESETS**</span><span class="sxs-lookup"><span data-stu-id="8ad60-161">**PLUGIN\_FLAGS\_HASPRESETS**</span></span>         | <span data-ttu-id="8ad60-162">0x4000000</span><span class="sxs-lookup"><span data-stu-id="8ad60-162">0x4000000</span></span>  | <span data-ttu-id="8ad60-163">UI 外掛程式會使用預設值。</span><span class="sxs-lookup"><span data-stu-id="8ad60-163">The UI plug-in uses presets.</span></span> <span data-ttu-id="8ad60-164">如果外掛程式指定此旗標，Windows Media Player 會呼叫 [**IWMPPluginUI：： GetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-getproperty) ，以查詢外掛程式是否有預設的資訊。</span><span class="sxs-lookup"><span data-stu-id="8ad60-164">If the plug-in specifies this flag, Windows Media Player will query the plug-in for preset information by calling [**IWMPPluginUI::GetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-getproperty) .</span></span>                                                                                                                                                                                                      |
| <span data-ttu-id="8ad60-165">**外掛程式 \_ 旗標 \_ HASPROPERTYPAGE**</span><span class="sxs-lookup"><span data-stu-id="8ad60-165">**PLUGIN\_FLAGS\_HASPROPERTYPAGE**</span></span>    | <span data-ttu-id="8ad60-166">0x80000000</span><span class="sxs-lookup"><span data-stu-id="8ad60-166">0x80000000</span></span> | <span data-ttu-id="8ad60-167">UI 外掛程式提供屬性頁對話方塊。</span><span class="sxs-lookup"><span data-stu-id="8ad60-167">The UI plug-in provides a property page dialog.</span></span> <span data-ttu-id="8ad60-168">如果叫用屬性頁時設定這個旗標，Windows Media Player 會呼叫 [**IWMPPluginUI：:D isplaypropertypage**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-displaypropertypage) 。</span><span class="sxs-lookup"><span data-stu-id="8ad60-168">Windows Media Player will call [**IWMPPluginUI::DisplayPropertyPage**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-displaypropertypage) if this flag is set when the property page is invoked.</span></span>                                                                                                                                                                                                 |
| <span data-ttu-id="8ad60-169">**外掛程式 \_ 旗標 \_ 隱藏**</span><span class="sxs-lookup"><span data-stu-id="8ad60-169">**PLUGIN\_FLAGS\_HIDDEN**</span></span>             | <span data-ttu-id="8ad60-170">0x02000000</span><span class="sxs-lookup"><span data-stu-id="8ad60-170">0x02000000</span></span> | <span data-ttu-id="8ad60-171">背景 UI 外掛程式不會出現在從 [ **View** ] 或 [ **Tools** ] 功能表中存取的 [**外掛程式]** 功能表上，或現在現正播放的 [**立即播放] 選項** 按鈕。</span><span class="sxs-lookup"><span data-stu-id="8ad60-171">The background UI plug-in does not appear on the **Plug-ins** menu that is accessed from the **View** or **Tools** menus or the **Select Now Playing options** button in Now Playing.</span></span> <span data-ttu-id="8ad60-172">它會出現在 [選項] 對話方塊的 [ **外掛程式** ] 索引標籤上。</span><span class="sxs-lookup"><span data-stu-id="8ad60-172">It does appear on the **Plug-ins** tab of the Options dialog.</span></span> <span data-ttu-id="8ad60-173">這會導致背景外掛程式執行圖示出現在狀態列中。此旗標不會影響背景 UI 外掛程式以外的外掛程式。</span><span class="sxs-lookup"><span data-stu-id="8ad60-173">It does cause the Background Plug-in Running icon to appear in the status bar.This flag has no effect on plug-ins other than background UI plug-ins.</span></span><br/> |
| <span data-ttu-id="8ad60-174">**外掛程式 \_ 旗標 \_ INSTALLAUTORUN**</span><span class="sxs-lookup"><span data-stu-id="8ad60-174">**PLUGIN\_FLAGS\_INSTALLAUTORUN**</span></span>     | <span data-ttu-id="8ad60-175">0x40000000</span><span class="sxs-lookup"><span data-stu-id="8ad60-175">0x40000000</span></span> | <span data-ttu-id="8ad60-176">當安裝外掛程式時，Windows Media Player 會自動執行 UI 外掛程式。</span><span class="sxs-lookup"><span data-stu-id="8ad60-176">Windows Media Player runs the UI plug-in automatically when the plug-in is installed.</span></span>                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="8ad60-177">**外掛程式 \_ 旗標 \_ LAUNCHPROPERTYPAGE**</span><span class="sxs-lookup"><span data-stu-id="8ad60-177">**PLUGIN\_FLAGS\_LAUNCHPROPERTYPAGE**</span></span> | <span data-ttu-id="8ad60-178">0x20000000</span><span class="sxs-lookup"><span data-stu-id="8ad60-178">0x20000000</span></span> | <span data-ttu-id="8ad60-179">當 UI 外掛程式第一次執行時，Windows Media Player 會呼叫 [**IWMPPluginUI：:D isplaypropertypage**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-displaypropertypage) 。如果指定此旗標，則也應該指定 **外掛程式 \_ 旗標 \_ HASPROPERTYPAGE** 。</span><span class="sxs-lookup"><span data-stu-id="8ad60-179">Windows Media Player calls [**IWMPPluginUI::DisplayPropertyPage**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-displaypropertypage) when the UI plug-in runs for the first time.If this flag is specified, **PLUGIN\_FLAGS\_HASPROPERTYPAGE** should be specified also.</span></span><br/>                                                                                                                                                             |



 

<span data-ttu-id="8ad60-180">下列常數定義于 wmpplug 中。</span><span class="sxs-lookup"><span data-stu-id="8ad60-180">The following constants are defined in wmpplug.h.</span></span> <span data-ttu-id="8ad60-181">請勿變更與這些常數相關聯的值。</span><span class="sxs-lookup"><span data-stu-id="8ad60-181">Do not change the values associated with these constants.</span></span>



| <span data-ttu-id="8ad60-182">Name</span><span class="sxs-lookup"><span data-stu-id="8ad60-182">Name</span></span>                                    | <span data-ttu-id="8ad60-183">描述</span><span class="sxs-lookup"><span data-stu-id="8ad60-183">Description</span></span>                               |
|-----------------------------------------|-------------------------------------------|
| <span data-ttu-id="8ad60-184">**外掛程式 \_ INSTALLREGKEY**</span><span class="sxs-lookup"><span data-stu-id="8ad60-184">**PLUGIN\_INSTALLREGKEY**</span></span>               | <span data-ttu-id="8ad60-185">外掛程式登錄機碼的位置。</span><span class="sxs-lookup"><span data-stu-id="8ad60-185">The location of the plug-in registry key.</span></span> |
| <span data-ttu-id="8ad60-186">**外掛程式 \_ INSTALLREGKEY \_ FRIENDLYNAME**</span><span class="sxs-lookup"><span data-stu-id="8ad60-186">**PLUGIN\_INSTALLREGKEY\_FRIENDLYNAME**</span></span> | <span data-ttu-id="8ad60-187">易記名稱值的名稱。</span><span class="sxs-lookup"><span data-stu-id="8ad60-187">The name of the friendly name value.</span></span>      |
| <span data-ttu-id="8ad60-188">**外掛程式 \_ INSTALLREGKEY \_ 描述**</span><span class="sxs-lookup"><span data-stu-id="8ad60-188">**PLUGIN\_INSTALLREGKEY\_DESCRIPTION**</span></span>  | <span data-ttu-id="8ad60-189">描述值的名稱。</span><span class="sxs-lookup"><span data-stu-id="8ad60-189">The name of the description value.</span></span>        |
| <span data-ttu-id="8ad60-190">**外掛程式 \_ INSTALLREGKEY \_ 功能**</span><span class="sxs-lookup"><span data-stu-id="8ad60-190">**PLUGIN\_INSTALLREGKEY\_CAPABILITIES**</span></span> | <span data-ttu-id="8ad60-191">功能值的名稱。</span><span class="sxs-lookup"><span data-stu-id="8ad60-191">The name of the capabilities value.</span></span>       |
| <span data-ttu-id="8ad60-192">**外掛程式 \_ INSTALLREGKEY \_ 卸載**</span><span class="sxs-lookup"><span data-stu-id="8ad60-192">**PLUGIN\_INSTALLREGKEY\_UNINSTALL**</span></span>    | <span data-ttu-id="8ad60-193">卸載路徑值的名稱。</span><span class="sxs-lookup"><span data-stu-id="8ad60-193">The name of the uninstall path value.</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="8ad60-194">相關主題</span><span class="sxs-lookup"><span data-stu-id="8ad60-194">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8ad60-195">**IWMPPluginUI：:D isplayPropertyPage**</span><span class="sxs-lookup"><span data-stu-id="8ad60-195">**IWMPPluginUI::DisplayPropertyPage**</span></span>](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-displaypropertypage)
</dt> <dt>

[<span data-ttu-id="8ad60-196">**IWMPPluginUI：： GetProperty**</span><span class="sxs-lookup"><span data-stu-id="8ad60-196">**IWMPPluginUI::GetProperty**</span></span>](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-getproperty)
</dt> <dt>

[<span data-ttu-id="8ad60-197">**IWMPPluginUI：： SetProperty**</span><span class="sxs-lookup"><span data-stu-id="8ad60-197">**IWMPPluginUI::SetProperty**</span></span>](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-setproperty)
</dt> <dt>

[<span data-ttu-id="8ad60-198">**消費者介面外掛程式程式設計參考**</span><span class="sxs-lookup"><span data-stu-id="8ad60-198">**User Interface Plug-ins Programming Reference**</span></span>](user-interface-plug-ins-programming-reference.md)
</dt> </dl>

 

 





