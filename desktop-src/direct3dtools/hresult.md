---
description: 圖形診斷捕捉介面的自訂 HRESULT 值。
MS-HAID: vspixengine.Hresult
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Hresult 列舉
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 246FA53F-FF5B-44E1-BABB-F45AE0212687
api_name:
- Hresult
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3d5419feb0acb5967132fbb804a9bbc11bfa4248
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510053"
---
# <a name="span-idvspixenginehresultspanhresult-enumeration"></a><span id="vspixengine.hresult"></span>Hresult 列舉

圖形診斷捕捉介面的自訂 HRESULT 值。

## <a name="syntax"></a>Syntax


```C++
};
```

## <a name="constants"></a>常數

<span id="PIX_S_OK"></span><span id="pix_s_ok"></span>**PIX \_ S \_ 正常**  
一般 HRESULT，表示作業如預期般成功。

<span id="PIX_S_FALSE"></span><span id="pix_s_false"></span>**PIX \_ S \_ FALSE**  
一般 HRESULT，表示作業已成功，但以與預期不同的方式運作。

<span id="PIX_ERROR_FILE_NOT_FOUND"></span><span id="pix_error_file_not_found"></span>**\_ \_ \_ \_ 找不到 PIX 錯誤檔案**  
將 \_ \_ 找不到錯誤檔案的自訂 HRESULT \_ 。

<span id="PIX_ERROR_BAD_ENVIRONMENT"></span><span id="pix_error_bad_environment"></span>**PIX \_ 錯誤 \_ 的 \_ 環境錯誤**  
將錯誤環境錯誤的自訂 HRESULT \_ \_ 。

<span id="PIX_ERROR_BAD_FORMAT"></span><span id="pix_error_bad_format"></span>**PIX \_ 錯誤 \_ \_ 格式錯誤**  
將錯誤格式錯誤的自訂 HRESULT \_ \_ 。

<span id="PIX_ERROR_SHARING_VIOLATION"></span><span id="pix_error_sharing_violation"></span>**PIX \_ 錯誤 \_ 共用 \_ 違規**  
將錯誤共用違規的自訂 HRESULT \_ \_ 。

<span id="PIX_ERROR_DISK_FULL"></span><span id="pix_error_disk_full"></span>**PIX \_ 錯誤 \_ 磁片已 \_ 滿**  
將錯誤磁片已滿的自訂 HRESULT \_ \_ 。

<span id="PIX_ERROR_MORE_DATA"></span><span id="pix_error_more_data"></span>**PIX \_ 錯誤 \_ 更多 \_ 資料**  
將錯誤更多資料的自訂 HRESULT \_ \_ 。

<span id="PIX_E_MISSING_DEBUG_KITS_POLICY"></span><span id="pix_e_missing_debug_kits_policy"></span>**PIX \_ E \_ 遺失的 \_ DEBUG \_ 套件 \_ 原則**  
自訂 HRESULT，表示缺少 Debug 套件原則。

<span id="PIX_E_INVALID_VERSION"></span><span id="pix_e_invalid_version"></span>**PIX \_ E \_ 不正確 \_ 版本**  
自訂 HRESULT，表示正在使用不正確版本。

<span id="PIX_E_USING_DCOMP"></span><span id="pix_e_using_dcomp"></span>**\_ \_ 使用 \_ DCOMP 的 PIX E**  
自訂 HRESULT，指出 DirectComposition 正在使用中 (不支援 DirectComposition 的捕獲。 ) 

<span id="PIX_E_USING_DIRECTWRITE"></span><span id="pix_e_using_directwrite"></span>**\_ \_ 使用 \_ DIRECTWRITE 的 PIX E**  
自訂 HRESULT，指出 DirectWrite 正在使用中 (不支援 DirectWrite 的捕獲。 ) 

<span id="PIX_E_USING_D3D9"></span><span id="pix_e_using_d3d9"></span>**\_ \_ 使用 \_ D3D9 的 PIX E**  
自訂 HRESULT，表示 Windows 10 不支援 Direct3D9 在使用中 (捕捉 Direct3D9。 ) 

