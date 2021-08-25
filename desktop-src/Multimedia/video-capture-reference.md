---
title: 影片捕獲參考
description: 影片捕獲參考
ms.assetid: 5356c575-2a59-4459-b4eb-76967deb6877
keywords:
- 影片 Windows (VFW) 、影片捕獲參考
- 適用于 Windows) 、影片捕獲參考的 VFW (影片
- AVICap，參考
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 166bdcf06e700023a197334b0e63f612398485affe21dc9ffbc6e7ac0800926a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119804308"
---
# <a name="video-capture-reference"></a>影片捕獲參考

本節描述與 AVICap 視窗類別相關聯的函式、結構、訊息和宏。 這些元素的分組方式如下。

## <a name="basic-capture-operations"></a>基本的捕獲作業

-   [**capCreateCaptureWindow**](/windows/desktop/api/Vfw/nf-vfw-capcreatecapturewindowa)
-   [**WM \_ 上限 \_ 中止**](wm-cap-abort.md)
-   [**WM \_ CAP \_ 驅動程式 \_ 連接**](wm-cap-driver-connect.md)
-   [**WM \_ CAP \_ 序列**](wm-cap-sequence.md)
-   [**WM \_ CAP \_ 停止**](wm-cap-stop.md)

## <a name="capture-windows"></a>Capture Windows

-   [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus)
-   [**capGetDriverDescription**](/windows/desktop/api/Vfw/nf-vfw-capgetdriverdescriptiona)
-   [**WM \_ CAP \_ 驅動程式 \_ 連接**](wm-cap-driver-connect.md)
-   [**WM \_ CAP \_ 驅動程式 \_ 中斷連線**](wm-cap-driver-disconnect.md)
-   [**WM \_ CAP \_ 取得 \_ 狀態**](wm-cap-get-status.md)

## <a name="capture-drivers"></a>捕獲驅動程式

-   [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps)
-   [**WM \_ CAP \_ 驅動程式 \_ 取得 \_ 上限**](wm-cap-driver-get-caps.md)
-   [**WM \_ CAP \_ 驅動程式 \_ 取得 \_ 名稱**](wm-cap-driver-get-name.md)
-   [**WM \_ CAP \_ 驅動程式 \_ 取得 \_ 版本**](wm-cap-driver-get-version.md)
-   [**WM \_ CAP \_ GET \_ AUDIOFORMAT**](wm-cap-get-audioformat.md)
-   [**WM \_ CAP \_ GET \_ VIDEOFORMAT**](wm-cap-get-videoformat.md)
-   [**WM \_ CAP \_ 設定 \_ AUDIOFORMAT**](wm-cap-set-audioformat.md)
-   [**WM \_ CAP \_ 設定 \_ VIDEOFORMAT**](wm-cap-set-videoformat.md)

## <a name="capture-driver-preview-and-overlay-modes"></a>捕獲驅動程式預覽和重迭模式

-   [**WM \_ CAP \_ 設定重迭 \_**](wm-cap-set-overlay.md)
-   [**WM \_ CAP \_ 設定 \_ 預覽**](wm-cap-set-preview.md)
-   [**WM \_ CAP \_ 設定 \_ PREVIEWRATE**](wm-cap-set-previewrate.md)
-   [**WM \_ CAP \_ 設定 \_ 規模**](wm-cap-set-scale.md)
-   [**WM \_ CAP \_ 設定 \_ 捲軸**](wm-cap-set-scroll.md)

## <a name="capture-driver-video-dialog-boxes"></a>[捕獲驅動程式影片] 對話方塊

-   [**WM \_ CAP \_ DLG \_ VIDEOCOMPRESSION**](wm-cap-dlg-videocompression.md)
-   [**WM \_ CAP \_ DLG \_ VIDEODISPLAY**](wm-cap-dlg-videodisplay.md)
-   [**WM \_ CAP \_ DLG \_ VIDEOFORMAT**](wm-cap-dlg-videoformat.md)
-   [**WM \_ CAP \_ DLG \_ VIDEOSOURCE**](wm-cap-dlg-videosource.md)

## <a name="audio-format"></a>音訊格式

-   [**WM \_ CAP \_ GET \_ AUDIOFORMAT**](wm-cap-get-audioformat.md)
-   [**WM \_ CAP \_ 設定 \_ AUDIOFORMAT**](wm-cap-set-audioformat.md)

## <a name="video-capture-settings"></a>影片捕獲設定

-   [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms)
-   [**WM \_ CAP \_ 取得 \_ 順序 \_ 設定**](wm-cap-get-sequence-setup.md)
-   [**WM \_ CAP \_ 設定 \_ 順序 \_ 設定**](wm-cap-set-sequence-setup.md)

## <a name="capture-file-and-buffers"></a>捕獲檔案和緩衝區

-   [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms)
-   [**WM \_ CAP \_ 檔案 \_ 配置**](wm-cap-file-allocate.md)
-   [**WM \_ CAP \_ 檔案 \_ 取得 \_ 捕獲 \_ 檔案**](wm-cap-file-get-capture-file.md)
-   [**WM \_ CAP \_ 檔案 \_ 另存**](wm-cap-file-saveas.md)
-   [**WM \_ CAP \_ FILE \_ SET \_ CAPTURE \_ 檔案**](wm-cap-file-set-capture-file.md)

## <a name="directly-using-capture-data"></a>直接使用 Capture 資料

-   [**WM \_ CAP \_ 序列 \_ NOFILE**](wm-cap-sequence-nofile.md)

## <a name="capture-from-mci-device"></a>從 MCI 裝置捕獲

-   [**WM \_ CAP \_ 設定 \_ MCI \_ 裝置**](wm-cap-set-mci-device.md)

## <a name="manual-frame-capture"></a>手動畫面格捕獲

-   [**WM \_ CAP \_ 單一 \_ 框架**](wm-cap-single-frame.md)
-   [**WM \_ 封閉 \_ 單一 \_ 畫面格 \_ 關閉**](wm-cap-single-frame-close.md)
-   [**已 \_ 開啟 WM CAP \_ 單一 \_ 畫面 \_**](wm-cap-single-frame-open.md)

## <a name="still-image-capture"></a>Still-Image Capture

-   [**WM \_ CAP \_ 編輯 \_ 複本**](wm-cap-edit-copy.md)
-   [**WM \_ CAP \_ FILE \_ SAVEDIB**](wm-cap-file-savedib.md)
-   [**WM \_ 上限 \_ 抓取 \_ 框架**](wm-cap-grab-frame.md)
-   [**WM \_ CAP \_ 抓取 \_ 框架 \_ NOSTOP**](wm-cap-grab-frame-nostop.md)

## <a name="advanced-capture-options"></a>Advanced Capture 選項

-   [**WM \_ CAP \_ FILE \_ SET \_ INFOCHUNK**](wm-cap-file-set-infochunk.md)
-   [**WM \_ CAP \_ 取得 \_ 使用者 \_ 資料**](wm-cap-get-user-data.md)
-   [**WM \_ CAP \_ 設定 \_ 使用者 \_ 資料**](wm-cap-set-user-data.md)

## <a name="working-with-palettes"></a>使用調色板

-   [**WM \_ CAP \_ 編輯 \_ 複本**](wm-cap-edit-copy.md)
-   [**已自動將 WM \_ CAP \_ PAL \_**](wm-cap-pal-autocreate.md)
-   [**WM \_ CAP \_ PAL \_ MANUALCREATE**](wm-cap-pal-manualcreate.md)
-   [**已 \_ 開啟 WM CAP \_ PAL \_**](wm-cap-pal-open.md)
-   [**WM \_ CAP \_ PAL \_ 貼上**](wm-cap-pal-paste.md)
-   [**WM \_ CAP \_ PAL \_ 儲存**](wm-cap-pal-save.md)

## <a name="yielding-to-other-applications"></a>產生給其他應用程式

-   [**WM \_ CAP \_ 取得 \_ 順序 \_ 設定**](wm-cap-get-sequence-setup.md)
-   [**WM \_ CAP \_ 設定 \_ 回呼 \_ YIELD**](wm-cap-set-callback-yield.md)
-   [**WM \_ CAP \_ 設定 \_ 順序 \_ 設定**](wm-cap-set-sequence-setup.md)

## <a name="avicap-callback-functions"></a>AVICap 回呼函式

-   [**capControlCallback**](/windows/desktop/api/Vfw/nc-vfw-capcontrolcallback)
-   [**capErrorCallback**](/windows/desktop/api/Vfw/nc-vfw-caperrorcallbacka)
-   [**capStatusCallback**](/windows/desktop/api/Vfw/nc-vfw-capstatuscallbacka)
-   [**capVideoStreamCallback**](/windows/desktop/api/Vfw/nc-vfw-capvideocallback)
-   [**capWaveStreamCallback**](/windows/desktop/api/Vfw/nc-vfw-capwavecallback)
-   [**capYieldCallback**](/windows/desktop/api/Vfw/nc-vfw-capyieldcallback)
-   [**WM \_ CAP \_ 設定 \_ 回呼 \_ CAPCONTROL**](wm-cap-set-callback-capcontrol.md)
-   [**WM \_ CAP \_ 設定 \_ 回呼 \_ 錯誤**](wm-cap-set-callback-error.md)
-   [**WM \_ CAP \_ 設定 \_ 回呼 \_ 框架**](wm-cap-set-callback-frame.md)
-   [**WM \_ CAP \_ 設定 \_ 回呼 \_ 狀態**](wm-cap-set-callback-status.md)
-   [**WM \_ CAP \_ 設定 \_ 回呼 \_ M**](wm-cap-set-callback-videostream.md)
-   [**WM \_ CAP \_ 設定 \_ 回呼 \_ WAVESTREAM**](wm-cap-set-callback-wavestream.md)
-   [**WM \_ CAP \_ 設定 \_ 回呼 \_ YIELD**](wm-cap-set-callback-yield.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[影片捕獲](video-capture.md)
</dt> </dl>

 

 




