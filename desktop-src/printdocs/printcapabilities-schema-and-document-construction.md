---
title: PrintCapabilities 架構和檔
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: c4727c17-3122-456c-967d-d1d6ce6a5402
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be1b8e2827e451fd8b1df477c33fe18d6203d10c
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106974775"
---
# <a name="printcapabilities-schema-and-document-construction"></a>PrintCapabilities 架構和檔結構

本主題並非最新的。 如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。

目前的 Win32 DevCaps 函式 (例如 GetDeviceCaps 或 DeviceCapabilities，在 Microsoft 平臺軟體發展工具組 (SDK) 檔中所述，) 嚴格地限制非驅動程式元件可取得的資訊類型，與列印裝置的功能和屬性有關。 不支援發行列印處理器的功能，也不會有列舉非標準功能的方法。 因此，驅動程式以外的元件無法用來建立完整的使用者介面。 此外，用戶端或應用程式無法完全判斷裝置的功能，或除了 Win32 DevCaps 函式所提供的列印佇列以外的其他功能。 目前的函式無法擴充，因此裝置無法發佈新的屬性或功能。

PrintCapabilities 架構的目的是要藉由提供這些函式所提供功能的超集合，來消除 Win32 DevCaps 函數的許多限制。 如果需要更多的功能，PrintCapabilities 檔的提供者可以藉由新增私用定義的元素實例，來擴充 print schema Framework 的條件約束中的列印架構關鍵字。 由於它依賴 XML 做為交換的媒體，因此 PrintCapabilities 檔的任何取用者都可以存取檔中的所有資料，而不受限制，也不會考慮與不同作業系統版本的相容性。 本節說明 PrintCapabilities 架構，並詳細說明其用法。

本章節的目標物件包括下列群組：

-   PrintTicket/PrintCapabilities 提供者介面的實作者

-   PrintCapabilities 的取用者

-   PrintTicket/PrintCapabilities 提供者介面的用戶端

上述清單中的第一個類別在本節的其餘部分稱為 PrintCapabilities 提供者。 第二和第三個類別稱為 PrintCapabilities 取用者。

## <a name="relationship-to-print-schema-and-printticket-schema"></a>與列印架構和 PrintTicket 架構的關聯性

PrintCapabilities 和 PrintTicket 架構都是列印架構的特殊部分。 這兩個列印架構子集之間的主要結構差異在於，PrintCapabilities 架構包含了不包含在 PrintTicket 架構中的屬性和 ParameterDef 實例，而 PrintTicket 架構則包含不包含在 PrintCapabilities 架構中的屬性和 ParameterInit 實例。 除了這些差異之外，PrintCapabilities 和 PrintTicket 架構通常會在內容、共用功能、選項、ScoredProperty 和值實例中彼此進行鏡像。 任何這類共用內容都必須保持在最新狀態。 例如，如果在 PrintCapabilities 架構的 PageMediaSize 功能中進行了變更，則必須在 PrintTicket 架構中進行相同的變更。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



