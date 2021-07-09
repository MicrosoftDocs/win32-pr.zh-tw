---
description: 取得 Option 元素的相關資訊。 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: feda78d9-58e7-4668-8a25-40e5fd8ad456
title: 選項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ac4318e6a79a3d4daa77f15901d032c66134bdd
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549376"
---
# <a name="option"></a>選項

本主題並非最新的。 如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。

Option 元素包含與此選項相關聯的所有屬性和 ScoredProperty 元素。

## <a name="element-tag"></a>元素標記

<Option>

## <a name="xml-attributes"></a>XML 屬性

下表列出可能與此元素相關的 XML 屬性。



| XML 屬性          | 詳細資料                                                                                                                                                                                                                                                                                                                                         |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 約束<br/> | PrintCapabilities 檔的這個屬性是選擇性的。<br/> 這個屬性會指出選項是否可供選取或使用。 這個 XML 屬性可以設定為下列其中一個值： None、PrintTicketSettings、AdminSetting 或 DeviceSettings。 <br/> 查看 [XML 屬性](xml-attributes.md)<br/> |
| NAME<br/>        | 保存選項的名稱，也就是標準選項或私用定義的選項。 這種方式會使用 XML 屬性來區分選項實例。 <br/>                                                                                                                                                        |



 

如需詳細資訊，請參閱 [XML 屬性](xml-attributes.md) 一節。

## <a name="element-information"></a>項目資訊

下表列出可能是這個專案之父代的元素、可能是這個專案之子系的專案，以及專案本身的任何限制。



| 類別                   | 詳細資料                                                                                                                                                                                                                                                                                          |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 父元素<br/> | 功能 <br/>                                                                                                                                                                                                                                                                              |
| 子元素<br/>  | *屬性* (零或多個) <br/> *ScoredProperty* (零或多個用於具有 XML 屬性 ' name ' 的選項;一或多個選項用於未使用 XML 屬性 ' name ' 的選項 \*) <br/> \* 只有在列印架構中定義的公用選項才能有 ' name ' 屬性，例如 DocumentNUp) <br/> |
| 這個元素<br/>    | 不允許任何字元資料。<br/> 不允許重複的子同級。<br/>                                                                                                                                                                                                |



 

## <a name="configuration-dependencies"></a>設定相依性

Option definition 元素可能沒有任何設定相依性。

## <a name="element-usage"></a>專案使用方式

Option 元素的目的是要說明裝置設定屬性（由功能元素代表）可以假設的其中一個狀態。 每個選項專案定義都包含一或多個 ScoredProperty 元素，這些元素會描述該選項的內建或基本特性。 為了促進可攜性和保存意圖，列印架構會定義許多常見的功能元素，以及每項功能的各種選項元素。 因此，在您建立自己的選項定義之前，請務必先使用列印架構定義的選項元素（如果可能的話）。 瞭解定義 Option 元素的程式，可提供 PrintCapabilities 檔和 PrintTickets 在 Microsoft .NET Framework 3.0 版和 Windows Vista 列印架構中的使用方式的實用深入解析。

## <a name="example"></a>範例

下列範例會定義選項的名稱。

``` syntax
<psf:Option name="psk:PrintFront" />
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




