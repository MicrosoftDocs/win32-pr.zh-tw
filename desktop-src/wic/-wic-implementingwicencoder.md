---
description: 執行 WIC-Enabled 編碼器
ms.assetid: 9c1a4fa4-30b9-445f-8aee-46711355ace7
title: 執行 WIC-Enabled 編碼器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6e65f969ba7c65e6860009b2fc998024d358301
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193712"
---
# <a name="implementing-a-wic-enabled-encoder"></a>執行 WIC-Enabled 編碼器

## <a name="introduction"></a>簡介

執行 Windows 影像處理元件 (WIC) 編碼器需要撰寫兩個類別，也就是執行 WIC 解碼器的情況。 這些類別上的介面直接對應至 Windows 影像處理元件運作方式的 [編碼](-wic-howwicworks.md) 區段中所述的編碼器責任。

其中一個類別會提供容器層級的服務，並管理容器內個別影像框架的序列化。 這個類別會實 [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) 介面。 如果您的影像格式支援容器層級的中繼資料，您也必須在這個類別上執行 [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) 介面。

另一個類別會提供框架層級的服務，並針對容器中的每個框架執行影像位的實際編碼。 它也會逐一查看每個框架的中繼資料區塊，並要求適當的中繼資料寫入器來序列化區塊。 這個類別會實 **IWICBitmapFrameEncode** 介面和 [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) 介面。 此類別應該具有在具現化時，容器層級類別初始化的 IStream 成員， **Commit** 方法會將框架資料序列化至該成員。

在某些情況下（例如 raw 格式），編解碼器作者可能不希望應用程式能夠編碼或重新編碼為原始格式，因為原始檔案的目的是要包含與相機完全相同的感應器資料。 在編解碼器作者不想啟用編碼的情況下，仍必須執行基本編碼器，才可啟用新增中繼資料。 在這種情況下，編碼器只需要支援寫入中繼資料所需的方法，並可從解碼器複製不變的影像位。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**參考**
</dt> <dt>

[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)
</dt> <dt>

**概念**
</dt> <dt>

[執行 IWICDevelopRaw](-wic-imp-iwicdevelopraw.md)
</dt> <dt>

[編碼器介面](-wic-encoderinterfaces.md)
</dt> <dt>

[如何撰寫 WIC-Enabled 編解碼器](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows 影像處理元件總覽](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



