---
title: IMsRdpClientAdvancedSettings PerformanceFlags 屬性
description: 指定可在伺服器上設定的一組功能，以改善效能。
ms.assetid: dbbc7c13-ad8a-461d-9d2e-c454bf4b9dea
ms.tgt_platform: multiple
keywords:
- PerformanceFlags 屬性遠端桌面服務
- PerformanceFlags 屬性遠端桌面服務，IMsRdpClientAdvancedSettings 介面
- IMsRdpClientAdvancedSettings 介面遠端桌面服務，PerformanceFlags 屬性
- PerformanceFlags 屬性遠端桌面服務，IMsRdpClientAdvancedSettings2 介面
- IMsRdpClientAdvancedSettings2 介面遠端桌面服務，PerformanceFlags 屬性
- PerformanceFlags 屬性遠端桌面服務，IMsRdpClientAdvancedSettings3 介面
- IMsRdpClientAdvancedSettings3 介面遠端桌面服務，PerformanceFlags 屬性
- PerformanceFlags 屬性遠端桌面服務，IMsRdpClientAdvancedSettings4 介面
- IMsRdpClientAdvancedSettings4 介面遠端桌面服務，PerformanceFlags 屬性
- PerformanceFlags 屬性遠端桌面服務，IMsRdpClientAdvancedSettings5 介面
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務，PerformanceFlags 屬性
- PerformanceFlags 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，PerformanceFlags 屬性
- PerformanceFlags 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，PerformanceFlags 屬性
- PerformanceFlags 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，PerformanceFlags 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.PerformanceFlags
- IMsRdpClientAdvancedSettings.get_PerformanceFlags
- IMsRdpClientAdvancedSettings.put_PerformanceFlags
- IMsRdpClientAdvancedSettings2.PerformanceFlags
- IMsRdpClientAdvancedSettings2.get_PerformanceFlags
- IMsRdpClientAdvancedSettings2.put_PerformanceFlags
- IMsRdpClientAdvancedSettings3.PerformanceFlags
- IMsRdpClientAdvancedSettings3.get_PerformanceFlags
- IMsRdpClientAdvancedSettings3.put_PerformanceFlags
- IMsRdpClientAdvancedSettings4.PerformanceFlags
- IMsRdpClientAdvancedSettings4.get_PerformanceFlags
- IMsRdpClientAdvancedSettings4.put_PerformanceFlags
- IMsRdpClientAdvancedSettings5.PerformanceFlags
- IMsRdpClientAdvancedSettings5.get_PerformanceFlags
- IMsRdpClientAdvancedSettings5.put_PerformanceFlags
- IMsRdpClientAdvancedSettings6.PerformanceFlags
- IMsRdpClientAdvancedSettings6.get_PerformanceFlags
- IMsRdpClientAdvancedSettings6.put_PerformanceFlags
- IMsRdpClientAdvancedSettings7.PerformanceFlags
- IMsRdpClientAdvancedSettings7.get_PerformanceFlags
- IMsRdpClientAdvancedSettings7.put_PerformanceFlags
- IMsRdpClientAdvancedSettings8.PerformanceFlags
- IMsRdpClientAdvancedSettings8.get_PerformanceFlags
- IMsRdpClientAdvancedSettings8.put_PerformanceFlags
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1731afc6d58cede5da055da8cacaf11c8712d3c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384301"
---
# <a name="imsrdpclientadvancedsettingsperformanceflags-property"></a><span data-ttu-id="d876e-120">IMsRdpClientAdvancedSettings：:P erformanceFlags 屬性</span><span class="sxs-lookup"><span data-stu-id="d876e-120">IMsRdpClientAdvancedSettings::PerformanceFlags property</span></span>

<span data-ttu-id="d876e-121">指定可在伺服器上設定的一組功能，以改善效能。</span><span class="sxs-lookup"><span data-stu-id="d876e-121">Specifies a set of features that can be set at the server to improve performance.</span></span>

<span data-ttu-id="d876e-122">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="d876e-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="d876e-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="d876e-123">Syntax</span></span>


```C++
HRESULT put_PerformanceFlags(
  [in]  LONG DisableList = TS_PERF_DISABLE_NOTHING
);

HRESULT get_PerformanceFlags(
  [out] LONG *pDisableList
);
```



## <a name="property-value"></a><span data-ttu-id="d876e-124">屬性值</span><span class="sxs-lookup"><span data-stu-id="d876e-124">Property value</span></span>

