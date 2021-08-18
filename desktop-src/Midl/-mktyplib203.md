---
title: /mktyplib203 參數
description: /Mktyplib203 參數會強制 MIDL 編譯器剖析輸入檔。
ms.assetid: e1eddf03-db42-426e-bdf1-b7122b862756
keywords:
- /mktyplib203 參數 MIDL
topic_type:
- apiref
api_name:
- /mktyplib203
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc887560401986b9a7d5e0f0aa7c8b36d61874bf245a88ade7a149cd084f1ee3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014146"
---
# <a name="mktyplib203-switch"></a>/mktyplib203 參數

**/Mktyplib203** 參數會強制 MIDL 編譯器剖析輸入檔。

``` syntax
midl /mktyplib203
```

## <a name="switch-options"></a>切換選項

此參數沒有任何參數。

## <a name="remarks"></a>備註

為了使用 **/mktyplib203** 參數，輸入檔必須完全遵循 ODL 語法，這表示您不能將任何語句放在程式庫區塊之外。 範例

**midl/mktyplib203 myoldodl. odl**

**midl/mktyplib203 oldhabit .idl**

## <a name="see-also"></a>另請參閱

<dl> <dt>

[一般 MIDL 命令列語法](general-midl-command-line-syntax.md)
</dt> <dt>

[使用 MIDL 產生類型程式庫](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 




