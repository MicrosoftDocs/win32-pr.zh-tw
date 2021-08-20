---
description: 瞭解 PrintCapabilities 檔中的參數。 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: d317d052-c207-412a-896e-09cb57b0dd5f
title: PrintCapabilities 檔中的參數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67a2d88e75372cfc2f1301c630116c12510b37c91aadbf94a04ac07a3f4906cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117867990"
---
# <a name="parameters-in-the-printcapabilities-document"></a>PrintCapabilities 檔中的參數

本主題並非最新的。 如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。

如 [參數參考](parameter-reference-elements.md)專案中所述，可從選項實例中參考 ParameterInit 元素，但參數結構也具有與這種類型的元素無關的用途。

裝置設定屬性的範例，很適合用於參數標記法 CopyCount。 您可以輕鬆且精確地定義此裝置設定屬性的允許值，而不需要明確列出每個值。 雖然有可能是很繁瑣的，若要在自己的選項中列出每個 CopyCount 值，某些裝置設定屬性就無法使用功能/選項結構來表示。 例如，假設有一個裝置接受文字字串，然後用來在每個輸出頁面上產生虛擬水位線。 所有可能的文字字串集合都無法輕易地明確列舉，但是可以使用 ParameterDef 元素輕鬆描述文字字串。

Print Schema 關鍵字檔會定義許多常用的參數結構，但 PrintCapabilities 提供者可自由定義自己的其他專案。 不過，這些私用定義的參數結構無法移植到其他裝置，因為另一方提供的 PrintCapabilities 檔不會定義這類參數結構。 無論是架構定義或私下定義，ParameterDef 實例都必須存在於 PrintCapabilities 檔中，用戶端才能辨識並使用參數。 這些參數稱為 *指定的參數*。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