<span data-ttu-id="d876e-125">新的旗標。</span><span class="sxs-lookup"><span data-stu-id="d876e-125">The new flags.</span></span> <span data-ttu-id="d876e-126">預設值為 0 (**TS \_ 效能 \_ 停用 \_ 任何** 專案。 ) </span><span class="sxs-lookup"><span data-stu-id="d876e-126">The default is 0 (**TS\_PERF\_DISABLE\_NOTHING**.)</span></span>

<dt>

<span id="TS_PERF_DISABLE_NOTHING"></span><span id="ts_perf_disable_nothing"></span>

<span data-ttu-id="d876e-127"><span id="TS_PERF_DISABLE_NOTHING"></span><span id="ts_perf_disable_nothing"></span>**TS \_效能 \_ 停用 \_ 任何** (0x00000000) </span><span class="sxs-lookup"><span data-stu-id="d876e-127"><span id="TS_PERF_DISABLE_NOTHING"></span><span id="ts_perf_disable_nothing"></span>**TS\_PERF\_DISABLE\_NOTHING** (0x00000000)</span></span>


</dt> <dd>

<span data-ttu-id="d876e-128">未停用任何功能。</span><span class="sxs-lookup"><span data-stu-id="d876e-128">No features are disabled.</span></span>

</dd> <dt>

<span id="TS_PERF_DISABLE_WALLPAPER"></span><span id="ts_perf_disable_wallpaper"></span>

<span data-ttu-id="d876e-129"><span id="TS_PERF_DISABLE_WALLPAPER"></span><span id="ts_perf_disable_wallpaper"></span>**TS \_效能 \_ 停用 \_ 壁紙** (0x00000001) </span><span class="sxs-lookup"><span data-stu-id="d876e-129"><span id="TS_PERF_DISABLE_WALLPAPER"></span><span id="ts_perf_disable_wallpaper"></span>**TS\_PERF\_DISABLE\_WALLPAPER** (0x00000001)</span></span>


</dt> <dd>

<span data-ttu-id="d876e-130">桌面上不會顯示壁紙。</span><span class="sxs-lookup"><span data-stu-id="d876e-130">Wallpaper on the desktop is not displayed.</span></span>

</dd> <dt>

<span id="TS_PERF_DISABLE_FULLWINDOWDRAG"></span><span id="ts_perf_disable_fullwindowdrag"></span>

<span data-ttu-id="d876e-131"><span id="TS_PERF_DISABLE_FULLWINDOWDRAG"></span><span id="ts_perf_disable_fullwindowdrag"></span>**TS \_效能 \_ 停用 \_ FULLWINDOWDRAG** (0x00000002) </span><span class="sxs-lookup"><span data-stu-id="d876e-131"><span id="TS_PERF_DISABLE_FULLWINDOWDRAG"></span><span id="ts_perf_disable_fullwindowdrag"></span>**TS\_PERF\_DISABLE\_FULLWINDOWDRAG** (0x00000002)</span></span>


</dt> <dd>

<span data-ttu-id="d876e-132">全視窗拖曳已停用;移動視窗時只會顯示視窗大綱。</span><span class="sxs-lookup"><span data-stu-id="d876e-132">Full-window drag is disabled; only the window outline is displayed when the window is moved.</span></span>

</dd> <dt>

<span id="TS_PERF_DISABLE_MENUANIMATIONS"></span><span id="ts_perf_disable_menuanimations"></span>

<span data-ttu-id="d876e-133"><span id="TS_PERF_DISABLE_MENUANIMATIONS"></span><span id="ts_perf_disable_menuanimations"></span>**TS \_PERF \_ DISABLE \_ MENUANIMATIONS** (0x00000004) </span><span class="sxs-lookup"><span data-stu-id="d876e-133"><span id="TS_PERF_DISABLE_MENUANIMATIONS"></span><span id="ts_perf_disable_menuanimations"></span>**TS\_PERF\_DISABLE\_MENUANIMATIONS** (0x00000004)</span></span>


</dt> <dd>

<span data-ttu-id="d876e-134">功能表動畫已停用。</span><span class="sxs-lookup"><span data-stu-id="d876e-134">Menu animations are disabled.</span></span>

</dd> <dt>

<span id="TS_PERF_DISABLE_THEMING"></span><span id="ts_perf_disable_theming"></span>

