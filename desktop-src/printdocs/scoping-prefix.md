---
description: 範圍前置詞是將文字標籤預先附加至 schema 關鍵字，以提供內容約制，包括作業、檔和頁面。
ms.assetid: 4bad85d7-a933-43fe-9d79-4835d92c82d6
title: 範圍前置詞
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2c027de94fda403eb58905e536d8c6256cb2d6c
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404901"
---
# <a name="scoping-prefix"></a>範圍前置詞

本主題並非最新的。 如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。

範圍前置詞是一種文字標籤，預先附加至 schema 關鍵字以提供內容相關的範圍。 這可讓您以預先定義的方式將特定且易懂的內容 ascribing 至關鍵字。 Print Schema Feature、ParameterDef、ParameterInit 和 ParameterRef 和根層級屬性關鍵字元素必須有下列其中一個範圍前置詞：「作業」、「檔」或「頁面」。

## <a name="interpretation-of-the-scoping-prefix-with-printticket-content"></a>使用 PrintTicket 內容進行範圍前置詞的解讀

PrintTicket 可以細分為三個代表高階工作的內容層級、作業中的檔，以及每份檔中的頁面。 這些層級會根據明確程度進行排名;作業層級最普遍，而檔層級和頁面層級是最特定的。 作業包含一或多個檔，而檔是由一或多個頁面所組成。

## <a name="job-level-prefix"></a>作業層級前置詞

作業層級票證包含所有預定要套用至整個作業的工作格式設定。 作業層級票證中允許任何具有「作業」、「檔」或「頁面」範圍前置詞的元素。

作業層級票證中指定的「檔」和「頁面」前置設定，會自動套用至檔和頁面層級的票證。

## <a name="document-level-prefix"></a>檔層級前置詞

檔層級票證包含任何預定要套用至工作中一或多個檔的工作格式設定。 這些可能包括先前在作業層級票證中指定的設定。 檔層級票證中只允許範圍前置詞為 "Document" 或 "Page" 的元素。

檔層級票證可能包含先前由作業層級票證指定的檔前置詞設定。

## <a name="page-level-prefix"></a>頁面層級前置詞

頁面層級票證包含任何要套用至一或多個頁面的工作格式設定， (不限於單一檔) 。 這些可能包括先前在作業或檔層級票證中指定的設定。 頁面層級票證中只允許範圍前置詞為 "Page" 的元素。

頁面層級票證可能包含先前由作業層級票證和/或檔層級票證所指定的「頁面」前置詞設定。

## <a name="prefix-usage-within-a-printticket-or-print-capabilities-document"></a>在 PrintTicket 或列印功能檔中使用前置詞

PrintTicket 和 PrintCapabilities 檔不能包含多個關鍵字，這些關鍵字只會在範圍前置詞中不同。 例如，PrintCapabilities 檔不能同時指定 JobInputBin 和 PageInputBin。 不過，列印功能檔可能會同時指定 JobDuplexAllDocumentsContiguously 和 DocumentDuplex，因為這些會被視為不同的功能，因為它們表現不同的行為。 此範例也適用于單一 PrintTicket。

## <a name="prefix-conflict-management"></a>前置詞衝突管理

設定之間的關鍵字衝突定義為，以 XML 屬性 "name" 表示的相同根層級列印架構元素，出現在多個層級票證中。 如果沒有衝突，前置詞範圍專案可能會從更一般的票證向下推送或繼承至更特定的票證。 如果發生衝突，則會優先使用最特定票證的設定。 也就是說，頁面層級票證中的每個頁面設定會覆寫檔或作業層級票證中的每頁設定相同的設定。 同樣地，檔層級票證中的檔設定會優先于作業層級票證中的檔設定。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