<span id="PIX_E_CANT_CREATE_SHADER"></span><span id="pix_e_cant_create_shader"></span>**PIX \_ E \_ 無法 \_ 建立 \_ 著色器**  
自訂 HRESULT，表示無法建立指定的著色器。

<span id="PIX_E_USING_D2D"></span><span id="pix_e_using_d2d"></span>**\_ \_ 使用 \_ D2D 的 PIX E**  
自訂 HRESULT，指出 Direct2D 正在使用中 (不支援 Direct2D 的捕獲。 ) 

<span id="PIX_E_NO_FRAMES"></span><span id="pix_e_no_frames"></span>**PIX \_ E \_ 沒有 \_ 框架**  
自訂 HRESULT，指出未捕獲任何框架。

<span id="PIX_E_DISABLE_SPY"></span><span id="pix_e_disable_spy"></span>**PIX \_ E \_ 停用 \_ SPY**  

<span id="PIX_E_WIN8LOG_ON_WIN7"></span><span id="pix_e_win8log_on_win7"></span>**\_ \_ \_ WIN7 上的 PIX E WIN8LOG \_**  
自訂 HRESULT，表示無法在 Windows 7 上播放 Windows 8 vsglog。

<span id="PIX_E_BUILD_SHADER_TRACE"></span><span id="pix_e_build_shader_trace"></span>**PIX \_ E \_ 組建 \_ 著色器 \_ 追蹤**  
自訂 HRESULT，表示建立著色器追蹤時發生錯誤。

<span id="PIX_E_NO_CS_DATA_VISUALIZATION"></span><span id="pix_e_no_cs_data_visualization"></span>**PIX \_ E \_ NO \_ CS \_ 資料 \_ 視覺效果**  
自訂 HRESULT，指出沒有計算著色器資料視覺效果。

<span id="PIX_E_MISMATCH_SDK"></span><span id="pix_e_mismatch_sdk"></span>**PIX \_ E \_ 不相符 \_ SDK**  
自訂 HRESULT，表示與目前的 SDK 不符。

<span id="PIX_E_POSSIBLE_MISMATCH_SDK"></span><span id="pix_e_possible_mismatch_sdk"></span>**PIX \_ E \_ 可能 \_ 不相符的 \_ SDK**  
自訂 HRESULT，指出目前的 SDK 可能不相符。

<span id="PIX_E_UNDETECTABLE_PIXEL"></span><span id="pix_e_undetectable_pixel"></span>**PIX \_ E 無法偵測 \_ \_ 圖元**  
自訂 HRESULT，表示有無法偵測的圖元。

<span id="PIX_E_CANT_DEBUG_SHADER_USING_SYSTEM_VALUE_SEMANTICS"></span><span id="pix_e_cant_debug_shader_using_system_value_semantics"></span>**PIX \_ E \_ 無法 \_ \_ \_ 使用 \_ 系統 \_ 值 \_ 語義來對著色器進行 DEBUG 錯**  
自訂 HRESULT，表示無法使用系統值語義來調試 sahder。

<span id="PIX_S_UPDATEAVAILABLE"></span><span id="pix_s_updateavailable"></span>**PIX \_ S \_ UPDATEAVAILABLE**  
自訂 HRESULT，指出有可用的更新。

<span id="PIX_DXGI_STATUS_NO_REDIRECTION"></span><span id="pix_dxgi_status_no_redirection"></span>**PIX \_ DXGI \_ 狀態 \_ 無 \_ 重新導向**  
將 DXGI 狀態不會重新導向的自訂 HRESULT \_ \_ \_ 。

<span id="PIX_DXGI_STATUS_NO_DESKTOP_ACCESS"></span><span id="pix_dxgi_status_no_desktop_access"></span>**PIX \_ DXGI \_ 狀態 \_ 沒有 \_ 桌面 \_ 存取**  
將 DXGI \_ 狀態 \_ 無 \_ 桌面存取的自訂 HRESULT \_ 。

<span id="PIX_DXGI_STATUS_GRAPHICS_VIDPN_SOURCE_IN_USE"></span><span id="pix_dxgi_status_graphics_vidpn_source_in_use"></span>**\_ \_ \_ \_ \_ \_ 使用中的 PIX DXGI 狀態圖形 VIDPN 來源 \_**  
使用將 DXGI \_ 狀態 \_ 圖形 \_ VIDPN \_ 來源的 \_ 自訂 HRESULT \_ 。

