---
description: 編碼器和解碼器開發
ms.assetid: 075aaf0f-63c6-4286-966e-fdc72d0acb6e
title: 編碼器和解碼器開發
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbe45fc726338e33205831959986178f4527673a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109204"
---
# <a name="encoder-and-decoder-development"></a>編碼器和解碼器開發

本章節包含適用于 DirectShow 的編碼器和解碼器開發的相關文章。 這些主題與應用程式開發人員無關。

支援 DirectX Video 加速 (VA) 的軟體解碼器必須實作為 DirectShow 複製轉換篩選。 如果此解碼器不支援 DirectX VA，也可以將它實作為 DirectX 媒體物件 (的) 。 連接至影片轉譯器的解碼器不應該實作為就地篩選，因為這樣會導致效能大幅降低。 如需如何撰寫複製轉換篩選的相關資訊，請參閱 [寫入轉換篩選](writing-transform-filters.md)。

軟體編碼器可以實作為轉換篩選或 DMOs。 編碼器不會使用 DirectX VA，因為 DirectX VA 目前僅用於解壓縮。 本節所述的編碼器 API 規格與硬體和軟體編碼器有關。

本節包含下列主題：

-   [編碼器 API](encoder-api.md)
-   [解碼器介面和規格](decoder-interfaces-and-specifications.md)
-   [Windows Media Center Edition 的解碼器設定](decoder-settings-for-windows-media-center-edition.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 VMR 來進行 DirectShow 篩選器開發人員](using-the-vmr-for-directshow-filter-developers.md)
</dt> </dl>

 

 



