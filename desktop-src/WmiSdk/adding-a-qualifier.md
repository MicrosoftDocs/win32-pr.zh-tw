---
description: 辨識符號是提供類別、實例、屬性、方法或參數之詳細資訊的資料字串。
ms.assetid: 6984b575-b365-49dd-aeab-a763430f434c
ms.tgt_platform: multiple
title: 新增限定詞
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5a6f18f2b79bcd25b2b4ca75811157c9091e6eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975565"
---
# <a name="adding-a-qualifier"></a>新增限定詞

辨識符號是提供類別、實例、屬性、方法或參數之詳細資訊的資料字串。

下列類別定義是具有類別限定詞的衍生類別範例。

``` syntax
[Dynamic, Provider ("ProviderX")] 
class MyDerivedClass : MyClass
{
    [key] string sKey;
    [Implemented] sint32 ValueMethod();
    [Implemented] sint32 MyMethod ([in, Id(0)] sint32 Param);
};
```

限定詞可以分成標準限定詞、CIM 限定詞和唯一的限定詞，如下所示：

-   標準辨識符號

    標準限定詞是 WMI 所定義的辨識符號，通常用於 MOF 程式碼中。 例如， [**動態**](dynamic-qualifier.md) 和 [**讀取**](standard-qualifiers.md) 限定詞都是標準限定詞。 如需詳細資訊，請參閱 [WMI 限定詞](wmi-qualifiers.md)。

-   CIM 辨識符號

    CIM 辨識符號是 CIM 規格中包含的限定詞。 雖然在 MOF 程式碼中使用 CIM 辨識符號，但標準限定詞是特別針對 WMI 所設計。 如需詳細資訊，請參閱「DMTF [CIM」規格](https://www.dmtf.org/spec/cims.html/)。

-   唯一限定詞

    唯一限定詞是由類別提供者特別針對新類別所定義的辨識符號。 例如， [**單位**](standard-qualifiers.md) 限定詞是非標準的提供者特定限定詞。 您可以建立自己的限定詞來與提供者搭配使用。 如需建立提供者的詳細資訊，請參閱 [開發 WMI 提供者](developing-a-wmi-provider.md)。

無論您的辨識符號有哪些，您執行的主要程式是在您的 MOF 程式碼中使用辨識符號。 如需詳細資訊，請參閱套用 [限定詞](applying-a-qualifier.md)。 您可以進一步描述限定詞類別的辨識符號。 限定詞類別包含有關提供者如何使用限定詞的詳細資訊。 如需詳細資訊，請參閱描述限定詞類別的辨識 [符號](describing-a-qualifier-with-a-qualifier-flavor.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[設計受控物件格式 (MOF) 類別](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 