<span id="PIX_DXGI_STATUS_MODE_CHANGED"></span><span id="pix_dxgi_status_mode_changed"></span>**PIX \_ DXGI \_ 狀態 \_ 模式 \_ 已變更**  
將 DXGI \_ 狀態 \_ 模式已變更的自訂 HRESULT \_ 。

<span id="PIX_DXGI_STATUS_MODE_CHANGE_IN_PROGRESS"></span><span id="pix_dxgi_status_mode_change_in_progress"></span>**PIX \_ DXGI \_ 狀態 \_ 模式 \_ 變更 \_ \_ 進行中**  
將 DXGI \_ 狀態 \_ 模式 \_ 變更 \_ \_ 進行中的自訂 HRESULT。

<span id="PIX_DXGI_STATUS_UNOCCLUDED"></span><span id="pix_dxgi_status_unoccluded"></span>**PIX \_ DXGI \_ 狀態 \_ UNOCCLUDED**  
將 DXGI 狀態 UNOCCLUDED 的自訂 HRESULT \_ \_ 。

<span id="PIX_DXGI_STATUS_DDA_WAS_STILL_DRAWING"></span><span id="pix_dxgi_status_dda_was_still_drawing"></span>**PIX \_ DXGI \_ 狀態 \_ DDA \_ \_ 仍在 \_ 繪圖中**  
將 DXGI 狀態 DDA 的自訂 HRESULT \_ \_ 仍在 \_ \_ \_ 繪圖中。

<span id="PIX_E_NOTIMPL"></span><span id="pix_e_notimpl"></span>**PIX \_ E \_ >NOTIMPL**  
將 E >notimpl 的自訂 HRESULT \_ 。

<span id="PIX_E_NOINTERFACE"></span><span id="pix_e_nointerface"></span>**PIX \_ E \_ NOINTERFACE**  
將 E NOINTERFACE 的自訂 HRESULT \_ 。

<span id="PIX_E_POINTER"></span><span id="pix_e_pointer"></span>**PIX \_ E \_ 指標**  
將 E 指標的自訂 HRESULT \_ 。

<span id="PIX_E_ABORT"></span><span id="pix_e_abort"></span>**PIX \_ E \_ 中止**  
將 E 中止的自訂 HRESULT \_ 。

<span id="PIX_E_FAIL"></span><span id="pix_e_fail"></span>**PIX \_ E \_ 失敗**  
將 E 失敗的自訂 HRESULT \_ 。

<span id="PIX_E_UNEXPECTED"></span><span id="pix_e_unexpected"></span>**PIX \_ E 未 \_ 預期**  
將 E 非預期的自訂 HRESULT \_ 。

<span id="PIX_E_ACCESSDENIED"></span><span id="pix_e_accessdenied"></span>**PIX \_ E \_ ACCESSDENIED**  
將 E ACCESSDENIED 的自訂 HRESULT \_ 。

<span id="PIX_E_HANDLE"></span><span id="pix_e_handle"></span>**PIX \_ E \_ 控制碼**  
將 E 控制碼的自訂 HRESULT \_ 。

<span id="PIX_E_OUTOFMEMORY"></span><span id="pix_e_outofmemory"></span>**PIX \_ E \_ OUTOFMEMORY**  
將 E OUTOFMEMORY 的自訂 HRESULT \_ 。

<span id="PIX_E_INVALIDARG"></span><span id="pix_e_invalidarg"></span>**PIX \_ E \_ INVALIDARG**  
將 E INVALIDARG 的自訂 HRESULT \_ 。

<span id="PIX_XBOX_ERROR_DISK_FULL"></span><span id="pix_xbox_error_disk_full"></span>**PIX \_ XBOX \_ ERROR \_ 磁片已 \_ 滿**  
指出磁片已滿的自訂 HRESULT。

<span id="PIX_WS_E_ADDRESS_IN_USE"></span><span id="pix_ws_e_address_in_use"></span>**\_ \_ \_ \_ 使用中的 PIX WS E 位址 \_**  
自訂 HRESULT，表示位址已在使用中。

