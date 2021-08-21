---
title: Capture 檔案名
description: Capture 檔案名
ms.assetid: b17ecdd4-899e-4e94-98f2-496f93491e06
keywords:
- WM_CAP_FILE_SET_CAPTURE_FILE 訊息
- capFileSetCaptureFile 宏
- WM_CAP_FILE_GET_CAPTURE_FILE 訊息
- capFileGetCaptureFile 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47e48ecd727accccb868d0f78c68a833ac6ec6655bada23db8a56f2a9aeaffd1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118941593"
---
# <a name="capture-filename"></a>Capture 檔案名

根據預設，AVICap 會從捕捉視窗將影片和音訊串流資料，路由至目前磁片磁碟機根目錄中名為 CAPTURE.AVI 的檔案。 您可以藉由將 [**WM \_ CAP \_ file \_ SET \_ CAPTURE \_ file**](wm-cap-file-set-capture-file.md) message (或 [**capFileSetCaptureFile**](/windows/desktop/api/Vfw/nf-vfw-capfilesetcapturefile) 宏) 傳送至 CAPTURE 視窗，來指定替代檔案名。 此訊息會指定檔案名;它不會建立、配置或開啟檔案。 您可以藉由將「 [**WM \_ CAP 檔案 \_ \_ 取得 \_ 捕獲 \_**](wm-cap-file-get-capture-file.md) 檔案」訊息 (或 [**capFileGetCaptureFile**](/windows/desktop/api/Vfw/nf-vfw-capfilegetcapturefile) 宏) 傳送至「捕獲視窗」，以抓取目前的 capture 檔案名。

 

 




