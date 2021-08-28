---
title: 手動畫面格捕獲
description: 手動畫面格捕獲
ms.assetid: 7c5576ff-2694-4f44-a386-03bbc6f9c2ed
keywords:
- WM_CAP_SINGLE_FRAME_OPEN 訊息
- WM_CAP_SINGLE_FRAME 訊息
- WM_CAP_SINGLE_FRAME_CLOSE 訊息
- capCaptureSingleFrameOpen 宏
- capCaptureSingleFrame 宏
- capCaptureSingleFrameClose 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e9024f8759697248b1aadf2f46f902c4bf706c9d10417281d9b5c4f61fc1e94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118138853"
---
# <a name="manual-frame-capture"></a>手動畫面格捕獲

如果您想要個別指定要在影片串流中捕捉的框架，您可以使用「 [**wm」 \_ \_ 單一 \_ 畫面格 \_ 開啟**](wm-cap-single-frame-open.md)、 [**WM \_ cap \_ 單一 \_ 框架**](wm-cap-single-frame.md)，以及「 [**wm 端點」 \_ \_ 單一 \_ 框架 \_ 關閉**](wm-cap-single-frame-close.md) 訊息 (或 [**capCaptureSingleFrameOpen**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframeopen)、 [**capCaptureSingleFrame**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframe)和 [**capCaptureSingleFrameClose**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframeclose) 宏) 來控制序列。 一般而言，這些訊息是用來建立動畫，方法是將個別的框架附加至 capture 檔案。 [WM \_ CAP \_ 單一畫面格開啟] 會開啟檔案 \_ \_ 以進行手動驅動的捕獲操作。 WM \_ CAP \_ 單一 \_ 畫面格會捕捉個別的畫面格，並將其附加至 capture 檔案。 WM \_ CAP \_ 單一 \_ 畫面格 \_ 關閉會關閉手動畫面格捕獲所用的檔案。

> [!Note]  
> 此捕捉方法不支援使用影片捕獲同時進行音訊捕獲。

 

 

 




