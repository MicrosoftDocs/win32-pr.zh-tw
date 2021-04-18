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
# <a name="transliteration-services"></a><span data-ttu-id="aa27b-103">音譯服務</span><span class="sxs-lookup"><span data-stu-id="aa27b-103">Transliteration Services</span></span>

<span data-ttu-id="aa27b-104">ELS 音譯服務會將 UTF-16 文字從一個書寫系統對應到另一個寫入系統。</span><span class="sxs-lookup"><span data-stu-id="aa27b-104">The ELS transliteration services map UTF-16 text from one writing system to another writing system.</span></span> <span data-ttu-id="aa27b-105">每個服務實際上都是套用至一組特定輸入和輸出 Unicode 腳本的資料，而實際的音譯是在 ELS 平臺內部。</span><span class="sxs-lookup"><span data-stu-id="aa27b-105">Each service is really data applying to a specific set of input and output Unicode scripts, and the actual transliteration is internal to the ELS platform.</span></span> <span data-ttu-id="aa27b-106">應用程式可以選擇性地列舉特定輸入和輸出腳本的可用服務，並選取所需的服務。</span><span class="sxs-lookup"><span data-stu-id="aa27b-106">The application can optionally enumerate the available services for specific input and output scripts and select the service that it requires.</span></span>

<span data-ttu-id="aa27b-107">平臺會維護 ELS 音譯服務的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="aa27b-107">The platform maintains metadata for the ELS transliteration services.</span></span> <span data-ttu-id="aa27b-108">每個服務的中繼資料會提供服務的描述，並列出服務所支援的輸入和輸出腳本。</span><span class="sxs-lookup"><span data-stu-id="aa27b-108">Metadata for each service provides a description of the service and lists the input and output scripts that the service supports.</span></span> <span data-ttu-id="aa27b-109">中繼資料是由 [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices)函數所抓取的 [**對應 \_ 服務 \_ 資訊**](/windows/desktop/api/Elscore/ns-elscore-mapping_service_info)結構所表示。</span><span class="sxs-lookup"><span data-stu-id="aa27b-109">The metadata is represented by a [**MAPPING\_SERVICE\_INFO**](/windows/desktop/api/Elscore/ns-elscore-mapping_service_info) structure retrieved by the [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) function.</span></span>

## <a name="input-to-a-transliteration-service"></a><span data-ttu-id="aa27b-110">音譯服務的輸入</span><span class="sxs-lookup"><span data-stu-id="aa27b-110">Input to a Transliteration Service</span></span>

<span data-ttu-id="aa27b-111">音譯服務的輸入是一個書寫系統中的 UTF-16 文字。</span><span class="sxs-lookup"><span data-stu-id="aa27b-111">The input to a transliteration service is UTF-16 text in one writing system.</span></span>

## <a name="output-of-a-transliteration-service"></a><span data-ttu-id="aa27b-112">音譯服務的輸出</span><span class="sxs-lookup"><span data-stu-id="aa27b-112">Output of a Transliteration Service</span></span>

<span data-ttu-id="aa27b-113">音譯服務的輸出是對應至第二個書寫系統的 UTF-16 文字。</span><span class="sxs-lookup"><span data-stu-id="aa27b-113">The output of a transliteration service is UTF-16 text mapped to a second writing system.</span></span> <span data-ttu-id="aa27b-114">如果輸入文字的任何指定區塊都沒有適當的音譯對應，區塊會維持不變。</span><span class="sxs-lookup"><span data-stu-id="aa27b-114">If no appropriate transliteration mapping is available for any given chunk of the input text, the chunk remains unchanged.</span></span>

## <a name="transliteration-service-operation"></a><span data-ttu-id="aa27b-115">音譯服務作業</span><span class="sxs-lookup"><span data-stu-id="aa27b-115">Transliteration Service Operation</span></span>

<span data-ttu-id="aa27b-116">音譯服務會適當地將輸入腳本中的 Unicode 文字對應至輸出腳本、字元或詞彙。</span><span class="sxs-lookup"><span data-stu-id="aa27b-116">A transliteration service maps Unicode text from an input script to an output script, character by character or term by term, as appropriate.</span></span> <span data-ttu-id="aa27b-117">應用程式可以選擇在呼叫 [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices)時指定輸入和輸出腳本，或藉由提供服務 GUID，來取得感興趣的特定音譯服務。</span><span class="sxs-lookup"><span data-stu-id="aa27b-117">The application can choose to obtain the specific transliteration service of interest by specifying input and output scripts when calling [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices), or by providing the service GUID.</span></span> <span data-ttu-id="aa27b-118">應用程式的另一個選項是在呼叫 **MappingGetServices** 時，藉由指定服務類別 "音譯" 來列舉所有可用的音譯服務。</span><span class="sxs-lookup"><span data-stu-id="aa27b-118">Another option for the application is to enumerate all available transliteration services by specifying the service category "Transliteration" when calling **MappingGetServices**.</span></span> <span data-ttu-id="aa27b-119">在此情況下，應用程式會呼叫每個服務並將結果與原始文字進行比較，以查看特定服務的作業是否已變更結果。</span><span class="sxs-lookup"><span data-stu-id="aa27b-119">In this case, the application calls each service and compares the results with the original text to see if the results have been changed by the operation of a particular service.</span></span>

<span data-ttu-id="aa27b-120">應用程式可以透過呼叫 [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext)來要求 ELS 音譯服務的文字辨識。</span><span class="sxs-lookup"><span data-stu-id="aa27b-120">The application can request text recognition for an ELS transliteration service with a call to [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext).</span></span> <span data-ttu-id="aa27b-121">當它收到要求時，音譯服務會配置一個緩衝區來包含所轉譯的資料，然後針對應用程式所提供的輸入字串中的每個程式碼點執行文字辨識。</span><span class="sxs-lookup"><span data-stu-id="aa27b-121">When it receives the request, the transliteration service allocates a buffer to contain the transliterated data, and then performs text recognition for each code point in the input string supplied by the application.</span></span>

> [!Note]  
> <span data-ttu-id="aa27b-122">原始文字和轉譯的文字可能會有不同的長度。</span><span class="sxs-lookup"><span data-stu-id="aa27b-122">The original text and the transliterated text might have different lengths.</span></span>

 

## <a name="transliteration-service-guids"></a><span data-ttu-id="aa27b-123">音譯服務 Guid</span><span class="sxs-lookup"><span data-stu-id="aa27b-123">Transliteration Service GUIDs</span></span>

<span data-ttu-id="aa27b-124">音譯服務的 Guid 是在 Elssrvc 中宣告，如下列程式碼所示。</span><span class="sxs-lookup"><span data-stu-id="aa27b-124">The GUIDs for the transliteration services are declared in Elssrvc.h, as shown in the following code.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="aa27b-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="aa27b-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa27b-126">關於擴充的語言服務</span><span class="sxs-lookup"><span data-stu-id="aa27b-126">About Extended Linguistic Services</span></span>](about-extended-linguistic-services.md)
</dt> </dl>

 

 



