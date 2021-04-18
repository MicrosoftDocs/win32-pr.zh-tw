---
description: ELS 音譯服務會將 UTF-16 文字從一個書寫系統對應到另一個寫入系統。
ms.assetid: 32e46c52-5c3c-4e22-8f4e-05286ee213ba
title: 音譯服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc00b96d56e6b05e70b352c81da0280e9ef35043
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115620"
---
# <a name="transliteration-services"></a>音譯服務

ELS 音譯服務會將 UTF-16 文字從一個書寫系統對應到另一個寫入系統。 每個服務實際上都是套用至一組特定輸入和輸出 Unicode 腳本的資料，而實際的音譯是在 ELS 平臺內部。 應用程式可以選擇性地列舉特定輸入和輸出腳本的可用服務，並選取所需的服務。

平臺會維護 ELS 音譯服務的中繼資料。 每個服務的中繼資料會提供服務的描述，並列出服務所支援的輸入和輸出腳本。 中繼資料是由 [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices)函數所抓取的 [**對應 \_ 服務 \_ 資訊**](/windows/desktop/api/Elscore/ns-elscore-mapping_service_info)結構所表示。

## <a name="input-to-a-transliteration-service"></a>音譯服務的輸入

音譯服務的輸入是一個書寫系統中的 UTF-16 文字。

## <a name="output-of-a-transliteration-service"></a>音譯服務的輸出

音譯服務的輸出是對應至第二個書寫系統的 UTF-16 文字。 如果輸入文字的任何指定區塊都沒有適當的音譯對應，區塊會維持不變。

## <a name="transliteration-service-operation"></a>音譯服務作業

音譯服務會適當地將輸入腳本中的 Unicode 文字對應至輸出腳本、字元或詞彙。 應用程式可以選擇在呼叫 [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices)時指定輸入和輸出腳本，或藉由提供服務 GUID，來取得感興趣的特定音譯服務。 應用程式的另一個選項是在呼叫 **MappingGetServices** 時，藉由指定服務類別 "音譯" 來列舉所有可用的音譯服務。 在此情況下，應用程式會呼叫每個服務並將結果與原始文字進行比較，以查看特定服務的作業是否已變更結果。

應用程式可以透過呼叫 [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext)來要求 ELS 音譯服務的文字辨識。 當它收到要求時，音譯服務會配置一個緩衝區來包含所轉譯的資料，然後針對應用程式所提供的輸入字串中的每個程式碼點執行文字辨識。

> [!Note]  
> 原始文字和轉譯的文字可能會有不同的長度。

 

## <a name="transliteration-service-guids"></a>音譯服務 Guid

音譯服務的 Guid 是在 Elssrvc 中宣告，如下列程式碼所示。


```C++
// {A3A8333B-F4FC-42f6-A0C4-0462FE7317CB}
static const GUID ELS_GUID_TRANSLITERATION_HANT_TO_HANS =
    { 0xA3A8333B, 0xF4FC, 0x42f6, { 0xA0, 0xC4, 0x04, 0x62, 0xFE, 0x73, 0x17, 0xCB } };

// {3CACCDC8-5590-42dc-9A7B-B5A6B5B3B63B}
static const GUID ELS_GUID_TRANSLITERATION_HANS_TO_HANT =
    { 0x3CACCDC8, 0x5590, 0x42dc, { 0x9A, 0x7B, 0xB5, 0xA6, 0xB5, 0xB3, 0xB6, 0x3B } };

// {D8B983B1-F8BF-4a2b-BCD5-5B5EA20613E1}
static const GUID ELS_GUID_TRANSLITERATION_MALAYALAM_TO_LATIN =
    { 0xD8B983B1, 0xF8BF, 0x4a2b, { 0xBC, 0xD5, 0x5B, 0x5E, 0xA2, 0x06, 0x13, 0xE1 } };

// {C4A4DCFE-2661-4d02-9835-F48187109803}
static const GUID ELS_GUID_TRANSLITERATION_DEVANAGARI_TO_LATIN =
    { 0xC4A4DCFE, 0x2661, 0x4d02, { 0x98, 0x35, 0xF4, 0x81, 0x87, 0x10, 0x98, 0x03 } };

// {3DD12A98-5AFD-4903-A13F-E17E6C0BFE01}
static const GUID ELS_GUID_TRANSLITERATION_CYRILLIC_TO_LATIN =
    { 0x3DD12A98, 0x5AFD, 0x4903, { 0xA1, 0x3F, 0xE1, 0x7E, 0x6C, 0x0B, 0xFE, 0x01 } };

// {F4DFD825-91A4-489f-855E-9AD9BEE55727}
static const GUID ELS_GUID_TRANSLITERATION_BENGALI_TO_LATIN =
    { 0xF4DFD825, 0x91A4, 0x489f, { 0x85, 0x5E, 0x9A, 0xD9, 0xBE, 0xE5, 0x57, 0x27 } };
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於擴充的語言服務](about-extended-linguistic-services.md)
</dt> </dl>

 

 



