---
description: 在 Windows 影像處理元件 (wic) 平臺上建立編解碼器，可讓所有在 wic 上建立的應用程式都能針對您的映射格式取得相同的平臺支援，以供平臺隨附的通用映射格式使用。
ms.assetid: 4f25f0f4-246c-4cbd-bd11-d061dbc7de45
title: '結論 (如何撰寫 WIC-Enabled 編解碼器) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5288438ea518e1776562b288184067df6d82c326eb6786b163f20e90c6febc05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118205819"
---
# <a name="conclusion-how-to-write-a-wic-enabled-codec"></a>結論 (如何撰寫 WIC-Enabled 編解碼器) 

在 Windows 影像處理元件 (wic) 平臺上建立編解碼器，可讓所有在 wic 上建立的應用程式都能針對您的映射格式取得相同的平臺支援，以供平臺隨附的通用映射格式使用。 它也可讓 Windows Vista 影像中心、Windows 檔案總管和相片檢視器使用您提供的解碼器，以您的格式顯示影像的縮圖和預覽。 針對原始格式，它可讓更精密的影像處理應用程式充分利用您的解碼器原始處理功能。 根據您支援的編碼器選項，您也可以公開編碼器的獨特功能，讓應用程式能夠充分利用影像格式的先進功能。

開發已啟用 WIC 的編解碼器需要您執行一些新的介面。 在許多情況下，您可以為現有的編解碼器撰寫可執行這些介面的包裝函式。 當您安裝編解碼器時，必須建立一些登錄專案，讓 WIC 平臺可以探索編解碼器，並將其與適當的元資料處理程式產生關聯。 您也必須叫用 API，以清除任何預設 (空白) 縮圖的縮圖快取，這些縮圖先前可能已與您格式的影像相關聯。 如果您想要的話，可以啟用 Windows Vista 影像中心，在影像中心遇到具有您副檔名的映射時，為使用者提供下載編解碼器的連結。 若要這樣做，您必須為 Microsoft 提供您的編解碼器副檔名的相關資訊，以及下載網站的 URL。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[編解碼器安裝和註冊](-wic-codecinstallandreg.md)
</dt> <dt>

[如何撰寫 WIC-Enabled 編解碼器](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows映射處理元件總覽](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



