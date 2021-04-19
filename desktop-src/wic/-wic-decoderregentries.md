---
description: Decoder-Specific 登錄專案
ms.assetid: 64ef260a-ed7f-4253-a644-bd3352b0ee41
title: Decoder-Specific 登錄專案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17485e7adca62abd31643d84d371a0002724ea9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980067"
---
# <a name="decoder-specific-registry-entries"></a>Decoder-Specific 登錄專案


除了所有編碼器和解碼器所需的登錄專案之外，還需要下列登錄專案，特別是針對該解碼器。

這些專案會將您的解碼器註冊在 Windows 影像處理元件 (WIC) 解碼器的類別中。 這些專案中的第一個 GUID 是 [**WICBitmapDecoders**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder))  (CATID 的分類識別碼。

```
HKEY_CLASSES_ROOT
   CLSID
      {7ED96837-96F0-4812-B211-F13C24117ED3}
         Instance
            {Decoder CLSID}
               CLSID = {Decoder CLSID}
               FriendlyName = {Name of Decoder}
```

如同 Windows 影像處理元件運作方式的 [探索和仲裁](-wic-howwicworks.md) 一節中所述，在執行時間針對特定映射啟用適當的解碼器的機制，是以比對影像檔案中的識別模式與在解碼器登錄專案中指定的模式來進行。 若要啟用以執行時間探索的解碼器，您必須為映射格式註冊唯一的識別模式，如下所示。 除了 **EndOfStream** 專案之外，所有的登錄專案都是必要專案，這是選擇性的，如下表所述。

```
HKEY_CLASSES_ROOT
   CLSID
      {Decoder CLSID}
         Patterns
            {0}
               Position = Offset in block
               Length = Length of pattern
               Pattern = Pattern to match
               Mask = FF FF FF FF
               EndOfStream = 0|1
```



| 值       | 描述                                                                                                                                                                                                                                                                                                                     |
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 位置    | 可以在檔案中找到模式的位移。                                                                                                                                                                                                                                                                        |
| 長度      | 模式的長度。                                                                                                                                                                                                                                                                                                      |
| 模式     | 構成模式的實際位。 這些是在探索期間針對影像檔案中的識別模式比對的位。                                                                                                                                                                                |
| Mask        | 在模式中允許萬用字元值。 遮罩的套用方式是在模式和遮罩上執行邏輯 AND 運算。 在模式中，對應至遮罩中位（值為0）的任何位都會被忽略。                                                                                                       |
| EndOfStream | 識別模式的位移應從資料流程的結尾，而不是從開頭算起。 某些影像格式會將識別模式放在檔案結尾或附近。 由於預設是從開頭開始搜尋，除非您的模式接近檔案結尾，否則您可以省略此專案。 |



 

編解碼器可支援一個以上的識別模式。 在這種情況下，您會在 **HKEY \_ 類別的 \_ 根 \\ CLSID \\ {解碼器 clsid} \\ 模式** 下重複所有的金鑰，並在範例) 中使用 (0 的數位鍵來區別不同的模式。 您必須在每個模式的索引鍵下包含四個值。

## <a name="registering-a-container-format-with-metadata-readers"></a>使用中繼資料讀取器註冊容器格式

如果您為編解碼器建立新的容器格式，您也必須建立登錄專案，以支援針對影像中的中繼資料區塊探索中繼資料讀取器，就像您針對中繼資料寫入器所做的一樣。 您必須根據容器格式所支援的每個元資料格式，在中繼資料讀取器 (CLSID) 的類別識別碼底下建立下列專案。  (請注意，如果您的編解碼器使用標記的影像檔案格式 (TIFF) 容器，則這項資訊已在登錄中。 ) 

```
HKEY_CLASSES_ROOT
   CLSID
      {Metadata Reader CLSID}
         Containers
            {Container Format GUID}
               
                  Position = Offset relative to its container
                  Pattern = Pattern used for metadata header
                  Mask = FF FF FF FF
                  DataOffset = Offset from beginning of header
```

因為中繼資料讀取器的專案也用來進行探索，所以它們非常類似于「解碼器」的專案。 元件 factory 會使用這些專案來尋找您的容器所支援的中繼資料讀取器，並在您的 [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) 執行要求中繼資料讀取器時，選取適當的專案。



| 值      | 描述                                                                                                                                                                                                                                                                 |
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 位置   | 中繼資料區塊容器中可以找到中繼資料標頭的位移。 針對最上層的中繼資料區塊，這是檔案資料流程中的位移。 針對其他中繼資料區塊中嵌套的中繼資料區塊，它是相對於包含中繼資料區塊的位移。 |
| 模式    | 構成模式的實際位。 這些是在探索期間針對影像檔案中的識別模式比對的位。                                                                                                                            |
| Mask       | 中繼資料標頭通常是由元資料處理程式所定義。 您應該針對每個讀取器使用標準中繼資料標頭，除非基於某些原因，此模式在您的容器中必須有不同的格式。                                                          |
| DataOffset | 中繼資料標頭開頭的位移，實際的資料會從此處開始。 如果中繼資料不是位於標頭的特定位移，則可以省略此專案。                                                                            |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[編碼器特定的登錄專案](-wic-encoderregentries.md)
</dt> <dt>

[與 Windows 影像中心和 Windows 檔案總管整合](-wic-integrationregentries.md)
</dt> <dt>

[如何撰寫 WIC-Enabled 編解碼器](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows 影像處理元件總覽](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



