---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: d746bdd1-96c2-41f5-ad99-0b51c8ee8731
title: 舊版列印架構參考
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 881e986501950108c06e1e92303d13dc06265aae
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106991951"
---
# <a name="legacy-print-schema-reference"></a>舊版列印架構參考

本主題並非最新的。 如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。

您可以在 Microsoft .NET Framework 3.0、Microsoft Windows Vista 及更新版本中取得列印架構和相關技術。

列印架構會提供以 XML 為基礎的格式來表示和組織一組大量的屬性，這些屬性會以階層結構化的方式來描述作業格式或 PrintCapabilities。

列印架構是一種涵蓋了兩個元件、Print Schema 關鍵字和 Print Schema Framework 的廣義詞彙。 Print Schema 關鍵字檔是一個公用架構，它會定義一組可用來描述裝置屬性和列印工作格式的元素實例。 Print Schema Framework 是一個公用架構，可定義 XML 專案型別的階層式結構化集合，並指定如何一起使用專案類型。

Print Schema 關鍵字和 Print Schema Framework 構成兩個列印架構相關技術、PrintCapabilities 架構和 PrintTicket 架構的基礎。

請務必記住，列印架構的其中一個目標是要讓提供者支援架構延伸。 也就是說，提供者不會限制為只使用在 Print Schema Framework 上建的技術中，在 Print Schema 關鍵字中定義的屬性、功能、選項或 ParameterInit 實例。 提供者特定的元素實例可以自由地在 Print Schema 關鍵字中定義的元素實例內。 唯一的需求是提供者特定的 (，也就是私用) 屬性實例必須屬於與提供者清楚相關聯的命名空間。

-   [列印架構背景](print-schema-background.md)

-   [列印 Schema-Related 技術](print-schema-related-technologies.md)

-   [列印架構中使用的詞彙](terms-used-in-the-print-schema.md)

-   [列印架構的語法](syntax-of-the-print-schema.md)

-   [元素類型的摘要](summary-of-element-types.md)

-   [Print Schema Framework](print-schema-framework.md)

-   [列印架構公用關鍵字](print-schema-public-keywords.md)

-   [PrintCapabilities 架構和檔結構](printcapabilities-schema-and-document-construction.md)

-   [PrintTicket 架構和檔結構](printticket-schema-and-document-construction.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



