---
description: 深入瞭解 PrintCapabilities 元素，其代表 PrintCapabilities 檔的根目錄。
ms.assetid: f503b62f-02e1-4621-8799-a8b6ad12f489
title: PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2158fd651849df2e4ea24c640065f1041569741a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407021"
---
# <a name="printcapabilities"></a>PrintCapabilities

本主題並非最新的。 如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。

PrintCapabilities 元素代表 PrintCapabilities 檔的根目錄。 PrintCapabilities 檔包含在指定特定裝置設定的情況下，描述支援的裝置屬性所需的所有資訊。

## <a name="element-tag"></a>元素標記

<PrintCapabilities>

## <a name="xml-attributes"></a>XML 屬性

下表列出可能與此元素相關的 XML 屬性。



| XML 屬性      | 詳細資料                                                                                                                                                                                                             |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| version<br/> | 指定定義元素類型及其結構的架構版本。 Version 屬性的類型為 integer。 目前的架構版本指定為 "1"。 這是必要屬性。 <br/> |



 

如需詳細資訊，請參閱 [XML 屬性](xml-attributes.md) 一節。

## <a name="element-information"></a>項目資訊

下表列出可能是這個專案之父代的元素、可能是這個專案之子系的專案，以及專案本身的任何限制。



| 類別                   | 詳細資料                                                                                                           |
|----------------------------|-------------------------------------------------------------------------------------------------------------------|
| 父元素<br/> | 僅限檔根目錄。<br/>                                                                                    |
| 子元素<br/>  | *功能* (零或多個) <br/> *ParameterDef* (零或多個) <br/> *屬性* (零或多個) <br/> |
| 這個元素<br/>    | 不允許任何字元資料。<br/> 不允許重複的子同級。<br/>                 |



 

## <a name="configuration-dependencies"></a>設定相依性

根項目可能沒有任何設定相依性。

## <a name="example"></a>範例

請參閱 [PrintCapabilities 檔範例](printcapabilities-document-example.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




