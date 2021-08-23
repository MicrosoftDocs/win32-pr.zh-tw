---
title: DirectShow 和 Windows 媒體
description: DirectShow 和 Windows 媒體
ms.assetid: e2ddc781-9f56-4f77-a191-015018755eff
keywords:
- Windows媒體格式 SDK，DirectShow
- Advanced Systems Format (ASF) ，DirectShow
- ASF (Advanced Systems Format) ，DirectShow
- DirectShow，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b975347d26414dda0c1f54c0b71ac852541bd58c314e3724725c3768ddfc7bfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027906"
---
# <a name="directshow-and-windows-media"></a>DirectShow 和 Windows 媒體

除了單獨使用 Windows 媒體格式 SDK 之外，應用程式也可以使用 Microsoft® DirectShow®串流架構來讀取和寫入 Windows 媒體型內容，如下列各節所述。



| 區段                                                                                   | 描述                                                                                                                                 |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [關於 DirectShow](about-directshow.md)                                                  | 描述一般詞彙的 DirectShow，並告訴您要在何處取得相關資訊。                                                     |
| [為何要使用 DirectShow？](why-use-directshow.md)                                             | 描述 DirectShow 如何簡化 Windows 媒體型內容建立和播放的特定工作。                              |
| [在 DirectShow 中讀取 ASF 檔案](reading-asf-files-in-directshow.md)                    | 說明如何使用 DirectShow 播放 ASF 檔案。                                                                                           |
| [在 DirectShow 中建立 ASF 檔案](creating-asf-files-in-directshow.md)                  | 說明如何使用 DirectShow 建立 ASF 檔案。                                                                                         |
| [\_DirectShow 中的 WMT 狀態事件通知](wmt-status-notification-in-directshow.md) | 描述 ASF 讀取器和 ASF 寫入器篩選器會處理哪些 **WMT \_ 狀態** 事件，以及應用程式如何接收這些事件。 |
| [DirectShow 中的 DRM 支援](drm-support-in-directshow.md)                                | 說明如何透過 DirectShow 讀取和寫入受 DRM 保護的檔案。                                                                     |
| [DirectShowQASF 參考](directshow-qasf-reference.md)                                | 包含支援 Windows 媒體之 DirectShow 元件的參考檔。                                              |



 

SDK 中的三個範例應用程式說明如何使用 DirectShow： DSCopy、DSPlay 和 DSSeekFM。 如需詳細資訊，請參閱 [範例應用程式](sample-applications.md)。

> [!Note]  
> 使用此 SDK 所含 QASF 元件的應用程式需要在 Windows®2000、Windows 98 和 Windows 95 系統上安裝 Microsoft DirectX®8.1 或更新版本的 SDK 執行時間。 具體而言，在 DirectShow 篩選圖形中裝載 Windows 媒體編解碼器的 DMO 包裝函式篩選器需要此執行時間。

 

 

 




