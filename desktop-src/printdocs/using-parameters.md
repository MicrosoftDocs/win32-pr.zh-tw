---
description: 瞭解如何在 PrintCapabilities 檔中使用參數。 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 4a596604-8a0d-4971-96f3-643727312cfc
title: 使用參數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dc19b6c2b6deb269c0d3a34140bc0e9816febc86d33adfdb6ed0c91fe38f666
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118469323"
---
# <a name="using-parameters"></a>使用參數

本主題並非最新的。 如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。

除了適當計分包含 ParameterRef 實例的選項 (請參閱) 、PrintCapabilities 或 PrintTicket 提供者的 [參考參數](referencing-parameters.md) ，以及用戶端必須準備好處理下列涉及參數的狀況。

使用者介面 (UI) 用戶端必須提示使用者提供參數初始化運算式 (值給適當時間的指定參數) ，以便將適當的 ParameterInit 元素插入至 PrintTicket。 UI 用戶端必須能夠區分這兩種類型的參數（無條件強制），並有條件地強制性，而且必須能夠適當地處理每個型別。 若為無條件強制參數，UI 必須確保為此類型的參數提供 ParameterInit 元素。 針對有條件的強制參數，如果在 PrintTicket 中選取的選項參考參數，則 UI 必須提供 ParameterInit 值。 參數的強制狀態是在 ParameterDef 實例中指定。 如需詳細資訊，請參閱 [ParameterDef 和 ParameterInit 元素](parameterdef-and-parameterinit-elements.md)。 UI 用戶端應該驗證使用者提供的 ParameterInit 值，以確認它們符合 ParameterDef 實例中指定的需求。

PrintTicket 提供者也應該檢查 PrintTicket 提供的 ParameterInit 實例，以確認所有必要的參數都存在，而且它們滿足 ParameterDef 實例中指定的需求。 當 ParameterInit 值無效或遺失時，驗證程式代碼應該提供合理的預設值。 請注意，ParameterDef 允許針對此用途提供預設值。 此外，如果有涉及參數的條件約束，例如「如果 *CopyCount* 大於 N，則請勿使用小型容量輸入 bin」。「PrintTicket 驗證程式代碼應該偵測到此條件約束，並修改 printticket 以避免啟用條件約束。

如果在 PrintTicket 中指定的參數上有 PrintCapabilities 的相依性，PrintCapabilities 提供者必須監視 ParameterInit 值並產生適當的 PrintCapabilities 檔。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



