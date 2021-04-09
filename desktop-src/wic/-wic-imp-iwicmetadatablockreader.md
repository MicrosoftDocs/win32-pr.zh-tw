---
description: 執行 IWICMetadataBlockReader
ms.assetid: 80ad8e20-a9d4-4503-94ba-1b7699e36111
title: 執行 IWICMetadataBlockReader
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55bfe53e87dae52d004fa90d1104fb60f252085d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849506"
---
# <a name="implementing-iwicmetadatablockreader"></a>執行 IWICMetadataBlockReader

## <a name="iwicmetadatablockreader"></a>IWICMetadataBlockReader

多個中繼資料區塊通常存在於影像中，每個區塊都會以不同的格式公開不同類型的資訊。 在 Windows 影像處理元件 (WIC) 模型中，元資料處理程式是在執行時間可搜尋的相異元件，例如，其為解碼器。 每個元資料格式都有個別的處理常式，而且每個元資料處理程式都可以搭配任何支援它所處理之元資料格式的影像格式使用。 因此，如果您的影像格式支援 EXIF、XMP、IPTC 或其他格式，您可以利用 WIC 隨附的這些格式的標準元資料處理程式，而不需要自行撰寫。 當然，如果您建立新的元資料格式，就必須撰寫它的元資料處理程式，它會在執行時間探索並叫用，就像標準的格式一樣。

> [!Note]  
> 如果您的影像格式是根據標記的影像檔案格式 (TIFF) 或 JPEG 容器，除非您) 建立新的或專屬的元資料格式，否則您不需要撰寫任何元資料處理程式 (。 在 TIFF 和 JPEG 容器中，中繼資料的區塊位於 IFDs 內，而每個容器都有不同的 IFD 結構。 WIC 提供這兩種容器格式的 IFD 處理常式，可流覽 IFD 結構並委派給標準元資料處理程式來存取它們內的中繼資料。 因此，如果您的映射格式是以其中一個容器為基礎，您就可以自動利用 WIC IFD 處理常式。 但是，如果您擁有專屬的容器格式，且其擁有專屬的最上層元資料結構，則必須撰寫可流覽該最上層結構並委派給適當元資料處理程式的處理常式，就像 IFD 處理常式一樣 ) 

 

同樣地，WIC 也為應用程式提供了一層抽象概念，讓它們能夠透過一組一致的介面，以相同的方式處理所有影像格式，WIC 為編解碼器作者提供了元資料格式的抽象層。 如先前所述，編解碼器作者通常不需要直接使用影像中可能存在的各種元資料格式。 不過，每個編解碼器作者都必須負責提供方法來列舉中繼資料的區塊，以便探索並針對每個區塊來具現化適當的元資料處理程式。

您必須在您的框架層級解碼類別上執行這個介面。 如果您的影像格式在任何個別影像框架之外公開全域中繼資料，您可能也需要在容器層級的解碼器類別上執行它。

``` syntax
interface IWICMetadataBlockReader : IUnknown
{
   // All methods required
   HRESULT GetContainerFormat ( GUID *pguidContainerFormat );
   HRESULT GetCount ( UINT *pcCount );
   HRESULT GetEnumerator ( IEnumUnknown **ppIEnumMetadata );
   HRESULT GetReaderByIndex ( UINT nIndex, IWICMetadataReader **ppIMetadataReader );
}
```