<span id="PIX_WS_E_MISSING_KITS_POLICY"></span><span id="pix_ws_e_missing_kits_policy"></span>**PIX \_ WS \_ E \_ 遺失 \_ 套件 \_ 原則**  
自訂 HRESULT，表示無法使用位址。

<span id="PIX_TE_FAILEDTOLOADSOFTWAREMODULE"></span><span id="pix_te_failedtoloadsoftwaremodule"></span>**PIX \_ TE \_ FAILEDTOLOADSOFTWAREMODULE**  
自訂 HRESULT，表示無法載入必要的軟體模組。

<span id="PIX_TE_USEDSOFTWAREMODULETHATWASNTWARPORREF"></span><span id="pix_te_usedsoftwaremodulethatwasntwarporref"></span>**PIX \_ TE \_ USEDSOFTWAREMODULETHATWASNTWARPORREF**  
自訂 HRESULT，表示所使用的軟體模組並非變形或 REF 驅動程式。

<span id="PIX_TE_CORRUPTEDFILE"></span><span id="pix_te_corruptedfile"></span>**PIX \_ TE \_ CORRUPTEDFILE**  
自訂 HRESULT，表示檔案已損毀。

<span id="PIX_TE_FAILEDTOOPENFILE"></span><span id="pix_te_failedtoopenfile"></span>**PIX \_ TE \_ FAILEDTOOPENFILE**  
自訂 HRESULT，表示檔案無法開啟。

<span id="PIX_TE_CALLFAILEDONPLAYBACK"></span><span id="pix_te_callfailedonplayback"></span>**PIX \_ TE \_ CALLFAILEDONPLAYBACK**  
自訂 HRESULT，表示播放期間的呼叫失敗。

<span id="PIX_TE_UNKNOWNUUID"></span><span id="pix_te_unknownuuid"></span>**PIX \_ TE \_ UNKNOWNUUID**  
自訂 HRESULT，指出發生未知的 UUID;永遠不會發生這種情況。

<span id="PIX_TE_NOTCAPTUREFILEORCORRUPTED"></span><span id="pix_te_notcapturefileorcorrupted"></span>**PIX \_ TE \_ NOTCAPTUREFILEORCORRUPTED**  
自訂 HRESULT，表示檔案不是捕獲檔案或已損毀。

<span id="PIX_TE_NEWERFILE"></span><span id="pix_te_newerfile"></span>**PIX \_ TE \_ NEWERFILE**  

<span id="PIX_TE_OLDERFILE"></span><span id="pix_te_olderfile"></span>**PIX \_ TE \_ OLDERFILE**  

<span id="PIX_TE_INVALIDMOMENT"></span><span id="pix_te_invalidmoment"></span>**PIX \_ TE \_ INVALIDMOMENT**  

<span id="PIX_TE_BAD_DRIVER"></span><span id="pix_te_bad_driver"></span>**PIX \_ TE \_ \_ 驅動程式錯誤**  
自訂 HRESULT，指出驅動程式不正確。

<span id="PIX_ERROR_CANT_ACCESS_DEPTHSTENCIL_IN_CPU"></span><span id="pix_error_cant_access_depthstencil_in_cpu"></span>**PIX \_ 錯誤 \_ 無法 \_ 存取 \_ \_ CPU 中的 DEPTHSTENCIL \_**  
自訂 HRESULT，表示 CPU 嘗試存取深度樣板緩衝區，而導致錯誤。

<span id="PIX_ERROR_CANT_RESOLVE_MULTISAMPLED_TEXTURE"></span><span id="pix_error_cant_resolve_multisampled_texture"></span>**PIX \_ 錯誤 \_ 無法 \_ 解析 \_ 多重取樣 \_ 材質**  
自訂 HRESULT，表示嘗試解析多樣本材質，導致錯誤。

<span id="PIX_DXGI_ERROR_INVALID_CALL"></span><span id="pix_dxgi_error_invalid_call"></span>**PIX \_ DXGI \_ 錯誤 \_ 不正確 \_ 呼叫**  
將 DXGI \_ 錯誤無效呼叫的自訂 HRESULT \_ \_ 。

