---
description: 瞭解 PrintTicket 和 PrintCapabilities 如何處理參數化和非參數化選項。
ms.assetid: 92438df1-afde-4038-853e-9b98f7e589ea
title: 參數化選項與 Nonparameterized 選項的比較
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4c788eaf2fa08f4f29a541a775d2bcbf523aa51
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407221"
---
# <a name="parameterized-options-versus-nonparameterized-options"></a>參數化選項與 Nonparameterized 選項的比較

本主題並非最新的。 如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。

PrintCapabilities 和 PrintTicket 提供者必須在 PrintTicket 驗證過程中正確處理參數化選項實例。 如 [選項定義](option-definitions.md)中所述，在 printticket 驗證中執行的一個步驟是在目前裝置的 PrintCapabilities 檔中尋找選項 (候選選項) 最符合 PrintTicket (參考選項) 中指定的選項。 當其中一個或兩個選項實例都已參數化時，有三種可能的案例必須由設備磁碟機定義的評分程式來處理：兩個選項實例都已參數化的情況，以及一個選項已參數化的兩個案例，另一個則不是。 在下列情況下，會假設 PrintTicket 選項中的參數化 ScoredProperty 實例與 PrintCapabilities 選項中的特定 ScoredProperty 之間有對應關係。 如果沒有任何對應，評分程式可以將這些 ScoredProperty 實例視為處理任何其他 noncorresponding ScoredProperty 實例的相同方式。

## <a name="case-1---parameterized-printticket-and-printcapabilities-document-options"></a>案例 1-參數化的 PrintTicket 和 PrintCapabilities 檔選項

在此情況下，在 PrintTicket) 中 (的參考選項以及在 PrintCapabilities) 檔中 (的候選選項會進行參數化。 存取候選選項所參考的 ParameterDef 實例， (在 PrintCapabilities 檔) 中，然後判斷 PrintTicket 中指定的 ParameterInit 值是否落在 ParameterDef 實例允許的範圍內。 如果是，請將此 ScoredProperty 視為相符。 否則，此 ScoredProperty 不相符。

## <a name="case-2---parameterized-printticket-option-nonparameterized-printcapabilities-document-option"></a>案例 2-參數型的 PrintTicket 選項，Nonparameterized PrintCapabilities Document 選項

在此情況下，PrintTicket 包含具有參數化選項的功能，而 PrintCapabilities 檔中的對應功能至少包含一個未參數化的選項。 即使 PrintCapabilities 檔也包含其他已參數化的選項實例，評分程式也必須套用至每個選項，因為目標是要識別最符合的選項。 用戶端必須能夠比較 nonparameterized 選項候選項目與已參數化的參考選項。

因為參數化選項出現在 PrintTicket 中，所以 ParameterInit 實例也應該存在，如先前的案例所示。 評分程式只要以 PrintTicket 的 ParameterInit 實例所指定的值，取代了 PrintTicket 的參數化選項中的任何 ParameterRef 實例即可。 這可有效地將參數化選項轉換成未參數化的選項。 此時可以使用傳統比對程式。

## <a name="case-3---nonparameterized-printticket-option-parameterized-printcapabilities-document-option"></a>案例 3-Nonparameterized PrintTicket 選項，參數化 PrintCapabilities 檔選項

在此情況下，在 PrintTicket 中的參考選項不會參數化，而 PrintCapabilities 檔中的候選選項會進行參數化。 存取 PrintCapabilities 檔中的 ParameterDef 實例，該檔是由 PrintTicket 中候選選項的 ParameterRef 實例所參考，並判斷對應 ScoredProperty 的參考選項中所定義的值是否落在 ParameterDef 實例允許的範圍內。 如果是，請將此 ScoredProperty 視為相符。 如果不是，則此 ScoredProperty 不相符。

請注意，您應該先判斷出兩個選項實例比對 ScoredProperty 實例的數目 (和精確度) ，與 ScoredProperty 實例是否包含明確值實例或 ParameterRef 實例無關。 候選選項可以是最符合的選項，即使它包含數個不符合參考選項的屬性實例，或是在參考選項中沒有對應屬性的屬性實例也是一樣。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



