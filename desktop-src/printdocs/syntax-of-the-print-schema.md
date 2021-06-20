---
description: 瞭解列印架構的語法，此語法以 XML 語法表示，並由少量的元素類型所組成。
ms.assetid: d67518e3-c379-4a50-aeda-31afaa7f05dd
title: 列印架構的語法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ef52dbdbdfacc2d3cc947b46558319577a75b1b
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405291"
---
# <a name="syntax-of-the-print-schema"></a>列印架構的語法

本主題並非最新的。 如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。

列印架構是以 XML 語法表示。 因此讀者應該熟悉 XML 語法和詞彙，例如專案、專案標記、元素內容、屬性和命名空間。 Print Schema Framework 是由少量的元素類型所組成;每個元素類型都可在以列印架構為基礎的技術中提供特定用途。

專案類型是由其 XML 元素標記所區分。 Print Schema Framework 會藉由為每個專案類型表示允許做為子專案的元素類型，來定義相依技術的整體結構和組織。

許多專案類型都與名稱屬性的相同類型的其他專案不同，這在架構中扮演著重要的角色。 Name 屬性可用來識別每個元素類型的實例。 Print Schema 關鍵字會為許多專案類型的名稱屬性定義一組值。 在大多數情況下，提供者可以將自己的值指派給 name 屬性。 它們只需要確保值是以提供者唯一的命名空間限定的 XML QNames。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



