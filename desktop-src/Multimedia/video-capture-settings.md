---
title: 影片捕獲設定
description: 影片捕獲設定
ms.assetid: f5c887ca-9430-4221-8748-5b389247b7a4
keywords:
- CAPTUREPARMS 結構
- WM_CAP_GET_SEQUENCE_SETUP 訊息
- capCaptureGetSetup 宏
- WM_CAP_SET_SEQUENCE_SETUP 訊息
- capCaptureSetSetup 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b50eb26170c8b1594d288cec903ef0c05867a24db2d5a89a6ad60f66eef4fd0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118135586"
---
# <a name="video-capture-settings"></a>影片捕獲設定

[**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms)結構包含串流處理影片捕獲的控制項參數。 此結構可控制捕捉程式的幾個層面，並可讓您執行下列工作：

-   指定畫面播放速率。
-   指定已配置的影片緩衝區數目。
-   停用並啟用音訊捕獲。
-   指定 capture 的時間間隔。
-   指定是否在捕獲期間使用 MCI 裝置 (VCR 或 videodisc) 。
-   指定用於結束資料流程的鍵盤或滑鼠控制項。
-   指定在捕捉期間套用的最平均影片類型。

您可以在 [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) 結構中取出目前的捕獲設定，方法是將 [**WM \_ CAP \_ GET \_ SEQUENCE \_ 安裝**](wm-cap-get-sequence-setup.md) 訊息 (或 [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) 宏) 傳送至 capture 視窗。 您可以設定一或多個目前的捕獲設定，方法是更新 **CAPTUREPARMS** 結構的適當成員，然後將 [**WM \_ CAP \_ set \_ SEQUENCE 設定 \_**](wm-cap-set-sequence-setup.md) 訊息 (或 [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) 宏) 和 **CAPTUREPARMS** 傳送至 [capture] 視窗。

 

 




