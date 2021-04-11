---
description: '介紹 (適用于相機原始影像格式的 WIC 指導方針) '
ms.assetid: 3c588386-1d4d-4ee0-b633-bfc94ca751ea
title: '介紹 (適用于相機原始影像格式的 WIC 指導方針) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec6ee2607326afe289e0a3e54b254dcf581cbf86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194116"
---
# <a name="introduction-wic-guidelines-for-camera-raw-image-formats"></a>介紹 (適用于相機原始影像格式的 WIC 指導方針) 

Windows 影像處理元件 (WIC) 提供可延伸的架構，可用於處理影像和影像中繼資料。 WIC 讓軟體和硬體廠商能夠開發編解碼器，讓自己的映射格式可以取得與原生映射格式相同的平臺支援，例如標記的影像檔案格式 (TIFF) 、聯合攝影專家群組 (JPEG) 或 HD 相片。

WIC 針對所有影像處理提供單一且一致的介面集，不論影像格式為何。 因此，任何使用 WIC 的應用程式都會在安裝編解碼器時，立即收到新映射格式的自動支援。 WIC 也提供可延伸的中繼資料架構，讓應用程式可以將自己的專屬中繼資料直接讀取和寫入影像檔案，因此中繼資料永遠不會遺失或與影像分開。

WIC 包含在 Windows Presentation Foundation (WPF) 中，並內建于 Windows Vista 和更新版本的 Windows 版本。 它也可作為 Windows XP 的獨立可轉散發元件。

這些指導方針是設計來協助原始格式製造商開發 WIC 編解碼器。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[Windows 影像處理元件總覽](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[相機原始影像格式的 WIC 指導方針](-wic-rawguidelines.md)
</dt> <dt>

[如何撰寫 WIC-Enabled 編解碼器](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



