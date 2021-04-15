---
title: 關於影片壓縮管理員
description: 關於影片壓縮管理員
ms.assetid: 2a5ebc95-3ee8-4145-b2c5-512d82e49c6d
keywords:
- 'Windows 多媒體、視訊壓縮管理員 (BC-VCM-LVM-HYPERV) '
- '多媒體、視訊壓縮管理員 (BC-VCM-LVM-HYPERV) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6841446a5a0f22b8c05c2419448e65b035f90703
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104463060"
---
# <a name="about-the-video-compression-manager"></a>關於影片壓縮管理員

通常，可安裝的壓縮機會使用儲存在音訊中的影片影像資料（ (AVI) 檔案的影片）來運作。 本總覽說明用來透過 BC-VCM-LVM-HYPERV 存取可安裝壓縮機的程式設計技術，並涵蓋下列主題：

-   適用于 Windows 架構的 BC-VCM-LVM-HYPERV 和影片
-   從應用程式壓縮和解壓縮映射資料
-   使用 BC-VCM-LVM-HYPERV 轉譯器從您的應用程式中繪製資料
-   BC-VCM-LVM-HYPERV 函式和結構

閱讀此總覽之前，您應該先熟悉 Microsoft Win32 圖形服務。 尤其是 [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) 和 [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader)等點陣圖和點陣圖相關結構會由 bc-vcm-lvm-hyperv 廣泛使用。 如需 **BITMAPINFO** 和 **BITMAPINFOHEADER** 結構的詳細資訊，請參閱 [點陣圖](/previous-versions//ms532349(v=vs.85))。

> [!Note]  
> 音訊壓縮管理員 (的) 提供音訊壓縮和解壓縮驅動程式的系統層級支援。 如需音訊壓縮服務的說明，請參閱 [音訊壓縮管理員](audio-compression-manager.md)。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[影片壓縮管理員](video-compression-manager.md)
</dt> </dl>

 

 