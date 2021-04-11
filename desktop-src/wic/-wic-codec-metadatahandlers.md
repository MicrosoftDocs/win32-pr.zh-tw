---
description: 本主題將介紹針對 Windows 影像處理元件 (WIC) （包括中繼資料讀取器和寫入器）建立自訂元資料處理程式的需求。
ms.assetid: 08f1872b-6e4d-44ee-abc7-48685e435acc
title: 中繼資料擴充性總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6576585f7f35628432504086695dd6c64091d3b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193563"
---
# <a name="metadata-extensibility-overview"></a>中繼資料擴充性總覽

本主題將介紹針對 Windows 影像處理元件 (WIC) （包括中繼資料讀取器和寫入器）建立自訂元資料處理程式的需求。 此外，也會討論擴充 WIC 執行時間元件探索以包含自訂元資料處理程式的需求。

本主題包含下列各節。

-   [先決條件](#prerequisites)
-   [簡介](#introduction)
-   [建立中繼資料讀取器](#creating-a-metadata-reader)
    -   [IWICMetadataReader 介面](#iwicmetadatareader-interface)
    -   [IWICPersistStream 介面](#iwicpersiststream-interface)
    -   [IWICStreamProvider 介面](#iwicstreamprovider-interface)
-   [建立中繼資料寫入器](#creating-a-metadata-writer)
    -   [IWICMetadataWriter 介面](#iwicmetadatawriter-interface)
    -   [IWICPersistStream 介面](#iwicpersiststream-interface)
    -   [IWICStreamProvider 介面](#iwicstreamprovider-interface)
-   [安裝和註冊元資料處理程式](#installing-and-registering-a-metadata-handler)
    -   [元資料處理程式登錄機碼](#metadata-handler-registry-keys)
    -   [中繼資料讀取器](#metadata-readers)
    -   [中繼資料寫入器](#metadata-writers)
    -   [簽署元資料處理程式](#signing-a-metadata-handler)
-   [特殊考慮](#special-considerations)
    -   [PROPVARIANTS](#propvariants)
    -   [8BIM 處理常式](#8bim-handlers)
-   [相關主題](#related-topics)

## <a name="prerequisites"></a>必要條件

若要瞭解本主題，您應該對 WIC、其元件和映射的中繼資料有深入的瞭解。 如需 WIC 中繼資料的詳細資訊，請參閱 [Wic 中繼資料總覽](-wic-about-metadata.md)。 如需 WIC 元件的詳細資訊，請參閱 [Windows 影像處理元件總覽](-wic-about-windows-imaging-codec.md)。

## <a name="introduction"></a>簡介

如 [WIC 中繼資料總覽](-wic-about-metadata.md)中所述，影像中通常會有多個中繼資料區塊，每個區塊都會以不同的元資料格式公開不同類型的資訊。 若要與內嵌于影像內的元資料格式互動，應用程式必須使用適當的元資料處理程式。 WIC 提供數個元資料處理程式 (中繼資料讀取器和寫入器，) 可讓您讀取和寫入特定類型的中繼資料，例如 Exif 或 XMP。

除了提供的原生處理常式之外，WIC 還提供 Api，可讓您建立新的元資料處理程式來參與 WIC 的執行時間元件探索。 這可讓使用 WIC 的應用程式讀取及寫入您的自訂元資料格式。

下列步驟可讓您的元資料處理程式參與 WIC 的執行時間中繼資料探索。

-   實 ([**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)) 的中繼資料讀取器處理常式類別，其會公開所需的 WIC 介面以讀取您的自訂元資料格式。 這可讓 WIC 型應用程式以讀取原生元資料格式的相同方式讀取您的元資料格式。
-   將中繼資料寫入器處理常式類別 (為公開必要的 WIC 介面以編碼自訂元資料格式的 [**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)) 。 這可讓 WIC 型應用程式將您的元資料格式序列化為支援的影像格式。
-   以數位方式簽署並註冊您的元資料處理程式。 這可讓您在執行時間探索元資料處理程式，方法是將登錄中的識別模式與內嵌在影像檔中的模式比對。

## <a name="creating-a-metadata-reader"></a>建立中繼資料讀取器

編解碼器內中繼資料區塊的主要存取是透過每個 WIC 編解碼器所實行的 [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) 介面。 此介面會列舉以影像格式內嵌的每個中繼資料區塊，以針對每個區塊探索並具現化適當的元資料處理程式。 WIC 無法辨識的中繼資料區塊會被視為未知，而且會定義為 GUID CLSID \_ WICUnknownMetadataReader。 若要讓 WIC 辨識您的元資料格式，您必須建立可執行三個介面的類別： [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)、 [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream)和 [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider)。

> [!Note]  
> 如果您的元資料格式具有可轉譯某些必要介面方法的限制，這類方法應該會傳回 WINCODEC \_ ERR \_ UNSUPPORTEDOPERATION。

 

### <a name="iwicmetadatareader-interface"></a>IWICMetadataReader 介面

建立中繼資料讀取器時，必須執行 [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader) 介面。 這個介面可讓您存取元資料格式之資料流程內的基礎中繼資料專案。

下列程式碼顯示 wincodecsdk .idl 檔中所定義之中繼資料讀取器介面的定義。

``` syntax
interface IWICMetadataReader : IUnknown
{
    HRESULT GetMetadataFormat(
        [out] GUID *pguidMetadataFormat
        );

    HRESULT GetMetadataHandlerInfo(
        [out] IWICMetadataHandlerInfo **ppIHandler
        );

    HRESULT GetCount(
        [out] UINT *pcCount
        );

    HRESULT GetValueByIndex(
        [in] UINT nIndex,
        [in, out, unique] PROPVARIANT *pvarSchema,
        [in, out, unique] PROPVARIANT *pvarId,
        [in, out, unique] PROPVARIANT *pvarValue
        );

    HRESULT GetValue(
        [in, unique] const PROPVARIANT *pvarSchema,
        [in] const PROPVARIANT *pvarId,
        [in, out, unique] PROPVARIANT *pvarValue
        );

    HRESULT GetEnumerator(
        [out] IWICEnumMetadataItem **ppIEnumMetadata
        );
};
```

**GetMetadataFormat** 方法會傳回元資料格式的 GUID。

**GetMetadataHandlerInfo** 方法會傳回 [**IWICMetadataHandlerInfo**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatahandlerinfo)介面，提供元資料處理程式的相關資訊。 這包括了哪些影像格式支援元資料格式的資訊，以及您的中繼資料讀取器是否需要存取完整的中繼資料資料流程。

**GetCount** 方法會傳回個別中繼資料專案的數目 (包括中繼資料資料流程中) 找到的內嵌中繼資料區塊。

**GetValueByIndex** 方法會依索引值傳回中繼資料專案。 這個方法可讓應用程式在中繼資料區塊中的每個中繼資料專案之間執行迴圈。 下列程式碼將示範應用程式如何使用這個方法來取得中繼資料區塊中的每個中繼資料專案。


```C++
PROPVARIANT readerValue;
IWICMetadataBlockReader *blockReader = NULL;
IWICMetadataReader *reader = NULL;

PropVariantInit(&readerValue);

hr = pFrameDecode->QueryInterface(IID_IWICMetadataBlockReader, (void**)&blockReader);

if (SUCCEEDED(hr))
{
    // Retrieve the third block in the image. This is image specific and
    // ideally you should call this by retrieving the reader count
    // first.
    hr = blockReader->GetReaderByIndex(2, &reader);
}

if (SUCCEEDED(hr))
{
    UINT numValues = 0;

    hr = reader->GetCount(&numValues);

    // Loop through each item and retrieve by index
    for (UINT i = 0; SUCCEEDED(hr) && i < numValues; i++)
    {
        PROPVARIANT id, value;

        PropVariantInit(&id);
        PropVariantInit(&value);

        hr = reader->GetValueByIndex(i, NULL, &id, &value);

        if (SUCCEEDED(hr))
        {
            // Do something with the metadata item.
            //...
        }
        PropVariantClear(&id);
        PropVariantClear(&value);
    }               
}
```



**GetValue** 方法會依架構和/或識別碼來抓取特定的中繼資料專案。 這個方法類似于 **GetValueByIndex** 方法，不同之處在于它會抓取具有特定架構或識別碼的中繼資料專案。

**GetEnumerator** 方法會傳回中繼資料區塊中每個中繼資料專案的列舉值。 這可讓應用程式使用列舉值來流覽您的元資料格式。

如果您的元資料格式沒有中繼資料專案的架構概念，則為 GetValue .。。方法應該忽略這個屬性。 但是，如果您的格式支援架構命名，您應該預期會有 **Null** 值。

如果中繼資料專案是內嵌的中繼資料區塊，請從內嵌內容的子流建立元資料處理程式，並傳回新的元資料處理程式。 如果沒有可用於嵌套區塊的中繼資料讀取器，請具現化並傳回未知的中繼資料讀取器。 若要為內嵌區塊建立新的中繼資料讀取器，請呼叫元件 factory 的 **CreateMetadataReaderFromContainer** 或 **CreateMetadataReader** 方法，或呼叫 [**WICMatchMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicmatchmetadatacontent) 函數。

如果中繼資料資料流程包含位元組由大到小的內容，中繼資料讀取器會負責交換其處理的任何資料值。 它也會負責通知任何嵌套的中繼資料讀取器，其正在使用位元組由大到小的資料流程。 不過，所有值都應該以位元組由小到大的格式傳回。

藉由支援查詢（中繼資料專案識別碼是 `VT_CLSID` (GUID) 對應至元資料格式），來執行命名空間導覽的支援。 如果在剖析期間識別出該格式的嵌套中繼資料讀取器，則必須將它傳回。 這可讓應用程式使用中繼資料查詢讀取器來搜尋您的元資料格式。

依識別碼取得中繼資料專案時，您應該使用 [PropVariantChangeType](/windows/win32/api/propvarutil/nf-propvarutil-propvariantchangetype) 函式將識別碼強制轉型為預期的型別。 例如，IFD 讀取器會將識別碼強制轉換成型別 `VT_UI2` ，以符合 IFD 標記識別項 USHORT 的資料型別。 輸入型別和預期的型別都必須 [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) 來進行這項作業。 這並不是必要的，但執行這項強制轉換可簡化呼叫讀取器以查詢中繼資料專案的程式碼。

### <a name="iwicpersiststream-interface"></a>IWICPersistStream 介面

[**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream)介面繼承自 **IPersistStream** ，並提供使用 [**WICPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions)列舉來儲存和載入物件的其他方法。

下列程式碼顯示 wincodecsdk .idl 檔中所定義之 [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) 介面的定義。

``` syntax
interface IWICPersistStream : IPersistStream
{
    HRESULT LoadEx(
        [in, unique] IStream *pIStream,
        [in, unique] const GUID *pguidPreferredVendor,
        [in] DWORD dwPersistOptions
        );

    HRESULT SaveEx(
        [in] IStream *pIStream,
        [in] DWORD dwPersistOptions,
        [in] BOOL fClearDirty
        );
};
```

**LoadEx** 方法會為您的中繼資料讀取器提供包含中繼資料區塊的資料流程。 您的讀取器會剖析此資料流程以存取基礎中繼資料專案。 您的中繼資料讀取器會使用位於原始中繼資料內容開頭的子流進行初始化。 如果您的讀取器不需要完整資料流程，則子資料流程的範圍僅限於中繼資料區塊的內容;否則，系統會提供完整的中繼資料資料流程，並在中繼資料區塊的開頭設定位置。

中繼資料寫入器會使用 **SaveEx** 方法來序列化中繼資料區塊。 當 **SaveEx** 用於中繼資料讀取器時，它應該會傳回 WINCODEC \_ ERR \_ UNSUPPORTEDOPERATION。

### <a name="iwicstreamprovider-interface"></a>IWICStreamProvider 介面

[**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider)介面可讓您的中繼資料讀取器提供其內容資料流程的參考、提供資料流程的相關資訊，以及重新整理資料流程的快取版本。

下列程式碼顯示 wincodecsdk .idl 檔中所定義之 [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider) 介面的定義。

``` syntax
interface IWICStreamProvider : IUnknown
{
    HRESULT GetStream(
        [out] IStream **ppIStream
        );

    HRESULT GetPersistOptions(
        [out] DWORD *pdwPersistOptions
        );

    HRESULT GetPreferredVendorGUID(
        [out] GUID *pguidPreferredVendor
        );

    HRESULT RefreshStream(
        );
};
```

**GetStream** 方法會捕獲中繼資料資料流程的參考。 您傳回的資料流程應該將資料流程指標重設為開始位置。 如果您的元資料格式需要完整的資料流程存取，則開始位置應該是中繼資料區塊的開頭。

**GetPersistOptions** 方法會從 [**WICPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions)列舉傳回資料流程的目前選項。

**GetPreferredVendorGUID** 方法會傳回中繼資料讀取器的廠商 GUID。

**RefreshStream** 方法會重新整理中繼資料資料流程。 此方法必須為任何嵌套中繼資料區塊呼叫具有 **Null** 資料流程的 **LoadEx** 。 這是必要的，因為就地編輯時，因為有嵌套的中繼資料區塊及其專案可能已不存在。

## <a name="creating-a-metadata-writer"></a>建立中繼資料寫入器

中繼資料寫入器是一種元資料處理程式類型，可讓您將中繼資料區塊序列化至影像框架，或在個別框架之外（如果影像格式支援的話）。 編解碼器內中繼資料寫入器的主要存取是透過每個 WIC 編碼器所實行的 [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) 介面。 這個介面可讓應用程式列舉內嵌于影像中的每個中繼資料區塊，以針對每個中繼資料區塊探索和具現化適當的中繼資料。 沒有對應中繼資料寫入器的中繼資料區塊會被視為未知，而且會定義為 GUID CLSID \_ WICUnknownMetadataReader。 若要啟用已啟用 WIC 的應用程式來序列化和寫入您的元資料格式，您必須建立可執行下列介面的類別： [**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)、 [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)、 [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream)和 [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider)。

> [!Note]  
> 如果您的元資料格式具有可轉譯某些必要介面方法的限制，這類方法應該會傳回 WINCODEC \_ ERR \_ UNSUPPORTEDOPERATION。

 

### <a name="iwicmetadatawriter-interface"></a>IWICMetadataWriter 介面

[**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)介面必須由您的中繼資料寫入器來執行。 此外，由於 **IWICMetadataWriter** 繼承自 [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)，因此您也必須執行 **IWICMetadataReader** 的所有方法。 由於這兩種處理常式類型都需要相同的介面繼承，因此您可能會想要建立可同時提供讀取和寫入功能的單一類別。

下列程式碼顯示 wincodecsdk .idl 檔中所定義之中繼資料寫入器介面的定義。

``` syntax
interface IWICMetadataWriter : IWICMetadataReader
{
    HRESULT SetValue(
        [in, unique] const PROPVARIANT *pvarSchema,
        [in] const PROPVARIANT *pvarId,
        [in] const PROPVARIANT *pvarValue
        );

    HRESULT SetValueByIndex(
        [in] UINT nIndex,
        [in, unique] const PROPVARIANT *pvarSchema,
        [in] const PROPVARIANT *pvarId,
        [in] const PROPVARIANT *pvarValue
        );

    HRESULT RemoveValue(
        [in, unique] const PROPVARIANT *pvarSchema,
        [in] const PROPVARIANT *pvarId
        );

    HRESULT RemoveValueByIndex(
        [in] UINT nIndex
        );
};
```

**SetValue** 方法會將指定的中繼資料專案寫入中繼資料資料流程。

**SetValueByIndex** 方法會將指定的中繼資料專案寫入中繼資料資料流程中的指定索引處。 索引不會參考識別碼，而是參考中繼資料區塊內的專案位置。

**RemoveValue** 方法會從中繼資料資料流程中移除指定的中繼資料專案。

**RemoveValueByIndex** 方法會從中繼資料資料流程中移除位於指定索引位置的中繼資料專案。 移除專案之後，如果索引不是最後一個索引，則其餘的中繼資料專案應該會佔用空的索引。 這也預期計數會在移除專案之後變更。

中繼資料編寫者必須負責將 [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) 專案轉換成您的格式所需的基礎結構。 不過，與中繼資料讀取器不同的是，變數類型通常不應該強制轉型成不同的類型，因為呼叫端會特別指出要使用的資料型別。

您的中繼資料寫入器必須將所有中繼資料專案認可至影像資料流程，包括隱藏或無法辨識的值。 這包括未知的嵌套中繼資料區塊。 不過，編碼器在起始儲存作業之前，必須負責設定任何重要的中繼資料專案。

如果中繼資料資料流程包含位元組由大到小的內容，中繼資料寫入器就會負責交換其處理的任何資料值。 它也負責通知任何嵌套的中繼資料寫入器，以便在儲存時使用位元組由大到小的資料流程。

藉由 `VT_CLSID` (GUID) 對應至元資料格式的中繼資料專案支援集合和移除作業，來支援建立和移除命名空間。 中繼資料寫入器會呼叫 [**WICSerializeMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicserializemetadatacontent) 函式，將嵌套的中繼資料寫入器內容正確地內嵌至父中繼資料寫入器中。

如果您的元資料格式支援就地編碼，則必須負責管理必要的填補。 如需就地編碼的詳細資訊，請參閱 [WIC 中繼資料總覽](-wic-about-metadata.md) 和 [讀取和寫入影像中繼資料的總覽](-wic-codec-readingwritingmetadata.md)。

### <a name="iwicpersiststream-interface"></a>IWICPersistStream 介面

[**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream)介面繼承自 **IPersistStream** ，並提供使用 [**WICPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions)列舉來儲存和載入物件的其他方法。

下列程式碼顯示 wincodecsdk .idl 檔中所定義之 [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) 介面的定義。

``` syntax
interface IWICPersistStream : IPersistStream
{
    HRESULT LoadEx(
        [in, unique] IStream *pIStream,
        [in, unique] const GUID *pguidPreferredVendor,
        [in] DWORD dwPersistOptions
        );

    HRESULT SaveEx(
        [in] IStream *pIStream,
        [in] DWORD dwPersistOptions,
        [in] BOOL fClearDirty
        );
};
```

**LoadEx** 方法會使用包含中繼資料區塊的資料流程來提供元資料處理程式。

**SaveEx** 方法會將中繼資料序列化為數據流。 如果提供的資料流程與初始化資料流程相同，您應該執行就地編碼。 如果支援就地編碼，則在沒有 \_ \_ 足夠填補可執行就地編碼時，此方法應該會傳回 WINCODEC 錯誤 TOOMUCHMETADATA。 如果不支援就地編碼，此方法應該會傳回 WINCODEC \_ ERR \_ UNSUPPORTEDOPERATION。

必須實作為 **IPersistStream：： GetSizeMax** 方法，且必須傳回在後續儲存時寫入之中繼資料內容的確切大小。

如果中繼資料寫入器是透過資料流程初始化，則應實作為 **IPersistStream：： IsDirty** 方法，如此一來，映射就可以可靠地判斷其內容是否已變更。

如果您的元資料格式支援嵌套中繼資料區塊，則在儲存至資料流程時，您的中繼資料寫入器應該會將其內容的序列化委派給嵌套中繼資料寫入器。

### <a name="iwicstreamprovider-interface"></a>IWICStreamProvider 介面

中繼資料寫入器的 [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider) 介面實作為中繼資料讀取器的實作為。 如需詳細資訊，請參閱本檔中的建立中繼資料讀取器一節。

## <a name="installing-and-registering-a-metadata-handler"></a>安裝和註冊元資料處理程式

若要安裝元資料處理程式，您必須提供處理常式元件，並在系統登錄中註冊它。 您可以決定如何及何時填入登錄機碼。

> [!Note]  
> 為了方便閱讀，在本檔的下列各節所示的登錄機碼中，不會顯示實際的十六進位 Guid。 若要找出指定之易記名稱的十六進位值，請參閱 wincodec .idl 和 wincodecsdk .idl 檔。

 

### <a name="metadata-handler-registry-keys"></a>元資料處理程式登錄機碼

每個元資料處理程式都是以唯一 CLSID 來識別，而每個處理常式都需要在元資料處理程式的類別識別碼 GUID 下註冊其 CLSID。 每個處理常式類型的類別目錄識別碼都定義于 wincodec 中;讀者的分類識別碼名稱是 CATID \_ WICMetadataReader，而寫入器的類別識別碼名稱是 catid \_ WICMetadataWriter。

每個元資料處理程式都是以唯一 CLSID 來識別，而每個處理常式都需要在元資料處理程式的類別識別碼 GUID 下註冊其 CLSID。 每個處理常式類型的類別目錄識別碼都定義于 wincodec 中;讀者的分類識別碼名稱是 CATID \_ WICMetadataReader，而寫入器的類別識別碼名稱是 catid \_ WICMetadataWriter。

> [!Note]  
> 在下列登錄機碼清單中，{Reader CLSID} 是指您為中繼資料讀取器提供的唯一 CLSID。 {Writer CLSID} 是指您為中繼資料寫入器提供的唯一 CLSID。 {處理常式 CLSID} 是指讀取器的 CLSID、寫入器的 CLSID，或兩者都是根據您所提供的處理常式而定。 {容器 GUID} 是指容器物件 (映射格式或元資料格式) 可包含中繼資料區塊。

 

下列登錄機碼會使用其他可用的元資料處理程式來註冊您的元資料處理程式：

``` syntax
[HKEY_CLASSES_ROOT\CLSID\{CATID_WICMetadataReaders}\Instance\{Reader CLSID}]
CLSID={Reader CLSID}
Friendly Name="Reader Name"

[HKEY_CLASSES_ROOT\CLSID\{CATID_ WICMetadataWriters}\Instance\{Writer CLSID}]
CLSID={Writer CLSID}
Friendly Name="Writer Name"
```

除了在各自的類別中註冊處理常式之外，您還必須註冊額外的索引鍵，以提供處理常式的特定資訊。 讀取器和寫入器共用類似的登錄機碼需求。 下列語法顯示如何註冊處理常式。 讀取器處理常式和寫入器處理常式都必須使用其各自的 Clsid 以這種方式註冊：

``` syntax
[HKEY_CLASSES_ROOT\CLSID\{CLSID}]
"Vendor"={VendorGUID}
"Date"="yyyy-mm-dd"
"Version"="Major.Minor.Build.Number"
"SpecVersion"="Major.Minor.Build.Number"
"MetadataFormat"={MetadataFormatGUID}
"RequiresFullStream"=dword:1|0
"SupportsPadding"= dword:1|0
"FixedSize"=0

[HKEY_CLASSES_ROOT\CLSID\{CLSID}\InProcServer32]
@="drive:\path\yourdll.dll"
"ThreadingModel"="Apartment"

[HKEY_CLASSES_ROOT\CLSID\{CLSID}\{LCID}]
Author="Author's Name"
Description = " Metadata Description"
DeviceManufacturer ="Manufacturer Name"
DeviceModels="Device,Device"
FriendlyName="Friendly Name"
```

### <a name="metadata-readers"></a>中繼資料讀取器

中繼資料讀取器註冊也會包含描述如何以容器格式內嵌讀取器的索引鍵。 容器格式可以是影像格式，例如 TIFF 或 JPEG;它也可以是另一個元資料格式，例如 IFD 中繼資料區塊。 原生支援的映射容器格式會列在 wincodec 中;每個影像容器格式都會定義為名稱以 GUID ContainerFormat 開頭的 GUID \_ 。 原生支援的中繼資料容器格式會列在 wincodecsdk 中;每個中繼資料容器格式都會定義為名稱以 GUID MetadataFormat 開頭的 GUID \_ 。

下列索引鍵會註冊中繼資料讀取器所支援的容器，以及要從該容器讀取的資料。 讀取器所支援的每個容器都必須以這種方式註冊。

``` syntax
[HKEY_CLASSES_ROOT\CLSID\{Reader CLSID}\Containers\{Container GUID}\0]
"Position"=dword:00000000
"Pattern"=hex:ff,ff,ff,...
"Mask"=hex:ff,ff,ff,...
"DataOffset"=dword:00000006
```

模式索引鍵描述用來比對中繼資料區塊與讀取器的二進位模式。 為您的中繼資料讀取器定義模式時，應該夠可靠，因為正相符表示中繼資料讀取器可以瞭解中繼資料區塊中處理的中繼資料。

DataOffset 索引鍵會描述區塊標頭中中繼資料的固定位移。 此索引鍵是選擇性的，如果未指定，則表示無法使用來自區塊標頭的固定位移找出實際的中繼資料。

### <a name="metadata-writers"></a>中繼資料寫入器

中繼資料寫入器註冊也包含索引鍵，以描述如何寫出以容器格式內嵌之中繼資料內容前面的標頭。 如同讀取器，容器格式可以是影像格式或另一個中繼資料區塊。

下列索引鍵會註冊中繼資料寫入器支援的容器，以及寫入標頭和中繼資料所需的資料。 寫入器支援的每個容器都必須以這種方式註冊。

``` syntax
[HKEY_CLASSES_ROOT\CLSID\{Writer CLSID}\Containers\{Container GUID}]
"WritePosition"=dword:00000000
"WriteHeader"=hex:ff,ff,ff,...
"WriteOffset"=dword:00000000
```

WriteHeader 索引鍵描述要寫入之中繼資料區塊標頭的二進位模式。 此二進位模式與元資料格式的讀取器模式索引鍵一致。

WriteOffset 索引鍵會描述應寫入中繼資料之區塊標頭中的固定位移。 此索引鍵是選擇性的，如果未指定，則表示不應使用標頭來寫出實際的中繼資料。

### <a name="signing-a-metadata-handler"></a>簽署元資料處理程式

所有元資料處理程式都必須經過數位簽署，才能參與 WIC 探索進程。 WIC 不會載入任何未由受信任的憑證授權單位單位簽署的處理常式。 如需有關數位簽章的詳細資訊，請參閱程式 [代碼簽署簡介](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))。

## <a name="special-considerations"></a>特殊考慮

下列各節包含您在建立自己的元資料處理程式時，必須考慮的其他資訊。

### <a name="propvariants"></a>PROPVARIANTS

WIC 使用 [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) 來代表讀取和寫入的中繼資料專案。 PROPVARIANT 會針對元資料格式內使用的中繼資料專案，提供資料類型和資料值。 做為元資料處理程式的寫入器，您有很大的彈性，可讓您以元資料格式儲存資料，以及如何在中繼資料區塊內表示資料。 下表提供的指導方針可協助您決定要在不同情況下使用的適當 PROPVARIANT 型別。



| 元資料類型為 .。。          | 使用 PROPVARIANT 類型      | PROPVARIANT 屬性                                                                                                                                                                                                                                                           |
|------------------------------|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 空白或不存在。       | VT \_ 空白                 | 不適用。                                                                                                                                                                                                                                                                |
| 未定義。                   | VT \_ BLOB                  | 使用 blob 屬性來設定使用 CoTaskMemAlloc 配置之 BLOB 物件的大小和指標。                                                                                                                                                                           |
| 中繼資料區塊。            | VT \_ 不明               | 此類型使用 punkVal 屬性。                                                                                                                                                                                                                                           |
| 型別的陣列。           | VT \_ 向量 \| VT \_ {type}  | 使用 ca {type} 屬性來設定使用 CoTaskMemAlloc 配置之陣列的計數和指標。                                                                                                                                                                            |
| 中繼資料區塊的陣列。 | VT \_ 向量 \| VT \_ 變異 | 您可以使用 capropvar 屬性來設定 variant 的陣列。                                                                                                                                                                                                                       |
| 帶正負號的有理數值。     | VT \_ I8                    | 使用 hVal 屬性來設定值。 將 [高] 字組設為分母，然後將 [低] 字組設為分子。                                                                                                                                                                |
| 有理數值。            | VT \_ UI8                   | 使用 uhVal 屬性來設定值。 將 HighPart 設定為分母，並將 LowPart 設定為分子。 請注意，LowPart 是不帶正負號的整數。分子應從不帶正負號的 int 轉換成 int，以確保會保留正負號位（如果有的話）。 |



 

若要避免代表陣列專案的重複專案，請不要使用安全陣列;只使用簡單的陣列。 這可減少應用程式在解讀 [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) 類型時需要執行的工作。

請盡可能避免使用 `VT_BYREF` 和儲存值。 `VT_BYREF` 適用于小型類型 (常見的中繼資料專案) ，而且不提供大小資訊。

在使用 [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)之前，請一律呼叫 **PropVariantInit** 來將值初始化。 當您完成 PROPVARIANT 時，請一律呼叫 **PropVariantClear** 來釋放配置給變數的任何記憶體。

### <a name="8bim-handlers"></a>8BIM 處理常式

撰寫8BIM 中繼資料區塊的元資料處理程式時，您必須使用同時封裝8BIM 簽章和識別碼的簽章。 例如，原生8BIMIPTC 中繼資料讀取器會提供下列讀取器探索的登錄資訊：

``` syntax
[HKEY_CLASSES_ROOT\CLSID\{0010668C-0801-4DA6-A4A4-826522B6D28F}\Containers\{16100D66-8570-4BB9-B92D-FDA4B23ECE67}\0]
"Position"=dword:00000000
"Pattern"=hex:38,42,49,4d,04,04
"Mask"=hex:ff,ff,ff,ff,ff,ff
"DataOffset"=dword:00000006
```

8BIMIPTC 讀取器具有已註冊的0x38、0x42、0x49、0x4D、0x04、0x04 模式。 前四個位元組 (0x38、0x42、0x49、0x4D) 是8BIM 簽章，而最後兩個位元組 (0x04，0x04) 是 IPTC 記錄的識別碼。

因此，若要撰寫8BIM 中繼資料讀取器來取得解析資訊，您需要已註冊的0x38、0x42、0x49、0x4D、0x03、0xED 模式。 同樣地，前四個位元組 (0x38、0x42、0x49、0x4D) 是8BIM 簽章。 不過，最後兩個位元組 (0x03，0xED) ，則是由 PSD 格式所定義的解析資訊識別碼。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[Windows 影像處理元件總覽](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[WIC 中繼資料總覽](-wic-about-metadata.md)
</dt> <dt>

[中繼資料查詢語言總覽](-wic-codec-metadataquerylanguage.md)
</dt> <dt>

[讀取和寫入影像中繼資料的總覽](-wic-codec-readingwritingmetadata.md)
</dt> <dt>

[How to：使用中繼資料重新編碼 JPEG 影像](-wic-codec-jpegmetadataencoding.md)
</dt> <dt>

**其他資源**
</dt> <dt>

[如何撰寫 WIC-Enabled 編解碼器](-wic-howtowriteacodec.md)
</dt> </dl>

 

 
