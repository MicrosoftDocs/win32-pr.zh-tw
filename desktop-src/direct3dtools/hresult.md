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
# <a name="span-idvspixenginehresultspanhresult-enumeration"></a><span data-ttu-id="d5649-103"><span id="vspixengine.hresult"></span>Hresult 列舉</span><span class="sxs-lookup"><span data-stu-id="d5649-103"><span id="vspixengine.hresult"></span>Hresult enumeration</span></span>

<span data-ttu-id="d5649-104">圖形診斷捕捉介面的自訂 HRESULT 值。</span><span class="sxs-lookup"><span data-stu-id="d5649-104">Custom HRESULT values for the graphics diagnostics capture interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5649-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d5649-105">Syntax</span></span>


```C++
};
```

## <a name="constants"></a><span data-ttu-id="d5649-106">常數</span><span class="sxs-lookup"><span data-stu-id="d5649-106">Constants</span></span>

<span data-ttu-id="d5649-107"><span id="PIX_S_OK"></span><span id="pix_s_ok"></span>**PIX \_ S \_ 正常**</span><span class="sxs-lookup"><span data-stu-id="d5649-107"><span id="PIX_S_OK"></span><span id="pix_s_ok"></span>**PIX\_S\_OK**</span></span>  
<span data-ttu-id="d5649-108">一般 HRESULT，表示作業如預期般成功。</span><span class="sxs-lookup"><span data-stu-id="d5649-108">A common HRESULT which indicates that the operation succeeded as expected.</span></span>

<span data-ttu-id="d5649-109"><span id="PIX_S_FALSE"></span><span id="pix_s_false"></span>**PIX \_ S \_ FALSE**</span><span class="sxs-lookup"><span data-stu-id="d5649-109"><span id="PIX_S_FALSE"></span><span id="pix_s_false"></span>**PIX\_S\_FALSE**</span></span>  
<span data-ttu-id="d5649-110">一般 HRESULT，表示作業已成功，但以與預期不同的方式運作。</span><span class="sxs-lookup"><span data-stu-id="d5649-110">A common HRESULT which indicates that the operation succeeded, but in a different way than was expected.</span></span>

<span data-ttu-id="d5649-111"><span id="PIX_ERROR_FILE_NOT_FOUND"></span><span id="pix_error_file_not_found"></span>**\_ \_ \_ \_ 找不到 PIX 錯誤檔案**</span><span class="sxs-lookup"><span data-stu-id="d5649-111"><span id="PIX_ERROR_FILE_NOT_FOUND"></span><span id="pix_error_file_not_found"></span>**PIX\_ERROR\_FILE\_NOT\_FOUND**</span></span>  
<span data-ttu-id="d5649-112">將 \_ \_ 找不到錯誤檔案的自訂 HRESULT \_ 。</span><span class="sxs-lookup"><span data-stu-id="d5649-112">A custom HRESULT that echos ERROR\_FILE\_NOT\_FOUND.</span></span>

<span data-ttu-id="d5649-113"><span id="PIX_ERROR_BAD_ENVIRONMENT"></span><span id="pix_error_bad_environment"></span>**PIX \_ 錯誤 \_ 的 \_ 環境錯誤**</span><span class="sxs-lookup"><span data-stu-id="d5649-113"><span id="PIX_ERROR_BAD_ENVIRONMENT"></span><span id="pix_error_bad_environment"></span>**PIX\_ERROR\_BAD\_ENVIRONMENT**</span></span>  
<span data-ttu-id="d5649-114">將錯誤環境錯誤的自訂 HRESULT \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="d5649-114">A custom HRESULT that echos ERROR\_BAD\_ENVIRONMENT.</span></span>

<span data-ttu-id="d5649-115"><span id="PIX_ERROR_BAD_FORMAT"></span><span id="pix_error_bad_format"></span>**PIX \_ 錯誤 \_ \_ 格式錯誤**</span><span class="sxs-lookup"><span data-stu-id="d5649-115"><span id="PIX_ERROR_BAD_FORMAT"></span><span id="pix_error_bad_format"></span>**PIX\_ERROR\_BAD\_FORMAT**</span></span>  
<span data-ttu-id="d5649-116">將錯誤格式錯誤的自訂 HRESULT \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="d5649-116">A custom HRESULT that echos ERROR\_BAD\_FORMAT.</span></span>

<span data-ttu-id="d5649-117"><span id="PIX_ERROR_SHARING_VIOLATION"></span><span id="pix_error_sharing_violation"></span>**PIX \_ 錯誤 \_ 共用 \_ 違規**</span><span class="sxs-lookup"><span data-stu-id="d5649-117"><span id="PIX_ERROR_SHARING_VIOLATION"></span><span id="pix_error_sharing_violation"></span>**PIX\_ERROR\_SHARING\_VIOLATION**</span></span>  
<span data-ttu-id="d5649-118">將錯誤共用違規的自訂 HRESULT \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="d5649-118">A custom HRESULT that echos ERROR\_SHARING\_VIOLATION.</span></span>

<span data-ttu-id="d5649-119"><span id="PIX_ERROR_DISK_FULL"></span><span id="pix_error_disk_full"></span>**PIX \_ 錯誤 \_ 磁片已 \_ 滿**</span><span class="sxs-lookup"><span data-stu-id="d5649-119"><span id="PIX_ERROR_DISK_FULL"></span><span id="pix_error_disk_full"></span>**PIX\_ERROR\_DISK\_FULL**</span></span>  
<span data-ttu-id="d5649-120">將錯誤磁片已滿的自訂 HRESULT \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="d5649-120">A custom HRESULT that echos ERROR\_DISK\_FULL.</span></span>

<span data-ttu-id="d5649-121"><span id="PIX_ERROR_MORE_DATA"></span><span id="pix_error_more_data"></span>**PIX \_ 錯誤 \_ 更多 \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="d5649-121"><span id="PIX_ERROR_MORE_DATA"></span><span id="pix_error_more_data"></span>**PIX\_ERROR\_MORE\_DATA**</span></span>  
<span data-ttu-id="d5649-122">將錯誤更多資料的自訂 HRESULT \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="d5649-122">A custom HRESULT that echos ERROR\_MORE\_DATA.</span></span>

<span data-ttu-id="d5649-123"><span id="PIX_E_MISSING_DEBUG_KITS_POLICY"></span><span id="pix_e_missing_debug_kits_policy"></span>**PIX \_ E \_ 遺失的 \_ DEBUG \_ 套件 \_ 原則**</span><span class="sxs-lookup"><span data-stu-id="d5649-123"><span id="PIX_E_MISSING_DEBUG_KITS_POLICY"></span><span id="pix_e_missing_debug_kits_policy"></span>**PIX\_E\_MISSING\_DEBUG\_KITS\_POLICY**</span></span>  
<span data-ttu-id="d5649-124">自訂 HRESULT，表示缺少 Debug 套件原則。</span><span class="sxs-lookup"><span data-stu-id="d5649-124">A custom HRESULT which indicates that the Debug Kits policy is missing.</span></span>

<span data-ttu-id="d5649-125"><span id="PIX_E_INVALID_VERSION"></span><span id="pix_e_invalid_version"></span>**PIX \_ E \_ 不正確 \_ 版本**</span><span class="sxs-lookup"><span data-stu-id="d5649-125"><span id="PIX_E_INVALID_VERSION"></span><span id="pix_e_invalid_version"></span>**PIX\_E\_INVALID\_VERSION**</span></span>  
<span data-ttu-id="d5649-126">自訂 HRESULT，表示正在使用不正確版本。</span><span class="sxs-lookup"><span data-stu-id="d5649-126">A custom HRESULT which indicates that an invalid version is being used.</span></span>

<span data-ttu-id="d5649-127"><span id="PIX_E_USING_DCOMP"></span><span id="pix_e_using_dcomp"></span>**\_ \_ 使用 \_ DCOMP 的 PIX E**</span><span class="sxs-lookup"><span data-stu-id="d5649-127"><span id="PIX_E_USING_DCOMP"></span><span id="pix_e_using_dcomp"></span>**PIX\_E\_USING\_DCOMP**</span></span>  
<span data-ttu-id="d5649-128">自訂 HRESULT，指出 DirectComposition 正在使用中 (不支援 DirectComposition 的捕獲。 ) </span><span class="sxs-lookup"><span data-stu-id="d5649-128">A custom HRESULT which indicates that DirectComposition is in use (capture of DirectComposition is not supported.)</span></span>

<span data-ttu-id="d5649-129"><span id="PIX_E_USING_DIRECTWRITE"></span><span id="pix_e_using_directwrite"></span>**\_ \_ 使用 \_ DIRECTWRITE 的 PIX E**</span><span class="sxs-lookup"><span data-stu-id="d5649-129"><span id="PIX_E_USING_DIRECTWRITE"></span><span id="pix_e_using_directwrite"></span>**PIX\_E\_USING\_DIRECTWRITE**</span></span>  
<span data-ttu-id="d5649-130">自訂 HRESULT，指出 DirectWrite 正在使用中 (不支援 DirectWrite 的捕獲。 ) </span><span class="sxs-lookup"><span data-stu-id="d5649-130">A custom HRESULT which indicates that DirectWrite is in use (capture of DirectWrite is not supported.)</span></span>

