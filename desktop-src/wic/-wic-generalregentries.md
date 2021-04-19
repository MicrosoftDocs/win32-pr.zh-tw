---
description: 一般登錄專案
ms.assetid: 6a140c7f-df8c-4a8e-9e4d-dbb38901e14f
title: 一般登錄專案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d7c3514adcc0aeaaf9adadd2b71dfdffcd8d408
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978224"
---
# <a name="general-registry-entries"></a>一般登錄專案


下列登錄專案必須分別針對解碼器和編碼器進行：

```
HKEY_CLASSES_ROOT
   CLSID
      {Your Encoder/Decoder CLSID}
         Author = Author's Name
         Description = Your Codec Description
         DeviceManufacturer = Manufacturer's Name
         DeviceModels = Device,Device
         FriendlyName = Codec Friendly Name
         Date = mm-dd-yyyy
         Vendor = {GUID_Vendor}
         ContainerFormat = {GUID_ContainerFormat}
         Version = Major.Minor.Build.Number
         SpecVersion = Major.Minor.Build.Number
         MimeTypes = Your Mime Type
         SupportAnimation = 0|1
         SupportChromakey = 0|1
         SupportLossless = 0|1
         SupportMultiframe = 0|1
         Formats
            {Supported PixelFormat GUID 1}
            {Supported PixelFormat GUID ...}
            {Supported PixelFormat GUID N}
         ArbitrationPriority  = 0-10
```

FriendlyName、VendorGUID、ContainerFormat、Mimetype、FileExtensions 和格式專案都是必要專案。 所有其他專案都是選擇性的。

請注意，DeviceManufacturer 和 DeviceModels 專案是原始編解碼器特有的，而且是指編解碼器適用的攝影機製造商和相機型號。 規格版本是編解碼器符合的映射格式規格版本。 格式專案會指定編解碼器所支援的像素格式。 編解碼器可支援一個以上的像素格式。 在這種情況下，您會在 HKEY \_ 類別的 \_ 根 \\ CLSID \\ {編碼器/解碼器 clsid} \\ 格式下輸入多個索引鍵。

## <a name="arbitrationpriority"></a>ArbitrationPriority

從 Windows 8 開始，ArbitrationPriority 是新的登錄專案。 有效的值為0到10。 當 ArbitrationPriority 索引鍵存在時，此機碼的值會指示 WIC 將相關編解碼器的優先順序設定為較低 ArbitrationPriority 值的任何其他編解碼器後方。 這項評估會在現有的 WIC 編解碼器仲裁發生之前發生，並確保相關聯的編解碼器會優先于任何競爭的編解碼器，即使它是一樣或更有能力。 登錄中未定義明確 ArbitrationPriority 值的任何編解碼器都會預設為優先權0。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[編解碼器安裝和註冊](-wic-codecinstallandreg.md)
</dt> <dt>

[編碼器特定的登錄專案](-wic-encoderregentries.md)
</dt> <dt>

[如何撰寫 WIC-Enabled 編解碼器](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows 影像處理元件總覽](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[**Windows 影像處理元件的運作方式：編解碼器探索和仲裁**](-wic-howwicworks.md)
</dt> </dl>

 

 



