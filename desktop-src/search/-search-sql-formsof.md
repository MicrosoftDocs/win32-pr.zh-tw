---
description: FORMSOF 字詞會使用單字的其他語言形式來執行符合專案。
ms.assetid: b705b8bc-dc2c-4cee-8306-f494b0f96cbf
title: FORMSOF 字詞
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20504a7a36c7f0cb9c69b9513f33446501641bc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107000240"
---
# <a name="formsof-term"></a>FORMSOF 字詞

FORMSOF 字詞會使用單字的其他語言形式來執行符合專案。 以下是 FORMSOF 字詞語法：


```
FORMSOF (<generation_type>,<match_words>)
```



世代類型會指定 Microsoft Windows Search 如何選擇替代字組表單。 **字形變化** 值會選擇相符字組的替代變化表單。 如果單字是動詞，則會使用替代時態。 如果單字是名詞，則會使用單數、複數和所有格形式來偵測相符專案。

Match \_ 單字值是一或多個單字，以逗號分隔。

## <a name="examples"></a>範例

下列範例會搜尋 "run" 這個字的字形變化相符專案。 此範例符合包含 "run"、"run" 或 "run" 的檔。


```
...CONTAINS('FORMSOF(INFLECTIONAL,"run")')
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

**參考**
</dt> <dt>

[FREETEXT 述詞](-search-sql-freetext.md)
</dt> <dt>

[WHERE 子句](-search-sql-where.md)
</dt> </dl>

 

 