<span data-ttu-id="d876e-135"><span id="TS_PERF_DISABLE_THEMING"></span><span id="ts_perf_disable_theming"></span>**TS \_效能 \_ 停用 \_ 主題** (0x00000008) </span><span class="sxs-lookup"><span data-stu-id="d876e-135"><span id="TS_PERF_DISABLE_THEMING"></span><span id="ts_perf_disable_theming"></span>**TS\_PERF\_DISABLE\_THEMING** (0x00000008)</span></span>


</dt> <dd>

<span data-ttu-id="d876e-136">主題已停用。</span><span class="sxs-lookup"><span data-stu-id="d876e-136">Themes are disabled.</span></span>

</dd> <dt>

<span id="TS_PERF_ENABLE_ENHANCED_GRAPHICS"></span><span id="ts_perf_enable_enhanced_graphics"></span>

<span data-ttu-id="d876e-137"><span id="TS_PERF_ENABLE_ENHANCED_GRAPHICS"></span><span id="ts_perf_enable_enhanced_graphics"></span>**TS \_效能 \_ 啟用 \_ 增強的圖形** (0x00000010) </span><span class="sxs-lookup"><span data-stu-id="d876e-137"><span id="TS_PERF_ENABLE_ENHANCED_GRAPHICS"></span><span id="ts_perf_enable_enhanced_graphics"></span>**TS\_PERF\_ENABLE\_ENHANCED GRAPHICS** (0x00000010)</span></span>


</dt> <dd>

<span data-ttu-id="d876e-138">啟用增強的圖形。</span><span class="sxs-lookup"><span data-stu-id="d876e-138">Enable enhanced graphics.</span></span>

</dd> <dt>

<span id="TS_PERF_DISABLE_CURSOR_SHADOW"></span><span id="ts_perf_disable_cursor_shadow"></span>

<span data-ttu-id="d876e-139"><span id="TS_PERF_DISABLE_CURSOR_SHADOW"></span><span id="ts_perf_disable_cursor_shadow"></span>**TS \_效能 \_ 停用資料 \_ 指標 \_ 陰影** (0x00000020) </span><span class="sxs-lookup"><span data-stu-id="d876e-139"><span id="TS_PERF_DISABLE_CURSOR_SHADOW"></span><span id="ts_perf_disable_cursor_shadow"></span>**TS\_PERF\_DISABLE\_CURSOR\_SHADOW** (0x00000020)</span></span>


</dt> <dd>

<span data-ttu-id="d876e-140">沒有顯示資料指標的陰影。</span><span class="sxs-lookup"><span data-stu-id="d876e-140">No shadow is displayed for the cursor.</span></span>

</dd> <dt>

<span id="TS_PERF_DISABLE_CURSORSETTINGS"></span><span id="ts_perf_disable_cursorsettings"></span>

<span data-ttu-id="d876e-141"><span id="TS_PERF_DISABLE_CURSORSETTINGS"></span><span id="ts_perf_disable_cursorsettings"></span>**TS \_PERF \_ DISABLE \_ CURSORSETTINGS** (0x00000040) </span><span class="sxs-lookup"><span data-stu-id="d876e-141"><span id="TS_PERF_DISABLE_CURSORSETTINGS"></span><span id="ts_perf_disable_cursorsettings"></span>**TS\_PERF\_DISABLE\_CURSORSETTINGS** (0x00000040)</span></span>


</dt> <dd>

<span data-ttu-id="d876e-142">資料指標閃爍已停用。</span><span class="sxs-lookup"><span data-stu-id="d876e-142">Cursor blinking is disabled.</span></span>

</dd> <dt>

<span id="TS_PERF_ENABLE_FONT_SMOOTHING"></span><span id="ts_perf_enable_font_smoothing"></span>

<span data-ttu-id="d876e-143"><span id="TS_PERF_ENABLE_FONT_SMOOTHING"></span><span id="ts_perf_enable_font_smoothing"></span>**TS \_效能 \_ 啟用 \_ 字型 \_ 平滑** 處理 (0x00000080) </span><span class="sxs-lookup"><span data-stu-id="d876e-143"><span id="TS_PERF_ENABLE_FONT_SMOOTHING"></span><span id="ts_perf_enable_font_smoothing"></span>**TS\_PERF\_ENABLE\_FONT\_SMOOTHING** (0x00000080)</span></span>


</dt> <dd>

<span data-ttu-id="d876e-144">啟用字型平滑處理。</span><span class="sxs-lookup"><span data-stu-id="d876e-144">Enable font smoothing.</span></span>

</dd> <dt>

<span id="TS_PERF_ENABLE_DESKTOP_COMPOSITION"></span><span id="ts_perf_enable_desktop_composition"></span>

