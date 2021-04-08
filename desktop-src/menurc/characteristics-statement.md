---
title: 特性語句
description: 定義可供讀取和寫入資源定義檔的工具使用之資源的相關資訊。
ms.assetid: 07834b02-a36e-40cc-8907-bff6631842f3
keywords:
- 特性語句功能表和其他資源
topic_type:
- apiref
api_name:
- CHARACTERISTICS
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de681785fa2ec815b1edbdda913dd8032f8feb8e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104022454"
---
# <a name="characteristics-statement"></a>特性語句

定義可供讀取和寫入資源定義檔的工具使用之資源的相關資訊。 在編譯的 .res 檔中，會顯示指定的 **DWORD** 值與資源。 不過，此值不會儲存在可執行檔中，而且對系統沒有任何意義。

**特性** 語句會出現在 [**加速器**](accelerators-resource.md)、[**對話方塊**](dialog-resource.md)、[**功能表**](menu-resource.md)、 [**RCDATA**](rcdata-resource.md)或 [**STRINGTABLE**](stringtable-resource.md)資源定義的主體開頭之前。 指定的值僅適用于該資源。

``` syntax
CHARACTERISTICS dword
```

<dl> <dt>

<span id="dword"></span><span id="DWORD"></span>*Dword*
</dt> <dd>

使用者定義的 **DWORD** 值。

</dd> </dl>

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**加速器**](accelerators-resource.md)
</dt> <dt>

[**對話 框**](dialog-resource.md)
</dt> <dt>

[**語言**](language-statement.md)
</dt> <dt>

[**功能表**](menu-resource.md)
</dt> <dt>

[**RCDATA**](rcdata-resource.md)
</dt> <dt>

[**STRINGTABLE**](stringtable-resource.md)
</dt> </dl>

 

 




