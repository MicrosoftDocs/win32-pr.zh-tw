---
description: 本主題說明如何撰寫 Microsoft 媒體基礎媒體來源的自訂 Shell 屬性處理常式。
ms.assetid: f8cf70ff-8324-4308-8adf-a145aa351ca9
title: 媒體檔案的自訂中繼資料提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1951fd90265299cb53369d521193740b7d4d05e0f1650583965eb670ab375cc1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777598"
---
# <a name="custom-metadata-providers-for-media-files"></a>媒體檔案的自訂中繼資料提供者

本主題說明如何撰寫 Microsoft 媒體基礎媒體來源的自訂 Shell 屬性處理常式。

> [!Note]  
> 如需媒體基礎中中繼資料提供者的背景資訊，請參閱 [媒體中繼資料](media-metadata.md)。 本主題討論 Shell 屬性處理常式;它不會描述第1版的中繼資料介面 [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata)。

 

中繼資料會緊密地系結至檔案的格式。 在媒體基礎中，檔案格式會以媒體來源表示。 如果您想要支援媒體基礎中原生不支援的格式中繼資料，則必須使用屬性處理常式來執行自訂媒體來源。 屬性處理常式可讓 Shell 屬性系統有效率地讀取和寫入中繼資料。

屬性處理常式是一個 COM 物件，它會執行下列介面：

-   [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream)
-   [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

也可以選擇公開下列介面：

-   [**IPropertyStoreCapabilities**](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities)

如果 Shell 屬性系統需要取得檔案的中繼資料，它會呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 來建立屬性處理常式，然後在 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) 介面上呼叫適當的讀取和寫入方法。

媒體基礎管線會使用稍微不同的機制，因為管線會直接從媒體來源取得屬性處理常式。 管線會呼叫媒體來源上的 [**IMFGetService：： GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) ，而不是呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)來建立屬性處理常式，如 [Shell 中繼資料提供者](shell-metadata-providers.md)的主題所述。

若要建立自訂屬性處理常式，請執行下列動作：

-   執行 [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) 介面以公開 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。 服務 GUID 是 **MF \_ 屬性 \_ 處理常式 \_ 服務**。
-   如果將從遠端使用媒體來源，則除了 [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)以外，它也必須透過媒體來源的 **QueryInterface** 方法公開 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)介面。
-   若要將屬性處理常式提供給 Shell 屬性系統，請如 [註冊和散發屬性處理常式](../properties/prophand-reg-dist.md)中所述，註冊屬性處理常式的 DLL。
-   媒體來源會分開註冊，如 [配置處理常式和 Byte-Stream 處理常式](scheme-handlers-and-byte-stream-handlers.md)中所述。

### <a name="implementation-tips"></a>執行提示

如需中繼資料屬性索引鍵的清單，請參閱媒體檔案的 [中繼資料屬性](metadata-properties-for-media-files.md)。

屬性處理常式必須快速;它們必須提供對中繼資料的有效讀取和寫入存取權。  (考慮到 Shell 可能會從數百個檔案取出中繼資料 ) 。因此，請不要從您的屬性處理常式呼叫 [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) 。 **MFStartup** 函式會引進啟動延遲，因為它會建立多個工作佇列執行緒，並配置全域記憶體。

在一般的執行中，屬性處理常式和媒體來源會共用部分相同的剖析程式碼。 不過，媒體來源會針對 i/o 使用非同步 [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) 呼叫，而屬性處理常式會使用 [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) 介面。 媒體基礎提供可包裝 **IStream** 型資料流程，並將其公開為 **IMFByteStream** 資料流程的 helper 物件。 若要建立包裝函式，請呼叫 [**MFCreateMFByteStreamOnStream**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemfbytestreamonstream)。

更新中繼資料時，建議您將資料直接寫入原始資料流程。 這項建議與大部分屬性處理常式的 *複製寫入* 行為不同，後者會修改資料的複本。 媒體檔案可能很大，所以寫入時複製通常太慢，無法進行有效率的執行。 若要停用寫入時複製，請設定 **ManualSafeSave** 登錄設定，如 [註冊和散發屬性處理常式](../properties/prophand-reg-dist.md)中所述。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體中繼資料](media-metadata.md)
</dt> <dt>

[媒體來源](media-sources.md)
</dt> <dt>

[撰寫自訂媒體來源](writing-a-custom-media-source.md)
</dt> </dl>

 

 