<span data-ttu-id="d5649-131"><span id="PIX_E_USING_D3D9"></span><span id="pix_e_using_d3d9"></span>**\_ \_ 使用 \_ D3D9 的 PIX E**</span><span class="sxs-lookup"><span data-stu-id="d5649-131"><span id="PIX_E_USING_D3D9"></span><span id="pix_e_using_d3d9"></span>**PIX\_E\_USING\_D3D9**</span></span>  
<span data-ttu-id="d5649-132">自訂 HRESULT，表示 Windows 10 不支援 Direct3D9 在使用中 (捕捉 Direct3D9。 ) </span><span class="sxs-lookup"><span data-stu-id="d5649-132">A custom HRESULT which indicates that Direct3D9 is in use (capture of Direct3D9 is not supported in Windows 10.)</span></span>

<span data-ttu-id="d5649-133"><span id="PIX_E_CANT_CREATE_SHADER"></span><span id="pix_e_cant_create_shader"></span>**PIX \_ E \_ 無法 \_ 建立 \_ 著色器**</span><span class="sxs-lookup"><span data-stu-id="d5649-133"><span id="PIX_E_CANT_CREATE_SHADER"></span><span id="pix_e_cant_create_shader"></span>**PIX\_E\_CANT\_CREATE\_SHADER**</span></span>  
<span data-ttu-id="d5649-134">自訂 HRESULT，表示無法建立指定的著色器。</span><span class="sxs-lookup"><span data-stu-id="d5649-134">A custom HRESULT which indicates that a specified shader can't be created.</span></span>

<span data-ttu-id="d5649-135"><span id="PIX_E_USING_D2D"></span><span id="pix_e_using_d2d"></span>**\_ \_ 使用 \_ D2D 的 PIX E**</span><span class="sxs-lookup"><span data-stu-id="d5649-135"><span id="PIX_E_USING_D2D"></span><span id="pix_e_using_d2d"></span>**PIX\_E\_USING\_D2D**</span></span>  
<span data-ttu-id="d5649-136">自訂 HRESULT，指出 Direct2D 正在使用中 (不支援 Direct2D 的捕獲。 ) </span><span class="sxs-lookup"><span data-stu-id="d5649-136">A custom HRESULT which indicates that Direct2D is in use (capture of Direct2D is not supported.)</span></span>

<span data-ttu-id="d5649-137"><span id="PIX_E_NO_FRAMES"></span><span id="pix_e_no_frames"></span>**PIX \_ E \_ 沒有 \_ 框架**</span><span class="sxs-lookup"><span data-stu-id="d5649-137"><span id="PIX_E_NO_FRAMES"></span><span id="pix_e_no_frames"></span>**PIX\_E\_NO\_FRAMES**</span></span>  
<span data-ttu-id="d5649-138">自訂 HRESULT，指出未捕獲任何框架。</span><span class="sxs-lookup"><span data-stu-id="d5649-138">A custom HRESULT which indicates that no frames have been captured.</span></span>

<span data-ttu-id="d5649-139"><span id="PIX_E_DISABLE_SPY"></span><span id="pix_e_disable_spy"></span>**PIX \_ E \_ 停用 \_ SPY**</span><span class="sxs-lookup"><span data-stu-id="d5649-139"><span id="PIX_E_DISABLE_SPY"></span><span id="pix_e_disable_spy"></span>**PIX\_E\_DISABLE\_SPY**</span></span>  

<span data-ttu-id="d5649-140"><span id="PIX_E_WIN8LOG_ON_WIN7"></span><span id="pix_e_win8log_on_win7"></span>**\_ \_ \_ WIN7 上的 PIX E WIN8LOG \_**</span><span class="sxs-lookup"><span data-stu-id="d5649-140"><span id="PIX_E_WIN8LOG_ON_WIN7"></span><span id="pix_e_win8log_on_win7"></span>**PIX\_E\_WIN8LOG\_ON\_WIN7**</span></span>  
<span data-ttu-id="d5649-141">自訂 HRESULT，表示無法在 Windows 7 上播放 Windows 8 vsglog。</span><span class="sxs-lookup"><span data-stu-id="d5649-141">A custom HRESULT which indicates that a Windows 8 vsglog cannot be played back on Windows 7.</span></span>

<span data-ttu-id="d5649-142"><span id="PIX_E_BUILD_SHADER_TRACE"></span><span id="pix_e_build_shader_trace"></span>**PIX \_ E \_ 組建 \_ 著色器 \_ 追蹤**</span><span class="sxs-lookup"><span data-stu-id="d5649-142"><span id="PIX_E_BUILD_SHADER_TRACE"></span><span id="pix_e_build_shader_trace"></span>**PIX\_E\_BUILD\_SHADER\_TRACE**</span></span>  
<span data-ttu-id="d5649-143">自訂 HRESULT，表示建立著色器追蹤時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="d5649-143">A custom HRESULT which indicates that there was an error building the shader trace.</span></span>

<span data-ttu-id="d5649-144"><span id="PIX_E_NO_CS_DATA_VISUALIZATION"></span><span id="pix_e_no_cs_data_visualization"></span>**PIX \_ E \_ NO \_ CS \_ 資料 \_ 視覺效果**</span><span class="sxs-lookup"><span data-stu-id="d5649-144"><span id="PIX_E_NO_CS_DATA_VISUALIZATION"></span><span id="pix_e_no_cs_data_visualization"></span>**PIX\_E\_NO\_CS\_DATA\_VISUALIZATION**</span></span>  
<span data-ttu-id="d5649-145">自訂 HRESULT，指出沒有計算著色器資料視覺效果。</span><span class="sxs-lookup"><span data-stu-id="d5649-145">A custom HRESULT which indicates that there is no compute shader data visualization.</span></span>

<span data-ttu-id="d5649-146"><span id="PIX_E_MISMATCH_SDK"></span><span id="pix_e_mismatch_sdk"></span>**PIX \_ E \_ 不相符 \_ SDK**</span><span class="sxs-lookup"><span data-stu-id="d5649-146"><span id="PIX_E_MISMATCH_SDK"></span><span id="pix_e_mismatch_sdk"></span>**PIX\_E\_MISMATCH\_SDK**</span></span>  
<span data-ttu-id="d5649-147">自訂 HRESULT，表示與目前的 SDK 不符。</span><span class="sxs-lookup"><span data-stu-id="d5649-147">A custom HRESULT which indicates that there is a mismatch with the current SDK.</span></span>

<span data-ttu-id="d5649-148"><span id="PIX_E_POSSIBLE_MISMATCH_SDK"></span><span id="pix_e_possible_mismatch_sdk"></span>**PIX \_ E \_ 可能 \_ 不相符的 \_ SDK**</span><span class="sxs-lookup"><span data-stu-id="d5649-148"><span id="PIX_E_POSSIBLE_MISMATCH_SDK"></span><span id="pix_e_possible_mismatch_sdk"></span>**PIX\_E\_POSSIBLE\_MISMATCH\_SDK**</span></span>  
<span data-ttu-id="d5649-149">自訂 HRESULT，指出目前的 SDK 可能不相符。</span><span class="sxs-lookup"><span data-stu-id="d5649-149">A custom HRESULT which indicates that there is a possible mismatch with the current SDK.</span></span>

<span data-ttu-id="d5649-150"><span id="PIX_E_UNDETECTABLE_PIXEL"></span><span id="pix_e_undetectable_pixel"></span>**PIX \_ E 無法偵測 \_ \_ 圖元**</span><span class="sxs-lookup"><span data-stu-id="d5649-150"><span id="PIX_E_UNDETECTABLE_PIXEL"></span><span id="pix_e_undetectable_pixel"></span>**PIX\_E\_UNDETECTABLE\_PIXEL**</span></span>  
<span data-ttu-id="d5649-151">自訂 HRESULT，表示有無法偵測的圖元。</span><span class="sxs-lookup"><span data-stu-id="d5649-151">A custom HRESULT which indicates that there is an undetectable pixel.</span></span>

<span data-ttu-id="d5649-152"><span id="PIX_E_CANT_DEBUG_SHADER_USING_SYSTEM_VALUE_SEMANTICS"></span><span id="pix_e_cant_debug_shader_using_system_value_semantics"></span>**PIX \_ E \_ 無法 \_ \_ \_ 使用 \_ 系統 \_ 值 \_ 語義來對著色器進行 DEBUG 錯**</span><span class="sxs-lookup"><span data-stu-id="d5649-152"><span id="PIX_E_CANT_DEBUG_SHADER_USING_SYSTEM_VALUE_SEMANTICS"></span><span id="pix_e_cant_debug_shader_using_system_value_semantics"></span>**PIX\_E\_CANT\_DEBUG\_SHADER\_USING\_SYSTEM\_VALUE\_SEMANTICS**</span></span>  
<span data-ttu-id="d5649-153">自訂 HRESULT，表示無法使用系統值語義來調試 sahder。</span><span class="sxs-lookup"><span data-stu-id="d5649-153">A custom HRESULT which indicates that the sahder can't be debugged using system value semantics.</span></span>

<span data-ttu-id="d5649-154"><span id="PIX_S_UPDATEAVAILABLE"></span><span id="pix_s_updateavailable"></span>**PIX \_ S \_ UPDATEAVAILABLE**</span><span class="sxs-lookup"><span data-stu-id="d5649-154"><span id="PIX_S_UPDATEAVAILABLE"></span><span id="pix_s_updateavailable"></span>**PIX\_S\_UPDATEAVAILABLE**</span></span>  
<span data-ttu-id="d5649-155">自訂 HRESULT，指出有可用的更新。</span><span class="sxs-lookup"><span data-stu-id="d5649-155">A custom HRESULT which indicates that there is an update available.</span></span>

