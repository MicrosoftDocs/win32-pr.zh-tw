---
description: 受控物件格式 (MOF) 編譯器會使用兩種不同的批註分隔符號樣式來支援兩種形式的批註。
ms.assetid: 5ab71b45-7ed1-44c4-8710-6b833b0afb80
ms.tgt_platform: multiple
title: 建立批註
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 870833f1dbb86f53c7114c4e376af2b4882906ffe1b8cc10f5876bd2c80492e3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097338"
---
# <a name="creating-a-comment"></a>建立批註

受控物件格式 (MOF) 編譯器會使用兩種不同的批註分隔符號樣式來支援兩種形式的批註。

下表列出用於批註的分隔符號，以及分隔符號在程式碼中的效果。



| 分隔符號   | 標記                                                                                         |
|-------------|-----------------------------------------------------------------------------------------------|
| //          | 在行尾終止的批註開頭。                                    |
| /\* 和 \*/ | 批註的開頭和結尾可能橫跨多行，或只跨越某部分的行。 |



 

如同 C 和 c + + 程式設計語言，您必須只使用單一行批註的//分隔符號，但使用/ \* 和 \* /分隔符號搭配單行或多行批註。

下列程式碼範例描述兩個分隔符號樣式。

``` syntax
int32 MyProp = 2; // This is a comment until the line ends.
int32 /* This is a comment. */ MyProp = 2;
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[設計受控物件格式 (MOF) 類別](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 



