---
title: 影片捕獲參考
description: 影片捕獲參考
ms.assetid: 5356c575-2a59-4459-b4eb-76967deb6877
keywords:
- Windows (VFW) 影片捕獲參考影片
- 適用于 Windows) 的 VFW (影片、影片捕獲參考
- AVICap，參考
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cef19834e244f6070a1d8bb3383dcac017e4d161
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021046"
---
# <a name="video-capture-reference"></a><span data-ttu-id="08c31-106">影片捕獲參考</span><span class="sxs-lookup"><span data-stu-id="08c31-106">Video Capture Reference</span></span>

<span data-ttu-id="08c31-107">本節描述與 AVICap 視窗類別相關聯的函式、結構、訊息和宏。</span><span class="sxs-lookup"><span data-stu-id="08c31-107">This section describes the functions, structures, messages, and macros associated with the AVICap window class.</span></span> <span data-ttu-id="08c31-108">這些元素的分組方式如下。</span><span class="sxs-lookup"><span data-stu-id="08c31-108">These elements are grouped as follows.</span></span>

## <a name="basic-capture-operations"></a><span data-ttu-id="08c31-109">基本的捕獲作業</span><span class="sxs-lookup"><span data-stu-id="08c31-109">Basic Capture Operations</span></span>

-   [<span data-ttu-id="08c31-110">**capCreateCaptureWindow**</span><span class="sxs-lookup"><span data-stu-id="08c31-110">**capCreateCaptureWindow**</span></span>](/windows/desktop/api/Vfw/nf-vfw-capcreatecapturewindowa)
-   [<span data-ttu-id="08c31-111">**WM \_ 上限 \_ 中止**</span><span class="sxs-lookup"><span data-stu-id="08c31-111">**WM\_CAP\_ABORT**</span></span>](wm-cap-abort.md)
-   [<span data-ttu-id="08c31-112">**WM \_ CAP \_ 驅動程式 \_ 連接**</span><span class="sxs-lookup"><span data-stu-id="08c31-112">**WM\_CAP\_DRIVER\_CONNECT**</span></span>](wm-cap-driver-connect.md)
-   [<span data-ttu-id="08c31-113">**WM \_ CAP \_ 序列**</span><span class="sxs-lookup"><span data-stu-id="08c31-113">**WM\_CAP\_SEQUENCE**</span></span>](wm-cap-sequence.md)
-   [<span data-ttu-id="08c31-114">**WM \_ CAP \_ 停止**</span><span class="sxs-lookup"><span data-stu-id="08c31-114">**WM\_CAP\_STOP**</span></span>](wm-cap-stop.md)

## <a name="capture-windows"></a><span data-ttu-id="08c31-115">捕獲 Windows</span><span class="sxs-lookup"><span data-stu-id="08c31-115">Capture Windows</span></span>

-   [<span data-ttu-id="08c31-116">**CAPSTATUS**</span><span class="sxs-lookup"><span data-stu-id="08c31-116">**CAPSTATUS**</span></span>](/windows/win32/api/vfw/ns-vfw-capstatus)
-   [<span data-ttu-id="08c31-117">**capGetDriverDescription**</span><span class="sxs-lookup"><span data-stu-id="08c31-117">**capGetDriverDescription**</span></span>](/windows/desktop/api/Vfw/nf-vfw-capgetdriverdescriptiona)
-   [<span data-ttu-id="08c31-118">**WM \_ CAP \_ 驅動程式 \_ 連接**</span><span class="sxs-lookup"><span data-stu-id="08c31-118">**WM\_CAP\_DRIVER\_CONNECT**</span></span>](wm-cap-driver-connect.md)
-   [<span data-ttu-id="08c31-119">**WM \_ CAP \_ 驅動程式 \_ 中斷連線**</span><span class="sxs-lookup"><span data-stu-id="08c31-119">**WM\_CAP\_DRIVER\_DISCONNECT**</span></span>](wm-cap-driver-disconnect.md)
-   [<span data-ttu-id="08c31-120">**WM \_ CAP \_ 取得 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="08c31-120">**WM\_CAP\_GET\_STATUS**</span></span>](wm-cap-get-status.md)

## <a name="capture-drivers"></a><span data-ttu-id="08c31-121">捕獲驅動程式</span><span class="sxs-lookup"><span data-stu-id="08c31-121">Capture Drivers</span></span>

-   [<span data-ttu-id="08c31-122">**CAPDRIVERCAPS**</span><span class="sxs-lookup"><span data-stu-id="08c31-122">**CAPDRIVERCAPS**</span></span>](/windows/win32/api/vfw/ns-vfw-capdrivercaps)
-   [<span data-ttu-id="08c31-123">**WM \_ CAP \_ 驅動程式 \_ 取得 \_ 上限**</span><span class="sxs-lookup"><span data-stu-id="08c31-123">**WM\_CAP\_DRIVER\_GET\_CAPS**</span></span>](wm-cap-driver-get-caps.md)
-   [<span data-ttu-id="08c31-124">**WM \_ CAP \_ 驅動程式 \_ 取得 \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="08c31-124">**WM\_CAP\_DRIVER\_GET\_NAME**</span></span>](wm-cap-driver-get-name.md)
-   [<span data-ttu-id="08c31-125">**WM \_ CAP \_ 驅動程式 \_ 取得 \_ 版本**</span><span class="sxs-lookup"><span data-stu-id="08c31-125">**WM\_CAP\_DRIVER\_GET\_VERSION**</span></span>](wm-cap-driver-get-version.md)
-   [<span data-ttu-id="08c31-126">**WM \_ CAP \_ GET \_ AUDIOFORMAT**</span><span class="sxs-lookup"><span data-stu-id="08c31-126">**WM\_CAP\_GET\_AUDIOFORMAT**</span></span>](wm-cap-get-audioformat.md)
-   [<span data-ttu-id="08c31-127">**WM \_ CAP \_ GET \_ VIDEOFORMAT**</span><span class="sxs-lookup"><span data-stu-id="08c31-127">**WM\_CAP\_GET\_VIDEOFORMAT**</span></span>](wm-cap-get-videoformat.md)
-   [<span data-ttu-id="08c31-128">**WM \_ CAP \_ 設定 \_ AUDIOFORMAT**</span><span class="sxs-lookup"><span data-stu-id="08c31-128">**WM\_CAP\_SET\_AUDIOFORMAT**</span></span>](wm-cap-set-audioformat.md)
-   [<span data-ttu-id="08c31-129">**WM \_ CAP \_ 設定 \_ VIDEOFORMAT**</span><span class="sxs-lookup"><span data-stu-id="08c31-129">**WM\_CAP\_SET\_VIDEOFORMAT**</span></span>](wm-cap-set-videoformat.md)

## <a name="capture-driver-preview-and-overlay-modes"></a><span data-ttu-id="08c31-130">捕獲驅動程式預覽和重迭模式</span><span class="sxs-lookup"><span data-stu-id="08c31-130">Capture Driver Preview and Overlay Modes</span></span>

-   [<span data-ttu-id="08c31-131">**WM \_ CAP \_ 設定重迭 \_**</span><span class="sxs-lookup"><span data-stu-id="08c31-131">**WM\_CAP\_SET\_OVERLAY**</span></span>](wm-cap-set-overlay.md)
-   [<span data-ttu-id="08c31-132">**WM \_ CAP \_ 設定 \_ 預覽**</span><span class="sxs-lookup"><span data-stu-id="08c31-132">**WM\_CAP\_SET\_PREVIEW**</span></span>](wm-cap-set-preview.md)
-   [<span data-ttu-id="08c31-133">**WM \_ CAP \_ 設定 \_ PREVIEWRATE**</span><span class="sxs-lookup"><span data-stu-id="08c31-133">**WM\_CAP\_SET\_PREVIEWRATE**</span></span>](wm-cap-set-previewrate.md)
-   [<span data-ttu-id="08c31-134">**WM \_ CAP \_ 設定 \_ 規模**</span><span class="sxs-lookup"><span data-stu-id="08c31-134">**WM\_CAP\_SET\_SCALE**</span></span>](wm-cap-set-scale.md)
-   [<span data-ttu-id="08c31-135">**WM \_ CAP \_ 設定 \_ 捲軸**</span><span class="sxs-lookup"><span data-stu-id="08c31-135">**WM\_CAP\_SET\_SCROLL**</span></span>](wm-cap-set-scroll.md)

## <a name="capture-driver-video-dialog-boxes"></a><span data-ttu-id="08c31-136">[捕獲驅動程式影片] 對話方塊</span><span class="sxs-lookup"><span data-stu-id="08c31-136">Capture Driver Video Dialog Boxes</span></span>

-   [<span data-ttu-id="08c31-137">**WM \_ CAP \_ DLG \_ VIDEOCOMPRESSION**</span><span class="sxs-lookup"><span data-stu-id="08c31-137">**WM\_CAP\_DLG\_VIDEOCOMPRESSION**</span></span>](wm-cap-dlg-videocompression.md)
-   [<span data-ttu-id="08c31-138">**WM \_ CAP \_ DLG \_ VIDEODISPLAY**</span><span class="sxs-lookup"><span data-stu-id="08c31-138">**WM\_CAP\_DLG\_VIDEODISPLAY**</span></span>](wm-cap-dlg-videodisplay.md)
-   [<span data-ttu-id="08c31-139">**WM \_ CAP \_ DLG \_ VIDEOFORMAT**</span><span class="sxs-lookup"><span data-stu-id="08c31-139">**WM\_CAP\_DLG\_VIDEOFORMAT**</span></span>](wm-cap-dlg-videoformat.md)
-   [<span data-ttu-id="08c31-140">**WM \_ CAP \_ DLG \_ VIDEOSOURCE**</span><span class="sxs-lookup"><span data-stu-id="08c31-140">**WM\_CAP\_DLG\_VIDEOSOURCE**</span></span>](wm-cap-dlg-videosource.md)

## <a name="audio-format"></a><span data-ttu-id="08c31-141">音訊格式</span><span class="sxs-lookup"><span data-stu-id="08c31-141">Audio Format</span></span>

-   [<span data-ttu-id="08c31-142">**WM \_ CAP \_ GET \_ AUDIOFORMAT**</span><span class="sxs-lookup"><span data-stu-id="08c31-142">**WM\_CAP\_GET\_AUDIOFORMAT**</span></span>](wm-cap-get-audioformat.md)
-   [<span data-ttu-id="08c31-143">**WM \_ CAP \_ 設定 \_ AUDIOFORMAT**</span><span class="sxs-lookup"><span data-stu-id="08c31-143">**WM\_CAP\_SET\_AUDIOFORMAT**</span></span>](wm-cap-set-audioformat.md)

## <a name="video-capture-settings"></a><span data-ttu-id="08c31-144">影片捕獲設定</span><span class="sxs-lookup"><span data-stu-id="08c31-144">Video Capture Settings</span></span>

-   [<span data-ttu-id="08c31-145">**CAPTUREPARMS**</span><span class="sxs-lookup"><span data-stu-id="08c31-145">**CAPTUREPARMS**</span></span>](/windows/win32/api/vfw/ns-vfw-captureparms)
-   [<span data-ttu-id="08c31-146">**WM \_ CAP \_ 取得 \_ 順序 \_ 設定**</span><span class="sxs-lookup"><span data-stu-id="08c31-146">**WM\_CAP\_GET\_SEQUENCE\_SETUP**</span></span>](wm-cap-get-sequence-setup.md)
-   [<span data-ttu-id="08c31-147">**WM \_ CAP \_ 設定 \_ 順序 \_ 設定**</span><span class="sxs-lookup"><span data-stu-id="08c31-147">**WM\_CAP\_SET\_SEQUENCE\_SETUP**</span></span>](wm-cap-set-sequence-setup.md)

## <a name="capture-file-and-buffers"></a><span data-ttu-id="08c31-148">捕獲檔案和緩衝區</span><span class="sxs-lookup"><span data-stu-id="08c31-148">Capture File and Buffers</span></span>

-   [<span data-ttu-id="08c31-149">**CAPTUREPARMS**</span><span class="sxs-lookup"><span data-stu-id="08c31-149">**CAPTUREPARMS**</span></span>](/windows/win32/api/vfw/ns-vfw-captureparms)
-   [<span data-ttu-id="08c31-150">**WM \_ CAP \_ 檔案 \_ 配置**</span><span class="sxs-lookup"><span data-stu-id="08c31-150">**WM\_CAP\_FILE\_ALLOCATE**</span></span>](wm-cap-file-allocate.md)
-   [<span data-ttu-id="08c31-151">**WM \_ CAP \_ 檔案 \_ 取得 \_ 捕獲 \_ 檔案**</span><span class="sxs-lookup"><span data-stu-id="08c31-151">**WM\_CAP\_FILE\_GET\_CAPTURE\_FILE**</span></span>](wm-cap-file-get-capture-file.md)
-   [<span data-ttu-id="08c31-152">**WM \_ CAP \_ 檔案 \_ 另存**</span><span class="sxs-lookup"><span data-stu-id="08c31-152">**WM\_CAP\_FILE\_SAVEAS**</span></span>](wm-cap-file-saveas.md)
-   [<span data-ttu-id="08c31-153">**WM \_ CAP \_ FILE \_ SET \_ CAPTURE \_ 檔案**</span><span class="sxs-lookup"><span data-stu-id="08c31-153">**WM\_CAP\_FILE\_SET\_CAPTURE\_FILE**</span></span>](wm-cap-file-set-capture-file.md)

## <a name="directly-using-capture-data"></a><span data-ttu-id="08c31-154">直接使用 Capture 資料</span><span class="sxs-lookup"><span data-stu-id="08c31-154">Directly Using Capture Data</span></span>

-   [<span data-ttu-id="08c31-155">**WM \_ CAP \_ 序列 \_ NOFILE**</span><span class="sxs-lookup"><span data-stu-id="08c31-155">**WM\_CAP\_SEQUENCE\_NOFILE**</span></span>](wm-cap-sequence-nofile.md)

## <a name="capture-from-mci-device"></a><span data-ttu-id="08c31-156">從 MCI 裝置捕獲</span><span class="sxs-lookup"><span data-stu-id="08c31-156">Capture from MCI Device</span></span>

-   [<span data-ttu-id="08c31-157">**WM \_ CAP \_ 設定 \_ MCI \_ 裝置**</span><span class="sxs-lookup"><span data-stu-id="08c31-157">**WM\_CAP\_SET\_MCI\_DEVICE**</span></span>](wm-cap-set-mci-device.md)

## <a name="manual-frame-capture"></a><span data-ttu-id="08c31-158">手動畫面格捕獲</span><span class="sxs-lookup"><span data-stu-id="08c31-158">Manual Frame Capture</span></span>

-   [<span data-ttu-id="08c31-159">**WM \_ CAP \_ 單一 \_ 框架**</span><span class="sxs-lookup"><span data-stu-id="08c31-159">**WM\_CAP\_SINGLE\_FRAME**</span></span>](wm-cap-single-frame.md)
-   [<span data-ttu-id="08c31-160">**WM \_ 封閉 \_ 單一 \_ 畫面格 \_ 關閉**</span><span class="sxs-lookup"><span data-stu-id="08c31-160">**WM\_CAP\_SINGLE\_FRAME\_CLOSE**</span></span>](wm-cap-single-frame-close.md)
-   [<span data-ttu-id="08c31-161">**已 \_ 開啟 WM CAP \_ 單一 \_ 畫面 \_**</span><span class="sxs-lookup"><span data-stu-id="08c31-161">**WM\_CAP\_SINGLE\_FRAME\_OPEN**</span></span>](wm-cap-single-frame-open.md)

## <a name="still-image-capture"></a><span data-ttu-id="08c31-162">Still-Image Capture</span><span class="sxs-lookup"><span data-stu-id="08c31-162">Still-Image Capture</span></span>

-   [<span data-ttu-id="08c31-163">**WM \_ CAP \_ 編輯 \_ 複本**</span><span class="sxs-lookup"><span data-stu-id="08c31-163">**WM\_CAP\_EDIT\_COPY**</span></span>](wm-cap-edit-copy.md)
-   [<span data-ttu-id="08c31-164">**WM \_ CAP \_ FILE \_ SAVEDIB**</span><span class="sxs-lookup"><span data-stu-id="08c31-164">**WM\_CAP\_FILE\_SAVEDIB**</span></span>](wm-cap-file-savedib.md)
-   [<span data-ttu-id="08c31-165">**WM \_ 上限 \_ 抓取 \_ 框架**</span><span class="sxs-lookup"><span data-stu-id="08c31-165">**WM\_CAP\_GRAB\_FRAME**</span></span>](wm-cap-grab-frame.md)
-   [<span data-ttu-id="08c31-166">**WM \_ CAP \_ 抓取 \_ 框架 \_ NOSTOP**</span><span class="sxs-lookup"><span data-stu-id="08c31-166">**WM\_CAP\_GRAB\_FRAME\_NOSTOP**</span></span>](wm-cap-grab-frame-nostop.md)

## <a name="advanced-capture-options"></a><span data-ttu-id="08c31-167">Advanced Capture 選項</span><span class="sxs-lookup"><span data-stu-id="08c31-167">Advanced Capture Options</span></span>

-   [<span data-ttu-id="08c31-168">**WM \_ CAP \_ FILE \_ SET \_ INFOCHUNK**</span><span class="sxs-lookup"><span data-stu-id="08c31-168">**WM\_CAP\_FILE\_SET\_INFOCHUNK**</span></span>](wm-cap-file-set-infochunk.md)
-   [<span data-ttu-id="08c31-169">**WM \_ CAP \_ 取得 \_ 使用者 \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="08c31-169">**WM\_CAP\_GET\_USER\_DATA**</span></span>](wm-cap-get-user-data.md)
-   [<span data-ttu-id="08c31-170">**WM \_ CAP \_ 設定 \_ 使用者 \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="08c31-170">**WM\_CAP\_SET\_USER\_DATA**</span></span>](wm-cap-set-user-data.md)

## <a name="working-with-palettes"></a><span data-ttu-id="08c31-171">使用調色板</span><span class="sxs-lookup"><span data-stu-id="08c31-171">Working with Palettes</span></span>

-   [<span data-ttu-id="08c31-172">**WM \_ CAP \_ 編輯 \_ 複本**</span><span class="sxs-lookup"><span data-stu-id="08c31-172">**WM\_CAP\_EDIT\_COPY**</span></span>](wm-cap-edit-copy.md)
-   [<span data-ttu-id="08c31-173">**已自動將 WM \_ CAP \_ PAL \_**</span><span class="sxs-lookup"><span data-stu-id="08c31-173">**WM\_CAP\_PAL\_AUTOCREATE**</span></span>](wm-cap-pal-autocreate.md)
-   [<span data-ttu-id="08c31-174">**WM \_ CAP \_ PAL \_ MANUALCREATE**</span><span class="sxs-lookup"><span data-stu-id="08c31-174">**WM\_CAP\_PAL\_MANUALCREATE**</span></span>](wm-cap-pal-manualcreate.md)
-   [<span data-ttu-id="08c31-175">**已 \_ 開啟 WM CAP \_ PAL \_**</span><span class="sxs-lookup"><span data-stu-id="08c31-175">**WM\_CAP\_PAL\_OPEN**</span></span>](wm-cap-pal-open.md)
-   [<span data-ttu-id="08c31-176">**WM \_ CAP \_ PAL \_ 貼上**</span><span class="sxs-lookup"><span data-stu-id="08c31-176">**WM\_CAP\_PAL\_PASTE**</span></span>](wm-cap-pal-paste.md)
-   [<span data-ttu-id="08c31-177">**WM \_ CAP \_ PAL \_ 儲存**</span><span class="sxs-lookup"><span data-stu-id="08c31-177">**WM\_CAP\_PAL\_SAVE**</span></span>](wm-cap-pal-save.md)

## <a name="yielding-to-other-applications"></a><span data-ttu-id="08c31-178">產生給其他應用程式</span><span class="sxs-lookup"><span data-stu-id="08c31-178">Yielding to Other Applications</span></span>

-   [<span data-ttu-id="08c31-179">**WM \_ CAP \_ 取得 \_ 順序 \_ 設定**</span><span class="sxs-lookup"><span data-stu-id="08c31-179">**WM\_CAP\_GET\_SEQUENCE\_SETUP**</span></span>](wm-cap-get-sequence-setup.md)
-   [<span data-ttu-id="08c31-180">**WM \_ CAP \_ 設定 \_ 回呼 \_ YIELD**</span><span class="sxs-lookup"><span data-stu-id="08c31-180">**WM\_CAP\_SET\_CALLBACK\_YIELD**</span></span>](wm-cap-set-callback-yield.md)
-   [<span data-ttu-id="08c31-181">**WM \_ CAP \_ 設定 \_ 順序 \_ 設定**</span><span class="sxs-lookup"><span data-stu-id="08c31-181">**WM\_CAP\_SET\_SEQUENCE\_SETUP**</span></span>](wm-cap-set-sequence-setup.md)

## <a name="avicap-callback-functions"></a><span data-ttu-id="08c31-182">AVICap 回呼函式</span><span class="sxs-lookup"><span data-stu-id="08c31-182">AVICap Callback Functions</span></span>

-   [<span data-ttu-id="08c31-183">**capControlCallback**</span><span class="sxs-lookup"><span data-stu-id="08c31-183">**capControlCallback**</span></span>](/windows/desktop/api/Vfw/nc-vfw-capcontrolcallback)
-   [<span data-ttu-id="08c31-184">**capErrorCallback**</span><span class="sxs-lookup"><span data-stu-id="08c31-184">**capErrorCallback**</span></span>](/windows/desktop/api/Vfw/nc-vfw-caperrorcallbacka)
-   [<span data-ttu-id="08c31-185">**capStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="08c31-185">**capStatusCallback**</span></span>](/windows/desktop/api/Vfw/nc-vfw-capstatuscallbacka)
-   [<span data-ttu-id="08c31-186">**capVideoStreamCallback**</span><span class="sxs-lookup"><span data-stu-id="08c31-186">**capVideoStreamCallback**</span></span>](/windows/desktop/api/Vfw/nc-vfw-capvideocallback)
-   [<span data-ttu-id="08c31-187">**capWaveStreamCallback**</span><span class="sxs-lookup"><span data-stu-id="08c31-187">**capWaveStreamCallback**</span></span>](/windows/desktop/api/Vfw/nc-vfw-capwavecallback)
-   [<span data-ttu-id="08c31-188">**capYieldCallback**</span><span class="sxs-lookup"><span data-stu-id="08c31-188">**capYieldCallback**</span></span>](/windows/desktop/api/Vfw/nc-vfw-capyieldcallback)
-   [<span data-ttu-id="08c31-189">**WM \_ CAP \_ 設定 \_ 回呼 \_ CAPCONTROL**</span><span class="sxs-lookup"><span data-stu-id="08c31-189">**WM\_CAP\_SET\_CALLBACK\_CAPCONTROL**</span></span>](wm-cap-set-callback-capcontrol.md)
-   [<span data-ttu-id="08c31-190">**WM \_ CAP \_ 設定 \_ 回呼 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="08c31-190">**WM\_CAP\_SET\_CALLBACK\_ERROR**</span></span>](wm-cap-set-callback-error.md)
-   [<span data-ttu-id="08c31-191">**WM \_ CAP \_ 設定 \_ 回呼 \_ 框架**</span><span class="sxs-lookup"><span data-stu-id="08c31-191">**WM\_CAP\_SET\_CALLBACK\_FRAME**</span></span>](wm-cap-set-callback-frame.md)
-   [<span data-ttu-id="08c31-192">**WM \_ CAP \_ 設定 \_ 回呼 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="08c31-192">**WM\_CAP\_SET\_CALLBACK\_STATUS**</span></span>](wm-cap-set-callback-status.md)
-   [<span data-ttu-id="08c31-193">**WM \_ CAP \_ 設定 \_ 回呼 \_ M**</span><span class="sxs-lookup"><span data-stu-id="08c31-193">**WM\_CAP\_SET\_CALLBACK\_VIDEOSTREAM**</span></span>](wm-cap-set-callback-videostream.md)
-   [<span data-ttu-id="08c31-194">**WM \_ CAP \_ 設定 \_ 回呼 \_ WAVESTREAM**</span><span class="sxs-lookup"><span data-stu-id="08c31-194">**WM\_CAP\_SET\_CALLBACK\_WAVESTREAM**</span></span>](wm-cap-set-callback-wavestream.md)
-   [<span data-ttu-id="08c31-195">**WM \_ CAP \_ 設定 \_ 回呼 \_ YIELD**</span><span class="sxs-lookup"><span data-stu-id="08c31-195">**WM\_CAP\_SET\_CALLBACK\_YIELD**</span></span>](wm-cap-set-callback-yield.md)

## <a name="related-topics"></a><span data-ttu-id="08c31-196">相關主題</span><span class="sxs-lookup"><span data-stu-id="08c31-196">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08c31-197">影片捕獲</span><span class="sxs-lookup"><span data-stu-id="08c31-197">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 