<span id="PIX_DXGI_ERROR_NOT_FOUND"></span><span id="pix_dxgi_error_not_found"></span>**\_ \_ \_ \_ 找不到 PIX DXGI 錯誤**  
\_ \_ 找不到將 DXGI 錯誤的自訂 HRESULT \_ 。

<span id="PIX_DXGI_ERROR_MORE_DATA"></span><span id="pix_dxgi_error_more_data"></span>**PIX \_ DXGI \_ 錯誤 \_ 更多 \_ 資料**  
將 DXGI \_ 錯誤 \_ 更多資料的自訂 HRESULT \_ 。

<span id="PIX_DXGI_ERROR_UNSUPPORTED"></span><span id="pix_dxgi_error_unsupported"></span>**未 \_ 支援 PIX DXGI \_ 錯誤 \_**  
不支援將 DXGI 錯誤的自訂 HRESULT \_ \_ 。

<span id="PIX_DXGI_ERROR_DEVICE_REMOVED"></span><span id="pix_dxgi_error_device_removed"></span>**\_已移除 PIX DXGI \_ 錯誤 \_ 裝置 \_**  
已移除將 DXGI 錯誤裝置的自訂 HRESULT \_ \_ \_ 。

<span id="PIX_DXGI_ERROR_DEVICE_HUNG"></span><span id="pix_dxgi_error_device_hung"></span>**PIX \_ DXGI \_ 錯誤 \_ 裝置無 \_ 反應**  
將 DXGI 錯誤裝置無反應的自訂 HRESULT \_ \_ \_ 。

<span id="PIX_DXGI_ERROR_DEVICE_RESET"></span><span id="pix_dxgi_error_device_reset"></span>**PIX \_ DXGI \_ 錯誤 \_ 裝置 \_ 重設**  
將 DXGI \_ 錯誤 \_ 裝置重設的自訂 HRESULT \_ 。

<span id="PIX_DXGI_ERROR_WAS_STILL_DRAWING"></span><span id="pix_dxgi_error_was_still_drawing"></span>**PIX \_ DXGI \_ 錯誤 \_ \_ 仍在 \_ 繪圖中**  
將 DXGI 錯誤的自訂 \_ HRESULT \_ \_ 仍在 \_ 繪圖中。

<span id="PIX_DXGI_ERROR_FRAME_STATISTICS_DISJOINT"></span><span id="pix_dxgi_error_frame_statistics_disjoint"></span>**PIX \_ DXGI \_ 錯誤 \_ 框架 \_ 統計資料不 \_ 相交**  
將 DXGI \_ 錯誤 \_ 框架 \_ 統計資料的自訂 HRESULT \_ 。

<span id="PIX_DXGI_ERROR_GRAPHICS_VIDPN_SOURCE_IN_USE"></span><span id="pix_dxgi_error_graphics_vidpn_source_in_use"></span>**\_ \_ \_ \_ \_ \_ 使用中的 PIX DXGI 錯誤圖形 VIDPN 來源 \_**  
使用將 DXGI \_ 錯誤 \_ 圖形 \_ VIDPN \_ 來源的 \_ 自訂 HRESULT \_ 。

<span id="PIX_DXGI_ERROR_DRIVER_INTERNAL_ERROR"></span><span id="pix_dxgi_error_driver_internal_error"></span>**PIX \_ DXGI \_ 錯誤 \_ 驅動程式 \_ 內部 \_ 錯誤**  
將 DXGI \_ 錯誤 \_ 驅動程式 \_ 內部錯誤的自訂 HRESULT \_ 。

<span id="PIX_DXGI_ERROR_NONEXCLUSIVE"></span><span id="pix_dxgi_error_nonexclusive"></span>**PIX \_ DXGI \_ 錯誤非 \_ 獨佔**  
將 DXGI 錯誤非獨佔的自訂 HRESULT \_ \_ 。

<span id="PIX_DXGI_ERROR_NOT_CURRENTLY_AVAILABLE"></span><span id="pix_dxgi_error_not_currently_available"></span>**PIX \_ DXGI \_ 錯誤 \_ \_ 目前無法 \_ 使用**  
將 \_ \_ 目前無法使用的 DXGI 錯誤的自訂 HRESULT \_ \_ 。