<span data-ttu-id="d5649-156"><span id="PIX_DXGI_STATUS_NO_REDIRECTION"></span><span id="pix_dxgi_status_no_redirection"></span>**PIX \_ DXGI \_ 狀態 \_ 無 \_ 重新導向**</span><span class="sxs-lookup"><span data-stu-id="d5649-156"><span id="PIX_DXGI_STATUS_NO_REDIRECTION"></span><span id="pix_dxgi_status_no_redirection"></span>**PIX\_DXGI\_STATUS\_NO\_REDIRECTION**</span></span>  
<span data-ttu-id="d5649-157">將 DXGI 狀態不會重新導向的自訂 HRESULT \_ \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="d5649-157">A custom HRESULT that echos DXGI\_STATUS\_NO\_REDIRECTION.</span></span>

<span data-ttu-id="d5649-158"><span id="PIX_DXGI_STATUS_NO_DESKTOP_ACCESS"></span><span id="pix_dxgi_status_no_desktop_access"></span>**PIX \_ DXGI \_ 狀態 \_ 沒有 \_ 桌面 \_ 存取**</span><span class="sxs-lookup"><span data-stu-id="d5649-158"><span id="PIX_DXGI_STATUS_NO_DESKTOP_ACCESS"></span><span id="pix_dxgi_status_no_desktop_access"></span>**PIX\_DXGI\_STATUS\_NO\_DESKTOP\_ACCESS**</span></span>  
<span data-ttu-id="d5649-159">將 DXGI \_ 狀態 \_ 無 \_ 桌面存取的自訂 HRESULT \_ 。</span><span class="sxs-lookup"><span data-stu-id="d5649-159">A custom HRESULT that echos DXGI\_STATUS\_NO\_DESKTOP\_ACCESS.</span></span>

<span data-ttu-id="d5649-160"><span id="PIX_DXGI_STATUS_GRAPHICS_VIDPN_SOURCE_IN_USE"></span><span id="pix_dxgi_status_graphics_vidpn_source_in_use"></span>**\_ \_ \_ \_ \_ \_ 使用中的 PIX DXGI 狀態圖形 VIDPN 來源 \_**</span><span class="sxs-lookup"><span data-stu-id="d5649-160"><span id="PIX_DXGI_STATUS_GRAPHICS_VIDPN_SOURCE_IN_USE"></span><span id="pix_dxgi_status_graphics_vidpn_source_in_use"></span>**PIX\_DXGI\_STATUS\_GRAPHICS\_VIDPN\_SOURCE\_IN\_USE**</span></span>  
<span data-ttu-id="d5649-161">使用將 DXGI \_ 狀態 \_ 圖形 \_ VIDPN \_ 來源的 \_ 自訂 HRESULT \_ 。</span><span class="sxs-lookup"><span data-stu-id="d5649-161">A custom HRESULT that echos DXGI\_STATUS\_GRAPHICS\_VIDPN\_SOURCE\_IN\_USE.</span></span>

<span data-ttu-id="d5649-162"><span id="PIX_DXGI_STATUS_MODE_CHANGED"></span><span id="pix_dxgi_status_mode_changed"></span>**PIX \_ DXGI \_ 狀態 \_ 模式 \_ 已變更**</span><span class="sxs-lookup"><span data-stu-id="d5649-162"><span id="PIX_DXGI_STATUS_MODE_CHANGED"></span><span id="pix_dxgi_status_mode_changed"></span>**PIX\_DXGI\_STATUS\_MODE\_CHANGED**</span></span>  
<span data-ttu-id="d5649-163">將 DXGI \_ 狀態 \_ 模式已變更的自訂 HRESULT \_ 。</span><span class="sxs-lookup"><span data-stu-id="d5649-163">A custom HRESULT that echos DXGI\_STATUS\_MODE\_CHANGED.</span></span>

<span data-ttu-id="d5649-164"><span id="PIX_DXGI_STATUS_MODE_CHANGE_IN_PROGRESS"></span><span id="pix_dxgi_status_mode_change_in_progress"></span>**PIX \_ DXGI \_ 狀態 \_ 模式 \_ 變更 \_ \_ 進行中**</span><span class="sxs-lookup"><span data-stu-id="d5649-164"><span id="PIX_DXGI_STATUS_MODE_CHANGE_IN_PROGRESS"></span><span id="pix_dxgi_status_mode_change_in_progress"></span>**PIX\_DXGI\_STATUS\_MODE\_CHANGE\_IN\_PROGRESS**</span></span>  
<span data-ttu-id="d5649-165">將 DXGI \_ 狀態 \_ 模式 \_ 變更 \_ \_ 進行中的自訂 HRESULT。</span><span class="sxs-lookup"><span data-stu-id="d5649-165">A custom HRESULT that echos DXGI\_STATUS\_MODE\_CHANGE\_IN\_PROGRESS.</span></span>

<span data-ttu-id="d5649-166"><span id="PIX_DXGI_STATUS_UNOCCLUDED"></span><span id="pix_dxgi_status_unoccluded"></span>**PIX \_ DXGI \_ 狀態 \_ UNOCCLUDED**</span><span class="sxs-lookup"><span data-stu-id="d5649-166"><span id="PIX_DXGI_STATUS_UNOCCLUDED"></span><span id="pix_dxgi_status_unoccluded"></span>**PIX\_DXGI\_STATUS\_UNOCCLUDED**</span></span>  
<span data-ttu-id="d5649-167">將 DXGI 狀態 UNOCCLUDED 的自訂 HRESULT \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="d5649-167">A custom HRESULT that echos DXGI\_STATUS\_UNOCCLUDED.</span></span>

<span data-ttu-id="d5649-168"><span id="PIX_DXGI_STATUS_DDA_WAS_STILL_DRAWING"></span><span id="pix_dxgi_status_dda_was_still_drawing"></span>**PIX \_ DXGI \_ 狀態 \_ DDA \_ \_ 仍在 \_ 繪圖中**</span><span class="sxs-lookup"><span data-stu-id="d5649-168"><span id="PIX_DXGI_STATUS_DDA_WAS_STILL_DRAWING"></span><span id="pix_dxgi_status_dda_was_still_drawing"></span>**PIX\_DXGI\_STATUS\_DDA\_WAS\_STILL\_DRAWING**</span></span>  
<span data-ttu-id="d5649-169">將 DXGI 狀態 DDA 的自訂 HRESULT \_ \_ 仍在 \_ \_ \_ 繪圖中。</span><span class="sxs-lookup"><span data-stu-id="d5649-169">A custom HRESULT that echos DXGI\_STATUS\_DDA\_WAS\_STILL\_DRAWING.</span></span>

<span data-ttu-id="d5649-170"><span id="PIX_E_NOTIMPL"></span><span id="pix_e_notimpl"></span>**PIX \_ E \_ >NOTIMPL**</span><span class="sxs-lookup"><span data-stu-id="d5649-170"><span id="PIX_E_NOTIMPL"></span><span id="pix_e_notimpl"></span>**PIX\_E\_NOTIMPL**</span></span>  
<span data-ttu-id="d5649-171">將 E >notimpl 的自訂 HRESULT \_ 。</span><span class="sxs-lookup"><span data-stu-id="d5649-171">A custom HRESULT that echos E\_NOTIMPL.</span></span>

<span data-ttu-id="d5649-172"><span id="PIX_E_NOINTERFACE"></span><span id="pix_e_nointerface"></span>**PIX \_ E \_ NOINTERFACE**</span><span class="sxs-lookup"><span data-stu-id="d5649-172"><span id="PIX_E_NOINTERFACE"></span><span id="pix_e_nointerface"></span>**PIX\_E\_NOINTERFACE**</span></span>  
<span data-ttu-id="d5649-173">將 E NOINTERFACE 的自訂 HRESULT \_ 。</span><span class="sxs-lookup"><span data-stu-id="d5649-173">A custom HRESULT that echos E\_NOINTERFACE.</span></span>

<span data-ttu-id="d5649-174"><span id="PIX_E_POINTER"></span><span id="pix_e_pointer"></span>**PIX \_ E \_ 指標**</span><span class="sxs-lookup"><span data-stu-id="d5649-174"><span id="PIX_E_POINTER"></span><span id="pix_e_pointer"></span>**PIX\_E\_POINTER**</span></span>  
<span data-ttu-id="d5649-175">將 E 指標的自訂 HRESULT \_ 。</span><span class="sxs-lookup"><span data-stu-id="d5649-175">A custom HRESULT that echos E\_POINTER.</span></span>

<span data-ttu-id="d5649-176"><span id="PIX_E_ABORT"></span><span id="pix_e_abort"></span>**PIX \_ E \_ 中止**</span><span class="sxs-lookup"><span data-stu-id="d5649-176"><span id="PIX_E_ABORT"></span><span id="pix_e_abort"></span>**PIX\_E\_ABORT**</span></span>  
<span data-ttu-id="d5649-177">將 E 中止的自訂 HRESULT \_ 。</span><span class="sxs-lookup"><span data-stu-id="d5649-177">A custom HRESULT that echos E\_ABORT.</span></span>

