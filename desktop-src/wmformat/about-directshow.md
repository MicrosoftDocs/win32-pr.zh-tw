---
title: '關於 DirectShow (Windows Media Format 11 SDK) '
description: 關於 DirectShow
ms.assetid: 1a0b68c7-9444-4389-8d81-dc734e95634d
keywords:
- Windows Media Format SDK、DirectShow
- Advanced Systems Format (ASF) 、DirectShow
- ASF (Advanced Systems Format) ，DirectShow
- DirectShow，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd77507643edb220bc71a029779c88fe56760eae
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104024477"
---
# <a name="about-directshow-windows-media-format-11-sdk"></a>關於 DirectShow (Windows Media Format 11 SDK) 

DirectShow 是適用于 Windows 平臺的高階、模組化、可擴充的資料串流架構。 它提供基礎軟體元件和應用程式開發介面， (Api) 適用于現今市場上的各種數位音訊和影片應用程式。 DirectShow 可作為 Microsoft DirectX 軟體發展工具組的一部分。 若要深入瞭解 DirectShow，請參閱 Microsoft Platform SDK。

在 DirectShow 中，所有資料串流元件都稱為 *篩選*。 篩選器可能代表硬體裝置、軟體編碼器或編碼器、音訊或影片轉譯器，或任何音訊影片處理功能。 為了讓 DirectShow 型應用程式能夠讀取和寫入 Windows Media 格式內容（包括受數位 Rights Management (DRM) 保護的內容），Microsoft 提供兩個篩選器來封裝 Windows Media Format SDK 的部分。 這些是 [WM Asf 讀取器](wm-asf-reader-filter.md) 和 [Wm asf 寫入器](wm-asf-writer-filter.md)。 這些篩選器和它們公開的介面統稱為 QASF 元件，在封裝的 DLL 之後也稱為這些元件。  (Q 代表 Quartz，這是一種 DirectShow 的早期程式碼名稱 ) 

> [!Note]  
> 透過 DirectShow QASF 元件使用 Windows Media 音訊和影片9系列編解碼器需要 Microsoft Windows Millennium Edition 或更新版本，或 DirectX 8.0 或更新版本。

 

下圖顯示用來播放 Windows Media 視訊檔案的 DirectShow 篩選圖形。

![windows media 影片播放圖表](images/wmv-wmasfreader.png)

[WM ASF 讀取器](wm-asf-reader-filter.md)是 QASF 元件，而元件是) 中裝載的 Windows MEDIA 格式 SDK 元件， (QASF 元件，而轉譯器為 DirectShow 元件。

 

 




