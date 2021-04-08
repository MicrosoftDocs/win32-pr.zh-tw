---
title: 捕獲視窗狀態
description: 捕獲視窗狀態
ms.assetid: c3f80cac-30b2-42f0-8a9c-4053728c558b
keywords:
- WM_CAP_GET_STATUS 訊息
- capGetStatus 宏
- CAPSTATUS 結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e6019009c8510abe3429c1043527156c55f0c4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021842"
---
# <a name="capture-window-status"></a>捕獲視窗狀態

您可以使用 [ [**WM \_ CAP \_ 取得 \_ 狀態**](wm-cap-get-status.md) 消息 (] 或 [ [**capGetStatus**](/windows/desktop/api/Vfw/nf-vfw-capgetstatus) 宏) ]，以抓取捕捉視窗的目前狀態。 此訊息會以其成員的目前值抓取 [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) 結構的複本。 **CAPSTATUS** 結構包含影像維度、捲軸位置，以及是否啟用影像的重迭或預覽的相關資訊。 因為 **CAPSTATUS** 中表示的資訊是動態的，所以當所捕捉的影片資料流程大小或格式可能已變更時，您的應用程式應該重新整理結構的內容 (例如，在顯示 capture 驅動程式) 的影片格式之後。

變更 [捕捉] 視窗的維度不會影響實際所捕獲影片資料流程的維度。 影片擷取裝置磁碟機所顯示的 [格式] 對話方塊會控制所捕獲影片串流的維度。

 

 




