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
ms.openlocfilehash: 4856649906e09f212d2f8992c9d4fb9b8f4c37d4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106966799"
---
# <a name="capture-filename"></a><span data-ttu-id="ccea4-107">Capture 檔案名</span><span class="sxs-lookup"><span data-stu-id="ccea4-107">Capture Filename</span></span>

<span data-ttu-id="ccea4-108">根據預設，AVICap 會從捕捉視窗將影片和音訊串流資料，路由至目前磁片磁碟機根目錄中名為 CAPTURE.AVI 的檔案。</span><span class="sxs-lookup"><span data-stu-id="ccea4-108">AVICap, by default, routes video and audio stream data from a capture window to a file named CAPTURE.AVI in the root directory of the current drive.</span></span> <span data-ttu-id="ccea4-109">您可以藉由將 [**WM \_ CAP \_ file \_ SET \_ CAPTURE \_ file**](wm-cap-file-set-capture-file.md) message (或 [**capFileSetCaptureFile**](/windows/desktop/api/Vfw/nf-vfw-capfilesetcapturefile) 宏) 傳送至 CAPTURE 視窗，來指定替代檔案名。</span><span class="sxs-lookup"><span data-stu-id="ccea4-109">You can specify an alternate filename by sending the [**WM\_CAP\_FILE\_SET\_CAPTURE\_FILE**](wm-cap-file-set-capture-file.md) message (or the [**capFileSetCaptureFile**](/windows/desktop/api/Vfw/nf-vfw-capfilesetcapturefile) macro) to a capture window.</span></span> <span data-ttu-id="ccea4-110">此訊息會指定檔案名;它不會建立、配置或開啟檔案。</span><span class="sxs-lookup"><span data-stu-id="ccea4-110">This message specifies the filename; it does not create, allocate, or open the file.</span></span> <span data-ttu-id="ccea4-111">您可以藉由將「 [**WM \_ CAP 檔案 \_ \_ 取得 \_ 捕獲 \_**](wm-cap-file-get-capture-file.md) 檔案」訊息 (或 [**capFileGetCaptureFile**](/windows/desktop/api/Vfw/nf-vfw-capfilegetcapturefile) 宏) 傳送至「捕獲視窗」，以抓取目前的 capture 檔案名。</span><span class="sxs-lookup"><span data-stu-id="ccea4-111">You can retrieve the current capture filename by sending the [**WM\_CAP\_FILE\_GET\_CAPTURE\_FILE**](wm-cap-file-get-capture-file.md) message (or the [**capFileGetCaptureFile**](/windows/desktop/api/Vfw/nf-vfw-capfilegetcapturefile) macro) to a capture window.</span></span>

 

 




