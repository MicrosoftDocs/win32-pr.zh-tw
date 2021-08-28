---
description: 編碼
ms.assetid: 501e63bf-26ef-42fb-b181-f1a8b26c122c
title: '編碼 (Windows 影像處理元件) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0b3d6eef499379bbdc668e70d5d0ec4326b390372da910934a6e7c7f547d177
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964647"
---
# <a name="encoding-windows-imaging-component"></a>編碼 (Windows 影像處理元件) 

編碼器作者必須執行下列動作：

-   執行 [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) 和 [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) 介面。
-   在畫面格編碼器上執行 [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) 。 如果編解碼器支援容器層級的中繼資料，則必須在容器層級編碼器以及框架編碼器上實作為此介面。
-   如果容器格式隱含地包含任何必要的中繼資料區塊，請為每個這類區塊具現化中繼資料寫入器。 例如，TIFF 格式需要介面裝置 (每個框架的 IFD) ，因此必須一律公開 IFD 寫入器。
-   執行管理中繼資料寫入器集合的支援。 區塊寫入器會針對可編碼的中繼資料區塊類型，管理任何順序需求或容器限制。 區塊寫入器必須確認是否有任何新的中繼資料寫入器可內嵌在容器格式內。
-   編碼影像資料流程時，請呼叫 [**WICSerializeMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicserializemetadatacontent) 將每個中繼資料寫入器的內容序列化為數據流。 如果中繼資料區塊包含 "critical" 中繼資料，則編碼器必須先設定重要的中繼資料專案，然後再要求中繼資料寫入器序列化內容。
-   檢查是否有任何未知的元資料處理程式，以確保不會有多餘的中繼資料區塊。 這點很重要，因為在解碼或編碼案例中保留中繼資料時，未知的區塊可能是強制中繼資料區塊的重複項。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[Windows映射處理元件總覽](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[相機原始影像格式的 WIC 指導方針](-wic-rawguidelines.md)
</dt> <dt>

[如何撰寫 WIC-Enabled 編解碼器](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



