---
title: Still-Image Capture
description: Still-Image Capture
ms.assetid: 9e84b385-aedb-4132-8a2d-72c32594083a
keywords:
- WM_CAP_GRAB_FRAME_NOSTOP 訊息
- WM_CAP_GRAB_FRAME 訊息
- capGrabFrameNoStop 宏
- capGrabFrame 宏
- WM_CAP_EDIT_COPY 訊息
- capEditCopy 宏
- WM_CAP_FILE_SAVEDIB 訊息
- capFileSaveDIB 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c0d822292489be4093998ac18d70191dbe2b87327a33adaba26e8442420d93b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688598"
---
# <a name="still-image-capture"></a>Still-Image Capture

如果您想要將單一框架視為靜止影像，您可以使用 [**wm \_ cap \_ 抓取 \_ 框架 \_ NOSTOP**](wm-cap-grab-frame-nostop.md) 或 [**Wm \_ 帽 \_ 抓取 \_ 框架**](wm-cap-grab-frame.md) 訊息 (或 [**capGrabFrameNoStop**](/windows/desktop/api/Vfw/nf-vfw-capgrabframenostop) 或 [**capGrabFrame**](/windows/desktop/api/Vfw/nf-vfw-capgrabframe) 宏) ，以在內部畫面緩衝區中捕獲數位化的影像。 您可以使用 WM \_ CAP 抓取框架凍結已捕捉映射上的 \_ 顯示 \_ 。 否則，請使用 WM \_ CAP \_ 抓取畫面格 \_ \_ NOSTOP。

一旦捕獲之後，您就可以複製映射以供其他應用程式使用。 您可以使用 [ [**WM \_ CAP \_ 編輯 \_ 複製**](wm-cap-edit-copy.md) 訊息 (] 或 [ [**capEditCopy**](/windows/desktop/api/Vfw/nf-vfw-capeditcopy) 宏) ，將影像從框架緩衝區複製到剪貼簿。 您也可以使用 [**WM \_ CAP \_ FILE \_ SAVEDIB**](wm-cap-file-savedib.md) message (或 [**capFileSaveDIB**](/windows/desktop/api/Vfw/nf-vfw-capfilesavedib) 宏) ，將影像從框架緩衝區複製到與裝置無關的點陣圖 (DIB) 。

您的應用程式也可以使用這兩個單一畫面格捕獲訊息，依框架編輯序列框架，或建立時間間隔的攝影順序。

 

 




