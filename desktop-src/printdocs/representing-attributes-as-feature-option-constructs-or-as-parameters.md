---
description: 以功能/選項結構或參數表示屬性。 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 055e502d-631f-49d2-8577-65396373d478
title: 將屬性工作表示為功能/選項結構或參數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c93f4de56709ed310a7f0aa259b1dbfd3377ed42
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120053"
---
# <a name="representing-attributes-as-featureoption-constructs-or-as-parameters"></a>將屬性工作表示為功能/選項結構或參數

本主題並非最新的。 如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。

PrintCapabilities 檔的作者會定義組成設定的裝置屬性。 在 PrintCapabilities 檔中，作者可以選擇將裝置屬性工作表示為功能/選項結構或參數結構。

如果裝置屬性有相對較少的可能狀態，而不屬於任何明顯的模式，則功能/選項結構通常是較佳的選擇。 例如，如果 PageMediaSize 裝置屬性的允許值為字母、合法、A4ISO、Tabloid 和 Envelope10，則功能/選項結構會是標記法的較佳選擇。 由於與表示允許值沒有明確列舉相關聯的困難和不明確，因此參數結構不適合 PageMediaSize 屬性。

如果裝置屬性可由整數範圍表示，參數表示通常是較佳的選擇，特別是包含許多值的範圍。 例如，如果特定印表機模型的 CopyCount 裝置屬性可以範圍從1到99999，則應該藉由定義 ParameterDef 實例將此屬性分類為參數。 將值指派給 ParameterDef 專案的 MinValue 和 int32.maxvalue 標準屬性實例，以定義 JobCopyCount 屬性的值範圍。 由於必須明確地列為 Option 元素的大量值，因此功能/選項表示不適合 JobCopyCount 裝置屬性。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



