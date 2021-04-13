---
title: 指定時間格式
description: 指定時間格式
ms.assetid: 11d28d63-ed3e-4137-b9d8-1681bf0e33ff
keywords:
- MCIWndGetTimeFormat 宏
- MCIWndSetTimeFormat 宏
- MCIWndUseTime 宏
- MCIWndUseFrames 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e390e811bde4d797572c19f372923906f6b738b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300908"
---
# <a name="specifying-time-formats"></a>指定時間格式

多媒體資料類型通常可以使用時間來識別其內容中的重要位置。 常見的時間格式為毫秒、追蹤和框架;其他較不常見的時間格式，例如 SMPTE (社會的運動圖片和電視工程師) 24）也存在。 時間是波形-音訊、MIDI 和 CD 音訊資料的格式和參考系統。 雖然影片會記錄為一系列的畫面格 (串流) 通常會以特定速度播放，但影片仍支援時間。 有幾個宏可以用來指定時間格式。

您可以使用 [**MCIWndGetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat) 宏來取得檔案或裝置的目前時間格式。 您可以使用 [**MCIWndSetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimeformat) 宏，將目前的時間格式變更為裝置所支援的任何其他時間格式。 或者，您可以使用 [**MCIWndUseTime**](/windows/desktop/api/Vfw/nf-vfw-mciwndusetime) 或 [**MCIWndUseFrames**](/windows/desktop/api/Vfw/nf-vfw-mciwnduseframes) 宏將時間格式設定為毫秒或框架。

> [!Note]  
> Noncontinuous 格式（例如追蹤和 SMPTE）可能會造成工具列的行為不穩定。 針對這些時間格式，您可能會想要在 \_ 建立 MCIWnd 視窗時，指定 MCIWNDF NOPLAYBAR 視窗樣式來關閉工具列。

 

 

 




