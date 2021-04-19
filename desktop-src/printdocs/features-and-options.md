---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 8084fa15-85e5-4c8d-b585-8c349482a6eb
title: 功能與選項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 866cead02021b8d933ca03483e77de832d8d094a
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106992118"
---
# <a name="features-and-options"></a>功能與選項

本主題並非最新的。 如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。

功能/選項和參數結構會在 PrintCapabilities 檔中用來代表構成裝置設定定義的裝置屬性。 如需功能/選項結構的範例，請考慮能夠以數種解析度列印的列印裝置。 定義解析的裝置屬性可以表示為功能實例，其中每個可能的輸出解析度值都表示為個別的選項實例。 其中一個選項實例可以代表 300 DPI 的解析度，另一個則代表 600 DPI 的解析度等等。

請注意，列印架構要求每個 PrintCapabilities 檔中報告的功能、選項和 ParameterDef 實例清單必須保持不變，而不受設定影響。 這可讓您以明確的方式表示設定的設定和相依性。 這項需求的含意是，不論任何其他功能或 subfeature 的設定為何，每個功能和 subfeature 都必須有妥善定義的設定。 因此，每個 subfeature 都必須有相當於無 op ([關閉]、[已停用] 或 [無] 設定) 的選項，當使用者在父功能中選取 [無操作] 選項時，就會自動為所有子功能選取。 相反地，當其中一個子功能設定為啟用的選項時，也會啟用父功能和其他相關聯的子功能。 在此同時，PrintTicket 提供者必須確保在 PrintTicket) 驗證期間 (，因為所有功能和 subfeature 實例的設定都已定義，無論裝置設定為何，以及 subfeature 設定與父功能的設定一致。 這樣可確保裝置不會有不一致的 PrintTicket，其中某些子功能表示已啟用裝訂，但其他子功能表示已停用裝訂。

請注意，PrintCapabilities 作者不需要利用功能元素的嵌套功能。 如果您想要的話，可以將所有的功能實例呈現為一般結構，作為彼此的同級。 另外也請注意，只要將所有子功能移至根層級，就可以壓平合併功能實例的集合。 唯一必須採取的預防措施是確保這些功能實例的名稱屬性是唯一的。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



