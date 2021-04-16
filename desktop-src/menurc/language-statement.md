---
title: LANGUAGE 語句
description: 定義所有資源的語言，直到下一個語言語句或檔案結尾為止。
ms.assetid: 175e27e2-903a-4aaf-89ef-532166b167e8
keywords:
- 語言語句功能表與其他資源
topic_type:
- apiref
api_name:
- LANGUAGE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9563ba2ec00362a3b9caa3911a701919a81cae1e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104507911"
---
# <a name="language-statement"></a>LANGUAGE 語句

定義所有資源的語言，直到下一個 **語言** 語句或檔案結尾為止。

當 **LANGUAGE** 語句出現在 [**加速器**](accelerators-resource.md)、 [**DIALOGEX**](dialogex-resource.md)、 [**MENU**](menu-resource.md)、 [**RCDATA**](rcdata-resource.md)或 [**STRINGTABLE**](stringtable-resource.md) 資源定義的主體開頭之前，指定的語言只適用于該資源。

``` syntax
LANGUAGE language, sublanguage
```

<dl> <dt>

<span id="language"></span><span id="LANGUAGE"></span>*語言*
</dt> <dd>

語言識別項。

</dd> <dt>

<span id="sublanguage"></span><span id="SUBLANGUAGE"></span>*語言*
</dt> <dd>

子語言識別項。

</dd> </dl>

如需詳細資訊，請參閱 [語言識別項常數和字串](/windows/desktop/Intl/language-identifier-constants-and-strings)。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**加速器**](accelerators-resource.md)
</dt> <dt>

[**特徵**](characteristics-statement.md)
</dt> <dt>

[**功能表**](menu-resource.md)
</dt> <dt>

[**RCDATA**](rcdata-resource.md)
</dt> <dt>

[**STRINGTABLE**](stringtable-resource.md)
</dt> <dt>

[**版本**](version-statement.md)
</dt> </dl>

 

 