<span data-ttu-id="d5649-178"><span id="PIX_E_FAIL"></span><span id="pix_e_fail"></span>**PIX \_ E \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="d5649-178"><span id="PIX_E_FAIL"></span><span id="pix_e_fail"></span>**PIX\_E\_FAIL**</span></span>  
<span data-ttu-id="d5649-179">將 E 失敗的自訂 HRESULT \_ 。</span><span class="sxs-lookup"><span data-stu-id="d5649-179">A custom HRESULT that echos E\_FAIL.</span></span>

<span data-ttu-id="d5649-180"><span id="PIX_E_UNEXPECTED"></span><span id="pix_e_unexpected"></span>**PIX \_ E 未 \_ 預期**</span><span class="sxs-lookup"><span data-stu-id="d5649-180"><span id="PIX_E_UNEXPECTED"></span><span id="pix_e_unexpected"></span>**PIX\_E\_UNEXPECTED**</span></span>  
<span data-ttu-id="d5649-181">將 E 非預期的自訂 HRESULT \_ 。</span><span class="sxs-lookup"><span data-stu-id="d5649-181">A custom HRESULT that echos E\_UNEXPECTED.</span></span>

<span data-ttu-id="d5649-182"><span id="PIX_E_ACCESSDENIED"></span><span id="pix_e_accessdenied"></span>**PIX \_ E \_ ACCESSDENIED**</span><span class="sxs-lookup"><span data-stu-id="d5649-182"><span id="PIX_E_ACCESSDENIED"></span><span id="pix_e_accessdenied"></span>**PIX\_E\_ACCESSDENIED**</span></span>  
<span data-ttu-id="d5649-183">將 E ACCESSDENIED 的自訂 HRESULT \_ 。</span><span class="sxs-lookup"><span data-stu-id="d5649-183">A custom HRESULT that echos E\_ACCESSDENIED.</span></span>

<span data-ttu-id="d5649-184"><span id="PIX_E_HANDLE"></span><span id="pix_e_handle"></span>**PIX \_ E \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="d5649-184"><span id="PIX_E_HANDLE"></span><span id="pix_e_handle"></span>**PIX\_E\_HANDLE**</span></span>  
<span data-ttu-id="d5649-185">將 E 控制碼的自訂 HRESULT \_ 。</span><span class="sxs-lookup"><span data-stu-id="d5649-185">A custom HRESULT that echos E\_HANDLE.</span></span>

<span data-ttu-id="d5649-186"><span id="PIX_E_OUTOFMEMORY"></span><span id="pix_e_outofmemory"></span>**PIX \_ E \_ OUTOFMEMORY**</span><span class="sxs-lookup"><span data-stu-id="d5649-186"><span id="PIX_E_OUTOFMEMORY"></span><span id="pix_e_outofmemory"></span>**PIX\_E\_OUTOFMEMORY**</span></span>  
<span data-ttu-id="d5649-187">將 E OUTOFMEMORY 的自訂 HRESULT \_ 。</span><span class="sxs-lookup"><span data-stu-id="d5649-187">A custom HRESULT that echos E\_OUTOFMEMORY.</span></span>

<span data-ttu-id="d5649-188"><span id="PIX_E_INVALIDARG"></span><span id="pix_e_invalidarg"></span>**PIX \_ E \_ INVALIDARG**</span><span class="sxs-lookup"><span data-stu-id="d5649-188"><span id="PIX_E_INVALIDARG"></span><span id="pix_e_invalidarg"></span>**PIX\_E\_INVALIDARG**</span></span>  
<span data-ttu-id="d5649-189">將 E INVALIDARG 的自訂 HRESULT \_ 。</span><span class="sxs-lookup"><span data-stu-id="d5649-189">A custom HRESULT that echos E\_INVALIDARG.</span></span>

<span data-ttu-id="d5649-190"><span id="PIX_XBOX_ERROR_DISK_FULL"></span><span id="pix_xbox_error_disk_full"></span>**PIX \_ XBOX \_ ERROR \_ 磁片已 \_ 滿**</span><span class="sxs-lookup"><span data-stu-id="d5649-190"><span id="PIX_XBOX_ERROR_DISK_FULL"></span><span id="pix_xbox_error_disk_full"></span>**PIX\_XBOX\_ERROR\_DISK\_FULL**</span></span>  
<span data-ttu-id="d5649-191">指出磁片已滿的自訂 HRESULT。</span><span class="sxs-lookup"><span data-stu-id="d5649-191">A custom HRESULT which indicates that the disk is full.</span></span>

<span data-ttu-id="d5649-192"><span id="PIX_WS_E_ADDRESS_IN_USE"></span><span id="pix_ws_e_address_in_use"></span>**\_ \_ \_ \_ 使用中的 PIX WS E 位址 \_**</span><span class="sxs-lookup"><span data-stu-id="d5649-192"><span id="PIX_WS_E_ADDRESS_IN_USE"></span><span id="pix_ws_e_address_in_use"></span>**PIX\_WS\_E\_ADDRESS\_IN\_USE**</span></span>  
<span data-ttu-id="d5649-193">自訂 HRESULT，表示位址已在使用中。</span><span class="sxs-lookup"><span data-stu-id="d5649-193">A custom HRESULT which indicates that the address is already in use.</span></span>

<span data-ttu-id="d5649-194"><span id="PIX_WS_E_MISSING_KITS_POLICY"></span><span id="pix_ws_e_missing_kits_policy"></span>**PIX \_ WS \_ E \_ 遺失 \_ 套件 \_ 原則**</span><span class="sxs-lookup"><span data-stu-id="d5649-194"><span id="PIX_WS_E_MISSING_KITS_POLICY"></span><span id="pix_ws_e_missing_kits_policy"></span>**PIX\_WS\_E\_MISSING\_KITS\_POLICY**</span></span>  
<span data-ttu-id="d5649-195">自訂 HRESULT，表示無法使用位址。</span><span class="sxs-lookup"><span data-stu-id="d5649-195">A custom HRESULT which indicates that the address is not available.</span></span>

<span data-ttu-id="d5649-196"><span id="PIX_TE_FAILEDTOLOADSOFTWAREMODULE"></span><span id="pix_te_failedtoloadsoftwaremodule"></span>**PIX \_ TE \_ FAILEDTOLOADSOFTWAREMODULE**</span><span class="sxs-lookup"><span data-stu-id="d5649-196"><span id="PIX_TE_FAILEDTOLOADSOFTWAREMODULE"></span><span id="pix_te_failedtoloadsoftwaremodule"></span>**PIX\_TE\_FAILEDTOLOADSOFTWAREMODULE**</span></span>  
<span data-ttu-id="d5649-197">自訂 HRESULT，表示無法載入必要的軟體模組。</span><span class="sxs-lookup"><span data-stu-id="d5649-197">A custom HRESULT which indicates that a necessary software module failed to load.</span></span>

<span data-ttu-id="d5649-198"><span id="PIX_TE_USEDSOFTWAREMODULETHATWASNTWARPORREF"></span><span id="pix_te_usedsoftwaremodulethatwasntwarporref"></span>**PIX \_ TE \_ USEDSOFTWAREMODULETHATWASNTWARPORREF**</span><span class="sxs-lookup"><span data-stu-id="d5649-198"><span id="PIX_TE_USEDSOFTWAREMODULETHATWASNTWARPORREF"></span><span id="pix_te_usedsoftwaremodulethatwasntwarporref"></span>**PIX\_TE\_USEDSOFTWAREMODULETHATWASNTWARPORREF**</span></span>  
<span data-ttu-id="d5649-199">自訂 HRESULT，表示所使用的軟體模組並非變形或 REF 驅動程式。</span><span class="sxs-lookup"><span data-stu-id="d5649-199">A custom HRESULT which indicates that the used software module was not the WARP or REF driver.</span></span>

<span data-ttu-id="d5649-200"><span id="PIX_TE_CORRUPTEDFILE"></span><span id="pix_te_corruptedfile"></span>**PIX \_ TE \_ CORRUPTEDFILE**</span><span class="sxs-lookup"><span data-stu-id="d5649-200"><span id="PIX_TE_CORRUPTEDFILE"></span><span id="pix_te_corruptedfile"></span>**PIX\_TE\_CORRUPTEDFILE**</span></span>  
<span data-ttu-id="d5649-201">自訂 HRESULT，表示檔案已損毀。</span><span class="sxs-lookup"><span data-stu-id="d5649-201">A custom HRESULT which indicates that the file is corrupted.</span></span>

<span data-ttu-id="d5649-202"><span id="PIX_TE_FAILEDTOOPENFILE"></span><span id="pix_te_failedtoopenfile"></span>**PIX \_ TE \_ FAILEDTOOPENFILE**</span><span class="sxs-lookup"><span data-stu-id="d5649-202"><span id="PIX_TE_FAILEDTOOPENFILE"></span><span id="pix_te_failedtoopenfile"></span>**PIX\_TE\_FAILEDTOOPENFILE**</span></span>  
<span data-ttu-id="d5649-203">自訂 HRESULT，表示檔案無法開啟。</span><span class="sxs-lookup"><span data-stu-id="d5649-203">A custom HRESULT which indicates that the file failed to open.</span></span>

<span data-ttu-id="d5649-204"><span id="PIX_TE_CALLFAILEDONPLAYBACK"></span><span id="pix_te_callfailedonplayback"></span>**PIX \_ TE \_ CALLFAILEDONPLAYBACK**</span><span class="sxs-lookup"><span data-stu-id="d5649-204"><span id="PIX_TE_CALLFAILEDONPLAYBACK"></span><span id="pix_te_callfailedonplayback"></span>**PIX\_TE\_CALLFAILEDONPLAYBACK**</span></span>  
<span data-ttu-id="d5649-205">自訂 HRESULT，表示播放期間的呼叫失敗。</span><span class="sxs-lookup"><span data-stu-id="d5649-205">A custom HRESULT which indicates that a call failed during playback.</span></span>

