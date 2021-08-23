---
description: 深入瞭解 ParameterInit 元素，此元素會定義 ParameterDef 元素之實例的值。
ms.assetid: d5419c40-43e9-49ff-a378-9aeb0757e400
title: ParameterInit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b961ede78b313e7fb3655024705a13f04edb947344493be4fe49ff14b5d00843
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119947854"
---
# <a name="parameterinit"></a>ParameterInit

本主題並非最新的。 如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。

定義 ParameterDef 元素之實例的值。 ParameterInit 元素是 ParameterRef 專案所做之參考的目標。

## <a name="element-tag"></a>元素標記

<ParameterInit>

## <a name="xml-attributes"></a>XML 屬性

下表列出可能與此元素相關的 XML 屬性。



| XML 屬性   | 詳細資料                                                                                                                               |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------|
| NAME<br/> | 保存 ParameterDef 專案的 name 屬性，該專案是要在目前檔的內容中初始化。<br/> |



 

如需詳細資訊，請參閱 [XML 屬性](xml-attributes.md) 一節。

## <a name="element-information"></a>項目資訊

下表列出可能是這個專案之父代的元素、可能是這個專案之子系的專案，以及專案本身的任何限制。



| 類別                   | 名稱或限制                                                                                                  |
|----------------------------|---------------------------------------------------------------------------------------------------|
| 父元素<br/> | PrintTicket (PrintTicket 根) <br/>                                                         |
| 子元素<br/>  | 值 (一) <br/>                                                                            |
| 這個元素<br/>    | 不允許任何字元資料。<br/> 不允許重複的子同級。<br/> |



 

## <a name="configuration-dependencies"></a>設定相依性

None

## <a name="example"></a>範例

下列範例會將參數初始化為1。 [ParameterDef](parameterdef.md)中的範例示範如何為此參數設定所有必要的屬性元素。

``` syntax
<psf:ParameterInit name="psk:PageCopyCount">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
</psf:ParameterInit>
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




