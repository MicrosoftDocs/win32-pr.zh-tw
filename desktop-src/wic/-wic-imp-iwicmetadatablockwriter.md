---
description: 執行 IWICMetadataBlockWriter
ms.assetid: 31824f21-04b1-45ca-adfa-15fd348e14a1
title: 執行 IWICMetadataBlockWriter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62044ce9695a45a8fe052d67479158aa9e4baf6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104514173"
---
# <a name="implementing-iwicmetadatablockwriter"></a>執行 IWICMetadataBlockWriter

## <a name="iwicmetadatablockwriter"></a>IWICMetadataBlockWriter

-   [InitializeFromBlockReader](#initializefromblockreader)
-   [GetWriterByIndex](#getwriterbyindex)
-   [AddWriter](#addwriter)
-   [SetWriterByIndex](#setwriterbyindex)
-   [RemoveWriterByIndex](#removewriterbyindex)

框架層級編碼類別會執行這個介面，以公開所有中繼資料區塊，並為每個區塊要求適當的中繼資料寫入器。 如果您的影像格式支援全域中繼資料，在任何個別的框架之外，您也應該在容器層級編碼器類別上執行此介面。 如需元資料處理程式的更詳細討論，請參閱有關如何執行 WIC-Enabled 的解碼器一節中的 [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) 一節。

``` syntax
interface IWICMetadataBlockWriter : IWICMetadataBlockReader
{
   // All methods required
   HRESULT InitializeFromBlockReader ( IWICMetadataBlockReader *pIMDBlockReader );
   HRESULT GetWriterByIndex ( UINT nIndex, IWICMetadataWriter **ppIMetadataWriter );
   HRESULT AddWriter (IWICMetadataWriter *pIMetadataWriter );
   HRESULT SetWriterByIndex ( UINT nIndex, IWICMetadataWriter *pIMetadataWriter );
   HRESULT RemoveWriterByIndex ( UINT nIndex );
}
```

### <a name="initializefromblockreader"></a>InitializeFromBlockReader

[**InitializeFromBlockReader**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-initializefromblockreader) 會使用 [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) 來初始化區塊寫入器。 您可以從解碼映射的解碼器取得 **IWICMetadataBlockReader** 。


```C++
UINT blockCount = 0;
IWICMetadataReader* pMetadataReader = NULL;
IWICMetadataWriter** ppMetadataWriter = NULL;
HRESULT hr;

hr = m_pBlockReader->GetCount(&blockCount);
ppMetadataWriter = IWICMetadataWriter*[blockCount];

for (UINT x=0; x < blockCount; x++)
{
   hr = m_pBlockReader->GetReaderByIndex(&pMetadataReader);
   hr = m_pComponentFactory->CreateMetadataWriterFromReader(
         pMetadataReader, NULL, &ppMetadataWriter[x]);
}
```



由於使用 [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)初始化 [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter)會將 **IWICMetadataBlockReader** 物件所公開之每個中繼資料讀取器的中繼資料寫入器具現化，因此應用程式不需要明確要求每個中繼資料區塊的寫入器。

### <a name="getwriterbyindex"></a>GetWriterByIndex

[**GetWriterByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-getwriterbyindex) 會傳回第 n 個中繼資料區塊的 [**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter) 物件，其中 n 是在 *nIndex* 參數中傳遞的值。 如果沒有任何已註冊的中繼資料寫入器可處理第 n 個區塊中的元資料類型，則元件 factory 會傳回未知的元資料處理程式，此處理程式會將中繼資料區塊視為二進位大型物件 (BLOB) 。 它會將它序列化為位資料流程，而不會嘗試加以剖析。

### <a name="addwriter"></a>AddWriter

[**AddWriter**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-addwriter) 可讓呼叫者加入新的中繼資料寫入器。 如果應用程式想要加入的中繼資料，與任何現有的中繼資料區塊不同，則這是必要的。 例如，應用程式可能會想要新增一些 XMP 中繼資料。 如果沒有任何現有的 XMP 中繼資料區塊，則應用程式必須具現化 XMP 中繼資料寫入器，並使用 **AddWriter** 方法將它包含在中繼資料寫入器的集合中。

### <a name="setwriterbyindex"></a>SetWriterByIndex

[**SetWriterByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-setwriterbyindex) 是用來在集合中的特定索引處加入中繼資料寫入器。 如果中繼資料寫入器目前存在於該索引中，則新的寫入器應該取代它。

### <a name="removewriterbyindex"></a>RemoveWriterByIndex

[**RemoveWriterByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-removewriterbyindex) 是用來從集合中移除中繼資料寫入器。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[執行 IWICBitmapFrameEncode](-wic-imp-iwicbitmapframeencode.md)
</dt> <dt>

[編解碼器安裝和註冊](-wic-codecinstallandreg.md)
</dt> <dt>

[如何撰寫 WIC-Enabled 編解碼器](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows 影像處理元件總覽](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



