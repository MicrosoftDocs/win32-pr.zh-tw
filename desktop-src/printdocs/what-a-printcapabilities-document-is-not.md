---
description: 瞭解 PrintCapabilities 檔不打算提供的部分功能和資訊。
ms.assetid: 87a897cd-d3aa-488a-b129-9837d3500d0d
title: PrintCapabilities 檔不是什麼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 180c303a21dbed39908d87831a1e01e2965b09a68e1e23a6e1f8793e247556f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119718538"
---
# <a name="what-a-printcapabilities-document-is-not"></a>PrintCapabilities 檔不是什麼

本主題並非最新的。 如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。

您可以列出 PrintCapabilities 檔不打算提供的部分功能和資訊。

PrintCapabilities 檔：

-   不代表 (設定相依) 資料的多重值。

    每個 PrintCapabilities 檔都是針對特定設定所建立。 檔中沒有任何屬性或 ScoredProperty 可以有相依于特定設定的值。 在初始架構版本中，PrintCapabilities 提供者必須處理輸入 PrintTicket，然後建立 PrintCapabilities 檔，其中包含適用于 PrintTicket 中所指定設定的屬性值。

-   不包含條件約束資訊。

    PrintCapabilities 檔不會指出允許哪些設定，哪些是不允許的設定。 在初始架構版本中，PrintCapabilities 提供者必須儲存驗證設定所需的任何資訊、提供驗證輸入 PrintTicket 的方法，並在指定的 PrintTicket 違反一或多個條件約束的情況下傳回更正的 PrintTicket。

-   不包含動態裝置資訊。

    建立 PrintCapabilities 檔時，需要太多額外負荷來保存快速變更的狀態資訊，例如筆墨層級、每個紙匣剩餘的紙張，或是紙匣狀態。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



