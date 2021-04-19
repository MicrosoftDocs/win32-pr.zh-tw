---
description: 擴充的語言服務 (ELS) 會實作為動態連結程式庫 (DLL) ，可針對應用程式所指定的文字提供各種語言支援功能。
ms.assetid: 23d4e42a-a5bb-467c-a8b9-6a57ae39daa0
title: 關於擴充的語言服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a6594fcfe67954a56cb09e239221b2b529d4d01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983753"
---
# <a name="about-extended-linguistic-services"></a>關於擴充的語言服務

擴充的語言服務 (ELS) 會實作為動態連結程式庫 (DLL) ，可針對應用程式所指定的文字提供各種語言支援功能。 這項技術包含了 ELS 平臺和外掛程式，可讓應用程式透過平臺存取數個預先定義的語言服務類型。

> [!Note]  
> 在 Windows 7 和更新版本中，會自動安裝 ELS 模組。

 

## <a name="els-platform"></a>ELS 平臺

ELS 平臺是您的應用程式和 ELS 服務之間的介面。 它提供簡單的方法，讓您透過相同的 API 來執行數種語言功能，讓應用程式能夠存取及使用特定的服務。 如需 API 的詳細資訊，請參閱 [擴充語言服務參考。](extended-linguistic-services-reference.md)

> [!Note]  
> 當應用程式呼叫任何的 ELS API 函式時，此平臺會視需要配置記憶體和資源，以便與服務通訊。 應用程式會負責再次呼叫平臺以釋放這些資源。

 

該平臺會在應用程式虛擬記憶體空間內部執行，而且所有配置的記憶體都是此空間的一部分。 因此，您的應用程式只需要連結至 Elscore 或動態載入 Elscore.dll，就可以連結至 ELS 元件 DLL (Elscore.dll) 。

## <a name="els-services"></a>ELS 服務

針對 Windows 7 和更新版本，ELS 平臺僅支援下列預先定義的服務。

-   [Microsoft 語言偵測](microsoft-language-detection.md)
-   [Microsoft 腳本偵測](microsoft-script-detection.md)
-   [音譯服務](transliteration-services.md)

> [!Note]  
> 未來的 ELS 版本將會支援 Microsoft 或服務提供者所提供的其他服務。

 

每項服務都與描述服務用途的服務類別相關聯。 類別目錄是以 nonlocalizable 字串表示。 應用程式會使用它來列舉可用的服務。 目前的服務類別為：

-   "語言偵測"
-   「腳本偵測」
-   音譯

平臺會使用服務中繼資料來列舉應用程式所要求的服務。 服務全域唯一識別碼 (GUID) 、支援的輸入和輸出語言和腳本等屬性，以及應用程式可使用服務類別來列舉所需的 ELS 服務。

每個 ELS 服務都會實作為可安裝在作業系統上的 DLL 所支援的外掛程式，讓 ELS 平臺可以偵測和使用它。 如有必要，服務可以公開自己的子服務。

## <a name="main-els-operations"></a>主要的 ELS 作業

本節說明 ELS 平臺所支援的主要作業。 平臺同時支援同步和非同步呼叫模式。 非同步呼叫模式會使用應用程式執行緒集區來排程處理要求的執行緒。

> [!Note]  
> 因為此平臺支援非同步模式，所以 ELS 服務不需要自行執行這類的功能。

 

### <a name="service-enumeration"></a>服務列舉

ELS 平臺會載入和管理所有的 ELS 服務，讓應用程式透明地運作。 應用程式會藉由呼叫 [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices)來列舉可用的服務。 如需程式設計指示，請參閱 [列舉和釋放服務](enumerating-and-freeing-services.md)。

> [!Note]  
> 基於效能考慮，建議您讓應用程式只列舉可用服務一次。 ELS 平臺會再次檢查下一個列舉上的服務，以確保它的列舉結果一律是最新的。

 

### <a name="text-recognition"></a>文字辨識

在服務列舉之後，應用程式會呼叫 [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) 函數，以使用特定的 ELS 服務，將輸入文字的任何文字範圍對應至輸出文字。 文字辨識的範例是使用語言偵測服務來接收文字區段，並偵測其最可能的語言。

在服務辨識出文字之後， [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) 會傳回 [**對應 \_ 屬性 \_ 包**](/windows/desktop/api/Elscore/ns-elscore-mapping_property_bag) 結構，其中填入了服務所產生的輸出資料和屬性。 為了避免記憶體流失，應用程式必須在每次 [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext)傳回 S OK 時呼叫 [**MappingFreePropertyBag**](/windows/desktop/api/Elscore/nf-elscore-mappingfreepropertybag) ，以釋放屬性包 \_ 。 應用程式通常會在使用輸出資料完成時，或輸出資料不再相關時執行這項工作，因為文字的輸入區域已經過修改，例如編輯或刪除。 釋放屬性包時， **MappingFreePropertyBag** 會傳回。

文字辨識的程式設計指示是在 [要求文字](requesting-text-recognition.md)辨識中提供。

### <a name="service-termination"></a>服務終止

當您的應用程式不再需要 ELS 服務時，它會在結束之前呼叫 [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices) 。 如需詳細資訊，請參閱 [列舉和釋放服務](enumerating-and-freeing-services.md)。

### <a name="versioning"></a>版本控制

未來的 ELS 版本將允許更新 ELS 服務。 應用程式將能夠檢查 [**對應 \_ 服務 \_ 資訊**](/windows/desktop/api/Elscore/ns-elscore-mapping_service_info) 結構的版本號碼，以偵測服務中的任何變更。

> [!Note]  
> 您的 ELS 應用程式不應假設相同服務的不同版本可以完全取得相同的結果。

 

 

 



