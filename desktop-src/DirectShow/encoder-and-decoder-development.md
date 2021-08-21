---
description: 編碼器和解碼器開發
ms.assetid: 075aaf0f-63c6-4286-966e-fdc72d0acb6e
title: 編碼器和解碼器開發
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8619225f5d4df9596523724259eb4eee1a9b3bb4c978a3fc400156bc9ee56a4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015816"
---
# <a name="encoder-and-decoder-development"></a>編碼器和解碼器開發

本章節包含 DirectShow 的編碼器和解碼器開發相關文章。 這些主題與應用程式開發人員無關。

支援 DirectX Video 加速 (VA) 的軟體解碼器必須實作為 DirectShow 複製轉換篩選。 如果此解碼器不支援 directx VA，也可以將它實作為 directx 媒體物件 (DMO) 。 連接至影片轉譯器的解碼器不應該實作為就地篩選，因為這樣會導致效能大幅降低。 如需如何撰寫複製轉換篩選的相關資訊，請參閱 [寫入轉換篩選](writing-transform-filters.md)。

軟體編碼器可以實作為轉換篩選或 DMOs。 編碼器不會使用 DirectX VA，因為 DirectX VA 目前僅用於解壓縮。 本節所述的編碼器 API 規格與硬體和軟體編碼器有關。

本節包含下列主題：

-   [編碼器 API](encoder-api.md)
-   [解碼器介面和規格](decoder-interfaces-and-specifications.md)
-   [Windows Media Center Edition 的解碼器設定](decoder-settings-for-windows-media-center-edition.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[針對 DirectShow 濾波器開發人員使用 VMR](using-the-vmr-for-directshow-filter-developers.md)
</dt> </dl>

 

 



