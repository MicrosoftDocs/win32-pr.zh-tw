---
description: SQL-DMO 媒體類型
ms.assetid: 40958e12-09c7-4ce5-aa4d-5ed8b1f40aa3
title: SQL-DMO 媒體類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1997abb1cc3c8eb10301778982ef7a46690855ed
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104514361"
---
# <a name="dmo-media-types"></a>SQL-DMO 媒體類型

媒體類型描述與媒體資料資料流程相關聯的格式。 本文描述 DMOs 如何處理媒體類型。 它主要適用于撰寫自己的自訂 DMOs 的開發人員。

媒體類型是使用 [**Sql-dmo \_ 媒體 \_ 類型**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) 結構來定義。 此結構包含下列資訊：

-   *主要類型* 是定義廣大類別的全域唯一識別碼 (GUID) ，例如音訊或影片。
-   *子類型* 是定義更具體的型別層面的 GUID。 例如，在影片中，子類型包含16位 RGB、24位 RGB、UYVY、DV 編碼的影片等等。
-   *格式區塊* 是完整指定格式的輔助結構。 格式區塊的版面配置取決於資料的類型。 例如，PCM 音訊會使用 **WAVEFORMATEX** 結構。 影片使用各種其他結構，包括 **VIDEOINFOHEADER** 和 **VIDEOINFOHEADER2**。 格式區塊的版面配置是以格式類型 GUID 來識別。 例如，FORMAT \_ WaveFormatEx 會指定 **WaveFormatEx** 結構。

第一次建立時，資料流程沒有媒體類型。 用戶端必須先設定每個資料流程的媒體類型，然後才能處理任何資料。 從用戶端的觀點來看， [設定媒體類型](setting-media-types-on-a-dmo.md)時，會說明此程式。

**登錄中的媒體類型**

SQL-DMO 可以藉由呼叫 [**DMORegister**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoregister) 函式，將它支援的媒體類型清單新增至登錄。 應用程式可以使用這項資訊來搜尋符合特定格式的 DMOs。 登錄中的資訊並不是完整的。 一般情況下，您只會包含 SQL-DMO 所支援的主要類型。 登錄專案的輸入和輸出類型都有不同的金鑰，但無法區分個別的資料流程。

**DMORegister** 函式會使用 [**sql-dmo \_ 部分 \_**](/previous-versions/windows/desktop/api/Dmoreg/ns-dmoreg-dmo_partial_mediatype)媒體型結構來描述媒體類型。 此結構包含在 **Sql-dmo \_ 媒體 \_ 類型** 結構中找到的資訊子集，也就是主要類型和子類型。 它不包含格式區塊，因為格式區塊通常包含太細微而無法包含在登錄中的資訊，例如影片影像的高度和寬度。

**慣用的媒體類型**

應用程式建立了一來，它就可以查詢它所支援的媒體類型。 針對每個資料流程，每個資料流程會建立一份媒體類型清單 (可能是空的) ，並依喜好設定排列順序。 [**IMediaObject：： GetInputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getinputtype)和 [**IMediaObject：： GetOutputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getoutputtype)方法會列舉慣用的類型。 當應用程式在其他資料流程上設定媒體類型時，資料流程的慣用類型可能會動態變更。 例如，慣用的輸出類型清單可能會在設定輸入類型之後變更，反之亦然。 但是，不需要以動態方式更新其慣用類型。 應用程式無法假設它收到的每個類型都是有效的。 基於這個理由， [**IMediaObject：： SetInputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-setinputtype) 和 [**IMediaObject：： SetOutputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-setoutputtype) 方法支援用於測試特定型別的旗標。

**GetInputType** 和 **GetOutputType** 方法都會傳回 **sql-dmo \_ 媒體 \_ 類型** 結構。 您可以將此結構中的部分資訊留白，以表示類型的範圍。 主要類型或子類型可以是 GUID \_ Null，且格式區塊可以是空的 (零位元組) 。 如果格式區塊是空的，格式類型必須是 GUID \_ Null。

應用程式設定所有的輸入型別之後，每個輸出資料流程通常應該會傳回至少一個完整型別。 完整的輸出型別可加速測試，應用程式可以使用它做為合理的預設值。 SQL-DMO 測試應用程式依賴此行為。  (請參閱 [使用 DMOTest 應用程式](using-the-dmotest-application.md)。 ) 

**設定媒體類型**

應用程式會使用 **SetInputType** 和 **SetOutputType** 方法來測試、設定或清除指定之資料流程上的類型。 應用程式必須完全指定類型。 SQL-DMO 會驗證它是否可以接受建議的型別。 答案可能取決於已在其他資料流程上設定的類型。 SQL-DMO \_ SET \_ TYPEF \_ CLEAR 旗標會清除資料流程的類型，因此應用程式可以「返回」並嘗試另一個組合。

**示範案例**

下列範例說明一些一般案例，以說明在先前章節中所做的點。

-   **影片解碼器。** 在典型的影片解碼中，輸入類型部分會決定輸出類型。 例如，這兩個數據流通常都必須有相同的畫面播放速率和影像維度。 其中一個選項是在設定輸入類型之前，不會定義任何慣用的輸出類型。 另一個選項是列舉不完整的類型集合，並省略格式區塊。 您可以使用子類型來指出支援的未壓縮類型，例如16位 RGB、24位 RGB 等等。 此外，影片解碼器通常不支援在輸入類型之前設定輸出類型。 常見的案例是從已知的輸入格式解碼，因此這項限制是合理的。
-   **音訊解碼器。** 音訊解碼器可能會支援一組有限且固定的輸出格式。 在這種情況下，它可能會在已知輸入格式之前，建立慣用輸出格式的清單。
-   **壓縮機。** 在大多數情況下，影片壓縮程式無法完全指定其慣用的輸出格式，直到應用程式設定輸入格式為止，反之亦然。 取而代之的是，，則應該傳回不完整的類型，而不含格式區塊。 針對音訊和影片壓縮，應用程式通常需要設定各種輸出參數，例如位元速率。 不過，在設定輸入類型之後，基於上述原因，壓縮程式應該會傳回至少一個完整輸出類型。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[撰寫 SQL-DMO](writing-a-dmo.md)
</dt> </dl>

 

 



