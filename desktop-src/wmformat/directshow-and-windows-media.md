---
title: DirectShow 和 Windows Media
description: DirectShow 和 Windows Media
ms.assetid: e2ddc781-9f56-4f77-a191-015018755eff
keywords:
- Windows Media Format SDK、DirectShow
- Advanced Systems Format (ASF) 、DirectShow
- ASF (Advanced Systems Format) ，DirectShow
- DirectShow，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd4ca8eb4b1051d6685efa0bf73052ad9e7b31fa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675676"
---
# <a name="directshow-and-windows-media"></a>DirectShow 和 Windows Media

除了單獨使用 Windows Media 格式 SDK 之外，應用程式也可以使用 Microsoft® DirectShow®串流架構來讀取和寫入 Windows Media 內容，如下列各節所述。



| 區段                                                                                   | 描述                                                                                                                                 |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [關於 DirectShow](about-directshow.md)                                                  | 描述 DirectShow 的一般術語，並告訴您要在哪裡取得更多相關資訊。                                                     |
| [為何要使用 DirectShow？](why-use-directshow.md)                                             | 描述 DirectShow 如何簡化建立和播放 Windows Media 內容的特定工作。                              |
| [在 DirectShow 中讀取 ASF 檔案](reading-asf-files-in-directshow.md)                    | 說明如何使用 DirectShow 播放 ASF 檔案。                                                                                           |
| [在 DirectShow 中建立 ASF 檔案](creating-asf-files-in-directshow.md)                  | 說明如何使用 DirectShow 建立 ASF 檔案。                                                                                         |
| [\_DirectShow 中的 WMT 狀態事件通知](wmt-status-notification-in-directshow.md) | 描述 ASF 讀取器和 ASF 寫入器篩選器會處理哪些 **WMT \_ 狀態** 事件，以及應用程式如何接收這些事件。 |
| [DirectShow 中的 DRM 支援](drm-support-in-directshow.md)                                | 說明如何透過 DirectShow 讀取和寫入受 DRM 保護的檔案。                                                                     |
| [DirectShow QASF 參考](directshow-qasf-reference.md)                                | 包含支援 Windows Media 之 DirectShow 元件的參考檔。                                              |



 

SDK 中的三個範例應用程式說明如何使用 DirectShow： DSCopy、DSPlay 和 DSSeekFM。 如需詳細資訊，請參閱 [範例應用程式](sample-applications.md)。

> [!Note]  
> 使用此 SDK 所含 QASF 元件的應用程式需要在 Windows®2000、Windows 98 和 Windows 95 系統上安裝 Microsoft DirectX®8.1 或更新版本的 SDK 執行時間。 具體而言，在 DirectShow 篩選圖形中裝載 Windows Media 編解碼器的 SQL-DMO 包裝函式篩選器需要此執行時間。

 

 

 




