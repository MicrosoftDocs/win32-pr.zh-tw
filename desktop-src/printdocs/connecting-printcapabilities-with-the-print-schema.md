---
description: 瞭解一般 PrintCapabilities 架構，其中涵蓋各種專案類型的結構、用途和使用。
ms.assetid: 2f6c51a3-003c-4d68-9e4d-9be5d325a477
title: 將 PrintCapabilities 與列印架構連接
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 661a8eb93c6f788381713c0c6620e8a09a53648f
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409641"
---
# <a name="connecting-printcapabilities-with-the-print-schema"></a>將 PrintCapabilities 與列印架構連接

本主題並非最新的。 如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。

一般 PrintCapabilities 架構涵蓋各種元素類型的結構、用途和使用。 它會指定名稱屬性，用來定義每個元素類型的特定實例。 它會指定 PrintCapabilities 作者可以使用 Print Schema 關鍵字所定義之專案的實例，或者，只要這些私用定義的實例定義在明確識別為其本身的命名空間中，就可能會引入自己的私用實例。  (PrintCapabilities 作者也可以使用先前在另一個私用命名空間中定義的實例。 ) 

列印架構關鍵字檔會定義每個專案類型的特定實例，可用於 PrintCapabilities 檔和 PrintTickets 中。 它也記載了其用途和使用方式。 列印架構關鍵字檔也會定義數個元素類型的實例，如下所示：

-   位於 PrintCapabilities 檔根目錄的屬性和子屬性實例

    -   這些元素說明裝置的各種層面和功能，並提供描述裝置的常見詞彙。

-   屬於 Feature 元素子系的屬性和子屬性實例

    -   這些元素會描述與特定功能相關的各種層面。

-   屬於 Option 元素子系的屬性和子屬性實例

    -   這些元素會描述裝置的各個層面和功能，而這些功能相依于特定功能所選的選項。 這些可能會由位於 PrintCapabilities 檔根目錄的屬性實例取代，但在某些情況下可提供額外的便利性。 如需詳細資訊，請參閱 [加入屬性實例](adding-property-instances.md)。

<!-- -->

-   ScoredProperty 實例

    -   ScoredProperty 實例會定義用來定義選項特性的語言。 在 Print Schema 關鍵字中定義的 ScoredProperty 實例，可讓許多不同的合作物件為許多不同的合作物件撰寫的選項實例，讓許多裝置都能成為可攜性，並可供任何其他設備磁碟機或 PrintCapabilities 或 PrintTicket 提供者瞭解。

-   ScoredProperty 值實例

    -   針對提供 ScoredProperty 實例的相同原因，提供這些值實例。

-   功能實例

    -   每個選項都必須屬於特定功能，因此需要定義功能本身。

-   ParameterDef 實例

    -   列印架構關鍵字提供的 ParameterDef 實例也會針對其中包含的每個屬性定義一個值。 PrintCapabilities 提供者可自由修改可變更之屬性實例的值實例。 如需可以變更哪些屬性實例，以及哪些 (無法變更) 的詳細資訊，請參閱 [ParameterDef 和 ParameterInit 元素](parameterdef-and-parameterinit-elements.md)。

請務必注意，PrintCapabilities 架構不會命名任何選項實例。 選項實例的特性僅由其整體 ScoredProperty 實例所組成。 常見的誤解是，使用 ' name ' 屬性定義選項來識別選項實例，但這是不正確的。 選項元素不需要為同一個選項實例的唯一，也不能使用 ' name ' 屬性來定義所需的選項。

Print Schema 關鍵字檔會定義 PrintCapabilities 和 PrintTicket 架構中的所有實例名稱屬性所屬的標準命名空間。 專案類型所使用的所有元素類型標記和 XML 屬性也都屬於這個命名空間。

針對 PrintCapabilities 架構中定義的每個實例，PrintCapabilities 架構會同時指定名稱屬性和實例的位置。 在 PrintCapabilities 檔或 PrintTicket 中使用這個實例時，提供者和用戶端都必須保留這兩者。

Print Schema 關鍵字檔會將某些實例指定為強制性。 這些實例必須出現在每個 PrintCapabilities 檔中，而且必須使用有效值正確地初始化。 列印架構關鍵字中未指定為強制的所有實例都是選擇性的。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



