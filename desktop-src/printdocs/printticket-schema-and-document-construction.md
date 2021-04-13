---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 573c2c82-aeb9-4ef2-8a1b-40b4db6ac6e4
title: PrintTicket 架構和檔結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffe386638a7f119c52982f1911d602691455343f
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "104195819"
---
# <a name="printticket-schema-and-document-construction"></a>PrintTicket 架構和檔結構

本主題並非最新的。 如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。

目前使用 DEVMODE 結構指定裝置設定資訊的方法，有數項限制。 首先，DEVMODE 結構是二進位結構，可能會導致不同版本的問題。 其次，它會分成 nonextensible 的公開部分和私用部分，只能由驅動程式存取，而且只能由建立它的特定驅動程式存取。 PrintTicket 格式使用以 XML 為基礎的列印架構架構來表示設定資訊，以消除這些 DEVMODE 結構的缺點。

PrintTicket 架構會解決剛剛提到的兩個問題。 首先，PrintTicket 架構是以 XML 為基礎的文字檔，因此會排除擴充性和版本設定的問題。 其次，所有用戶端都可以使用設定資訊，也就是說，任何用戶端或提供者都可以儲存和取出 PrintTicket 中包含的任何資訊。 選項的描述方式是使用 Print Schema Framework 和衍生的 PrintCapabilities 檔所使用的相同技術。 基於這個理由，PrintTicket 可提供要實現之選項定義模型的所有潛在可攜性優點。 如需詳細資訊，請參閱 [Print Schema Framework](print-schema-framework.md) 。 本章節的目標物件包括下列群組：

-   PrintTicket/PrintCapabilities 提供者介面的實作者

-   PrintTicket 的取用者

-   PrintTicket/PrintCapabilities 提供者介面的用戶端

上述清單中第一個類別目錄的成員在本節的其餘部分稱為「PrintTicket 提供者」。 最後兩個類別的成員稱為「PrintTicket 取用者」。

## <a name="relationship-to-print-schema-and-printcapabilities-schema"></a>與列印架構和 PrintCapabilities 架構的關聯性

PrintTicket 和 PrintCapabilities 架構都是列印架構的特殊部分。 這兩個列印架構子集之間的主要結構差異，是 PrintTicket 架構包含未包含在 PrintCapabilities 架構中的屬性和 ParameterInit 實例，而 PrintCapabilities 架構則包含不包含在 PrintTicket 架構中的屬性和 ParameterDef 實例。 除了這些差異之外，PrintCapabilities 和 PrintTicket 架構通常會在內容、共用功能、選項、ScoredProperty 和值實例中彼此進行鏡像。 任何這類共用內容都必須保持在最新狀態。 例如，如果在 PrintCapabilities 架構的 MediaSize 功能中進行了變更，則必須在 PrintTicket 架構中進行相同的變更。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