<span data-ttu-id="d5649-206"><span id="PIX_TE_UNKNOWNUUID"></span><span id="pix_te_unknownuuid"></span>**PIX \_ TE \_ UNKNOWNUUID**</span><span class="sxs-lookup"><span data-stu-id="d5649-206"><span id="PIX_TE_UNKNOWNUUID"></span><span id="pix_te_unknownuuid"></span>**PIX\_TE\_UNKNOWNUUID**</span></span>  
<span data-ttu-id="d5649-207">自訂 HRESULT，指出發生未知的 UUID;永遠不會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="d5649-207">A custom HRESULT which indicates that an unknown UUID was encountered; this should never occur.</span></span>

<span data-ttu-id="d5649-208"><span id="PIX_TE_NOTCAPTUREFILEORCORRUPTED"></span><span id="pix_te_notcapturefileorcorrupted"></span>**PIX \_ TE \_ NOTCAPTUREFILEORCORRUPTED**</span><span class="sxs-lookup"><span data-stu-id="d5649-208"><span id="PIX_TE_NOTCAPTUREFILEORCORRUPTED"></span><span id="pix_te_notcapturefileorcorrupted"></span>**PIX\_TE\_NOTCAPTUREFILEORCORRUPTED**</span></span>  
<span data-ttu-id="d5649-209">自訂 HRESULT，表示檔案不是捕獲檔案或已損毀。</span><span class="sxs-lookup"><span data-stu-id="d5649-209">A custom HRESULT which indicates that the file is not a capture file or is corrupted.</span></span>

<span data-ttu-id="d5649-210"><span id="PIX_TE_NEWERFILE"></span><span id="pix_te_newerfile"></span>**PIX \_ TE \_ NEWERFILE**</span><span class="sxs-lookup"><span data-stu-id="d5649-210"><span id="PIX_TE_NEWERFILE"></span><span id="pix_te_newerfile"></span>**PIX\_TE\_NEWERFILE**</span></span>  

<span data-ttu-id="d5649-211"><span id="PIX_TE_OLDERFILE"></span><span id="pix_te_olderfile"></span>**PIX \_ TE \_ OLDERFILE**</span><span class="sxs-lookup"><span data-stu-id="d5649-211"><span id="PIX_TE_OLDERFILE"></span><span id="pix_te_olderfile"></span>**PIX\_TE\_OLDERFILE**</span></span>  

<span data-ttu-id="d5649-212"><span id="PIX_TE_INVALIDMOMENT"></span><span id="pix_te_invalidmoment"></span>**PIX \_ TE \_ INVALIDMOMENT**</span><span class="sxs-lookup"><span data-stu-id="d5649-212"><span id="PIX_TE_INVALIDMOMENT"></span><span id="pix_te_invalidmoment"></span>**PIX\_TE\_INVALIDMOMENT**</span></span>  

<span data-ttu-id="d5649-213"><span id="PIX_TE_BAD_DRIVER"></span><span id="pix_te_bad_driver"></span>**PIX \_ TE \_ \_ 驅動程式錯誤**</span><span class="sxs-lookup"><span data-stu-id="d5649-213"><span id="PIX_TE_BAD_DRIVER"></span><span id="pix_te_bad_driver"></span>**PIX\_TE\_BAD\_DRIVER**</span></span>  
<span data-ttu-id="d5649-214">自訂 HRESULT，指出驅動程式不正確。</span><span class="sxs-lookup"><span data-stu-id="d5649-214">A custom HRESULT which indicates that the driver is bad.</span></span>

<span data-ttu-id="d5649-215"><span id="PIX_ERROR_CANT_ACCESS_DEPTHSTENCIL_IN_CPU"></span><span id="pix_error_cant_access_depthstencil_in_cpu"></span>**PIX \_ 錯誤 \_ 無法 \_ 存取 \_ \_ CPU 中的 DEPTHSTENCIL \_**</span><span class="sxs-lookup"><span data-stu-id="d5649-215"><span id="PIX_ERROR_CANT_ACCESS_DEPTHSTENCIL_IN_CPU"></span><span id="pix_error_cant_access_depthstencil_in_cpu"></span>**PIX\_ERROR\_CANT\_ACCESS\_DEPTHSTENCIL\_IN\_CPU**</span></span>  
<span data-ttu-id="d5649-216">自訂 HRESULT，表示 CPU 嘗試存取深度樣板緩衝區，而導致錯誤。</span><span class="sxs-lookup"><span data-stu-id="d5649-216">A custom HRESULT which indicates that the CPU attempted to access the depth-stencil buffer, resulting in an error.</span></span>

<span data-ttu-id="d5649-217"><span id="PIX_ERROR_CANT_RESOLVE_MULTISAMPLED_TEXTURE"></span><span id="pix_error_cant_resolve_multisampled_texture"></span>**PIX \_ 錯誤 \_ 無法 \_ 解析 \_ 多重取樣 \_ 材質**</span><span class="sxs-lookup"><span data-stu-id="d5649-217"><span id="PIX_ERROR_CANT_RESOLVE_MULTISAMPLED_TEXTURE"></span><span id="pix_error_cant_resolve_multisampled_texture"></span>**PIX\_ERROR\_CANT\_RESOLVE\_MULTISAMPLED\_TEXTURE**</span></span>  
<span data-ttu-id="d5649-218">自訂 HRESULT，表示嘗試解析多樣本材質，導致錯誤。</span><span class="sxs-lookup"><span data-stu-id="d5649-218">A custom HRESULT which indicates that there was an attempt to resolve a multi-sampled texture, resulting in an error.</span></span>

<span data-ttu-id="d5649-219"><span id="PIX_DXGI_ERROR_INVALID_CALL"></span><span id="pix_dxgi_error_invalid_call"></span>**PIX \_ DXGI \_ 錯誤 \_ 不正確 \_ 呼叫**</span><span class="sxs-lookup"><span data-stu-id="d5649-219"><span id="PIX_DXGI_ERROR_INVALID_CALL"></span><span id="pix_dxgi_error_invalid_call"></span>**PIX\_DXGI\_ERROR\_INVALID\_CALL**</span></span>  
<span data-ttu-id="d5649-220">將 DXGI \_ 錯誤無效呼叫的自訂 HRESULT \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="d5649-220">A custom HRESULT that echos DXGI\_ERROR\_INVALID\_CALL.</span></span>

<span data-ttu-id="d5649-221"><span id="PIX_DXGI_ERROR_NOT_FOUND"></span><span id="pix_dxgi_error_not_found"></span>**\_ \_ \_ \_ 找不到 PIX DXGI 錯誤**</span><span class="sxs-lookup"><span data-stu-id="d5649-221"><span id="PIX_DXGI_ERROR_NOT_FOUND"></span><span id="pix_dxgi_error_not_found"></span>**PIX\_DXGI\_ERROR\_NOT\_FOUND**</span></span>  
<span data-ttu-id="d5649-222">\_ \_ 找不到將 DXGI 錯誤的自訂 HRESULT \_ 。</span><span class="sxs-lookup"><span data-stu-id="d5649-222">A custom HRESULT that echos DXGI\_ERROR\_NOT\_FOUND.</span></span>

<span data-ttu-id="d5649-223"><span id="PIX_DXGI_ERROR_MORE_DATA"></span><span id="pix_dxgi_error_more_data"></span>**PIX \_ DXGI \_ 錯誤 \_ 更多 \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="d5649-223"><span id="PIX_DXGI_ERROR_MORE_DATA"></span><span id="pix_dxgi_error_more_data"></span>**PIX\_DXGI\_ERROR\_MORE\_DATA**</span></span>  
<span data-ttu-id="d5649-224">將 DXGI \_ 錯誤 \_ 更多資料的自訂 HRESULT \_ 。</span><span class="sxs-lookup"><span data-stu-id="d5649-224">A custom HRESULT that echos DXGI\_ERROR\_MORE\_DATA.</span></span>

<span data-ttu-id="d5649-225"><span id="PIX_DXGI_ERROR_UNSUPPORTED"></span><span id="pix_dxgi_error_unsupported"></span>**未 \_ 支援 PIX DXGI \_ 錯誤 \_**</span><span class="sxs-lookup"><span data-stu-id="d5649-225"><span id="PIX_DXGI_ERROR_UNSUPPORTED"></span><span id="pix_dxgi_error_unsupported"></span>**PIX\_DXGI\_ERROR\_UNSUPPORTED**</span></span>  
<span data-ttu-id="d5649-226">不支援將 DXGI 錯誤的自訂 HRESULT \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="d5649-226">A custom HRESULT that echos DXGI\_ERROR\_UNSUPPORTED.</span></span>

<span data-ttu-id="d5649-227"><span id="PIX_DXGI_ERROR_DEVICE_REMOVED"></span><span id="pix_dxgi_error_device_removed"></span>**\_已移除 PIX DXGI \_ 錯誤 \_ 裝置 \_**</span><span class="sxs-lookup"><span data-stu-id="d5649-227"><span id="PIX_DXGI_ERROR_DEVICE_REMOVED"></span><span id="pix_dxgi_error_device_removed"></span>**PIX\_DXGI\_ERROR\_DEVICE\_REMOVED**</span></span>  
<span data-ttu-id="d5649-228">已移除將 DXGI 錯誤裝置的自訂 HRESULT \_ \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="d5649-228">A custom HRESULT that echos DXGI\_ERROR\_DEVICE\_REMOVED.</span></span>