<span id="PIX_DXGI_ERROR_REMOTE_CLIENT_DISCONNECTED"></span><span id="pix_dxgi_error_remote_client_disconnected"></span>**PIX \_ DXGI \_ 錯誤 \_ 遠端 \_ 用戶端 \_ 中斷連線**  
將 DXGI \_ 錯誤 \_ 遠端 \_ 用戶端中斷的自訂 HRESULT \_ 。

<span id="PIX_DXGI_ERROR_REMOTE_OUTOFMEMORY"></span><span id="pix_dxgi_error_remote_outofmemory"></span>**PIX \_ DXGI \_ 錯誤 \_ 遠端 \_ OUTOFMEMORY**  
將 DXGI \_ ERROR REMOTE OUTOFMEMORY 的自訂 HRESULT \_ \_ 。

<span id="PIX_DXGI_ERROR_MODE_CHANGE_IN_PROGRESS"></span><span id="pix_dxgi_error_mode_change_in_progress"></span>**PIX \_ DXGI \_ 錯誤 \_ 模式 \_ 變更 \_ \_ 進行中**  
將 DXGI \_ 錯誤 \_ 模式 \_ 變更 \_ \_ 進行中的自訂 HRESULT。

<span id="PIX_DXGI_ERROR_ACCESS_LOST"></span><span id="pix_dxgi_error_access_lost"></span>**PIX \_ DXGI \_ 錯誤 \_ 存取 \_ 遺失**  
將 DXGI \_ 錯誤存取遺失的自訂 HRESULT \_ \_ 。

<span id="PIX_DXGI_ERROR_WAIT_TIMEOUT"></span><span id="pix_dxgi_error_wait_timeout"></span>**PIX \_ DXGI \_ 錯誤 \_ 等候 \_ 超時**  
將 DXGI \_ 錯誤等候超時的自訂 HRESULT \_ \_ 。

<span id="PIX_DXGI_ERROR_SESSION_DISCONNECTED"></span><span id="pix_dxgi_error_session_disconnected"></span>**PIX \_ DXGI \_ 錯誤 \_ 會話已 \_ 中斷連線**  
將 DXGI 錯誤會話已中斷連線的自訂 HRESULT \_ \_ \_ 。

<span id="PIX_DXGI_ERROR_RESTRICT_TO_OUTPUT_STALE"></span><span id="pix_dxgi_error_restrict_to_output_stale"></span>**PIX \_ DXGI \_ 錯誤 \_ 限制 \_ 為 \_ 輸出 \_ 過時**  
將 DXGI \_ 錯誤 \_ 限制 \_ 為 \_ 輸出 \_ 過時的自訂 HRESULT。

<span id="PIX_DXGI_ERROR_CANNOT_PROTECT_CONTENT"></span><span id="pix_dxgi_error_cannot_protect_content"></span>**PIX \_ DXGI \_ 錯誤 \_ 無法 \_ 保護 \_ 內容**  
將 DXGI 錯誤的自訂 \_ HRESULT \_ 無法 \_ 保護 \_ 內容。

<span id="PIX_DXGI_ERROR_ACCESS_DENIED"></span><span id="pix_dxgi_error_access_denied"></span>**PIX \_ DXGI \_ \_ 拒絕存取 \_ 錯誤**  
將 DXGI 錯誤存取的自訂 HRESULT \_ \_ \_ 。

<span id="PIX_DXGI_ERROR_NAME_ALREADY_EXISTS"></span><span id="pix_dxgi_error_name_already_exists"></span>**PIX \_ DXGI \_ 錯誤 \_ 名稱 \_ 已 \_ 存在**  
將 DXGI 錯誤名稱的自訂 HRESULT \_ \_ \_ 已經 \_ 存在。

<span id="PIX_DXGI_ERROR_SDK_COMPONENT_MISSING"></span><span id="pix_dxgi_error_sdk_component_missing"></span>**PIX \_ DXGI \_ 錯誤 \_ SDK \_ 元件 \_ 遺失**  
缺少將 DXGI \_ 錯誤 SDK 元件的自訂 HRESULT \_ \_ \_ 。

