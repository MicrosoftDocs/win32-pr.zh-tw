---
description: 瞭解 ParameterRef 元素，它會定義 ParameterInit 專案的參考，以及它如何與 ScoredProperty 搭配使用。
ms.assetid: 35e1ccc2-ffc1-47a6-aba8-5a5cb442e8ae
title: ParameterRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ff3b0e16f53e8399a5bbbb5974a05fd6886cdd2
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407181"
---
# <a name="parameterref"></a>ParameterRef

本主題並非最新的。 如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。

ParameterRef 元素會定義 ParameterInit 元素的參考。 包含 ParameterRef 元素的 ScoredProperty 元素沒有明確設定的 Value 元素。 相反地，ScoredProperty 專案會從 ParameterRef 元素所參考的 ParameterInit 元素接收其值。

## <a name="element-tag"></a>元素標記

<ParameterRef>

## <a name="xml-attributes"></a>XML 屬性

下表列出可能與此元素相關的 XML 屬性。



| XML 屬性   | 詳細資料                                                                                                                        |
|-----------------|--------------------------------------------------------------------------------------------------------------------------------|
| NAME<br/> | 保留目前檔內容中所參考之 ParameterDef 元素的 name 屬性。<br/> |



 

如需詳細資訊，請參閱 [XML 屬性](xml-attributes.md) 一節。

## <a name="element-information"></a>項目資訊

下表列出可能是這個專案之父代的元素、可能是這個專案之子系的專案，以及專案本身的任何限制。



| 類別                   | 詳細資料                                                                                           |
|----------------------------|---------------------------------------------------------------------------------------------------|
| 父元素<br/> | ScoredProperty <br/>                                                                        |
| 子元素<br/>  | 無允許。<br/>                                                                        |
| 這個元素<br/>    | 不允許任何字元資料。<br/> 不允許重複的子同級。<br/> |



 

## <a name="configuration-dependencies"></a>設定相依性

ParameterRef 元素可能沒有任何設定相依性。

## <a name="example"></a>範例

下列範例說明如何使用 ParameterRef 元素，讓使用者輸入自訂媒體大小參數。

``` syntax
<psf:Option name="psk:CustomMediaSize" constrained="psk:None">
  <psf:ScoredProperty name="psk:MediaSizeWidth">
    <psf:ParameterRef name="psk:PageMediaSizeMediaSizeWidth" />
  </psf:ScoredProperty>
  <psf:ScoredProperty name="psk:MediaSizeHeight">
    <psf:ParameterRef name="psk:PageMediaSizeMediaSizeHeight" />
  </psf:ScoredProperty>
  <psf:Property name="psk:DisplayName">
    <psf:Value xsi:type="xs:string">Fabrikam User Custom</psf:Value>
  </psf:Property>
</psf:Option>
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




