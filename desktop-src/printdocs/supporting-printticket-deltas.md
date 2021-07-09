---
description: 瞭解如何支援 PrintTicket 差異。 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 80fdc8f1-4fda-4102-9b27-16d9acb4d077
title: 支援 PrintTicket 差異
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7f72f82875d0207ed232f4db897c78295ce2ee0
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548776"
---
# <a name="supporting-printticket-deltas"></a>支援 PrintTicket 差異

本主題並非最新的。 如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。

PrintTicket 提供者介面具有可用來對現有的 PrintTicket 進行累加式變更的方法。 增量的 PrintTicket 變更可以在稱為 PrintTicket delta 的部分 PrintTicket 中指定。 修改過的 PrintTicket 是藉由合併 PrintTicket delta 與現有的 PrintTicket 來建立。 如需有關具有 PrintTicket 差異之方法的詳細資訊，請參閱即將推出的 PrintTicket 提供者介面檔。

處理 PrintTicket 差異時，必須執行下列步驟。

1.  識別現有的 PrintTicket (目標 PrintTicket) 和 PrintTicket 差異通用的功能或 ParameterInit 實例。

    -   針對目標 PrintTicket 和 PrintTicket 差異通用的每個功能，以 PrintTicket 差異中的對應功能取代目標 PrintTicket 中的功能。

    -   針對目標 PrintTicket 和 PrintTicket 差異通用的每個 ParameterInit，將目標 PrintTicket 中的 ParameterInit 取代為 PrintTicket delta 中對應的 ParameterInit。

2.  將 PrintTicket delta 中所有剩餘的功能和 ParameterInit 實例複製到目標 PrintTicket。

3.  如果您的衝突解決演算法允許在 PrintTicket 本身指定優先權，您可以選擇提高在 PrintTicket delta 中命名的功能和 ParameterInit 實例的優先順序。

4.  執行 printticket 驗證，如 [Printticket 驗證檢查清單](printticket-validation-checklist.md)中所述。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