<span id="PIX_DXGI_DDI_ERR_WASSTILLDRAWING"></span><span id="pix_dxgi_ddi_err_wasstilldrawing"></span>**PIX \_ DXGI \_ DDI \_ ERR \_ WASSTILLDRAWING**  
將 DXGI \_ DDI ERR WASSTILLDRAWING 的自訂 HRESULT \_ \_ 。

<span id="PIX_DXGI_DDI_ERR_UNSUPPORTED"></span><span id="pix_dxgi_ddi_err_unsupported"></span>**PIX \_ DXGI \_ DDI \_ 錯誤 \_ 不受支援**  
將 DXGI DDI ERR 的自訂 HRESULT \_ \_ \_ 不受支援。

<span id="PIX_DXGI_DDI_ERR_NONEXCLUSIVE"></span><span id="pix_dxgi_ddi_err_nonexclusive"></span>**PIX \_ DXGI \_ DDI \_ 錯誤非 \_ 獨佔**  
將 DXGI DDI 錯誤非獨佔的自訂 HRESULT \_ \_ \_ 。

<span id="PIX_D3D10_ERROR_TOO_MANY_UNIQUE_STATE_OBJECTS"></span><span id="pix_d3d10_error_too_many_unique_state_objects"></span>**PIX \_ D3D10 \_ 錯誤 \_ 太 \_ 多 \_ 唯一的 \_ 狀態 \_ 物件**  
將 D3D10 \_ 錯誤 \_ 太 \_ 多 \_ 唯一 \_ 狀態 \_ 物件的自訂 HRESULT。

<span id="PIX_D3D10_ERROR_FILE_NOT_FOUND"></span><span id="pix_d3d10_error_file_not_found"></span>**\_ \_ \_ \_ \_ 找不到 PIX D3D10 錯誤檔案**  
\_ \_ \_ 找不到將 D3D10 錯誤檔案的自訂 HRESULT \_ 。

<span id="PIX_D3D11_ERROR_TOO_MANY_UNIQUE_STATE_OBJECTS"></span><span id="pix_d3d11_error_too_many_unique_state_objects"></span>**PIX \_ D3D11 \_ 錯誤 \_ 太 \_ 多 \_ 唯一的 \_ 狀態 \_ 物件**  
將 D3D11 \_ 錯誤 \_ 太 \_ 多 \_ 唯一 \_ 狀態 \_ 物件的自訂 HRESULT。

<span id="PIX_D3D11_ERROR_FILE_NOT_FOUND"></span><span id="pix_d3d11_error_file_not_found"></span>**\_ \_ \_ \_ \_ 找不到 PIX D3D11 錯誤檔案**  
\_ \_ \_ 找不到將 D3D11 錯誤檔案的自訂 HRESULT \_ 。

<span id="PIX_D3D11_ERROR_TOO_MANY_UNIQUE_VIEW_OBJECTS"></span><span id="pix_d3d11_error_too_many_unique_view_objects"></span>**PIX \_ D3D11 \_ 錯誤 \_ 太 \_ 多 \_ 唯一的 \_ VIEW \_ 物件**  
將 D3D11 的自訂 HRESULT \_ 錯誤 \_ 太 \_ 多 \_ 唯一 \_ VIEW \_ 物件。

<span id="PIX_D3D11_ERROR_DEFERRED_CONTEXT_MAP_WITHOUT_INITIAL_DISCARD"></span><span id="pix_d3d11_error_deferred_context_map_without_initial_discard"></span>**PIX \_ D3D11 \_ 錯誤 \_ 延遲的 \_ 內容 \_ 對應， \_ 沒有 \_ 初始 \_ 捨棄**  
自訂 HRESULT 將 D3D11 \_ 錯誤 \_ 延遲的 \_ 內容 \_ 對應， \_ 不含 \_ 初始 \_ 捨棄。

<span id="PIX_ERROR_OCCLUDED_DRAW_CALL"></span><span id="pix_error_occluded_draw_call"></span>**PIX \_ 錯誤 \_ PIXELS OCCLUDED \_ 繪製 \_ 呼叫**  
自訂 HRESULT，表示繪製呼叫已完全 pixels occluded，因而導致錯誤。

## <a name="requirements"></a>規格需求

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>標頭</p></td><td>Vspixengine。h</td></tr></tbody></table>

 

 