<span data-ttu-id="d5649-229"><span id="PIX_DXGI_ERROR_DEVICE_HUNG"></span><span id="pix_dxgi_error_device_hung"></span>**PIX \_ DXGI \_ 錯誤 \_ 裝置無 \_ 反應**</span><span class="sxs-lookup"><span data-stu-id="d5649-229"><span id="PIX_DXGI_ERROR_DEVICE_HUNG"></span><span id="pix_dxgi_error_device_hung"></span>**PIX\_DXGI\_ERROR\_DEVICE\_HUNG**</span></span>  
<span data-ttu-id="d5649-230">將 DXGI 錯誤裝置無反應的自訂 HRESULT \_ \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="d5649-230">A custom HRESULT that echos DXGI\_ERROR\_DEVICE\_HUNG.</span></span>

<span data-ttu-id="d5649-231"><span id="PIX_DXGI_ERROR_DEVICE_RESET"></span><span id="pix_dxgi_error_device_reset"></span>**PIX \_ DXGI \_ 錯誤 \_ 裝置 \_ 重設**</span><span class="sxs-lookup"><span data-stu-id="d5649-231"><span id="PIX_DXGI_ERROR_DEVICE_RESET"></span><span id="pix_dxgi_error_device_reset"></span>**PIX\_DXGI\_ERROR\_DEVICE\_RESET**</span></span>  
<span data-ttu-id="d5649-232">將 DXGI \_ 錯誤 \_ 裝置重設的自訂 HRESULT \_ 。</span><span class="sxs-lookup"><span data-stu-id="d5649-232">A custom HRESULT that echos DXGI\_ERROR\_DEVICE\_RESET.</span></span>

<span data-ttu-id="d5649-233"><span id="PIX_DXGI_ERROR_WAS_STILL_DRAWING"></span><span id="pix_dxgi_error_was_still_drawing"></span>**PIX \_ DXGI \_ 錯誤 \_ \_ 仍在 \_ 繪圖中**</span><span class="sxs-lookup"><span data-stu-id="d5649-233"><span id="PIX_DXGI_ERROR_WAS_STILL_DRAWING"></span><span id="pix_dxgi_error_was_still_drawing"></span>**PIX\_DXGI\_ERROR\_WAS\_STILL\_DRAWING**</span></span>  
<span data-ttu-id="d5649-234">將 DXGI 錯誤的自訂 \_ HRESULT \_ \_ 仍在 \_ 繪圖中。</span><span class="sxs-lookup"><span data-stu-id="d5649-234">A custom HRESULT that echos DXGI\_ERROR\_WAS\_STILL\_DRAWING.</span></span>

<span data-ttu-id="d5649-235"><span id="PIX_DXGI_ERROR_FRAME_STATISTICS_DISJOINT"></span><span id="pix_dxgi_error_frame_statistics_disjoint"></span>**PIX \_ DXGI \_ 錯誤 \_ 框架 \_ 統計資料不 \_ 相交**</span><span class="sxs-lookup"><span data-stu-id="d5649-235"><span id="PIX_DXGI_ERROR_FRAME_STATISTICS_DISJOINT"></span><span id="pix_dxgi_error_frame_statistics_disjoint"></span>**PIX\_DXGI\_ERROR\_FRAME\_STATISTICS\_DISJOINT**</span></span>  
<span data-ttu-id="d5649-236">將 DXGI \_ 錯誤 \_ 框架 \_ 統計資料的自訂 HRESULT \_ 。</span><span class="sxs-lookup"><span data-stu-id="d5649-236">A custom HRESULT that echos DXGI\_ERROR\_FRAME\_STATISTICS\_DISJOINT.</span></span>

<span data-ttu-id="d5649-237"><span id="PIX_DXGI_ERROR_GRAPHICS_VIDPN_SOURCE_IN_USE"></span><span id="pix_dxgi_error_graphics_vidpn_source_in_use"></span>**\_ \_ \_ \_ \_ \_ 使用中的 PIX DXGI 錯誤圖形 VIDPN 來源 \_**</span><span class="sxs-lookup"><span data-stu-id="d5649-237"><span id="PIX_DXGI_ERROR_GRAPHICS_VIDPN_SOURCE_IN_USE"></span><span id="pix_dxgi_error_graphics_vidpn_source_in_use"></span>**PIX\_DXGI\_ERROR\_GRAPHICS\_VIDPN\_SOURCE\_IN\_USE**</span></span>  
<span data-ttu-id="d5649-238">使用將 DXGI \_ 錯誤 \_ 圖形 \_ VIDPN \_ 來源的 \_ 自訂 HRESULT \_ 。</span><span class="sxs-lookup"><span data-stu-id="d5649-238">A custom HRESULT that echos DXGI\_ERROR\_GRAPHICS\_VIDPN\_SOURCE\_IN\_USE.</span></span>

<span data-ttu-id="d5649-239"><span id="PIX_DXGI_ERROR_DRIVER_INTERNAL_ERROR"></span><span id="pix_dxgi_error_driver_internal_error"></span>**PIX \_ DXGI \_ 錯誤 \_ 驅動程式 \_ 內部 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="d5649-239"><span id="PIX_DXGI_ERROR_DRIVER_INTERNAL_ERROR"></span><span id="pix_dxgi_error_driver_internal_error"></span>**PIX\_DXGI\_ERROR\_DRIVER\_INTERNAL\_ERROR**</span></span>  
<span data-ttu-id="d5649-240">將 DXGI \_ 錯誤 \_ 驅動程式 \_ 內部錯誤的自訂 HRESULT \_ 。</span><span class="sxs-lookup"><span data-stu-id="d5649-240">A custom HRESULT that echos DXGI\_ERROR\_DRIVER\_INTERNAL\_ERROR.</span></span>

<span data-ttu-id="d5649-241"><span id="PIX_DXGI_ERROR_NONEXCLUSIVE"></span><span id="pix_dxgi_error_nonexclusive"></span>**PIX \_ DXGI \_ 錯誤非 \_ 獨佔**</span><span class="sxs-lookup"><span data-stu-id="d5649-241"><span id="PIX_DXGI_ERROR_NONEXCLUSIVE"></span><span id="pix_dxgi_error_nonexclusive"></span>**PIX\_DXGI\_ERROR\_NONEXCLUSIVE**</span></span>  
<span data-ttu-id="d5649-242">將 DXGI 錯誤非獨佔的自訂 HRESULT \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="d5649-242">A custom HRESULT that echos DXGI\_ERROR\_NONEXCLUSIVE.</span></span>

<span data-ttu-id="d5649-243"><span id="PIX_DXGI_ERROR_NOT_CURRENTLY_AVAILABLE"></span><span id="pix_dxgi_error_not_currently_available"></span>**PIX \_ DXGI \_ 錯誤 \_ \_ 目前無法 \_ 使用**</span><span class="sxs-lookup"><span data-stu-id="d5649-243"><span id="PIX_DXGI_ERROR_NOT_CURRENTLY_AVAILABLE"></span><span id="pix_dxgi_error_not_currently_available"></span>**PIX\_DXGI\_ERROR\_NOT\_CURRENTLY\_AVAILABLE**</span></span>  
<span data-ttu-id="d5649-244">將 \_ \_ 目前無法使用的 DXGI 錯誤的自訂 HRESULT \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="d5649-244">A custom HRESULT that echos DXGI\_ERROR\_NOT\_CURRENTLY\_AVAILABLE.</span></span>

<span data-ttu-id="d5649-245"><span id="PIX_DXGI_ERROR_REMOTE_CLIENT_DISCONNECTED"></span><span id="pix_dxgi_error_remote_client_disconnected"></span>**PIX \_ DXGI \_ 錯誤 \_ 遠端 \_ 用戶端 \_ 中斷連線**</span><span class="sxs-lookup"><span data-stu-id="d5649-245"><span id="PIX_DXGI_ERROR_REMOTE_CLIENT_DISCONNECTED"></span><span id="pix_dxgi_error_remote_client_disconnected"></span>**PIX\_DXGI\_ERROR\_REMOTE\_CLIENT\_DISCONNECTED**</span></span>  
<span data-ttu-id="d5649-246">將 DXGI \_ 錯誤 \_ 遠端 \_ 用戶端中斷的自訂 HRESULT \_ 。</span><span class="sxs-lookup"><span data-stu-id="d5649-246">A custom HRESULT that echos DXGI\_ERROR\_REMOTE\_CLIENT\_DISCONNECTED.</span></span>

<span data-ttu-id="d5649-247"><span id="PIX_DXGI_ERROR_REMOTE_OUTOFMEMORY"></span><span id="pix_dxgi_error_remote_outofmemory"></span>**PIX \_ DXGI \_ 錯誤 \_ 遠端 \_ OUTOFMEMORY**</span><span class="sxs-lookup"><span data-stu-id="d5649-247"><span id="PIX_DXGI_ERROR_REMOTE_OUTOFMEMORY"></span><span id="pix_dxgi_error_remote_outofmemory"></span>**PIX\_DXGI\_ERROR\_REMOTE\_OUTOFMEMORY**</span></span>  
<span data-ttu-id="d5649-248">將 DXGI \_ ERROR REMOTE OUTOFMEMORY 的自訂 HRESULT \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="d5649-248">A custom HRESULT that echos DXGI\_ERROR\_REMOTE\_OUTOFMEMORY.</span></span>

