---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: fe6bd921-cbf3-4cca-afae-82d3822206ba
title: PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3d2e225eb38584e290db55c33594be80d0d7999
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106986458"
---
# <a name="printticket"></a>PrintTicket

本主題並非最新的。 如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。

PrintTicket 元素是 PrintTicket 檔的根項目。 PrintTicket 元素包含輸出工作所需的所有工作格式資訊。

## <a name="element-tag"></a>元素標記

<PrintTicket>

## <a name="xml-attributes"></a>XML 屬性

下表列出可能與此元素相關的 XML 屬性。



| XML 屬性      | 詳細資料                                                                                                                                                                                   |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| version<br/> | 指定定義專案類型和其結構的架構版本（整數類型的常值）。 目前的架構版本為 "1"。 這是必要屬性。 <br/> |



 

如需詳細資訊，請參閱 [XML 屬性](xml-attributes.md) 一節。

## <a name="element-information"></a>項目資訊

下表列出可能是這個專案之父代的元素、可能是這個專案之子系的專案，以及專案本身的任何限制。



| 類別                   | 詳細資料                                                                                                            |
|----------------------------|--------------------------------------------------------------------------------------------------------------------|
| 父元素<br/> | 僅限檔根目錄。<br/>                                                                                     |
| 子元素<br/>  | *功能* (零或多個) <br/> *ParameterInit* (零或多個) <br/> *屬性* (零或多個) <br/> |
| 這個元素<br/>    | 不允許任何字元資料。<br/> 不允許重複的子同級。<br/>                  |



 

## <a name="configuration-dependencies"></a>設定相依性

設定相依性只適用于 PrintCapabilities 檔中的元素。

## <a name="example"></a>範例

請參閱 [PrintTicket 範例](printticket-example.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




