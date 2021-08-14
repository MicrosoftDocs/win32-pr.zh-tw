---
description: Encoder-Specific 登錄專案
ms.assetid: bbb78d70-bd3e-4d5a-ba59-2e17d2d1cf30
title: Encoder-Specific 登錄專案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83d5d91d917be3940bcece4bed7c224e0f281dbb1cade5d0dc2c25872f89af93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118711227"
---
# <a name="encoder-specific-registry-entries"></a>Encoder-Specific 登錄專案


除了上述針對編碼器所列的專案之外，您還必須在 Windows 影像處理元件 (WIC) 編碼器的類別下註冊您的編碼器，讓探索引擎可以找到它。 您可以藉由建立下列登錄專案來執行此動作。 下列專案中的第一個 GUID 是 WICBitmapEncoders)  (CATID 的分類識別碼。

```
HKEY_CLASSES_ROOT
   CLSID
      {AC757296-3522-4E11-9862-C17BE5A1767E}
         Instance
            {Encoder CLSID}
               CLSID = {Encoder CLSID}
               FriendlyName = {Name of Encoder}
```

## <a name="registering-a-container-format-with-metadata-writers"></a>使用中繼資料寫入器註冊容器格式

如果您為編解碼器建立新的容器格式，則也必須建立登錄專案，以支援您影像中中繼資料區塊的中繼資料寫入器。 下列專案必須根據您的容器格式所支援的每個元資料格式，在中繼資料寫入器 (CLSID) 的類別識別碼底下建立。 如果您的編解碼器使用標記的影像檔案格式 (TIFF) 容器，則這項資訊已在登錄中，因此您不需要建立這些專案。

```
HKEY_CLASSES_ROOT
   CLSID
      {Metadata Writer CLSID}
         Containers
            {Container Format GUID}
               WritePosition = Offset relative to its container
               WriteHeader = Pattern used for metadata header
               WriteOffset = Offset from beginning of header
```

如果您使用 TIFF 樣式或 JPEG 樣式的容器格式，則必須在容器與該容器格式之間註冊關聯。 如需詳細資訊，請參閱[整合 Windows 的簡介影像中心和 Windows 檔案總管](-wic-integrationregentries.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[一般登錄專案](-wic-generalregentries.md)
</dt> <dt>

[編碼器特定的登錄專案](-wic-decoderregentries.md)
</dt> <dt>

[如何撰寫 WIC-Enabled 編解碼器](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows映射處理元件總覽](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