<span data-ttu-id="d5649-249"><span id="PIX_DXGI_ERROR_MODE_CHANGE_IN_PROGRESS"></span><span id="pix_dxgi_error_mode_change_in_progress"></span>**PIX \_ DXGI \_ 錯誤 \_ 模式 \_ 變更 \_ \_ 進行中**</span><span class="sxs-lookup"><span data-stu-id="d5649-249"><span id="PIX_DXGI_ERROR_MODE_CHANGE_IN_PROGRESS"></span><span id="pix_dxgi_error_mode_change_in_progress"></span>**PIX\_DXGI\_ERROR\_MODE\_CHANGE\_IN\_PROGRESS**</span></span>  
<span data-ttu-id="d5649-250">將 DXGI \_ 錯誤 \_ 模式 \_ 變更 \_ \_ 進行中的自訂 HRESULT。</span><span class="sxs-lookup"><span data-stu-id="d5649-250">A custom HRESULT that echos DXGI\_ERROR\_MODE\_CHANGE\_IN\_PROGRESS.</span></span>

<span data-ttu-id="d5649-251"><span id="PIX_DXGI_ERROR_ACCESS_LOST"></span><span id="pix_dxgi_error_access_lost"></span>**PIX \_ DXGI \_ 錯誤 \_ 存取 \_ 遺失**</span><span class="sxs-lookup"><span data-stu-id="d5649-251"><span id="PIX_DXGI_ERROR_ACCESS_LOST"></span><span id="pix_dxgi_error_access_lost"></span>**PIX\_DXGI\_ERROR\_ACCESS\_LOST**</span></span>  
<span data-ttu-id="d5649-252">將 DXGI \_ 錯誤存取遺失的自訂 HRESULT \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="d5649-252">A custom HRESULT that echos DXGI\_ERROR\_ACCESS\_LOST.</span></span>

<span data-ttu-id="d5649-253"><span id="PIX_DXGI_ERROR_WAIT_TIMEOUT"></span><span id="pix_dxgi_error_wait_timeout"></span>**PIX \_ DXGI \_ 錯誤 \_ 等候 \_ 超時**</span><span class="sxs-lookup"><span data-stu-id="d5649-253"><span id="PIX_DXGI_ERROR_WAIT_TIMEOUT"></span><span id="pix_dxgi_error_wait_timeout"></span>**PIX\_DXGI\_ERROR\_WAIT\_TIMEOUT**</span></span>  
<span data-ttu-id="d5649-254">將 DXGI \_ 錯誤等候超時的自訂 HRESULT \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="d5649-254">A custom HRESULT that echos DXGI\_ERROR\_WAIT\_TIMEOUT.</span></span>

<span data-ttu-id="d5649-255"><span id="PIX_DXGI_ERROR_SESSION_DISCONNECTED"></span><span id="pix_dxgi_error_session_disconnected"></span>**PIX \_ DXGI \_ 錯誤 \_ 會話已 \_ 中斷連線**</span><span class="sxs-lookup"><span data-stu-id="d5649-255"><span id="PIX_DXGI_ERROR_SESSION_DISCONNECTED"></span><span id="pix_dxgi_error_session_disconnected"></span>**PIX\_DXGI\_ERROR\_SESSION\_DISCONNECTED**</span></span>  
<span data-ttu-id="d5649-256">將 DXGI 錯誤會話已中斷連線的自訂 HRESULT \_ \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="d5649-256">A custom HRESULT that echos DXGI\_ERROR\_SESSION\_DISCONNECTED.</span></span>

<span data-ttu-id="d5649-257"><span id="PIX_DXGI_ERROR_RESTRICT_TO_OUTPUT_STALE"></span><span id="pix_dxgi_error_restrict_to_output_stale"></span>**PIX \_ DXGI \_ 錯誤 \_ 限制 \_ 為 \_ 輸出 \_ 過時**</span><span class="sxs-lookup"><span data-stu-id="d5649-257"><span id="PIX_DXGI_ERROR_RESTRICT_TO_OUTPUT_STALE"></span><span id="pix_dxgi_error_restrict_to_output_stale"></span>**PIX\_DXGI\_ERROR\_RESTRICT\_TO\_OUTPUT\_STALE**</span></span>  
<span data-ttu-id="d5649-258">將 DXGI \_ 錯誤 \_ 限制 \_ 為 \_ 輸出 \_ 過時的自訂 HRESULT。</span><span class="sxs-lookup"><span data-stu-id="d5649-258">A custom HRESULT that echos DXGI\_ERROR\_RESTRICT\_TO\_OUTPUT\_STALE.</span></span>

<span data-ttu-id="d5649-259"><span id="PIX_DXGI_ERROR_CANNOT_PROTECT_CONTENT"></span><span id="pix_dxgi_error_cannot_protect_content"></span>**PIX \_ DXGI \_ 錯誤 \_ 無法 \_ 保護 \_ 內容**</span><span class="sxs-lookup"><span data-stu-id="d5649-259"><span id="PIX_DXGI_ERROR_CANNOT_PROTECT_CONTENT"></span><span id="pix_dxgi_error_cannot_protect_content"></span>**PIX\_DXGI\_ERROR\_CANNOT\_PROTECT\_CONTENT**</span></span>  
<span data-ttu-id="d5649-260">將 DXGI 錯誤的自訂 \_ HRESULT \_ 無法 \_ 保護 \_ 內容。</span><span class="sxs-lookup"><span data-stu-id="d5649-260">A custom HRESULT that echos DXGI\_ERROR\_CANNOT\_PROTECT\_CONTENT.</span></span>

<span data-ttu-id="d5649-261"><span id="PIX_DXGI_ERROR_ACCESS_DENIED"></span><span id="pix_dxgi_error_access_denied"></span>**PIX \_ DXGI \_ \_ 拒絕存取 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="d5649-261"><span id="PIX_DXGI_ERROR_ACCESS_DENIED"></span><span id="pix_dxgi_error_access_denied"></span>**PIX\_DXGI\_ERROR\_ACCESS\_DENIED**</span></span>  
<span data-ttu-id="d5649-262">將 DXGI 錯誤存取的自訂 HRESULT \_ \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="d5649-262">A custom HRESULT that echos DXGI\_ERROR\_ACCESS\_DENIED.</span></span>

<span data-ttu-id="d5649-263"><span id="PIX_DXGI_ERROR_NAME_ALREADY_EXISTS"></span><span id="pix_dxgi_error_name_already_exists"></span>**PIX \_ DXGI \_ 錯誤 \_ 名稱 \_ 已 \_ 存在**</span><span class="sxs-lookup"><span data-stu-id="d5649-263"><span id="PIX_DXGI_ERROR_NAME_ALREADY_EXISTS"></span><span id="pix_dxgi_error_name_already_exists"></span>**PIX\_DXGI\_ERROR\_NAME\_ALREADY\_EXISTS**</span></span>  
<span data-ttu-id="d5649-264">將 DXGI 錯誤名稱的自訂 HRESULT \_ \_ \_ 已經 \_ 存在。</span><span class="sxs-lookup"><span data-stu-id="d5649-264">A custom HRESULT that echos DXGI\_ERROR\_NAME\_ALREADY\_EXISTS.</span></span>

<span data-ttu-id="d5649-265"><span id="PIX_DXGI_ERROR_SDK_COMPONENT_MISSING"></span><span id="pix_dxgi_error_sdk_component_missing"></span>**PIX \_ DXGI \_ 錯誤 \_ SDK \_ 元件 \_ 遺失**</span><span class="sxs-lookup"><span data-stu-id="d5649-265"><span id="PIX_DXGI_ERROR_SDK_COMPONENT_MISSING"></span><span id="pix_dxgi_error_sdk_component_missing"></span>**PIX\_DXGI\_ERROR\_SDK\_COMPONENT\_MISSING**</span></span>  
<span data-ttu-id="d5649-266">缺少將 DXGI \_ 錯誤 SDK 元件的自訂 HRESULT \_ \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="d5649-266">A custom HRESULT that echos DXGI\_ERROR\_SDK\_COMPONENT\_MISSING.</span></span>

<span data-ttu-id="d5649-267"><span id="PIX_DXGI_DDI_ERR_WASSTILLDRAWING"></span><span id="pix_dxgi_ddi_err_wasstilldrawing"></span>**PIX \_ DXGI \_ DDI \_ ERR \_ WASSTILLDRAWING**</span><span class="sxs-lookup"><span data-stu-id="d5649-267"><span id="PIX_DXGI_DDI_ERR_WASSTILLDRAWING"></span><span id="pix_dxgi_ddi_err_wasstilldrawing"></span>**PIX\_DXGI\_DDI\_ERR\_WASSTILLDRAWING**</span></span>  
<span data-ttu-id="d5649-268">將 DXGI \_ DDI ERR WASSTILLDRAWING 的自訂 HRESULT \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="d5649-268">A custom HRESULT that echos DXGI\_DDI\_ERR\_WASSTILLDRAWING.</span></span>