<span data-ttu-id="d876e-145"><span id="TS_PERF_ENABLE_DESKTOP_COMPOSITION"></span><span id="ts_perf_enable_desktop_composition"></span>**TS \_效能 \_ 啟用 \_ 桌上型電腦 \_ 組合** (0x00000100) </span><span class="sxs-lookup"><span data-stu-id="d876e-145"><span id="TS_PERF_ENABLE_DESKTOP_COMPOSITION"></span><span id="ts_perf_enable_desktop_composition"></span>**TS\_PERF\_ENABLE\_DESKTOP\_COMPOSITION** (0x00000100)</span></span>


</dt> <dd>

<span data-ttu-id="d876e-146">啟用桌面組合。</span><span class="sxs-lookup"><span data-stu-id="d876e-146">Enable desktop composition.</span></span>

</dd> <dt>

<span id="TS_PERF_DEFAULT_NONPERFCLIENT_SETTING"></span><span id="ts_perf_default_nonperfclient_setting"></span>

<span data-ttu-id="d876e-147"><span id="TS_PERF_DEFAULT_NONPERFCLIENT_SETTING"></span><span id="ts_perf_default_nonperfclient_setting"></span>**TS \_效能 \_ 預設 \_ NONPERFCLIENT \_ 設定** (0x40000000) </span><span class="sxs-lookup"><span data-stu-id="d876e-147"><span id="TS_PERF_DEFAULT_NONPERFCLIENT_SETTING"></span><span id="ts_perf_default_nonperfclient_setting"></span>**TS\_PERF\_DEFAULT\_NONPERFCLIENT\_SETTING** (0x40000000)</span></span>


</dt> <dd>

<span data-ttu-id="d876e-148">在內部針對不知道此設定的用戶端設定。</span><span class="sxs-lookup"><span data-stu-id="d876e-148">Set internally for clients not aware of this setting.</span></span>

</dd> <dt>

<span id="TS_PERF_RESERVED1"></span><span id="ts_perf_reserved1"></span>

<span data-ttu-id="d876e-149"><span id="TS_PERF_RESERVED1"></span><span id="ts_perf_reserved1"></span>**TS \_效能 \_ RESERVED1** (0x80000000) </span><span class="sxs-lookup"><span data-stu-id="d876e-149"><span id="TS_PERF_RESERVED1"></span><span id="ts_perf_reserved1"></span>**TS\_PERF\_RESERVED1** (0x80000000)</span></span>


</dt> <dd>

<span data-ttu-id="d876e-150">由用戶端在內部保留和使用。</span><span class="sxs-lookup"><span data-stu-id="d876e-150">Reserved and used internally by the client.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="d876e-151">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="d876e-151">Error codes</span></span>

<span data-ttu-id="d876e-152">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="d876e-152">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="d876e-153">備註</span><span class="sxs-lookup"><span data-stu-id="d876e-153">Remarks</span></span>

<span data-ttu-id="d876e-154">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="d876e-154">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d876e-155">規格需求</span><span class="sxs-lookup"><span data-stu-id="d876e-155">Requirements</span></span>



| <span data-ttu-id="d876e-156">需求</span><span class="sxs-lookup"><span data-stu-id="d876e-156">Requirement</span></span> | <span data-ttu-id="d876e-157">值</span><span class="sxs-lookup"><span data-stu-id="d876e-157">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d876e-158">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d876e-158">Minimum supported client</span></span><br/> | <span data-ttu-id="d876e-159">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d876e-159">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="d876e-160">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d876e-160">Minimum supported server</span></span><br/> | <span data-ttu-id="d876e-161">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d876e-161">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="d876e-162">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="d876e-162">Type library</span></span><br/>             | <dl> <span data-ttu-id="d876e-163"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d876e-163"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="d876e-164">DLL</span><span class="sxs-lookup"><span data-stu-id="d876e-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d876e-165"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d876e-165"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="d876e-166">IID</span><span class="sxs-lookup"><span data-stu-id="d876e-166">IID</span></span><br/>                      | <span data-ttu-id="d876e-167">IID \_ IMsRdpClientAdvancedSettings 定義為3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="d876e-167">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d876e-168">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d876e-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d876e-169">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="d876e-169">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="d876e-170">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="d876e-170">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="d876e-171">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="d876e-171">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="d876e-172">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="d876e-172">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="d876e-173">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="d876e-173">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="d876e-174">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="d876e-174">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="d876e-175">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="d876e-175">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="d876e-176">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="d876e-176">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