-   [GetContainerFormat](#getcontainerformat)
-   [GetCount](#getcount)
-   [GetEnumerator](#getenumerator)
-   [GetReaderByIndex](#getreaderbyindex)

### <a name="getcontainerformat"></a>GetContainerFormat

[**GetContainerFormat**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcontainerformat)與 [執行 IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md)的 [GetContainerFormat](-wic-imp-iwicbitmapdecoder.md)方法相同。

### <a name="getcount"></a>GetCount

[**GetCount**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcount) 會傳回與框架相關聯的最上層中繼資料區塊數目。

### <a name="getenumerator"></a>GetEnumerator

[**GetEnumerator**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getenumerator) 會傳回一個列舉值，呼叫者可以用來列舉框架中的中繼資料區塊，並讀取其中繼資料。 若要執行這個方法，您必須為每個中繼資料區塊建立中繼資料讀取器，並執行列舉中繼資料讀取器集合的列舉物件。 列舉物件必須執行 [IEnumUnknown](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown) ，因此當您在 *ppIEnumMetadata* 參數中傳回它時，可以將它轉換成 IEnumUnknown。

在實作為列舉物件時，您可以在第一次建立 [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) 物件時或第一次建立列舉物件時建立所有中繼資料讀取器，也可以在 [IEnumUnknown：： Next](/windows/win32/api/objidlbase/nf-objidlbase-ienumunknown-next) 方法的執行中延遲建立。 在許多情況下，更有效率地建立它們，但在下列範例中，區塊讀取器全都是在用來節省空間的函式中建立的。


```C++
public class MetadataReaderEnumerator : public IEnumUnknown
{
   UINT m_current;
   UINT m_blockCount;
   IWICMetadataReader** m_ppMetadataReader;
   IStream* m_pStream;

   MetadataReaderEnumerator() 
   {
       // Set m_blockCount to the number of metadata blocks in the frame. 
      ...
      m_ppMetadataReader = IWICMetadataReader*[m_blockCount];
       m_current = 0;

      for (UINT x=0; x < m_blockCount; x++) 
      {
         // Find the position in the file where the xth
         // block of metadata lives and seek m_piStream 
         // to that position.
         ...

         m_pComponentFactory->CreateMetadataReaderFromContainer(
            GUID_ContainerFormatTiff,
                        NULL,
                        WICPersistOptions.WICPersistOptionsDefault | 
            WICMetadataCreationOptions.WICMetadataCreationDefault, 
                        m_pStream, &m_ppMetadataReader[x]);
        }
    }

    // Implementation of IEnumUnknown and IUnknown interfaces
    ...
}
```



若要建立中繼資料讀取器，請使用 [**CreateMetadataReaderFromContainer**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createmetadatareaderfromcontainer) 方法。 叫用這個方法時，您會在 *guidContainerFormat* 參數中傳入容器格式的 GUID。 如果您有針對中繼資料讀取器的廠商喜好設定，就可以在 *pGuidVendor* 參數中傳遞慣用廠商的 GUID。 例如，如果您的公司寫入元資料處理程式，而您想要使用自己的（如果有的話），您可以傳入廠商的 GUID。 在大部分的情況下，您只會傳遞 **Null**，讓系統選取適當的中繼資料讀取器。 如果您要求特定廠商，而該廠商已在電腦上安裝中繼資料讀取器，WIC 將會傳回該廠商的讀者。 但是，如果要求的廠商未在電腦上安裝中繼資料讀取器，而且有適當的中繼資料讀取器可供使用，即使該讀取器不是來自慣用的廠商也會傳回。 如果電腦上沒有任何中繼資料讀取器可用於區塊中的元資料類型，則元件 factory 會傳回未知的元資料處理程式，此處理程式會將中繼資料的區塊視為二進位大型物件 (BLOB) ，而且會從檔案還原序列化中繼資料的區塊，而不會嘗試進行剖析。

針對 *>dwoptions* 參數，請使用適當的 [**WICMetadataCreationOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicmetadatacreationoptions)，在適當的 [**WICPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions)之間執行 OR 運算。 **WICPersistOptions** 描述容器的配置方式。預設值為位元組由小到大。

``` syntax
enum WICPersistOptions
{   
   WICPersistOptionDefault,
   WICPersistOptionLittleEndian,
   WICPersistOptionBigEndian,
   WICPersistOptionStrictFormat,
   WICPersistOptionNoCacheStream,
   WICPersistOptionPreferUTF8
};
```

[**WICMetadataCreationOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicmetadatacreationoptions)指定如果在可讀取特定區塊之元資料格式的電腦上找不到任何中繼資料讀取器，是否要取回 UnknownMetadataHandler。 **WICMetadataCreationAllowUnknown** 是預設值，您應該一律允許建立 UnknownMetadtataHandler。 UnknownMetadataHandler 會將無法辨識的中繼資料視為 BLOB。 它無法剖析它，但它會將它寫出到資料流程中做為 BLOB，並在編碼期間將資料寫回至資料流程時保持不變。 這可讓您安全地針對未隨附于系統的專屬中繼資料或元資料格式建立元資料處理程式。 因為中繼資料會原封不動地保留，即使電腦上沒有任何處理程式可辨識它，當適當的元資料處理程式稍後安裝時，中繼資料仍會存在且可供讀取。 如果您不允許建立 UnknownMetadataHandler，替代方法會捨棄或覆寫無法辨識的中繼資料。 這是一種資料遺失的形式。

> [!Note]  
> 如果您為專屬中繼資料撰寫自己的元資料處理程式，您永遠不應該包含中繼資料區塊本身以外的任何參考。 雖然 UnknownMetadataHandler 會保持中繼資料不變，但在編輯檔案時就會移動中繼資料，而在此情況下，任何對其本身區塊以外之任何參考的參考將不再有效。

 

``` syntax
enum WICMetadataCreationOptions
{
   WICMetadataCreationDefault = 0x00000000,
   WICMetadataCreationAllowUnknown = WICMetadataCreationDefault,
   WICMetadataCreationFailUnknown = 0x00010000,
   WICMetadataCreationMask = 0xFFFF0000
};
```

*PIStream* 參數是您正在解碼的實際資料流程。 傳入串流之前，您應該先搜尋您要要求讀取器的中繼資料區塊的開頭。 在 [IStream](/windows/desktop/api/objidl/nn-objidl-istream) 的目前位置，中繼資料區塊的適當中繼資料讀取器會在 *ppiReader* 參數中傳回。

### <a name="getreaderbyindex"></a>GetReaderByIndex

[**GetReaderByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getreaderbyindex) 會傳回集合中要求之索引的中繼資料讀取器。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**參考**
</dt> <dt>

[**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)
</dt> <dt>

**概念**
</dt> <dt>

[執行 IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md)
</dt> <dt>

[執行 IWICBitmapSourceTransform](-wic-imp-iwicbitmapsourcetransform.md)
</dt> <dt>

[如何撰寫 WIC-Enabled 編解碼器](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows 影像處理元件總覽](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 