<span data-ttu-id="d5649-269"><span id="PIX_DXGI_DDI_ERR_UNSUPPORTED"></span><span id="pix_dxgi_ddi_err_unsupported"></span>**PIX \_ DXGI \_ DDI \_ 錯誤 \_ 不受支援**</span><span class="sxs-lookup"><span data-stu-id="d5649-269"><span id="PIX_DXGI_DDI_ERR_UNSUPPORTED"></span><span id="pix_dxgi_ddi_err_unsupported"></span>**PIX\_DXGI\_DDI\_ERR\_UNSUPPORTED**</span></span>  
<span data-ttu-id="d5649-270">將 DXGI DDI ERR 的自訂 HRESULT \_ \_ \_ 不受支援。</span><span class="sxs-lookup"><span data-stu-id="d5649-270">A custom HRESULT that echos DXGI\_DDI\_ERR\_UNSUPPORTED.</span></span>

<span data-ttu-id="d5649-271"><span id="PIX_DXGI_DDI_ERR_NONEXCLUSIVE"></span><span id="pix_dxgi_ddi_err_nonexclusive"></span>**PIX \_ DXGI \_ DDI \_ 錯誤非 \_ 獨佔**</span><span class="sxs-lookup"><span data-stu-id="d5649-271"><span id="PIX_DXGI_DDI_ERR_NONEXCLUSIVE"></span><span id="pix_dxgi_ddi_err_nonexclusive"></span>**PIX\_DXGI\_DDI\_ERR\_NONEXCLUSIVE**</span></span>  
<span data-ttu-id="d5649-272">將 DXGI DDI 錯誤非獨佔的自訂 HRESULT \_ \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="d5649-272">A custom HRESULT that echos DXGI\_DDI\_ERR\_NONEXCLUSIVE.</span></span>

<span data-ttu-id="d5649-273"><span id="PIX_D3D10_ERROR_TOO_MANY_UNIQUE_STATE_OBJECTS"></span><span id="pix_d3d10_error_too_many_unique_state_objects"></span>**PIX \_ D3D10 \_ 錯誤 \_ 太 \_ 多 \_ 唯一的 \_ 狀態 \_ 物件**</span><span class="sxs-lookup"><span data-stu-id="d5649-273"><span id="PIX_D3D10_ERROR_TOO_MANY_UNIQUE_STATE_OBJECTS"></span><span id="pix_d3d10_error_too_many_unique_state_objects"></span>**PIX\_D3D10\_ERROR\_TOO\_MANY\_UNIQUE\_STATE\_OBJECTS**</span></span>  
<span data-ttu-id="d5649-274">將 D3D10 \_ 錯誤 \_ 太 \_ 多 \_ 唯一 \_ 狀態 \_ 物件的自訂 HRESULT。</span><span class="sxs-lookup"><span data-stu-id="d5649-274">A custom HRESULT that echos D3D10\_ERROR\_TOO\_MANY\_UNIQUE\_STATE\_OBJECTS.</span></span>

<span data-ttu-id="d5649-275"><span id="PIX_D3D10_ERROR_FILE_NOT_FOUND"></span><span id="pix_d3d10_error_file_not_found"></span>**\_ \_ \_ \_ \_ 找不到 PIX D3D10 錯誤檔案**</span><span class="sxs-lookup"><span data-stu-id="d5649-275"><span id="PIX_D3D10_ERROR_FILE_NOT_FOUND"></span><span id="pix_d3d10_error_file_not_found"></span>**PIX\_D3D10\_ERROR\_FILE\_NOT\_FOUND**</span></span>  
<span data-ttu-id="d5649-276">\_ \_ \_ 找不到將 D3D10 錯誤檔案的自訂 HRESULT \_ 。</span><span class="sxs-lookup"><span data-stu-id="d5649-276">A custom HRESULT that echos D3D10\_ERROR\_FILE\_NOT\_FOUND.</span></span>

<span data-ttu-id="d5649-277"><span id="PIX_D3D11_ERROR_TOO_MANY_UNIQUE_STATE_OBJECTS"></span><span id="pix_d3d11_error_too_many_unique_state_objects"></span>**PIX \_ D3D11 \_ 錯誤 \_ 太 \_ 多 \_ 唯一的 \_ 狀態 \_ 物件**</span><span class="sxs-lookup"><span data-stu-id="d5649-277"><span id="PIX_D3D11_ERROR_TOO_MANY_UNIQUE_STATE_OBJECTS"></span><span id="pix_d3d11_error_too_many_unique_state_objects"></span>**PIX\_D3D11\_ERROR\_TOO\_MANY\_UNIQUE\_STATE\_OBJECTS**</span></span>  
<span data-ttu-id="d5649-278">將 D3D11 \_ 錯誤 \_ 太 \_ 多 \_ 唯一 \_ 狀態 \_ 物件的自訂 HRESULT。</span><span class="sxs-lookup"><span data-stu-id="d5649-278">A custom HRESULT that echos D3D11\_ERROR\_TOO\_MANY\_UNIQUE\_STATE\_OBJECTS.</span></span>

<span data-ttu-id="d5649-279"><span id="PIX_D3D11_ERROR_FILE_NOT_FOUND"></span><span id="pix_d3d11_error_file_not_found"></span>**\_ \_ \_ \_ \_ 找不到 PIX D3D11 錯誤檔案**</span><span class="sxs-lookup"><span data-stu-id="d5649-279"><span id="PIX_D3D11_ERROR_FILE_NOT_FOUND"></span><span id="pix_d3d11_error_file_not_found"></span>**PIX\_D3D11\_ERROR\_FILE\_NOT\_FOUND**</span></span>  
<span data-ttu-id="d5649-280">\_ \_ \_ 找不到將 D3D11 錯誤檔案的自訂 HRESULT \_ 。</span><span class="sxs-lookup"><span data-stu-id="d5649-280">A custom HRESULT that echos D3D11\_ERROR\_FILE\_NOT\_FOUND.</span></span>

<span data-ttu-id="d5649-281"><span id="PIX_D3D11_ERROR_TOO_MANY_UNIQUE_VIEW_OBJECTS"></span><span id="pix_d3d11_error_too_many_unique_view_objects"></span>**PIX \_ D3D11 \_ 錯誤 \_ 太 \_ 多 \_ 唯一的 \_ VIEW \_ 物件**</span><span class="sxs-lookup"><span data-stu-id="d5649-281"><span id="PIX_D3D11_ERROR_TOO_MANY_UNIQUE_VIEW_OBJECTS"></span><span id="pix_d3d11_error_too_many_unique_view_objects"></span>**PIX\_D3D11\_ERROR\_TOO\_MANY\_UNIQUE\_VIEW\_OBJECTS**</span></span>  
<span data-ttu-id="d5649-282">將 D3D11 的自訂 HRESULT \_ 錯誤 \_ 太 \_ 多 \_ 唯一 \_ VIEW \_ 物件。</span><span class="sxs-lookup"><span data-stu-id="d5649-282">A custom HRESULT that echos D3D11\_ERROR\_TOO\_MANY\_UNIQUE\_VIEW\_OBJECTS.</span></span>

<span data-ttu-id="d5649-283"><span id="PIX_D3D11_ERROR_DEFERRED_CONTEXT_MAP_WITHOUT_INITIAL_DISCARD"></span><span id="pix_d3d11_error_deferred_context_map_without_initial_discard"></span>**PIX \_ D3D11 \_ 錯誤 \_ 延遲的 \_ 內容 \_ 對應， \_ 沒有 \_ 初始 \_ 捨棄**</span><span class="sxs-lookup"><span data-stu-id="d5649-283"><span id="PIX_D3D11_ERROR_DEFERRED_CONTEXT_MAP_WITHOUT_INITIAL_DISCARD"></span><span id="pix_d3d11_error_deferred_context_map_without_initial_discard"></span>**PIX\_D3D11\_ERROR\_DEFERRED\_CONTEXT\_MAP\_WITHOUT\_INITIAL\_DISCARD**</span></span>  
<span data-ttu-id="d5649-284">自訂 HRESULT 將 D3D11 \_ 錯誤 \_ 延遲的 \_ 內容 \_ 對應， \_ 不含 \_ 初始 \_ 捨棄。</span><span class="sxs-lookup"><span data-stu-id="d5649-284">A custom HRESULT that echos D3D11\_ERROR\_DEFERRED\_CONTEXT\_MAP\_WITHOUT\_INITIAL\_DISCARD.</span></span>

<span data-ttu-id="d5649-285"><span id="PIX_ERROR_OCCLUDED_DRAW_CALL"></span><span id="pix_error_occluded_draw_call"></span>**PIX \_ 錯誤 \_ PIXELS OCCLUDED \_ 繪製 \_ 呼叫**</span><span class="sxs-lookup"><span data-stu-id="d5649-285"><span id="PIX_ERROR_OCCLUDED_DRAW_CALL"></span><span id="pix_error_occluded_draw_call"></span>**PIX\_ERROR\_OCCLUDED\_DRAW\_CALL**</span></span>  
<span data-ttu-id="d5649-286">自訂 HRESULT，表示繪製呼叫已完全 pixels occluded，因而導致錯誤。</span><span class="sxs-lookup"><span data-stu-id="d5649-286">A custom HRESULT which indicates that a draw call was entirely occluded, resulting in an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5649-287">規格需求</span><span class="sxs-lookup"><span data-stu-id="d5649-287">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="d5649-288">標頭</span><span class="sxs-lookup"><span data-stu-id="d5649-288">Header</span></span></p></td><td><span data-ttu-id="d5649-289">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="d5649-289">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



