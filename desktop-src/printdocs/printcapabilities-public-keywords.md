---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 7f08747f-f7ff-4381-b2b9-1917e4708ee3
title: PrintCapabilities 公用關鍵字
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81d5e7b001a8106f95c830f0af5e99ee9821af64
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106975606"
---
# <a name="printcapabilities-public-keywords"></a>PrintCapabilities 公用關鍵字

本主題並非最新的。 如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。

下一節會指定可用於 PrintCapabilities 檔的使用者可設定元素和參數定義。

## <a name="user-configurable-elements-usage"></a>使用者可設定的專案使用方式

使用者可設定的元素代表可能出現在 PrintCapabilities 檔或 PrintTicket 中的列印架構公用關鍵字。 它們的目的是要代表特定裝置所支援的可設定裝置屬性，或由應用程式或使用者傳達列印設定意圖。

使用者可設定的專案可以參考參數參考元素。 如需詳細資訊，請參閱 [參數參考元素](parameter-reference-elements.md) 一節。

## <a name="parameter-definitions-usage"></a>參數定義使用方式

參數定義在列印功能檔中採用 ParameterDef 元素類型的形式。 ParameterDef 元素類型會使用 ParameterInit 專案類型在 PrintTicket 中初始化。 參數的值將使用 ParameterInit 元素來指定。 使用者可設定的關鍵字可以使用 ParameterRef 元素類型來參考參數定義。 如需詳細資訊，請參閱 [參數結構](parameter-constructs.md) 一節。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



