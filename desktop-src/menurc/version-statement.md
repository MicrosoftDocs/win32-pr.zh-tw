---
title: VERSION 語句
description: 定義可供讀取和寫入資源檔的工具使用之資源的版本資訊。
ms.assetid: 3a33cff3-b8b3-43f4-b43a-ff1d1728cdc1
keywords:
- 版本語句功能表和其他資源
topic_type:
- apiref
api_name:
- VERSION
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c95f2af63d5c7bdb499d371892d0c2fa6ddb875fda5daf5b19fd0d188a478fa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776658"
---
# <a name="version-statement"></a>VERSION 語句

定義可供讀取和寫入資源檔的工具使用之資源的版本資訊。 指定的 *dword* 值會隨著資源出現在已編譯的中。RES 檔。 不過，此值不會儲存在可執行檔中，而且對系統沒有任何意義。

**版本** 語句會出現在 [**加速器**](accelerators-resource.md)、 [**DIALOGEX**](dialogex-resource.md)、[**功能表**](menu-resource.md)、 [**RCDATA**](rcdata-resource.md)或 [**STRINGTABLE**](stringtable-resource.md)資源定義的主體開頭之前。 指定的值僅適用于該資源。

``` syntax
VERSION dword
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

[**特徵**](characteristics-statement.md)
</dt> <dt>

[**語言**](language-statement.md)
</dt> <dt>

[**功能表**](menu-resource.md)
</dt> <dt>

[**RCDATA**](rcdata-resource.md)
</dt> <dt>

[**STRINGTABLE**](stringtable-resource.md)
</dt> </dl>

 

 




